---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 20, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 20, v3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 124dad5438f9489d1ddbc952cecaee977b6b7f01
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949089"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="faada-103">Rakenduse Project Service Automation, värskenduse väljaanne 20, v3</span><span class="sxs-lookup"><span data-stu-id="faada-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="faada-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="faada-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="faada-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="faada-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="faada-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="faada-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="faada-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="faada-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="faada-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="faada-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="faada-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 20 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="faada-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="faada-110">Selle versiooni järgu number on V 3.10.31.37 ja on üldiselt saadaval 2020. a juuni enesevärskenduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="faada-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="faada-111">Värskenduste väljalase 20</span><span class="sxs-lookup"><span data-stu-id="faada-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="faada-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="faada-112">Bug fixes</span></span>

<span data-ttu-id="faada-113">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="faada-113">**Project Management**</span></span>

<span data-ttu-id="faada-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="faada-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="faada-115">Projekti meeskonnaliikmete importimine jaotamismeetodiga, mis nõuab tundide tulemit ebaselges tõrketeates, kui määratud tunnid on null.</span><span class="sxs-lookup"><span data-stu-id="faada-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="faada-116">Kasutajatele kuvatakse vale tõrge, kui projekti tööülesande väljale **Kirjeldus** on sisestatud maksimaalne arv märke.</span><span class="sxs-lookup"><span data-stu-id="faada-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="faada-117">Leht **Microsoft Dynamics 365 Project Service Automationi lisandmooduli allalaadimine** suunab inglisekeelsele allalaadimise lehele, kus kasutaja keelesätted on määratud jaapani keelele.</span><span class="sxs-lookup"><span data-stu-id="faada-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="faada-118">Kui ilmneb serveri tõrge, jääb mõnikord sünkroonimise silt vahekaardil **Ajakava** rakenduse **Projektid** vormides alles.</span><span class="sxs-lookup"><span data-stu-id="faada-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="faada-119">Liigsed tööülesannete värskendused saadetakse serverisse tööülesande muutmisel.</span><span class="sxs-lookup"><span data-stu-id="faada-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="faada-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="faada-120">**Sales**</span></span>

<span data-ttu-id="faada-121">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="faada-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="faada-122">Vormil **Leping** loob käsu **Loo arve** kaks arvet ühe tegeliku kirje kohta.</span><span class="sxs-lookup"><span data-stu-id="faada-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="faada-123">Rakenduses Internet Explorer 11 ei saa kasutajad kulukirjeid luua.</span><span class="sxs-lookup"><span data-stu-id="faada-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="faada-124">Kulu tagasipööramine ja arveldamata müügi tegelike näitajate tühistamine pole lingitud.</span><span class="sxs-lookup"><span data-stu-id="faada-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="faada-125">Nupp **Värskenda tegelikud näitajad** **Projekti** vormil ei värskenda väärtust **Tööülesande tegelikud tunnid**.</span><span class="sxs-lookup"><span data-stu-id="faada-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="faada-126">**PreValidateProjectTeamMemberCreate** lisandmoodul saab dubleerida üldkasutatavaid ressursse juhul, kui atribuudi **msdyn_isgenericresourceprojectscoped** väärtuseks on seatud **väär**.</span><span class="sxs-lookup"><span data-stu-id="faada-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="faada-127">Käsk **Arvuta** tühistab tootepõhise hinnapakkumise rea üksikasjade ja lepingurea üksikasjadega seotud tasustatavad kulud.</span><span class="sxs-lookup"><span data-stu-id="faada-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="faada-128">Teatud juhtudel kuvab lisandmoodul **PostEstimateLineUpdate** nullviite erandi tõrke.</span><span class="sxs-lookup"><span data-stu-id="faada-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="faada-129">Ajaetapi kestus **Kasumlikkuse analüüsi diagrammil** ei vasta fikseeritud hinnaga hinnapakkumise rea üksikasjade kulude kestusele.</span><span class="sxs-lookup"><span data-stu-id="faada-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="faada-130">Üksuste ja üksuste rühma kulukategooriate väärtused ei ole vaikimisi õigedvormidel **Lepingurea üksikasjad** ja **Hinnapakkumise rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="faada-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="faada-131">**Organisatsiooni ühiku omahinna** loendid lubavad efektiivse kuupäeva kattumist.</span><span class="sxs-lookup"><span data-stu-id="faada-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="faada-132">Kasutajad ei tohi muuta **OrgUnit** it juhul, kui tellimuse tüüp ei ole tööpõhine, kuna selle tulemuseks on nullviite erandi tõrge.</span><span class="sxs-lookup"><span data-stu-id="faada-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="faada-133">Kui proovite navigeerida vormilt **Hinnapakkumise rea üksikasjad** tagasi vahekaardile **Hinnapakkumine**, siis vorm värskendab ja kuvab vahekaardi **Kokkuvõte**.</span><span class="sxs-lookup"><span data-stu-id="faada-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]