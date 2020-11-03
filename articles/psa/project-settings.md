---
title: Projekti sätted
description: Selles teemas antakse teavet projektihalduse sätete kohta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075119"
---
# <a name="project-settings"></a>Projekti sätted

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekti plaanimise funktsioonidele juurdepääsemiseks kasutage järgmisi sätteid.

## <a name="work-template"></a>Töömall

Projekti ajakava loomiseks peate looma projektikalendri malli, mis määratleb töötundide arvu päevas ja kõik äri lõpetamised. Projektikalendri malli loomiseks seostage projekti väljaga **Kalendrimall** töömall. Töömalli loomiseks tehke järgmist.

1. Klõpsake rakenduse PSA vasakpoolsel navigeerimispaanil nuppu **Ressursid**. 
2. Avage loendilehel **Ressursid** kasutajakirje ja seejärel tehke valik **Kuva töötunnid**.

  > [!NOTE]
  > Veenduge, et brauseriaknas oleks hüpikaknad lubatud. Nii saate vaadata ressursi jaoks määratud töötunde.
  
3. Klõpsake vahekaardil **Kuuvaade** nuppu **Seadista**. Kuvatakse kolme suvandiga loend. 

  - Uus nädalagraafik
  - Ühe päeva töögraafik
  - Vaba aeg

> ![Suvandite seadistamine](media/project-13.png)

4. Tehke valik **Uus nädalagraafik** ja seejärel määrake selle ressurside ajakava suvandid. Saate määrata korduva nädalagraafiku, iga päeva tunniparameetrid, äri lõpetamised ja muud.
5. Määrake kuupäevavahemik, tehke valik **Salvesta** ja seejärel klõpsake käsku **Sule**. 
6. Minge tagasi loendilehele **Ressursid** ja valige ressurss, mille jaoks töötunde määrate. 
7. Töömalli määramiseks tehke valik **Seadista kalender nimega**. 
8. Sisestage dialoogiboksis **Töömall** töömalli nimi ja seejärel tehke valik **Rakenda**. 

Nüüd saate seostada töömalli projektikalendri malliga.

## <a name="resource-roles"></a>Ressursirollid

Mõiste *ressursiroll* viitab oskuste, pädevuste ja sertide komplektile, mis peavad isikul olema, et teha projekti jaoks teatud ülesandeid. Rakendus PSA võimaldab teil vastavalt rollile, millega ressurss seotud on, ressursi ajakulu arvesse võtta ja sellega arveldada. Kõik organisatsioonid peavad need rollid seadistama, kasutades selleks menüü **Project Service** vasakpoolset navigeerimist.

Kõik organisatsioonid peavad need rollid seadistama lehel **Aktiivsed ressursikategooriad**. Selle lehe avamiseks valige vasakpoolsel navigeerimispaanil suvand **Ressursirollid**.

## <a name="price-lists"></a>Hinnakirjad

Hinnakirjad võimaldavad teil määrata organisatsioonis ressursirollide, kulukategooriate, toodete ja muude elementide jaoks oma- ning müügihinnad. Enne, kui määrate projekti jaoks edastatava töö finantskalkulatsioonid, peate looma tugikulud ja müügihinnakirja. Peate parameetrite jaotises seadistama ka vaikimisi kulu- ja müügihinnakirja, mis rakendub kõigile organisatsioonis loodavatele projektidele. Seadistage kindlasti lehel **Aktiivsed projektiparameetrid** vaikimisi kulu- ja müügihinnakiri.