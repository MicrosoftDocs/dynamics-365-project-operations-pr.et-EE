---
title: Finantsdimensiooni vaikeväärtused
description: Selles teemas antakse teavet, kuidas häälestada finantsdimensiooni vaikeväärtused.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131878"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="dbf01-103">Finantsdimensiooni vaikeväärtused</span><span class="sxs-lookup"><span data-stu-id="dbf01-103">Financial dimension defaults</span></span>

<span data-ttu-id="dbf01-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="dbf01-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dbf01-105">Dynamics 365 Project Operationskasutab [finantsdimensioonide](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) raamistikku rakenduses Dynamics 365 Finance, et pakkuda projekti alammooduli ja üldiste pearaamatu tehingute kohta täiendavad ülevaateid.</span><span class="sxs-lookup"><span data-stu-id="dbf01-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="dbf01-106">Vaikimisi finantsdimensioonid saab määrata kliendile, projekti finantseerimisallikale, vahe-eesmärgile, projekti leingureale või projektile.</span><span class="sxs-lookup"><span data-stu-id="dbf01-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="dbf01-107">Kliendi vaikimisi finantsdimensioonide määratlemine</span><span class="sxs-lookup"><span data-stu-id="dbf01-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="dbf01-108">Rakenduses Finance määratletud kliendi dimensiooni vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="dbf01-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="dbf01-109">Dimensiooni vaikeväärtuste määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="dbf01-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="dbf01-110">Avage **Mügireskontro** > **Kliendid** > **Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="dbf01-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="dbf01-111">Lehe **Kliendid** vahekaardil **Finantsdimensioonid** määrake konkreetse kliendi finantsdimensiooni väärtused.</span><span class="sxs-lookup"><span data-stu-id="dbf01-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="dbf01-112">Projektilepingute vaikimisi finantsdimensioonide määratlemine</span><span class="sxs-lookup"><span data-stu-id="dbf01-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="dbf01-113">Projektilepinguid luuakse ja hallatakse teenuses Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="dbf01-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="dbf01-114">Projektilepingute raamatupidamise atribuudid määratakse rakenduse Finance moodulis **Projektihaldus ja raamatupidamine**.</span><span class="sxs-lookup"><span data-stu-id="dbf01-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="dbf01-115">Projekti finantseerimisallika finantsdimensioonide määramine</span><span class="sxs-lookup"><span data-stu-id="dbf01-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="dbf01-116">Avage **Projektijuhtimine ja raamatupidamine** > **Projektid** > **Projekti lepingud**.</span><span class="sxs-lookup"><span data-stu-id="dbf01-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="dbf01-117">Valige kirje, mida soovite värskendada, ja valige vahekaardil **Projektileping** suvand **Kuva vaikimisi raamatupidamine**.</span><span class="sxs-lookup"><span data-stu-id="dbf01-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="dbf01-118">Laiendage suvandit **Seotud teave** ja valige vahekaart **Rahastamisallikad**.</span><span class="sxs-lookup"><span data-stu-id="dbf01-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="dbf01-119">Määrake finantsdimensiooni vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="dbf01-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="dbf01-120">Pange tähele, et finantsdimensioonide vaikeväärtused pärinevad kliendi kontolt.</span><span class="sxs-lookup"><span data-stu-id="dbf01-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="dbf01-121">Projekti lepingurea finantsdimensioonide määramine</span><span class="sxs-lookup"><span data-stu-id="dbf01-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="dbf01-122">Avage **Projektijuhtimine ja raamatupidamine** > **Projektid** > **Projekti lepingud**.</span><span class="sxs-lookup"><span data-stu-id="dbf01-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="dbf01-123">Valige kirje, mida soovite värskendada, ja valige vahekaardil **Projektileping** suvand **Kuva vaikimisi raamatupidamine**.</span><span class="sxs-lookup"><span data-stu-id="dbf01-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="dbf01-124">Laiendage suvandit **Seotud teave** ja valige vahekaart **Lepinguread**.</span><span class="sxs-lookup"><span data-stu-id="dbf01-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="dbf01-125">Määrake finantsdimensiooni vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="dbf01-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="dbf01-126">Finantsdimensioonide vaikeväärtused kehtivad ja saab kasutada ainult fikseeritud hinnaga (vahe-eesmärgi) lepinguridadega.</span><span class="sxs-lookup"><span data-stu-id="dbf01-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="dbf01-127">Neid vaikeväärtusi kasutatakse seostuvates projektides kontoga seotud kannetes ja arveridadel.</span><span class="sxs-lookup"><span data-stu-id="dbf01-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="dbf01-128">Projektide vaikimisi finantsdimensioonide määratlemine</span><span class="sxs-lookup"><span data-stu-id="dbf01-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="dbf01-129">Projekte luuakse ja hallatakse CDS-is.</span><span class="sxs-lookup"><span data-stu-id="dbf01-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="dbf01-130">Projektide raamatupidamise atribuudid määratakse rakenduse Finance moodulis **Projektihaldus ja raamatupidamine**.</span><span class="sxs-lookup"><span data-stu-id="dbf01-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="dbf01-131">Minge jaotisse **Projektijuhtimine ja raamatupidamine** > **Projektid** > **Kõik projektid**.</span><span class="sxs-lookup"><span data-stu-id="dbf01-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="dbf01-132">Valige kirje, mida soovite värskendada, ja valige vahekaardil **Projekt** suvand **Kuva vaikimisi raamatupidamine**.</span><span class="sxs-lookup"><span data-stu-id="dbf01-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="dbf01-133">Laiendage suvandit **Seotud teave** ja valige vahekaart **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="dbf01-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="dbf01-134">Määrake finantsdimensiooni vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="dbf01-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="dbf01-135">Pange tähele, et finantsdimensioonide vaikeväärtused pärinevad kliendi kontolt.</span><span class="sxs-lookup"><span data-stu-id="dbf01-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="dbf01-136">Kui projekt on seostatud mitme projektilepingu kliendiga lepingureaga, kasutatakse vaikimisi finatsdimensioonideks peamist klienti.</span><span class="sxs-lookup"><span data-stu-id="dbf01-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="dbf01-137">Projekti vaikimisi finantsdimensioone kasutatakse suvandis **Project Operationsi integreerimise tööleht** ja seotud projekti arvete ridade jaoks aja, kulu ja tasu kannete jaoks tööleherea vaikeväärtuste määramiseks.</span><span class="sxs-lookup"><span data-stu-id="dbf01-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
