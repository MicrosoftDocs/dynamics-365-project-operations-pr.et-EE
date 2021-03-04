---
title: Arve ajakava loomine projektipõhisel lepingureal
description: Selles teemas antakse teavet lepinguridade arve ajakavade ja vahe-eesmärkide loomise kohta.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2fbec567c07d7567f1d133fa3512496039f16a1
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513919"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Arve ajakava loomine projektipõhisel lepingureal 

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Saate luua arve ajakava projektipõhisele lepingureale. Arveldamine on lubatud ainult pärast lepingu võitmist ja projekti lepingu loomist. Arve ajakava võimaldab automaatselt luua projektipõhise lepingurea jaoks arvete mustandeid. Kui aga loote arveid ainult käsitsi, võite lepinguridadel arvete ajakava loomise vahele jätta.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Lepingurea jaoks aja ja materjali arve ajakava loomine

Kui projektipõhisel lepingureal on aja ja materjali arveldusmeetod, saate luua kuupäeval põhineva arve ajakava. Kuupäeval põhineva arve ajakava automaatseks loomiseks tehke järgmist.

1. Avage **Sätted** > **Arve sagedused** ja seadistage arve sagedus.
2. Avage projekti lepingu kirjed ja valige vahekaardil **Kokkuvõte** väljal **Soovitud tarnekuupäev** kuupäev.
3. Avage lepingurida **Aeg ja materjal**, mille jaoks te kuupäeval põhineva arve ajakava loote. 
4. Valige vahekaardil **Arve ajakava** arveldamise alguskuupäev ja arve sagedus.
5. Valige andmeruudustikus suvand **Loo arve ajakava**. Arve ajakava luuakse koos väljadega **Arve käitamise kuupäev**, **Kande katkestamise kuupäev** ja **Käituse olek**, mis on määratud järgmisel viisil.

    - **Arve käitamise kuupäev**: see kuupäev on määratud arve sageduse järgi.
    - **Tehingu katkestamise kuupäev**: päev enne arve käitamise kuupäeva.
    - **Käitamise olek**: automaatselt määratud kui **Käivitamata**. Kui automaatse arve loomise töö käitab teatud arve käivitamise kuupäeva, uuendab see välja valikule **Käitamine õnnestus** või **Käitamine nurjus**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Lepingurea jaoks fikseeritud hinnaga arve ajakava loomine

Kui lepingurea arveldusmeetod on fikseeritud, saate luua vahe-eesmärgi põhise arve ajakava. 

> [!NOTE]
> Neid vahe-eesmärke ei saa lepingureal luua, kui ükski projekt pole lepingureale vastendatud.

Kui soovite selle vahe-eesmärgil põhineva ajakava luua fikseeritud vahe-eesmärkide kogumi jaoks, mis on kalendriperioodil ühtlaselt jaotatud, tehke järgmist.

1. Avage **Sätted** > **Arve sagedused** ja seadistage arve sagedus.
2. Avage projekti lepingu kirjed ja valige vahekaardil **Kokkuvõte** väljal **Soovitud tarnekuupäev** kuupäev.
3. Avage lepingurida **Fikseeritud hind**, mille jaoks vahe-eesmärgi ajakava loote. Valige vahekaardil **Arveldamise vahe-eesmärgid** arveldamise alguskuupäev ja arve sagedus. 
4. Valige andmeruudustikus suvand **Loo perioodilised vahe-eesmärgid**. Arve ajakava luuakse väljaga **Vahe-eesmärgi nimi**, **Vahe-eesmärgi kuupäev** ja **Vahe-eesmärgi summa**, määratakse järgmiselt.

    - **Vahe-eesmärgi nimi**: selle nime määrab arvete sagedus.
    - **Vahe-eesmärgi kuupäev**: see kuupäev on määratud arve sageduse järgi.
    - **Vahe-eesmärgi summa**: see summa arvutatakse, jagades lepingureal oleva lepingu summa vahe-eesmärkide arvuga, nagu arvelduse sagedus, algus ja nõutavad tarnekuupäevad ette näevad.

    Kui lepingureal on väärtus väljal **Prognoositav maksusumma**, jagatakse see väli ka iga vahe-eesmärgiga samaks perioodiks perioodiliste vahe-eesmärkide loomisel.

Arveldamise vahe-eesmärgid peaksid võrduma lepingurea lepingu väärtusega. Kui need sellega ei võrdu, kuvatakse teile lehel **Lepingurida** tõrge. Tõrke saate parandada vahe-eesmärkide loomise, muutmise või kustutamise teel, kontrollides, kas arveldamise vahe-eesmärgid vastavad rea lepingu väärtuse. Pärast muudatuste tegemist värskendage lehte, et tõrge eemaldada.

### <a name="manually-create-milestones"></a>Käsitsi loodud vahe-eesmärgid

Saate luua fikseeritud hinnaga vahe-eesmärke käsitsi, kui neid ei jagata perioodiliselt. Vahe-eesmärgi käsitsi loomiseks tehke järgmist.

1. Avage fikseeritud hinna lepingurida, mille jaoks soovite vahe-eesmärgi luua, ja klõpsake andmeruudustiku vahekaardil **Arve ajakava** nuppu **+ Loo uus lepingurea vahe-eesmärk**. 
2. Sisestage lehel **Vahe-eesmärgi loomine** järgmise tabeli põhjal soovitud teave.

| Väli | Asukoht | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- | --- |
| Vahekokkuvõtte nimi | Kiirloomine | Vahe-eesmärgi nime tekstiväli. | See kantakse projekti lepingurea vahe-eesmärgile ja arvele. |
| Projekti ülesanne | Kiirloomine | Kui vahe-eesmärk on seotud projekti tööülesandega, saate selle viite abil lisada kohandatud loogika, mis määrab vahe-eesmärgi oleku tööülesande oleku põhjal. | Rakendusel ei ole selle ülesande viite puhul ühtegi allavoolu mõju. |
| Vahekokkuvõtte kuupäev | Kiirloomine | Määrake kuupäev, millal arvete automaatse loomise protsess peaks selle vahe-eesmärgi olekut arveldamise jaoks vaatama. | See kantakse projekti lepingurea vahe-eesmärgile ja arvele. |
| Arve olek | Kiirloomine | Kui vahe-eesmärk on loodud, on see olek alati määratud valikule **Pole arveldamiseks valmis** või **Pole alustatud**. | See kantakse projekti lepingurea vahe-eesmärgile ja arvele. |
| Rea summa | Kiirloomine | Vahe-eesmärgi summa või väärtus, mille eest esitatakse kliendile arve. | See kantakse projekti lepingurea vahe-eesmärgile ja arvele. |
| Maks | Kiirloomine | Vahe-eesmärgile rakendatav maksusumma. | See kantakse projekti lepingurea vahe-eesmärgile ja arvele. |

3. Valige **Salvesta ja sule**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]