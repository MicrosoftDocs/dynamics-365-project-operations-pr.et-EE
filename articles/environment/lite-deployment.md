---
title: Project Operationsi juurutamine – liht
description: See artikkel annab teavet selle kohta, kuidas installida Project Operations Lite’i juurutust – tehing näidisarveldusele.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930313"
---
# <a name="deploy-project-operations---lite"></a>Project Operationsi juurutamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_



Project Operations toetab mitut juurutusmudelit. Parima juurutuse mudeli määratlemiseks vaadake teemat [Juurutuse tüübid](determine-deployment-type.md).


> [!IMPORTANT]
> Selle juurutuse (Lite’i juurutus – tehing näidisarveldusele) tulemuseks on **Project Operationsi ainult Dataverse’i juurutus**.

- [Project Operationsi installimine uude Dataverse keskkonda](#new)
- [Installimine olemasolevasse Dataverse keskkonda](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Project Operationsi installimine uude Dataverse keskkonda

1. [Globaalse või teenuse Power Platform administraatorina](/power-platform/admin/global-service-administrators-can-administer-without-license), kellel on rakenduse Project Operations litsents, saate luua uue Dataverse keskkonna [Halduskeskuses PowerPlatform](https://admin.powerplatform.com). Veenduge, et **Selle keskkonna jaoks andmebaasi loomine** ja **Dynamics 365 rakendused** on lubatud. Lisateavet vaadake teemast [Keskkondade loomine ja haldamine Power Platformi halduskeskuses](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Valige Dynamics 365 rakenduste juurutamise loendist **Microsoft Dynamics 365 Project Operations**.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Project Operationsi installimine olemasolevasse Dataverse keskkonda
1. Veenduge, et keskkonda poleks konfigureeritud [kahekordne kirjutamine](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), sest siis paigaldatakse [Project Operationsi ressursipõhiste/logimata stsenaariumide jaoks](project-operations-integrated-deployment-overview.md) võimalused.
2. [Globaalse või Power Platformi administraatorina](/power-platform/admin/global-service-administrators-can-administer-without-license), kellel on Project Operationsi litsents, leidke [PowerPlatformi halduskeskuses](https://admin.powerplatform.com) keskkond, kuhu soovite rakenduse Project Operations installida.
3. Installige Dynamics 365 rakenduste juurutamise loendist **Microsoft Dynamics 365 Project Operations**. Lisateavet leiate teemast [Dynamics 365 rakenduste haldamine](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
