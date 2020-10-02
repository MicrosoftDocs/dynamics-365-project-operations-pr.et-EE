---
title: Kviitungi vastendamine kuluga OCR-i kasutades
description: Selles teemas antakse teavet kviitungite tähemärkide optilise tuvastamise (OCR) töötlemise kohta.
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
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896996"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="10cf2-103">Kviitungi vastendamine kuluga OCR-i kasutades</span><span class="sxs-lookup"><span data-stu-id="10cf2-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="10cf2-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="10cf2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="10cf2-105">Kulude sisetamist on täiustatud kviitungite tähemärkide optilise tuvastamise (OCR) töötlemise juurutamisega.</span><span class="sxs-lookup"><span data-stu-id="10cf2-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="10cf2-106">See funktsioon on mõeldud kuluaruannete loomisel kasutuskogemuse parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="10cf2-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="10cf2-107">Põhifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="10cf2-107">Key features</span></span>

- <span data-ttu-id="10cf2-108">Süsteem ekstraktib kviitungitelt kaupmehe nime, kuupäeva ja kogusumma.</span><span class="sxs-lookup"><span data-stu-id="10cf2-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="10cf2-109">Süsteem proovib vastendada mitteseotud kviitungid mitteseotud kulutehingutega.</span><span class="sxs-lookup"><span data-stu-id="10cf2-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="10cf2-110">Võite kviitungitest luua käsitsi sisestatud kulutehinguid.</span><span class="sxs-lookup"><span data-stu-id="10cf2-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="10cf2-111">Kviitungite manustamine kuluaruande külge</span><span class="sxs-lookup"><span data-stu-id="10cf2-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="10cf2-112">Kui soovite kuluaruande loomisel automaatselt manustada sinna ka krediitkaardi tehingute kviitungid, täitke järgmised etapid.</span><span class="sxs-lookup"><span data-stu-id="10cf2-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="10cf2-113">Avage tööruum **Kuluhaldus**.</span><span class="sxs-lookup"><span data-stu-id="10cf2-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="10cf2-114">Kontrollige vahekaardil **Kviitungid**, kas manustamata kviitungeid on.</span><span class="sxs-lookup"><span data-stu-id="10cf2-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="10cf2-115">Vahekaardil **Kviitungid** saate kviitungeid ka üles laadida.</span><span class="sxs-lookup"><span data-stu-id="10cf2-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="10cf2-116">Kontrollige vahekaardil **Kulud**, kas manustamata kulusid on.</span><span class="sxs-lookup"><span data-stu-id="10cf2-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="10cf2-117">Tavaliselt impordib kuluhaldur need kulud krediitkaardi pakkujalt.</span><span class="sxs-lookup"><span data-stu-id="10cf2-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="10cf2-118">Valige **Uus kuluaruanne**.</span><span class="sxs-lookup"><span data-stu-id="10cf2-118">Select **New expense report**.</span></span> <span data-ttu-id="10cf2-119">Pange tähele, et saate nüüd kuluaruande loomisel kaasata ka kulud ja kviitungid.</span><span class="sxs-lookup"><span data-stu-id="10cf2-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="10cf2-120">Kui lisate nii kulud kui ka kviitungid, käivitatakse kviitungite automaatne vastendamine kuludega.</span><span class="sxs-lookup"><span data-stu-id="10cf2-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="10cf2-121">Looge või vastendage kviitungid kuluaruandesse</span><span class="sxs-lookup"><span data-stu-id="10cf2-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="10cf2-122">Kulu loomiseks või kulu kviitungi kaudu vastendamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="10cf2-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="10cf2-123">Manustage kviitung kuluaruande vahekaardile **Kviitungid**, valides suvandi **Lisa kviitungeid**.</span><span class="sxs-lookup"><span data-stu-id="10cf2-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="10cf2-124">Pange tähele kviitungi üleslaaditud pildi all suvandeid **Loo** ja **Vastenda**.</span><span class="sxs-lookup"><span data-stu-id="10cf2-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="10cf2-125">Valige **Loo**, et luua käsitsi sisestatud kulukanne ja täitke arvelt saadud väärtused.</span><span class="sxs-lookup"><span data-stu-id="10cf2-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="10cf2-126">Kui valite suvandi **Vastenda**, proovib süsteem vastendada olemasoleva kulu kviitungiga.</span><span class="sxs-lookup"><span data-stu-id="10cf2-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="10cf2-127">Installimine</span><span class="sxs-lookup"><span data-stu-id="10cf2-127">Installation</span></span>

<span data-ttu-id="10cf2-128">Nende täiustatud kulude võimaluste kasutamiseks installige Microsoft Dynamics 365 Finance'i jaoks kuluhaldusteenuse lisandmoodul ja lülitage sisse oma eksemplari funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="10cf2-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="10cf2-129">Lisandmoodulile pääsete ligi oma projektist teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu.</span><span class="sxs-lookup"><span data-stu-id="10cf2-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="10cf2-130">Logige LCS-i sisse ja avage soovitud keskkond.</span><span class="sxs-lookup"><span data-stu-id="10cf2-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="10cf2-131">Minge jaotisse **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="10cf2-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="10cf2-132">Valige käsk **Säilita** või Kerige alla kiirkaardile **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="10cf2-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="10cf2-133">Valige käsk **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="10cf2-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="10cf2-134">Valige jaotis **Kuluhaldusteenus**.</span><span class="sxs-lookup"><span data-stu-id="10cf2-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="10cf2-135">Järgige installiviisardi juhiseid ja nõustuge tingimustega.</span><span class="sxs-lookup"><span data-stu-id="10cf2-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="10cf2-136">Valige käsk **Installi**.</span><span class="sxs-lookup"><span data-stu-id="10cf2-136">Select **Install**.</span></span>

<span data-ttu-id="10cf2-137">Lülitage välja tööruumis **Funktsioonide haldus** sisse järgmised funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="10cf2-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="10cf2-138">Ümberkujundatud kuluaruanded</span><span class="sxs-lookup"><span data-stu-id="10cf2-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="10cf2-139">Automaatne vastendamine ja kviitungist kulu loomine</span><span class="sxs-lookup"><span data-stu-id="10cf2-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="10cf2-140">Nende funktsioonide sisselülitamisel tehakse järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="10cf2-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="10cf2-141">Olemasolev tööruum **Kuluhaldus** asendatakse uue tööruumiga.</span><span class="sxs-lookup"><span data-stu-id="10cf2-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="10cf2-142">Lisatakse uus menüü element kulu välja nähtavuse kohta.</span><span class="sxs-lookup"><span data-stu-id="10cf2-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="10cf2-143">Saate siiski avada eelmise lehe **Kuluaruanded**, avades jaotise **Kuluhaldus > Minu kulud > Kuluaruanded**.</span><span class="sxs-lookup"><span data-stu-id="10cf2-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="10cf2-144">Töövood ja kõik kinnitused viivad teid ikka olemasolevate kuluaruannete lehele.</span><span class="sxs-lookup"><span data-stu-id="10cf2-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="10cf2-145">Kviitungeid töödeldakse Microsoft Azure Cognitive Services'i kaudu ja metaandmed eraldatakse ning lisatakse.</span><span class="sxs-lookup"><span data-stu-id="10cf2-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="10cf2-146">Lisatakse suvand, mis võimaldab luua kuluaruande, mis sisaldab vastendatud kinnitamata kviitungeid.</span><span class="sxs-lookup"><span data-stu-id="10cf2-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="10cf2-147">Suvand, mis lisatakse kuluaruannetesse, võimaldab teil luua kviitungi põhjal kulurea või üritab vastendada olemasoleva kviitungi olemasoleva kulureaga.</span><span class="sxs-lookup"><span data-stu-id="10cf2-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="10cf2-148">Korduma kippuvad küsimused</span><span class="sxs-lookup"><span data-stu-id="10cf2-148">Frequently asked questions</span></span>

<span data-ttu-id="10cf2-149">**Kas Microsoft kasutab oma mudelite jaoks minu andmeid?**</span><span class="sxs-lookup"><span data-stu-id="10cf2-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="10cf2-150">Ei, Microsoft on oma kviitungite töötlemise teenuse jaoks loonud üldise masinõppe mudeli.</span><span class="sxs-lookup"><span data-stu-id="10cf2-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="10cf2-151">See mudel ei põhine teie üleslaetud kviitungitel.</span><span class="sxs-lookup"><span data-stu-id="10cf2-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="10cf2-152">**Kus see funktsioon on saadaval ja töödeldud?**</span><span class="sxs-lookup"><span data-stu-id="10cf2-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="10cf2-153">Praegu toetatakse seda Ameerika Ühendriikides.</span><span class="sxs-lookup"><span data-stu-id="10cf2-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="10cf2-154">**Kuhu minu kviitungid lähevad?**</span><span class="sxs-lookup"><span data-stu-id="10cf2-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="10cf2-155">Finance kontakteerub rakendusega Cognitive Services, et eraldada väljade andmeid.</span><span class="sxs-lookup"><span data-stu-id="10cf2-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="10cf2-156">Rakendus Cognitive Services säilitab töötlemisel teie kviitungi koopiat kuni 24ks tunniks.</span><span class="sxs-lookup"><span data-stu-id="10cf2-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="10cf2-157">Pärast töötlemise lõpuleviimist eemaldab Cognitive Services kviitungi.</span><span class="sxs-lookup"><span data-stu-id="10cf2-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="10cf2-158">Kviitungid talletatakse endiselt rakenduses Finance.</span><span class="sxs-lookup"><span data-stu-id="10cf2-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="10cf2-159">Lisateavet leiate teemast [Kviitungite mõitsmise lubamine vormituvastaja uue võimalusega](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="10cf2-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
