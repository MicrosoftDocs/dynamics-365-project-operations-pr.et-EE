---
title: Kuludokumentide töötlemine
description: Selles teemas antakse teavet kviitungite tähemärkide optilise tuvastamise (OCR) töötlemise kohta. See funktsioon on mõeldud rakenduses Microsoft Dynamics 365 Finance kuluaruannete loomisel kasutuskogemuse parandamiseks.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 57ef67412eb3c5795559e4f6d011e97c4d7a1338
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271798"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="b393e-104">Kuludokumentide töötlemine</span><span class="sxs-lookup"><span data-stu-id="b393e-104">Expense receipt processing</span></span>

<span data-ttu-id="b393e-105">Kulude sisetamist on täiustatud kviitungite tähemärkide optilise tuvastamise (OCR) töötlemise juurutamisega.</span><span class="sxs-lookup"><span data-stu-id="b393e-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="b393e-106">See funktsioon on mõeldud kuluaruannete loomisel kasutuskogemuse parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="b393e-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="b393e-107">Põhifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="b393e-107">Key features</span></span>

- <span data-ttu-id="b393e-108">Kviitungitelt ekstraktitakse kaupmehe nim, kuupäev ja kogusumma.</span><span class="sxs-lookup"><span data-stu-id="b393e-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="b393e-109">Funktsioon proovib vastendada mitteseotud kviitungid mitteseotud kulutehingutega.</span><span class="sxs-lookup"><span data-stu-id="b393e-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="b393e-110">Kasutajad võivad kviitungitest luua käsitsi sisestatud kulutehinguid.</span><span class="sxs-lookup"><span data-stu-id="b393e-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="b393e-111">Näited kasutuse kohta</span><span class="sxs-lookup"><span data-stu-id="b393e-111">Usage examples</span></span>

<span data-ttu-id="b393e-112">Kui soovite kuluaruande loomisel automaatselt manustada sinna ka krediitkaardi tehingute kviitungid, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b393e-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="b393e-113">Avage tööruum **Kuluhaldus**.</span><span class="sxs-lookup"><span data-stu-id="b393e-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="b393e-114">Kontrollige vahekaardil **Kviitungid**, kas manustamata kviitungeid on.</span><span class="sxs-lookup"><span data-stu-id="b393e-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="b393e-115">Vahekaardil **Kviitungid** saate kviitungeid ka üles laadida.</span><span class="sxs-lookup"><span data-stu-id="b393e-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="b393e-116">Kontrollige vahekaardil **Kulud**, kas manustamata kulusid on.</span><span class="sxs-lookup"><span data-stu-id="b393e-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="b393e-117">Tavaliselt impordib kuluhaldur need kulud krediitkaardi pakkujalt.</span><span class="sxs-lookup"><span data-stu-id="b393e-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="b393e-118">Valige **Uus kuluaruanne**.</span><span class="sxs-lookup"><span data-stu-id="b393e-118">Select **New expense report**.</span></span> <span data-ttu-id="b393e-119">Pange tähele, et saate nüüd kuluaruande loomisel kaasata ka kulud ja kviitungid.</span><span class="sxs-lookup"><span data-stu-id="b393e-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="b393e-120">Kui lisate nii kulud kui ka kviitungid, käivitatakse kviitungite automaatne vastendamine kuludega.</span><span class="sxs-lookup"><span data-stu-id="b393e-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="b393e-121">Kulu loomiseks või kulu kviitungi kaudu vastendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b393e-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="b393e-122">Manustage kviitung kuluaruande vahekaardile **Kviitungid**, valides suvandi **Lisa kviitungeid**.</span><span class="sxs-lookup"><span data-stu-id="b393e-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="b393e-123">Pange tähele kviitungi üleslaaditud pildi all suvandeid **Loo** ja **Vastenda**.</span><span class="sxs-lookup"><span data-stu-id="b393e-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="b393e-124">Valige **Loo**, et luua käsitsi sisestatud kulukanne ja täitke arvelt saadud väärtused.</span><span class="sxs-lookup"><span data-stu-id="b393e-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="b393e-125">Kui valite suvandi **Vastenda**, proovib süsteem vastendada olemasoleva kulu kviitungiga.</span><span class="sxs-lookup"><span data-stu-id="b393e-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="b393e-126">Installimine</span><span class="sxs-lookup"><span data-stu-id="b393e-126">Installation</span></span>

<span data-ttu-id="b393e-127">See funktsioon töötab koos funktsiooniga **Kuluaruannete ümberkujundamine**, et aidata lihtsustada kulu kogemust.</span><span class="sxs-lookup"><span data-stu-id="b393e-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="b393e-128">See funktsioon on saadaval ainult Tier 2+ keskkondades, milleks on on Liivakasti ja tootmine.</span><span class="sxs-lookup"><span data-stu-id="b393e-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="b393e-129">Nende täiustatud kulude võimaluste kasutamiseks installige Microsoft Dynamics 365 Finance'i jaoks kuluhaldusteenuse lisandmoodul ja lülitage sisse oma eksemplari funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="b393e-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="b393e-130">Lisandmoodulile pääsete ligi oma projektist teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu.</span><span class="sxs-lookup"><span data-stu-id="b393e-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="b393e-131">Logige LCS-i sisse ja avage soovitud keskkond.</span><span class="sxs-lookup"><span data-stu-id="b393e-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="b393e-132">Minge jaotisse **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="b393e-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="b393e-133">Valige käsk **Säilita** või Kerige alla kiirkaardile **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="b393e-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="b393e-134">Valige käsk **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="b393e-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="b393e-135">Valige jaotis **Kuluhaldusteenus**.</span><span class="sxs-lookup"><span data-stu-id="b393e-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="b393e-136">Järgige installiviisardi juhiseid ja nõustuge tingimustega.</span><span class="sxs-lookup"><span data-stu-id="b393e-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="b393e-137">Valige käsk **Installi**.</span><span class="sxs-lookup"><span data-stu-id="b393e-137">Select **Install**.</span></span>

<span data-ttu-id="b393e-138">Lülitage välja tööruumis **Funktsioonide haldus** sisse järgmised funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="b393e-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="b393e-139">Ümberkujundatud kuluaruanded</span><span class="sxs-lookup"><span data-stu-id="b393e-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="b393e-140">Automaatne vastendamine ja kviitungist kulu loomine</span><span class="sxs-lookup"><span data-stu-id="b393e-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="b393e-141">Nende funktsioonide sisselülitamisel tehakse järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="b393e-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="b393e-142">Olemasolev tööruum **Kuluhaldus** asendatakse uue tööruumiga.</span><span class="sxs-lookup"><span data-stu-id="b393e-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="b393e-143">Lisatakse uus menüü element kulu välja nähtavuse kohta.</span><span class="sxs-lookup"><span data-stu-id="b393e-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="b393e-144">Saate siiski avada eelmise lehe **Kuluaruanded**, avades jaotise **Kuluhaldus > Minu kulud > Kuluaruanded**.</span><span class="sxs-lookup"><span data-stu-id="b393e-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="b393e-145">Töövood ja kõik kinnitused viivad teid ikka olemasolevate kuluaruannete lehele.</span><span class="sxs-lookup"><span data-stu-id="b393e-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="b393e-146">Kviitungeid töödeldakse Microsoft Azure Cognitive Services'i kaudu ja metaandmed eraldatakse ning lisatakse.</span><span class="sxs-lookup"><span data-stu-id="b393e-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="b393e-147">Lisatakse suvand, mis võimaldab luua kuluaruande, mis sisaldab vastendatud kinnitamata kviitungeid.</span><span class="sxs-lookup"><span data-stu-id="b393e-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="b393e-148">Suvand, mis lisatakse kuluaruannetesse, võimaldab teil luua kviitungi põhjal kulurea või üritab vastendada olemasoleva kviitungi olemasoleva kulureaga.</span><span class="sxs-lookup"><span data-stu-id="b393e-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="b393e-149">Lisateavet kuluaruannete ümberkujundamise funktsiooni kohta leiate teemast [Kuluaruannete ümberkujundamine](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="b393e-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="b393e-150">Korduma kippuvad küsimused</span><span class="sxs-lookup"><span data-stu-id="b393e-150">Frequently asked questions</span></span>

<span data-ttu-id="b393e-151">**Kas Microsoft kasutab oma mudelite jaoks minu andmeid?**</span><span class="sxs-lookup"><span data-stu-id="b393e-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="b393e-152">Ei, Microsoft on oma kviitungite töötlemise teenuse jaoks loonud üldise masinõppe mudeli.</span><span class="sxs-lookup"><span data-stu-id="b393e-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="b393e-153">See mudel ei põhine teie üleslaetud kviitungitel.</span><span class="sxs-lookup"><span data-stu-id="b393e-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="b393e-154">**Kus see funktsioon on saadaval ja töödeldud?**</span><span class="sxs-lookup"><span data-stu-id="b393e-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="b393e-155">Praegu toetatakse seda Ameerika Ühendriikides.</span><span class="sxs-lookup"><span data-stu-id="b393e-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="b393e-156">**Kuhu minu kviitungid lähevad?**</span><span class="sxs-lookup"><span data-stu-id="b393e-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="b393e-157">Finance kontakteerub rakendusega Cognitive Services, et eraldada väljade andmeid.</span><span class="sxs-lookup"><span data-stu-id="b393e-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="b393e-158">Rakendus Cognitive Services säilitab töötlemisel teie kviitungi koopiat kuni 24ks tunniks.</span><span class="sxs-lookup"><span data-stu-id="b393e-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="b393e-159">Pärast töötlemise lõpuleviimist eemaldab Cognitive Services kviitungi.</span><span class="sxs-lookup"><span data-stu-id="b393e-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="b393e-160">Kviitungid talletatakse endiselt rakenduses Finance.</span><span class="sxs-lookup"><span data-stu-id="b393e-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="b393e-161">Lisateavet leiate teemast [Kviitungite mõitsmise lubamine vormituvastaja uue võimalusega](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="b393e-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]