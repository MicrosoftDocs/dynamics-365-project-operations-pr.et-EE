---
title: Project Operationsi registreerumine eelvaate kordustellimusele ressursside/mitte laosolevate stsenaariumite jaoks
description: Sellest artiklist leiate teavet selle kohta, kuidas tellida ja juurutada projektitoiminguid ressursipõhiste/varudeta stsenaariumide jaoks.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3164add153d77a52f85c2aac442dcf90baa24440
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/10/2022
ms.locfileid: "9842010"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Project Operationsi registreerumine eelvaate kordustellimusele ressursside/mitte laosolevate stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_



See artikkel kirjeldab, kuidas tellida prooviversiooni ja juurutada Project Operationsi keskkonda ressursipõhistes/mittelaopõhistes stsenaariumides.

## <a name="prerequisites"></a>Eeltingimused
- Kasutajal, kes eelvaate juurutab, peab olema Azure'i rentniku globaalse administraatori õigused. Rentniku saate luua esimese pakkumise lunastamise ajal. 
- Finance'i keskkonna juurutamiseks on vaja kehtivat Azure'i tellimust, mida arveldatakse keskkonna põhiselt. Alustamiseks võite kasutada oma organisatsiooni olemasolevat kordustellimust või kasutada [Azure'i prooviversiooni](https://azure.microsoft.com/free/). CDS-i keskkonda pakutakse piiratud 30-päevase perioodi jooksul tasuta.

> [!IMPORTANT]
> Selle toimingu peab organisatsioonis tegema ainult üks inimene, rentniku administraator. Kui te pole selle väljalaske tellija, oodake, kuni teie organisatsioon on registreeritud ja teile on saadetud kasutaja mandaat.
> 
> Prooviversioonid on rentnikus ühekordselt kasutatav. Prooviversiooni saab käitada ainult üks kord. Soovitame teil luua prooviversiooni eesmärgil uus rentnik.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) – eelversiooni prooviversioon 

Enne alustamist veenduge, et oleksite brauseris sisse logitud kasutaja töökontoga rentnikusse, kus soovite Project Operationsi eelvaadet näha.

1. Lunastage esimene pakkumise kood **Dynamics 365 Project Operations** siin [Project Operationsi prooviversioon](https://aka.ms/try-po).
2. Kinnitage oma tellimus.

  Näete, et kinnituse pakkumine on edukalt lunastatud.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance’i prooviversiooni eelvaade

Minge jaotisse [Dynamics 365 for Finance eelversiooni prooviversioon](https://aka.ms/trypoche) ja korrake pakkumisega eelmise jaotise juhiseid, registreeruge pilvmajutusega keskkondade jaoks.  

## <a name="assign-licenses"></a>Litsentside määramine

> [!IMPORTANT]
> Järgmiste toimingute lõpuleviimiseks on teil vaja oma organisatsiooni Microsoft 365 portaali administraatori juurdepääsu.

1. Oma kasutajatele litsentside määramiseks avage [Microsoft 365 halduskeskus](https://portal.office.com/).

2. Valige lehel **Aktiivsed kasutajad** need kasutajad, kellele soovite litsentsi määrata.

3. Kontrollige, kas litsents **Dynamics 365 Project Operations** on valitud, ja valige käsk **Salvesta muudatused**.

> [!NOTE]
> Finance'i prooviversiooni pakkumist ei pea kasutajale määrama.

## <a name="start-a-new-project-in-lcs"></a>LCS-is uue projekti alustamine

Looge uus LCS-i projekt, nagu kirjeldatud artiklis [LCS-is uue projekti alustamine](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Azure’i kordustellimuse lisamine LCS-i projektile

Selle ülesande lõpuleviimiseks järgige juhiseid artiklis [Azure’i tellimuse lisamine LCS-i projektile](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Finance'i demokeskkonna juurutamine Project Operationsiga ressursi/mitte laosoleva stsenaariumide jaoks

Juurutuse lõpuleviimiseks järgige juhiseid artiklis [Uue keskkonna ettevalmistamine](resource-provision-new-environment.md). Kasutage eelversiooni korral [demokeskkonna](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) juurutuse tüüpi. 

## <a name="install-cds-setup-and-configuration-data"></a>CDS-i seadistuse ja konfiguratsiooniandmete installimine

Installige artiklis kirjeldatud CDS-i seadistuse ja konfiguratsiooni andmed, [Seadistage ja rakendage konfiguratsiooni andmeid rakenduses Common Data Service](resource-apply-pro-setup-config-data.md).
Viige see etapp lõpule alles pärast teenuse Finance juurutamist ja kui demoandmed on valmis.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
