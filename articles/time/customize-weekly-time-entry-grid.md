---
title: Ajakirjete laiendamine
description: See artikkel annab teavet selle kohta, kuidas saavad arendajad ajakirje juhtelementi laiendada.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914765"
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
Sisestus seostatakse iga kord ajaallika kirjega. See kirje määrab, millised rakendused peaksid aja sisestamist töötlema ja kuidas.

Ajakirjed on alati ühe järjestikuses ajaplokis, kus algus, lõpp ja kestus on seotud.

Loogika uuendab automaatselt ajakirje kirjet järgmistel juhtudel.

- Kui esitatakse kaks kolmest järgmisest väljast, arvutatakse kolmas automaatselt. 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- **msdyn_start** ja **msdyn_end** väljad arvestavad ajavööndiga.
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

1. Lisage kohandatud väli **kiirloomise** dialoogiboksi.
2. Konfigureerige ruudustikku kohandatud välja kuvamiseks.
3. Lisage kohandatud väli vastavalt vajadusele lehele **Rea redigeerimine** või **Ajakirje redigeerimine**.

Veenduge, et uuel väljal oleks lehel **Rea redigeerimine** või **Ajakirje redigeerimine**. Selle ülesande osana lukustage väli ajakirje oleku alusel.

Kui lisate ruudustikule **Ajakirje** kohandatud välja ja loote seejärel otse ruudustikus ajakirjed, määratakse nende kirjete kohandatud väli automaatselt nii, et see ühtib reaga. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Lisage kohandatud väli kiirloomise dialoogiboksi
Lisage kohandatud väli dialoogiboksi **Kiirloomine: ajakirje loomine**. Kasutajad saavad seejärel sisestada väärtuse, kui nad lisavad ajakirjeid, valides suvandi **Uus**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigureerige ruudustikku kohandatud välja kuvamiseks
**Iganädalase ajakirje** ruudustikku kohandatud välja lisamiseks on kaks viisi.

- Kohandage vaadet **Minu iganädalased ajakirjed** ja lisage sinna kohandatud välja. Saate täpsustada kohandatud välja asukoha ja suuruse ruudustikus, kui redigeerite vaates neid atribuute.
- Looge uus kohandatud ajakirje vaade ja seadke see vaikevaateks. Peale nende veergude, mida soovite ruudustikusse kaasata, peaks see vaade sisaldama ka välju **Kirjeldus** ja **Välised kommentaarid**. Saate täpsustada ruudustiku asukoha, suuruse ja sortimise vaikejärjekorra, kui redigeerite vaates neid atribuute. Seejärel konfigureerige selle vaate kohandatud juhtelementi nii, et see oleks **Ajakirje ruudustiku** juhtelement. Lisage juhtelement vaatesse ja valige see **Veebirakenduse**, **Telefoni** ja **Tahvelarvuti** jaoks. Seejärel konfigureerige **Iganädalase ajakirje** ruudustiku parameetrid. Seadke välja **Alguskuupäev** väärtuseks **msdyn\_date**, välja **Kestus** väärtuseks **msdyn\_duration** ja välja **Olek** väärtuseks **msdyn\_entrystatus**. **Kirjutuskaitstud olekuloendi** välja väärtuseks on seatud **192350002 (Kinnitatud)**, **192350003 (edastatud)** või **192350004 (Tagasikutsumine taotletud)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Kohandatud välja lisamine sobivale redigeerimise lehele
Lehed, mida kasutatakse ajakirje või ajakirjete rea redigeerimiseks, leiate jaotisest **Vormid**. Ruudustiku nupp **Kirje redigeerimine** avab lehe **Kirje redigeerimine** ja nupp **Rea redigeerimine** avab lehe **Rea redigeerimine**. Saate neid lehti redigeerida nii, et need sisaldaksid kohandatud välju.

Mõlemad valikud eemaldavad olemitest **Projekt** ja **Projekti ülesanne** mõned kastivälised filtreerimised nii, et kõik olemite otsinguvaated on nähtavad. Valmis, kuvatakse ainult asjakohased otsinguvaated.

Peate kohandatud välja jaoks määrama sobiva lehe. Kui lisasite välja ruudustikku, peaks see kõige tõenäolisemalt minema **Row edit** lehele, mida kasutatakse nende väljade jaoks, mida rakendatakse tervele ajakirjete reale. Kui kohandatud väljal on iga päev real kordumatu väärtus (näiteks kui see on lõppaja kohandatud väli), peaks see minema lehele **Ajakirje redigeerimine**.

Kohandatud välja lehele lisamiseks lohistage **Välja** element lehel sobivasse asukohta ja seadistage selle atribuudid.

### <a name="add-new-option-set-values"></a>Uute suvandikomplekti väärtuste lisamine
Valikute komplekti väärtuste lisamiseks kastivälisele väljale järgige neid samme.

1. Avage välja redigeerimisleht ja seejärel valige jaotisest **Tüüp** suvandikomplekti kõrval olev käsk **Redigeeri**.
2. Lisage uus suvand, millel on kohandatud silt ja värv. Kui soovite lisada uue ajakirje oleku, on kastivälise välja nimi **Kirje olek**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Uue ajakirje oleku määramine kirjutuskaitstuks
Selleks et määrata uue ajakirje olek kirjutuskaitstuks, lisage atribuudile **Kirjutuskaitstud olekuloend** uus ajakirje väärtus. Lisage kindlasti number, mitte silt. Ajakirjete ruudustiku redigeeritav osa lukustatakse nüüd uue olekuga ridade jaoks. Atribuudi **Kirjutuskaitstud olekuloend** eri vaadete **Ajakirje** ruudustik **Ajakirje** jaoks erinevalt seadistamiseks lisage vaate jaotisesse **Kohandatud juhtelemendid** ja konfigureerige parameetreid vastavalt vajadusele.

Seejärel lisage ärireeglid, et lukustada kõik väljad TBX-i lehtedel **Rea redigeerimine** ja **Ajakirje redigeerimine**. Nende lehtede ärireeglitele juurdepääsemiseks avage iga lehe väljaredaktor ja seejärel valige **Ärireeglid**. Saate lisada olemasolevate ärireeglite tingimusele uue oleku või uuele olekule uue ärireegli.

### <a name="add-custom-validation-rules"></a>Kohandatud valideerimisreeglite lisamine
Ruudustiku **Nädalase ajakirje** jaoks saate lisada kahte tüüpi kinnitamisreegleid.

- Lehtedel töötavad kliendipoolsed ärireeglid
- Serveripoolse lisandmooduli valideerimised, mis kehtivad kõikidele ajakirjete värskendustele

#### <a name="client-side-business-rules"></a>Kliendipoolsed ärireeglid
Ärireeglite abil saate välju lukustada ja avada, sisestada väljade vaikeväärtused ning määrata kinnitused, mis nõuavad ainult praeguse ajakirje kirje teavet. Lehe ärireeglitele juurdepääsemiseks avage väljaredaktor ja seejärel valige **Ärireeglid**. Saate redigeerida olemasolevaid ärireegleid või lisada uue ärireegli.

#### <a name="server-side-plug-in-validations"></a>Serveripoolse lisandmooduli kinnitamised
Peaksite kasutama lisandmoodulite kinnitusi kõikide nende kinnituste jaoks, mis vajavad rohkem konteksti, kui on olemas ühes ajakirje kirjes. Peaksite neid kasutama ka kõigi kinnitamiste jaoks, mida soovite ruudustikus sisemiste värskenduste puhul käivitada. Kinnituste lõpuleviimiseks looge olemisse **Ajakirje** kohandatud lisandmoodul.

### <a name="limits"></a>Limiidid
Praegu on ruudustiku **Ajakirje** mahupiirang 500 rida. Kui ridu on rohkem kui 500, siis üleliigseid ridu ei kuvata. Seda mahupiirangut ei saa kuidagi suurendada.

### <a name="copying-time-entries"></a>Ajakirjete kopeerimine
Kasutage vaadet **Kopeeri ajakirje veerge**, et määratleda ajavahemiku jooksul kopeeritavate väljade loend. Väljad **Kuupäev** ja **Kestus** on nõutavad ja neid ei tohi vaatest eemaldada.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
