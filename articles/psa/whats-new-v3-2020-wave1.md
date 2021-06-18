---
title: Mis on uut või muudetud Project Service Automation versioonis 3.x laine 1 2020
description: Selles teemas kirjeldatakse, mis on Project Service Automationi versioonis 3 laine 1 2020 uus ja mida on muudetud.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f77c881c62428e423e0dab66eb34b033628a2a1b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996831"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="ac38a-103">Mis on uut või muudetud Project Service Automation versioonis 3 laine 1 2020</span><span class="sxs-lookup"><span data-stu-id="ac38a-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ac38a-104">Teema toob esile peamised versiooniuuenduse kaalutlused, kui liigute Project Service Automationi (PSA) uusimale väljaande versioonile 3. x Wave 1 2020.</span><span class="sxs-lookup"><span data-stu-id="ac38a-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="ac38a-105">Ajakirje</span><span class="sxs-lookup"><span data-stu-id="ac38a-105">Time entry</span></span>
<span data-ttu-id="ac38a-106">Ajakirje kogemust on pikendatud, et pakkuda võimalusi ajakirje pikendamiseks rohkemateks klientide stsenaariumiteks.</span><span class="sxs-lookup"><span data-stu-id="ac38a-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="ac38a-107">See hõlmab võimalust lisada kirjetüüpe, mis juhivad nüüd konkreetset käitumist, mis põhineb välja skeemil nimega **Ajakirje sätted**, mida kuvatakse kui **Aja allikas**.</span><span class="sxs-lookup"><span data-stu-id="ac38a-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="ac38a-108">Selle funktsiooni toetamiseks on lisatud uus lahendus, mida nimetatakse Time, Expense, Statusing, and Approvals (aeg, kulu, olek ja kinnitused) (TESA).</span><span class="sxs-lookup"><span data-stu-id="ac38a-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="ac38a-109">Mida versioonitäienduse puhul arvestada</span><span class="sxs-lookup"><span data-stu-id="ac38a-109">Upgrade consideration</span></span>
<span data-ttu-id="ac38a-110">Selle funktsiooni toetamiseks värskendatakse PSA rolle, et kaasata uusi õigusi.</span><span class="sxs-lookup"><span data-stu-id="ac38a-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="ac38a-111">Need õigused lubavad lugeda juurdepääsu uuele olemile, **Ajakirje sätetele**.</span><span class="sxs-lookup"><span data-stu-id="ac38a-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="ac38a-112">Kasutajatele, kes vajavad aja logimise võimalust, tuleks lisaks olemasolevatele rollidele anda kasutajaroll **Ajakirje kasutaja**.</span><span class="sxs-lookup"><span data-stu-id="ac38a-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="ac38a-113">See roll hõlmab uut funktsionaalsust ja kindlustab, et ajakirje töötab edasi.</span><span class="sxs-lookup"><span data-stu-id="ac38a-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="ac38a-114">Lisaks, kui teil on mis tahes kohandatud rakenduste moodulid, mis sisaldavad ka ajakirje olemi kõiki vorme, on teil vaja eemaldada moodulist **TESA time Entry Quick Create Form**.</span><span class="sxs-lookup"><span data-stu-id="ac38a-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="ac38a-115">Praegu laiendatud ajakirje muudatused</span><span class="sxs-lookup"><span data-stu-id="ac38a-115">Currently extended time entry changes</span></span>
<span data-ttu-id="ac38a-116">Selleks, et vähendada mõju praegustele ajakirjete kasutajatele, on see rollimuutus ainuke põhiline nõue ajakirje kasutamise jätkamiseks.</span><span class="sxs-lookup"><span data-stu-id="ac38a-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="ac38a-117">Kui olete loonud kohandatud vaated või eraldi ajakirjega kogemused, peate seadistama väljad **Ajakirje sätted** õigetele PSA väärtustele.</span><span class="sxs-lookup"><span data-stu-id="ac38a-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]