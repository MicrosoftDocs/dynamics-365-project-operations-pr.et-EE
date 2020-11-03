---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 12, V3
description: Selles teemas antakse teavet selle kohta, mida on uut rakenduse Project Service Automation värskenduse väljaandes 12, v3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 62c3a0c5cfbecb568faef570da309c20afd86de9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074917"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="70358-103">Rakenduse Project Service Automation, värskenduse väljaanne 12, v3</span><span class="sxs-lookup"><span data-stu-id="70358-103">Project Service Automation Update Release 12, V3</span></span>
<span data-ttu-id="70358-104">Meil on hea meel teatada uusimast rakenduse Dynamics 365 Project Service Automation (PSA) värskendusest.</span><span class="sxs-lookup"><span data-stu-id="70358-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="70358-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="70358-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="70358-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="70358-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="70358-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskust ja avage värskenduse installimiseks lahenduste leht.</span><span class="sxs-lookup"><span data-stu-id="70358-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="70358-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="70358-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="70358-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 12 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="70358-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="70358-110">Selle versiooni järgunumber on V3.10.2.34 ja see on oktoobris 2019 automaatvärskendusega kõigile saadaval.</span><span class="sxs-lookup"><span data-stu-id="70358-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="70358-111">Värskenduste väljalase 12</span><span class="sxs-lookup"><span data-stu-id="70358-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="70358-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="70358-112">Bug fixes</span></span>

- <span data-ttu-id="70358-113">Aeg ja kulu</span><span class="sxs-lookup"><span data-stu-id="70358-113">Time and Expense</span></span>

    - <span data-ttu-id="70358-114">Parandatud: ajakirje tõrketeateid on värskendatud asjakohasema konteksti abil.</span><span class="sxs-lookup"><span data-stu-id="70358-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="70358-115">Parandatud: ajakirje ruudustik ja ajakava kuvavad vajadusel vertikaalset kerimisriba õigesti.</span><span class="sxs-lookup"><span data-stu-id="70358-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="70358-116">Parandatud: edastatud kulu- ja ajakirjeid saab kinnitada.</span><span class="sxs-lookup"><span data-stu-id="70358-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="70358-117">Parandatud: kinnituse kinnitamise dialoogisõnumi tühistamine on parandatud ja see kuvab kinnitamise olekut, kui seda on muudetud olekust **kinnitatud** olekusse **edastatud**.</span><span class="sxs-lookup"><span data-stu-id="70358-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="70358-118">Parandatud: väljad **hind** , **ühik** ja **kogus** on nüüd kulukirjes pärast kinnitamist lukustatud.</span><span class="sxs-lookup"><span data-stu-id="70358-118">Fixed: **Price** , **Unit** , and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="70358-119">Projektijuhtimine</span><span class="sxs-lookup"><span data-stu-id="70358-119">Project Management</span></span>

    - <span data-ttu-id="70358-120">Parandatud: toiming **uus** on põhivormilt **meeskonnaliige** eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="70358-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="70358-121">Parandatud: ressursi määramised on värskendatud ja võtavad arvesse ebatäpseid ümardamisvigu, mis viivad ülesande lõpukuupäeva nihkeni.</span><span class="sxs-lookup"><span data-stu-id="70358-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="70358-122">Parandatud: ülesande ruudustikul tuuakse asjakohased serveripoolsed tõrked kasutajale välja.</span><span class="sxs-lookup"><span data-stu-id="70358-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="70358-123">Parandatud: ülesande inimeste valijas renderdatakse nüüd meeskonnaliikme nimi, mitte ametikoha nimi.</span><span class="sxs-lookup"><span data-stu-id="70358-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="70358-124">Ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="70358-124">Resource Management</span></span>

    - <span data-ttu-id="70358-125">Parandatud: mallist loodud projektide ressursivajaduste üksikasjad kasutavad nüüd projekti kalendrit.</span><span class="sxs-lookup"><span data-stu-id="70358-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="70358-126">Parandatud: oskused ja pädevused tulevad nüüd vaikimisi rolli põhiandmetest selle rolli jaoks loodud ressursi nõudetele.</span><span class="sxs-lookup"><span data-stu-id="70358-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="70358-127">Sales</span><span class="sxs-lookup"><span data-stu-id="70358-127">Sales</span></span>

    - <span data-ttu-id="70358-128">Parandatud: põhivormist **Leping** on leitud topelt objekti ID-d.</span><span class="sxs-lookup"><span data-stu-id="70358-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="70358-129">Parandatud: loogikat on värskendatud, et muuta vahekaart **hinnapakkumise analüüs** nähtavale, nii et see kuvaks vahekaardi metaandmete seadistust.</span><span class="sxs-lookup"><span data-stu-id="70358-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="70358-130">Parandatud: tegeliku kirje arvestuskuupäev tuleb nüüd aja-/kulukirje kuupäevast ja mitte kinnitamise kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="70358-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
