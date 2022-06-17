---
title: Rakendage mobiilirakenduse Microsoft Dynamics 365 Project Timesheet iOS-i ja Androidi kohandatud väljad
description: Selles artiklis on toodud levinud mustrid laienduste kasutamiseks kohandatud väljade rakendamiseks.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 03b79d58d1f91e07034b8c9efb408e6d7a9c29a8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913707"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Rakendage mobiilirakenduse Microsoft Dynamics 365 Project Timesheet iOS-i ja Androidi kohandatud väljad

[!include [banner](../includes/banner.md)]

Selles artiklis on toodud levinud mustrid laienduste kasutamiseks kohandatud väljade rakendamiseks. Käsitletakse järgmisi artikleid:

- Erinevad andmetüübid, mida kohandatud väljaraamistik toetab
- Kuidas kuvada kirjutuskaitstud või redigeeritavaid välju ajatabeli kirjetesse ja salvestada kasutaja esitatud väärtused tagasi andmebaasi
- Ajatabeli päises kirjutuskaitstud väljade kuvamine
- Muu kohandatud äriloogika integreerimine väljadele vaikeväärtuste sisestamiseks ja täiendavaks valideerimiseks

## <a name="audience"></a>Publik

See artikkel on mõeldud arendajatele, kes integreerivad oma kohandatud väljad mobiilirakendusse Microsoft Dynamics 365 Project Timesheet, mis on saadaval Apple iOS-ile ja Google'ile Android. Eeldame, et lugejad tunnevad X + + arenduse ja projekti ajatabeli funktsioone.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Andmete leping – TSTimesheetCustomField X++ klass

Klass **TSTimesheetCustomField** on X++ andmete lepingu klass, mis esindab teavet kohandatud välja kohta ajatabeli toimimise jaoks. Kohandatud välja objektide loendid edastatakse nii TSTimesheetDetails kui ka TSTimesheetEntry, et kuvada mobiilirakenduse kohandatud välju.

- **TSTimesheetDetails** – ajatabeli päise leping.
- **TSTimesheetEntry** – ajatabeli kande leping. Nende objektide rühmad, millel on sama projekti teave ja **timesheetLineRecId,** moodustavad rea.

### <a name="fieldbasetype-types"></a>fieldBaseType (Types)

Atribuut **FieldBaseType** objektil **TsTimesheetCustom** määratleb rakenduses kuvatava välja tüübi. Toetatakse järgmisi **Tüüpide** väärtusi.

| Tüüpide väärtus | Tüüp              | Märkmed |
|-------------|-------------------|-------|
| 0           | String (ja loetelu) | Väli kuvatakse tekstiväljana. |
| 1           | Integer           | Väärtus kuvatakse arvuna ilma kümnendkohtadeta. |
| 2           | Reaalarv              | Väärtus kuvatakse arvuna, millel on kümnendkohad.<p>Tegeliku väärtuse kuvamiseks rakenduses valuutana kasutage **fieldExtenededType** atribuuti. Atribuudi **numberOfDecimals** abil saate määrata kuvatavate kümnendkohtade arvu.</p> |
| 3           | Kuupäev              | Kuupäeva vormingud on määratletud kasutaja **Kuupäeva, kellaaja ja arvuvormingu** sättega, mis on määratud **Keele ja riigi/regiooni eelistuste** all **Kasutajasuvandites**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Kui **stringOptions** atribuuti pole **TSTimesheetCustomField** objektil, pakutakse kasutajale vabas kirjas tekstivälja.

    Atribuuti **stringLength** saab kasutada maksimaalse stringi pikkuse seadmiseks, mida kasutajad saavad sisestada.

- Kui atribuut **stringOptions** on esitatud **TSTimesheetCustomField** objektil, on need loendi elemendid ainsad väärtused, mida kasutajad saavad valida valikunuppude (raadionuppude) abil.

    Sellisel juhul võib väljal string olla loendiväärtus kasutaja kirje eesmärgil. Kui soovite väärtuse andmebaasi nuumväärtusena salvestada, vastendage stringi väärtus enne loendisse salvestamist käsitsi käsuliini abil (vt klassi TSTimesheetEntryService käsuahelat ajatabeli kirje salvestamiseks rakendusest tagasi andmebaasi" jaotisest, mis on selle artikli hilisemas osas).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Seda atribuuti saate kasutada tegelike väärtuste vormindamiseks valuutana. See lähenemine on kohaldatav ainult juhul, kui **fieldBaseType** väärtus on **Real**.

- **TSCustomFieldExtendedType:None** – vormingut ei rakendata.
- **TSCustomFieldExtendedType::Currency** – vormindage väärtus valuutana.

    Kui valuutavorming on aktiivne, saab **stringValue** välja abil edastada valuutakoodi, mis tuleb rakenduses kuvada. Väärtus on kirjutuskaitstud väärtus.

    Välin **realValue** sisaldab rahasummat, mis tuleb andmebaasi salvestada.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Selle atribuudi abil saate määrata, kus rakendus peaks kuvama kohandatud välja.

- **TSCustomFieldSection::Header** – väli kuvatakse rakenduse jaotises **Kuva rohkem üksikasju**. Need väljad on alati kirjutuskaitstud.
- **TSCustomFieldSection::Line** – väli kuvatakse pärast valmis välju ajatabeli kirjetes. Neid välju saavad olla redigeeritavad või kirjutuskaitstud.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

See atribuut määratleb välja, kui rakenduse pakutavad väärtused on andmebaasi tagasi salvestatud.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

See atribuut määratleb välja, kui rakenduse pakutavad väärtused on andmebaasi tagasi salvestatud.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Määrake selle atribuudi väärtuseks **Jah**, kui soovite, et kasutajad saavad redigeerida välja ajatabeli kirje jaotises. Määrake atribuudi väärtuseks **Ei**, et väli oleks kirjutuskaitstud.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Määrake selle atribuudi väärtuseks **Jah**, kui soovite, et väli ajatabeli kirje jaotises on kohustuslik.

### <a name="label-str"></a>label (str)

See atribuut määrab sildi, mis kuvatakse rakenduses välja kõrval.

### <a name="stringoptions-list-of-strings"></a>stringOptions (List of Strings)

See atribuut rakendub ainult juhul, kui välja **fieldBaseType** väärtuseks on seatud **String**. Kui **stringOptions** on seatud, siis stringi väärtused, mis on saadaval valikunuppude (raadionuppude) kaudu, määratakse loendis olevate stringide järgi. Kui stringe ei pakuta, on stringiväljale vabas vormis kirje lubatud (vt näiteks selle artikli hilisemas artiklis jaotist "TSTimesheetEntryService'i käsuliini kasutamine ajatabeli kirje salvestamiseks rakendusest tagasi andmebaasi").

### <a name="stringlength-int"></a>stringLength (int)

See atribuut määrab stringi välja maksimumpikkuse. See rakendub ainult juhul, kui välja **fieldBaseType** väärtuseks on seatud **String**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

See atribuut määrab tegeliku välja jaoks kuvatavate kümnendkohtade arvu. See rakendub ainult juhul, kui välja **fieldBaseType** väärtuseks on seatud **Real**.

### <a name="ordersequence-int"></a>orderSequence (int)

See atribuut kontrollib, millises järjestuses kuvatakse kohandatud väljad rakenduses, kui määratud on rohkem kui üks kohandatud väli. Väiksema arvuga väljad kuvatakse esimesena.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

**Boolean** tüüpi väljade korral edastab see atribuut serveri ja rakenduse vahel oleva välja loogikaväärtuse.

### <a name="guidvalue-guid"></a>guidValue (guid)

**GUID** tüüpi väljade korral edastab see atribuut serveri ja rakenduse vahel oleva välja globaalse ainuidentifikaatori (GUID) väärtuse.

### <a name="int64value-int64"></a>int64Value (int64)

**Int64** tüüpi välja korral edastab see atribuut serveri ja rakenduse vahel oleva välja int64 väärtuse.

### <a name="intvalue-int"></a>intValue (int)

**Int** tüüpi välja korral edastab see atribuut serveri ja rakenduse vahel oleva välja int-väärtuse.

### <a name="realvalue-real"></a>realValue (real)

**Reaalarv** tüüpi välja korral edastab see atribuut serveri ja rakenduse vahel oleva välja reaalarvuväärtuse.

### <a name="stringvalue-str"></a>stringValue (str)

**String** tüüpi välja korral edastab see atribuut serveri ja rakenduse vahel oleva välja stringiväärtuse. Seda kasutatakse ka **Reaalarvu** tüüpi väljadel, mis on vormindatud valuutana. Nende väljade jaoks kasutatakse atribuuti valuutatähise edastamiseks rakendusse.

### <a name="datevalue-date"></a>dateValue (date)

**Kuupäev** tüüpi välja korral edastab see atribuut serveri ja rakenduse vahel oleva välja kuupäevaväärtuse.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Kohandatud välja kuvamine ja salvestamine ajatabeli kirje jaotises

Allpool on pilt mobiilirakendusest ajatabeli kirje loomise kohta. See näitab valmis välju ja kohandatud välja jaotises Ajakanne nimega Teststring, mille loeteluväärtus Teine variant on juba seatud.

![Teststringi kohandatud väli rakenduses.](media/timesheet-entry.jpg)



Allpool on pilt mobiilirakenduse kasutajast, kes valib ühe loetelusuvanditest, mis on saadaval Testistringi kohandatud välja jaoks.  Kaks valikut Esimene valik ja Teine valik on kuvatud raadionuppudena. Teine suvand on praegu valitud.

![Teststringi kohandatud välja valikunupud (raadionupud).](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Laiendage TSTimesheetLine tabelit, et sellel oleks kohandatud väli

Tüüpilistes stsenaariumides salvestatakse tõenäoliselt ajatabeli kirje jaotises kohandatud välja andmed TSTimesheetLine tabelisse. Kuid muid tabeleid saab kasutada juhul, kui andmete toomisel lähtutakse TSTimesheetTrans kirjest, mis on esitatud või millel pole kindlat kirje konteksti (näiteks juhul, kui see väli on seatud projekti parameetrites kirjutuskaitstuks).

Pange tähele, et kohandatud väljadel ei pea olema andmebaasi kirjete varundamist. Neid saab dünaamiliselt genereerida X++ loogika põhjal. See lähenemine võib olla kasulik kirjutuskaitstud stsenaariumides (vt jaotist "TSTimesheetDetails klassis käsuahela kasutamine, buildCustomFieldListForHeader meetod, et täita ajatabeli üksikasjad" dünaamiliselt loodud kohandatud väljaväärtuste näitena.)

Allpool on ekraanipilt Visual Studio rakendusobjektide puust. See näitab TSTimesheetLine tabeli laiendust, mille väli TestLineString on lisatud kohandatud väljana.

![Reastring.](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Kasutage TSTimesheetSettings klassi buildCustomFieldList meetodi käsuahelat, et kuvada väli ajatabeli kirje jaotises

See kood reguleerib rakenduses välja kuvasätted. Näiteks kontrollib see väljatüüpi, silti, olenemata sellest, kas väli on kohustuslik ja millises jaotises väli kuvatakse.

Järgmises näites on kuvatud stringiväli ajakannetes. Sellel väljal on kaks suvandit, **Esimene suvand** ja **Teine suvand**, mis on saadaval valikunuppude (raadionupud) kaudu. Rakenduse väli on seostatud **TestLineString** väljaga, mis lisatakse tabelisse TSTimesheetLine.

Pange tähele **TSTimesheetCustomField::newFromMetatdata()** meetodi kasutamist kohandatud väljaatribuutide lähtestamise lihtsustamiseks: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** ja **numberOfDecimals**. Soovi korral saate need parameetrid määrata ka käsitsi.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Kasutage TSTimesheetEntry klassi buildCustomFieldListForEntry meetodi käsuahelat, et sisestada väärtused ajatabeli kirjesse

**buildCustomFieldListForEntry** meetodi abil sisestatakse mobiilirakenduses salvestatud ajatabeli ridadele väärtused. See võtab TSTimesheetTrans kirjet parameetrina. Selle kirje välju saab kasutada rakenduse kohandatud välja väärtuse täitmiseks.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>TSTimesheetEntryService klassis saate kasutada käsuliini, et salvestada ajatabeli kirje rakendusest tagasi andmebaasi.

Kohandatud välja salvestamiseks tagasi andmebaasi tüüpilises kasutuses peate laiendama mitut viisi.

- **timesheetLineNeedsUpdating** meetodit kasutatakse selleks, et teha kindlaks, kas kasutaja on rakenduses muutnud reakirjet ja see tuleb salvestada andmebaasi. Kui jõudlus pole mure, saab seda meetodit lihtsustada, et see tagastaks alati väärtuse **tõene**.
- **populateTimesheetLineFromEntryDuringCreate** ja **populateTimesheetLineFromEntryDuringUpdate** meetodeid saab laiendada nii, et nad sisestavad väärtused TSTimesheetLine-i andmebaasikirjesse esitatud TSTimesheetEntry andmete lepingukirjest. Järgnevas näites märkate, et andmebaasi välja ja kirje välja vastendamine toimub käsitsi X++ koodi kaudu.
- **populateTimesheetWeekFromEntry** meetodit saab pikendada ka juhul, kui **TSTimesheetEntry** objektile vastendatud kohandatud väli peab kirjutama tagasi TSTimesheetLineweek andmebaasi tabelisse.

> [!NOTE]
> Järgmises näites salvestatakse **firstOption** või **secondOption** väärtus, mille kasutaja valib andmebaasile töötlemata stringi väärtusena. Kui andmebaasi väli on **loendi** tüüpi väli, saab neid väärtusi käsitsi vastendada loendi väärtusega ja salvestada seejärel andmebaasi tabeli väljale loend.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Kohandatud välja kuvamine ajatabeli päise jaotises

Allpool on pilt mobiilirakenduse kasutajast, kes vaatab ajatabelit. Ülemises parempoolses nurgas on valitud nupp Rohkem teavet, et kuvada suvandit Kuva rohkem üksikasju.  

![Käsk Kuva rohkem üksikasju.](media/show-more.png)

Allpool on pilt mobiilirakendusest, kus kuvatakse ajatabeli jaotist Rohkem. Kohandatud väli nimega "Selle ajatabeli kasutamise määr (arvutatud kohandatud väli)" on lisatud ajatabeli päise jaotisse. Kohandatud väljale seatakse kirjutuskaitstud väärtus 0,667.

![Jaotis Rohkem.](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Laiendage TSTimesheetTable tabelit, et sellel oleks kohandatud väli

Tüüpilistes stsenaariumides tõmmatakse tõenäoliselt päise jaotise kohandatud välja andmed TSTimesheetHeader tabelist. Kuid muid tabeleid saab kasutada juhul, kui andmete toomisel lähtutakse TSTimesheetTable kirjest, mis on esitatud või millel pole kindlat kirje konteksti (näiteks juhul, kui see väli on seatud projekti parameetrites kirjutuskaitstuks).

Pange tähele, et kohandatud väljadel ei pea olema andmebaasi kirjete varundamist. Neid saab dünaamiliselt genereerida X++ loogika põhjal. Järgnev näide näitab seda lähenemist.

Päise jaotise väljad on rakenduses alati kirjutuskaitstud.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Kasutage TSTimesheetSettings klassi buildCustomFieldList meetodi käsuliini, et kuvada väli ajatabeli päise jaotises

See kood reguleerib rakenduses välja kuvasätted. Näiteks kontrollib see väljatüüpi, silti, olenemata sellest, kas väli on kohustuslik ja millises jaotises väli kuvatakse.

Järgmises näites kuvatakse arvutatud väärtus rakenduse päisejaotises.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Kasutage TSTimesheetDetails klassi buildCustomFieldListForHeader meetodi käsuliini, et sisestada väärtused ajatabeli üksikasjadesse

**buildCustomFieldListForHeader** meetodi abil sisestatakse mobiilirakendusse ajatabeli päise üksikasjad. See võtab TSTimesheetTable kirjet parameetrina. Selle kirje välju saab kasutada rakenduse kohandatud välja väärtuse täitmiseks. Järgmises näites ei loeta andmebaasist ühtegi väärtust. Selle asemel kasutatakse X++ loogikat, et luua arvutatud väärtus, mis kuvatakse rakenduses.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Muud konfigureerimise/laiendatavuse võimalused

### <a name="adding-additional-validation-for-the-app"></a>Rakendusele täiendava valideerimise lisamine

Ajatabeli funktsionaalsuse andmebaasi taseme olemasolev loogika töötab endiselt ootuspäraselt. Salvestamise või edastamise lõpuleviimise katkestamiseks ja kindla tõrketeate kuvamiseks saate lisada koodile **tõrketeate ("sõnum kasutajale")** käsulaienduste liini kaudu. Siin on kasulike laiendusmeetodite kolm näidet.

- Kui **validateWrite** TSTimesheetLine tabelis tagastab väärtuse **vale** ajatabeli rea salvestamisel, kuvatakse mobiilirakenduses tõrketeade.
- Kui **validateSubmit** TSTimesheetTable tabelis tagastab väärtuse **vale** ajatabeli rea salvestamisel rakenduses, kuvatakse kasutajale tõrketeade.
- Loogika, mis täidab väljad (näiteks **Reaatribuut**) **sisestamise** meetodi ajal TSTimesheetLine tabelisse toimib ikka.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Valmis väljade peitmine ja märkimine konfiguratsiooni kaudu kirjutuskaitstuks

Mobiilirakenduses saate projektiparameetrites teha valmisväljad kirjutuskaitstuks või peidetuks. Seadistage suvandid jaotise **Mobiili ajatabelid** vahekaardi **Ajatabel** lehel **Projekti haldamise ja raamatupidamise parameetrid**.

![Projekti parameetrid.](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Laienduste kaudu valimiseks saadaolevate tegevuste muutmine

Projekti jaoks valimiseks saadaolevad tegevused täidetakse meetodite **getActivitiesForProject()** ja **getActivityQuery()** abil **TsTimesheetProjectService** klassis. Võite kasutada käsuahelat, et muuta seda käitumist vastavalt teie äristsenaariumile tegevuste jaoks, mis on saadaval valimiseks mõne kindla projekti jaoks.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Vaikimisi projekti kategooria sisestamine ajatabeli kirjetele

Vaikimisi projekti kategooria sisestamine ajatabeli kirjetele toimub kolmel tasemel. Saate kasutada käsuahelat, et laiendada käitumist mis tahes või kõigil nendel tasemetel, et saavutada soovitud käitumist. Kasutatakse järgmist hierarhiat.

1. Rakendus proovib panna vaikimisi kategooria projekti ressursist. See vaikekategooria seatakse **getCurrentUserResource** ja **getDelegatedResourcesForCurrentUser** meetodite kaudu klassis **TSTimesheetSettingsService**.
2. Kui vaikekategooriat ei pakuta projektiressursi tasemel, proovib rakendus seda projektitegevusest tõmmata. See vaikekategooria seatakse meetodis **getActivitiesForProject** klassis **TSTimesheetProjectService**.
3. Kui vaikekategooriat ei pakuta projektitegevuse tasemel, võetakse vaikekategooria projektiparameetritest. See vaikekategooria seatakse meetodis **getProjectDetailsbyRule** klassis **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]