---
title: Tööülesande ruudustikus töötamise tõrkeotsing
description: Selles teemas kirjeldatakse tõrkeotsingu teavet, mida on vaja tööülesande ruudustikus töötamisel.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031532"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="1140f-103">Tööülesande ruudustikus töötamise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="1140f-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="1140f-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="1140f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1140f-105">Selles teemas kirjeldatakse, kuidas parandada probleeme, mis võivad ilmneda kuluhaldusega töötamisel.</span><span class="sxs-lookup"><span data-stu-id="1140f-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="1140f-106">Küpsiste lubamine</span><span class="sxs-lookup"><span data-stu-id="1140f-106">Enable cookies</span></span>

<span data-ttu-id="1140f-107">Project Operations vajab, et kolmanda osapoole küpsised oleksid lubatud, et tööjaotuse struktuuri renderdada.</span><span class="sxs-lookup"><span data-stu-id="1140f-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="1140f-108">Kui kolmanda osapoole küpsised pole lubatud, näete toimingute nägemise asemel tühja lehte, kui valite vahekaardi **Tööülesanded** lehel **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="1140f-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Tühi vahekaart, kui kolmanda osapoole küpsised pole lubatud](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="1140f-110">Lahendus</span><span class="sxs-lookup"><span data-stu-id="1140f-110">Workaround</span></span>
<span data-ttu-id="1140f-111">Brauserite Microsoft Edge või Google Chrome korral kirjeldavad järgmised toimingud seda, kuidas oma brauserisätteid värskendada ja lubada kolmanda osapoole küpsiseid.</span><span class="sxs-lookup"><span data-stu-id="1140f-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="1140f-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1140f-112">Microsoft Edge</span></span>

1. <span data-ttu-id="1140f-113">Avage brauser Edge.</span><span class="sxs-lookup"><span data-stu-id="1140f-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="1140f-114">Valige paremas ülanurgas **kolmikpunkt** (...) ja seejärel valige **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="1140f-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="1140f-115">Valige jaotises **Küpsised ja saidiõigused** suvand **Küpsised ja saidiandmed**.</span><span class="sxs-lookup"><span data-stu-id="1140f-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="1140f-116">Lülitage **Kolmanda osapoole küpsiste blokeerimine** välja.</span><span class="sxs-lookup"><span data-stu-id="1140f-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="1140f-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="1140f-117">Google Chrome</span></span>

1. <span data-ttu-id="1140f-118">Avage brauser Chrome.</span><span class="sxs-lookup"><span data-stu-id="1140f-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="1140f-119">Valige paremas ülanurgas kolm vertikaalset punkti ja seejärel valige **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="1140f-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="1140f-120">Valige jaotises **Privaatsus ja turvalisus** suvand **Küpsised ja muud saidiandmed**.</span><span class="sxs-lookup"><span data-stu-id="1140f-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="1140f-121">Valige **Luba kõik küpsised**.</span><span class="sxs-lookup"><span data-stu-id="1140f-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1140f-122">Kui te blokeerite kolmanda osapoole küpsised, blokeeritakse kõik muude saitide küpsised ja saidiandmed, isegi kui see sait on lubatud teie erandite loendis.</span><span class="sxs-lookup"><span data-stu-id="1140f-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="1140f-123">PEX-i lõpp-punkt</span><span class="sxs-lookup"><span data-stu-id="1140f-123">PEX Endpoint</span></span>

<span data-ttu-id="1140f-124">Project Operations vajab, et projekti parameeter viitaks PEX-i lõpp-punktile.</span><span class="sxs-lookup"><span data-stu-id="1140f-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="1140f-125">See lõpp-punkt on nõutav, et suhelda teenusega, mida kasutatakse tööjaotuse struktuuri renderdamiseks.</span><span class="sxs-lookup"><span data-stu-id="1140f-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="1140f-126">Kui parameeter pole lubatud, kuvatakse tõrketeade "Projekti parameeter ei ole kehtiv".</span><span class="sxs-lookup"><span data-stu-id="1140f-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="1140f-127">Lahendus</span><span class="sxs-lookup"><span data-stu-id="1140f-127">Workaround</span></span>
 ![PEX-i lõpp-punkti väli projekti parameetris](media/projectparameter.png)

1. <span data-ttu-id="1140f-129">Lisage **PEX-i lõpp-punkti** väli lehele **Projekti parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1140f-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="1140f-130">Lisage väljale järgmine väärtus: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="1140f-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="1140f-131">Eemaldage väli lehelt **Projekti parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1140f-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="1140f-132">Projekti õigused veebi jaoks</span><span class="sxs-lookup"><span data-stu-id="1140f-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="1140f-133">Project Operations sõltub välisest ajastamisteenusest.</span><span class="sxs-lookup"><span data-stu-id="1140f-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="1140f-134">Teenuse kasutamiseks peab kasutajale olema määratud mitu rolli, et lugeda ja kirjutada tööjaotuse struktuuriga seotud olemeid.</span><span class="sxs-lookup"><span data-stu-id="1140f-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="1140f-135">Nende olemite hulka kuuluvad projektiülesanded, ressursi määramised ja ülesande sõltuvused.</span><span class="sxs-lookup"><span data-stu-id="1140f-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="1140f-136">Kui kasutaja ei saa tööjaotuse struktuuri renderdada, kui ta läheb vahekaardile **Tööülesanded**, on see tõenäoliselt sellepärast, et projekt pole Project Operationsi jaoks lubatud.</span><span class="sxs-lookup"><span data-stu-id="1140f-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="1140f-137">Kasutaja võib saada kas turberolliga või juurdepääsu keelamisega seotud tõrke.</span><span class="sxs-lookup"><span data-stu-id="1140f-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="1140f-138">Lahendus</span><span class="sxs-lookup"><span data-stu-id="1140f-138">Workaround</span></span>

1. <span data-ttu-id="1140f-139">Avage **Sätted > Turvalisus > Kasutajad > Rakenduse kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="1140f-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Rakenduse lugeja](media/applicationuser.jpg)
   
2. <span data-ttu-id="1140f-141">Topeltklõpsake rakenduse kasutajakirjet, et kontrollida järgmist.</span><span class="sxs-lookup"><span data-stu-id="1140f-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="1140f-142">Kasutajal on projektile juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="1140f-142">The user has access to the project.</span></span> <span data-ttu-id="1140f-143">Seda kontrolli tehakse tavaliselt kinnitades, et kasutajal on **Projektijuhi** turberoll.</span><span class="sxs-lookup"><span data-stu-id="1140f-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="1140f-144">Microsoft Projecti rakenduse kasutaja on olemas ja on õigesti konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="1140f-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="1140f-145">Kui kasutajat pole olemas, saate luua uue kasutajakirje.</span><span class="sxs-lookup"><span data-stu-id="1140f-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="1140f-146">Valige **Uued kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="1140f-146">Select **New Users**.</span></span> <span data-ttu-id="1140f-147">Muutke sisestusvormiks **Rakenduse kasutaja** ja seejärel lisage **Rakenduse ID**.</span><span class="sxs-lookup"><span data-stu-id="1140f-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Rakenduse kasutaja üksikasjad](media/applicationuserdetails.jpg)

4. <span data-ttu-id="1140f-149">Kontrollige, et kasutajale on määratud õige litsents ja et teenus on litsentsi teenuseplaani üksikasjades lubatud.</span><span class="sxs-lookup"><span data-stu-id="1140f-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="1140f-150">Veenduge, et kasutaja saab avada lehe project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="1140f-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="1140f-151">Kontrollige läbi projekti parameetrite, et süsteem osutab õigele projekti lõpp-punktile.</span><span class="sxs-lookup"><span data-stu-id="1140f-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="1140f-152">Kontrollige, kas projekti rakenduse kasutaja on loodud.</span><span class="sxs-lookup"><span data-stu-id="1140f-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="1140f-153">Rakendage kasutajale järgmised turberollid.</span><span class="sxs-lookup"><span data-stu-id="1140f-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="1140f-154">Dataverse'i kasutaja</span><span class="sxs-lookup"><span data-stu-id="1140f-154">Dataverse User</span></span>
  - <span data-ttu-id="1140f-155">Project Operationsi süsteem</span><span class="sxs-lookup"><span data-stu-id="1140f-155">Project Operations System</span></span>
  - <span data-ttu-id="1140f-156">Projekti süsteem</span><span class="sxs-lookup"><span data-stu-id="1140f-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="1140f-157">Tõrge tööjaotuse struktuuri värskendamisel</span><span class="sxs-lookup"><span data-stu-id="1140f-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="1140f-158">Kui tööjaotuse struktuurile tehakse üks või mitu värskendust, siis muudatused lõpuks nurjuvad ja neid ei salvestata.</span><span class="sxs-lookup"><span data-stu-id="1140f-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="1140f-159">Ajakavaruudustikus kuvatakse tõrge, et "Teie hiljutisi muudatusi ei saanud salvestada".</span><span class="sxs-lookup"><span data-stu-id="1140f-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="1140f-160">Lahendus</span><span class="sxs-lookup"><span data-stu-id="1140f-160">Workaround</span></span>

1. <span data-ttu-id="1140f-161">Kontrollige, et kasutajale on määratud õige litsents ja et teenus on litsentsi teenuseplaani üksikasjades lubatud.</span><span class="sxs-lookup"><span data-stu-id="1140f-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="1140f-162">Veenduge, et kasutaja saab avada lehe project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="1140f-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="1140f-163">Kontrollige, et süsteem osutab õigele projekti lõpp-punktile.</span><span class="sxs-lookup"><span data-stu-id="1140f-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="1140f-164">Kontrollige, kas projekti rakenduse kasutaja on loodud.</span><span class="sxs-lookup"><span data-stu-id="1140f-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="1140f-165">Rakendage kasutajale järgmised turberollid.</span><span class="sxs-lookup"><span data-stu-id="1140f-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="1140f-166">Dataverse'i kasutaja või baaskasutaja</span><span class="sxs-lookup"><span data-stu-id="1140f-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="1140f-167">Project Operationsi süsteem</span><span class="sxs-lookup"><span data-stu-id="1140f-167">Project Operations System</span></span>
  - <span data-ttu-id="1140f-168">Projekti süsteem</span><span class="sxs-lookup"><span data-stu-id="1140f-168">Project System</span></span>
  - <span data-ttu-id="1140f-169">Project Operationsi topeltkirjutamise süsteem (see roll on vajalik, kui kasutate Project Operationsi ressursipõhist/mittelaopõhist stsenaariumi.)</span><span class="sxs-lookup"><span data-stu-id="1140f-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
