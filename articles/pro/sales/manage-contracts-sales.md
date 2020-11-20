---
title: Projektilepingute haldamine
description: See teema sisaldab teavet projektipõhiste lepingute vaatamise kohta.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441fbc378a423334f45bc65658811ef238515393
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177326"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="d7858-103">Projektilepingute haldamine</span><span class="sxs-lookup"><span data-stu-id="d7858-103">Manage project contracts</span></span>

<span data-ttu-id="d7858-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="d7858-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d7858-105">Rakenduse Dynamics 365 Project Operations projekti lepingud hõivavad ja haldavad lepinguga kokku lepitud projekti kohustusi ja arvedamise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="d7858-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="d7858-106">Project Operationsi projektilepingu struktuur on kohandatud projektipõhisele tööle koos järgmiste komponentidega.</span><span class="sxs-lookup"><span data-stu-id="d7858-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="d7858-107">Lepinguread, mis määratlevad töö eraldi komponendid, mis esitatakse projekti arvel kõrgetasemeliste komponentidena.</span><span class="sxs-lookup"><span data-stu-id="d7858-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="d7858-108">Lepingurea üksikasjad, mis määratlevad ja hindavad iga kõrgetasemelise komponendi või lepingurea tööd.</span><span class="sxs-lookup"><span data-stu-id="d7858-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="d7858-109">Prognoos sisaldab lepingureaga seotud töö ajakava ja finantsaspekte.</span><span class="sxs-lookup"><span data-stu-id="d7858-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="d7858-110">Lepingulised mudelid ja tasustatavad komponendid seadistatakse iga lepingurea jaoks, mis sisaldab iga lepingurea ja lepingu üldist arveldamise korraldust.</span><span class="sxs-lookup"><span data-stu-id="d7858-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="d7858-111">Kõikide projektipõhiste lepingute vaatamine</span><span class="sxs-lookup"><span data-stu-id="d7858-111">View all project-based contracts</span></span>

<span data-ttu-id="d7858-112">Kõigi projektilepingute loendit saab vaadata loendi **Lepingud** lehel.</span><span class="sxs-lookup"><span data-stu-id="d7858-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="d7858-113">Avage **Müük** > **Lepingud**.</span><span class="sxs-lookup"><span data-stu-id="d7858-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="d7858-114">Kuvatakse loend kõikide teie projektilepingutega.</span><span class="sxs-lookup"><span data-stu-id="d7858-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="d7858-115">Teiste filtreeritud vaadete valimiseks valige suvand **Vaatevahetaja** (vaate nime kõrval olev ripploendi nool).</span><span class="sxs-lookup"><span data-stu-id="d7858-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="d7858-116">Te saate luua kohandatud filtreerimiskriteeriumitega oma vaateid.</span><span class="sxs-lookup"><span data-stu-id="d7858-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="d7858-117">Lepinguid saab luua või kustutada sellelt loendi lehelt või üksikasjade lehtedelt.</span><span class="sxs-lookup"><span data-stu-id="d7858-117">Contracts can be created or deleted from this list page or detail pages.</span></span>
