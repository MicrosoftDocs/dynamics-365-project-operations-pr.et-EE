---
title: Demoseadistamise ja konfiguratsiooniandmete rakendamine – liht
description: Selles teemas kirjeldatakse, kuidas rakendada demoseadistamist ja konfiguratsiooni andmeid Project Operationsis.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401258"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="7cc5c-103">Project Operationsi demoseadistamise ja konfiguratsiooniandmete rakendamine – liht</span><span class="sxs-lookup"><span data-stu-id="7cc5c-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="7cc5c-104">_\*\*Lite’i juurutamine – tehing näidisarveldusele_</span><span class="sxs-lookup"><span data-stu-id="7cc5c-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7cc5c-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="7cc5c-105">Prerequisites</span></span>

<span data-ttu-id="7cc5c-106">Enne konfigureerimise alustamist peab teil olema teenuse Common Data Service (CDS) keskkond rakenduse Dynamics 365 Project Operations jaoks ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="7cc5c-107">Juhised</span><span class="sxs-lookup"><span data-stu-id="7cc5c-107">Instructions</span></span>

1. <span data-ttu-id="7cc5c-108">Laadige alla [Master Data pakett](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="7cc5c-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="7cc5c-109">Liikuge kausta *ProjOpsDemoDataSetupAndMaster – integreeritud CMT* ja käitage käivitatav fail *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="7cc5c-110">Valige Common Data Service'i konfiguratsiooni migreerimise viisardi (CMT) 1. lehel käsk **Impordi andmed** ja seejärel valige **Jätka**.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfiguratsiooni migreerimine](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="7cc5c-112">Valige CMT viisardi lehel 2 **juurutuse tüübiks** **Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="7cc5c-113">Valige märkeruudud **Saadaolevate asutuste loendi kuvamine** ja **Kuva täpsemad**.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="7cc5c-114">Valige oma rentniku piirkond, sisestage oma mandaat ja valige seejärel **Logi sisse**.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Konfiguratsioon Sisselogimine](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="7cc5c-116">Valige 3. lehel rentniku organisatsioonide loendist organisatsioon, kuhu soovite demo andmed importida ja valige seejärel **Logi sisse**.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="7cc5c-117">Valige lahtipakitud kaustast leheküljel 4 zip fail *MasterAndSetupData*, *ProjOpsDemoDataSetupAndMaster – integreeritud CMT*.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip-fail](./media/3ZipFile.png)

![Faili valimine](./media/4SelectAFile.png)

9. <span data-ttu-id="7cc5c-120">Pärast ZIP-faili valimist valige käsk **Impordi andmed**.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-120">After the zip file is selected, select **Import Data**.</span></span>

![Importimise andmed](./media/5ImportData.png)

10. <span data-ttu-id="7cc5c-122">Importimine töötab umbes kaks kuni kümme minutit, olenevalt teie võrguühenduse kiirusest.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="7cc5c-123">Pärast selle lõpuleviimist väljuge CMT-i viisardist.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="7cc5c-124">Kontrollige organisatsioonist järgmise 20 olemi andmeid.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="7cc5c-125">Valuuta</span><span class="sxs-lookup"><span data-stu-id="7cc5c-125">Currency</span></span>
-   <span data-ttu-id="7cc5c-126">Ettevõte</span><span class="sxs-lookup"><span data-stu-id="7cc5c-126">Account</span></span>
-   <span data-ttu-id="7cc5c-127">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="7cc5c-127">Organizational Unit</span></span>
-   <span data-ttu-id="7cc5c-128">Kontakt</span><span class="sxs-lookup"><span data-stu-id="7cc5c-128">Contact</span></span>
-   <span data-ttu-id="7cc5c-129">Maksurühm</span><span class="sxs-lookup"><span data-stu-id="7cc5c-129">Tax Group</span></span>
-   <span data-ttu-id="7cc5c-130">Kliendirühm</span><span class="sxs-lookup"><span data-stu-id="7cc5c-130">Customer Group</span></span>
-   <span data-ttu-id="7cc5c-131">Üksus</span><span class="sxs-lookup"><span data-stu-id="7cc5c-131">Unit</span></span>
-   <span data-ttu-id="7cc5c-132">Ühikurühm</span><span class="sxs-lookup"><span data-stu-id="7cc5c-132">Unit Group</span></span>
-   <span data-ttu-id="7cc5c-133">Hinnakiri</span><span class="sxs-lookup"><span data-stu-id="7cc5c-133">Price List</span></span>
-   <span data-ttu-id="7cc5c-134">Projekti parameetrite hinnakiri</span><span class="sxs-lookup"><span data-stu-id="7cc5c-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="7cc5c-135">Arve sagedus</span><span class="sxs-lookup"><span data-stu-id="7cc5c-135">Invoice Frequency</span></span>
-   <span data-ttu-id="7cc5c-136">Reserveeritava ressursi kategooria</span><span class="sxs-lookup"><span data-stu-id="7cc5c-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="7cc5c-137">Kande kategooria</span><span class="sxs-lookup"><span data-stu-id="7cc5c-137">Transaction Category</span></span>
-   <span data-ttu-id="7cc5c-138">Kulukategooria</span><span class="sxs-lookup"><span data-stu-id="7cc5c-138">Expense Category</span></span>
-   <span data-ttu-id="7cc5c-139">Rolli hind</span><span class="sxs-lookup"><span data-stu-id="7cc5c-139">Role Price</span></span>
-   <span data-ttu-id="7cc5c-140">Kandekategooria hind</span><span class="sxs-lookup"><span data-stu-id="7cc5c-140">Transaction Category Price</span></span>
-   <span data-ttu-id="7cc5c-141">Tunnus</span><span class="sxs-lookup"><span data-stu-id="7cc5c-141">Characteristic</span></span>
-   <span data-ttu-id="7cc5c-142">Broneeritav ressurss</span><span class="sxs-lookup"><span data-stu-id="7cc5c-142">Bookable Resource</span></span>
-   <span data-ttu-id="7cc5c-143">Broneeritava ressursi kategooria seos</span><span class="sxs-lookup"><span data-stu-id="7cc5c-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="7cc5c-144">Reserveeritava ressursi tunnus</span><span class="sxs-lookup"><span data-stu-id="7cc5c-144">Bookable Resource Characteristic</span></span>

![Lõpetage importimine](./media/6CompleteImport.png)
