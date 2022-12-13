---
title: Arve graafikud projekti hinnapakkumise ridadel
description: See artikkel kirjeldab hinnapakkumise ridade arve ajakavade ja vahekokkuvõtete loomist.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 98006cc2857f01298054c4f0e70781bf4b8b474b
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825747"
---
# <a name="invoice-schedules-on-project-quote-lines"></a>Arve graafikud projekti hinnapakkumise ridadel

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Projekti hinnapakkumise rida annab võimaluse väljendada arve ajakava. See on hinnapakkumise etapis valikuline, kuna rakendus ei toeta projekti arveldamist kui see on seotud hinnapakkumise reaga. Arveldamine on lubatud ainult pärast hinnapakkumise võitmist. Hinnapakkumise faasis arve ajakava loomise ainuke allavoolu mõju on, et see arve ajakava kopeeritakse projektipõhisele lepingureale. Kui te ei loo hinnapakkumise faasis arve ajakava, saate seda teha projektipõhisel lepingureal.

Üldiselt on arve ajakavade eesmärk lubada projektipõhise kontaktirea jaoks arvete mustandite automaatset loomist. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-quote-line"></a>Projekti hinnapakkumise rea aja- ja materjaliarve graafiku loomine

Kui projektipõhise hinnapakkumise rea arveldamise meetod on aeg ja materjal, loob süsteem kuupäeval põhineva arve ajakava. Kuupäeval põhineva arve ajakava automaatseks loomiseks tehke järgmist.

1. Avage **Sätted** > **arve sagedused** ja seadistage arve sagedus.
2. Avage lehel **Hinnapakkumised** projekti hinnapakkumine ja määrake vahekaardil **Kokkuvõte** nõutav tarnekuupäev.
3. Avage aja ja materjali hinnapakkumise rida, mille jaoks teil on vaja luua kuupäeval põhinev arve ajakava. 
4. Valige vahekaardil **Arve ajakava** väärtused väljade **Arvelduse algus** ja **Arve sagedus** jaoks. 
5. Valige andmeruudustikus suvand **Loo arve ajakava**.
6. Rakendus loob arve ajakava koos väljadega **Arve käitamise kuupäev**, **Kande katkestamise kuupäev** ja **Käituse olek** määratud järgmisel viisil.

    - **Arve käitamise kuupäev** on märatud kuupäevale, mis on määratud arve sageduse põhjal.
    - **Kande katkestamise kuupäev** on määratud kuupäevale enne **arve käitamise kuupäeva**.
    - **Käitamise olek** on määratud autmaatselt olekusse **Käivitamata**. Kui automaatse arve loomise töö käitab teatud arve käivitamise kuupäeva, uuendab see välja valikule **Käitamine õnnestus** või **Käitamine nurjus**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-quote-line"></a>Fikseeritud hinnaga arve graafiku loomine projekti hinnapakkumise reale

Kui projektipõhise hinnapakkumise rea arveldusmeetod on **Fikseeritud**, loob süsteem vahe-eesmärgi põhise arve ajakava. Kui soovite selle ajakava automaatselt genereerida fikseeritud vahe-eesmärkide kogumi jaoks, mis on kalendriperioodil ühtlaselt jaotatud, tehke järgmist.

1. Avage **Sätted** > **arve sagedused** ja seadistage arve sagedus.
2. Avage lehel **Hinnapakkumised** projekti hinnapakkumine ja määrake vahekaardil **Kokkuvõte** nõutav tarnekuupäev.
3. Avage fikseeritud hinnaga hinnapakkumise rida, mille jaoks peate vahe-eesmärkide ajakava looma. 
4. Valige vahekaardil **Arve ajakava** väärtused väljade **Arvelduse algus** ja **Arve sagedus** jaoks. 
5. Valige andmeruudustikus suvand **Loo perioodilised vahe-eesmärgid**.
6. Rakendus loob arve ajakava vahe-eesmärgi nime, kuupäeva ja summaga.

    - Vahe-eesmärgi nimi on märatud kuupäevale, mis on määratud arve sageduse põhjal.
    - Vahe-eesmärgi kuupäev on märatud kuupäevale, mis on määratud arve sageduse põhjal.
    - Vahe-eesmärgi summa arvutatakse, jagades projektipõhise hinnapakkumise real oleva hinnapakkumise summa vahe-eesmärkide arvuga, nagu arvelduse sagedus, algus ja nõutavad tarnekuupäevad ette näevad.
    - Kui hinnapakkumise real on ka eeldatav maksusumma, jaotatakse see väärtus perioodiliste vahe-eesmärkide loomisel iga etapi vahel võrdselt.

### <a name="manually-create-milestones"></a>Käsitsi loodud vahe-eesmärgid

Fikseeritud hinnaga vahe-eesmärke saab luua ka käsitsi, kui neid ei jagata perioodiliselt. Vahe-eesmärkide käsitsi loomiseks tehke järgmist.

Avage fikseeritud hinnaga hinnapakkumise rida, kuhu peate vahe-eesmärgi looma. Valige andmeruuustiku vahekaardil **Arve ajakava** suvand **+ Loo uus hinnapakkumise rea vahe-eesmärk** ja sisestage järgmise tabeli põhjal nõutav teave.

| **Väli** | **Asukoht** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- | --- |
| Vahe-eesmärgi nimi | Kiirloomine | Vahe-eesmärgi nimi. | See paljundatakse projekti lepingurea vahe-eesmärgile ja arvele |
| Projekti ülesanne | Kiirloomine | Kui vahe-eesmärk on seotud projekti tööülesandega, saate selle viite abil lisada kohandatud loogika, mis määrab vaheeesmärgi oleku tööülesande oleku põhjal. | Rakendusel ei ole selle ülesande viite puhul ühtegi allavoolu mõju. |
| Vahe-eesmärgi kuupäev | Kiirloomine | Määrake kuupäev, millal arvete automaatse loomise protsess peaks selle vahe-eesmärgi olekut arveldamise jaoks vaatama. | See paljundatakse projekti lepingurea vahe-eesmärgile ja arvele. |
| Arve olek | Kiirloomine | Kui vahe-eesmärk on loodud, on see olek alati määratud valikule **Pole arveldamiseks valmis**. | See paljundatakse projekti lepingurea vahe-eesmärgile ja arvele. |
| Rea summa | Kiirloomine | Vahe-eesmärgi summa või väärtus, mille eest esitatakse kliendile arve. | See paljundatakse projekti lepingurea vahe-eesmärgile ja arvele. |
| Maks | Kiirloomine | Vahe-eesmärgile rakendatav maksu summa. | See paljundatakse projekti lepingurea vahe-eesmärgile ja arvele. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
