---
title: Konfiguratsiooniandmete häälestamine ja rakendamine teenuses Common Data Service
description: Selles teemas kirjeldatakse konfiguratsiooni andmete seadistamist ja rakendamist Project Operationsis.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001286"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="a0468-103">Konfiguratsiooniandmete häälestamine ja rakendamine teenuses Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a0468-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="a0468-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="a0468-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="a0468-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="a0468-105">Prerequisites</span></span>

<span data-ttu-id="a0468-106">Enne andmete teenuses Common Data Service (CDS) konfigureerimise alustamist peavad olema täidetud järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="a0468-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="a0468-107">Valmistage CDS-i keskkond ja rakenduse Dynamics 365 Finance keskkond Project Operationsi jaoks ette.</span><span class="sxs-lookup"><span data-stu-id="a0468-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="a0468-108">Rakenduse Dynamics 365 Finance juriidilise olemi teavet jagatakse CDS-i keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="a0468-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="a0468-109">See tähendab, et CDS-i olemil **Ettevõte** on järgmised ettevõtte kirjed.</span><span class="sxs-lookup"><span data-stu-id="a0468-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="a0468-110">THPM</span><span class="sxs-lookup"><span data-stu-id="a0468-110">THPM</span></span>
  - <span data-ttu-id="a0468-111">USPM</span><span class="sxs-lookup"><span data-stu-id="a0468-111">USPM</span></span>
  - <span data-ttu-id="a0468-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="a0468-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="a0468-113">Seadistuse ja konfiguratsiooniandmete installimine</span><span class="sxs-lookup"><span data-stu-id="a0468-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="a0468-114">Laadige alla, avage ja pakkige lahti [Seadistuse ja konfiguratsiooni andmepakett](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="a0468-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="a0468-115">Liikuge lahtipakitud kausta ja käivitage käivitatav fail *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="a0468-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="a0468-116">Valige Common Data Service'i konfiguratsiooni migreerimise viisardi (CMT) 1. lehel käsk **Impordi andmed** ja seejärel valige **Jätka**.</span><span class="sxs-lookup"><span data-stu-id="a0468-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfiguratsiooni migreerimine](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="a0468-118">Valige CMT viisardi lehel 2 **juurutuse tüübiks** **Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="a0468-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="a0468-119">Valige märkeruudud **Saadaolevate asutuste loendi kuvamine** ja **Kuva täpsemad**.</span><span class="sxs-lookup"><span data-stu-id="a0468-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="a0468-120">Valige oma rentniku piirkond, sisestage oma mandaat ja valige **Logi sisse**.</span><span class="sxs-lookup"><span data-stu-id="a0468-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfiguratsioon Sisselogimine](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="a0468-122">Valige 3. lehel rentniku organisatsioonide loendist see organisatsioon, kuhu soovite demo andmed importida ja valige **Logi sisse**.</span><span class="sxs-lookup"><span data-stu-id="a0468-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="a0468-123">Valige lahtipakitud kaustast leheküljel 4 zip fail *SampleSetupAndConfigData*.</span><span class="sxs-lookup"><span data-stu-id="a0468-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![ZIP-faili valimine](./media/3ZipFile.png)

![Faili valimine](./media/4SelectAFile.png)

9. <span data-ttu-id="a0468-126">Pärast ZIP-faili valimist valige käsk **Impordi andmed**.</span><span class="sxs-lookup"><span data-stu-id="a0468-126">After the zip file is selected, select **Import Data**.</span></span>

![Impordi andmed](./media/5ImportData.png)

10. <span data-ttu-id="a0468-128">Importimine töötab umbes kaks kuni kümme minutit, olenevalt teie võrguühenduse kiirusest.</span><span class="sxs-lookup"><span data-stu-id="a0468-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="a0468-129">Pärast importimise lõpuleviimist väljuge CMT-i viisardist.</span><span class="sxs-lookup"><span data-stu-id="a0468-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="a0468-130">Kontrollige organisatsioonist järgmise 26 olemi andmeid.</span><span class="sxs-lookup"><span data-stu-id="a0468-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="a0468-131">Valuuta</span><span class="sxs-lookup"><span data-stu-id="a0468-131">Currency</span></span>
  - <span data-ttu-id="a0468-132">Kontoplaan</span><span class="sxs-lookup"><span data-stu-id="a0468-132">Chart of Accounts</span></span>
  - <span data-ttu-id="a0468-133">Finantskalender</span><span class="sxs-lookup"><span data-stu-id="a0468-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="a0468-134">Valuuta vahetuskursside tüübid</span><span class="sxs-lookup"><span data-stu-id="a0468-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="a0468-135">Maksmise päev</span><span class="sxs-lookup"><span data-stu-id="a0468-135">Payment Day</span></span>
  - <span data-ttu-id="a0468-136">Maksegraafik</span><span class="sxs-lookup"><span data-stu-id="a0468-136">Payment Schedule</span></span>
  - <span data-ttu-id="a0468-137">Maksetähtaeg</span><span class="sxs-lookup"><span data-stu-id="a0468-137">Payment Term</span></span>
  - <span data-ttu-id="a0468-138">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="a0468-138">Organizational Unit</span></span>
  - <span data-ttu-id="a0468-139">Kontaktandmed</span><span class="sxs-lookup"><span data-stu-id="a0468-139">Contact</span></span>
  - <span data-ttu-id="a0468-140">Maksurühm</span><span class="sxs-lookup"><span data-stu-id="a0468-140">Tax Group</span></span>
  - <span data-ttu-id="a0468-141">Kliendirühm</span><span class="sxs-lookup"><span data-stu-id="a0468-141">Customer Group</span></span>
  - <span data-ttu-id="a0468-142">Hankijate rühm</span><span class="sxs-lookup"><span data-stu-id="a0468-142">Vendor Group</span></span>
  - <span data-ttu-id="a0468-143">Üksus</span><span class="sxs-lookup"><span data-stu-id="a0468-143">Unit</span></span>
  - <span data-ttu-id="a0468-144">Ühikurühm</span><span class="sxs-lookup"><span data-stu-id="a0468-144">Unit Group</span></span>
  - <span data-ttu-id="a0468-145">Hinnakiri</span><span class="sxs-lookup"><span data-stu-id="a0468-145">Price List</span></span>
  - <span data-ttu-id="a0468-146">Projekti parameetrite hinnakiri</span><span class="sxs-lookup"><span data-stu-id="a0468-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="a0468-147">Arve sagedus</span><span class="sxs-lookup"><span data-stu-id="a0468-147">Invoice Frequency</span></span>
  - <span data-ttu-id="a0468-148">Reserveeritava ressursi kategooria</span><span class="sxs-lookup"><span data-stu-id="a0468-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="a0468-149">Kande kategooria</span><span class="sxs-lookup"><span data-stu-id="a0468-149">Transaction Category</span></span>
  - <span data-ttu-id="a0468-150">Kulukategooria</span><span class="sxs-lookup"><span data-stu-id="a0468-150">Expense Category</span></span>
  - <span data-ttu-id="a0468-151">Rolli hind</span><span class="sxs-lookup"><span data-stu-id="a0468-151">Role Price</span></span>
  - <span data-ttu-id="a0468-152">Kandekategooria hind</span><span class="sxs-lookup"><span data-stu-id="a0468-152">Transaction Category Price</span></span>
  - <span data-ttu-id="a0468-153">Tunnus</span><span class="sxs-lookup"><span data-stu-id="a0468-153">Characteristic</span></span>
  - <span data-ttu-id="a0468-154">Broneeritav ressurss</span><span class="sxs-lookup"><span data-stu-id="a0468-154">Bookable Resource</span></span>
  - <span data-ttu-id="a0468-155">Broneeritava ressursi kategooria seos</span><span class="sxs-lookup"><span data-stu-id="a0468-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="a0468-156">Reserveeritava ressursi tunnus</span><span class="sxs-lookup"><span data-stu-id="a0468-156">Bookable Resource Characteristic</span></span>

![Lõpetage importimine](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="a0468-158">Värskendage Project Operationsi konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="a0468-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="a0468-159">Liikuge CE keskkonda.</span><span class="sxs-lookup"><span data-stu-id="a0468-159">Navigate to the CE environment.</span></span> <span data-ttu-id="a0468-160">Selle leiate, kui avate [Power Platformi halduskeskuse](https://admin.powerplatform.microsoft.com/environments), valides keskkonna ja seejärel valides suvandi **Avatud keskkond**.</span><span class="sxs-lookup"><span data-stu-id="a0468-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Avatud keskkond](./media/7OpenEnvironment.png)

2. <span data-ttu-id="a0468-162">Oma kasutajale broneeritava ressursi loomiseks minge jaotisse **Projektid** > **Ressursid** ja valige seejärel **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a0468-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Reserveeritavad ressursid](./media/8BookableResources.png)

3. <span data-ttu-id="a0468-164">Valige administraator vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="a0468-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="a0468-165">Kontrollige, kas ajavöönd vastab teie asukohale.</span><span class="sxs-lookup"><span data-stu-id="a0468-165">Verify that the time zone matches the one you are in.</span></span> 

![Uus broneeritav ressurss](./media/9NewBookableResource.png)

4. <span data-ttu-id="a0468-167">Valige vahekaardil **Kavandamine** väljal **Ettevõte** ettevõtteks **USPM** ja seejärel valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a0468-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Kavandamise vahekaart](./media/10SchedulingTab.png)

5. <span data-ttu-id="a0468-169">Valige vahekaart **Töötunnid**.</span><span class="sxs-lookup"><span data-stu-id="a0468-169">Select the **Work hours** tab.</span></span>  

![Tööaeg](./media/11WorkHours.png)

6. <span data-ttu-id="a0468-171">Topeltklõpsake kalendris mis tahes väärtust ja valige **Redigeeri** > **Kõik sarja sündmused**.</span><span class="sxs-lookup"><span data-stu-id="a0468-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Töökalender](./media/12WorkCalendar.png)

7. <span data-ttu-id="a0468-173">Muutke tööaega kaheksa (8) tunniseks tööpäevaks, märkige nädalavahetused mitte-tööpäevad ja veenduge, et ajavöönd vastab teie omale.</span><span class="sxs-lookup"><span data-stu-id="a0468-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="a0468-174">Valige **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="a0468-174">Select **Save and close**.</span></span>

![Kalendri värskendamine](./media/13UpdateCalendar.png)

9. <span data-ttu-id="a0468-176">Minge jaotisse **Sätted** > **Kalendri mallid** ja valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a0468-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendri mallid](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="a0468-178">Sisestage nimi, valige loodud malli ressurss ja seejärel valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a0468-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Kalendri malli salvestamine](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="a0468-180">Minge jaotisse **Parameetrid** ja topeltklõpsake kirjel.</span><span class="sxs-lookup"><span data-stu-id="a0468-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projekti parameetrid](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="a0468-182">Värskendage järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="a0468-182">Update the following fields:</span></span>

 - <span data-ttu-id="a0468-183">**Vaikeettevõte**: USPM</span><span class="sxs-lookup"><span data-stu-id="a0468-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="a0468-184">**Organisatsiooni vaikeühik**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="a0468-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="a0468-185">**Arve sagedus**: seitsmes ja viimane päev</span><span class="sxs-lookup"><span data-stu-id="a0468-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="a0468-186">**Tööaja mall**: muutke loodud malliks.</span><span class="sxs-lookup"><span data-stu-id="a0468-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="a0468-187">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a0468-187">Select **Save**.</span></span> 

![Värskendatud projekti parameetrid](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
