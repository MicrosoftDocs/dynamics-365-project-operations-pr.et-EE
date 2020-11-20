---
title: Käsitsi näidisarve loomine – liht
description: Selles teemas antakse teavet Project Operationsis näidisarvete käsitsi loomise kohta.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176381"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="76d7f-103">Käsitsi näidisarve loomine – liht</span><span class="sxs-lookup"><span data-stu-id="76d7f-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="76d7f-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="76d7f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="76d7f-105">Dynamics 365 Project Operationsis saab näidisarveid vajaduse kohaselt käsitsi luua.</span><span class="sxs-lookup"><span data-stu-id="76d7f-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="76d7f-106">Saate loendilehel **Projekti lepingud** või üksikasjade lehel **Projekti leping** käsitsi näidisarve luua.</span><span class="sxs-lookup"><span data-stu-id="76d7f-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="76d7f-107">Projektilepingu loendileht</span><span class="sxs-lookup"><span data-stu-id="76d7f-107">Project Contracts list page</span></span>

<span data-ttu-id="76d7f-108">Valige loendilehelt **Projekti lepingud** üks või mitu projekti lepingut ja looge kõigi valitud kirjete jaoks arved.</span><span class="sxs-lookup"><span data-stu-id="76d7f-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="76d7f-109">Süsteem kontrollib, millisel valitud projekti lepingutest on suvandi **Arveldamiseks valmis** võlgnevus tänasest kuupäevast varasem.</span><span class="sxs-lookup"><span data-stu-id="76d7f-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="76d7f-110">Nendest lepingutest loob süsteem näidisarvete mustandeid.</span><span class="sxs-lookup"><span data-stu-id="76d7f-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="76d7f-111">Kui projekti lepingul on mitu klienti, võib kliendi kohta olla loodud üks arve ja projekti lepingu kohta mitu arvet.</span><span class="sxs-lookup"><span data-stu-id="76d7f-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="76d7f-112">Kõik loodud projekti arved on saadaval lehe **Arve** jaotises **Arveldamine** alas **Müük**.</span><span class="sxs-lookup"><span data-stu-id="76d7f-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="76d7f-113">Projekti lepingu üksikasjade leht</span><span class="sxs-lookup"><span data-stu-id="76d7f-113">Project Contract details page</span></span>

<span data-ttu-id="76d7f-114">Näidisarve saab luua ka üksikasjade lehel **Projekti leping**, mis loob konkreetse projekti lepingu arve.</span><span class="sxs-lookup"><span data-stu-id="76d7f-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="76d7f-115">Süsteem kontrollib, kas projekti lepingul on suvandi **Arveldamiseks valmis** võlgnevus tänasest kuupäevast varasem.</span><span class="sxs-lookup"><span data-stu-id="76d7f-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="76d7f-116">Nendest lepingutest loob süsteem iga lepingurea klientide arvu põhjal näidisarvete mustandid.</span><span class="sxs-lookup"><span data-stu-id="76d7f-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="76d7f-117">Kui loodud on üks näidisarve, avaneb leht **Arve**.</span><span class="sxs-lookup"><span data-stu-id="76d7f-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="76d7f-118">Kui selle projekti lepingu jaoks on loodud mitu arvet, avaneb loendileht **Arved**, et kuvada kõik loodud arved.</span><span class="sxs-lookup"><span data-stu-id="76d7f-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
