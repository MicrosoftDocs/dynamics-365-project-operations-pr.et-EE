---
title: Projekti eelarvetele prognoosimudeli loomine
description: Selles teemas antakse teavet, kuidas luua järelejäänud eelarvete jaoks prognoosimudel.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 992dd74524ae6a7c329612a125d60bebfcbe7dd2
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683625"
---
# <a name="create-forecast-models-for-project-budgets"></a>Projekti eelarvetele prognoosimudeli loomine 

[!include [banner](../includes/banner.md)]

Selles teemas antakse teavet, kuidas luua järelejäänud eelarvete jaoks prognoosimudel. Projekt, mille suhtes rakendatakse eelarve kontrolli, kasutab kahte tüüpi eelarveid: algne ja järelejäänud. Projekti eelarve loomisel tuleb määrata algsed ja järelejäänud eelarve prognoosimudelid, mis on loodud rakenduse lehel **Prognoosimudel**. Määratud mudelitel põhinevad projekti eelarved luuakse projekti eelarve täitmisel.

> [!NOTE]
> Prognoosimudel, mida kasutatakse eelarve kontrollimisel, ei saa olla allmudeliga ning seda ei saa kasutada allmudelina.

1. Valige **Projekti haldamine ja raamatupidamine** > **Seadistamine** > **Prognoosid**  > **Prognoosimudelid**.
2. Uue prognoosimudeli loomiseks valige suvand **Uus** ning seejärel sisestage uue mudeli ID-number ja nimi. 
3. Seadke suvandi **Peatatud** väärtuseks **Jah**, et vältida prognoosimudeli prognoosiridade muutmist. 
4. Kui selle mudeliga seotud prognoosiread peaksid tekitama pearaamatus rahavoogude prognoose, määrake suvandi **Kaasa rahavoo prognoosid** väärtuseks **Jah**. 
5. Projekti kuupäeva kasutamiseks arve kuupäevana seadke suvandi **Prognoosi arve kuupäev** väärtuseks **Jah**. 
6. Valige väljal **Eelarve tüüp** üks järgmistest mudeli tüüpidest.

   - **Algne eelarve**: kasutage algse eelarve loomisel ja kinnitamisel kulutatud algse eelarve summasid.
   - **Järelejäänud eelarve**: kasutage projekti kasutusea jooksul järelejäänud eelarve summasid. Selle prognoosimudeli saldosid vähendatakse tegelike tehingute võrra ning suurendatakse või vähendatakse eelarvete läbivaatamisel.
   - **Ülekandmine**: kasutage projekti jaoks ülekantud eelarve summasid. Ülekandmine on valikuline protsess, mida saab käitada kasutamata eelarve summade ülekandmiseks ühest finantsaastast teise.

7. Määrake vajaduse järgi järgmised suvandid.

   - Projekti kuupäeva kasutamiseks arve kuupäevana lubage suvand **Prognoosi arve kuupäev**.
   - Lubage poolelioleval tööl (WIP )põhinevaks prognoosimiseks suvand **Prognoosimine WIP-iga**, seejärel valige WIP-i tüüp. 
   - Saate suvandi **Eelarve tüüp** vaikeväärtuseks jätta väärtuse **Pole** või sisestada uue tüübi. Pärast kirje muutmist ei saa eelarve tüüpi muuta.     
    > [!NOTE]
    > Kui muudate eelarve vaiketüübi, muutuvad kõik muud suvandid värskenduste jaoks kättesaamatuks ning seda prognoosimudelit ei saa uuesti kasutada. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]