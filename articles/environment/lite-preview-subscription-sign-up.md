---
title: Eelversiooni kordustellimuseks registreerumine – liht
description: See artikkel annab teavet selle kohta, kuidas tellida ja juurutada Project Operations lite juurutust - tegeleda proforma arveldusega.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6953956c0b3401a6c64ee597f966ba4a4c0d07b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921251"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Eelversiooni kordustellimuseks registreerumine – liht 

Selles artiklis selgitatakse, kuidas tellida proovipakkumine ja juurutada Dynamics 365 Project Operations lite juurutamine - tegeleda proforma arvete esitamisega.

> [!NOTE]
> See toiming muutub Project Operationsi eelseisvates väljaannetes.

## <a name="prerequisites"></a>Eeltingimused
- Kasutajal, kes eelvaate juurutab, peab olema Azure'i rentniku globaalse administraatori õigused. Rentniku saate luua esimese pakkumise lunastamise ajal.

> [!IMPORTANT]
> Selle toimingu peab organisatsioonis tegema ainult üks inimene, rentniku administraator. Kui te pole selle väljalaske tellija, oodake, kuni teie organisatsioon on registreeritud ja teile on saadetud kasutaja mandaat.
> 
> Prooviversioonid on rentnikus ühekordselt kasutatav. Prooviversiooni saab käitada ainult üks kord. Soovitame teil luua prooviversiooni eesmärgil uus rentnik.

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operationsi prooviversioon 

Enne alustamist veenduge, et oleksite brauseris sisse logitud kasutaja töökontoga rentnikusse, kus soovite Project Operationsi eelvaadet näha.

1. Avage [Project Operationsi prooviversioon](https://aka.ms/try-po), et lunastada esimese pakkumise kood, **Dynamics 365 Project Operations**.
2. Kinnitage oma tellimus.

  Näete kinnitust, et pakkumise lunastamine õnnestus.

## <a name="assign-licenses"></a>Litsentside määramine

> [!IMPORTANT]
> Järgmiste toimingute lõpuleviimiseks on teil vaja oma organisatsiooni Microsoft 365 portaali administraatori juurdepääsu.


1. Kasutajatele litsentside määramiseks minge [Microsoft 365 halduskeskusesse](https://portal.office.com/).
2. Valige lehel **Aktiivsed kasutajad** need kasutajad, kellele soovite litsentsi määrata.
3. Veenduge, et valitaks litsents **Dynamics 365 Project Operations**. 
4. Valige käsk **Salvesta muudatused**.

## <a name="create-a-new-dataverse-environment"></a>Loo uus Dataverse keskkond

1. Uue Project Operationsi Dataverse juurutuskeskkonna pakkumine, järgides artiklis toodud juhiseid juurutusmudel [Dataverse](lite-deployment.md). Keskkonnatüübi valimisel kasutage kindlasti valikut **Prooviversioon (tellimusepõhine)**.

  ![Uus keskkond.](./media/19CreateEnvironment.png)

2. Valige säte **Luba Dynamics 365 rakendused** ja jätke väli **Juuruta neid rakendusi automaatselt** tühjaks.  
3. Keskkonna loomiseks valige nupp **Salvesta**.

  ![Andmebaasi lisamine.](./media/20CreateEnvironment1.png)

4. Pärast keskkonna loomist installige **Microsofti Dynamics 365 Project Operations** lahendus. 

![Lahenduse installimine.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS-i konfiguratsiooni ja seadistuse demoandmete installimine

Installige CDS-konfiguratsioon ja seadistage demoandmed, järgides artiklis olevaid juhiseid, [Rakenda demo häälestust ja konfiguratsiooniandmeid](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
