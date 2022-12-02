---
title: Kirjete töölehtede loomine ja kinnitamine
description: See artikkel annab teavet selle kohta, kuidas luua ja kinnitada kandetöölehed rakenduses Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912327"
---
# <a name="create-and-confirm-entry-journals"></a>Kirjete töölehtede loomine ja kinnitamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Te kasutate kandetöölehti tegelike näitajate salvestamiseks otse rakenduses Microsoft Dynamics 365 Project Operations. Kui kasutate kandetöölehti, ei pea te rakenduses Project Operations sisestama aja-, kulu- ja materjalikasutuse logisid.

Üks kandetööleht võimaldab teil luua mitu töölehele kandmist. Kui tööleht on kinnitatud, salvestab töölehele kantud tegelikud näitajad järgmiste üksikasjade jaoks.

- Kulud või tulud olenevalt valitud tehingutüübist.
- Valitud tehinguklass. Saadaolevad klassid on **Aeg**, **Kulu**, **Materjal**, **Honorar**, **Vahekokkuvõte** ja **Maksud**.
- Projekt ja/või tööülesanne, mis on valitud töölehele kandmisel.

Rakenduses Project Operations kandetöölehe loomiseks järgige neid samme.

1. Minge jaotisse **Müügid** \> **Tehingud** \> **Töölehed**.
2. Valige loendilehe **Kandetöölehed** toimingupaanil **Uus**, et luua tööleht.
3. Sisestage lehel **Uus tööleht** väljale **Kirjeldus** töölehe kirjeldus.
4. Veenduge, et väljal **Töölehe tüüp** on määratud **Kirje**, ja seejärel valige **Salvesta**. Pärast uue kandetöölehe salvestamist peaks töölehe lehele ilmuma vahekaart **Tööleht loetud**.
5. Vahekaardil **Töölehele kandmised** valige ruudustiku kohal asuval tööriistaribal **Uus**, et luua kandetöölehele kandmine.
6. Kandetöölehele kandmise loomise dialoogiboksis **Kiirloomine** määrake väljad järgmises tabelis kirjeldatud viisil.

    | Väli | Kirjeldus | Funktsionaalne mõju |
    | --- | --- | --- |
    | Tehingu klass | Töölehele kandmise saab liigitada ühte kuuest tehinguklassist: **Aeg**, **Kulu**, **Materjal**, **Honorar**, **Vahekokkuvõte** või **Maksud**. | Tehinguklass **Maksud** on rakenduses Project Operations aegunud. <br> Kui loote tehinguklassi **Maksud**, ei töödelda seda arvete ega kulude või tulude arvutamisel. **Vahekokkuvõte** on ainult tuluga tehinguklass. <br>Tehinguklass **Honorar** tähistab kliendilt saadud ettemaksu. See tuleks alati luua arveldatud müügi ja arveldamata müügi töölehele kandmiste paarina. |
    | Tehingu tüüp | Kulude registreerimiseks tuleks kasutada tehingutüüpe **Kulu**, **Interorgi müügid** ja **Ressursiühiku maksumus**.<br> Tulu registreerimiseks tuleks kasutada tehingutüüpe **Arveldamata müügid** ja **Arveldatud müügid**. | Tehinguklass **Honorar** töötab ainult tehingutüüpidega **Arveldamata müügid** ja **Arveldatud müügid**.<br> Tehinguklass **Vahekokkuvõte** töötab ainult tehingutüübiga **Arveldatud müük**. <br>Tehingutüübid **Interorgi müügid** ja **Ressursside ühikukulu** on rakendatavad ainult tehinguklassi **Aeg** jaoks ja need on saadaval ainult lihtjuurutamise stsenaariumi kandetöölehtedes, mitte aga rakenduse Project Operations kasutuselevõtmisel ressurssi-/mittelaopõhistes stsenaariumides. |
    | Vali toode | Kui valitud on tehinguklass **Materjal**, saate sellel väljal määrata, kas materjalitehing, mille jaoks te töölehele kandmist loote, on olemasolev toode või sisestatav toode. | Kui valite **Sisestatav toode**, saate sisestada tootele nime. |
    | Toode | Viide tootele kataloogist. | |
    | Kirjeldus | Töölehele kandmise kirjeldus, mis hõlbustab tuvastamist. | Arveldamata müükide töölehele kandmise puhul kasutatakse väärtust kirjeldusena arverea üksikasjade loomisel. |
    | Väline kirjeldus | Töölehele kandmise kirjeldus, mida saab kasutada väliste huvirühmadega jagamiseks. | Arveldamata müükide töölehele kandmise puhul kasutatakse väärtust välise kirjeldusena arverea üksikasjade loomisel. See võib ilmuda ka arvel, mis kliendile saadetakse. |
    | Arveldustüüp | Väärtus, mis näitab, kas töölehele kandmist arvestatakse projekti tasulise, tasuta või mittetasulise komponendina. | Tavalises voos tuletatakse arveldustüüp lepingus sätestatud kokkulepitud tingimustest. Kui aga salvestate töölehele kandmise, saate sellele väljale sisestada väärtuse. |
    | Dokumendi kuupäev | Kasutage tehingu toimumise kuupäeva. | |
    | Alguskuupäev | Kasutage tehingu toimumise kuupäeva. | Seda välja kasutatakse **Arveldamata müügid** tüüpi tehingute arve koostamise kuupäevaga võrdlemiseks. See võrdlus aitab teil otsustada, kas tehing on tulevikus või minevikus. Arvele lisatakse ainult varasema kuupäevaga tehingud. |
    | Lõpukuupäev | Kasutage tehingu toimumise kuupäeva. | |
    | Aruandluskuupäev | Kasutage kuupäeva, millal raamatupidamismõju salvestatakse. | |
    | Lepingurea klient | Kui lepingureal on ainult üks klient, määratakse selle välja vaikimisi töölehele kandmise salvestamisel lepingureal olev klient. Kui lepingureal on mitu klienti, valige lepingurealt õige klient. | Kui süsteem ei suuda töölehele kandmise lepingurea klienti määrata ja kui see on tühi tüübi **Arveldamata müügid** tegeliku näitaja kohta, mis luuakse töölehele kandmisel, siis tegeliku näitaja arvet ei esitata. |
    | Project | Valige projekt, kuhu tegelik näitaja salvestada. | Valitud projekti, tehinguklassi ja ülesande põhjal püüab süsteem määrata lepingu, lepingurea ja lepingurea kliendi. |
    | Toiming | Valige ülesanne, millele tegelik näitaja salvestada. | Kui sidusite lepingu seadistamise ajal ülesanded lepinguridadega, kasutab süsteem lepingu, lepingurea ja lepingurea kliendi määramiseks valitud ülesannet koos projekti ja tehinguklassiga. |
    | Tehingu kategooria | Valige tehingukategooria, millesse tegelik näitaja salvestada. | Kulude jaoks määrab valitud tehingukategooria vaikehinna, mis sisestatakse selle salvestamisel töölehele kandmisel. |
    | Roll | See väli on asjakohane Aja töölehele kandmiste jaoks. Valige projektile ja/või ülesandele aega kulutanud ressursi roll. | Kui kasutate Aja töölehele kandmiste puhul ressursi vaikekulude ja arvemäärade sisestamiseks kastist väljas konfiguratsiooni, kasutatakse valitud rolli koos ressursiüksusega, et määrata vaikehind, mis sisestatakse töölehele kandmisel, kui see on salvestatud. Kui kasutate vaikehindade sisestamiseks kohandatud konfiguratsiooni, peaksite selle konfiguratsiooni üle vaatama, et teha kindlaks, kas välja **Roll** kasutatakse vaikehinna väärtuste sisestamiseks. |
    | Allhankeleping | Kui töölehele kandmine tähistab allhanke võimsust või allhankelepingu alusel sõlmitud kulusid või materjale, valige asjakohane allhankeleping. | Kui kulu töölehele kandmine on salvestatud, määrab valitud allhankeleping hinnakirja, mida kasutatakse vaikeühiku maksumuse sisestamiseks. |
    | Allhankelepingu rida | Kui töölehele kandmine tähistab allhanke võimsust või allhankelepingu alusel sõlmitud kulusid või materjale, valige asjakohane allhankelepingu rida. | Kulu töölehele kandmise salvestamisel tagab valitud allhankelepingu rida, et allhankereal olevad vaba võimsuse arvutused on õigesti arvutatud. |
    | Summa meetod | Vaikimisi on selle välja väärtus **Korruta kogus hinnaga**. Selle meetodi kasutamisel arvutatakse summa järgmiselt: *Kogus* × *Hind*. Teine toetatud meetod on **Fikseeritud hind**. Selle meetodi kasutamisel määratakse hinnaks summa ja kogust arvutuses ei kasutata. | |
    | Ühiku ajakava ja ühik | Ühiku ajakava ja ühik määravad koos kindlaks koguse ühiku. | Ühiku ja tehingukategooria kombinatsiooni kasutatakse kulude vaikehindade sisestamiseks. Rakenduse Project Operations vaikimisi konfiguratsioonis kasutatakse üksuse, rolli ja ressursiühiku kombinatsiooni, et sisestada vaikimisi ajahinnad. Kui teil on vaikehindade sisestamiseks kohandatud konfiguratsioon, kasutatakse seda koos ühikuga. Toote ja ühiku kombinatsiooni kasutatakse materjalide vaikehindade sisestamiseks. |
    | Kogus | Sisestage kogus. | |
    | Hind | Kui töölehele kandmise loomisel jäetakse hind tühjaks, kasutatakse vaikehindade sisestamiseks vastavaid väärtusi sõltuvalt tehinguklassist. Kui töölehele kandmise loomisel on sisestatud hind, kasutatakse seda hinda. | |
    | Maks | Sisestage mis tahes maksusumma. | Sõltuvalt sisestatud maksusummast arvutatakse laiendatud summa järgmiselt: *Summa* + *Maksud*. |

## <a name="confirm-an-entry-journal"></a>Kinnitage kandetööleht

Pärast seda, kui olete sisestanud kõik töölehele kandmised kandetöölehele, saate töölehe kinnitada. Selle protsessi käigus salvestatakse iga töölehele kandmine vastavate projektide tegelike näitajatena.

Pärast töölehe kinnitamist ei saa seda ega ühtegi selle rida enam redigeerida.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Tegelikud näitajad, mis on loodud kandetöölehe kinnitusega

On mõned olulised erinevused tegelike näitajate vahel, mis luuakse kandetöölehe kinnitamisel, ja tegelike näitajate vahel, mis luuakse aja-, kulu- ja materjali kasutuslogide kinnitamisel ja arve kinnitamisel rakenduses Project Operations:

- Kandetöölehed ei kasuta tehinguühendusi, et siduda kulu tegelik näitaja ja arveldamata müügi tegeliku näitaja väärtusega. Tegelikud näitajad, mis luuakse aja-, kulu- ja materjali kasutuslogide kinnitamisel, kasutavad alati tehinguühendusi, et siduda kulud ja arveldamata müügi tegelikud näitajad.
- Kandetöölehed ei kasuta tehingu algupära, et siduda kulu tegelikku näitajat ja arveldamata müügi tegelikke näitajaid ühegi algupärase kirjega. Tegelikud näitajad, mis luuakse aja-, kulu- ja materjali kasutuslogide kinnitamisel, kasutavad alati tehingu algupära, et siduda kulud ja arveldamata müügi tegelikud näitajad algse ajakirjega.
- Kui kandetöölehe kinnitamisega loodud arveldamata müügi tegelike näitajatega esitatakse arve, on arve kinnitamise käigus loodud arveldatud müügi tegelike näitajatega seotud arveldamata müügi tegelike näitajatega sarnaselt arveldamata müügi tegelike näitajatega, mis luuakse aja-, kulu- ja materjali kasutuslogide kinnitamisel.
- Organisatsioonidevaheliste ressursside poolt sisestatud aja kohta loodud kandetöölehe read ei tekita automaatselt tüübi **Ressursiühiku kulu** ja **Interorgi müügid** tegelikke näitajaid. Need tegelikud näitajad tuleb käsitsi luua. See käitumine erineb organisatsioonisiseste ressursside poolt salvestatud ajakirjete käitumisest. Sellisel juhul, kui aeg on kinnitatud, loob rakendus automaatselt projektile tüübi **Kulu** tegelikud näitajad ning töötaja omavale osakonnale tüübi **Ressursiühiku kulu** ja **Interorgi müügid** tegelikud näitajad. Seejärel kasutatakse tehinguühendusi, et siduda need tegelikud näitajad omavahel ja tehingu algupära, et siduda need algse ajakirjega.
- Kui kandetöölehed on kinnitatud, loovad need tegelikud näitajad. Paranduse töölehti ei saa aga nende tegelike näitajate parandamiseks kasutada. See käitumine erineb tegelike näitajate käitumisest, mis luuakse aja-, kulu- ja materjalide kasutuslogide kinnitatud ajale. Sellisel juhul võimaldab rakendus teil vigade parandamiseks kasutada paranduse töölehti, tingimusel, et need tegelikud näitajad ei ole veel arvele lisatud. Kui need on juba arveldatud, saate tegelikke limiite siiski parandada, kui töötlete kliendile selle tegeliku väärtuse täielikku limiiti.

> [!NOTE]
> Kandetöölehed ei kehtesta rangeid vaikereegleid. Seetõttu kasutage neid kandetöölehti nii vähe kui võimalik ning olge ettevaatlik ja hoolikas, et tagada, et te ei tekita oma süsteemis vigaseid finantsandmeid. Kui saate, kasutage aja-, kulu- ja materjali kasutuslogisid, projektilepingute vahekokkuvõtete ja honorari seadistust ning projektiarvete kinnitamise protsessi, mitte kandetöölehti, et luua tegelikke näitajaid.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
