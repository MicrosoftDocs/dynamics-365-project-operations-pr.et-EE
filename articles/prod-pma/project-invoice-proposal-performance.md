---
title: Projektiarve ettepaneku tulemus
description: Selles teemas antakse teavet projektiarve ettepaneku jõudluse täiustuste kohta.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269785"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="c9a26-103">Projektiarve ettepaneku tulemus</span><span class="sxs-lookup"><span data-stu-id="c9a26-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9a26-104">Uue arve loomisel võib ilmneda jõudlusprobleeme, kuna projektide ja alamprojektide arv suureneb.</span><span class="sxs-lookup"><span data-stu-id="c9a26-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="c9a26-105">Jõudluse parandamiseks on saadaval funktsioon, mis vähendab sisestatud projektitehingute jaoks uue arve loomiseks vajalikku aega.</span><span class="sxs-lookup"><span data-stu-id="c9a26-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="c9a26-106">Projektiarve ettepaneku jõudluse täiustamise lubamine</span><span class="sxs-lookup"><span data-stu-id="c9a26-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="c9a26-107">Projektiarve jõudluse ettepaneku jõudluse täiustusfunktsiooni lubamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c9a26-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="c9a26-108">Avage **Funktsioonihaldus** > **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="c9a26-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="c9a26-109">Leidke funktsiooniloendist suvand **Projektiarve ettepaneku jõudluse täiustus**.</span><span class="sxs-lookup"><span data-stu-id="c9a26-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="c9a26-110">Valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="c9a26-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="c9a26-111">Värskendage brauserit ja looge seejärel uus arve ettepanek.</span><span class="sxs-lookup"><span data-stu-id="c9a26-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="c9a26-112">Projektiarve ettepaneku jõudluse täiustamise väljalülitamine</span><span class="sxs-lookup"><span data-stu-id="c9a26-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="c9a26-113">Projektiarve jõudluse ettepaneku jõudluse täiustusfunktsiooni väljalülitamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c9a26-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="c9a26-114">Avage **Funktsioonihaldus** > **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="c9a26-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="c9a26-115">Leidke funktsiooniloendist suvand **Projektiarve ettepaneku jõudluse täiustus**.</span><span class="sxs-lookup"><span data-stu-id="c9a26-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="c9a26-116">Valige **Keela**.</span><span class="sxs-lookup"><span data-stu-id="c9a26-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="c9a26-117">Värskendage oma brauser.</span><span class="sxs-lookup"><span data-stu-id="c9a26-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="c9a26-118">Arve ettepaneku jõudlust ei saa rakendada, kui arveldamise reeglid on lubatud.</span><span class="sxs-lookup"><span data-stu-id="c9a26-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="c9a26-119">Arve ettepanekute loomise partiina töötlemise ajal jaotab alamülesannete arv ülesanded maksimaalseks numbriks, mis põhineb arveldatavate tehingute lepingute arvul, olenemata sellest, mida olete sisestanud.</span><span class="sxs-lookup"><span data-stu-id="c9a26-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="c9a26-120">Kui näiteks sisestate arve partiina loomise alamülesannete arvuks **3** ja arveldatavate tehingutega on ainult kaks lepingut, luuakse ainult kaks alamülesandet.</span><span class="sxs-lookup"><span data-stu-id="c9a26-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
