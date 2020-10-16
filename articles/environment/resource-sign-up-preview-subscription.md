---
title: Project Operationsi registreerumine eelvaate kordustellimusele ressursside/mitte laosolevate stsenaariumite jaoks
description: Selles teemas antakse teavet Project Operationsi tellimise ja juurutamise kohta ressursi-/mitte laosolevate stsenaariumite jaoks.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948832"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Project Operationsi registreerumine eelvaate kordustellimusele ressursside/mitte laosolevate stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles teemas selgitatakse, kuidas tellida eelvaadet/partneri pakkumist ja juurutada Project Operationsi keskkonda ressursi/mitte laosoleva põhiste stsenaariumide jaoks.

## <a name="prerequisites"></a>Eeltingimused

- Teile saadetakse meil, mis kutsub teid eelvaates osalema. Eelvaadet saate taotleda [Project Operationsi veebisaidilt](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Kasutajal, kes eelvaate juurutab, peab olema Azure'i rentniku globaalse administraatori õigused.
- Finance'i keskkonna juurutamiseks on vaja kehtivat Azure'i tellimust, mida arveldatakse keskkonna põhiselt. Alustamiseks võite kasutada oma organisatsiooni olemasolevat kordustellimust või kasutada [Azure'i prooviversiooni](https://azure.microsoft.com/en-us/free/). CDS-i keskkonda pakutakse piiratud 30-päevase perioodi jooksul tasuta.

## <a name="subscribe"></a>Telli

Kui teie [eelvaate taotlus](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) kinnitatakse, saadab Microsoft teile maili teel kaks pakkumist. Need pakkumised võimaldavad teil juurutada Project Operationsi eelvaate.

- Dynamics 365 Project Operations - Eelversiooni prooviversioon
- Dynamics 365 for Finance and Operationsi eelversiooni prooviversioon.

> [!IMPORTANT]
> Selle toimingu peab organisatsioonis tegema ainult üks inimene, rentniku administraator. Kui te pole selle väljalaske tellija, oodake, kuni teie organisatsioon on registreeritud ja teile on saadetud kasutaja mandaat.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations - Eelversiooni prooviversioon

1. Lunastage esimene pakkumine, **Dynamics 365 Project Operationsi prooviversioon**, mille URL on antud teie tervitusmeilis.

![Esimene pakkumine](./media/1FirstOffer.png)

2. Veenduge, et olete sisse logitud kasutajana, kes kuulub organisatsiooni, kes teenust tellib.
3. Jätkake pakkumise lunastamisega. 
4. Valige **Jah, lisage see minu kontole**.

![Lunasta pakkumine](./media/2RedeemFirstOffer.png)

![Kinnita pakkumine](./media/3ConfirmFirstOffer.png)

![Pakkumine lunastatud](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance'i eelversiooni prooviversioon

Korrake samu samme tervitusmeili teise pakkumisega.

## <a name="assign-licenses"></a>Litsentside määramine

> [!IMPORTANT]
> Järgmiste toimingute lõpuleviimiseks on teil vaja oma organisatsiooni Office 365 portaali administraatori juurdepääsu.

1. Oma kasutajatele litsentside määramiseks avage [Microsofti 365 halduskeskus](https://portal.office.com/).

![Office'i haldusportaal](./media/5OfficeAdminPortal.png)

2. Valige lehel **Aktiivsed kasutajad** need kasutajad, kellele soovite litsentsi määrata.

![Litsentside määramine](./media/6AssignLicenses.png)

3. Kontrollige, kas Project Oprationsi litsents on valitud ja valige **Salvesta muudatused**. 

> [!NOTE]
> Finance'i prooviversiooni pakkumist ei pea kasutajale määrama.

## <a name="start-a-new-project-in-lcs"></a>LCS-is uue projekti alustamine

Looge uus LCS-i projekt, nagu kirjeldatud teemas [LCS-is uue projekti alustamine](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Azure’i kordustellimuse lisamine LCS-i projektile

Selle toimingu lõpuleviimiseks järgige juhiseid teemas [Azure'i tellimuse lisamine LCS-i projektile](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Finance'i demokeskkonna juurutamine Project Operationsiga ressursi/mitte laosoleva stsenaariumide jaoks

Juurutuse lõpuleviimiseks järgige juhiseid teemas [Uue keskkonna ettevalmistamine](resource-provision-new-environment.md). Kasutage eelversiooni korral [demokeskkonna](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) juurutuse tüüpi.

## <a name="install-cds-setup-and-configuration-data"></a>CDS-i seadistuse ja konfiguratsiooniandmete installimine

Installige teemas kirjeldatud CDS-i seadistuse ja konfiguratsiooni andmed, [Seadistage ja rakendage konfiguratsiooni andmeid rakenduses Common Data Service](resource-apply-pro-setup-config-data.md).

