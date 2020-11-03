---
title: Projekti eelarvetele prognoosimudeli loomine
description: Selles teemas antakse teavet, kuidas luua järelejäänud eelarvete jaoks prognoosimudel.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075092"
---
# <a name="create-forecast-models-for-project-budgets"></a>Projekti eelarvetele prognoosimudeli loomine 

[!include [banner](../includes/banner.md)]

Selles teemas antakse teavet, kuidas luua järelejäänud eelarvete jaoks prognoosimudel. Projekt, mille suhtes rakendatakse eelarve kontrolli, kasutab kahte tüüpi eelarveid: algne ja järelejäänud. Projekti eelarve loomisel tuleb määrata algsed ja järelejäänud eelarve prognoosimudelid, mis on loodud rakenduse lehel **Prognoosimudel**. Määratud mudelitel põhinevad projekti eelarved luuakse projekti eelarve täitmisel.

> [!NOTE]
> Prognoosimudel, mida kasutatakse eelarve kontrollimisel, ei saa olla allmudeliga ning seda ei saa kasutada allmudelina.

1. Valige **Projekti haldamine ja raamatupidamine** > **Seadistamine** > **Prognoosid**  > **Prognoosimudelid**.
2. Uue prognoosimudeli loomiseks valige suvand **Uus** ning seejärel sisestage uue mudeli ID-number ja nimi. 
3. Seadke suvandi **Peatatud** väärtuseks **Jah** , et vältida prognoosimudeli prognoosiridade muutmist. 
4. Kui selle mudeliga seotud prognoosiread peaksid tekitama pearaamatus rahavoogude prognoose, määrake suvandi **Kaasa rahavoo prognoosid** väärtuseks **Jah**. 
5. Projekti kuupäeva kasutamiseks arve kuupäevana seadke suvandi **Prognoosi arve kuupäev** väärtuseks **Jah**. 
6. Valige väljal **Eelarve tüüp** üks järgmistest mudeli tüüpidest.

   - **Algne eelarve** : kasutage algse eelarve loomisel ja kinnitamisel kulutatud algse eelarve summasid.
   - **Järelejäänud eelarve** : kasutage projekti kasutusea jooksul järelejäänud eelarve summasid. Selle prognoosimudeli saldosid vähendatakse tegelike tehingute võrra ning suurendatakse või vähendatakse eelarvete läbivaatamisel.
   - **Ülekandmine** : kasutage projekti jaoks ülekantud eelarve summasid. Ülekandmine on valikuline protsess, mida saab käitada kasutamata eelarve summade ülekandmiseks ühest finantsaastast teise.

7. Määrake vajaduse järgi järgmised suvandid.

   - Projekti kuupäeva kasutamiseks arve kuupäevana lubage suvand **Prognoosi arve kuupäev**.
   - Lubage poolelioleval tööl (WIP )põhinevaks prognoosimiseks suvand **Prognoosimine WIP-iga** , seejärel valige WIP-i tüüp. 
   - Saate suvandi **Eelarve tüüp** vaikeväärtuseks jätta väärtuse **Pole** või sisestada uue tüübi. Pärast kirje muutmist ei saa eelarve tüüpi muuta.     
    > [!NOTE]
    > Kui muudate eelarve vaiketüübi, muutuvad kõik muud suvandid värskenduste jaoks kättesaamatuks ning seda prognoosimudelit ei saa uuesti kasutada. 
   


 

