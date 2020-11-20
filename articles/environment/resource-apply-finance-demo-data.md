---
title: Demoandmete rakendamine rakenduse Finance pilvepõhises keskkonnas
description: Selles teemas kirjeldatakse Project Operationsi demoandmete rakendamist Dynamics 365 Finance pilvepõhisesse keskkonda.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7cdbd2847ce45972aadd0d1a2d4f26270727ad9
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365233"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="52d5d-103">Demoandmete rakendamine rakenduse Finance pilvepõhises keskkonnas</span><span class="sxs-lookup"><span data-stu-id="52d5d-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="52d5d-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="52d5d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52d5d-105">See teema on rakendatav ainult Microsoft Dynamics 365 Finance'i versiooniga 10.0.13 ja seda saab teha ainult pilvepõhises keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="52d5d-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="52d5d-106">**ENNE** keskkonnale kvaliteedivärskenduste rakendamist viige lõpule selle teema etapid.</span><span class="sxs-lookup"><span data-stu-id="52d5d-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="52d5d-107">Avage oma LCS-i projektis leht **Keskkonna üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="52d5d-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="52d5d-108">Pange tähele, et see sisaldab Remote Desktop Protocoli (RDP) abil keskkonnaga ühenduse loomiseks vajalikke üksikasju.</span><span class="sxs-lookup"><span data-stu-id="52d5d-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![i keskkonna üksikasjad](./media/1EnvironmentDetails.png)

<span data-ttu-id="52d5d-110">Esimene esiletõstetud mandaatide komplekt on kohaliku ettevõtte mandaat ja sisaldab hüperlinki kaugtöölaua ühendusele.</span><span class="sxs-lookup"><span data-stu-id="52d5d-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="52d5d-111">Mandaat sisaldab keskkonna administraatori kasutajanime ja parooli.</span><span class="sxs-lookup"><span data-stu-id="52d5d-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="52d5d-112">Teist mandaatide kogumit kasutatakse selles keskkonnas SQL-i serverisse sisselogimiseks.</span><span class="sxs-lookup"><span data-stu-id="52d5d-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="52d5d-113">Liikuge keskkonda läbi hüperlingi jaotises **Kohalikud kontod** ja kasutage autentimiseks **Kohaliku konto mandaati**.</span><span class="sxs-lookup"><span data-stu-id="52d5d-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="52d5d-114">Minge jaotisse **Interneti infoteenused** > **Rakenduste kogumid** > **AOSService** ja peatage teenus.</span><span class="sxs-lookup"><span data-stu-id="52d5d-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="52d5d-115">Peatate praegu teenuse, et saaksite minna edasi SQL-i andmebaasi asendamisega.</span><span class="sxs-lookup"><span data-stu-id="52d5d-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![AOS-i peatamine](./media/2StopAOS.png)

4. <span data-ttu-id="52d5d-117">Minge jaotisse **Teenused** ja peatage järgmised kaks üksust.</span><span class="sxs-lookup"><span data-stu-id="52d5d-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="52d5d-118">Microsoft Dynamics 365 Unified Operations: paketthalduse teenus</span><span class="sxs-lookup"><span data-stu-id="52d5d-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="52d5d-119">Microsoft Dynamics 365 Unified Operations: andmete importimise eksportimise raamistik</span><span class="sxs-lookup"><span data-stu-id="52d5d-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Peatage teenused](./media/3StopServices.png)

5. <span data-ttu-id="52d5d-121">Avage Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="52d5d-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="52d5d-122">Logige sisse SQL serveri mandaadiga ja kasutage axdbadmin kasutajat ja parooli LCS-i lehelt **Keskkondade üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="52d5d-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="52d5d-124">Avage Object Exploereris **Andmebaasid** ja otsige üles **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="52d5d-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="52d5d-125">Andmebaasi asendate uue andmebaasiga, mis asub [allalaadimiskeskuses](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="52d5d-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="52d5d-126">Kopeerige ZIP-fail VM-i, millesse oled kaugelt sisenenud, ja pakkige zip-faili sisu lahti.</span><span class="sxs-lookup"><span data-stu-id="52d5d-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="52d5d-127">Paremklõpsake SQL Server Management Studios valikul **AxDB** ja seejärel valige **Tööülesanded** > **Taasta** > **Andmebaas**.</span><span class="sxs-lookup"><span data-stu-id="52d5d-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Andmebaasi taastamine](./media/5RestoreDatabase.png)

9. <span data-ttu-id="52d5d-129">Valige **Lähteseade** ja liikuge kopeeritud zip-failist lahtipakitud faili juurde.</span><span class="sxs-lookup"><span data-stu-id="52d5d-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Lähteseadmed](./media/6SourceDevice.png)

10. <span data-ttu-id="52d5d-131">Valige **Suvandid** ja seejärel valige **Kirjuta olemasolev andmebaas üle** ja **Sulge olemasolevad ühendused sihtkoha andmebaasiga**.</span><span class="sxs-lookup"><span data-stu-id="52d5d-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="52d5d-132">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="52d5d-132">Select **OK**.</span></span>

![Sätete taastamine](./media/7RestoreSetting.png)

<span data-ttu-id="52d5d-134">Teile saadetakse kinnitus, et AXDB-i taastamine õnnestus.</span><span class="sxs-lookup"><span data-stu-id="52d5d-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="52d5d-135">Pärast selle kinnituse saamist saate SQL Services Management Studio sulgeda.</span><span class="sxs-lookup"><span data-stu-id="52d5d-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="52d5d-136">Minge tagasi jaotisse **Interneti infoteenused** > **Rakenduste kogumid** > **AOSService** ja käivitage AOSService.</span><span class="sxs-lookup"><span data-stu-id="52d5d-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="52d5d-137">Minge jaotisse **Teenused** ja käivitage kaks teenust, mille varem peatasite.</span><span class="sxs-lookup"><span data-stu-id="52d5d-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="52d5d-138">Otsige üles selle VM-i AdminUserProvisioning tööriist.</span><span class="sxs-lookup"><span data-stu-id="52d5d-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="52d5d-139">Vaadake asukohta K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="52d5d-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="52d5d-140">Käivitage .ext-faili kasutades oma kasutaja aadressi väljal **Meiliaadress**.</span><span class="sxs-lookup"><span data-stu-id="52d5d-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="52d5d-141">Valige käsk **Esita**.</span><span class="sxs-lookup"><span data-stu-id="52d5d-141">Select **Submit**.</span></span>

![Administraatori ettevalmistamine](./media/8AdminUserProvisioning.png)

<span data-ttu-id="52d5d-143">Selle lõpuleviimiseks kulub mõni minut.</span><span class="sxs-lookup"><span data-stu-id="52d5d-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="52d5d-144">Peaksite saama kinnituse, et administraatori kasutaja värskendamine õnnestus.</span><span class="sxs-lookup"><span data-stu-id="52d5d-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="52d5d-145">Lõpuks käivitage administraatorina käsuviip ja tehke iisreset</span><span class="sxs-lookup"><span data-stu-id="52d5d-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS reset](./media/9IISReset.png)

18. <span data-ttu-id="52d5d-147">Sulgege kaugtöölaua seanss ja kasutage LCS-i lehte **Keskkonna üksikasjad**, et logida keskkonda sisse ja kontrollida, et see töötab ootuspäraselt.</span><span class="sxs-lookup"><span data-stu-id="52d5d-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
