---
title: Konfiguratsiooniandmete häälestamine ja rakendamine teenuses Common Data Service
description: Selles teemas kirjeldatakse konfiguratsiooni andmete seadistamist ja rakendamist Project Operationsis.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1651d3b3b85d3dc581bf61976fada249bafd6b7b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289814"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="c5242-103">Konfiguratsiooniandmete häälestamine ja rakendamine teenuses Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c5242-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="c5242-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="c5242-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="c5242-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="c5242-105">Prerequisites</span></span>

<span data-ttu-id="c5242-106">Enne teenuses Common Data Service (CDS) andmete konfigureermise alustamist tuleb täita järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="c5242-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="c5242-107">Valmistage CDS-i keskkond ja rakenduse Dynamics 365 Finance keskkond Project Operationsi jaoks ette.</span><span class="sxs-lookup"><span data-stu-id="c5242-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="c5242-108">Rakenduse Dynamics 365 Finance juriidilise olemi teavet jagatakse CDS-i keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="c5242-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="c5242-109">See tähendab, et CDS-i olemil **Ettevõte** on järgmised ettevõtte kirjed.</span><span class="sxs-lookup"><span data-stu-id="c5242-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="c5242-110">THPM</span><span class="sxs-lookup"><span data-stu-id="c5242-110">THPM</span></span>
  - <span data-ttu-id="c5242-111">USPM</span><span class="sxs-lookup"><span data-stu-id="c5242-111">USPM</span></span>
  - <span data-ttu-id="c5242-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="c5242-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="c5242-113">Seadistuse ja konfiguratsiooniandmete installimine</span><span class="sxs-lookup"><span data-stu-id="c5242-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="c5242-114">Laadige alla, avage ja pakkige lahti [Seadistuse ja konfiguratsiooni andmepakett](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="c5242-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="c5242-115">Liikuge lahtipakitud kausta ja käivitage käivitatav fail *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="c5242-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="c5242-116">Valige Common Data Service'i konfiguratsiooni migreerimise viisardi (CMT) 1. lehel käsk **Impordi andmed** ja seejärel valige **Jätka**.</span><span class="sxs-lookup"><span data-stu-id="c5242-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfiguratsiooni migreerimine](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="c5242-118">Valige CMT viisardi lehel 2 **juurutuse tüübiks** **Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="c5242-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="c5242-119">Valige märkeruudud **Saadaolevate asutuste loendi kuvamine** ja **Kuva täpsemad**.</span><span class="sxs-lookup"><span data-stu-id="c5242-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="c5242-120">Valige oma rentniku piirkond, sisestage oma mandaat ja valige **Logi sisse**.</span><span class="sxs-lookup"><span data-stu-id="c5242-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfiguratsioon Sisselogimine](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="c5242-122">Valige 3. lehel rentniku organisatsioonide loendist see organisatsioon, kuhu soovite demo andmed importida ja valige **Logi sisse**.</span><span class="sxs-lookup"><span data-stu-id="c5242-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="c5242-123">Valige lahtipakitud kaustast leheküljel 4 zip fail *SampleSetupAndConfigData*.</span><span class="sxs-lookup"><span data-stu-id="c5242-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![ZIP-faili valimine](./media/3ZipFile.png)

![Faili valimine](./media/4SelectAFile.png)

9. <span data-ttu-id="c5242-126">Pärast ZIP-faili valimist valige käsk **Impordi andmed**.</span><span class="sxs-lookup"><span data-stu-id="c5242-126">After the zip file is selected, select **Import Data**.</span></span>

![Impordi andmed](./media/5ImportData.png)

10. <span data-ttu-id="c5242-128">Importimine töötab umbes kaks kuni kümme minutit, olenevalt teie võrguühenduse kiirusest.</span><span class="sxs-lookup"><span data-stu-id="c5242-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="c5242-129">Pärast importimise lõpuleviimist väljuge CMT-i viisardist.</span><span class="sxs-lookup"><span data-stu-id="c5242-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="c5242-130">Kontrollige organisatsioonist järgmise 19 olemi andmeid.</span><span class="sxs-lookup"><span data-stu-id="c5242-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="c5242-131">Valuuta</span><span class="sxs-lookup"><span data-stu-id="c5242-131">Currency</span></span>
  - <span data-ttu-id="c5242-132">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="c5242-132">Organizational Unit</span></span>
  - <span data-ttu-id="c5242-133">Kontakt</span><span class="sxs-lookup"><span data-stu-id="c5242-133">Contact</span></span>
  - <span data-ttu-id="c5242-134">Maksurühm</span><span class="sxs-lookup"><span data-stu-id="c5242-134">Tax Group</span></span>
  - <span data-ttu-id="c5242-135">Kliendirühm</span><span class="sxs-lookup"><span data-stu-id="c5242-135">Customer Group</span></span>
  - <span data-ttu-id="c5242-136">Üksus</span><span class="sxs-lookup"><span data-stu-id="c5242-136">Unit</span></span>
  - <span data-ttu-id="c5242-137">Ühikurühm</span><span class="sxs-lookup"><span data-stu-id="c5242-137">Unit Group</span></span>
  - <span data-ttu-id="c5242-138">Hinnakiri</span><span class="sxs-lookup"><span data-stu-id="c5242-138">Price List</span></span>
  - <span data-ttu-id="c5242-139">Projekti parameetrite hinnakiri</span><span class="sxs-lookup"><span data-stu-id="c5242-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="c5242-140">Arve sagedus</span><span class="sxs-lookup"><span data-stu-id="c5242-140">Invoice Frequency</span></span>
  - <span data-ttu-id="c5242-141">Reserveeritava ressursi kategooria</span><span class="sxs-lookup"><span data-stu-id="c5242-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="c5242-142">Kande kategooria</span><span class="sxs-lookup"><span data-stu-id="c5242-142">Transaction Category</span></span>
  - <span data-ttu-id="c5242-143">Kulukategooria</span><span class="sxs-lookup"><span data-stu-id="c5242-143">Expense Category</span></span>
  - <span data-ttu-id="c5242-144">Rolli hind</span><span class="sxs-lookup"><span data-stu-id="c5242-144">Role Price</span></span>
  - <span data-ttu-id="c5242-145">Kandekategooria hind</span><span class="sxs-lookup"><span data-stu-id="c5242-145">Transaction Category Price</span></span>
  - <span data-ttu-id="c5242-146">Tunnus</span><span class="sxs-lookup"><span data-stu-id="c5242-146">Characteristic</span></span>
  - <span data-ttu-id="c5242-147">Broneeritav ressurss</span><span class="sxs-lookup"><span data-stu-id="c5242-147">Bookable Resource</span></span>
  - <span data-ttu-id="c5242-148">Broneeritava ressursi kategooria seos</span><span class="sxs-lookup"><span data-stu-id="c5242-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="c5242-149">Reserveeritava ressursi tunnus</span><span class="sxs-lookup"><span data-stu-id="c5242-149">Bookable Resource Characteristic</span></span>

![Lõpetage importimine](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="c5242-151">Värskendage Project Operationsi konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="c5242-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="c5242-152">Liikuge CE keskkonda.</span><span class="sxs-lookup"><span data-stu-id="c5242-152">Navigate to the CE environment.</span></span> <span data-ttu-id="c5242-153">Selle leiate, kui avate [Power Platformi halduskeskuse](https://admin.powerplatform.microsoft.com/environments), valides keskkonna ja seejärel valides suvandi **Avatud keskkond**.</span><span class="sxs-lookup"><span data-stu-id="c5242-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Avatud keskkond](./media/7OpenEnvironment.png)

2. <span data-ttu-id="c5242-155">Oma kasutajale broneeritava ressursi loomiseks minge jaotisse **Projektid** > **Ressursid** ja valige seejärel **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c5242-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Reserveeritavad ressursid](./media/8BookableResources.png)

3. <span data-ttu-id="c5242-157">Valige administraator vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="c5242-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="c5242-158">Kontrollige, kas ajavöönd vastab teie asukohale.</span><span class="sxs-lookup"><span data-stu-id="c5242-158">Verify that the time zone matches the one you are in.</span></span> 

![Uus broneeritav ressurss](./media/9NewBookableResource.png)

4. <span data-ttu-id="c5242-160">Valige vahekaardil **Kavandamine** väljal **Ettevõte** ettevõtteks **USPM** ja seejärel valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c5242-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Kavandamise vahekaart](./media/10SchedulingTab.png)

5. <span data-ttu-id="c5242-162">Valige vahekaart **Töötunnid**.</span><span class="sxs-lookup"><span data-stu-id="c5242-162">Select the **Work hours** tab.</span></span>  

![Tööaeg](./media/11WorkHours.png)

6. <span data-ttu-id="c5242-164">Topeltklõpsake kalendris mis tahes väärtust ja valige **Redigeeri** > **Kõik sarja sündmused**.</span><span class="sxs-lookup"><span data-stu-id="c5242-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Töökalender](./media/12WorkCalendar.png)

7. <span data-ttu-id="c5242-166">Muutke tööaega kaheksa (8) tunniseks tööpäevaks, märkige nädalavahetused mitte-tööpäevad ja veenduge, et ajavöönd vastab teie omale.</span><span class="sxs-lookup"><span data-stu-id="c5242-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="c5242-167">Valige **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="c5242-167">Select **Save and close**.</span></span>

![Kalendri värskendamine](./media/13UpdateCalendar.png)

9. <span data-ttu-id="c5242-169">Minge jaotisse **Sätted** > **Kalendri mallid** ja valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c5242-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendri mallid](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="c5242-171">Sisestage nimi, valige loodud malli ressurss ja seejärel valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c5242-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Kalendri malli salvestamine](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="c5242-173">Minge jaotisse **Parameetrid** ja topeltklõpsake kirjel.</span><span class="sxs-lookup"><span data-stu-id="c5242-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projekti parameetrid](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="c5242-175">Värskendage järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="c5242-175">Update the following fields:</span></span>

 - <span data-ttu-id="c5242-176">**Vaikeettevõte**: USPM</span><span class="sxs-lookup"><span data-stu-id="c5242-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="c5242-177">**Vaike-organisatsiooniüksus**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="c5242-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="c5242-178">**Arve sagedus**: seitsmes ja viimane päev</span><span class="sxs-lookup"><span data-stu-id="c5242-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="c5242-179">**Tööaja mall**: muutke loodud malliks.</span><span class="sxs-lookup"><span data-stu-id="c5242-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="c5242-180">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c5242-180">Select **Save**.</span></span> 

![Värskendatud projekti parameetrid](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]