---
title: Project Operationsi juurutamine – liht
description: See teema pakub teavet selle kohta, kuidas installida Project Operations Lite’i juurutust – tehing näidisarveldusele.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0633585fcef91d9218d6140764addb7cf96ab31d
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175661"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="17255-103">Project Operationsi juurutamine – liht</span><span class="sxs-lookup"><span data-stu-id="17255-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="17255-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="17255-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="17255-105">Project Operations toetab mitut juurutusmudelit.</span><span class="sxs-lookup"><span data-stu-id="17255-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="17255-106">Parima juurutuse mudeli määratlemiseks vaadake teemat [Juurutuse tüübid](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="17255-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="17255-107">Selle juurutuse (Lite’i juurutus – tehing näidisarveldusele) tulemuseks on **Project Operationsi ainult Common Data Service’i juurutus**.</span><span class="sxs-lookup"><span data-stu-id="17255-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="17255-108">Project Operationsi installimine uude CDS-i keskkonda</span><span class="sxs-lookup"><span data-stu-id="17255-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="17255-109">Installimine olemasolevasse CDS-i keskkonda</span><span class="sxs-lookup"><span data-stu-id="17255-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="17255-110">Project Operationsi installimine uude CDS-i keskkonda</span><span class="sxs-lookup"><span data-stu-id="17255-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="17255-111">[Globaalse või Power Platformi administraatorina](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license), kellel on Project Operationsi litsents, saate luua [PowerPlatformi halduskeskuses](https://admin.powerplatform.com) uue CDS-i keskkonna.</span><span class="sxs-lookup"><span data-stu-id="17255-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="17255-112">Veenduge, et **CDS-i andmebaas** ja **Dynamics 365 rakendused** oleksid lubatud.</span><span class="sxs-lookup"><span data-stu-id="17255-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="17255-113">Lisateavet vaadake teemast [Keskkondade loomine ja haldamine Power Platformi halduskeskuses](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="17255-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="17255-114">Valige Dynamics 365 rakenduste juurutuste loendist **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="17255-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="17255-115">Project Operationsi installimine olemasolevasse CDS-i keskkonda</span><span class="sxs-lookup"><span data-stu-id="17255-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="17255-116">[Globaalse või Power Platformi administraatorina](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license), kellel on Project Operationsi litsents, leidke [PowerPlatformi halduskeskuses](https://admin.powerplatform.com) keskkond, kuhu soovite rakenduse Project Operations installida.</span><span class="sxs-lookup"><span data-stu-id="17255-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="17255-117">Installige Dynamics 365 rakenduste juurutuste loendist **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="17255-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="17255-118">Lisateavet leiate teemast [Dynamics 365 rakenduste haldamine](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="17255-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


