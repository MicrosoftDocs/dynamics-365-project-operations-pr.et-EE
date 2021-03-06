---
title: Reisitellimused
description: Selles teemas antakse teavet reisitellimuste kohta.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906136"
---
# <a name="travel-requisitions"></a>Reisitellimused

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Reisitellimus loetleb kulud, mis on tekkinud reisimise eesmärgil. Reisitellimus esitatakse läbivaatamiseks ja seda saab kasutada kulude lubamiseks.

Võimalik, et teil tuleb esitada reisitellimus enne seda, teete organisatsiooni tasutavaid kulusid. Seda nõuet kohaldatakse, olenemata sellest, kas tasute kulude eest ettevõtte krediitkaardiga, kulutate ettemaksuks saadud raha või tasute kulude eest oma taskust, mis hiljem organisatsiooni poolt hüvitatakse.

Reisitellimusi ja poliitikaid saab kasutada organisatsiooni kulude haldamiseks. Kui teie organisatsioon töötab näiteks fikseeritud hinnaga projektiga, mis nõuab reisimist, peavad projekti meeskonnaliikmete sõidukulud vastama projekti eelarvele. Nõudes, et reisikulud kinnitatakse enne nende tekkimist, saab organisatsioon aidata tagada, et projekt jääb eelarve piiresse.

## <a name="configuration"></a>Konfiguratsioon 

Reisitellimusi saab konfigureerida kui "kohustuslik", lubades kuluhalduse parameetrite all parameetri "Reisimise eelnev lubamine on kohustuslik". 

## <a name="create-and-submit-a-travel-requisition"></a>Reisitellimuse loomine ja esitamine

1. Avage **Minu kulud: reisitellimus** ja valige **Uus reisitellimus**.
2. Sisestage tellimuse eesmärk ja sihtkoht.
3. Sisestage täiendav teave väljale **Reisi kirjeldus**. 
4. Iga eeldatava kulu kohta, nagu näiteks lend, eined või autorent, looge kulu reaüksus. Lisage iga kulu eeldatav päev, eeldatav summa ja valuuta. 
5. Kui olete eeldatavate kulude lisamise lõpetanud, valige **Salvesta**.
6. Kui olete valmis reisitellimust esitama, valige **Töövoog** > **Esita**.

Oma heakskiidetud reisitellimusi saate vaadata jaotises **Minu kulud: reisitellimus**. 

## <a name="view-available-travel-requisitions"></a>Kuva saadaolevad reisitellimused

Kõiki oma reisitellimusi saate vaadata jaotises **Minu kulud: reisitellimused**.

## <a name="approve-travel-requisitions"></a>Reisitellimuste kinnitamine

Valige reisitellimus, mida soovite kinnitada, ja seejärel valige **Töövoog** > **Kinnita**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Kuluaruande esitamine kinnitatud reisitellimuse abil

1. Looge uus kuluaruanne ja kuluaruande päises ning heakskiidetud reiside loendist valige **Vastendage reisitellimusega**.
2. Väli **Reisitellimuse summa** värskendatakse kuluaruande päises automaatselt.
3. Lisage kõik reisi jaoks tehtud kulutused. Kui väli **Eelautoriseeritud** on lubatud, värskendatakse konkreetse kulukategooria vastavausse viidud summa ja lubatud summa.

> [!NOTE]
> Kui vastendate kuluaruande kinnitatud reisitellimusega, ei saa tehingu summa olla suurem kui lubatud summa. 
