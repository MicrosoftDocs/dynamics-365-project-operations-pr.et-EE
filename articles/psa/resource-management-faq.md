---
title: Ressursihalduse KKK
description: Selles teemas antakse vastused ressursihalduse korduma kippuvatele küsimustele.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 25e069beaffc9081a5516449d55b5c9304c23b0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008756"
---
# <a name="resource-management-faq"></a><span data-ttu-id="5ceec-103">Ressursihalduse KKK</span><span class="sxs-lookup"><span data-stu-id="5ceec-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="5ceec-104">Mis on meeskonnaliikme ja ressursinõude vahe?</span><span class="sxs-lookup"><span data-stu-id="5ceec-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="5ceec-105">Projekti meeskonnaliiget saab määrata ülesannetele (broneeritud või ülebroneeritud) ja määrata kinnitajaks.</span><span class="sxs-lookup"><span data-stu-id="5ceec-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="5ceec-106">Ressursinõue võib eksisteerida ilma projekti meeskonnaliikmeta, mustandmärkusena või nõudena.</span><span class="sxs-lookup"><span data-stu-id="5ceec-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="5ceec-107">Mis on pakutud ja esialgselt broneeritud tundide vahe?</span><span class="sxs-lookup"><span data-stu-id="5ceec-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="5ceec-108">Pakutud tundide ja esialgselt broneeritud tundide erinevuseks on nähtavus.</span><span class="sxs-lookup"><span data-stu-id="5ceec-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="5ceec-109">Pakutud tunnid on nähtavad ainult ressursihalduritele ja projektijuhile, kes nõudluse ressursitaotluse kasutamise kaudu algatas.</span><span class="sxs-lookup"><span data-stu-id="5ceec-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="5ceec-110">Esialgselt broneeritud tunnid on nähtavad kõigile, kellel on ajakavapaneelile juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="5ceec-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="5ceec-111">Kuidas vaadata meeskonna ressursside jaoks esialgselt broneeritud tunde?</span><span class="sxs-lookup"><span data-stu-id="5ceec-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="5ceec-112">Esialgseid broneerimisi saab teha ressursinõude broneerimisel.</span><span class="sxs-lookup"><span data-stu-id="5ceec-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="5ceec-113">Ressursid, mis on projektimeeskonnas esialgselt broneeritud kuvatakse meeskonnaliikmetena, kellel on esialgselt broneeritud tunnid.</span><span class="sxs-lookup"><span data-stu-id="5ceec-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="5ceec-114">Need kuvatakse ka ajakavapaneelil.</span><span class="sxs-lookup"><span data-stu-id="5ceec-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="5ceec-115">Kuidas muuta broneeritud ressursi (üldised või nimega) nõutavaid tunde ja algus- ning lõppkuupäevi?</span><span class="sxs-lookup"><span data-stu-id="5ceec-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="5ceec-116">Pärast ressursside broneerimist valige soovitud muudatuste tegemiseks **Halda broneeringuid**.</span><span class="sxs-lookup"><span data-stu-id="5ceec-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="5ceec-117">Milliseid ressursitüüpe Project Service Automation toetab?</span><span class="sxs-lookup"><span data-stu-id="5ceec-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="5ceec-118">**Kasutaja** ja **Kontakt** on ainsad ressursitüübid, mida rakendus Dynamics 365 Project Service Automation toetab.</span><span class="sxs-lookup"><span data-stu-id="5ceec-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="5ceec-119">Kuigi saate luua muid tüüpi ressursse (nt **Varustus** ja **Rühm**), ei toetata nende puhul ühtegi terviklikku kasutusjuhtumit.</span><span class="sxs-lookup"><span data-stu-id="5ceec-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="5ceec-120">Mis on määramise ja broneeringu vahe?</span><span class="sxs-lookup"><span data-stu-id="5ceec-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="5ceec-121">Määramised on projekti ajakavas tehtud ressursside määramised projekti ülesannetele.</span><span class="sxs-lookup"><span data-stu-id="5ceec-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="5ceec-122">Ressursid võivad olla kas tegelikud või üldised ressursid.</span><span class="sxs-lookup"><span data-stu-id="5ceec-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="5ceec-123">Broneeringud on ressursside fikseeritud või esialgsed projektile eraldamised.</span><span class="sxs-lookup"><span data-stu-id="5ceec-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="5ceec-124">Fikseeritud broneeringud tarbivad ressursivõimsust.</span><span class="sxs-lookup"><span data-stu-id="5ceec-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="5ceec-125">Ideaalis peaksid tegelike ressursside puhul broneeringud ja määramised ühtima, kuna need ei erine üksteisest.</span><span class="sxs-lookup"><span data-stu-id="5ceec-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="5ceec-126">Kuid PSA ei jõusta seda kokkulepet.</span><span class="sxs-lookup"><span data-stu-id="5ceec-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="5ceec-127">Vaates Vastavusseviimine kuvatakse projektijuhile kohti, kus ressursi broneeringud ja määramised ei ühti.</span><span class="sxs-lookup"><span data-stu-id="5ceec-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]