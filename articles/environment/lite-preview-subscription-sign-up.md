---
title: Eelversiooni kordustellimuseks registreerumine – liht
description: See teema pakub teavet selle kohta, kuidas tellida ja juurutada Project Operations Lite’i juurutust – tehing näidisarveldusele.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334777"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Eelversiooni kordustellimuseks registreerumine – liht 

Selles teemas selgitatakse, kuidas tellida proovipakkumist ja juurutada Dynamics 365 Project Operationsi lihtjuurutust  – tehing näidisarveldusele.

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


1. Oma kasutajatele litsentside määramiseks avage [Microsofti 365 halduskeskus](https://portal.office.com/).
2. Valige lehel **Aktiivsed kasutajad** need kasutajad, kellele soovite litsentsi määrata.
3. Veenduge, et valitaks litsents **Dynamics 365 Project Operations**. 
4. Valige käsk **Salvesta muudatused**.

## <a name="create-a-new-dataverse-environment"></a>Loo uus Dataverse keskkond

1. Valmistage ette uus Project Operationsi Dataverse’i juurutuse keskkond, järgides juhiseid teemas [Dataverse’i juurutuse mudel](lite-deployment.md). Keskkonnatüübi valimisel kasutage kindlasti valikut **Prooviversioon (tellimusepõhine)**.

  ![Uus keskkond](./media/19CreateEnvironment.png)

2. Valige säte **Luba Dynamics 365 rakendused** ja jätke väli **Juuruta neid rakendusi automaatselt** tühjaks.  
3. Keskkonna loomiseks valige nupp **Salvesta**.

  ![Lisa andmebaas](./media/20CreateEnvironment1.png)

4. Pärast keskkonna loomist installige **Microsofti Dynamics 365 Project Operations** lahendus. 

![Lahenduse installimine](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS-i konfiguratsiooni ja seadistuse demoandmete installimine

Installige CDS-i konfiguratsioon ja seadistage demoandmed, järgides juhiseid teemas [Demoseadistamise ja konfiguratsiooniandmete rakendamine](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
