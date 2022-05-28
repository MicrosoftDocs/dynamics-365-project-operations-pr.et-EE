---
title: Ajakirjete laiendamine
description: Selles teemas antakse teavet selle kohta, kuidas saavad arendajad saavad ajakirje juhtelementi laiendada.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582981"
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
Sisestus seostatakse iga kord ajaallika kirjega. See kirje määratleb, millised rakendused peaksid ajakirjet töötlema ja kuidas.

Ajakirjed on alati ühe järjestikuses ajaplokis, kus algus, lõpp ja kestus on seotud.

Loogika uuendab automaatselt ajakirje kirjet järgmistel juhtudel.

- Kui esitatakse kaks kolmest järgmisest väljast, arvutatakse kolmas automaatselt. 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Väljad **msdyn_start** ja **msdyn_end** on ajavööndist teadlikud.
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

1. Lisage kohandatud väli **dialoogiboksi Kiirloomine**.
2. Konfigureerige ruudustikku kohandatud välja kuvamiseks.
3. Lisage kohandatud väli vastavalt vajadusele **lehele Rea redigeerimine** või **kellaaja sisestamise redigeerimine**.

Veenduge, et uuel väljal **oleksid lehel Rea redigeerimine** või **ajakirje redigeerimine** nõutavad valideerimised. Selle ülesande osana lukustage väli ajakande oleku põhjal.

Kui lisate ajasisestuse **ruudustikku kohandatud välja** ja loote seejärel ajakirjed otse ruudustikus, seatakse nende kannete kohandatud väli automaatselt nii, et see vastaks reale. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Kohandatud välja lisamine dialoogiboksi Kiirloomine
Lisage kohandatud väli dialoogiboksi Kiirloomine **: Ajasisestuse loomine**. Kasutajad saavad seejärel sisestada väärtuse, kui nad lisavad ajakirjeid, valides suvandi **Uus**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigureerige ruudustikku kohandatud välja kuvamiseks
Kohandatud välja **lisamiseks nädalaaja sisestamise** ruudustikku on kaks võimalust.

- Kohandage vaadet **Minu nädalaajakirjed** ja lisage sellele kohandatud väli. Kohandatud välja asukoha ja suuruse ruudustikus saate määrata vaate atribuute redigeerides.
- Looge uus kohandatud ajasisestusvaade ja seadke see vaikevaateks. See vaade peaks **sisaldama lisaks veergudele, mida ruudustik peaks kaasama, väljad Kirjeldus** ja **Välised kommentaarid**. Ruudustiku asukoha, suuruse ja vaikesorteerimisjärjestuse saate määrata vaate atribuute redigeerides. Seejärel konfigureerige selle vaate kohandatud juhtelementi nii, et see oleks **Ajakirje ruudustiku** juhtelement. Lisage juhtelement vaatesse ja valige see veebi **,** telefoni **ja** tahvelarvuti **jaoks**. Seejärel konfigureerige iganädalase ajasisestusruudustiku **parameetrid**. Seadke **väli Alguskuupäev** msdyn-kuupäevaks **\_**, seadke **välja Kestus** väärtuseks **msdyn\_ kestus** ja seadke **välja Olek** väärtuseks **msdyn\_ entrystatus.** Välja **Kirjutuskaitstud olekuloend** väärtuseks **on seatud 192350002 (Kinnitatud)**, **192350003 (Esitatud)** või **192350004 (Tagasikutsumine taotletud)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Kohandatud välja lisamine sobivale redigeerimislehele
Leheküljed, mida kasutatakse ajakirje või ajakirjete rea redigeerimiseks, leiate jaotisest **Vormid**. Ruudustiku **nupp Redigeeri kirjet** avab **lehe Redigeeri kirjet** ja **nupp Redigeeri rida** avab **lehe Rea redigeerimine**. Neid lehti saate redigeerida nii, et need sisaldaksid kohandatud välju.

Mõlemad suvandid eemaldavad projekti **- ja** projektiülesande **olemites mõne kastivälise filtreerimise**, et kõik olemite otsinguvaated oleksid nähtavad. Valmis, kuvatakse ainult asjakohased otsinguvaated.

Peate määrama kohandatud välja jaoks sobiva lehe. Tõenäoliselt, kui lisasite välja ruudustikku, peaks see minema **lehele Rea redigeerimise** leht, mida kasutatakse väljade puhul, mis rakenduvad kogu ajakirjete reale. Kui kohandatud väljal on reas iga päev kordumatu väärtus (nt kui see on lõppaja jaoks kohandatud väli), peaks see minema **lehele Ajasisestuse redigeerimine**.

Kohandatud välja lisamiseks lehele lohistage **väljaelement** lehel sobivasse asendisse ja seejärel määrake selle atribuudid.

### <a name="add-new-option-set-values"></a>Uute suvandikomplekti väärtuste lisamine
Suvandikomplekt väärtuste lisamiseks väljale out-of-box tehke järgmist.

1. Avage välja redigeerimisleht ja seejärel valige jaotises **Tüüp** väärtus Redigeeri **suvandikomplekt kõrval.**
2. Lisage uus suvand, millel on kohandatud silt ja värv. Kui soovite lisada uue ajasisestuse oleku, nimetatakse **väljast väljas olevat välja kande olek**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Uue ajakirje oleku määramine kirjutuskaitstuks
Selleks et määrata uue ajakirje olek kirjutuskaitstuks, lisage atribuudile **Kirjutuskaitstud olekuloend** uus ajakirje väärtus. Lisage kindlasti number, mitte silt. Ajasisestusruudustiku redigeeritav osa lukustatakse nüüd ridadele, millel on uus olek. Atribuudi Kirjutuskaitstud olekuloend määramiseks **erinevate** ajasisestuse **vaadete jaoks erinevalt lisage** vaate **kohandatud juhtelementide** jaotisse ajasisestuse **ruudustik ja konfigureerige parameetrid** vastavalt vajadusele.

Seejärel lisage ärireeglid, et lukustada kõik väljad ridade redigeerimise **ja** ajakirje redigeerimise **lehtedel**. Nende lehtede ärireeglitele juurdepääsemiseks avage iga lehe väljaredaktor ja seejärel valige **Ärireeglid**. Saate lisada olemasolevate ärireeglite tingimusele uue oleku või uuele olekule uue ärireegli.

### <a name="add-custom-validation-rules"></a>Kohandatud valideerimisreeglite lisamine
Iganädalase ajasisestusruudustiku **kogemuse jaoks** saate lisada kahte tüüpi valideerimisreegleid.

- Kliendipoolsed ärireeglid, mis töötavad lehtedel
- Serveripoolsed lisandmooduli valideerimised, mis rakenduvad kõigi aegade sisestamise värskendustele

#### <a name="client-side-business-rules"></a>Kliendipoolsed ärireeglid
Ärireeglite abil saate välju lukustada ja avada, sisestada väljade vaikeväärtused ning määrata kinnitused, mis nõuavad ainult praeguse ajakirje kirje teavet. Lehe ärireeglitele juurdepääsemiseks avage väljaredaktor ja seejärel valige **Ärireeglid**. Saate redigeerida olemasolevaid ärireegleid või lisada uue ärireegli.

#### <a name="server-side-plug-in-validations"></a>Serveripoolsed lisandmooduli valideerimised
Peaksite kasutama pistikprogrammi valideerimist mis tahes valideerimiseks, mis nõuavad rohkem konteksti, kui on saadaval ühekordse kirje kirje puhul. Samuti peaksite neid kasutama mis tahes valideerimiseks, mida soovite ruudustiku tekstisisestes värskendustes käitada. Valideerimiste lõpuleviimiseks looge olemis Ajasisestus **kohandatud lisandmoodul**.

### <a name="limits"></a>Limiidid
**Praegu on aja sisestamise** ruudustiku suuruspiirang 500 rida. Kui ridu on rohkem kui 500, siis üleliigseid ridu ei kuvata. Seda suurusepiirangut ei ole võimalik suurendada.

### <a name="copying-time-entries"></a>Ajakirjete kopeerimine
Kasutage vaadet **Kopeeri ajakirje veerge**, et määratleda ajavahemiku jooksul kopeeritavate väljade loend. Väljad **Kuupäev** ja **Kestus** on nõutavad ja neid ei tohi vaatest eemaldada.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
