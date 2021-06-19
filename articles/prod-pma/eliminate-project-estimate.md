---
title: Projekti prognoosi eemaldamine
description: Selles teemas antakse teavet projekti prognoosi eemaldamise kohta pärast selle valmimist.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006911"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="8cf06-103">Projekti prognoosi eemaldamine</span><span class="sxs-lookup"><span data-stu-id="8cf06-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8cf06-104">Projekti prognoosid annavad finantsülevaate töö kohta, mis on projekti jaoks prognoositud ja plaanitud.</span><span class="sxs-lookup"><span data-stu-id="8cf06-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="8cf06-105">Projekti prognoosidega töötamiseks peate projekti prognoositud projektiga siduma.</span><span class="sxs-lookup"><span data-stu-id="8cf06-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="8cf06-106">Prognoositav projekt põhineb alati olemasoleval projektil, kuid mitme projekti puhul võib viidata ühele prognoositavale projektile.</span><span class="sxs-lookup"><span data-stu-id="8cf06-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="8cf06-107">Prognoositavatele projektidele saab lisada ainult fikseeritud hinnaga ja investeerimisprojekte ning need projektid peavad kuuluma samasse projekti rühma, kuhu kuulub prognoositav projekt.</span><span class="sxs-lookup"><span data-stu-id="8cf06-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="8cf06-108">Prognoositava projekti eemaldamiseks tuleb see valmis saada.</span><span class="sxs-lookup"><span data-stu-id="8cf06-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="8cf06-109">Järgmised juhised selgitavad, kuidas prognoosi eemaldada.</span><span class="sxs-lookup"><span data-stu-id="8cf06-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="8cf06-110">Minge jaotisse **Projekti haldamine ja raamatupidamine** > **Kõik projektid** ja avage projekt.</span><span class="sxs-lookup"><span data-stu-id="8cf06-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="8cf06-111">Valige vahekaardil **Halda** väärtus **Prognoosid** ja lehel **Hinnang** suvand **Eemalda**.</span><span class="sxs-lookup"><span data-stu-id="8cf06-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="8cf06-112">Seadke vahekaardil **Üldine** lehel **Prognoosi eemaldamine** järgmised suvandid.</span><span class="sxs-lookup"><span data-stu-id="8cf06-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="8cf06-113">**Perioodi kood**: valige sobiva prognoositava projektide valimiseks perioodi kood.</span><span class="sxs-lookup"><span data-stu-id="8cf06-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="8cf06-114">**Prognoosi kuupäev**: valige eemaldamiseks sobiv prognoosi kuupäev.</span><span class="sxs-lookup"><span data-stu-id="8cf06-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="8cf06-115">**Eemalda WIP-i hoiatustega**: lubage see suvand teatamiseks, kui poolelioleva tööga seotud prognoos eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="8cf06-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="8cf06-116">Kui see suvand pole lubatud, ei saa eemaldamist jätkata, kui olemas on mitte-prognoositavad tehingud.</span><span class="sxs-lookup"><span data-stu-id="8cf06-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="8cf06-117">See suvand on saadaval ainult siis, kui prognoositavale projektile on rakendatud eemaldamine.</span><span class="sxs-lookup"><span data-stu-id="8cf06-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="8cf06-118">See pole saadaval, kui kasutate perioodilist sisestust.</span><span class="sxs-lookup"><span data-stu-id="8cf06-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="8cf06-119">See säte töötab lehe **Projekti parameetrid** vahekaardi **Prognoos** sätetega, mis asub välja rühmas **Luba eemaldamine, kui olemas on mitte-prognoositavad tehingud**.</span><span class="sxs-lookup"><span data-stu-id="8cf06-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="8cf06-120">**Sea etapi väärtuseks Lõpetatud**: lubage see suvand, et seada prognoositava projekti etapi väärtuseks **Lõpetatud**, kui olete eemaldamise lõpetanud.</span><span class="sxs-lookup"><span data-stu-id="8cf06-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="8cf06-121">**Prindi prognooside loend**: valige teave, mis kaasatakse prognooside loendi printimisel.</span><span class="sxs-lookup"><span data-stu-id="8cf06-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="8cf06-122">**Kuva teabelogi**: lubage see suvand teabelogi kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="8cf06-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="8cf06-123">**Sisestamise kuupäev**: valige prognoosi pearaamatusse sisestamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="8cf06-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="8cf06-124">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="8cf06-124">Select **OK**.</span></span>
5. <span data-ttu-id="8cf06-125">Kui eemaldamise protsess on valmis, kuvatakse eemaldatud prognoositav projekt negatiivse väärtusega.</span><span class="sxs-lookup"><span data-stu-id="8cf06-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="8cf06-126">Kui te ei soovinud prognoosi eemaldada, saate valida eemaldatud prognoosi ja valida suvandi **Tühista eemaldamine**.</span><span class="sxs-lookup"><span data-stu-id="8cf06-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]