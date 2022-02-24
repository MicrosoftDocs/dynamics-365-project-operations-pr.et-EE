---
title: Project Operationsi registreerumine eelvaate kordustellimusele ressursside/mitte laosolevate stsenaariumite jaoks
description: Selles teemas antakse teavet Project Operationsi tellimise ja juurutamise kohta ressursi-/mitte laosolevate stsenaariumite jaoks.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 917ead8ff6d9d3ef8374f8ccde608b6cebd50c8c
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948459"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Project Operationsi registreerumine eelvaate kordustellimusele ressursside/mitte laosolevate stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas selgitatakse, kuidas tellida eelvaadet/partneri pakkumist ja juurutada Project Operationsi keskkonda ressursi/mitte laosoleva põhiste stsenaariumide jaoks.

## <a name="prerequisites"></a>Eeltingimused

- Teile saadetakse meil, mis kutsub teid eelvaates osalema. Eelvaadet saate taotleda [Project Operationsi veebisaidilt](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Kasutajal, kes eelvaate juurutab, peab olema Azure'i rentniku globaalse administraatori õigused.
- Finance'i keskkonna juurutamiseks on vaja kehtivat Azure'i tellimust, mida arveldatakse keskkonna põhiselt. Alustamiseks võite kasutada oma organisatsiooni olemasolevat kordustellimust või kasutada [Azure'i prooviversiooni](https://azure.microsoft.com/en-us/free/). CDS-i keskkonda pakutakse piiratud 30-päevase perioodi jooksul tasuta.

## <a name="subscribe"></a>Telli

Kui teie [eelvaate taotlus](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) kinnitatakse, saadab Microsoft teile maili teel kolm pakkumist. Need pakkumised võimaldavad teil juurutada Project Operationsi eelvaate.

- Dynamics 365 Project Operations (CRM) – eelversiooni prooviversioon
- Office 365 Project Operations –eelvaate prooviversioon
- Dynamics 365 Finance - eelversiooni prooviversioon

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

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance'i eelversiooni prooviversioon

Korrake samu samme tervitusmeili viimase pakkumisega.

## <a name="assign-licenses"></a>Litsentside määramine

> [!IMPORTANT]
> Järgmiste toimingute lõpuleviimiseks on teil vaja oma organisatsiooni Microsoft 365 portaali administraatori juurdepääsu.

1. Oma kasutajatele litsentside määramiseks avage [Microsofti 365 halduskeskus](https://portal.office.com/).

![Halduskeskuse avaleht](./media/14AdminPortal.png)

2. Valige lehel **Aktiivsed kasutajad** need kasutajad, kellele soovite litsentsi määrata.

![Litsentside määramine](./media/15AssignLicenses.png)

3. Veenduge, et valitud oleksid litsentsid **Dynamics 365 Project Operations (CRM), eelversioon** ja **Office 365 Project Operations – eelversioon** ja valige suvand **Salvesta muudatused**.

> [!NOTE]
> Finance'i prooviversiooni pakkumist ei pea kasutajale määrama.

## <a name="start-a-new-project-in-lcs"></a>LCS-is uue projekti alustamine

Looge uus LCS-i projekt, nagu kirjeldatud teemas [LCS-is uue projekti alustamine](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Azure’i kordustellimuse lisamine LCS-i projektile

Selle toimingu lõpuleviimiseks järgige juhiseid teemas [Azure'i tellimuse lisamine LCS-i projektile](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Finance'i demokeskkonna juurutamine Project Operationsiga ressursi/mitte laosoleva stsenaariumide jaoks

Juurutuse lõpuleviimiseks järgige juhiseid teemas [Uue keskkonna ettevalmistamine](resource-provision-new-environment.md). Kasutage eelversiooni korral [demokeskkonna](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) juurutuse tüüpi. 

## <a name="install-cds-setup-and-configuration-data"></a>CDS-i seadistuse ja konfiguratsiooniandmete installimine

Installige teemas kirjeldatud CDS-i seadistuse ja konfiguratsiooni andmed, [Seadistage ja rakendage konfiguratsiooni andmeid rakenduses Common Data Service](resource-apply-pro-setup-config-data.md).
Läbige see etapp alles pärast Finance'i demokeskkonna juurutamist ja kui demoandmed FO-s on valmis.


[!INCLUDE[footer-include](../includes/footer-banner.md)]