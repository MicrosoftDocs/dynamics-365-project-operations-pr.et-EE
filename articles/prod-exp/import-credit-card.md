---
title: Krediitkaarditehingute importimine ja säilitamine
description: Selles teemas kirjeldatakse kuluga seotud krediitkaarditehingute importimist ja haldamist. Neid tehinguid saab seadistada nii, et need imporditakse automaatselt regulaarselt teatud aja tagant, või neid saab vajaduse kohaselt käsitsi importida.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: edeab157aa2fa6cf518ad086b4c1f22c5b45fa04
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005156"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="3dc56-104">Krediitkaarditehingute importimine ja säilitamine</span><span class="sxs-lookup"><span data-stu-id="3dc56-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="3dc56-105">Kuluga seotud krediitkaarditehinguid saab seadistada nii, et need imporditakse automaatselt korduvas ajakava põhjal.</span><span class="sxs-lookup"><span data-stu-id="3dc56-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="3dc56-106">Teise võimalusena saab kandeid käsitsi vajadusel importida.</span><span class="sxs-lookup"><span data-stu-id="3dc56-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="3dc56-107">Krediitkaarditehinguid imporditakse krediitkaarditehingute andmete olemi kaudu.</span><span class="sxs-lookup"><span data-stu-id="3dc56-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="3dc56-108">Lisateavet andmeolemite kohta leiate teemast [Andmeolemid ](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="3dc56-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="3dc56-109">Krediitkaarditehingute importimine</span><span class="sxs-lookup"><span data-stu-id="3dc56-109">Import credit card transactions</span></span>

1. <span data-ttu-id="3dc56-110">Valige lehel **Krediitkaarditehingud** suvand **impordi tehingud**.</span><span class="sxs-lookup"><span data-stu-id="3dc56-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="3dc56-111">Kui avate andmehaldust esimest korda, peab süsteem enne jätkamist värskendama andmete olemite loendit.</span><span class="sxs-lookup"><span data-stu-id="3dc56-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="3dc56-112">Sisestage väljale **Nimi** imporditoimingule kordumatu kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="3dc56-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="3dc56-113">Valige väljal **Allika andmete vorming** imporditavaid krediitkaarditehinguid sisaldava faili vorming.</span><span class="sxs-lookup"><span data-stu-id="3dc56-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="3dc56-114">Valige **Laadi üles** ja seejärel otsige ja valige imporditav fail.</span><span class="sxs-lookup"><span data-stu-id="3dc56-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="3dc56-115">Pärast seda, kui fail on üles laaditud, valideerige krediitkaarditehingute faili vastendamine krediitkaarditehingute andmete olemi veergudega, valides paanil lingi **Vaata kaarti**.</span><span class="sxs-lookup"><span data-stu-id="3dc56-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="3dc56-116">Kui vastendamisel esineb vigu või kui peate vastendust muutma, muutke vastendust kas vahekaardilt **Vastenduse visualiseerimine** või vahekaardilt **Vastendamise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="3dc56-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="3dc56-117">Krediitkaarditehingute automatiseerimiseks valige **Loo korduvate andmete töö**.</span><span class="sxs-lookup"><span data-stu-id="3dc56-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="3dc56-118">Seejärel saate määrata korduvuse, mis määratleb, kui tihti tuleb krediitkaarditehinguid importida.</span><span class="sxs-lookup"><span data-stu-id="3dc56-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="3dc56-119">Kui olete lõpetanud, valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="3dc56-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="3dc56-120">Valitud faili kohe importimiseks valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="3dc56-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="3dc56-121">Kui importimisel ilmneb tõrkeid, saate vaadata täitmislogi või koondamise andmeid, et näha, milliseid vigu tuleb parandada, et aidata tagada edukat importimist.</span><span class="sxs-lookup"><span data-stu-id="3dc56-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="3dc56-122">Kui peate importima rohkem kui ühe failivormingu, peate looma eraldi importimistööd iga vormingu tüübi jaoks.</span><span class="sxs-lookup"><span data-stu-id="3dc56-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="3dc56-123">Lahkunud töötajate krediitkaarditehingute mujale määramine</span><span class="sxs-lookup"><span data-stu-id="3dc56-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="3dc56-124">Pärast seda, kui töötaja kirje on lõpetatud, on töötaja Active Directory Domain Services'i (AD DS) konto keelatud.</span><span class="sxs-lookup"><span data-stu-id="3dc56-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="3dc56-125">Siiski võib esineda aktiivseid krediitkaarditehinguid, mida peab veel kuludesse kandma ja tagasi maksma.</span><span class="sxs-lookup"><span data-stu-id="3dc56-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="3dc56-126">Lehelt **Krediitkaarditehingud** saate töötaja ümber määrata mistahes krediitkaarditehingu korral, kus seotud töötaja on töölt lahkunud.</span><span class="sxs-lookup"><span data-stu-id="3dc56-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="3dc56-127">Valige üks või mitu krediitkaarditehingut ja seejärel valige **Kannete ümbermääramine**.</span><span class="sxs-lookup"><span data-stu-id="3dc56-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="3dc56-128">Seejärel saate valida mõne muu töötaja, kellele soovite krediitkaarditehingud määrata.</span><span class="sxs-lookup"><span data-stu-id="3dc56-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="3dc56-129">Pärast seda, kui krediitkaarditehingud on ümber määratud, saab neid valida kuluaruande jaoks ja tagasi maksta kuluaruande tavalise protsessi kaudu.</span><span class="sxs-lookup"><span data-stu-id="3dc56-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]