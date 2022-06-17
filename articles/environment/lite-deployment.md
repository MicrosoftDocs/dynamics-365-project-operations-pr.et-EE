---
title: Project Operationsi juurutamine – liht
description: Selles artiklis antakse teavet selle kohta, kuidas installida Project Operations lite juurutus - tegeleda proforma arveldusega.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930313"
---
# <a name="deploy-project-operations---lite"></a>Project Operationsi juurutamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_



Project Operations toetab mitut juurutusmudelit. Parima juurutuse mudeli määratlemiseks vaadake teemat [Juurutuse tüübid](determine-deployment-type.md).


> [!IMPORTANT]
> Selle juurutuse (Lite’i juurutus – tehing näidisarveldusele) tulemuseks on **Project Operationsi ainult Dataverse’i juurutus**.

- [Projektitoimingute installimine uude Dataverse keskkonda](#new)
- [Installige olemasolevasse Dataverse keskkonda](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> Projektitoimingute installimine uude Dataverse keskkonda

1. [Projektitoimingute litsentsiga globaal- või Power Platform administraatorina](/power-platform/admin/global-service-administrators-can-administer-without-license) looge PowerPlatformi Dataverse halduskeskuses [uus](https://admin.powerplatform.com) keskkond. Veenduge, et **selle keskkonna** jaoks andmebaasi loomine ja **Dynamics 365 rakendused** oleksid lubatud. Lisateavet vaadake teemast [Keskkondade loomine ja haldamine Power Platformi halduskeskuses](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Valige Dynamics 365 rakenduste juurutamise loendist **Microsoft Dynamics 365 Project Operations**.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Projektitoimingute installimine olemasolevasse Dataverse keskkonda
1. Veenduge, et keskkonda pole konfigureeritud [topeltkirjutamisega](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), kuna installimine installib [seejärel projektitoimingud ressursi/ ladustamata põhistsenaariumide](project-operations-integrated-deployment-overview.md) võimaluste jaoks.
2. [Globaalse või Power Platformi administraatorina](/power-platform/admin/global-service-administrators-can-administer-without-license), kellel on Project Operationsi litsents, leidke [PowerPlatformi halduskeskuses](https://admin.powerplatform.com) keskkond, kuhu soovite rakenduse Project Operations installida.
3. Installige Dynamics 365 rakenduste juurutamise loendist **Microsoft Dynamics 365 Project Operations**. Lisateavet leiate teemast [Dynamics 365 rakenduste haldamine](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
