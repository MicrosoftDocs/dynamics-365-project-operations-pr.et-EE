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
ms.openlocfilehash: 3f0429366c69346113003355679c055cd2c74ca3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287053"
---
# <a name="expense-estimates"></a><span data-ttu-id="66e33-103">Kuluprognoosid</span><span class="sxs-lookup"><span data-stu-id="66e33-103">Expense estimates</span></span>
<span data-ttu-id="66e33-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="66e33-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="66e33-105">Koos ressursipõhiste prognooside määratlemisega võimaldab Dynamics 365 Project Operations projektijuhtidel määratleda iga projekti jaoks projektipõhiseid kulusid.</span><span class="sxs-lookup"><span data-stu-id="66e33-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="66e33-106">Iga kulukirje saab seostada kindla projekti ülesande või kulukategooriaga.</span><span class="sxs-lookup"><span data-stu-id="66e33-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="66e33-107">Kulukategooriad on tavaliselt määratletud organisatsiooni tasemel.</span><span class="sxs-lookup"><span data-stu-id="66e33-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="66e33-108">Iga kulukategooria hinna määratleb tavaliselt järgmine hierarhia.</span><span class="sxs-lookup"><span data-stu-id="66e33-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="66e33-109">Organisatsioon</span><span class="sxs-lookup"><span data-stu-id="66e33-109">Organization</span></span>
- <span data-ttu-id="66e33-110">Klient</span><span class="sxs-lookup"><span data-stu-id="66e33-110">Customer</span></span>
- <span data-ttu-id="66e33-111">Hinnapakkumine/leping</span><span class="sxs-lookup"><span data-stu-id="66e33-111">Quote/contract</span></span>

<span data-ttu-id="66e33-112">Projekti kulu vaatamiseks, lisamiseks või kustutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="66e33-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="66e33-113">Avage **Projektid** ja valige projekt, mille kallal soovite töötada.</span><span class="sxs-lookup"><span data-stu-id="66e33-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="66e33-114">Valige vahekaart **Projekti prognoosid** ja vaadake projekti kulude loendit.</span><span class="sxs-lookup"><span data-stu-id="66e33-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="66e33-115">Valige uue kulu lisamiseks suvand **Uus kulu**.</span><span class="sxs-lookup"><span data-stu-id="66e33-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="66e33-116">Või valige kustutamiseks kulu ja valige seejärel **Kustuta kulu**.</span><span class="sxs-lookup"><span data-stu-id="66e33-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="66e33-117">Iga kulurea üksuse jaoks on määratletud järgmised atribuudid.</span><span class="sxs-lookup"><span data-stu-id="66e33-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="66e33-118">**Kategooria**: levinud rühmitused, mida kasutatakse kõigi projektiga seotud kulude kirjeldamiseks.</span><span class="sxs-lookup"><span data-stu-id="66e33-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="66e33-119">**Alguskuupäev**: kulu prognoositav tekkimise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="66e33-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="66e33-120">**Kogus**: kindla kategooria kuluüksuste eeldatav arv.</span><span class="sxs-lookup"><span data-stu-id="66e33-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="66e33-121">**Ühiku omahind**: kulu maksumuse arvutamiseks kasutatava ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="66e33-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="66e33-122">**Ühiku müügihind**: kulu müüguhinna arvutamiseks kasutatava ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="66e33-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]