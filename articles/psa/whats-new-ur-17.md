---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 17, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 17, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: f9fb941a95b0610dc546b1c12a87aa7faef4d676
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143701"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="4f137-103">Rakenduse Project Service Automation, värskenduse väljaanne 17, v3</span><span class="sxs-lookup"><span data-stu-id="4f137-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4f137-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="4f137-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4f137-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="4f137-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="4f137-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="4f137-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4f137-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="4f137-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="4f137-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4f137-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4f137-109">Selles teemas loetletakse PSA V3 värskenduse väljalaske 17 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="4f137-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="4f137-110">Selle versiooni järgunumber on V3.10.6.34 ja see on märtsis 2020 automaatvärskendusega kõigile saadaval.</span><span class="sxs-lookup"><span data-stu-id="4f137-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="4f137-111">Värskenduste väljalase 17</span><span class="sxs-lookup"><span data-stu-id="4f137-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4f137-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="4f137-112">Bug fixes</span></span>

<span data-ttu-id="4f137-113">**Üldine**</span><span class="sxs-lookup"><span data-stu-id="4f137-113">**General**</span></span>

- <span data-ttu-id="4f137-114">Parandatud: värskendada Project Service Automation, et rakendada rakenduse Team Member litsentsid (Projekti ressursside keskus sisaldab Team Memberi teenuse plaani metaandmeid 3.x)</span><span class="sxs-lookup"><span data-stu-id="4f137-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="4f137-115">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="4f137-115">**Time and Expense**</span></span>

- <span data-ttu-id="4f137-116">Parandatud: ei ole võimalik muuta kuluprognoosi nullist erinevalt hinnalt nulli (0) peale.</span><span class="sxs-lookup"><span data-stu-id="4f137-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="4f137-117">Muudatust ignoreeritakse.</span><span class="sxs-lookup"><span data-stu-id="4f137-117">The change is ignored.</span></span>

<span data-ttu-id="4f137-118">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="4f137-118">**Project Management**</span></span>

- <span data-ttu-id="4f137-119">Parandatud: meeskonnaliikme positsiooni nimele on lisatud null-väärtuste kontroll.</span><span class="sxs-lookup"><span data-stu-id="4f137-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="4f137-120">Parandatud: **msdyn_userresourceid** väli olemil **msdyn_resourceassignment** on kasutuselt kõrvaldatud.</span><span class="sxs-lookup"><span data-stu-id="4f137-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="4f137-121">Parandatud: värskendus versioonilt 2.x versioonile 3.x käsitleb nüüd ülesande määrangute tühje panusekontuure.</span><span class="sxs-lookup"><span data-stu-id="4f137-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="4f137-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="4f137-122">**Sales**</span></span>

- <span data-ttu-id="4f137-123">Parandatud: **Arve.PreValidateInvoiceUpdate** käsitleb nüüd kirje omanike ümbermääramise stsenaariumi õigesti.</span><span class="sxs-lookup"><span data-stu-id="4f137-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="4f137-124">Parandatud: kui tehingu klass on **Aeg**, on **UnitGroup** redigeerimatu kõigi olemite, sealhulgas olemite **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** ja **ContractLineDetails**, korral.</span><span class="sxs-lookup"><span data-stu-id="4f137-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="4f137-125">Siiski, **Ühik** on redigeerimatu ainult olemite **JournalLine** ja **InvoiceLineDetails** korral.</span><span class="sxs-lookup"><span data-stu-id="4f137-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


