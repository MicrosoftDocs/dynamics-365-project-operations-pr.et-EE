---
title: Projekti müügitellimused aja- ja materjalikulu projektidele
description: Selles teemas selgitatakse, kuidas luua aja- ja materjalikulu projektidele projektipõhiseid müügitellimusi.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009656"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="eaee9-103">Projekti müügitellimused aja- ja materjalikulu projektidele</span><span class="sxs-lookup"><span data-stu-id="eaee9-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="eaee9-104">Selles teemas kirjeldatakse, kuidas luua projekti jaoks müügitellimust.</span><span class="sxs-lookup"><span data-stu-id="eaee9-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="eaee9-105">Müügitellimusi saab luua ainult **aja- ja materjalikulu** tüüpi projektidele.</span><span class="sxs-lookup"><span data-stu-id="eaee9-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="eaee9-106">Kui aja- ja materjalikulu projektil on projekti lepingus mitu rahastamisallikat, peate lubama lehel **Projektihalduse ja raamatupidamise parameetrid** parameetri **Luba mitme rahastamisallikaga projekti jaoks müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="eaee9-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="eaee9-107">Mitme rahastamisallikaga projekti müügitellimuste tugi on saadaval alates rakenduse väljalaskest 10.0.2 ja uuemad versioonid.</span><span class="sxs-lookup"><span data-stu-id="eaee9-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="eaee9-108">Mitme rahastamisallikaga projekti müügitellimuste toe lubamise parameeter eemaldatakse 2020. aasta aprilli väljalaske lainest, pärast mida on funktsioon alati lubatud.</span><span class="sxs-lookup"><span data-stu-id="eaee9-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="eaee9-109">Projektipõhiseid müügitellimusi saate luua kahel viisil.</span><span class="sxs-lookup"><span data-stu-id="eaee9-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="eaee9-110">Avage projekt ise.</span><span class="sxs-lookup"><span data-stu-id="eaee9-110">Go to the project itself.</span></span> <span data-ttu-id="eaee9-111">Valige tegevuspaanil suvand **Halda > Üksuse tööülesanded > Müügitellimus**.</span><span class="sxs-lookup"><span data-stu-id="eaee9-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="eaee9-112">Projekti teave kuvatakse vaikimisi projekti müügitellimuses.</span><span class="sxs-lookup"><span data-stu-id="eaee9-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="eaee9-113">Kui projekti lepingus on rohkem kui üks rahastamisallikas, peate valima rahastamisallika, et määrata müügitellimusele klient.</span><span class="sxs-lookup"><span data-stu-id="eaee9-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="eaee9-114">Kui projektil on ainult üks rahastamisallikas, määratakse klient automaatselt.</span><span class="sxs-lookup"><span data-stu-id="eaee9-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="eaee9-115">Avage loendi leht **Kõik müügitellimused** ja looge uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="eaee9-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="eaee9-116">Peate valima müügitellimuse jaoks projekti.</span><span class="sxs-lookup"><span data-stu-id="eaee9-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="eaee9-117">Pärast projekti valimist määratakse klient rahastamisallikast või teil tuleb valida rahastamisallikas, kui projekti lepingus on mitu rahastamisallikat.</span><span class="sxs-lookup"><span data-stu-id="eaee9-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]