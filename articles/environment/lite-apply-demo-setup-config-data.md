---
title: Demoseadistamise ja konfiguratsiooniandmete rakendamine
description: Selles teemas kirjeldatakse, kuidas rakendada demoseadistamist ja konfiguratsiooni andmeid Project Operationsis.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948827"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="2e0b7-103">Project Operations Lite’i juurutusele – tehing näidisarveldusele demoseadistamise või konfiguratsiooniandmete rakendamine</span><span class="sxs-lookup"><span data-stu-id="2e0b7-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="2e0b7-104">_\*\*Lite’i juurutamine – tehing näidisarveldusele_</span><span class="sxs-lookup"><span data-stu-id="2e0b7-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="2e0b7-105">Laadige alla [Master Data pakett](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="2e0b7-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="2e0b7-106">Liikuge kausta *ProjOpsDemoDataSetupAndMaster – integreeritud CMT* ja käitage käivitatav fail *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="2e0b7-107">Valige Common Data Service'i konfiguratsiooni migreerimise viisardi (CMT) 1. lehel käsk **Impordi andmed** ja seejärel valige **Jätka**.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfiguratsiooni migreerimine](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="2e0b7-109">Valige CMT viisardi lehel 2 **Office 365** **Juurutuse tüübiks**.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="2e0b7-110">Valige märkeruudud **Saadaolevate asutuste loendi kuvamine** ja **Kuva täpsemad**.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="2e0b7-111">Valige oma rentniku piirkond, sisestage oma mandaat ja valige seejärel **Logi sisse**.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Konfiguratsioon Sisselogimine](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="2e0b7-113">Valige 3. lehel rentniku organisatsioonide loendist organisatsioon, kuhu soovite demo andmed importida ja valige seejärel **Logi sisse**.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="2e0b7-114">Valige lahtipakitud kaustast leheküljel 4 zip fail *MasterAndSetupData*, *ProjOpsDemoDataSetupAndMaster – integreeritud CMT*.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip-fail](./media/3ZipFile.png)

![Faili valimine](./media/4SelectAFile.png)

9. <span data-ttu-id="2e0b7-117">Pärast ZIP-faili valimist valige käsk **Impordi andmed**.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-117">After the zip file is selected, select **Import Data**.</span></span>

![Importimise andmed](./media/5ImportData.png)

10. <span data-ttu-id="2e0b7-119">Importimine töötab umbes kaks kuni kümme minutit, olenevalt teie võrguühenduse kiirusest.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="2e0b7-120">Pärast selle lõpuleviimist väljuge CMT-i viisardist.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="2e0b7-121">Kontrollige organisatsioonist järgmise 20 olemi andmeid.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="2e0b7-122">Valuuta</span><span class="sxs-lookup"><span data-stu-id="2e0b7-122">Currency</span></span>
- <span data-ttu-id="2e0b7-123">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="2e0b7-123">Organizational Unit</span></span>
- <span data-ttu-id="2e0b7-124">Kontakt</span><span class="sxs-lookup"><span data-stu-id="2e0b7-124">Contact</span></span>
- <span data-ttu-id="2e0b7-125">Maksurühm</span><span class="sxs-lookup"><span data-stu-id="2e0b7-125">Tax Group</span></span>
- <span data-ttu-id="2e0b7-126">Kliendirühm</span><span class="sxs-lookup"><span data-stu-id="2e0b7-126">Customer Group</span></span>
- <span data-ttu-id="2e0b7-127">Üksus</span><span class="sxs-lookup"><span data-stu-id="2e0b7-127">Unit</span></span>
- <span data-ttu-id="2e0b7-128">Ühikurühm</span><span class="sxs-lookup"><span data-stu-id="2e0b7-128">Unit Group</span></span>
- <span data-ttu-id="2e0b7-129">Hinnakiri</span><span class="sxs-lookup"><span data-stu-id="2e0b7-129">Price List</span></span>
- <span data-ttu-id="2e0b7-130">Projekti parameetrite hinnakiri</span><span class="sxs-lookup"><span data-stu-id="2e0b7-130">Project Parameter Price List</span></span>
- <span data-ttu-id="2e0b7-131">Arve sagedus</span><span class="sxs-lookup"><span data-stu-id="2e0b7-131">Invoice Frequency</span></span>
- <span data-ttu-id="2e0b7-132">Arve sageduse üksikasjad</span><span class="sxs-lookup"><span data-stu-id="2e0b7-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="2e0b7-133">Reserveeritava ressursi kategooria</span><span class="sxs-lookup"><span data-stu-id="2e0b7-133">Bookable Resource Category</span></span>
- <span data-ttu-id="2e0b7-134">Kande kategooria</span><span class="sxs-lookup"><span data-stu-id="2e0b7-134">Transaction Category</span></span>
- <span data-ttu-id="2e0b7-135">Kulukategooria</span><span class="sxs-lookup"><span data-stu-id="2e0b7-135">Expense Category</span></span>
- <span data-ttu-id="2e0b7-136">Rolli hind</span><span class="sxs-lookup"><span data-stu-id="2e0b7-136">Role Price</span></span>
- <span data-ttu-id="2e0b7-137">Kandekategooria hind</span><span class="sxs-lookup"><span data-stu-id="2e0b7-137">Transaction Category Price</span></span>
- <span data-ttu-id="2e0b7-138">Tunnus</span><span class="sxs-lookup"><span data-stu-id="2e0b7-138">Characteristic</span></span>
- <span data-ttu-id="2e0b7-139">Broneeritav ressurss</span><span class="sxs-lookup"><span data-stu-id="2e0b7-139">Bookable Resource</span></span>
- <span data-ttu-id="2e0b7-140">Broneeritava ressursi kategooria seos</span><span class="sxs-lookup"><span data-stu-id="2e0b7-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="2e0b7-141">Reserveeritava ressursi tunnus</span><span class="sxs-lookup"><span data-stu-id="2e0b7-141">Bookable Resource Characteristic</span></span>

![Lõpetage importimine](./media/6CompleteImport.png)
