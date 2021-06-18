---
title: Eelversiooni kordustellimuseks registreerumine – liht
description: See teema pakub teavet selle kohta, kuidas tellida ja juurutada Project Operations Lite’i juurutust – tehing näidisarveldusele.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4de51277e5a08690cc16497e3916f40498b39fb8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997416"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Eelversiooni kordustellimuseks registreerumine – liht 

Selles teemas kirjeldatakse, kuidas tellida partnerpakkumise eelversiooni ja juurutada Dynamics 365 Project Operationsi  lihtjuurutamine – tehing näidisarveldusele.

> [!NOTE]
> See toiming muutub Project Operationsi eelseisvates väljaannetes.

## <a name="prerequisites"></a>Eeltingimused

- Teile saadetakse meil, mis kutsub teid eelvaates osalema. Eelvaadet saate taotleda [Project Operationsi veebisaidilt](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Kasutajal, kes eelvaate juurutab, peab olema Azure'i rentniku globaalse administraatori õigused.
- Vaadake üle kõik tingimused.

## <a name="subscribe"></a>Telli

Kui saate [eelvaate taotluse](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) kinnituse, saadab Microsoft teile maili teel kaks pakkumist. Need pakkumised võimaldavad teil juurutada Project Operationsi eelvaate.

- Dynamics 365 Project Operations (CRM) – eelversiooni prooviversioon
- Office 365 Project Operations –eelvaate prooviversioon

> [!IMPORTANT]
> Selle toimingu peab organisatsioonis tegema ainult üks inimene, rentniku administraator. Kui te pole selle väljalaske tellija, oodake, kuni teie organisatsioon on registreeritud ja teile on saadetud kasutaja mandaat.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – eelversiooni prooviversioon 

Enne alustamist veenduge, et oleksite brauseris sisse logitud kasutaja töökontoga rentnikusse, kus soovite Project Operationsi eelvaadet näha.

1. Lunastage esimese pakkumise kood **Dynamics 365 Project Operations (CRM) – eelversiooni prooviversioon**, kleepides selle brauseri URL-i.

![Lunasta pakkumine](./media/16RedeemFirstOfferNew.png)

2. Kinnitage oma tellimus.
![Tellimuse kinnitamine](./media/17ConfirmOrderNew.png)

Näete, et kinnituse pakkumine on edukalt lunastatud.

![Kinnitus](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations –eelvaate prooviversioon

Korrake samu toiminguid nagu esimese pakkumise koodiga. Lisage kindlasti teine pakkumise kood sama kasutajakontoga, mida kasutati esimese pakkumise koodiga.

## <a name="assign-licenses"></a>Litsentside määramine

> [!IMPORTANT]
> Järgmiste toimingute lõpuleviimiseks on teil vaja oma organisatsiooni Microsoft 365 portaali administraatori juurdepääsu.


1. Oma kasutajatele litsentside määramiseks avage [Microsofti 365 halduskeskus](https://portal.office.com/).

![Halduskeskuse avaleht](./media/14AdminPortal.png)

2. Valige lehel **Aktiivsed kasutajad** need kasutajad, kellele soovite litsentsi määrata.

![Litsentside määramine](./media/15AssignLicenses.png)

3. Veenduge, et **Dynamics 365 Project Operations (CRM) eelversiooni** ja **Office 365 Project Operations - eelversiooni** litsentsid oleksid valitud. 
4. Valige käsk **Salvesta muudatused**.

## <a name="create-a-new-cds-environment"></a>Uue CDS-i keskkonna loomine

1. Valmistage ette uus Project Operationsi CDS-i juurutuse keskkond, järgides juhiseid teemas [CDS-i juurutuse mudel](lite-deployment.md). Keskkonnatüübi valimisel kasutage kindlasti valikut **Prooviversioon (tellimusepõhine)**.
![Uus keskkond](./media/19CreateEnvironment.png)

2. Valige säte **Luba Dynamics 365 rakendused** ja jätke väli **Juuruta neid rakendusi automaatselt** tühjaks.  
3. Keskkonna loomiseks valige nupp **Salvesta**.

![Lisa andmebaas](./media/20CreateEnvironment1.png)

4. Pärast keskkonna loomist installige **Microsofti Dynamics 365 Project Operations** lahendus. 

![Lahenduse installimine](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS-i konfiguratsiooni ja seadistuse demoandmete installimine

Installige CDS-i konfiguratsioon ja seadistage demoandmed, järgides juhiseid teemas [Demoseadistamise ja konfiguratsiooniandmete rakendamine](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]