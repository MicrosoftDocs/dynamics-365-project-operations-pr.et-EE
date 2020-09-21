---
title: Näidisandmete installimine
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: kfend
ms.suite: ''
ms.technology: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.assetid: 8580fc8b-868a-42a3-aa04-2afab28d6de4
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 1c1300116fe42091620267fb128ca6c63184970e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750890"
---
# <a name="sample-data-installation-for-the-project-service-application"></a><span data-ttu-id="77ef9-102">Näidisandmete installimine Project Service’i rakendusele</span><span class="sxs-lookup"><span data-stu-id="77ef9-102">Sample data installation for the Project Service application</span></span>

<span data-ttu-id="77ef9-103">Selleks et aidata teil luua oma demokeskkondi, pakub Microsoft allalaaditavaid näidisandmete pakette, mis näitavad teie rakenduste võimeid.</span><span class="sxs-lookup"><span data-stu-id="77ef9-103">To help you build your own demo environments, Microsoft provides downloadable sample data packages that showcase the capabilities of your apps.</span></span> <span data-ttu-id="77ef9-104">Näidisandmete pakette on kaht tüüpi:</span><span class="sxs-lookup"><span data-stu-id="77ef9-104">There are two types of sample data packages:</span></span>
- <span data-ttu-id="77ef9-105">viiteandmed/seadistusandmed</span><span class="sxs-lookup"><span data-stu-id="77ef9-105">reference/setup data</span></span>
- <span data-ttu-id="77ef9-106">demoandmed (viite-/seadistusandmed ja tehingu andmed, nt töökäsud ja projektid)</span><span class="sxs-lookup"><span data-stu-id="77ef9-106">demo data (reference/setup and transactional data such as work orders and projects)</span></span>

<span data-ttu-id="77ef9-107">**Viiteandmete** näidispaketid on allalaaditavad kolme eraldi paketina, nii et saate andmeid installida ainult Project Service’i või Field Service’i jaoks või installida näidisandmed mõlema rakenduse jaoks korraga.</span><span class="sxs-lookup"><span data-stu-id="77ef9-107">The sample **reference** data packages are downloadable in three different packages, so you can install data only for Project Service, or only for Field Service, or you can install sample data for both applications at once.</span></span>

<span data-ttu-id="77ef9-108">Seadistus-/viiteandmete näidispaketid on järgmised:</span><span class="sxs-lookup"><span data-stu-id="77ef9-108">The sample setup/reference data packages are:</span></span>

- [<span data-ttu-id="77ef9-109">**V902PSMasterData** – ainult Project Service’i versioon 3.x</span><span class="sxs-lookup"><span data-stu-id="77ef9-109">**V902PSMasterData** - Project Service version 3.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [<span data-ttu-id="77ef9-110">**V902FSMasterData** – ainult Field Service’i versioon 8.x</span><span class="sxs-lookup"><span data-stu-id="77ef9-110">**V902FSMasterData** - Field Service version 8.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [<span data-ttu-id="77ef9-111">**V902FPSMasterData** – Field Service 8.x ja Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="77ef9-111">**V902FPSMasterData** - Field Service 8.x and Project Service 3.x</span></span>](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

<span data-ttu-id="77ef9-112">Uusi **demoandmete** pakett on järgmine:</span><span class="sxs-lookup"><span data-stu-id="77ef9-112">The latest **demo** data package is:</span></span>

 - [<span data-ttu-id="77ef9-113">**FPSDemoData** – Field Service 8.x ja Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="77ef9-113">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span></span>](https://aka.ms/fpsdemodatapackage)

   <span data-ttu-id="77ef9-114">Installijuhised erinevad veidi kasutajate loomise ja konfigureerimise osas, aga ülejäänu on sama kui eelmises [**ajaveebipostituses**](https://aka.ms/fpsdemodatablog).</span><span class="sxs-lookup"><span data-stu-id="77ef9-114">Installation instructions differ slightly in the users to create and configure section but the rest is the same as in the previous [**blog post**](https://aka.ms/fpsdemodatablog).</span></span> <span data-ttu-id="77ef9-115">Selles paketis on vähendatud demoandmete pakett ja selle installimine kestab umbes 3 tundi.</span><span class="sxs-lookup"><span data-stu-id="77ef9-115">This package features a reduced demo data set and takes approximately 3 hours to install.</span></span>

<span data-ttu-id="77ef9-116">Need näidisandmete paketid on saadaval ainult inglise keeles.</span><span class="sxs-lookup"><span data-stu-id="77ef9-116">These sample data packages are available in English only.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77ef9-117">**Näidisandmeid pole võimalik desinstallida.**</span><span class="sxs-lookup"><span data-stu-id="77ef9-117">**There is no way to uninstall the sample data.**</span></span> <span data-ttu-id="77ef9-118">Installige need paketid vaid demo-, hindamis-, õppe- või katsesüsteemidesse.</span><span class="sxs-lookup"><span data-stu-id="77ef9-118">You should only install these packages on demonstration, evaluation, training, or test systems.</span></span> <span data-ttu-id="77ef9-119">Peale selle pange tähele, et ei toetata üksiku paketi ja seejärel teise üksiku paketi installimist.</span><span class="sxs-lookup"><span data-stu-id="77ef9-119">Also note that installing an individual package, and then installing the other individual package, is not supported.</span></span> <span data-ttu-id="77ef9-120">(Teisisõnu pole teil võimalik installida paketti **FSMasterData** ja seejärel paketti **PSMasterData** või vastupidi.) Kui näete, et teil võib kunagi vaja minna mõlema rakenduse näidisandmeid, installige pakett **v902FPSMasterData**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-120">(In other words, you can't install **FSMasterData** followed by **PSMasterData**, or vice versa.) If you see yourself needing sample data for both applications at any point in the future, you should install the **v902FPSMasterData** package.</span></span>

<span data-ttu-id="77ef9-121">Kui installite mõne näidisandmete pakettidest, toimub installimisprotsessi käigus järgmine.</span><span class="sxs-lookup"><span data-stu-id="77ef9-121">When you install any of the sample data packages, the installation process performs the following actions:</span></span>

- <span data-ttu-id="77ef9-122">Luuakse või seadistatakse vaikeparameetrid Project Service’i, Field Service’i või mõlema rakenduse kasutamiseks (kui on olemas).</span><span class="sxs-lookup"><span data-stu-id="77ef9-122">Creates or sets default parameters for using Project Service, Field Service, or both applications (if applicable).</span></span>

- <span data-ttu-id="77ef9-123">Imporditakse rakenduste näidisandmed, nt broneeritavad ressursid, rakendusepõhised rollid, müügi ja kulu hinnakirjad, organisatsiooniüksused, müügiprotsessi kirjed ja muud üksused põhivõimaluste näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="77ef9-123">Imports sample data for the applications, such as bookable resources, application-specific roles, sales and cost price lists, organizational units, sales process records, and other entities to demonstrate key capabilities.</span></span>  

<span data-ttu-id="77ef9-124">**Demoandmete** paketiga saate ülaltoodud täiendavad tehingu andmed, nt töökäsud ja projektid.</span><span class="sxs-lookup"><span data-stu-id="77ef9-124">With the **demo data** package, you get the above and additional transactional data such as work orders and projects.</span></span>

<span data-ttu-id="77ef9-125">Kas mõtlete, milliseid võimalusi saate näidisandmetega demonstreerida?</span><span class="sxs-lookup"><span data-stu-id="77ef9-125">Wondering what capabilities you can demo with the sample data?</span></span> <span data-ttu-id="77ef9-126">Vaadake jaotisest [Tehnilised märkused](#technical-notes) väljamõeldud näidet ettevõttest Fabrikam Robotics.</span><span class="sxs-lookup"><span data-stu-id="77ef9-126">See the Fabrikam Robotics fictitious scenario in [Technical notes](#technical-notes).</span></span>

<span data-ttu-id="77ef9-127">Kui teil on küsimusi nende näidisandmete pakettide installimise kohta, [saatke meile meil aadressil fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="77ef9-127">If you have questions about installing these sample data packages, [send us an email at fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span></span>

## <a name="requirements"></a><span data-ttu-id="77ef9-128">Nõuded</span><span class="sxs-lookup"><span data-stu-id="77ef9-128">Requirements</span></span>

<span data-ttu-id="77ef9-129">Installimisprotokoll eeldab teie sihteksemplari (organisatsiooni) kohta järgmist.</span><span class="sxs-lookup"><span data-stu-id="77ef9-129">The installation protocol assumes the following about your target instance (org):</span></span>

- <span data-ttu-id="77ef9-130">Põhikeel on inglise keel ja põhivaluuta USA dollar (USD, $).</span><span class="sxs-lookup"><span data-stu-id="77ef9-130">Base language is English and base currency is US dollar (USD,$).</span></span>

- <span data-ttu-id="77ef9-131">Organisatsioonil pole veel Project Service’i või Field Service’i andmeid või on ainult minimaalsed vaikeandmed, mis on kaasas iga uue organisatsiooniga.</span><span class="sxs-lookup"><span data-stu-id="77ef9-131">The org has no Project Service or Field Service data already, or only has barebones default data that comes with any new org.</span></span>

- <span data-ttu-id="77ef9-132">Installitud on juba ärirakenduse õige versioon.</span><span class="sxs-lookup"><span data-stu-id="77ef9-132">The correct version of the business application is already installed:</span></span>
       
    - <span data-ttu-id="77ef9-133">**FPSDemoData või v902FPSMasterData jaoks:** organisatsiooni on installitud Field Service’i versioon 8.x ja Project Service’i versioon 3.x.</span><span class="sxs-lookup"><span data-stu-id="77ef9-133">**For FPSDemoData or v902FPSMasterData:** The org has Field Service version 8.x and Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="77ef9-134">**v902PSMasterData jaoks:** organisatsiooni on installitud Project Service’i versioon 3.x.</span><span class="sxs-lookup"><span data-stu-id="77ef9-134">**For v902PSMasterData:** The org has Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="77ef9-135">**v902FSMasterData jaoks:** organisatsiooni on installitud Field Service’i versioon 8.x.</span><span class="sxs-lookup"><span data-stu-id="77ef9-135">**For v902FSMasterData:** The org has Field Service version 8.x installed.</span></span>

> [!NOTE]
> <span data-ttu-id="77ef9-136">Kui peate installima näidisandmed lisaks olemasolevale Project Service’i ja Field Service’i proovi- või demokeskkonnale, milles juba on andmeid (pole soovitatav), peate seiskama installija tehtavad ohutuse kontrollid.</span><span class="sxs-lookup"><span data-stu-id="77ef9-136">If you need to install the sample data on top of an existing Project Service and Field Service trial or demo environment that already has data (not recommended), you'll need to suspend the safety prechecks performed by the installer.</span></span> <span data-ttu-id="77ef9-137">Lisateavet vt allolevatest tehnilistest märkustest.</span><span class="sxs-lookup"><span data-stu-id="77ef9-137">For more information, see the technical notes below.</span></span>

## <a name="prepare-for-installation"></a><span data-ttu-id="77ef9-138">Installimise ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="77ef9-138">Prepare for installation</span></span>

<span data-ttu-id="77ef9-139">Peate käivitama installija arvutis, millel on Windowsi uusim versioon (eelistatult Windows 10).</span><span class="sxs-lookup"><span data-stu-id="77ef9-139">You need to run the installer on a computer with a recent version of Windows (Windows 10 preferred).</span></span>

<span data-ttu-id="77ef9-140">Plaanige nii, et arvuti oleks võrku ühendatud ja **seadistus-/viiteandmete** installimine kestaks kuni **1 tund**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-140">You should plan for the computer to remain connected to a network, and for the installation to run for up to **1 hour** for **setup/reference data**.</span></span> <span data-ttu-id="77ef9-141">(Tavaliselt kestab **FPSMasterData** installimine umbes 30 minutit, see hõlmab mõlema rakenduse näidisandmeid.) **FPSDemoData** installimine kestab umbes **3 tundi**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-141">(Normally the installation takes around 30 minutes for **FPSMasterData**, which includes sample data for both applications.) For the **FPSDemoData**, the installation will take around **3 hours**.</span></span>

<span data-ttu-id="77ef9-142">Arvuti ekraanisäästja funktsioon peab olema välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="77ef9-142">The computer should have the screen saver function turned off.</span></span> <span data-ttu-id="77ef9-143">Muidu võivad installimise seansi mandaadid ekraanisäästja rakendumisel kaduma minna (kui te ei hoia seanssi pidevalt aktiivsena).</span><span class="sxs-lookup"><span data-stu-id="77ef9-143">Otherwise, session credentials for the installation may be lost when the screen saver engages (unless you keep your session active throughout).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="77ef9-144">![Ekraanisäästja sätete kuvatõmmis, ekraanisäästja on välja lülitatud](media/sample-data-1.png)</span><span class="sxs-lookup"><span data-stu-id="77ef9-144">![Screenshot of screen saver settings, with screen saver turned off](media/sample-data-1.png)</span></span>

## <a name="download-and-unpack"></a><span data-ttu-id="77ef9-145">Allalaadimine ja lahtipakkimine</span><span class="sxs-lookup"><span data-stu-id="77ef9-145">Download and unpack</span></span>

<span data-ttu-id="77ef9-146">Project Service’i ja Field Service’i näidisandmete installijat levitatakse ise lahtipakkiva täitmisfailina.</span><span class="sxs-lookup"><span data-stu-id="77ef9-146">The Project Service and Field Service sample data installer is distributed as a self-extracting executable.</span></span> <span data-ttu-id="77ef9-147">Failinimed võivad näidisandmete paketist olenevalt olla erinevad, aga etapid on samad, olenemata sellest, millise paketi installite.</span><span class="sxs-lookup"><span data-stu-id="77ef9-147">The file names may vary depending on the sample data package, but otherwise the steps are the same no matter which package you install.</span></span>

<span data-ttu-id="77ef9-148">Pärast paketi allalaadimist käivitage EXE-fail ja tihendatud ZIP-faili lahtipakkimiseks nõustuge tingimustega.</span><span class="sxs-lookup"><span data-stu-id="77ef9-148">After downloading a package, run the .exe file, and then accept terms and conditions to unpack the compressed zip file.</span></span> <span data-ttu-id="77ef9-149">Peate faili sisu lahti pakkima mõnda kausta arvutis.</span><span class="sxs-lookup"><span data-stu-id="77ef9-149">You then need to extract contents of that file to a folder on the computer.</span></span>

<span data-ttu-id="77ef9-150">Operatsioonisüsteemist ja turvasätetest olenevalt võivad pärast ZIP-faili lahtipakkimist vajalikud olla järgmised sammud.</span><span class="sxs-lookup"><span data-stu-id="77ef9-150">Depending on the operating system and security settings, you may need to perform the following steps after unpacking the zip file:</span></span>

1. <span data-ttu-id="77ef9-151">Otsige üles fail **FPSDemoData.dll** ja paremklõpsake sellel kaustas **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-151">Find and right-click the **FPSDemoData.dll** file in the **v902FPSMasterData** / **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="77ef9-152">Valige suvand **Tühista blokeerimine**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-152">Choose **Unblock**.</span></span>

3. <span data-ttu-id="77ef9-153">Valige suvand **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-153">Select **Apply**.</span></span>

4. <span data-ttu-id="77ef9-154">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-154">Select **OK**.</span></span>


## <a name="create-or-configure-users"></a><span data-ttu-id="77ef9-155">Kasutajate loomine või konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="77ef9-155">Create or configure users</span></span>

<span data-ttu-id="77ef9-156">**FPSDemoData** pakett nõuab kuut kasutajat, **FPSMasterData** paketid nõuavad üht kasutajat.</span><span class="sxs-lookup"><span data-stu-id="77ef9-156">The **FPSDemoData** package requires six users while **FPSMasterData** packages require one user.</span></span> <span data-ttu-id="77ef9-157">Kasutage oma näidisandmete paketi jaoks sobivat varianti.</span><span class="sxs-lookup"><span data-stu-id="77ef9-157">Refer to the correct one for your sample data package.</span></span>

## <a name="create-or-configure-users---setupreference-data-packages"></a><span data-ttu-id="77ef9-158">Kasutajate loomine või konfigureerimine – seadistus-/viiteandmete paketid</span><span class="sxs-lookup"><span data-stu-id="77ef9-158">Create or configure users - setup/reference data packages</span></span>

<span data-ttu-id="77ef9-159">Pakett **FPSMasterData** on mõeldud ühe kasutaja nimega Spencer Low installimiseks siin kirjeldatud sätetega.</span><span class="sxs-lookup"><span data-stu-id="77ef9-159">The **FPSMasterData** package is designed to install with one user named Spencer Low with the settings described here.</span></span> <span data-ttu-id="77ef9-160">Paketi õigesti installimiseks peate looma (või ajutiselt ümber nimetama) kasutajad teie keskkonnas, et need ühtiks sissetulevate näidisandmete konfiguratsiooniga.</span><span class="sxs-lookup"><span data-stu-id="77ef9-160">To install the package correctly, you need to create (or temporarily rename) users in your environment to match the incoming sample data configuration.</span></span>

<span data-ttu-id="77ef9-161">Kasutajate loomiseks või konfigureerimiseks valige **Sätted** > **Turve** > **Kasutajad** ja tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="77ef9-161">To create or configure users, go to **Settings** > **Security** > **Users**, and do the following:</span></span>

1. <span data-ttu-id="77ef9-162">Määrake suvand UserFullname="Spencer Low" kasutajanimega "spencerl" (**väiketähed**) Project Manageri ja Practice Manageri rollidele.</span><span class="sxs-lookup"><span data-stu-id="77ef9-162">Set UserFullname="Spencer Low" with username "spencerl" (**lowercase**) to the Project Manager and Practice Manager roles.</span></span>

2. <span data-ttu-id="77ef9-163">Valige kasutaja **Spencer Low** ja seejärel suvand **Rollide haldamine**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-163">Select the **Spencer Low** user, and then select **Manage Roles**.</span></span> <span data-ttu-id="77ef9-164">Otsige üles ja valige roll **Süsteemiadministraator** ning seejärel valige nupp **OK**, et anda kasutajale Spencer Low administraatori täielikud õigused.</span><span class="sxs-lookup"><span data-stu-id="77ef9-164">Find and select the **System Administrator** role, and then select **OK** to grant full admin rights to Spencer Low.</span></span> <span data-ttu-id="77ef9-165">See etapp on vajalik tagamaks, et näidiskirjed luuakse õige kasutaja omandusega ja seega vaated täidetakse õigesti.</span><span class="sxs-lookup"><span data-stu-id="77ef9-165">This step is necessary to ensure that sample records are created with the correct user ownership and therefore populate views correctly.</span></span>

3. <span data-ttu-id="77ef9-166">Allalaadimispaketist peate värskendama andmete vastendamise faili vaikimisi kasutaja konteksti meiliaadressidega.</span><span class="sxs-lookup"><span data-stu-id="77ef9-166">From the downloaded package, you need to update a data mapping file with email addresses of the default user context.</span></span> <span data-ttu-id="77ef9-167">Selleks avage kaust **PkgFolder** ning otsige üles ja avage fail **ImportUserMapFile.xml** Notepadis (või Visual Studios või muus XML-redaktoris).</span><span class="sxs-lookup"><span data-stu-id="77ef9-167">To do this, open **PkgFolder**, and then find and open the **ImportUserMapFile.xml** file in Notepad (or Visual Studio or another XML editor).</span></span> <span data-ttu-id="77ef9-168">Määrake välja **DefaultUserToMapTo=** väärtuseks kasutaja Spencer Low meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="77ef9-168">Set the **DefaultUserToMapTo=** field to the email address of the Spencer Low user.</span></span>

4. <span data-ttu-id="77ef9-169">Kui te ei kasuta kasutajat Spencer Low kasutajanimega **spencerl**, peate värskendama lisafaili.</span><span class="sxs-lookup"><span data-stu-id="77ef9-169">If you aren't using Spencer Low with username **spencerl**, you need to update an additional file.</span></span> <span data-ttu-id="77ef9-170">Avage fail **DemoDataPreImportConfig.xml** ja otsige üles silt **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-170">Open the **DemoDataPreImportConfig.xml** file, and then find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="77ef9-171">Värskendage silti **\<login\>** kasutaja Spencer Low kasutajanimega.</span><span class="sxs-lookup"><span data-stu-id="77ef9-171">Update the **\<login\>** tag with the username of your Spencer Low user.</span></span> <span data-ttu-id="77ef9-172">Üksikasju vaadake jaotisest [Tehnilised märkused](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="77ef9-172">For additional details, see [Technical notes](#technical-notes).</span></span>

## <a name="create-or-configure-users---demo-data-package"></a><span data-ttu-id="77ef9-173">Kasutajate loomine või konfigureerimine – demoandmete pakett</span><span class="sxs-lookup"><span data-stu-id="77ef9-173">Create or configure users - demo data package</span></span>

<span data-ttu-id="77ef9-174">Demoandmete paketi jaoks on vaja kuut kasutajat.</span><span class="sxs-lookup"><span data-stu-id="77ef9-174">The demo data package requires six users.</span></span> <span data-ttu-id="77ef9-175">Selleks et pakett õigesti installitaks, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="77ef9-175">For the package to install correctly, do the following:</span></span>

 1. <span data-ttu-id="77ef9-176">Looge kasutajad või nimetage ajutiselt ümber olemasolevad kasutajad, nii et need ühtiks sissetulevate näidisandmete konfiguratsiooniga, valides **Sätted** > **Turve** > **Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-176">Create or temporarily rename existing users to match incoming sample data configuration by going to **Settings** > **Security** > **Users**.</span></span>
 
    <span data-ttu-id="77ef9-177">Neid rolle on vaja ainult isiklike demode jaoks.</span><span class="sxs-lookup"><span data-stu-id="77ef9-177">These roles are only needed for persona-based demos.</span></span>  
    - <span data-ttu-id="77ef9-178">Väliteeninduse tehnik, kasutaja täisnimi = "David So"</span><span class="sxs-lookup"><span data-stu-id="77ef9-178">User Fullname="David So" as Field Service Technician</span></span>   
    - <span data-ttu-id="77ef9-179">Klienditeeninduse ja väliteeninduse dispetšer, kasutaja täisnimi = "Jamie Reding"</span><span class="sxs-lookup"><span data-stu-id="77ef9-179">User Fullname="Jamie Reding" as Customer Service & Field Service Dispatcher</span></span>   
    - <span data-ttu-id="77ef9-180">Kontohaldur, kasutaja täisnimi = "Molly Clark"</span><span class="sxs-lookup"><span data-stu-id="77ef9-180">User Fullname="Molly Clark" as Account Manager</span></span>   
    - <span data-ttu-id="77ef9-181">Praktika- ja projektijuht, kasutaja täisnimi = "Spencer Low"</span><span class="sxs-lookup"><span data-stu-id="77ef9-181">User Fullname="Spencer Low" as Practice and Project Manager</span></span>  
    - <span data-ttu-id="77ef9-182">Meeskonnaliige, kasutaja täisnimi = "Veronica Quek"</span><span class="sxs-lookup"><span data-stu-id="77ef9-182">User Fullname="Veronica Quek" as Team Member</span></span>   
    - <span data-ttu-id="77ef9-183">Kasutaja täisnimi = "William Jõgi"</span><span class="sxs-lookup"><span data-stu-id="77ef9-183">User Fullname="William Contoso"</span></span>
  
2. <span data-ttu-id="77ef9-184">Demoandmete importimiseks määrake ülaltoodud kuuele kasutajale administraatori roll, et näidiskirjed õigesti imporditaks.</span><span class="sxs-lookup"><span data-stu-id="77ef9-184">For the purposes of demo data import, assign the six users above the Administrator role so sample records import correctly.</span></span> 

3. <span data-ttu-id="77ef9-185">Avage **PkgFolder** ning otsige üles ja avage fail **ImportUserMapFile.xml**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-185">Open **PkgFolder** and then find and open **ImportUserMapFile.xml**.</span></span> <span data-ttu-id="77ef9-186">Värskendage väljad **New=** süsteemis vastavate kasutajate meiliaadressidega.</span><span class="sxs-lookup"><span data-stu-id="77ef9-186">Update the **New=** fields to the email addresses of corresponding Users in your system.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="77ef9-187">![UserMapFile’i kuvatõmmis](media/sample-data-7.png)</span><span class="sxs-lookup"><span data-stu-id="77ef9-187">![Screen shot of UserMapFile](media/sample-data-7.png)</span></span>

4. <span data-ttu-id="77ef9-188">Kui kasutajal täisnimega Spencer Low on muu kasutaja ID kui **"spencerl"**, peate värskendama täiendavat faili.</span><span class="sxs-lookup"><span data-stu-id="77ef9-188">If your "Spencer Low" full name user has a different user ID than **"spencerl"**, then you need to update an additional file.</span></span> <span data-ttu-id="77ef9-189">Avage fail **DemoDataPreImportConfig.xml** ja otsige üles silt **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-189">Open **DemoDataPreImportConfig.xml** and find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="77ef9-190">Värskendage silti **\<sisselogimine\>** sisselogimise ID-ga (tõstutundlik).</span><span class="sxs-lookup"><span data-stu-id="77ef9-190">Update the **\<login\>** tag with the loginId (case-sensitive).</span></span> 

5. <span data-ttu-id="77ef9-191">Esimese kasutaja kalendrit (sildil **userstocreateandconfigure**) kasutatakse kõikide broneeritavate ressursside tööaja väljade täitmiseks demoandmete importimisel.</span><span class="sxs-lookup"><span data-stu-id="77ef9-191">The first user's calendar (in the **userstocreateandconfigure** tag) is used to populate the work hours for all bookable resources on import of demo data.</span></span> <span data-ttu-id="77ef9-192">Valige **Sätted** > **Turve** > **Kasutajad**, otsige üles kasutaja Spencer Low ja avage suvand Tööaeg.</span><span class="sxs-lookup"><span data-stu-id="77ef9-192">Navigate to **Settings** > **Security** > **Users**, find your "Spencer Low" user, and open the "Work Hours" option.</span></span> <span data-ttu-id="77ef9-193">Muutke tööaega, valides suvandi **Terve korduv nädalaajakava algusest lõpuni**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-193">Edit the existing work hours, selecting the **Entire recurring weekly schedule from start to end** option.</span></span> <span data-ttu-id="77ef9-194">Kontrollige, kas **tööaeg on 8.00–17.00 (9 tundi), esmaspäevast reedeni, ja ajavöönd on määratud Vaikse ookeani ajale (USA ja Kanada)**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-194">Ensure the **Work hours are set to 8 AM - 5 PM (9 Hours), Monday to Friday and with the Timezone set to Pacific Time (US & Canada)**.</span></span> <span data-ttu-id="77ef9-195">Seda on vaja projekti- ja ajakavapaneeli õigesti kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="77ef9-195">This is needed to ensure that the Project and Schedule board show as expected.</span></span>

<span data-ttu-id="77ef9-196">**Soovitus.** Kaaluge organisatsioonist varukoopia loomist juhuks, kui peate minema tagasi lähtekohta, kui näidisandmete installimisel midagi valesti läheb.</span><span class="sxs-lookup"><span data-stu-id="77ef9-196">**Recommendation:** Consider creating a backup of your org now, in case you need to revert to your starting point if something goes wrong during the sample data installation.</span></span> <span data-ttu-id="77ef9-197">Lisateavet vt teemast [Eksemplaride varundamine ja taastamine](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span><span class="sxs-lookup"><span data-stu-id="77ef9-197">For more information, see [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span></span>

## <a name="run-the-package-deployer"></a><span data-ttu-id="77ef9-198">Käivitage Package Deployer</span><span class="sxs-lookup"><span data-stu-id="77ef9-198">Run the Package Deployer</span></span>

1. <span data-ttu-id="77ef9-199">Otsige üles ja käivitage fail **PackageDeployer.exe** kaustas **v902FPSMasterData** VÕI **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-199">Find and run **PackageDeployer.exe** in the **v902FPSMasterData** OR **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="77ef9-200">Nõustuge nõuete ja tingimustega.</span><span class="sxs-lookup"><span data-stu-id="77ef9-200">Accept the terms and conditions.</span></span>

3. <span data-ttu-id="77ef9-201">Järgmises aknas</span><span class="sxs-lookup"><span data-stu-id="77ef9-201">On the next window:</span></span>

   <span data-ttu-id="77ef9-202">a.</span><span class="sxs-lookup"><span data-stu-id="77ef9-202">a.</span></span> <span data-ttu-id="77ef9-203">Valige juurutustüübiks **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-203">Select deployment type **Office 365**.</span></span>

   <span data-ttu-id="77ef9-204">b.</span><span class="sxs-lookup"><span data-stu-id="77ef9-204">b.</span></span> <span data-ttu-id="77ef9-205">Kasutage jaotises „Create or configure users” kasutaja konfigureeritud süsteemiadministraatori kasutajanime ja parooli (kasutaja Spencer Low kasutajanimi spencerl).</span><span class="sxs-lookup"><span data-stu-id="77ef9-205">Use the user and password of the system administrator user configured in "Create or configure users" ("Spencer Low" with "spencerl" username).</span></span>

   <span data-ttu-id="77ef9-206">c.</span><span class="sxs-lookup"><span data-stu-id="77ef9-206">c.</span></span> <span data-ttu-id="77ef9-207">Veenduge, et valitud oleks suvand **Saadaolevate organisatsioonide loendi kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-207">Make sure **Display list of available organizations** is selected.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="77ef9-208">![Kuvatõmmis aknast Package Deployer – valitud suvand Saadaolevate organisatsioonide loendi kuvamine](media/sample-data-2.png)</span><span class="sxs-lookup"><span data-stu-id="77ef9-208">![Screenshot of Package Deployer window with "Display list of available organizations" selected](media/sample-data-2.png)</span></span>

4. <span data-ttu-id="77ef9-209">Valige organisatsioon, kuhu soovite näidisandmed installida.</span><span class="sxs-lookup"><span data-stu-id="77ef9-209">Select the organization where you want to install the sample data.</span></span>

5. <span data-ttu-id="77ef9-210">Valige nupp **Edasi**, kuni näete dialoogi **Demoandmete seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-210">Select **Next** until you see the **Demo Data Setup** dialog.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="77ef9-211">![Demoandmete installija olekuakna kuvatõmmis](media/sample-data-3.png)</span><span class="sxs-lookup"><span data-stu-id="77ef9-211">![Screenshot of the demo data installer status window](media/sample-data-3.png)</span></span>

6. <span data-ttu-id="77ef9-212">Enne jätkamist pange tähele, et näidisandmete installimine võib kesta kuni ühe tunni (tavaliselt ~10 minutit).</span><span class="sxs-lookup"><span data-stu-id="77ef9-212">Before proceeding, note that installing sample data could take up to one hour (normally ~10 minutes).</span></span> <span data-ttu-id="77ef9-213">Peate veenduma, et arvuti oleks kogu installimisprotsessi aja sees ja võrku ühendatud ning seanss oleks pidevalt aktiivne.</span><span class="sxs-lookup"><span data-stu-id="77ef9-213">You'll need to make sure the computer remains on and connected to a network throughout the installation process, and that your session remains active.</span></span>   

7. <span data-ttu-id="77ef9-214">Kui olete valmis, klõpsake nuppu **Edasi**, et alustada näidisandmete installimisega.</span><span class="sxs-lookup"><span data-stu-id="77ef9-214">When you're ready, click **Next** to start the sample data installation process.</span></span> <span data-ttu-id="77ef9-215">Pärast näidisandmete laadimist klõpsake nuppu **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-215">After the sample data is loaded, click **Finish**.</span></span>

## <a name="verify-the-sample-data-installation"></a><span data-ttu-id="77ef9-216">Näidisandmete installimise kontrollimine</span><span class="sxs-lookup"><span data-stu-id="77ef9-216">Verify the sample data installation</span></span>

<span data-ttu-id="77ef9-217">Õigsuse kontrollimiseks kontrollige, kas ettevõtte Fabrikam Robotics väljamõeldud stsenaariumis loendatud kirjete arv ja üksuste tüübid kuvatakse ootuspäraselt.</span><span class="sxs-lookup"><span data-stu-id="77ef9-217">For a sanity check, verify that the number of records and types of entities listed in Fabrikam Robotics fictitious scenario appear as expected.</span></span>

<span data-ttu-id="77ef9-218">Kui näidisandmed on täielikult laaditud, logige sisse kasutajana Spencer Low ja kinnitage järgmist.</span><span class="sxs-lookup"><span data-stu-id="77ef9-218">After the sample data completely loads, sign in as the Spencer Low user and confirm the following:</span></span>

- <span data-ttu-id="77ef9-219">Kui installitud on Project Service’i rakendus, valige suvandid **Project Service** > **Sätted** > **Hinnakirjad**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-219">If the Project Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="77ef9-220">Kinnitage, et andmekogumis oleks olemas iga riigi/piirkonna jaoks sobivas valuutas arveldus- ja kulumäärad.</span><span class="sxs-lookup"><span data-stu-id="77ef9-220">Confirm that bill rates and costs rates exist with the appropriate currency for each country/region in the data set.</span></span>

- <span data-ttu-id="77ef9-221">Kui Project Service’i rakendus on installitud, valige suvandid **Universal Resource Scheduling** > **Sätted** > **Organisatsiooniüksused**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-221">If the Project Service application is installed, go to **Universal Resource Scheduling** > **Settings** > **Organizational Units**.</span></span> <span data-ttu-id="77ef9-222">Kinnitage, et iga organisatsiooniüksusega (v.a linnakirjed) oleks seotud sobivas valuutas omahindade loend.</span><span class="sxs-lookup"><span data-stu-id="77ef9-222">Confirm that a cost price list with the appropriate currency has been associated with each org unit (excluding city entries).</span></span> <span data-ttu-id="77ef9-223">Kui mõni on puudu, otsige üles ja seostage õige omahindade loend.</span><span class="sxs-lookup"><span data-stu-id="77ef9-223">If any are missing, find and associate the correct cost price list.</span></span>

- <span data-ttu-id="77ef9-224">Kui Field Service’i rakendus on installitud, valige suvandid **Project Service** > **Sätted** > **Hinnakirjad**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-224">If the Field Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="77ef9-225">Kinnitage, et olemas oleks arveldus- ja kulumäärad.</span><span class="sxs-lookup"><span data-stu-id="77ef9-225">Confirm that bill rates and costs rates exist.</span></span> <span data-ttu-id="77ef9-226">Valige **Field Service** > **Sätted** > **Hinnakirjad** ning kontrollige, et andmekogumis oleks olemas iga riigi/piirkonna jaoks sobivas valuutas arveldus- ja kulumäärad.</span><span class="sxs-lookup"><span data-stu-id="77ef9-226">Go to **Field Service** > **Settings** > **Price Lists** and check that bill rates and costs rates exist, with the appropriate currency, for each country/region in the data set.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="77ef9-227">![Aktiivsete hinnakirjade kuvatõmmis](media/sample-data-4.png)</span><span class="sxs-lookup"><span data-stu-id="77ef9-227">![Screenshot of active price lists](media/sample-data-4.png)</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="77ef9-228">![Aktiivsete organisatsiooniüksuste kuvatõmmis](media/sample-data-5.png)</span><span class="sxs-lookup"><span data-stu-id="77ef9-228">![Screenshot of active organizational units](media/sample-data-5.png)</span></span>

## <a name="technical-notes"></a><span data-ttu-id="77ef9-229">Tehnilised märkused</span><span class="sxs-lookup"><span data-stu-id="77ef9-229">Technical notes</span></span>

<span data-ttu-id="77ef9-230">Nende andmete tehniliste üksikasjade nägemiseks vaadake teavet allpool.</span><span class="sxs-lookup"><span data-stu-id="77ef9-230">See below for more technical details on the installation of this data.</span></span>

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a><span data-ttu-id="77ef9-231">Näidisandmete installimine lisaks olemasolevatele andmetele (pole soovitatav)</span><span class="sxs-lookup"><span data-stu-id="77ef9-231">Installing sample data on top of existing data (not recommended)</span></span>

<span data-ttu-id="77ef9-232">Kui peate installima näidisandmed lisaks olemasolevale Field Service’i või Project Service’i proovi- või demokeskkonnale, milles juba on andmeid, peate seiskama installija tehtavad ohutuse kontrollid.</span><span class="sxs-lookup"><span data-stu-id="77ef9-232">If you need to install sample data on top of an existing Field Service or Project Service trial or demo environment that already has data, you'll need to suspend the safety prechecks performed by the installer.</span></span>

<span data-ttu-id="77ef9-233">Selleks minge kausta **PkgFolder** ning otsige üles ja avage fail **DemoDataPreImportConfig.xml** Notepadis (või muus XML-redaktoris).</span><span class="sxs-lookup"><span data-stu-id="77ef9-233">To do this, go to the **PkgFolder** folder to find and open the **DemoDataPreImportConfig.xml** file with Notepad (or another XML editor).</span></span>

<span data-ttu-id="77ef9-234">Otsige üles järgmine väärtus ja muutke säte õigest valeks.</span><span class="sxs-lookup"><span data-stu-id="77ef9-234">Find the following value, and then change the setting from true to false:</span></span>

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

<span data-ttu-id="77ef9-235">Selle muudatuse tõttu jätab installija vahele mõned olulised ohutuskontrolli, sh järgmised.</span><span class="sxs-lookup"><span data-stu-id="77ef9-235">This change causes the installer to bypass some important safety checks, including:</span></span>

- <span data-ttu-id="77ef9-236">Kinnitamine, et pole rohkem kui üks aktiivne kirje **Organisatsiooniüksus**, ja sellele nime **Fabrikam US** andmine.</span><span class="sxs-lookup"><span data-stu-id="77ef9-236">Confirming that there is no more than one active **Organizational Unit** record, and then renaming it to **Fabrikam US**.</span></span>

- <span data-ttu-id="77ef9-237">Kinnitamine, et pole rohkem kui üks aktiivne kirje **Töömall**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-237">Confirming that there is no more than one active **Work Template** record.</span></span>

- <span data-ttu-id="77ef9-238">Kinnitamine, et pole rohkem kui üks aktiivne kirje **Projekti parameeter**, ja sellele kandele nime **Parameetrid** andmine.</span><span class="sxs-lookup"><span data-stu-id="77ef9-238">Confirming that there is no more than one active **Project Parameter** record, and then renaming that entry to **Parameters**.</span></span>

### <a name="configuration-components"></a><span data-ttu-id="77ef9-239">Konfiguratsioonikomponendid</span><span class="sxs-lookup"><span data-stu-id="77ef9-239">Configuration components</span></span>

<span data-ttu-id="77ef9-240">Selles eelnevalt imporditud konfiguratsioonifailis on hulk muid konfiguratsioonikomponente.</span><span class="sxs-lookup"><span data-stu-id="77ef9-240">There are a number of other configuration components in this pre-import configuration file.</span></span> <span data-ttu-id="77ef9-241">Tehniliste kasutajate korral on osa neist järgmised.</span><span class="sxs-lookup"><span data-stu-id="77ef9-241">For technical users, some of these include:</span></span>

- <span data-ttu-id="77ef9-242">**\<RequiredSolutions\>** määrab eeltingimuse lahenduse installid ja nende versiooninumbrid.</span><span class="sxs-lookup"><span data-stu-id="77ef9-242">**\<RequiredSolutions\>** specifies prerequisite solution installations and their version numbers.</span></span>

- <span data-ttu-id="77ef9-243">**\<InstallSampleData\>** kontrollib, kas kasutusvalmis näidisandmed on rakenduse jaoks installitud.</span><span class="sxs-lookup"><span data-stu-id="77ef9-243">**\<InstallSampleData\>** controls whether out-of-the-box sample data for the apps is installed.</span></span>

    - <span data-ttu-id="77ef9-244">väär – jätab nende sisseehitatud andmete (mis on eemaldatavad) installimise vahele</span><span class="sxs-lookup"><span data-stu-id="77ef9-244">false - skips installation of this built-in data (which is removable)</span></span>

    - <span data-ttu-id="77ef9-245">tõene – installib sisseehitatud andmed koos FS-i ja PSA näidisandmete installimisega</span><span class="sxs-lookup"><span data-stu-id="77ef9-245">true - installs the built-in data concurrent with installation of the FS and PSA sample data</span></span>

- <span data-ttu-id="77ef9-246">**\<PreImportDataCollection\>** määrab lamefaili andmekaardid ja seostatud kirjed, mis imporditakse enne peamiste näidisandmete installimist.</span><span class="sxs-lookup"><span data-stu-id="77ef9-246">**\<PreImportDataCollection\>** specifies flat-file Data Maps and associated Records to be imported ahead of the main sample data installation.</span></span>

- <span data-ttu-id="77ef9-247">**\<EntitiesToEnableScheduling\>** määrab, millised olemid tuleks broneerimiseks lubada rakenduses Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span><span class="sxs-lookup"><span data-stu-id="77ef9-247">**\<EntitiesToEnableScheduling\>** specifies which entities should be enabled for Booking in Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span></span>

- <span data-ttu-id="77ef9-248">**\<UsersToCreateAndConfigure\>** määrab broneeritavad ressursid, mis luuakse (kui neid veel pole) enne näidisandmete importimist.</span><span class="sxs-lookup"><span data-stu-id="77ef9-248">**\<UsersToCreateAndConfigure\>** specifies Bookable Resources that will be created (if they don't exist already) before the sample data import executes.</span></span> <span data-ttu-id="77ef9-249">Pange tähele, et lähtesüsteemi näidisandmete broneeritav ressurss ühtib sihtsüsteemi broneeritava ressursi kirjetega iga ressursi täieliku nime ja sisselogimisandmete osas.</span><span class="sxs-lookup"><span data-stu-id="77ef9-249">Note that the source system sample data Bookable Resource match with the target system Bookable Resource records on the FullName and login of each resource.</span></span> <span data-ttu-id="77ef9-250">Seega EI OLE võimalik selles eelkonfiguratsioonifailis nimesid muuta, kui te ei impordi kõigepealt näidisandmeid sihtsüsteemi, kasutades neid nimesid, seejärel nimetate broneeritavad ressursid ümber sobiva nimega, mis on määratud koos lubatud kasutaja kirjetega, ja seejärel ekspordite andmed uuesti importimiseks lõplikku sihtsüsteemi (värskendades vastavalt faili **ImportUserMapFile.xml** vanu ja uusi kirjeid).</span><span class="sxs-lookup"><span data-stu-id="77ef9-250">Therefore, it is NOT possible to change the names in this preconfiguration file unless you first import sample data into a target system using these names, then rename the Bookable Resources to your desired name set along with the Enabled User records, and then export the data again for import into your final destination system (updating the **ImportUserMapFile.xml** Old and New entries accordingly).</span></span>

- <span data-ttu-id="77ef9-251">**\<PluginsToDisable\>** määrab väga diskreetsed rea kauba lisandmoodulid, mis tuleb näidisandmete importimisel keelata ja seejärel hiljem uuesti lubada.</span><span class="sxs-lookup"><span data-stu-id="77ef9-251">**\<PluginsToDisable\>** specifies very discrete line-item plug-ins that must be disabled during the sample data import and then reenabled afterwards.</span></span>

### <a name="fabrikam-robotics-fictitious-scenario"></a><span data-ttu-id="77ef9-252">Ettevõtte Fabrikam Robotics väljamõeldud stsenaarium</span><span class="sxs-lookup"><span data-stu-id="77ef9-252">Fabrikam Robotics fictitious scenario</span></span>

<span data-ttu-id="77ef9-253">Field Service’i ja Project Service’i viiteandmete näidispaketid installivad **lahenduse Fabrikam Manufacturing Master Data (v3.0.0.0)** koos umbes 4000 kirjega ja umbes 40 eri üksusega.</span><span class="sxs-lookup"><span data-stu-id="77ef9-253">The Field Service and Project Service sample reference data packages install the **Fabrikam Manufacturing Master Data (v3.0.0.0) solution**, along with approximately 4,000 records and approximately 40 different entities.</span></span> <span data-ttu-id="77ef9-254">Field Service’i või Project Service’i eraldi näidisandmete paketid sisaldavad selle rakenduse näidisandmete **v902FPSMasterData** alamkogumit.</span><span class="sxs-lookup"><span data-stu-id="77ef9-254">The separate sample data packages for Field Service or Project Service contain a subset of the **v902FPSMasterData** sample data for that application.</span></span> <span data-ttu-id="77ef9-255">**Demoandmete** pakett installib **lahenduse Fabrikam Manufacturing Demo Data (v3.0.0.7)** umbes 22 000 kirjega 148 üksuses.</span><span class="sxs-lookup"><span data-stu-id="77ef9-255">The **Demo Data** package installs the **Fabrikam Manufacturing Demo Data (v3.0.0.7) solution** with approximately 22,000 records across 148 entities.</span></span>

<span data-ttu-id="77ef9-256">Väljamõeldud ettevõte Fabrikam Robotics toodab elektroonikaseadme koosteliini roboteid ja on tuntud oma toodete kvaliteedi, uuendusmeelsuse ning tugeva klienditeeninduse poolest, sh installimiste planeerimine, rakendamine ja jooksvad hooldusteenused.</span><span class="sxs-lookup"><span data-stu-id="77ef9-256">The fictional company, Fabrikam Robotics, is a manufacturer of electronic device assembly line robots and is known for their product quality, innovation, and solid customer service, including installation planning, implementation, and ongoing maintenance services.</span></span> <span data-ttu-id="77ef9-257">Fabrikami peakorter asub Ameerika Ühendriikides (Fabrikam US) ja sellel on neli projektipõhist teenusetoimingut Prantsusmaal, Indias, Ühendkuningriigis ja Šveitsis.</span><span class="sxs-lookup"><span data-stu-id="77ef9-257">Fabrikam is headquartered in the United States (Fabrikam US), and has project-based service operations in France, India, the United Kingdom, and Switzerland.</span></span>

<span data-ttu-id="77ef9-258">Väliteeninduse toimingud on koondunud Ühendriikidesse, peamiselt Seattle’i piirkonda.</span><span class="sxs-lookup"><span data-stu-id="77ef9-258">Field service operations are centered in the United States, mostly in the greater Seattle area.</span></span> <span data-ttu-id="77ef9-259">Ettevõte keskendub asjade Interneti (IoT) connectivity parandamisele, et jälgida kliendi vara jõudlust ja pakkuda üha rohkem ennetavat kohapealset hooldust.</span><span class="sxs-lookup"><span data-stu-id="77ef9-259">The company is focused on leveraging Internet of Things (IoT) connectivity to monitor customer asset performance and deliver increasingly proactive onsite services.</span></span>

<span data-ttu-id="77ef9-260">Näidisandmete põhjalik ülevaade on järgmine.</span><span class="sxs-lookup"><span data-stu-id="77ef9-260">A high-level overview of the sample data is as follows:</span></span>

- <span data-ttu-id="77ef9-261">Üldised näidisandmete elemendid (lisatud mõlema rakenduse jaoks)</span><span class="sxs-lookup"><span data-stu-id="77ef9-261">Common sample data elements (included for both applications)</span></span>

    - <span data-ttu-id="77ef9-262">1 kasutaja</span><span class="sxs-lookup"><span data-stu-id="77ef9-262">1 user</span></span>

    - <span data-ttu-id="77ef9-263">71 kontot</span><span class="sxs-lookup"><span data-stu-id="77ef9-263">71 accounts</span></span>

    - <span data-ttu-id="77ef9-264">137 kontakti</span><span class="sxs-lookup"><span data-stu-id="77ef9-264">137 contacts</span></span>

    - <span data-ttu-id="77ef9-265">Mitmesugused kandetüübid ja -kategooriad</span><span class="sxs-lookup"><span data-stu-id="77ef9-265">Various transaction types and categories</span></span>

    - <span data-ttu-id="77ef9-266">50 toodet 1 toote hinnakirjaga</span><span class="sxs-lookup"><span data-stu-id="77ef9-266">50 products with 1 product price list</span></span>

    - <span data-ttu-id="77ef9-267">14 hinna-/kulukirja</span><span class="sxs-lookup"><span data-stu-id="77ef9-267">14 price/cost lists</span></span>

    - <span data-ttu-id="77ef9-268">31 näitajat (ressursioskused) 2 hindamismudelis 3 tasemega (hindamisväärtused)</span><span class="sxs-lookup"><span data-stu-id="77ef9-268">31 characteristics (resource skills) in 2 rating models with 3 levels (rating values)</span></span>

- <span data-ttu-id="77ef9-269">Project Service</span><span class="sxs-lookup"><span data-stu-id="77ef9-269">Project Service</span></span>

    - <span data-ttu-id="77ef9-270">8 organisatsiooniüksust</span><span class="sxs-lookup"><span data-stu-id="77ef9-270">8 organizational units</span></span>

    - <span data-ttu-id="77ef9-271">6 rollipõhist kasutustaset</span><span class="sxs-lookup"><span data-stu-id="77ef9-271">6 role-specific utilization levels</span></span>

    - <span data-ttu-id="77ef9-272">Üle 2800 rolli-hinna spetsifikatisooni</span><span class="sxs-lookup"><span data-stu-id="77ef9-272">2.8k+ role-price specifications</span></span>

- <span data-ttu-id="77ef9-273">Field Service</span><span class="sxs-lookup"><span data-stu-id="77ef9-273">Field Service</span></span>

    - <span data-ttu-id="77ef9-274">4 territooriumi</span><span class="sxs-lookup"><span data-stu-id="77ef9-274">4 territories</span></span>

    - <span data-ttu-id="77ef9-275">5 töökäsu tüüpi</span><span class="sxs-lookup"><span data-stu-id="77ef9-275">5 work order types</span></span>

    - <span data-ttu-id="77ef9-276">22 kliendivara</span><span class="sxs-lookup"><span data-stu-id="77ef9-276">22 customer assets</span></span>

    - <span data-ttu-id="77ef9-277">9 juhtumi tüüpi valiku seotud ressursi näitajate (9), teenuste (13) ja hooldustoimingutega (13)</span><span class="sxs-lookup"><span data-stu-id="77ef9-277">9 incident types with a range of associated resource characteristics (9), services (13) and service tasks (13)</span></span>
   
<span data-ttu-id="77ef9-278">**Demoandmete** pakett installib umbes 179 töökäsku, 12 projekti ja seotud tehingu andmed.</span><span class="sxs-lookup"><span data-stu-id="77ef9-278">The **Demo Data** package installs approximately 179 work orders, 12 projects, and associated transactional data.</span></span> 

### <a name="change-the-work-hours-for-sample-resources"></a><span data-ttu-id="77ef9-279">Näidisressursside töötundide muutmine</span><span class="sxs-lookup"><span data-stu-id="77ef9-279">Change the work hours for sample resources</span></span>

<span data-ttu-id="77ef9-280">Vaikimisi on kõigil broneeritavatel ressurssidel 24-tunnine töökalender.</span><span class="sxs-lookup"><span data-stu-id="77ef9-280">By default, all bookable resources have a 24 work hours calendar.</span></span>

<span data-ttu-id="77ef9-281">Kui peate muutma broneeritava näidisressursi töötunde, valige **Universal Resource Scheduling** > **Plaanimine** > **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-281">If you need to change the work hours for sample bookable resources, go to **Universal Resource Scheduling** > **Scheduling** > **Resources**.</span></span>

<span data-ttu-id="77ef9-282">Valige kasutaja (nt Spencer Low) ja muutke tema töötunnid tundidele, mida soovite rakendada mitmele kasutajale.</span><span class="sxs-lookup"><span data-stu-id="77ef9-282">Select a user (for example, Spencer Low) and change Spencer's work hours to the hours you want to apply to multiple users.</span></span> <span data-ttu-id="77ef9-283">Valige **Universal Resource Scheduling** > **Sätted** > **Töötundide mallid** ja muutke kirjet **Vaikimisi töömall**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-283">Go to **Universal Resource Scheduling** > **Settings** > **Work Hour Templates** and edit the **Default Work Template** record.</span></span> <span data-ttu-id="77ef9-284">Väljas **Malli ressurss** valige kasutaja töötundidega, mida soovite rakendada teistele ressurssidele.</span><span class="sxs-lookup"><span data-stu-id="77ef9-284">In the **Template Resource** field, select a user with work hours that you want to apply to other resources.</span></span> <span data-ttu-id="77ef9-285">Valige **Universal Resource Scheduling** > **Plaanimine** > **Ressursid** > **Aktiivsed broneeritavad ressursid**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-285">Go to **Universal Resource Scheduling** > **Scheduling** > **Resources** > **Active Bookable Resources**.</span></span> <span data-ttu-id="77ef9-286">Valige ressursid, mida soovite muuta, ja seejärel valige suvand **Kalendri määramine**.</span><span class="sxs-lookup"><span data-stu-id="77ef9-286">Select the resources you want to change, and then select **Set Calendar**.</span></span> <span data-ttu-id="77ef9-287">Ripploendist **Töömall** valige mall **Vaikimisi töötund** või muu õige ressursiga mall.</span><span class="sxs-lookup"><span data-stu-id="77ef9-287">On the **Work Template** drop-down list, select the **Default Work Hour** template or another template with the correct templating resource.</span></span> <span data-ttu-id="77ef9-288">Kui lähete plaanimistahvlile, peaksite nägema, et ressursside töötunde on nüüd värskendatud.</span><span class="sxs-lookup"><span data-stu-id="77ef9-288">When you go to the schedule board, you should see that the resources now have updated work hours.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="77ef9-289">![Aktiivsete broneeritavate ressursside kuvatõmmis](media/sample-data-6.png)</span><span class="sxs-lookup"><span data-stu-id="77ef9-289">![Screenshot of active bookable resources](media/sample-data-6.png)</span></span>
