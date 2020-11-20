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
ms.openlocfilehash: 3c33adabbd03cca19ae5e7f401f08a716e9242b2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177821"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="2e70f-103">Projekti hinnapakkumiste haldamine</span><span class="sxs-lookup"><span data-stu-id="2e70f-103">Manage project quotes</span></span>

<span data-ttu-id="2e70f-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="2e70f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2e70f-105">Rakenduses Dynamics 365 Project Operations on projekti hinnapakkumised loodud aitamaks projektipõhise töö ettepanekute koostamisel.</span><span class="sxs-lookup"><span data-stu-id="2e70f-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="2e70f-106">Project Operationsi projekti hinnapakkumise struktuur on loodud projekti hinnapakkumistele koos järgmiste komponentidega.</span><span class="sxs-lookup"><span data-stu-id="2e70f-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="2e70f-107">Hinnapakkumise read, mis määratlevad töö eraldi komponendid, mis esitatakse kõrgetasemeliste komponentidena.</span><span class="sxs-lookup"><span data-stu-id="2e70f-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="2e70f-108">Hinnapakkumise rea üksikasjad, mis määratlevad ja hindavad iga kõrgetasemelise komponendi või hinnapakkumise rea tööd.</span><span class="sxs-lookup"><span data-stu-id="2e70f-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="2e70f-109">Töö ajakava või kuupäeva hinnangud ja finantsaspektid on seotud selle hinnapakkumise reaga.</span><span class="sxs-lookup"><span data-stu-id="2e70f-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="2e70f-110">Iga hinnapakkumise rea jaoks seadistatakse lepingulised mudelid ja tasustatavad komponendid.</span><span class="sxs-lookup"><span data-stu-id="2e70f-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="2e70f-111">See seadistus aitab hinnata iga hinnapakkumise rea ja kogu hinnapakkumise tulu, kulutuste ja tasuvuse jaotumist.</span><span class="sxs-lookup"><span data-stu-id="2e70f-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="2e70f-112">Kõikide projektipõhiste hinnapakkumiste vaade</span><span class="sxs-lookup"><span data-stu-id="2e70f-112">View all project-based quotes</span></span>

<span data-ttu-id="2e70f-113">Kõigi projekti hinnapakkumiste loendit saab vaadata loendi **Hinnapakkumised** lehel.</span><span class="sxs-lookup"><span data-stu-id="2e70f-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="2e70f-114">Minge jaotisse **Müük** > **Hinnapakkumised**.</span><span class="sxs-lookup"><span data-stu-id="2e70f-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="2e70f-115">Kuvatakse loend kõikide teie projekti hinnapakkumistega.</span><span class="sxs-lookup"><span data-stu-id="2e70f-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="2e70f-116">Kasutage hinnapakkumise teiste filtreeritud vaadete valimiseks suvandit **Vaatevahetaja**.</span><span class="sxs-lookup"><span data-stu-id="2e70f-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="2e70f-117">Kohandatud filtri kriteeriumide abil saate konfigureerida oma vaateid ja navigeerimise suvandeid.</span><span class="sxs-lookup"><span data-stu-id="2e70f-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="2e70f-118">Hinnapakkumisi saab luua või kustutada sellelt loendi lehelt või üksikasjade lehtedelt.</span><span class="sxs-lookup"><span data-stu-id="2e70f-118">Quotes can be created or deleted from this list page or detail pages.</span></span>
