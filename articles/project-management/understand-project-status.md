---
title: Projekti oleku mõistmine
description: Selles teemas antakse teavet rakenduses Dynamics 365 Project Operations projektidele määratud oleku kohta.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965671"
---
# <a name="understand-project-status"></a><span data-ttu-id="9f5fd-103">Projekti oleku mõistmine</span><span class="sxs-lookup"><span data-stu-id="9f5fd-103">Understand project status</span></span>

<span data-ttu-id="9f5fd-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="9f5fd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9f5fd-105">Jaotis **Olek** lehel **Projekti olem** annab kokkuvõtte projekti tervisest vastavalt kulule ja pingutustele.</span><span class="sxs-lookup"><span data-stu-id="9f5fd-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="9f5fd-106">Oleku kokkuvõtte väljad</span><span class="sxs-lookup"><span data-stu-id="9f5fd-106">Status summary fields</span></span>

- <span data-ttu-id="9f5fd-107">Väli **Projekti üldine olek** on redigeeritav väli, mis kuvab projekti üldise oleku.</span><span class="sxs-lookup"><span data-stu-id="9f5fd-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="9f5fd-108">See väli kasutab kasvavale ohule viitamiseks värvkodeerimist (nt roheline, kollane ja punane).</span><span class="sxs-lookup"><span data-stu-id="9f5fd-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="9f5fd-109">Väli **Kommentaarid** võimaldab projektijuhil sisestada oleku kohta konkreetseid märkuseid.</span><span class="sxs-lookup"><span data-stu-id="9f5fd-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="9f5fd-110">Väli **Oleku värskendamise aeg** ei ole muudetav.</span><span class="sxs-lookup"><span data-stu-id="9f5fd-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="9f5fd-111">Selle välja väärtus on ajatempel, mis näitab, millal olek viimati värskendati.</span><span class="sxs-lookup"><span data-stu-id="9f5fd-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="9f5fd-112">Väljad **Ajakava täitmine** ja **Kulude täitmine** määratakse jälgimise ruudustikust.</span><span class="sxs-lookup"><span data-stu-id="9f5fd-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="9f5fd-113">Kui vaates **Panuse jälgimine** on juursõlme ajakava ja kuluhälve positiivsed, värskendatakse need väljad olekusse **Ees**.</span><span class="sxs-lookup"><span data-stu-id="9f5fd-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="9f5fd-114">Kui juursõlme ajakava ja kuluhälve on negatiivsed, määratakse need väljad väärtusele **Taga**.</span><span class="sxs-lookup"><span data-stu-id="9f5fd-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
