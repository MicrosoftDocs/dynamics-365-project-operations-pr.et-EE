---
title: Kinnitatud aja- ja kulukirjete loodud tegelike näitajate hulgiparandused
description: Selles teemas selgitatakse, kuidas administraator saab teha üksikuid või hulgiparandusi eelnevalt kinnitatud aja- või kulukirjetele, kui arveldus ei ole lõpetatud.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 17d6648840e27a4e573985af2cdd74c4adf878e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290894"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="1a22a-103">Kinnitatud aja- ja kulukirjete loodud tegelike näitajate hulgiparandused</span><span class="sxs-lookup"><span data-stu-id="1a22a-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1a22a-104">Mõnikord võib aja- või kulukirje olla valesti sisestatud.</span><span class="sxs-lookup"><span data-stu-id="1a22a-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="1a22a-105">Näiteks võib konsultant ajakirje loomisel valida vale kuupäev või kulu sisestades numbrite järjekorda muuta.</span><span class="sxs-lookup"><span data-stu-id="1a22a-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="1a22a-106">Kui konsultant ei saa esitatud kirjetele värskendusi teha, saab administraator projekti kirje otse ära parandada.</span><span class="sxs-lookup"><span data-stu-id="1a22a-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="1a22a-107">Selle teema toimingute lõpuleviimiseks on teil vaja administraatori õigusi.</span><span class="sxs-lookup"><span data-stu-id="1a22a-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="1a22a-108">Kinnitatud ajakirjete parandamine</span><span class="sxs-lookup"><span data-stu-id="1a22a-108">Correct approved time entries</span></span>     

<span data-ttu-id="1a22a-109">Projekti ühe või mitme ajakirje parandamiseks läbige järgmised sammud.</span><span class="sxs-lookup"><span data-stu-id="1a22a-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="1a22a-110">Valige alal **Müük** väärtus **Kanded** ja seejärel valige **Kinnitatud aeg**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="1a22a-111">Otsige ja valige loendist **Kinnitatud aeg** parandamiseks üks või rohkem kinnitatud ajakirjet.</span><span class="sxs-lookup"><span data-stu-id="1a22a-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="1a22a-112">Filtri abil saate otsida seostuvaid kirjeid.</span><span class="sxs-lookup"><span data-stu-id="1a22a-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="1a22a-113">Näiteks võite filtreerida projekti ID järgi ja valida kõik selle projekti ID-ga kinnitatud ajakirjed.</span><span class="sxs-lookup"><span data-stu-id="1a22a-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="1a22a-114">Valige **Kirjete parandamine**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-114">Select **Correct entries**.</span></span> <span data-ttu-id="1a22a-115">Luuakse automaatselt uus paranduse tööleht, millele on määratud tüüp **Aja parandus**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="1a22a-116">Teie valitud kirjed lisatakse töölehele.</span><span class="sxs-lookup"><span data-stu-id="1a22a-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="1a22a-117">Sisestage lehel **Uus tööleht** oma paranduste töölehele **Kirjeldus** ja seejärel valige vahekaart **Ajakirje parandused**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="1a22a-118">Värskendage jaotises **Ajakannete uued väärtused** väljad vajadusel õige teabega.</span><span class="sxs-lookup"><span data-stu-id="1a22a-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="1a22a-119">Näiteks saate muuta määratud projekti või reserveeritavat ressurssi.</span><span class="sxs-lookup"><span data-stu-id="1a22a-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="1a22a-120">Valige **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-120">Select **Preview**.</span></span> <span data-ttu-id="1a22a-121">Valkige dialoogiboksis **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="1a22a-122">Vahekaardil **Töölehe read** saate vaadata algsete tegelike näitajate loendit, mis on seotud valitud ajakannetega, mis on tagasipööratud, ja neile vastavate loodud parandatud ridadega.</span><span class="sxs-lookup"><span data-stu-id="1a22a-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="1a22a-123">Kui tuleb teha täiendavaid parandusi, korrake etappe 5 ja 6.</span><span class="sxs-lookup"><span data-stu-id="1a22a-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="1a22a-124">Kõik parandatud tegelikud väärtused on samad, mille valisite jaotises **Ajakannete uued väärtused**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="1a22a-125">Kui parandust kuvatakse nii nagu eeldati, valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="1a22a-126">Valkige dialoogiboksis **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="1a22a-127">Minge tagasi alasse **Müük**, valige **Projektid** ja seejärel avage projekt, mille ajakandeid te äsja uuendasite.</span><span class="sxs-lookup"><span data-stu-id="1a22a-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="1a22a-128">Vaadake tehtud muudatusi lehe **Projektid** vahekaardil **Tegelikud näitajad**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="1a22a-129">Kui vahekaart **Tegelikud näitajad** ei ole kuvatud, valige **Seostuvad** > **Tegelikud näitajad**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="1a22a-130">Loendis **Tegelik seostatud vaade** näete, et tagasipööratud algsed ajakanded on endiselt loetletud, nagu on ka vastavad parandatud ajakanded.</span><span class="sxs-lookup"><span data-stu-id="1a22a-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="1a22a-131">Näiteks on järgmisel joonisel kaks reaüksust kogustega 8.00, millel on summa veerus loetletud deebetid.</span><span class="sxs-lookup"><span data-stu-id="1a22a-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="1a22a-132">Lisaks on kaks reaüksust kogusega -8.00, mis näitavad summa veerus krediteeritud summasid.</span><span class="sxs-lookup"><span data-stu-id="1a22a-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="1a22a-133">Need parandused viivad koguse nulli.</span><span class="sxs-lookup"><span data-stu-id="1a22a-133">These corrections bring the quantity to zero.</span></span>

![Tegelik seostatud vaate loend](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="1a22a-135">Kinnitatud kulukirjete parandamine</span><span class="sxs-lookup"><span data-stu-id="1a22a-135">Correct approved expense entries</span></span>

<span data-ttu-id="1a22a-136">Ühe või rohkema kulukirje parandamiseks läbige järgmised etapid.</span><span class="sxs-lookup"><span data-stu-id="1a22a-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="1a22a-137">Valige alas **Müük** vasakpoolsel navigeerimispaanil jaotise **Tehingud** all **Kinnitatud kulud**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="1a22a-138">Valige loendis **Kinnitatud kulud** projekt, mida soovite parandada, ja seejärel valige **Kirjete parandamine**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="1a22a-139">Luuakse automaatselt uus paranduse tööleht, millele on määratud tüüp **Kulude parandus**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="1a22a-140">Sisestage lehel **Uus tööleht** parandusele **Kirjeldus** ja valige vahekaardi **Kulude parandus** jaotises **Kulude uued väärtused** need andmeväljad, mida soovite valitud kuluridade puhul parandada.</span><span class="sxs-lookup"><span data-stu-id="1a22a-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="1a22a-141">Näiteks saate määrata kulu teisele **Projektile** või parandada väärtusi **Kulu kategooria**, **Kulu kuupäeva** või **Reserveeritav ressurss**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="1a22a-142">Valige **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-142">Select **Preview**.</span></span> <span data-ttu-id="1a22a-143">Valkige dialoogiboksis **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="1a22a-144">Kinnitage parandused vahekaardil **Töölehe read**. Saate vaadata algsete tegelike näitajate loendit, mis on seotud valitud kulukirjetega, mis on tagasipööratud, ja neile vastavate loodud parandatud ridadega.</span><span class="sxs-lookup"><span data-stu-id="1a22a-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="1a22a-145">Kui parandatud väärtused on sellised nagu eeldati, valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="1a22a-146">Valkige dialoogiboksis **OK.**</span><span class="sxs-lookup"><span data-stu-id="1a22a-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="1a22a-147">Kui väärtused ei ole näidatud nii nagu eeldatud, valige **Tühista**, et naasta loendisse **Kinnitatud kulud**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="1a22a-148">Korrake toiminguid 2 kuni 5.</span><span class="sxs-lookup"><span data-stu-id="1a22a-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="1a22a-149">Parandatud tegelikud väärtused on samad, mille valisite jaotises **Kulude uued väärtused**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="1a22a-150">Pärast paranduste töölehe kinnitamist minge tagasi värskendatud projekti või projektide juurde, et saaksite oma muudatusi vaadata.</span><span class="sxs-lookup"><span data-stu-id="1a22a-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="1a22a-151">Vaadake projekti lehe vahekaardil **Tegelikud näitajad** välja **Tegelik seostatud vaade**.</span><span class="sxs-lookup"><span data-stu-id="1a22a-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="1a22a-152">Loetletud on algsed kirjed ja parandatud kirjed.</span><span class="sxs-lookup"><span data-stu-id="1a22a-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="1a22a-153">Järgmisel joonisel on kuvatud algsed kulukirje summad ja vastavad parandatud kulukirje summad.</span><span class="sxs-lookup"><span data-stu-id="1a22a-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Kulute tegelikud näitajad](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]