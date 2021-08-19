---
title: Ajakirjete laiendamine
description: Selles teemas antakse teavet selle kohta, kuidas saavad arendajad saavad ajakirje juhtelementi laiendada.
author: stsporen
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c36a47b09e6012925a047f81318e89167d5c506facaae8d72b0bb6e8e267a7d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993326"
---
# <a name="extending-time-entries"></a>Ajakirjete laiendamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations sisaldab laiendatavat ajakirje kohandatud juhtelementi. See juhtelement hõlmab järgmiseid funktsioone.

- Aja horisontaalselt üle nädala sisestamine
- Päeva, rea või nädala kokkuvõtted
- Ridade või nädalate kopeerimine
- Aja sisestamine HH:mm või HH.hh kaudu (teisendab automaatselt valikule HH.hh)
- Importimine määramistest, broneeringutest või kohtumistest

Ajakirjete laiendamine on võimalik kahes valdkonnas.
- [Kohandatud ajakirjete lisamine oma tarbeks](#add)
- [Iganädalase ajakirje juhtelemendi kohandamine](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Kohandatud ajakirjete lisamine oma tarbeks

Ajakirjed on mitme stsenaariumi korral kasutatav olemi tuumik. 2020. aasta aprilli 1. laines võeti kasutusele TESA tuumiklahendus. TESA pakub olemit **Sätted** ja uut turberolli **Ajakirje kasutaja**. Lisaks kaasati uued väljad **msdyn_start** ja **msdyn_end**, millel on otsene seos väljaga **msdyn_duration**. Uus olem, turberoll ja väljad võimaldavad mitmete toodete üleselt ajale ühtsemat kähenemist.


### <a name="time-source-entity"></a>Ajaallika olem
| Väli | Kirjeldus | 
|-------|------------|
| Nimetus  | Ajakirje loomise ajal vaikeväärtusena kasutatav ajaallika olemi nimi. |
| Vaikimisi ajaallikas [Time Source: isdefault] | Vaikimisi saab vaikimisi märkida ainult ühe ajaallika. See võimaldab sisestada vaikimisi ajaallika, kui see pole määratletud. |
|Ajaallika tüüp [Time Source: sourcetype] | Allika tüüp on suvand (Ajakirje allika tüüp), mis võimaldab ajaallika seostamist rakendusega. Microsoft reserveerib väärtused, mis on suuremad kui 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Ajakirjed ja ajaallika olem
Sisestus seostatakse iga kord ajaallika kirjega. See kirje määratleb, kuidas ja millised rakendused peaksid ajakirjet töötlema.

Ajakirjed on alati ühe järjestikuses ajaplokis, kus algus, lõpp ja kestus on seotud.

Loogika uuendab automaatselt ajakirje kirjet järgmistel juhtudel.

- Kui esitatakse kaks kolmest järgmisest väljast, arvutatakse kolmas automaatselt. 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Väljad **msdyn_start** ja **msdyn_end** arvestavad ajavööndiga.
- Ajakirjed, mis on loodud ainult väärtustega **msdyn_date** ja **msdyn_duration** algavad keskööl. Välju **msdyn_start** ja **msdyn_end** värskendatakse vastavalt.

#### <a name="time-entry-types"></a>Ajakirje tüübid

Ajakirje kirjetega on seostatud tüüp, mis määratleb seostatud rakenduse esitamise voos käitumise.

|Silt | Väärtus|
|-----|-----|
|Vaheajal   |192,355,000|
|Reisi | 192,355,001|
|Ületunnitöö   | 192,354,320|
|Tööta   | 192,350,000|
|Puudumine    | 192,350,001|
|Puhkus   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Iganädalase ajakirje juhtelemendi kohandamine
Arendajad saavad lisada teistele olemitele täiendavaid välju ja otsinguid ning rakendada oma äristsenaariumide toetamiseks kohandatud ärireegleid.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Muude olemite otsingutega kohandatud väljade lisamine
Iganädalase ajakirje ruudustikku kohandatud välja lisamiseks on vaja läbi teha kolm etappi.

1. Lisage kohandatud väli kiirloomise dialoogiboksi.
2. Konfigureerige ruudustikku kohandatud välja kuvamiseks.
3. Lisage kohandatud väli kas rea või lahtri muutmise ülesande voogu.

Veenduge, et uuel väljal oleksid rea või lahtri muutmise ülesande voos olemas nõutud kinnitused. Selles etapis lukustage väli, võttes aluseks ajakirje oleku.

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Lisage kohandatud väli kiirloomise dialoogiboksi
Lisage kohandatud välj dialoogiboksi **Ajakirje kiirloomine**. Kui ajakirjed on sisestatud, saavad kasutajad sisestada väärtuse, valides suvandi **Uus**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigureerige ruudustikku kohandatud välja kuvamiseks
Iganädalase ajakirje ruudustikku kohandatud välja lisamiseks on kaks viisi.

  - Vaate kohandamine ja kohandatud välja lisamine
  - Uue vaikimisi kohandatud ajakirje loomine 


#### <a name="customize-a-view-and-add-a-custom-field"></a>Vaate kohandamine ja kohandatud välja lisamine

Kohandage vaadet **Minu iganädalased ajakirjed** ja lisage sinna kohandatud välja. Saate valida kohandatud välja asukoha ja suuruse ruudustikus, kui redigeerite vaates neid atribuute.

#### <a name="create-a-new-default-custom-time-entry"></a>Uue vaikimisi kohandatud ajakirje loomine

Peale nende veergude, mida soovite ruudustikus näha, peaks see vaade sisaldama ka välju **Kirjeldus** ja **Välised kommentaarid**. 

1. Valige ruudustiku asukoha, suuruse ja sortimise vaikejärjekorra, kui redigeerite vaates neid atribuute. 
2. Konfigureerige selle vaate kohandatud juhtelementi nii, et see oleks **Ajakirje ruudustiku** juhtelement. 
3. Lisage see juhtelement vaatesse ja valige see veebirakenduse, telefoni ja tahvelarvuti jaoks. 
4. Konfigureerige iganädalase ajakirje ruudustiku parameetrid. 
5. Seadke välja **Alguskuupäev** väärtuseks **msdyn_date**, välja **Kestus** väärtuseks **msdyn_duration** ja välja **Olek** väärtuseks **msdyn_entrystatus**. 
6. Vaikevaate jaoks on välja **Kirjutuskaitstud oleku loend** väärtuseks **192350002,192350003,192350004**. Välja **Tööülesande voo rea redigeerimine** väärtuseks on **msdyn_timeentryrowedit**. Välja **Tööülesande voo lahtri redigeerimine** väärtuseks on **msdyn_timeentryedit**. 
7. Saate neid välju kohandada kirjutuskaitstud oleku lisamiseks või eemaldamiseks või mõne muu ülesandepõhise kogemuse (TBX) kasutamiseks, et ridu või lahtreid redigeerida. Need väljad on nüüd seotud staatilise väärtusega.


> [!NOTE] 
> Mõlemad valikud eemaldavad olemistest **Projekt** ja **Projekti ülesanne** mõned valmisfiltreerimised, et kõik olemite otsinguvaated oleksid nähtavad. Valmiskujul, kuvatakse ainult asjakohased otsinguvaated.

Määrake kohandatud välja jaoks sobiv ülesandevoog. Kui lisasite välja ruudustikku, peaks see minema rea muutmise ülesande voogu, mida kasutatakse nende väljade jaoks, mida rakendatakse tervele ajakirjete reale. Kui kohandatud väljal on iga päev kordumatu väärtus (nt kohandatud väli **Lõppaja** jaoks), peaks see minema lahtri muutmise ülesande voogu.

Kohandatud välja lisamiseks ülesandevoogu lohistage **välja** element lehel sobivasse asukohta ja seadistage välja atribuudid. Seadke atribuudi **Allikas** väärtuseks **Ajakirje** ja atribuut **Andmeväli** kohandatud väljale. Atribuut **Väli** määrab TBX-i lehel kuvatava nime. Välja muudatuste salvestamiseks valife **Rakenda** ja valige seejärel **Värskenda**, et salvestada oma muudatused lehel.

Kui soovite kasutada uut kohandatud TBX-i lehte, looge uus protsess. Seadke kategooria väärtuseks **Äriprotsessi voog**, olemi väärtuseks **Ajakirje** ja äriprotsessi tüübi väärtuseks **Protsessi käivitamine ülesandevoona**. Jaotises **Atribuudid** tuleb atribuudi **Lehe nimi** väärtuseks seada lehe kuvatav nimi. Kõikide asjakohaste väljade lisamine TBX-i lehele. Salvestage ja aktiveerige protsess. Värskendage vastava töövoo kohandatud juhtelemendi atribuut protsessis väärtusele **Nimi**.

### <a name="add-new-option-set-values"></a>Uute suvandikomplekti väärtuste lisamine
Valmisväljale uute suvandikomplekti väärtuste lisamiseks avage välja redigeerimisleht ja valige jaotisest **Tüüp** suvandikomplekti kõrval olev käsk **Redigeeri**. Lisage uus suvand, millel on kohandatud silt ja värv. Kui soovite lisada uue ajakirje oleku, on valmisvälja nimi **Kirje olek**, mitte **Olek**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Uue ajakirje oleku määramine kirjutuskaitstuks
Selleks et määrata uue ajakirje olek kirjutuskaitstuks, lisage atribuudile **Kirjutuskaitstud olekuloend** uus ajakirje väärtus. Ajakirjete ruudustiku redigeeritav osa lukustatakse uue olekuga ridade jaoks.
Seejärel lisage ärireeglid, et lukustada kõik väljad TBX-i lehtedel **Ajakirje rea redigeerimine** ja **Ajakirje redigeerimine**. Saate nende lehtede ärireeglitele ligi, kui avate lehe äriprotsessi voo redaktori ja valite suvandi **Ärireeglid.** Saate lisada olemasolevate ärireeglite tingimusele uue oleku või uuele olekule uue ärireegli.

### <a name="add-custom-validation-rules"></a>Kohandatud valideerimisreeglite lisamine
Iganädalasele ajakirje ruudustiku kasutuskogemusele saav lisada kahte tüüpi valideerimise reegleid.

- Kliendipoolsed ärireeglid, mis töötavad kiirloomise dialoogiboksides ja TBX-lehtedel.
- Serveripoolse lisandmooduli valideerimised, mis kehtivad kõikidele ajakirjete värskendustele.

#### <a name="business-rules"></a>Ärireeglid
Ärireeglite abil saate välju lukustada ja avada, sisestada väljade vaikeväärtused ning määrata kinnitused, mis nõuavad ainult praeguse ajakirje kirje teavet. Saate TBX-i lehe ärireeglitele ligi, kui avate lehe äriprotsessi voo redaktori ja valite suvandi **Ärireeglid.** Saate redigeerida olemasolevaid ärireegleid või lisada uue ärireegli. Veelgi enam kohandatud kinnituste jaoks saate kasutada ärireeglit ka JavaScript käivitamiseks.

#### <a name="plug-in-validations"></a>Lisandmooduli kinnitused
Kasutage lisandmoodulite kinnitusi kõikide nende kinnituste jaoks, mis vajavad rohkem konteksti, kui on olemas ühes ajakirje kirjes, või nende kinnituste jaoks, mida soovite käivitada ruudustikus tekstisiseste värskenduste kohta. Valideerimise lõpuleviimiseks looge olemisse **Ajakirje** kohandatud lisandmoodul.

### <a name="copying-time-entries"></a>Ajakirjete kopeerimine
Kasutage vaadet **Kopeeri ajakirje veerge**, et määratleda ajavahemiku jooksul kopeeritavate väljade loend. Väljad **Kuupäev** ja **Kestus** on nõutavad ja neid ei tohi vaatest eemaldada.


[!INCLUDE[footer-include](../includes/footer-banner.md)]