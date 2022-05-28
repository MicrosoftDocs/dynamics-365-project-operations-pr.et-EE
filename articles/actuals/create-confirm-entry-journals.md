---
title: Sisestustöölehtede loomine ja kinnitamine
description: Selles teemas antakse teavet selle kohta, kuidas luua ja kinnitada Microsofti sisestustöölehti Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584223"
---
# <a name="create-and-confirm-entry-journals"></a>Sisestustöölehtede loomine ja kinnitamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Sisestustöölehtede abil saate kirjendada tegelikke andmeid otse Microsoftis Dynamics 365 Project Operations. Kui kasutate kandežurnaure, ei pea te projektitoimingutesse sisestama aja-, kulu- ja materjalikasutuse logisid.

Üks sisenemisžurnaal võimaldab teil luua mitu žurnaalirida. Kui tööleht kinnitatakse, salvestab kandežurnaali rida tegeliku järgmiste üksikasjade jaoks.

- Kulu või tulu, sõltuvalt valitud kande tüübist.
- Valitud kandeklass. Saadaolevad klassid on **aeg**, **kulu**, **materjal**, **hoidja**, **verstapost** ja **maks**.
- Žurnaalireal valitud projekt ja/või ülesanne.

Järgige neid juhiseid sisestustöölehe loomiseks Project Operationsis.

1. **Avage müügikande** \> **töölehed** \> **·**.
2. Valige **lehe Kirje töölehed** tegevuspaanil suvand **Uus** žurnaali loomiseks.
3. Sisestage **lehe Uus tööleht** väljale **Kirjeldus** žurnaali kirjeldus.
4. Veenduge, et **välja žurnaali liik** väärtuseks **on seatud Kanne**, ja seejärel valige **Salvesta**. Pärast uue sisestustöölehe salvestamist **peaks töölehe lehel ilmuma vahekaart Žurnaaliread**.
5. Sisestusžurnaali **tööleherea loomiseks valige menüü žurnaaliridade vahekaardi žurnaaliridade vahekaardi žurnaali read** ruudustiku kohal oleval tööriistaribal suvand **Uus**.
6. Määrake dialoogiboksis **Kiirloomine** kandežurnaali rea loomiseks väljad, nagu on kirjeldatud järgmises tabelis.

    | Väli | Kirjeldus | Funktsionaalne mõju |
    | --- | --- | --- |
    | Tehingu liik | Žurnaalirea saab liigitada ühte kuuest kandeklassist: **aeg, kulu**, **materjal**, **hoidja** **,** verstapost **või** maks **.** | Maksukande **klass** on projektitoimingutes aegunud. <br> Kui loote **maksukande** klassi, ei töödelda seda arvete esitamise või kulu- või tuluarvutustes. **Verstapost** on ainult tulupõhine tehinguklass. <br>Säilitaja **kandeklass** kujutab endast kliendilt saadud ettemakset. See tuleks alati luua arveldatud müügi ja sisestamata müügižurnaali ridade paarina. |
    | Kandetüüp | **Kulude kirjendamiseks tuleks kasutada ühiku omahinna** kande tüüpe Kulu **,** Interorg Sales **ja** Resourcing.<br> Tulude **kirjendamiseks tuleks kasutada konteerimata müügi** ja **arveldatud müügi** kande tüüpe. | Säilitaja **kandeklass** töötab ainult **konteerimata müügi** ja **arveldatud müügikannete** tüüpidega.<br> Verstaposti **kandeklass** töötab ainult arveldatud müügikande **tüübiga**. <br>**Interorgi müügi-** ja **hankimisühiku omahinna** kandetüübid on rakendatavad ainult ajakande **klassile** ja need on kõikumatulevad ainult Lite juurutusskeemide sisenemistöölehtedel, mitte projektitoimingute juurutamisel ressursi/ ladustamata stsenaariumides. |
    | Vali toode | **Kui valitud on materjalikande** klass, võimaldab see väli määrata, kas materjalikanne, mille jaoks žurnaalirida loote, on olemasolev toode või sissekirjutustoode. | Kui valite **kirjutustoote**, saate sisestada toote nime. |
    | Toode | Viide tootele kataloogist. | |
    | Kirjeldus | Žurnaalirea kirjeldus, mis aitab seda hõlpsalt tuvastada. | Sisestamata müügižurnaali ridade puhul kasutatakse väärtust kirjeldusena arverea üksikasjade loomisel. |
    | Väline kirjeldus | Žurnaalirea kirjeldus, mida saab kasutada väliste sidusrühmadega jagamiseks. | Sisestamata müügižurnaali ridade puhul kasutatakse väärtust arverea üksikasjade loomisel välise kirjeldusena. See võib ilmuda ka kliendile saadetaval arvel. |
    | Arveldustüüp | Väärtus, mis näitab, kas žurnaalirida loetakse projekti tasuliseks, tasuta või mittetasustatavaks komponendiks. | Tüüpilises voos tuletatakse arveldustüüp lepingus seadistatud kokkulepitud tingimustest. Žurnaalirea salvestamisel saate sellele väljale sisestada väärtuse. |
    | Dokumendi kuupäev | Kasutage kande toimumise kuupäeva. | |
    | Alguskuupäev | Kasutage kande toimumise kuupäeva. | Seda välja kasutatakse võrdlemiseks arve loomise kuupäevaga konteerimata müügi **tüüpi kannete** puhul. See võrdlus aitab teil otsustada, kas tehing on tulevikku dateeritud või aegunud. Arvele lisatakse ainult varasema kuupäevaga kanded. |
    | Lõpukuupäev | Kasutage kande toimumise kuupäeva. | |
    | Aruandluskuupäev | Kasutage kuupäeva, millal raamatupidamismõju kirjendatakse. | |
    | Lepingurea klient | Vaikimisi, kui lepingureal on ainult üks klient, seatakse see väli žurnaalirea salvestamisel lepingureal olevale kliendile. Kui lepingureal on mitu klienti, valige lepingureal õige klient. | Kui süsteem ei suuda žurnaalireal lepingurea klienti määratleda ja kui see on tühi žurnaalirealt loodava **tühistatud müügi** liigi tegelikul tüübil, siis tegelikku arvet ei esitata. |
    | Project | Valige projekt, kus kirjendada tegelik sisselogimine. | Valitud projekti, kandeklassi ja ülesande põhjal püüab süsteem määrata lepingu, lepingurea ja lepingurea kliendi. |
    | Toiming | Valige ülesanne tegeliku sisselogimiseks. | Kui seostasite lepingu seadistamise ajal ülesandeid lepinguridadega, kasutab süsteem valitud ülesannet koos projekti- ja kandeklassiga lepingu, lepingurea ja lepingurea kliendi määramiseks. |
    | Tehingu kategooria | Valige kandekategooria, kus kirjendada tegelik sees. | Kulude puhul määratleb valitud kandekategooria vaikehinna, mis sisestatakse žurnaalireale salvestamisel. |
    | Roll | See väli on ajažurnaali ridade jaoks asjakohane. Valige selle ressursi roll, kes veetis aega projektis ja/või ülesandes. | Ajažurnaali ridade puhul, kui kasutate ressursi vaikekulude ja arvemäärade sisestamiseks kastivälist konfiguratsiooni, kasutatakse valitud rolli koos ressursikogumisüksusega, et määrata vaikehind, mis sisestatakse žurnaalireale salvestamisel. Kui kasutate vaikehindade sisestamiseks kohandatud konfiguratsiooni, peaksite selle konfiguratsiooni üle vaatama, et teha kindlaks, kas **välja Roll** kasutatakse vaikehinna väärtuste sisestamiseks. |
    | Allhankeleping | Kui tööleherida tähistab allhankemahtu või allhankekulusid või materjale, valige vastav allhankeleping. | Kulužurnaali ridade registreerimisel määrab valitud alltöövõtt hinnakirja, mida kasutatakse ühiku vaikeomahinna sisestamiseks. |
    | Alltöövõtu rida | Kui žurnaalirida tähistab allhankemahtu või allhankekulusid või materjale, valige vastav alltöövõturida. | Kulužurnaali ridade registreerimisel tagab valitud alltöövõturida, et alltöövõtureal olevad saadaolevad võimsuse arvutused on õigesti arvutatud. |
    | Summa meetod | Vaikimisi on selle välja väärtuseks **seatud Koguse korrutamine hinna järgi**. Kui seda meetodit kasutatakse, arvutatakse summa *kogusena* × *hind*. Teine toetatud meetod on **fikseeritud hind**. Kui seda meetodit kasutatakse, seatakse hind summale ja kogust arvutuses ei kasutata. | |
    | Ühiku ajakava ja ühik | Koos tuvastavad ühiku ajakava ja ühik koguse ühiku. | Ühiku ja kandekategooria kombinatsiooni kasutatakse kulude vaikehindade sisestamiseks. Project Operationsi vaikekonfiguratsioonis kasutatakse aja vaikehindade sisestamiseks ühiku, rolli ja ressursiühiku kombinatsiooni. Kui teil on vaikehindade sisestamiseks kohandatud konfiguratsioon, kasutatakse seda koos ühikuga. Toote ja ühiku kombinatsiooni kasutatakse materjalide vaikehindade sisestamiseks. |
    | Kogus | Sisestage kogus. | |
    | Hind | Kui hind jäetakse žurnaalirea loomisel tühjaks, kasutatakse vaikehindade sisestamiseks asjakohaseid väärtusi, sõltuvalt kandeklassist. Kui žurnaalirea loomisel sisestatakse hind, kasutatakse seda hinda. | |
    | Maks | Sisestage mis tahes maksusumma. | Sõltuvalt sisestatud maksusummast arvutatakse laiendatud summa *summamaksuna* + *·*. |

## <a name="confirm-an-entry-journal"></a>Sisestustöölehe kinnitamine

Pärast kõigi žurnaaliridade sisestamist kandežurnaali saate žurnaali kinnitada. See protsess salvestab iga žurnaalirea vastavate projektide tegelikena.

Pärast töölehe kinnitamist ei saa te seda ega ühtegi selle rida enam redigeerida.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Kirje töölehe kinnitusega loodud tegelikud

Kirježurnaali kinnitusega loodud tegelike tegelike ja tegelike vahel, mis luuakse aja-, kulu- ja materjali kasutuslogide kinnitamisel ning arve kinnitamisel Project Operationsis, on mõned peamised erinevused.

- Kandetöölehed ei kasuta kandeühendusi tegeliku kulu sidumiseks sisestamata müügi tegelikuga. Tegelikud andmed, mis luuakse aja-, kulu- ja materjalikasutuslogide kinnitamisel, kasutavad kulude ja sisestamata müügi tegelike seoste sidumiseks alati kandeühendusi.
- Kande töölehed ei kasuta kande päritolu, et siduda tegelik kulu ja sisestamata müügi tegelikud andmed mis tahes algkirjega. Aja-, kulu- ja materjalikasutuslogide kinnitamisel tekkivad tegelikud andmed kasutavad alati kande päritolu, et siduda kulu ja sisestamata müügi tegelikud andmed algse ajakandega.
- Kui sisestamisžurnaali kinnitusega loodud sisestamata müügi tegelikud tegelikud andmed arveldatakse, lingitakse arve kinnitamisel loodud arveldatud müügi tegelikud tegelikud summad sisestamata müügi tegelikega sarnaselt sisestamata müügi tegelikega, mis luuakse aja-, kulu- ja materjali kasutuslogide kinnitamisel.
- Organisatsioonidevahelise ressursiga sisestatud aja jaoks loodud kandežurnaali read ei põhjusta varude ühiku omahinna **ja** interorg-müügi **tüüpide automaatset** loomist. Need tegelikud andmed tuleb käsitsi luua. See käitumine erineb organisatsioonisiseste ressurssidega salvestatud ajakannete käitumisest. Sellisel juhul, kui aeg on kinnitatud, loob rakendus automaatselt projekti kulutüübi **tegelikud tegelikud summad** ning töötaja enda osakonna ressursiüksuse ühiku omahinna **ja** Interorg Salesi **tüüpide tegelikud tegelikud** andmed. Seejärel kasutab ta tehinguühendusi, et siduda need tegelikud andmed kokku ja tehingu päritolu, et siduda need algse ajakandega.
- Kui sisestustöölehed on kinnitatud, loovad need tegelikud andmed. Parandustöölehti ei saa siiski kasutada nende tegelike andmete parandamiseks. See käitumine erineb tegeliku käitumisest, mis luuakse aja-, kulu- ja materjalikasutuslogide kinnitamisel. Sellisel juhul võimaldab rakendus kasutada parandusžurnaate, et parandada tegelikke vigu, tingimusel et neid tegelikke andmeid pole veel arveldatud. Kui need on juba arveldatud, saate siiski tegeliku parandada, kui töötlete kliendile selle tegeliku krediidi täielikku krediiti.

> [!NOTE]
> Sisestustöölehed ei jõusta rangeid vaikereegleid. Seetõttu kasutage neid sisenemispäevikuid nii vähe kui võimalik ning olge ettevaatlik ja ettevaatlik, et tagada, et te ei loo oma süsteemis korrumpeerunud finantsandmeid. Alati, kui saate, kasutage tegelike tööde loomiseks aja-, kulu- ja materjalikasutuse logisid, projektilepingute verstaposti ja säilitaja seadistust ning projektiarve kinnitusprotsessi sisestustöölehtede asemel.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
