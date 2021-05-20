---
title: Turbemudel
description: Selles teemas antakse teavet rakenduse Dynamics 365 Project Operations turbe mudeli kohta.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 8acaa86dec8ebca8f9850877d345e30be3e3a919
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951204"
---
# <a name="security-model"></a><span data-ttu-id="ad9f3-103">Turbemudel</span><span class="sxs-lookup"><span data-stu-id="ad9f3-103">Security Model</span></span>

<span data-ttu-id="ad9f3-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="ad9f3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ad9f3-105">Microsoft Dynamics 365 Project Operations sisaldab ainulaadset turbemudelit, mis võimaldab rollipõhist ettevõtte turbemudelit, mis teeb koostööd Microsoft Office’i rühmadega.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-105">Microsoft Dynamics 365 Project Operations contains a unique security model that allows for a role-based business security model that collaborates with Microsoft Office Groups.</span></span> 


## <a name="security-roles"></a><span data-ttu-id="ad9f3-106">Turberollid</span><span class="sxs-lookup"><span data-stu-id="ad9f3-106">Security roles</span></span>
<span data-ttu-id="ad9f3-107">Project Operationsi kasutajaliidese võimalused sisaldavad järgmisi rolle.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-107">Project Operations front-end capabilities include the following roles:</span></span>

| <span data-ttu-id="ad9f3-108">Roll</span><span class="sxs-lookup"><span data-stu-id="ad9f3-108">Role</span></span>                          | <span data-ttu-id="ad9f3-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ad9f3-109">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="ad9f3-110">Scope</span><span class="sxs-lookup"><span data-stu-id="ad9f3-110">Scope</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="ad9f3-111">Praktikajuht</span><span class="sxs-lookup"><span data-stu-id="ad9f3-111">Practice manager</span></span>              | <span data-ttu-id="ad9f3-112">Toetab projektiülest aruandlust.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-112">Supports cross-project reporting.</span></span>                                                                                                            | <span data-ttu-id="ad9f3-113">Äriüksus</span><span class="sxs-lookup"><span data-stu-id="ad9f3-113">Business unit</span></span>              |
| <span data-ttu-id="ad9f3-114">Projekti kinnitaja</span><span class="sxs-lookup"><span data-stu-id="ad9f3-114">Project approver</span></span>              | <span data-ttu-id="ad9f3-115">Kinnitab projekti aega ja kulusid.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-115">Approves time and expenses against a project.</span></span>                                                                                                                              | <span data-ttu-id="ad9f3-116">Äriüksus</span><span class="sxs-lookup"><span data-stu-id="ad9f3-116">Business unit</span></span> |
| <span data-ttu-id="ad9f3-117">Projekti arveldushaldur</span><span class="sxs-lookup"><span data-stu-id="ad9f3-117">Project billing administrator</span></span> | <span data-ttu-id="ad9f3-118">Loob arve ettepaneku.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-118">Creates the invoice proposal.</span></span>                                                                                                                                                 | <span data-ttu-id="ad9f3-119">Äriüksus</span><span class="sxs-lookup"><span data-stu-id="ad9f3-119">Business unit</span></span> |
| <span data-ttu-id="ad9f3-120">Projektijuht</span><span class="sxs-lookup"><span data-stu-id="ad9f3-120">Project manager</span></span>               | <span data-ttu-id="ad9f3-121">Loob projekti kava ja taotleb ressursse.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-121">Creates the project plan and requests resources.</span></span>                                                                                                                              | <span data-ttu-id="ad9f3-122">Äriüksus</span><span class="sxs-lookup"><span data-stu-id="ad9f3-122">Business unit</span></span> |
| <span data-ttu-id="ad9f3-123">Projekti ressurss</span><span class="sxs-lookup"><span data-stu-id="ad9f3-123">Project resource</span></span>              | <span data-ttu-id="ad9f3-124">Meeskonnaliikmed, keda saab broneerida ja kes saavad esitada aega.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-124">Team members who can be booked and report time.</span></span>                                                                                                          | <span data-ttu-id="ad9f3-125">Äriüksus</span><span class="sxs-lookup"><span data-stu-id="ad9f3-125">Business unit</span></span>|
| <span data-ttu-id="ad9f3-126">Ressursihaldur</span><span class="sxs-lookup"><span data-stu-id="ad9f3-126">Resource manager</span></span>              | <span data-ttu-id="ad9f3-127">Kõik ressursihalduse funktsioonid, näiteks ressursi taotluste ja broneeringute täitmine, eraldatud, et toetada hübriidkonfiguratsiooni Projektijuht + Ressursihaldur ja ühe ning tsentraliseeritud ressursihalduri rolli.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-127">All resource management functions, such as fulfill resource requests and bookings, separated to support a hybrid Project manager + Resource manager configuration and a single and centralized Resource manager role.</span></span> | <span data-ttu-id="ad9f3-128">Äriüksus</span><span class="sxs-lookup"><span data-stu-id="ad9f3-128">Business unit</span></span> |


<span data-ttu-id="ad9f3-129">Microsoft Projecti veebilanedus sisaldab järgmisi rolle.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-129">Microsoft Project for the Web includes the following roles:</span></span>

| <span data-ttu-id="ad9f3-130">Roll</span><span class="sxs-lookup"><span data-stu-id="ad9f3-130">Role</span></span>           | <span data-ttu-id="ad9f3-131">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ad9f3-131">Description</span></span>                                                                                                        | <span data-ttu-id="ad9f3-132">Scope</span><span class="sxs-lookup"><span data-stu-id="ad9f3-132">Scope</span></span>  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| <span data-ttu-id="ad9f3-133">Projekti kasutaja</span><span class="sxs-lookup"><span data-stu-id="ad9f3-133">Project user</span></span>   | <span data-ttu-id="ad9f3-134">Projekti koostööpartner, kes saab luua oma projekte ja vaadata temaga ühiskasutusse antud projekte.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-134">Collaborative user of Project   who is able to create their own projects and view any projects shared with   them.</span></span> | <span data-ttu-id="ad9f3-135">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="ad9f3-135">User</span></span>   |
| <span data-ttu-id="ad9f3-136">Projekti süsteem</span><span class="sxs-lookup"><span data-stu-id="ad9f3-136">Project system</span></span> | <span data-ttu-id="ad9f3-137">Rakenduse kontekstis kasutatav roll.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-137">Role used for application   context.</span></span> <span data-ttu-id="ad9f3-138">Kliendid ei tohiks seda süsteemi rolli kasutada.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-138">Customers should not use this system role.</span></span>                                    | <span data-ttu-id="ad9f3-139">Globaalne</span><span class="sxs-lookup"><span data-stu-id="ad9f3-139">Global</span></span> |

## <a name="security-enforcement"></a><span data-ttu-id="ad9f3-140">Turvalisuse tagamine</span><span class="sxs-lookup"><span data-stu-id="ad9f3-140">Security enforcement</span></span>
<span data-ttu-id="ad9f3-141">Projektitasemel teostatud toiminguid teostatakse sisselogitud kasutaja kontekstis.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-141">Actions that are performed at the project level are performed in the context of the logged in user.</span></span> <span data-ttu-id="ad9f3-142">See tähendab, et projekti loomiseks, avamiseks või kustutamiseks peab kasutajal olema juurdepääs CDS-ile.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-142">This means that in order to create, open, or delete a project, the user is required to have access available in CDS.</span></span> <span data-ttu-id="ad9f3-143">Juurdepääs CDS-ile võidakse anda ühe platvormil oleva võimaliku mehhanismi kaudu.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-143">Access in CDS may be granted through any of the possible mechanisms included in the platform.</span></span> <span data-ttu-id="ad9f3-144">Näiteks võib projektile olla juurdepääs suurema ulatusega kasutajal või kui on teostatud konkreetne projekti ühiskasutusse andmise toiming, mis annab kasutajale juurdepääsu.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-144">For example, a user with a larger scope may access the project or if an explicit project share action has been performed which grants the user access.</span></span>

<span data-ttu-id="ad9f3-145">Oluline on seda Project Operationsis projektide loomisel arvestada.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-145">It's important to consider this when creating projects in Project Operations.</span></span>

## <a name="modern-group-collaboration-with-project-operations"></a><span data-ttu-id="ad9f3-146">Kaasaegne rühma koostöö Project Operationsiga</span><span class="sxs-lookup"><span data-stu-id="ad9f3-146">Modern group collaboration with Project Operations</span></span>
<span data-ttu-id="ad9f3-147">Veebi Project ja Project Operations toetavad kaasaegseid koostöörühmi.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-147">Project for the Web and Project Operations support modern groups for collaboration.</span></span> <span data-ttu-id="ad9f3-148">Projektile rühma kaudu lisatud kasutajad saavad projekti kava redigeerida.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-148">Users added to the project through a group are able to edit the project plan.</span></span>

<span data-ttu-id="ad9f3-149">Veebi Project lisab kasutajad määramisel automaatselt rühma.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-149">Project for the Web adds users to the group automatically upon assignment.</span></span>

<span data-ttu-id="ad9f3-150">Rühmad võimaldavad projekti õigusi ja toetavaid koostöö artefakte üheskoos töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-150">Groups allow the permissions of the project and supporting collaboration artifacts to be worked on collaboratively.</span></span> <span data-ttu-id="ad9f3-151">Järgmisel diagrammil on kujutatud sündmused ja oleku muudatused, mis toimuvad rühma määramise protsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-151">The following diagram depicts the events and state changes that happen during the group assignment process.</span></span>

<span data-ttu-id="ad9f3-152">Project Operations ei loo rühma kaudse tegevuse kaudu ja teeb seda ainult pakiliste rühmade selgesõnalise tegevuse kaudu.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-152">Project Operations does not create a group through implicit action and only does so through the explicit action of pressing groups.</span></span>

<span data-ttu-id="ad9f3-153">Rühma liikmete otsing dialoogis **Rühma haldus** on piiratud nendega, kes on määratud keskkonna turberühma osaks.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-153">Group member search in the **Group management** dialog, is limited to those who are set as part of the environment's security group.</span></span> <span data-ttu-id="ad9f3-154">Lisateavet vt jaotisest [Kasutajate keskkondadele juurdepääsu juhtimine: turberühmad ja litsentsid](/power-platform/admin/control-user-access).</span><span class="sxs-lookup"><span data-stu-id="ad9f3-154">For more information, see [Control user access to environments: security groups and licenses](/power-platform/admin/control-user-access).</span></span>

![Rühma režiim](./media/groupsmode.png)

1. <span data-ttu-id="ad9f3-156">Projekti loob ja omab loov kasutaja.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-156">The Project is created and owned by the creating User.</span></span>
2. <span data-ttu-id="ad9f3-157">Projekti omanikuks värskendatakse meeskond.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-157">The Project owner is updated to the team.</span></span>
3. <span data-ttu-id="ad9f3-158">Omanikuks olev meeskond vastendatakse määratud või loodud Office'i rühmaga.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-158">The Owner team is mapped to the specified or created Office Group.</span></span>
4. <span data-ttu-id="ad9f3-159">Projekti algne omanik lisatakse Office'i rühma.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-159">The original owner of the Project is added to the Office Group.</span></span>

## <a name="deployment-recommendation"></a><span data-ttu-id="ad9f3-160">Juurutamise soovitus</span><span class="sxs-lookup"><span data-stu-id="ad9f3-160">Deployment recommendation</span></span>
<span data-ttu-id="ad9f3-161">Office'i rühma koostöömudeli arenedes lisatakse funktsionaalsus, et aja jooksul saaks pakkuda üksikasjalikumat kontrolli.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-161">As the Office group collaboration model evolves, functionality will be added to provide more detailed control over time.</span></span> <span data-ttu-id="ad9f3-162">Klientidel, kes juurutavad Project Operationsi täna, soovitatakse keskenduda traditsioonilisele Microsoft Dynamics 365 turbemudelile.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-162">Customers that deploy Project Operations today are encouraged to focus on a traditional Microsoft Dynamics 365 security model.</span></span>

<span data-ttu-id="ad9f3-163">Lisateavet leiate jaotisest [Common Data Service'i turvalisus](/power-platform/admin/wp-security).</span><span class="sxs-lookup"><span data-stu-id="ad9f3-163">For more information, see [Security in Common Data Service](/power-platform/admin/wp-security).</span></span>

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a><span data-ttu-id="ad9f3-164">Project Operations ja Microsoft Dynamics 365 Finance'i turvalisus</span><span class="sxs-lookup"><span data-stu-id="ad9f3-164">Project Operations and Microsoft Dynamics 365 Finance security</span></span>
<span data-ttu-id="ad9f3-165">Project Operations sisaldab järgmisi rolle.</span><span class="sxs-lookup"><span data-stu-id="ad9f3-165">Project Operations includes the following roles:</span></span>

- <span data-ttu-id="ad9f3-166">Projektijuht</span><span class="sxs-lookup"><span data-stu-id="ad9f3-166">Project manager</span></span>
- <span data-ttu-id="ad9f3-167">Projekti raamatupidaja</span><span class="sxs-lookup"><span data-stu-id="ad9f3-167">Project accountant</span></span>

<span data-ttu-id="ad9f3-168">Lisateavet lahenduse Finance turbe kohta leiate teemast [Rollipõhine turve](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span><span class="sxs-lookup"><span data-stu-id="ad9f3-168">For more information about security in Finance, see [Role-based security](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]