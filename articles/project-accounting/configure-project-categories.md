---
title: Projektikategooriate konfigureerimine
description: Selles teemas antakse teavet projektikategooriate seadistamise kohta.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d82302f12ba75a92f2de0e9746ad7e61ce0cdc6b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995166"
---
# <a name="configure-project-categories"></a><span data-ttu-id="dcb5a-103">Projektikategooriate konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="dcb5a-103">Configure project categories</span></span>

<span data-ttu-id="dcb5a-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="dcb5a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dcb5a-105">Project Operations pakub projektide tulude ja kulude kategooriatesse jaotamiseks töökindlad funktsioone.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="dcb5a-106">Kategooriad pakuvad võimalust teatada ja analüüsida projekti kandeid ning vedada pearaamatusse märkimist.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="dcb5a-107">Järgmisel diagrammil on toodud kannete kategooriate, ühiskasutuses kategooriate ja projekti kategooriate vaheline korrelatsioon.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="dcb5a-108">Kannete kategooriad on projekti kannete peamine rühmitamine.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="dcb5a-109">Selles rühmas on ühiskasutuses kategooriate komplekt, mida saab rakenduste ja moodulite üleselt ühiselt kasutada.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="dcb5a-110">Täpsustades seda veelgi, siis projekti kategooriad on kategooriate kõige granuleeritum tase.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="dcb5a-111">Projekti kategooriad on omased juriidilistele olemitele, moodulitele ja rakendusele.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-111">Project categories are specific to legal entity, module, and application.</span></span>

![Kannete kategooriate, ühiskasutuses kategooriate ja projekti kategooriate vaheline korrelatsioon](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="dcb5a-113">Kandekategooriad</span><span class="sxs-lookup"><span data-stu-id="dcb5a-113">Transaction categories</span></span>

<span data-ttu-id="dcb5a-114">Kannete kategooriad esindavad projekti kannete põhirühmitust ja ei ole ettevõttele ega kande tüübile spetsiifilised.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="dcb5a-115">Näiteks Contoso Robotics kasutab projektitehingute rühmitamiseks kategooriaid kujundus, sõit, paigaldamine ja hooldustehingud.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="dcb5a-116">Kannete kategooriad on määratletud rakenduse Project Operations moodulis.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="dcb5a-117">Vormi avamiseks avage **Sätted** \> **Tehingu kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="dcb5a-118">Looge uus kande kategooria valides kas suvandi **Uus** või valides **Impordi Excelist**.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="dcb5a-119">Ühiskasutuses kategooriad</span><span class="sxs-lookup"><span data-stu-id="dcb5a-119">Shared categories</span></span>

<span data-ttu-id="dcb5a-120">Dynamics 365 kasutab ühiskasutuses kategooriate mõistet kulude kategoriseerimiseks erinevates rakendustes, näiteks rakendustes Dynamics 365 Finance, Dynamics 365 Supply Chain ja Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="dcb5a-121">Iga loodud kande kategooria jaoks loob Project Operations automaatselt neli seotud üiskasutuses kategooriat: tunnid, kulu, tasud ja kaup.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="dcb5a-122">Saate ühiskasutuses kategooriaid läbi vaadata, kui avate **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Kategooriad** \> **Ühiskasutuses kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="dcb5a-123">Projektikategooriad</span><span class="sxs-lookup"><span data-stu-id="dcb5a-123">Project categories</span></span>

<span data-ttu-id="dcb5a-124">Projekti kategooriad esindavad kategooriate konfigureerimise kõige granuleeritumat taset ja peavad olema projekti raamatupidaja poolt konfigureeritud eraldi ja iga ettevõtte jaoks.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="dcb5a-125">Avage **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Kategooriad** \> **Projekti kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="dcb5a-126">Tehke valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-126">Select **New**.</span></span>
3. <span data-ttu-id="dcb5a-127">Vaige ühiskasutuses kategooria jaoks **kategooria ID**, mille eelmises jaotises lõite.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="dcb5a-128">Project Operations võimaldab ainult nende ühiskasutuses kategooriate kasutamist, mis on tehingu kategooriatega seotud.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="dcb5a-129">Valige kategooria rühm.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="dcb5a-130">Kategooria rühmad</span><span class="sxs-lookup"><span data-stu-id="dcb5a-130">Category groups</span></span>

<span data-ttu-id="dcb5a-131">Kategooria rühmasid kasutatakse atribuutide ühiskasutuseks, peamiselt profiilide postitamiseks seotud projekti kategooriate vahel.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="dcb5a-132">Igal tehingu tüübil peab olema vähemalt üks kategooria rühm ja igale projekti kategooriale peab olema määratud rühm.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="dcb5a-133">Rakenduses Project Operations on postitamise tehnilised andmed määratletud projekti kulu- ja tuluprofiili reeglite, projekti kategooriate ja kategooriate rühmade poolt.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="dcb5a-134">Kategooria rühmad saate häälestada avades **Projektihaldus ja raamatupidamine** \> **Seadistamine** \> **Kategooriad** \> **Kategooria rühmad**.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]