---
title: Project Operationsi konfiguratsiooniandmete seadistamine rakendamine rakenduses Common Data Service
description: Selles teemas kirjeldatakse konfiguratsiooni andmete seadistamist ja rakendamist Project Operationsis.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074829"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="e635d-103">Project Operationsi konfiguratsiooniandmete seadistamine rakendamine rakenduses Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e635d-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="e635d-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="e635d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="e635d-105">Seadistuse ja konfiguratsiooniandmete installimine</span><span class="sxs-lookup"><span data-stu-id="e635d-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="e635d-106">Laadige alla, avage ja pakkige lahti [Seadistuse ja konfiguratsiooni andmepakett](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="e635d-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="e635d-107">Liikuge lahtipakitud kausta ja käivitage käivitatav fail *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="e635d-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="e635d-108">Valige Common Data Service'i konfiguratsiooni migreerimise viisardi (CMT) 1. lehel käsk **Impordi andmed** ja seejärel valige **Jätka**.</span><span class="sxs-lookup"><span data-stu-id="e635d-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfiguratsiooni migreerimine](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="e635d-110">Valige CMT viisardi lehel 2 **juurutuse tüübiks** **Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="e635d-110">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="e635d-111">Valige märkeruudud **Saadaolevate asutuste loendi kuvamine** ja **Kuva täpsemad**.</span><span class="sxs-lookup"><span data-stu-id="e635d-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="e635d-112">Valige oma rentniku piirkond, sisestage oma mandaat ja valige **Logi sisse**.</span><span class="sxs-lookup"><span data-stu-id="e635d-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfiguratsioon Sisselogimine](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="e635d-114">Valige 3. lehel rentniku organisatsioonide loendist see organisatsioon, kuhu soovite demo andmed importida ja valige **Logi sisse**.</span><span class="sxs-lookup"><span data-stu-id="e635d-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="e635d-115">Valige lahtipakitud kaustast leheküljel 4 zip fail *SampleSetupAndConfigData*.</span><span class="sxs-lookup"><span data-stu-id="e635d-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![ZIP-faili valimine](./media/3ZipFile.png)

![Faili valimine](./media/4SelectAFile.png)

9. <span data-ttu-id="e635d-118">Pärast ZIP-faili valimist valige käsk **Impordi andmed**.</span><span class="sxs-lookup"><span data-stu-id="e635d-118">After the zip file is selected, select **Import Data**.</span></span>

![Impordi andmed](./media/5ImportData.png)

10. <span data-ttu-id="e635d-120">Importimine töötab umbes kaks kuni kümme minutit, olenevalt teie võrguühenduse kiirusest.</span><span class="sxs-lookup"><span data-stu-id="e635d-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="e635d-121">Pärast importimise lõpuleviimist väljuge CMT-i viisardist.</span><span class="sxs-lookup"><span data-stu-id="e635d-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="e635d-122">Kontrollige organisatsioonist järgmise 19 olemi andmeid.</span><span class="sxs-lookup"><span data-stu-id="e635d-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="e635d-123">Valuuta</span><span class="sxs-lookup"><span data-stu-id="e635d-123">Currency</span></span>
  - <span data-ttu-id="e635d-124">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="e635d-124">Organizational Unit</span></span>
  - <span data-ttu-id="e635d-125">Kontakt</span><span class="sxs-lookup"><span data-stu-id="e635d-125">Contact</span></span>
  - <span data-ttu-id="e635d-126">Maksurühm</span><span class="sxs-lookup"><span data-stu-id="e635d-126">Tax Group</span></span>
  - <span data-ttu-id="e635d-127">Kliendirühm</span><span class="sxs-lookup"><span data-stu-id="e635d-127">Customer Group</span></span>
  - <span data-ttu-id="e635d-128">Üksus</span><span class="sxs-lookup"><span data-stu-id="e635d-128">Unit</span></span>
  - <span data-ttu-id="e635d-129">Ühikurühm</span><span class="sxs-lookup"><span data-stu-id="e635d-129">Unit Group</span></span>
  - <span data-ttu-id="e635d-130">Hinnakiri</span><span class="sxs-lookup"><span data-stu-id="e635d-130">Price List</span></span>
  - <span data-ttu-id="e635d-131">Projekti parameetrite hinnakiri</span><span class="sxs-lookup"><span data-stu-id="e635d-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="e635d-132">Arve sagedus</span><span class="sxs-lookup"><span data-stu-id="e635d-132">Invoice Frequency</span></span>
  - <span data-ttu-id="e635d-133">Reserveeritava ressursi kategooria</span><span class="sxs-lookup"><span data-stu-id="e635d-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="e635d-134">Kande kategooria</span><span class="sxs-lookup"><span data-stu-id="e635d-134">Transaction Category</span></span>
  - <span data-ttu-id="e635d-135">Kulukategooria</span><span class="sxs-lookup"><span data-stu-id="e635d-135">Expense Category</span></span>
  - <span data-ttu-id="e635d-136">Rolli hind</span><span class="sxs-lookup"><span data-stu-id="e635d-136">Role Price</span></span>
  - <span data-ttu-id="e635d-137">Kandekategooria hind</span><span class="sxs-lookup"><span data-stu-id="e635d-137">Transaction Category Price</span></span>
  - <span data-ttu-id="e635d-138">Tunnus</span><span class="sxs-lookup"><span data-stu-id="e635d-138">Characteristic</span></span>
  - <span data-ttu-id="e635d-139">Broneeritav ressurss</span><span class="sxs-lookup"><span data-stu-id="e635d-139">Bookable Resource</span></span>
  - <span data-ttu-id="e635d-140">Broneeritava ressursi kategooria seos</span><span class="sxs-lookup"><span data-stu-id="e635d-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="e635d-141">Reserveeritava ressursi tunnus</span><span class="sxs-lookup"><span data-stu-id="e635d-141">Bookable Resource Characteristic</span></span>

![Lõpetage importimine](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="e635d-143">Värskendage Project Operationsi konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="e635d-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="e635d-144">Liikuge CE keskkonda.</span><span class="sxs-lookup"><span data-stu-id="e635d-144">Navigate to the CE environment.</span></span> <span data-ttu-id="e635d-145">Selle leiate, kui avate [Power Platformi halduskeskuse](https://admin.powerplatform.microsoft.com/environments), valides keskkonna ja seejärel valides suvandi **Avatud keskkond**.</span><span class="sxs-lookup"><span data-stu-id="e635d-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Avatud keskkond](./media/7OpenEnvironment.png)

2. <span data-ttu-id="e635d-147">Oma kasutajale broneeritava ressursi loomiseks minge jaotisse **Projektid** > **Ressursid** ja valige seejärel **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e635d-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Reserveeritavad ressursid](./media/8BookableResources.png)

3. <span data-ttu-id="e635d-149">Valige administraator vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="e635d-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="e635d-150">Kontrollige, kas ajavöönd vastab teie asukohale.</span><span class="sxs-lookup"><span data-stu-id="e635d-150">Verify that the time zone matches the one you are in.</span></span> 

![Uus broneeritav ressurss](./media/9NewBookableResource.png)

4. <span data-ttu-id="e635d-152">Valige vahekaardil **Kavandamine** väljal **Ettevõte** ettevõtteks **USPM** ja seejärel valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e635d-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Kavandamise vahekaart](./media/10SchedulingTab.png)

5. <span data-ttu-id="e635d-154">Valige vahekaart **Töötunnid**.</span><span class="sxs-lookup"><span data-stu-id="e635d-154">Select the **Work hours** tab.</span></span>  

![Tööaeg](./media/11WorkHours.png)

6. <span data-ttu-id="e635d-156">Topeltklõpsake kalendris mis tahes väärtust ja valige **Redigeeri** > **Kõik sarja sündmused**.</span><span class="sxs-lookup"><span data-stu-id="e635d-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Töökalender](./media/12WorkCalendar.png)

7. <span data-ttu-id="e635d-158">Muutke tööaega kaheksa (8) tunniseks tööpäevaks, märkige nädalavahetused mitte-tööpäevad ja veenduge, et ajavöönd vastab teie omale.</span><span class="sxs-lookup"><span data-stu-id="e635d-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="e635d-159">Valige **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="e635d-159">Select **Save and close**.</span></span>

![Kalendri värskendamine](./media/13UpdateCalendar.png)

9. <span data-ttu-id="e635d-161">Minge jaotisse **Sätted** > **Kalendri mallid** ja valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e635d-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendri mallid](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="e635d-163">Sisestage nimi, valige loodud malli ressurss ja seejärel valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e635d-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Kalendri malli salvestamine](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="e635d-165">Minge jaotisse **Parameetrid** ja topeltklõpsake kirjel.</span><span class="sxs-lookup"><span data-stu-id="e635d-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projekti parameetrid](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="e635d-167">Värskendage järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="e635d-167">Update the following fields:</span></span>

 - <span data-ttu-id="e635d-168">**Vaikeettevõte** : USPM</span><span class="sxs-lookup"><span data-stu-id="e635d-168">**Default company** : USPM</span></span>
 - <span data-ttu-id="e635d-169">**Vaike-organisatsiooniüksus** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="e635d-169">**Default Organizational Unit** : Contoso Robotics Global</span></span>
 - <span data-ttu-id="e635d-170">**Arve sagedus** : seitsmes ja viimane päev</span><span class="sxs-lookup"><span data-stu-id="e635d-170">**Invoice Frequency** : Seventh and Last day</span></span>
 - <span data-ttu-id="e635d-171">**Tööaja mall** : muutke loodud malliks.</span><span class="sxs-lookup"><span data-stu-id="e635d-171">**Work hour template** : Change to the template you created.</span></span>

13. <span data-ttu-id="e635d-172">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e635d-172">Select **Save**.</span></span> 

![Värskendatud projekti parameetrid](./media/17UpdatedProjectParameters.png)
