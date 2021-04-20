---
title: Projektiarve ettepaneku tulemus
description: Selles teemas antakse teavet projektiarve ettepaneku jõudluse täiustuste kohta.
author: Yowelle
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 78c924cba8107471a5f8e6d6a38265890d32d72b
ms.sourcegitcommit: 2350c6f3728067a8298adde640e6fdd5984eb077
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573554"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="7aac5-103">Projektiarve ettepaneku tulemus</span><span class="sxs-lookup"><span data-stu-id="7aac5-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="7aac5-104">Uue arve loomisel võib ilmneda jõudlusprobleeme, kuna projektide ja alamprojektide arv suureneb.</span><span class="sxs-lookup"><span data-stu-id="7aac5-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="7aac5-105">Jõudluse parandamiseks on saadaval funktsioon, mis vähendab sisestatud projektitehingute jaoks uue arve loomiseks vajalikku aega.</span><span class="sxs-lookup"><span data-stu-id="7aac5-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="7aac5-106">Projektiarve ettepaneku jõudluse täiustamise lubamine</span><span class="sxs-lookup"><span data-stu-id="7aac5-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="7aac5-107">Projektiarve jõudluse ettepaneku jõudluse täiustusfunktsiooni lubamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="7aac5-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="7aac5-108">Avage **Funktsioonihaldus** > **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="7aac5-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="7aac5-109">Leidke funktsiooniloendist suvand **Projektiarve ettepaneku jõudluse täiustus**.</span><span class="sxs-lookup"><span data-stu-id="7aac5-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="7aac5-110">Valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="7aac5-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="7aac5-111">Värskendage brauserit ja looge seejärel uus arve ettepanek.</span><span class="sxs-lookup"><span data-stu-id="7aac5-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="7aac5-112">Projektiarve ettepaneku jõudluse täiustamise väljalülitamine</span><span class="sxs-lookup"><span data-stu-id="7aac5-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="7aac5-113">Projektiarve jõudluse ettepaneku jõudluse täiustusfunktsiooni väljalülitamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="7aac5-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="7aac5-114">Avage **Funktsioonihaldus** > **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="7aac5-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="7aac5-115">Leidke funktsiooniloendist suvand **Projektiarve ettepaneku jõudluse täiustus**.</span><span class="sxs-lookup"><span data-stu-id="7aac5-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="7aac5-116">Valige **Keela**.</span><span class="sxs-lookup"><span data-stu-id="7aac5-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="7aac5-117">Värskendage oma brauser.</span><span class="sxs-lookup"><span data-stu-id="7aac5-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="7aac5-118">Arve ettepaneku jõudlust ei saa rakendada, kui arveldusreeglid on lubatud või partiiprotsessid töötavad.</span><span class="sxs-lookup"><span data-stu-id="7aac5-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
