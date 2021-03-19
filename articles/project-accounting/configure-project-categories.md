---
title: Projektikategooriate konfigureerimine
description: Selles teemas antakse teavet projektikategooriate seadistamise kohta.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b7adf61a82714a0148d9c8b1d2b2b37fd611c1cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287503"
---
# <a name="configure-project-categories"></a><span data-ttu-id="f33a5-103">Projektikategooriate konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f33a5-103">Configure project categories</span></span>

<span data-ttu-id="f33a5-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="f33a5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f33a5-105">Project Operations pakub projektide tulude ja kulude kategooriatesse jaotamiseks töökindlad funktsioone.</span><span class="sxs-lookup"><span data-stu-id="f33a5-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="f33a5-106">Kategooriad pakuvad võimalust teatada ja analüüsida projekti kandeid ning vedada pearaamatusse märkimist.</span><span class="sxs-lookup"><span data-stu-id="f33a5-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="f33a5-107">Järgmisel diagrammil on toodud kannete kategooriate, ühiskasutuses kategooriate ja projekti kategooriate vaheline korrelatsioon.</span><span class="sxs-lookup"><span data-stu-id="f33a5-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="f33a5-108">Kannete kategooriad on projekti kannete peamine rühmitamine.</span><span class="sxs-lookup"><span data-stu-id="f33a5-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="f33a5-109">Selles rühmas on ühiskasutuses kategooriate komplekt, mida saab rakenduste ja moodulite üleselt ühiselt kasutada.</span><span class="sxs-lookup"><span data-stu-id="f33a5-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="f33a5-110">Täpsustades seda veelgi, siis projekti kategooriad on kategooriate kõige granuleeritum tase.</span><span class="sxs-lookup"><span data-stu-id="f33a5-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="f33a5-111">Projekti kategooriad on omased juriidilistele olemitele, moodulitele ja rakendusele.</span><span class="sxs-lookup"><span data-stu-id="f33a5-111">Project categories are specific to legal entity, module, and application.</span></span>

![Kannete kategooriate, ühiskasutuses kategooriate ja projekti kategooriate vaheline korrelatsioon](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="f33a5-113">Kandekategooriad</span><span class="sxs-lookup"><span data-stu-id="f33a5-113">Transaction categories</span></span>

<span data-ttu-id="f33a5-114">Kannete kategooriad esindavad projekti kannete põhirühmitust ja ei ole ettevõttele ega kande tüübile spetsiifilised.</span><span class="sxs-lookup"><span data-stu-id="f33a5-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="f33a5-115">Näiteks kasutab Contoso Robootika projekti kannete rühmitamiseks disaini, sõidu, paigalduse ja teeninduse tehingute kategooriaid.</span><span class="sxs-lookup"><span data-stu-id="f33a5-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="f33a5-116">Kannete kategooriad on määratletud rakenduse Project Operations moodulis.</span><span class="sxs-lookup"><span data-stu-id="f33a5-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="f33a5-117">Vormi avamiseks avage **Sätted** \> **Tehingu kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="f33a5-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="f33a5-118">Looge uus kande kategooria valides kas suvandi **Uus** või valides **Impordi Excelist**.</span><span class="sxs-lookup"><span data-stu-id="f33a5-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="f33a5-119">Ühiskasutuses kategooriad</span><span class="sxs-lookup"><span data-stu-id="f33a5-119">Shared categories</span></span>

<span data-ttu-id="f33a5-120">Dynamics 365 kasutab ühiskasutuses kategooriate mõistet kulude kategoriseerimiseks erinevates rakendustes, näiteks rakendustes Dynamics 365 Finance, Dynamics 365 Supply Chain ja Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f33a5-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="f33a5-121">Iga loodud kande kategooria jaoks loob Project Operations automaatselt neli seotud üiskasutuses kategooriat: tunnid, kulu, tasud ja kaup.</span><span class="sxs-lookup"><span data-stu-id="f33a5-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="f33a5-122">Saate ühiskasutuses kategooriaid läbi vaadata, kui avate **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Kategooriad** \> **Ühiskasutuses kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="f33a5-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="f33a5-123">Projektikategooriad</span><span class="sxs-lookup"><span data-stu-id="f33a5-123">Project categories</span></span>

<span data-ttu-id="f33a5-124">Projekti kategooriad esindavad kategooriate konfigureerimise kõige granuleeritumat taset ja peavad olema projekti raamatupidaja poolt konfigureeritud eraldi ja iga ettevõtte jaoks.</span><span class="sxs-lookup"><span data-stu-id="f33a5-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="f33a5-125">Avage **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Kategooriad** \> **Projekti kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="f33a5-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="f33a5-126">Tehke valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f33a5-126">Select **New**.</span></span>
3. <span data-ttu-id="f33a5-127">Vaige ühiskasutuses kategooria jaoks **kategooria ID**, mille eelmises jaotises lõite.</span><span class="sxs-lookup"><span data-stu-id="f33a5-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="f33a5-128">Project Operations võimaldab ainult nende ühiskasutuses kategooriate kasutamist, mis on tehingu kategooriatega seotud.</span><span class="sxs-lookup"><span data-stu-id="f33a5-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="f33a5-129">Valige kategooria rühm.</span><span class="sxs-lookup"><span data-stu-id="f33a5-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="f33a5-130">Kategooria rühmad</span><span class="sxs-lookup"><span data-stu-id="f33a5-130">Category groups</span></span>

<span data-ttu-id="f33a5-131">Kategooria rühmasid kasutatakse atribuutide ühiskasutuseks, peamiselt profiilide postitamiseks seotud projekti kategooriate vahel.</span><span class="sxs-lookup"><span data-stu-id="f33a5-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="f33a5-132">Igal tehingu tüübil peab olema vähemalt üks kategooria rühm ja igale projekti kategooriale peab olema määratud rühm.</span><span class="sxs-lookup"><span data-stu-id="f33a5-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="f33a5-133">Rakenduses Project Operations on postitamise tehnilised andmed määratletud projekti kulu- ja tuluprofiili reeglite, projekti kategooriate ja kategooriate rühmade poolt.</span><span class="sxs-lookup"><span data-stu-id="f33a5-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="f33a5-134">Kategooria rühmad saate häälestada avades **Projektihaldus ja raamatupidamine** \> **Seadistamine** \> **Kategooriad** \> **Kategooria rühmad**.</span><span class="sxs-lookup"><span data-stu-id="f33a5-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]