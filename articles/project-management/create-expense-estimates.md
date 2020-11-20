---
title: Kuluprognoosid
description: Selles teemas antakse teavet projektipõhiste kulude määratlemise või prognoosimise kohta.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 10872366453985561bda0c07e50cff7f5f6d333e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131698"
---
# <a name="expense-estimates"></a><span data-ttu-id="3030e-103">Kuluprognoosid</span><span class="sxs-lookup"><span data-stu-id="3030e-103">Expense estimates</span></span>
<span data-ttu-id="3030e-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="3030e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3030e-105">Lisaks ressursipõhiste prognooside määraltemisele võimaldab Dynamics 365 Project Operations projektijuhtidel määratleda iga projekti projektipõhised kulud.</span><span class="sxs-lookup"><span data-stu-id="3030e-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="3030e-106">Iga kulukirje saab seostada kindla projekti ülesande või kulukategooriaga.</span><span class="sxs-lookup"><span data-stu-id="3030e-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="3030e-107">Kulukategooriad on tavaliselt määratletud organisatsiooni tasemel.</span><span class="sxs-lookup"><span data-stu-id="3030e-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="3030e-108">Iga kulukategooria hinna määratleb tavaliselt järgmine hierarhia.</span><span class="sxs-lookup"><span data-stu-id="3030e-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="3030e-109">Organisatsioon</span><span class="sxs-lookup"><span data-stu-id="3030e-109">Organization</span></span>
- <span data-ttu-id="3030e-110">Klient</span><span class="sxs-lookup"><span data-stu-id="3030e-110">Customer</span></span>
- <span data-ttu-id="3030e-111">Hinnapakkumine/leping</span><span class="sxs-lookup"><span data-stu-id="3030e-111">Quote/contract</span></span>

<span data-ttu-id="3030e-112">Projekti kulu vaatamiseks, lisamiseks või kustutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3030e-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="3030e-113">Avage **Projektid** ja valige projekt, mille kallal soovite töötada.</span><span class="sxs-lookup"><span data-stu-id="3030e-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="3030e-114">Valige vahekaart **Projekti prognoosid** ja vaadake projekti kulude loendit.</span><span class="sxs-lookup"><span data-stu-id="3030e-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="3030e-115">Valige uue kulu lisamiseks suvand **Uus kulu**.</span><span class="sxs-lookup"><span data-stu-id="3030e-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="3030e-116">Või valige kustutamiseks kulu ja valige seejärel **Kustuta kulu**.</span><span class="sxs-lookup"><span data-stu-id="3030e-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="3030e-117">Iga kulurea üksuse jaoks on määratletud järgmised atribuudid.</span><span class="sxs-lookup"><span data-stu-id="3030e-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="3030e-118">**Kategooria**: levinud rühmitused, mida kasutatakse kõigi projektiga seotud kulude kirjeldamiseks.</span><span class="sxs-lookup"><span data-stu-id="3030e-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="3030e-119">**Alguskuupäev**: kulu prognoositav tekkimise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="3030e-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="3030e-120">**Kogus**: kindla kategooria kuluüksuste eeldatav arv.</span><span class="sxs-lookup"><span data-stu-id="3030e-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="3030e-121">**Ühiku omahind**: kulu maksumuse arvutamiseks kasutatava ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="3030e-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="3030e-122">**Ühiku müügihind**: kulu müüguhinna arvutamiseks kasutatava ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="3030e-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

