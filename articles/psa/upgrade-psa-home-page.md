---
title: Täiendamise avaleht
description: Selles teemas kirjeldatakse, kust leida olulist teavet Dynamics 365 Project Service Automation uute ja muudetud funktsioonide kohta ning kuidas täiendada uusimale versioonile.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fa25d069de8098c0e8788c9ebb8aa3426eec5db9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121753"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="1f19a-103">Täiendamise avaleht</span><span class="sxs-lookup"><span data-stu-id="1f19a-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="1f19a-104">Üleminek PSA versioonilt 2.x või 1.x versioonile 3.x</span><span class="sxs-lookup"><span data-stu-id="1f19a-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="1f19a-105">Uued eksemplarid</span><span class="sxs-lookup"><span data-stu-id="1f19a-105">New instances</span></span>

<span data-ttu-id="1f19a-106">Alates 17. maist 2019: kui uue eksemplari ettevalmistamisel valitakse Project Service Automation, installitakse vaikimisi versioon 3.x.</span><span class="sxs-lookup"><span data-stu-id="1f19a-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="1f19a-107">Olemasolevad eksemplarid</span><span class="sxs-lookup"><span data-stu-id="1f19a-107">Existing instances</span></span>

<span data-ttu-id="1f19a-108">Varem pidi kliendid, kellel on PSA versiooni 2.x eksemplar ja vajasid värskendamist versioonile 3.x, mis on PSA ühtse kliendiliidese põhine (UCI) versioon, võtma ühendust Microsofti toega ning esitama oma eksemplari üksikasjad, et tugi saaks võimaldada eksemplari täienduse versioonile 3.x.</span><span class="sxs-lookup"><span data-stu-id="1f19a-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="1f19a-109">2020 a. 1. märtsi seisuga saavad kliendid, kellel on PSA versiooni 2.x eksemplar ja vajavad värskendamist versioonile 3.x värskendada oma eksemplarid otse administreerimisportaalist ilma, et oleks vaja Microsofti tugiteenusega ühendust võtta.</span><span class="sxs-lookup"><span data-stu-id="1f19a-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="1f19a-110">PSA versioon 3.x sisaldab olulisi muudatusi.</span><span class="sxs-lookup"><span data-stu-id="1f19a-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="1f19a-111">See põhineb ühtse kasutajaliidese raamistikul, mis aitab pakkuda täiustatud kasutuskogemust.</span><span class="sxs-lookup"><span data-stu-id="1f19a-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="1f19a-112">Rakenduse uus versioon pakub ühtset kasutajaliidest (UI) ja järgib kiirelt reageeriva veebidisaini põhimõtteid, et tagada igasuguse ekraanisuuruse või seadme puhul optimaalne vaatamiskogemus.</span><span class="sxs-lookup"><span data-stu-id="1f19a-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="1f19a-113">Rakenduses on tehtud ka muid muudatusi.</span><span class="sxs-lookup"><span data-stu-id="1f19a-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="1f19a-114">Muudatusi on tehtud näiteks ka hinnakujunduses, ressursside broneerimises ja määramises, ajas, kuludes ning kinnitustes.</span><span class="sxs-lookup"><span data-stu-id="1f19a-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="1f19a-115">Enne kui alustate täiendusprotsessi, soovitame teil ära teha järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="1f19a-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="1f19a-116">Kontrollige, kas nii Dynamics 365 Field Service kui ka Project Service Automation on tuvastatud eksemplarile installitud.</span><span class="sxs-lookup"><span data-stu-id="1f19a-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="1f19a-117">Kui mõlemad lahendused on installitud, peaksite enne eksemplari tavapärase kasutamise jätkamist plaanima mõlema täiendamist.</span><span class="sxs-lookup"><span data-stu-id="1f19a-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="1f19a-118">Vaadake järgmised teemad tähelepanelikult üle.</span><span class="sxs-lookup"><span data-stu-id="1f19a-118">Carefully review the following topics.</span></span> <span data-ttu-id="1f19a-119">Kui olete teadlik versioonidevahelistest erinevustest ja mõistate neid, aitab see teil täiendusprotsessi teha.</span><span class="sxs-lookup"><span data-stu-id="1f19a-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="1f19a-120">Nendes teemades kirjeldatakse PSA-s tehtud olulisi muudatusi ning esitatakse kaalutlusi ja soovitusi versioonile 3.x ülemineku plaanimiseks.</span><span class="sxs-lookup"><span data-stu-id="1f19a-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="1f19a-121">Mis on uut või muudetud Project Service Automation versioonis 3?</span><span class="sxs-lookup"><span data-stu-id="1f19a-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="1f19a-122">Täienduse kaalutlused – üleminek Project Service Automation versioonilt 2.x või 1.x versioonile 3</span><span class="sxs-lookup"><span data-stu-id="1f19a-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="1f19a-123">Enne tootmiseksemplari täiendamist täiendage oma liivakasti eksemplari, et hinnata juurutamisel ilmnevaid muudatusi.</span><span class="sxs-lookup"><span data-stu-id="1f19a-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="1f19a-124">Kui olete eelmainitud teemad läbi vaadanud ja olete valmis täiendama PSA versioonile 3.x või UCI-põhisele versioonile, esitage Microsofti tugiteenusele oma avaldus, et muuta täiendus halduskeskuse kaudu kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="1f19a-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="1f19a-125">Esitage taotluses oma eksemplari üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="1f19a-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="1f19a-126">Vanemad PSA versioonid (PSA versioon 2.x) äsja loodud eksemplaris</span><span class="sxs-lookup"><span data-stu-id="1f19a-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="1f19a-127">Alates 17. maist 2019 on kõikidel uutel eksemplaridel vaikekliendina UCI.</span><span class="sxs-lookup"><span data-stu-id="1f19a-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="1f19a-128">Selle muudatusega joondamiseks valmistatakse vaikimisi ette PSA versioon 3.x ja Field Service’i versioon 8.x, sest need versioonid on loodud UCI kliendiga töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="1f19a-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="1f19a-129">Alates 1. märtsist 2020 ei saa Dynamics PSA kliendid enam uusi keskkondi luua vanade PSA versioonidega, nagu näiteks PSA versiooniga 2.x või vanemaga.</span><span class="sxs-lookup"><span data-stu-id="1f19a-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="1f19a-130">Iga uus keskkond saab saada ainult PSA versiooni 3.x.</span><span class="sxs-lookup"><span data-stu-id="1f19a-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="1f19a-131">Selleks et saada Field Service’i ja PSA rakenduste vanemaid versioone kasutades parimat kogemust, minge lehele **Süsteemisätted** ning valige välja **Kasuta ainult uut ühtset kasutajaliidest (soovitatav)** sätteks **Ei**, sest need versioonid ei ole loodud UCI-s õigesti laadimiseks.</span><span class="sxs-lookup"><span data-stu-id="1f19a-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="1f19a-132">Kui olete UCI välja lülitanud, saate neid Field Service’i ja PSA versioone avada ning käivitada vana veebikliendi kaudu.</span><span class="sxs-lookup"><span data-stu-id="1f19a-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 
