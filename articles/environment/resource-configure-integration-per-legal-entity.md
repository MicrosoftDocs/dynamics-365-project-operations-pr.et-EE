---
title: Project Operationsi integratsiooni konfigureerimine vastavalt juriidilise isikule
description: Selles teemas kirjeldatakse Project Operationsis integratsiooni seadistamist vastavalt juriidilisele isikule.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096747"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="9ef4e-103">Project Operationsi integratsiooni konfigureerimine vastavalt juriidilise isikule</span><span class="sxs-lookup"><span data-stu-id="9ef4e-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="9ef4e-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="9ef4e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9ef4e-105">See teema selgitab vajalikke etappe, mis on vajalikud Dynamics 365 Project Operationsi konfigureerimiseks vastavalt juriidilisele isikule.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="9ef4e-106">Funktsiooni võtmete lubamine rakenduses Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="9ef4e-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="9ef4e-107">Nõutavate funktsioonide lubamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="9ef4e-108">Avage rakenduses Dynamics 365 Finance tööruum **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="9ef4e-109">Leidke ja lubage jaotises **Funktsioonide loend** järgmised funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-109">In **Feature list** , find and enable the following features:</span></span>
  
    - <span data-ttu-id="9ef4e-110">**Mitme lepingurea lubamine projekti jaoks**</span><span class="sxs-lookup"><span data-stu-id="9ef4e-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="9ef4e-111">**Project Operationsi lubamine lahenduses Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="9ef4e-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="9ef4e-112">Kui te ei näe loendis valikut **Funktsiooni võtmed** veenduge, et teie Finance'i versioon vastab minimaalsetele versiooni nõuetele (rakenduse versioon 10.0.13 koos kõigi rakendatud kvaliteedivärskendustega, või uuem).</span><span class="sxs-lookup"><span data-stu-id="9ef4e-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="9ef4e-113">Valige funktsioonide loendi värskendamiseks suvand **Otsi värskendusi**.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="9ef4e-114">Juriidilisele isikule Project Operationsi juurutamise stsenaariumi määratlemine</span><span class="sxs-lookup"><span data-stu-id="9ef4e-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="9ef4e-115">Saate lahenduses Dynamics 365 Customer Engagement Project Operationsi lubada juriidilise isiku tasandil.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="9ef4e-116">Teil võib olla üks juriidiline isik, kes kasutab Project Operationsi lahenduses Dynamics 365 Customer Engagement ressursipõhiste/mitteaktsiapõhiste stsenaariumite jaoks.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="9ef4e-117">Samas keskkonnas võib teil olla veel üks juriidiline isik, kes kasutab Project Operationsi ressursi/tootmise tellimuste stsenaariumite jaoks.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="9ef4e-118">Minge rakenduses Dynamics 365 Finance jaotisse **Projektijuhtimine ja raamatupidamine** > **Seadistamine** > **Globaalsed projektijuhtimise ja raamatupidamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="9ef4e-119">Valige saadaolevate juriidiliste isikute loendis olemid, kus lubatakse mitu lepingurida ja Project Operationsi funktsioonid lahenduses Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="9ef4e-120">Jätke valimata juriidilised olemid, mis kasutavad Project Operationsi ressursi/tootmise tellimuste stsenaariumite jaoks.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="9ef4e-121">Juriidilise isiku saab valida ainult juhul, kui tal pole olemasolevaid projekte.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="9ef4e-122">Projektijuhtimise ja raamatupidamise parameetride konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9ef4e-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="9ef4e-123">Iga lahenduses Dynamics 365 Customer Engagement Project Operationsi kasutav juriidiline isik vajab vaikimisi määratud parameetrite kogumit.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="9ef4e-124">Need parameetrid on konfigureeritud vahekaardil **Project Operations** lehel **Projektijuhtimise ja raamatupidamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="9ef4e-125">Parameetrid on järgmised.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-125">The parameters are:</span></span>

  - <span data-ttu-id="9ef4e-126">**Arveldustüübi vaikesätted** : Project Operations kasutab fikseeritud arveldustüübi vaikeväärtuste kogumit, mis tuleb vastendada Finance'is rea atribuutidega.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-126">**Billing type defaults** : Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="9ef4e-127">Looge kirje iga arveldustüübi kohta: **Määramata** , **Tasustatav** , **Mittearveldatav** , **Tasuta** ja **Pole saadaval**.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-127">Create a record for each billing type: **Not specified** , **Chargeable** , **Non-chargeable** , **Complimentary** , and **Not available**.</span></span>
  - <span data-ttu-id="9ef4e-128">**Projekti kategooria vaikesätted** : valige iga kandetüübi jaoks kasutatavad projekti vaikekategooriad.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-128">**Project category defaults** : Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="9ef4e-129">Neid vaikeväärtusi kasutatakse **Project Operationsi integreerimise töölehel** ja nendes prognoosides, kus projekti tegelikuks näitajaks ei ole tehingu kategooriat määratud.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="9ef4e-130">**Prognoosid** : valige prognoosi mudel, mida kasutatakse aja- ja kuluprognoosideks.</span><span class="sxs-lookup"><span data-stu-id="9ef4e-130">**Forecasts** : Select the forecast model to be used for time and expense estimates.</span></span>
