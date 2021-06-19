---
title: Krediitkaardi integratsiooni seadistamine
description: Selles teemas selgitatakse, kuidas töötada kuludega seotud krediitkaarditehingutega.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001806"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="fcd6d-103">Krediitkaardi integratsiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="fcd6d-103">Set up credit card integration</span></span>

<span data-ttu-id="fcd6d-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="fcd6d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fcd6d-105">Kuluga seotud krediitkaarditehinguid saab seadistada nii, et need imporditakse automaatselt korduvas ajakava põhjal.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="fcd6d-106">Teise võimalusena saab kandeid käsitsi vajadusel importida.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="fcd6d-107">Krediitkaarditehinguid imporditakse krediitkaarditehingute andmete olemi kaudu.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="fcd6d-108">Krediitkaarditehingute importimine</span><span class="sxs-lookup"><span data-stu-id="fcd6d-108">Import credit card transactions</span></span>

<span data-ttu-id="fcd6d-109">Krediitkaarditehingute importimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="fcd6d-110">Valige lehel **Krediitkaarditehingud** suvand **impordi tehingud**.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="fcd6d-111">Kui avate andmehaldust esimest korda, peab süsteem enne jätkamist värskendama andmete olemite loendit.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="fcd6d-112">Sisestage väljale **Nimi** imporditöö kordumatu kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="fcd6d-113">Valige väljal **Allika andmete vorming** imporditavaid krediitkaarditehinguid sisaldava faili vorming.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="fcd6d-114">Valige **Laadi üles** ja seejärel otsige ja valige imporditav fail.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="fcd6d-115">Pärast seda, kui fail on üles laaditud, valideerige krediitkaarditehingute faili vastendamine krediitkaarditehingute andmete olemi veergudega, valides paanil lingi **Vaata kaarti**.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="fcd6d-116">Kui vastendamisel esineb vigu või kui peate vastendust muutma, muutke vastendust kas vahekaardilt **Vastenduse visualiseerimine** või vahekaardilt **Vastendamise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="fcd6d-117">Krediitkaarditehingute automatiseerimiseks valige **Loo korduvate andmete töö**.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="fcd6d-118">Seejärel saate määrata korduvuse, mis määratleb, kui tihti tuleb krediitkaarditehinguid importida.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="fcd6d-119">Kui olete lõpetanud, valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="fcd6d-120">Valitud faili kohe importimiseks valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="fcd6d-121">Kui importimise ajal tekib tõrkeid, saate vaadata käivituslogi või seadistusandmeid, et näha tõrkeid, mis tuleb eduka importimise tagamiseks parandada.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="fcd6d-122">Kui peate importima mitu failivormingut, peate looma iga vormingutüübi jaoks eraldi imporditööd.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="fcd6d-123">Lahkunud töötajate krediitkaarditehingute mujale määramine</span><span class="sxs-lookup"><span data-stu-id="fcd6d-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="fcd6d-124">Pärast seda, kui töötaja kirje on lõpetatud, on töötaja Active Directory Domain Services'i (AD DS) konto keelatud.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="fcd6d-125">Siiski võib esineda aktiivseid krediitkaarditehinguid, mida peab veel kuludesse kandma ja tagasi maksma.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="fcd6d-126">Lehel **Krediitkaarditehingud** saate määrata töötaja ümber mis tahes krediitkaarditehingu jaoks, kus seostatud töötaja on eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="fcd6d-127">Valige üks või mitu krediitkaarditehingut ja seejärel valige **Kannete ümbermääramine**.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="fcd6d-128">Seejärel saate valida mõne muu töötaja, kellele soovite krediitkaarditehingud määrata.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="fcd6d-129">Pärast seda, kui krediitkaarditehingud on ümber määratud, saab neid valida kuluaruande jaoks ja tagasi maksta kuluaruande tavalise protsessi kaudu.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="fcd6d-130">Krediitkaarditehingute kustutamine</span><span class="sxs-lookup"><span data-stu-id="fcd6d-130">Delete credit card transactions</span></span> 

<span data-ttu-id="fcd6d-131">Mõnikord võib pärast krediitkaarditehingute importimist olla vaja teatud tehingud kustutada.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="fcd6d-132">Selle põhjuseks võib olla, et tehingud on duplikaadid või kuna andmed ei pruugi olla täpsed.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="fcd6d-133">Administraatorid saavad kasutada funktsiooni **Kustuta krediitkaartide tehingud**, et valida ja kustutada krediidikaarditehingud, mis pole kuluaruandele **lisatud**.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="fcd6d-134">Avage **Perioodilised ülesanded** > **Krediitkaarditehingute kustutamine**.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="fcd6d-135">Valige **Filter** ja sisestage kaasatavate kirjete tuvastamiseks teave.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="fcd6d-136">Kirjete kustutamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
