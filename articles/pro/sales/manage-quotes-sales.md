---
title: Projekti hinnapakkumiste haldamine
description: Selles teemas antakse teavet projekti hinnapakkumiste kohta.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8e0b20d4780a14edc3c242e261e22d4905f783a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994806"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="ce5bd-103">Projekti hinnapakkumiste haldamine</span><span class="sxs-lookup"><span data-stu-id="ce5bd-103">Manage project quotes</span></span>

<span data-ttu-id="ce5bd-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="ce5bd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ce5bd-105">Rakenduses Dynamics 365 Project Operations on projekti hinnapakkumised loodud aitamaks projektipõhise töö ettepanekute koostamisel.</span><span class="sxs-lookup"><span data-stu-id="ce5bd-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="ce5bd-106">Project Operationsi projekti hinnapakkumise struktuur on loodud projekti hinnapakkumistele koos järgmiste komponentidega.</span><span class="sxs-lookup"><span data-stu-id="ce5bd-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="ce5bd-107">Hinnapakkumise read, mis määratlevad töö eraldi komponendid, mis esitatakse kõrgetasemeliste komponentidena.</span><span class="sxs-lookup"><span data-stu-id="ce5bd-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="ce5bd-108">Hinnapakkumise rea üksikasjad, mis määratlevad ja hindavad iga kõrgetasemelise komponendi või hinnapakkumise rea tööd.</span><span class="sxs-lookup"><span data-stu-id="ce5bd-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="ce5bd-109">Töö ajakava või kuupäeva hinnangud ja finantsaspektid on seotud selle hinnapakkumise reaga.</span><span class="sxs-lookup"><span data-stu-id="ce5bd-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="ce5bd-110">Iga hinnapakkumise rea jaoks seadistatakse lepingulised mudelid ja tasustatavad komponendid.</span><span class="sxs-lookup"><span data-stu-id="ce5bd-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="ce5bd-111">See seadistus aitab hinnata iga hinnapakkumise rea ja kogu hinnapakkumise tulu, kulutuste ja tasuvuse jaotumist.</span><span class="sxs-lookup"><span data-stu-id="ce5bd-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="ce5bd-112">Kõikide projektipõhiste hinnapakkumiste vaade</span><span class="sxs-lookup"><span data-stu-id="ce5bd-112">View all project-based quotes</span></span>

<span data-ttu-id="ce5bd-113">Kõigi projekti hinnapakkumiste loendit saab vaadata loendi **Hinnapakkumised** lehel.</span><span class="sxs-lookup"><span data-stu-id="ce5bd-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="ce5bd-114">Minge jaotisse **Müük** > **Hinnapakkumised**.</span><span class="sxs-lookup"><span data-stu-id="ce5bd-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="ce5bd-115">Kuvatakse loend kõikide teie projekti hinnapakkumistega.</span><span class="sxs-lookup"><span data-stu-id="ce5bd-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="ce5bd-116">Kasutage hinnapakkumise teiste filtreeritud vaadete valimiseks suvandit **Vaatevahetaja**.</span><span class="sxs-lookup"><span data-stu-id="ce5bd-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="ce5bd-117">Kohandatud filtri kriteeriumide abil saate konfigureerida oma vaateid ja navigeerimise suvandeid.</span><span class="sxs-lookup"><span data-stu-id="ce5bd-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="ce5bd-118">Hinnapakkumisi saab luua või kustutada sellelt loendi lehelt või üksikasjade lehtedelt.</span><span class="sxs-lookup"><span data-stu-id="ce5bd-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]