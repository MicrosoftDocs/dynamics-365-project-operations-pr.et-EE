---
title: Projekti hinnapakkumiste haldamine
description: Selles teemas antakse teavet projekti hinnapakkumiste kohta.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87921221ea210e67a3ddc53bd124f292de80de99
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272923"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="0cdae-103">Projekti hinnapakkumiste haldamine</span><span class="sxs-lookup"><span data-stu-id="0cdae-103">Manage project quotes</span></span>

<span data-ttu-id="0cdae-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="0cdae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0cdae-105">Rakenduses Dynamics 365 Project Operations on projekti hinnapakkumised loodud aitamaks projektipõhise töö ettepanekute koostamisel.</span><span class="sxs-lookup"><span data-stu-id="0cdae-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="0cdae-106">Project Operationsi projekti hinnapakkumise struktuur on loodud projekti hinnapakkumistele koos järgmiste komponentidega.</span><span class="sxs-lookup"><span data-stu-id="0cdae-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="0cdae-107">Hinnapakkumise read, mis määratlevad töö eraldi komponendid, mis esitatakse kõrgetasemeliste komponentidena.</span><span class="sxs-lookup"><span data-stu-id="0cdae-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="0cdae-108">Hinnapakkumise rea üksikasjad, mis määratlevad ja hindavad iga kõrgetasemelise komponendi või hinnapakkumise rea tööd.</span><span class="sxs-lookup"><span data-stu-id="0cdae-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="0cdae-109">Töö ajakava või kuupäeva hinnangud ja finantsaspektid on seotud selle hinnapakkumise reaga.</span><span class="sxs-lookup"><span data-stu-id="0cdae-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="0cdae-110">Iga hinnapakkumise rea jaoks seadistatakse lepingulised mudelid ja tasustatavad komponendid.</span><span class="sxs-lookup"><span data-stu-id="0cdae-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="0cdae-111">See seadistus aitab hinnata iga hinnapakkumise rea ja kogu hinnapakkumise tulu, kulutuste ja tasuvuse jaotumist.</span><span class="sxs-lookup"><span data-stu-id="0cdae-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="0cdae-112">Kõikide projektipõhiste hinnapakkumiste vaade</span><span class="sxs-lookup"><span data-stu-id="0cdae-112">View all project-based quotes</span></span>

<span data-ttu-id="0cdae-113">Kõigi projekti hinnapakkumiste loendit saab vaadata loendi **Hinnapakkumised** lehel.</span><span class="sxs-lookup"><span data-stu-id="0cdae-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="0cdae-114">Minge jaotisse **Müük** > **Hinnapakkumised**.</span><span class="sxs-lookup"><span data-stu-id="0cdae-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="0cdae-115">Kuvatakse loend kõikide teie projekti hinnapakkumistega.</span><span class="sxs-lookup"><span data-stu-id="0cdae-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="0cdae-116">Kasutage hinnapakkumise teiste filtreeritud vaadete valimiseks suvandit **Vaatevahetaja**.</span><span class="sxs-lookup"><span data-stu-id="0cdae-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="0cdae-117">Kohandatud filtri kriteeriumide abil saate konfigureerida oma vaateid ja navigeerimise suvandeid.</span><span class="sxs-lookup"><span data-stu-id="0cdae-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="0cdae-118">Hinnapakkumisi saab luua või kustutada sellelt loendi lehelt või üksikasjade lehtedelt.</span><span class="sxs-lookup"><span data-stu-id="0cdae-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]