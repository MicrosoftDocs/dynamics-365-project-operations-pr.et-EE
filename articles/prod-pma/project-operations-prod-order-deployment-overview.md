---
title: Rakenduse Project Operations ladustamise-/tootmispõhiste stsenaariumite jaoks juurutamise ülevaade
description: Selles teemas antakse teavet juurutuse tüübi kohta Project Operationsi ladustamise-/tootmispõhistes stsenaariumides.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7bad4de10a508f0c1aa2cc6bb0c41081f81fb259
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365450"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="37e04-103">Rakenduse Project Operations ladustamise-/tootmispõhiste stsenaariumite jaoks juurutamise ülevaade</span><span class="sxs-lookup"><span data-stu-id="37e04-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="37e04-104">_**Kehtib järgmiste puhul:** Project Operations ladustamise-/tootmispõhiste stsenaariumide jaoks_</span><span class="sxs-lookup"><span data-stu-id="37e04-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="37e04-105">Sellel juurutuse tüübil on projektipõhiste ettevõtete jaoks järgmised võimalused.</span><span class="sxs-lookup"><span data-stu-id="37e04-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="37e04-106">Projekti kavandamine kasutades [tööjaotuse struktuure](work-breakdown-structures.md)</span><span class="sxs-lookup"><span data-stu-id="37e04-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="37e04-107">Projektide ladustatud varude hankimine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="37e04-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="37e04-108">Projektipõhise müügi haldamine kasutades **müügi ja turunduse** moodulit Dynamics 365 Finance and Operationsi rakendustes</span><span class="sxs-lookup"><span data-stu-id="37e04-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="37e04-109">Projekti hinnakujundus ja kuluarvestus kasutades kulumäära ja arveldusmäära konfiguratsioone Finance and Operationsi rakendustes</span><span class="sxs-lookup"><span data-stu-id="37e04-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="37e04-110">Projektide ressursihaldus Finance and Operationsi rakendustes</span><span class="sxs-lookup"><span data-stu-id="37e04-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="37e04-111">Projekti edenemise ja aja jälgimine Finance and Operationsi rakendustes</span><span class="sxs-lookup"><span data-stu-id="37e04-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="37e04-112">Kuluhalduse kasutuskogemus projekti- ja mitte-projektipõhiste kulude jaoks koos kviitungite hõivamise OCR-i võimaluse kasutamisega</span><span class="sxs-lookup"><span data-stu-id="37e04-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="37e04-113">Arveldamine ettevõtte tasemel käibemaksu ja kuupäevapõhise vahetuskursi süsteemi kasutades</span><span class="sxs-lookup"><span data-stu-id="37e04-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="37e04-114">Konfigureeritavad projektirühmad poolelioleva töö raamatupidamise ja viitvõlgade jaoks</span><span class="sxs-lookup"><span data-stu-id="37e04-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="37e04-115">Projektide tulude kajastamine</span><span class="sxs-lookup"><span data-stu-id="37e04-115">Project revenue recognition</span></span>

<span data-ttu-id="37e04-116">See juurutuse tüüp pakub lisaks rakenduste Dynamics 365 Finance ja Dynamics 365 Supply Chain Management pakutavate funktsioonide laiendust.</span><span class="sxs-lookup"><span data-stu-id="37e04-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="37e04-117">Valige see juurutamise tüüp, et kasutada rakendust Dynamics 365 Project Operations projekti täispika elutsükli jaoks, mis sisaldab järgmisi põhinõudeid.</span><span class="sxs-lookup"><span data-stu-id="37e04-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="37e04-118">Ulatuslik projektijuhtimissüsteem, mis haldab inventeeritud üksusi ja töö/tootmise tellimuse maksumust ajakavade ja finantsasjade jaoks sisemiseks kasutuseks ja arveldatavate projektide jaoks.</span><span class="sxs-lookup"><span data-stu-id="37e04-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="37e04-119">Organisatsioonil on juba Dynamics 365 Finance või Dynamics 365 tarneahela ja tootmise rakendused olemas ning projektipõhiste tehingute integreerimine lihtsustab andmetele juurdepääsu ja aruandluse vajadusi.</span><span class="sxs-lookup"><span data-stu-id="37e04-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="37e04-120">Täielikult toimib kuluhaldussüsteem, mis hõlmab poliitika jõustamisi ja tagasimakseid projektipõhiste ja mitte-projektipõhiste kulude jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="37e04-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="37e04-121">Ettevõtte tasemel käibemaksu ja vahetuskursi määra mootor kliendile suunatud arvete loomiseks.</span><span class="sxs-lookup"><span data-stu-id="37e04-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="37e04-122">Rahvusvaheliste finantsaruandluse standardite (IFRS) nõuetele vastavad projekti raamatupidamise ja tuluarvestuse süsteem.</span><span class="sxs-lookup"><span data-stu-id="37e04-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>

