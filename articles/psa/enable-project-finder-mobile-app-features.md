---
title: Rakenduse Project Finder Mobile funktsioonide lubamine
description: Rakenduse Project Finder Mobile funktsioonide lubamine Project Service'i jaoks
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074963"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="e18e1-103">Rakenduse Project Finder Mobile funktsioonide lubamine (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e18e1-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e18e1-104">Teie ressursid saavad rakendust Project Finder Mobile kasutada oma telefonis koos rakendusega [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], et leida uusi projekte, millega töötada, ja värskendada oma oskusekomplekte.</span><span class="sxs-lookup"><span data-stu-id="e18e1-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="e18e1-105">Rakendus on saadaval [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]’idele, [!INCLUDE[tn_android](../includes/tn-android.md)]-telefonidele ja [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)]’ile.</span><span class="sxs-lookup"><span data-stu-id="e18e1-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="e18e1-106">Peate määrama oma organisatsiooniüksuse jaoks parameetrite sättes mõne suvandi, et võimaldada kasutajatel vaadata projektide ressursinõudeid ja värskendada oma oskusi.</span><span class="sxs-lookup"><span data-stu-id="e18e1-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e18e1-107">Rakendus Project Finder Mobile töötab ainult koos teenusega [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] (mitte asutusesiseste installide puhul).</span><span class="sxs-lookup"><span data-stu-id="e18e1-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="e18e1-108">Minge jaotisse **Project Service > Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e18e1-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="e18e1-109">Klõpsake parameetrite sättel, mida soovite kasutada rakenduse Project Finder Mobile funktsioonide lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="e18e1-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="e18e1-110">Määrake alal **Üldine** valiku **Ressurssidele nähtavad ressursinõuded** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e18e1-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="e18e1-111">Määrake valiku **Luba ressursil oskuste värskendamine** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e18e1-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="e18e1-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="e18e1-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="e18e1-113">See on globaalne säte.</span><span class="sxs-lookup"><span data-stu-id="e18e1-113">This is a global setting.</span></span> <span data-ttu-id="e18e1-114">Projektijuhid saavad üksiku projekti nähtavuse selle projekti lehel **Projektimeeskond**.</span><span class="sxs-lookup"><span data-stu-id="e18e1-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="e18e1-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="e18e1-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="e18e1-116">Meiliteatised</span><span class="sxs-lookup"><span data-stu-id="e18e1-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="e18e1-117">saadab ressursitaotlusi puudutavad meilid järgmistel aegadel järgmistele adressaatidele.</span><span class="sxs-lookup"><span data-stu-id="e18e1-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="e18e1-118">Adressaat</span><span class="sxs-lookup"><span data-stu-id="e18e1-118">Recipient</span></span>|<span data-ttu-id="e18e1-119">Üritus</span><span class="sxs-lookup"><span data-stu-id="e18e1-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="e18e1-120">Projektijuht</span><span class="sxs-lookup"><span data-stu-id="e18e1-120">Project manager</span></span>|<span data-ttu-id="e18e1-121">- Kui ressurss registreerub rakenduse Project Finder Mobile abil projektile.</span><span class="sxs-lookup"><span data-stu-id="e18e1-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="e18e1-122">Ressurss</span><span class="sxs-lookup"><span data-stu-id="e18e1-122">Resource</span></span>|<span data-ttu-id="e18e1-123">- Kui projektitöö, millele ressurss on registreerunud, on teine ressurss juba teinud.</span><span class="sxs-lookup"><span data-stu-id="e18e1-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="e18e1-124">- Kui tema oskuste kinnitustaotlus on kinnitatud või tagasi lükatud.</span><span class="sxs-lookup"><span data-stu-id="e18e1-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="e18e1-125">- Kui tema projektile registreerumise taotlus on kinnitatud või tagasi lükatud.</span><span class="sxs-lookup"><span data-stu-id="e18e1-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="e18e1-126">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="e18e1-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="e18e1-127">Vt ka</span><span class="sxs-lookup"><span data-stu-id="e18e1-127">See Also</span></span>  
 [<span data-ttu-id="e18e1-128">Ressursside seadistamine</span><span class="sxs-lookup"><span data-stu-id="e18e1-128">Set up resources</span></span>](../psa/set-up-resources.md)
