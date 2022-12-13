---
title: Juuruta projekti toimingud Lite
description: See artikkel annab teavet selle kohta, kuidas installida Project Operations Lite’i juurutust – tehing näidisarveldusele.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810973"
---
# <a name="deploy-project-operations-lite"></a>Juuruta projekti toimingud Lite

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_



Project Operations toetab mitut juurutusmudelit. Parima juurutuse mudeli määratlemiseks vaadake teemat [Juurutuse tüübid](determine-deployment-type.md).


> [!IMPORTANT]
> Selle juurutuse (Lite’i juurutus – tehing näidisarveldusele) tulemuseks on **Project Operationsi ainult Dataverse’i juurutus**.

- [Project Operationsi installimine uude Dataverse keskkonda](#new)
- [Installimine olemasolevasse Dataverse keskkonda](#existing)
- [Installimine olemasolevasse Dataverse keskkonda, millel on kaks kirjutuskomponenti](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a> Project Operations Lite’i installimine uude Dataverse keskkonda

1. [Globaalse või teenuse Power Platform administraatorina](/power-platform/admin/global-service-administrators-can-administer-without-license), kellel on rakenduse Project Operations litsents, saate luua uue Dataverse keskkonna [Halduskeskuses PowerPlatform](https://admin.powerplatform.com). Veenduge, et **Selle keskkonna jaoks andmebaasi loomine** ja **Dynamics 365 rakendused** on lubatud. Lisateavet vaadake teemast [Keskkondade loomine ja haldamine Power Platformi halduskeskuses](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Valige Dynamics 365 rakenduste juurutamise loendist **Microsoft Dynamics 365 Project Operations**.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a> Project Operations Lite’i installimine olemasolevasse Dataverse keskkonda 
1. [Globaalse või Power Platformi administraatorina](/power-platform/admin/global-service-administrators-can-administer-without-license), kellel on Project Operationsi litsents, leidke [PowerPlatformi halduskeskuses](https://admin.powerplatform.com) keskkond, kuhu soovite rakenduse Project Operations installida.
1. Installige Dynamics 365 rakenduste juurutamise loendist **Microsoft Dynamics 365 Project Operations**. Lisateavet leiate teemast [Dynamics 365 rakenduste haldamine](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> Project Operations Lite’i installimine olemasolevasse Dataverse keskkonda, kus topeltkirjutuslahendused on juba olemas

Kui soovite jätkata Project Operationsi käitamist režiimis Lite juurutus, toimige järgmiselt.

1. [Globaalse või Power Platformi administraatorina](/power-platform/admin/global-service-administrators-can-administer-without-license), kellel on Project Operationsi litsents, leidke [PowerPlatformi halduskeskuses](https://admin.powerplatform.com) keskkond, kuhu soovite rakenduse Project Operations installida.
1. Installige Dynamics 365 rakenduste juurutamise loendist **Microsoft Dynamics 365 Project Operations**. Lisateavet leiate teemast [Dynamics 365 rakenduste haldamine](/power-platform/admin/manage-apps).
1. Kuna teie keskkonnas on topeltkirjutuskomponendid, mis aitavad integreerida installitud rakendustesse Finance and Operations, installib Project Operationsi install ka võimalused ja laiendid, mis on vajalikud projektiga seotud andmete integreerimiseks Finance and Operationsi rakendustesse. Kuna soovite käivitada Project Operationsi Lite’i juurutuses, tuleks need integratsioonikomponendid eemaldada, kuna need loovad piiranguid ja üldkulusid Lite’i juurutusstsenaariumidele. Nende komponentide eemaldamiseks desinstallige lahendused **Dynamics 365 Project Operations Dual Write ja** Dual Write **Dynamics 365 Project Operations Entity Maps** käsitsi.
1. Avage Project **Operations -> Settings -> Parameters**.  **Avage leht Projekti parameetri** üksikasjad ja määrake **välja Lahenduse täiendamise käitumine** väärtuseks **Ainult** Liit. See tagab, et Project Operationsi hilisemad täiendused ei too integratsioonikomponente tagasi Project Operationsisse.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
