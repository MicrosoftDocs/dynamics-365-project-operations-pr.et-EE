---
title: Arve graafikute loomine projekti lepingu real
description: See artikkel annab teavet arve ajakavade ja vahekokkuvõtete loomise kohta.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1a6d0647ee012212a74a674cfa4e995d0e375b77
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824715"
---
# <a name="create-invoice-schedules-on-a-project-contract-line"></a>Arve graafikute loomine projekti lepingu real

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Saate lisada arve ajakava projektipõhisele lepingureale. Arveldamine on lubatud ainult pärast lepingu võitmist, et luua projektileping. Arve ajakavad võimaldavad luua automaatselt projektipõhise lepingurea jaoks arvete mustandeid. Kui plaanite luua arveid alati käsitsi, saate projektipõhise llepingureal või lepingureal arve ajakavade loomise vahele jätta.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Projektipõhise lepingurea jaoks aja ja materjali arve ajakava loomine

Kui projektipõhisel lepingureal on aja ja materjali arveldusmeetod, saate luua kuupäeval põhineva arve ajakava. Kuupäeval põhineva arve ajakava automaatseks loomiseks tehke järgmist.

1. Avage **Sätted** > **Arve sagesused**, et häälestada arve sagedus.
2. Avage projektileping ja vahekaardil **Kokkuvõte** määrake soovitud tarnekuupäev.
3. Avage aja ja materjali lepingurida, mille jaoks soovite kuupäevapõhise arve ajakava luua. 
4. Valige vahekaardil **Arve ajakava** arveldamise alguskuupäev ja arve sagedus. 
5. Valige andmeruudustikus suvand **Loo arve ajakava**.

    Süsteem loob arve ajakava järgmise välja teabega.

    - **Arve käivitamise kuupäev** määratakse arve sageduse põhjal.
    - **Kande katkestamise kuupäev** on määratud kuupäevale enne **arve käitamise kuupäeva**.
    - **Käitamise olek** on määratud autmaatselt olekusse **Käivitamata**. Kui automaatse arve loomise töö käitab teatud **arve käivitamise kuupäeva**, uuendab see välja valikule **Käitamine õnnestus** või **Käitamine nurjus**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Projektipõhise lepingurea jaoks fikseeritud hinnaga arve ajakava loomine

Kui projektipõhisel lepingureal on fikseeritud hinnaga arveldamise meetod, saate luua vahe-eesmärgil põhineva arve ajakava. Tehke järgmised toimingud, et genereerida automaatselt vahe-eesmärkidel põhinevad arve ajakavad fikseeritud vahe-eesmärkide komplekti jaoks, mis jaotatakse kalendri perioodi jaoks võrdselt.

1. Avage **Sätted** > **Arve sagesused**, et häälestada arve sagedus.
2. Avage projektileping ja vahekaardil **Kokkuvõte** määrake soovitud tarnekuupäev.
3. Avage fikseeritud hinnaga lepingurida, mille jaoks peate vahe-eesmärgi ajakava looma. 
4. Valige vahekaardil **Arve ajakava (arveldamise vahe-eesmärgid)** arveldamise alguskuupäev ja arve sagedus. 
5. Valige andmeruudustikus suvand **Loo perioodilised vahe-eesmärgid**.

    Süsteem loob arve ajakava järgmise vahe-eesmärgi teabega.

    - **Vahe-eesmärgi nimi** seatakse kuupäevale, mis määratakse arve sageduse põhjal.
    - **Vahe-eesmärgi kuupäev** seatakse kuupäevale, mis määratakse arve sageduse põhjal.
    - **Vahe-eesmärgi summa** arvutatakse jagades projektipõhise lepingurea lepingu summa vahe-eesmärkide arvuga, s on sageduse, arvelduse alguse ja taotletud tarnekuupäevade poolt määratletud.
    - Kui lepingureal on väärtus väljal **Eeldatav maksusumma**, jaotatakse perioodiliste vahe-eesmärkide genereerimisel see väli samuti iga vahe-eesmärgi jaoks võrdselt.

Arveldamise vahe-eesmärgid peaksid olema projektipõhise lepingurea lepingulise väärtusega võrdsed. Kui need pole võrdsed, võib esineda tõrge. Selle tõrke saate parandada, kui veendute, et arveldamise vahe-eesmärkide kogusumma oleks võrdne rea lepingu väärtusega, kas luues, muutes või kustutades vahe-eesmärke. Pärast muudatuste tegemist värskendage lehte.

### <a name="manually-create-milestones"></a>Käsitsi loodud vahe-eesmärgid

Kui fikseeritud hinnaga vahe-eesmärke ei jagata regulaarselt, saate need luua käsitsi. Vahe-eesmärgi käsitsi loomiseks täitke järgmised etapid.

1. Avage fikseeritud hinnaga lepingurida, mille jaoks tahate vahe-eesmärgi ajakava luua. 
2. Vahekaardi **Arve ajakava** andmeruudustikus valige suvand **+ Loo uus lepingurea vahe-eesmärk**.
3. Vormil **Vahe-eesmärgi loomine** sisestage järgmise tabeli põhjal nõutav teave. 

| Väli | Asukoht | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- | --- |
| Vahekokkuvõtte nimi | Kiirloomine | Vahe-eesmärgi nime tekstiväli. | See väli lisatakse projekti lepingurea vahe-eesmärgile ja arvele. |
| Projekti ülesanne | Kiirloomine | Kui vahe-eesmärk on seotud projekti ülesandega, kasutage seda viidet kohandatud loogika lisamiseks ja määrake tööülesande oleku põhjal vahe-eesmärgi olek. | Sellel ülesandele viitamisel ei ole edasist mõju. |
| Vahekokkuvõtte kuupäev | Kiirloomine | Kuupäev, mil automaatse arve loomise protsess peaks vaatama selle vahe-eesmärgi olekut, et kaaluda seda arveldamiseks. | See lisatakse projekti lepingurea vahe-eesmärgile ja arvele. |
| Arve olek | Kiirloomine | Kui vahe-eesmärk on loodud, seatakse olekuks alati **Ei ole arve esitamiseks valmis** või **Ei ole alustatud**. | See lisatakse projekti lepingurea vahe-eesmärgile ja arvele. |
| Rea summa | Kiirloomine | Vahe-eesmärgi summa või väärtus, mille eest esitatakse kliendile arve. | See väli lisatakse projekti lepingurea vahe-eesmärgile ja arvele. |
| Maks | Kiirloomine | Vahe-eesmärgile rakendatav maksusumma. | See lisatakse projekti lepingurea vahe-eesmärgile ja arvele. |

4. Valige **Salvesta ja sule**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
