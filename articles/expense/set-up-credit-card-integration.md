---
title: Krediitkaardi integratsiooni seadistamine
description: Selles teemas kirjeldatakse kuluga seotud krediitkaarditehingute importimist ja haldamist.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 483775e1334a281026dbfaf214d06d235255f13e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896816"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="880cb-103">Krediitkaardi integratsiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="880cb-103">Set up credit card integration</span></span>

<span data-ttu-id="880cb-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="880cb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="880cb-105">Kuluga seotud krediitkaarditehinguid saab seadistada nii, et need imporditakse automaatselt korduvas ajakava põhjal.</span><span class="sxs-lookup"><span data-stu-id="880cb-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="880cb-106">Teise võimalusena saab kandeid käsitsi vajadusel importida.</span><span class="sxs-lookup"><span data-stu-id="880cb-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="880cb-107">Krediitkaarditehinguid imporditakse krediitkaarditehingute andmete olemi kaudu.</span><span class="sxs-lookup"><span data-stu-id="880cb-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="880cb-108">Krediitkaarditehingute importimine</span><span class="sxs-lookup"><span data-stu-id="880cb-108">Import credit card transactions</span></span>

1. <span data-ttu-id="880cb-109">Valige lehel **Krediitkaarditehingud** suvand **impordi tehingud**.</span><span class="sxs-lookup"><span data-stu-id="880cb-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="880cb-110">Kui avate andmehaldust esimest korda, peab süsteem enne jätkamist värskendama andmete olemite loendit.</span><span class="sxs-lookup"><span data-stu-id="880cb-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="880cb-111">Sisestage väljale **Nimi** imporditoimingule kordumatu kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="880cb-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="880cb-112">Valige väljal **Allika andmete vorming** imporditavaid krediitkaarditehinguid sisaldava faili vorming.</span><span class="sxs-lookup"><span data-stu-id="880cb-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="880cb-113">Valige **Laadi üles** ja seejärel otsige ja valige imporditav fail.</span><span class="sxs-lookup"><span data-stu-id="880cb-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="880cb-114">Pärast seda, kui fail on üles laaditud, valideerige krediitkaarditehingute faili vastendamine krediitkaarditehingute andmete olemi veergudega, valides paanil lingi **Vaata kaarti**.</span><span class="sxs-lookup"><span data-stu-id="880cb-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="880cb-115">Kui vastendamisel esineb vigu või kui peate vastendust muutma, muutke vastendust kas vahekaardilt **Vastenduse visualiseerimine** või vahekaardilt **Vastendamise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="880cb-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="880cb-116">Krediitkaarditehingute automatiseerimiseks valige **Loo korduvate andmete töö**.</span><span class="sxs-lookup"><span data-stu-id="880cb-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="880cb-117">Seejärel saate määrata korduvuse, mis määratleb, kui tihti tuleb krediitkaarditehinguid importida.</span><span class="sxs-lookup"><span data-stu-id="880cb-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="880cb-118">Kui olete lõpetanud, valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="880cb-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="880cb-119">Valitud faili kohe importimiseks valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="880cb-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="880cb-120">Kui importimisel ilmneb tõrkeid, saate vaadata täitmislogi või koondamise andmeid, et näha, milliseid vigu tuleb parandada, et aidata tagada edukat importimist.</span><span class="sxs-lookup"><span data-stu-id="880cb-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="880cb-121">Kui peate importima rohkem kui ühe failivormingu, peate looma eraldi importimistööd iga vormingu tüübi jaoks.</span><span class="sxs-lookup"><span data-stu-id="880cb-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="880cb-122">Lahkunud töötajate krediitkaarditehingute mujale määramine</span><span class="sxs-lookup"><span data-stu-id="880cb-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="880cb-123">Pärast seda, kui töötaja kirje on lõpetatud, on töötaja Active Directory Domain Services'i (AD DS) konto keelatud.</span><span class="sxs-lookup"><span data-stu-id="880cb-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="880cb-124">Siiski võib esineda aktiivseid krediitkaarditehinguid, mida peab veel kuludesse kandma ja tagasi maksma.</span><span class="sxs-lookup"><span data-stu-id="880cb-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="880cb-125">Lehelt **Krediitkaarditehingud** saate töötaja ümber määrata mistahes krediitkaarditehingu korral, kus seotud töötaja on töölt lahkunud.</span><span class="sxs-lookup"><span data-stu-id="880cb-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="880cb-126">Valige üks või mitu krediitkaarditehingut ja seejärel valige **Kannete ümbermääramine**.</span><span class="sxs-lookup"><span data-stu-id="880cb-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="880cb-127">Seejärel saate valida mõne muu töötaja, kellele soovite krediitkaarditehingud määrata.</span><span class="sxs-lookup"><span data-stu-id="880cb-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="880cb-128">Pärast seda, kui krediitkaarditehingud on ümber määratud, saab neid valida kuluaruande jaoks ja tagasi maksta kuluaruande tavalise protsessi kaudu.</span><span class="sxs-lookup"><span data-stu-id="880cb-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
