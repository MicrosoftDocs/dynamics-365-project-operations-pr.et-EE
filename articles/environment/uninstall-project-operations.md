---
title: Rakenduse Dynamics 365 Project Operations desinstallimine
description: See artikkel annab teavet, kuidas rakendust Dynamics 365 Project Operations desinstallida.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911959"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Rakenduse Dynamics 365 Project Operations desinstallimine 

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Rakenduse Dynamics 365 Project Operations desinstallimiseks peab teile olema määratud administraatori roll.

1. Minge jaotisse **Sätted** > **Lahendused**.

    ![Sätete leht.](./media/uninstall-proj-ops-solutions.png)
  
2. Eemaldage lahendused täpselt selles järjestuses, nagu need on järgmises tabelis toodud. 

    | Samm | Lahenduse nimi                                    | Märge                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 2 | ProjectOperations_Anchor                           | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 5 | ProjectService                                     | Lisamärkused puuduvad.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Lisamärkused puuduvad.                                                                         |
    | 7 | ProjectServiceCore                                 | Lisamärkused puuduvad.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 9 | FieldServiceCommon                                 | Nõutav topeltkirjutuse jaoks rakendusega Dynamics 365 Finance või Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Nõutav topeltkirjutuse jaoks rakendusega Dynamics 365 Finance või Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Nõutav rakenduse Dynamics 365 Field Service puhul.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Nõutav rakenduse Dynamics 365 Field Service puhul.                                                     |
    | 13 | msdyn_TESA                                         | Nõutav rakenduse Dynamics 365 Field Service puhul.                                                     |
    | 14 | ResourceSchedulingControls                         | Nõutav rakenduse Dynamics 365 Field Service puhul.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Nõutav rakenduse Dynamics 365 Field Service puhul.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Nõutav rakenduse Dynamics 365 Field Service puhul.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Nõutav rakenduse Dynamics 365 Field Service puhul.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 19 | Dynamics365Notes                                   | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 21 | DualWriteCore                                      | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 23 | Dynamics365AssetManagement                         | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 26 | HCMCommon                                          | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 28 | Osapool                                              | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 29 | Dynamics365Company                                 | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 30 | CurrencyExchangeRates                              | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
    | 31 | AssetCommon                                        | Kui seda ei leitud, jätke see lahendus vahele.                                                            |
