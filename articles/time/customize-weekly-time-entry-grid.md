---
title: Ajakirjete laiendamine
description: Selles teemas antakse teavet selle kohta, kuidas saavad arendajad saavad ajakirje juhtelementi laiendada.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930875"
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

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Kohandatud ajakirjete lisamine oma tarbeks.

Ajakirjed on olemi tuumik, mis on mõeldud mitme stsenaariumi jaoks kasutamiseks. 2020. aasta aprilli 1. laines võeti kasutusele TESA tuumiklahendus, mis pakub olemit **Säätted** ja uut turberolli **Ajakirje kasutaja**. Lisaks kaasati uued väljad **msdyn_start** ja **msdyn_end**, millel on otsene seos väljaga **msdyn_duration**. Uus olem, turberoll ja väljad võimaldavad mitmete toodete üleselt ajale ühtsemat kähenemist.


### <a name="time-source-entity"></a>Aja lähteolem
| Väli | Kirjeldus | 
|-------|------------|
| Nimetus  | Ajakirje loomise ajal vaiku väärtusena kasutatav ajaallika kirje nimi. |
| Vaikimisi ajaallikas [Time Source: isdefault] | Vaikimsii saab vaikimisi ajaallika juures märkida ainult ühe ajaallika. See võimalus võimaldab sisestada vaikimisi ajaallika, kui see pole määratletud. |
|Ajaallika tüüp [Time Source: sourcetype] | Allika tüüp on suvand (Ajakirje allika tüüp), mis võimaldab ajaallika seostamist rakendusega. Sellele suvandikomplekt lisatakse täiendavad väärtused lisarakenduste lisamisel. Pange tähele, et Microsoft reserveerib väärtused, mis on suuremad kui 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Ajakirjed ja ajaallika olem
Sisestus seostatakse iga kord ajaallika kirjega. See kirje määratleb, kuidas ja millised rakendused peaksid ajakirjet töötlema.

Ajakirjed on alati ühe järjestikuses ajaplokis, kus algus, lõpp ja kestus on seotud.

Loogika uuendab automaatselt ajakirje kirjet järgmistel juhtudel.

- Kui esitatakse kaks kolmest järgmisest väljast, arvutatakse kolmas automaatselt 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Väljad **msdyn_start** ja **msdyn_end** arvestavad ajavööndiga.
- Ajakirjed, mis on loodud ainult määratletud väljadega **msdyn_date** ja **msdyn_duration**, algavad keskööl, ja **msdyn_start** ja **msdyn_end** värskendatakse vastavalt.

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

- Lisage kohandatud väli kiirloomise dialoogiboksi.
- Konfigureerige ruudustikku kohandatud välja kuvamiseks.
- Lisage kohandatud väli kas rea või lahtri muutmise ülesande voogu.

Samuti peate veenduma, et uuel väljal oleksid rea või lahtri muutmise ülesande voos olemas nõutud kinnitused. Selles etapis peate ka välja lukustama, võttes aluseks ajakirje oleku.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Lisage kohandatud väli kiirloomise dialoogiboksi
Peate lisama kohandatud välja dialoogiboksi **Ajakirje kiirloomine**. Kasutajad saavad seejärel sisestada väärtuse, kui nad lisavad ajakirjeid, valides suvandi **Uus**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigureerige ruudustikku kohandatud välja kuvamiseks
Iganädalase ajakirje ruudustikku kohandatud välja lisamiseks on kaks viisi.

  - Vaate kohandamine ja kohandatud välja lisamine
  - Uue vaikimisi kohandatud ajakirje loomine 


**Vaate kohandamine ja kohandatud välja lisamine**

Saate kohandada vaadet **Minu iganädalased ajakirjed** ja lisada sinna kohandatud välja. Saate valida kohandatud välja asukoha ja suuruse ruudustikus, kui redigeerite vaates neid atribuute.

**Uue vaikimisi kohandatud ajakirje loomine** 

Peale nende veergude, mida soovite ruudustikus näha, peaks see vaade sisaldama ka välju **Kirjeldus** ja **Välised kommentaarid**. 

1. Valige ruudustiku asukoha, suuruse ja sortimise vaikejärjekorra, kui redigeerite vaates neid atribuute. 
2. Konfigureerige selle vaate kohandatud juhtelementi nii, et see oleks **Ajakirje ruudustiku** juhtelement. 
3. Lisage see juhtelement vaatesse ja valige see veebirakenduse, telefoni ja tahvelarvuti jaoks. 
4. Konfigureerige iganädalase ajakirje ruudustiku parameetrid. Seadke välja **Alguskuupäev** väärtuseks **msdyn_date**, välja **Kestus** väärtuseks **msdyn_duration** ja välja **Olek** väärtuseks **msdyn_entrystatus**. 
5. Vaikevaate jaoks on välja **Kirjutuskaitstud olekuloendi** väärtuseks seatud **192350002, 192350003, 192350004**, välja **Rea muutmise ülesande voog** väärtuseks **msdyn_timeentryrowedit** ja välja **Lahtri muutmise ülesande voog** väärtuseks **msdyn_timeentryedit**. 
6. Saate neid välju kohandada kirjutuskaitstud oleku lisamiseks või eemaldamiseks või mõne muu ülesandepõhise kogemuse (TBX) kasutamiseks, et ridu või lahtreid redigeerida. Need väljad peaksid olema seotud staatilise väärtusega.


> [!NOTE] 
> Mõlemad valikud eemaldavad olemistest **Projekt** ja **Projekti ülesanne** mõned valmisfiltreerimised, et kõik olemite otsinguvaated oleksid nähtavad. Valmiskujul, kuvatakse ainult asjakohased otsinguvaated.
Peate kohandatud välja jaoks määrama sobiva ülesandevoo. Kui lisasite välja ruudustikku, peaks see kõige tõenäolisemalt minema rea muutmise ülesande voogu, mida kasutatakse nende väljade jaoks, mida rakendatakse tervele ajakirjete reale. Kui kohandatud väljal on iga päev kordumatu väärtus (nt kohandatud väli **Lõppaja** jaoks), peaks see minema lahtri muutmise ülesande voogu.

Kohandatud välja lisamiseks ülesandevoogu lohistage **välja** element lehel sobivasse asukohta ja seadistage välja atribuudid. Seadke atribuudi **Allikas** väärtuseks **Ajakirje** ja atribuut **Andmeväli** kohandatud väljale. Atribuut **Väli** määrab TBX-i lehel kuvatava nime. Välja muudatuste salvestamiseks valife **Rakenda** ja valige seejärel **Värskenda**, et salvestada oma muudatused lehel.

Kui soovite kasutada uut kohandatud TBX-i lehte, looge uus protsess. Seadke kategooria väärtuseks **Äriprotsessi voog**, olemi väärtuseks **Ajakirje** ja äriprotsessi tüübi väärtuseks **Protsessi käivitamine ülesandevoona**. Jaotises **Atribuudid** tuleb atribuudi **Lehe nimi** väärtuseks seada lehe kuvatav nimi. Kõikide asjakohaste väljade lisamine TBX-i lehele. Salvestage ja aktiveerige protsess ning seejärel värskendage vastava töövoo kohandatud juhtelemendi atribuut protsessis väärtusele **Nimi**.

### <a name="add-new-option-set-values"></a>Uute suvandikomplekti väärtuste lisamine
Valmisväljale uute suvandikomplekti väärtuste lisamiseks avage välja redigeerimisleht ja seejärel valige jaotisest **Tüüp** suvandikomplekti kõrval olev käsk **Redigeeri**. Seejärel lisage uus suvand, millel on kohandatud silt ja värv. Kui soovite lisada uue ajakirje oleku, on valmisvälja nimi **Kirje olek**, mitte **Olek**.

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
Peaksite kasutama lisandmoodulite kinnitusi kõikide nende kinnituste jaoks, mis vajavad rohkem konteksti, kui on olemas ühes ajakirje kirjes, või nende kinnituste jaoks, mida soovite käivitada ruudustikus tekstisiseste värskenduste kohta. Valideerimise lõpuleviimiseks looge olemisse **Ajakirje** kohandatud lisandmoodul.
