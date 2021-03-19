---
title: Käsitsi näidisarve loomine – liht
description: Selles teemas antakse teavet Project Operationsis näidisarvete käsitsi loomise kohta.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274183"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="95ab0-103">Käsitsi näidisarve loomine – liht</span><span class="sxs-lookup"><span data-stu-id="95ab0-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="95ab0-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="95ab0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="95ab0-105">Dynamics 365 Project Operationsis saab vajadusel proforma arveid luua käsitsi.</span><span class="sxs-lookup"><span data-stu-id="95ab0-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="95ab0-106">Saate loendilehel **Projekti lepingud** või üksikasjade lehel **Projekti leping** käsitsi näidisarve luua.</span><span class="sxs-lookup"><span data-stu-id="95ab0-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="95ab0-107">Projektilepingu loendileht</span><span class="sxs-lookup"><span data-stu-id="95ab0-107">Project Contracts list page</span></span>

<span data-ttu-id="95ab0-108">Valige loendilehelt **Projekti lepingud** üks või mitu projekti lepingut ja looge kõigi valitud kirjete jaoks arved.</span><span class="sxs-lookup"><span data-stu-id="95ab0-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="95ab0-109">Süsteem kontrollib, millisel valitud projekti lepingutest on suvandi **Arveldamiseks valmis** võlgnevus tänasest kuupäevast varasem.</span><span class="sxs-lookup"><span data-stu-id="95ab0-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="95ab0-110">Nendest lepingutest loob süsteem näidisarvete mustandeid.</span><span class="sxs-lookup"><span data-stu-id="95ab0-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="95ab0-111">Kui projekti lepingul on mitu klienti, võib kliendi kohta olla loodud üks arve ja projekti lepingu kohta mitu arvet.</span><span class="sxs-lookup"><span data-stu-id="95ab0-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="95ab0-112">Kõik loodud projekti arved on saadaval lehe **Arve** jaotises **Arveldamine** alas **Müük**.</span><span class="sxs-lookup"><span data-stu-id="95ab0-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="95ab0-113">Projekti lepingu üksikasjade leht</span><span class="sxs-lookup"><span data-stu-id="95ab0-113">Project Contract details page</span></span>

<span data-ttu-id="95ab0-114">Proforma arve saab luua ka **Projekti lepingu** üksikasjade lehelt.</span><span class="sxs-lookup"><span data-stu-id="95ab0-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="95ab0-115">Süsteem kontrollib, et projekti lepingul on **Arveldamiseks valmis** võlgnevus tänasest kuupäevast varasem.</span><span class="sxs-lookup"><span data-stu-id="95ab0-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="95ab0-116">Nendest lepingutest loob süsteem iga lepingurea klientide arvu põhjal näidisarvete mustandid.</span><span class="sxs-lookup"><span data-stu-id="95ab0-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="95ab0-117">Kui loodud on üks näidisarve, avaneb leht **Arve**.</span><span class="sxs-lookup"><span data-stu-id="95ab0-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="95ab0-118">Kui selle projektilepingu jaoks luuakse mitu arvet, avaneb loendileht **Arved**, et kuvada kõiki loodud arveid.</span><span class="sxs-lookup"><span data-stu-id="95ab0-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]