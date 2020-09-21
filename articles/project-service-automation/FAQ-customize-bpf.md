---
title: Kuidas ma saan projekti etappide äriprotsessi vooge kohandada?
description: Ülevaade, kuidas projekti etappide äriprotsessi vooge kohandada.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: 36f7df9e-117d-4f85-af4b-d842e93321bd
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d4b99f67e929ebcd1a684bcd1124756140107d17
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750920"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="e10de-103">Kuidas ma saan projekti etappide äriprotsessi vooge kohandada?</span><span class="sxs-lookup"><span data-stu-id="e10de-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="e10de-104">Rakenduse Project Service varasemates versioonides on teadaolev piirang, et projekti etappide äriprotsessi voos peavad etappide nimed täpselt ühtima oodatud ingliskeelsete nimedega (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="e10de-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="e10de-105">Vastasel korral ei tööta ingliskeelsetel etapinimedel tuginev äriloogika korrapäraselt.</span><span class="sxs-lookup"><span data-stu-id="e10de-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="e10de-106">Seetõttu ei näe te projekti vormil tuttavaid toiminguid nagu **Vaheta protsessi** või **Redigeeri protsessi**.</span><span class="sxs-lookup"><span data-stu-id="e10de-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="e10de-107">Selle piiranguga tegeleti versioonis 2.4.5.48 ja hilisemates.</span><span class="sxs-lookup"><span data-stu-id="e10de-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="e10de-108">Selles artiklis pakutakse võimalikke lahendusi, kui teil on vaja kohandada varasemate versioonide äriprotsessi voo vaikevariante.</span><span class="sxs-lookup"><span data-stu-id="e10de-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="e10de-109">Äriloogika vajab ingliskeelsete etapinimedega täpselt ühtimist</span><span class="sxs-lookup"><span data-stu-id="e10de-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="e10de-110">Projekti etappide äriprotsessi voog sisaldab äriloogikat, mis juhib rakenduses järgmisi käitumisi.</span><span class="sxs-lookup"><span data-stu-id="e10de-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="e10de-111">Kui projekt on seotud pakkumisega, siis määrab kood äriprotsessi voo etapile **Quote** (Pakkumine).</span><span class="sxs-lookup"><span data-stu-id="e10de-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="e10de-112">Kui projekt on seotud lepinguga, siis määrab kood äriprotsessi voo etapile **Plan** (Plaan).</span><span class="sxs-lookup"><span data-stu-id="e10de-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="e10de-113">Kui äriprotsessi voog liigutatakse etappi **Close** (Sulgemine), siis desaktiveeritakse projekti kirje.</span><span class="sxs-lookup"><span data-stu-id="e10de-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="e10de-114">Kui projekt desaktiveeritakse, siis seatakse projekti vorm ja tööjaotuse struktuur (WBS) kirjutuskaitstud olekusse, väljastatakse nimega ressursi reserveeringud ning desaktiveeritakse kõik seostatud hinnakirjad.</span><span class="sxs-lookup"><span data-stu-id="e10de-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="e10de-115">See äriloogika tugineb ingliskeelsetel projekti etappide nimedel.</span><span class="sxs-lookup"><span data-stu-id="e10de-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="e10de-116">Ingliskeelsetest etappide nimedest sõltumine on peamine põhjus, miks ei julgustata projekti etappide äriprotsessi voo kohandamist, ja miks te ei näe projekti üksuses tavapäraseid ärivoo toiminguid nagu **Vaheta protsessi** ega **Redigeeri protsessi**.</span><span class="sxs-lookup"><span data-stu-id="e10de-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="e10de-117">Mis juhtub, kui etapi nimed ei ühti ingliskeelsete nimedega?</span><span class="sxs-lookup"><span data-stu-id="e10de-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="e10de-118">Rakenduse Project Service versioon 1.x platvormil 8.2 – kui äriprotsessi voo etappide nimed ei ühti täpselt ingliskeelsete nimedega, siis äriloogika, mis määrab pakkumistele või lepingutele õige etapi või sulgeb need, jäetakse vahele.</span><span class="sxs-lookup"><span data-stu-id="e10de-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="e10de-119">Tõrketeadet ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="e10de-119">No error messages are displayed.</span></span> <span data-ttu-id="e10de-120">Seetõttu näib, nagu saaksite kohandada projekti etappide äriprotsessi vooge.</span><span class="sxs-lookup"><span data-stu-id="e10de-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="e10de-121">Kuid ükski automaatne protsess ei tööta pakkumiste, lepingute ega projektide sulgemiste jaoks.</span><span class="sxs-lookup"><span data-stu-id="e10de-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="e10de-122">Rakenduse Project Service versioonis 2.4.4.30 platvormil 9.0 muudeti äriprotsessi voogude arhitektuuri põhjalikult, mistõttu tuli ümber kirjutada äriprotsessi voo äriloogika.</span><span class="sxs-lookup"><span data-stu-id="e10de-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="e10de-123">Selle tulemusena kuvatakse teile tõrketeade, kui protsessi etappide nimed ei ühti oodatud ingliskeelsete nimedega.</span><span class="sxs-lookup"><span data-stu-id="e10de-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="e10de-124">Seega, kui soovite projekti üksuse jaoks kohandada projekti etappide äriprotsessi vooge, saate projekti üksuse äriprotsessi voo vaikevariandile lisada vaid täiesti uusi etappe, säilitades etappe **Quote** (Pakkumine), **Plan** (Plaan) ja **Close** (Sulgemine) oma esialgsetel kujudel.</span><span class="sxs-lookup"><span data-stu-id="e10de-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="e10de-125">See piirang tagab, et teil ei esine tõrkeid äriloogikas, mis ootab äriprotsessi voost ingliskeelseid etappide nimesid.</span><span class="sxs-lookup"><span data-stu-id="e10de-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="e10de-126">Versioonis 2.4.5.48 või hilisemas on selles artiklis kirjeldatud äriloogika projekti üksuse äriprotsessi voo vaikevariandist eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="e10de-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="e10de-127">Sellele või uuemale versioonile täiendamine võimaldab teil äriprotsessi voo vaikevarianti kohandada või enda omaga asendada.</span><span class="sxs-lookup"><span data-stu-id="e10de-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="e10de-128">Lahendused varasematele versioonidele</span><span class="sxs-lookup"><span data-stu-id="e10de-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="e10de-129">Kui täiendamine pole võimalik, saate projekti üksuse äriprotsessi voo projekti etappe kohandada kahel järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="e10de-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="e10de-130">Lisage vaikekonfiguratsioonile lisaetappe, säilitades ingliskeelsed nimetused etappidele **Quote** (Pakkumine), **Plan** (Plaan) ja **Close** (Sulgemine).</span><span class="sxs-lookup"><span data-stu-id="e10de-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="e10de-131">![Kuvatõmmis vaikekonfiguratsioonile etappide lisamisest](media/FAQ-Customize-BPF-1.png)</span><span class="sxs-lookup"><span data-stu-id="e10de-131">![Screenshot of adding stages to default configuration](media/FAQ-Customize-BPF-1.png)</span></span>
 
2. <span data-ttu-id="e10de-132">Looge oma äriprotsessi voog ja muutke see projekti üksuse jaoks peamiseks äriprotsessi vooks – see võimaldab teil etappide jaoks soovitud nimesid kasutada.</span><span class="sxs-lookup"><span data-stu-id="e10de-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="e10de-133">Siiski, kui soovite kasutada samu standardseid projekti etappe **Quote** (Pakkumine), **Plan** (Plaan) ja **Close** (Sulgemine), siis peate tegema kohandusi, mis põhinevad teie kohandatud etappide nimedel.</span><span class="sxs-lookup"><span data-stu-id="e10de-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="e10de-134">Keerukam loogika on projekti sulgemises, mille saate ikkagi käivitada, kui desaktiveerite projekti kirje.</span><span class="sxs-lookup"><span data-stu-id="e10de-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="e10de-135">![Kuvatõmmis BPF-i kohandamisest](media/FAQ-Customize-BPF-2.png)</span><span class="sxs-lookup"><span data-stu-id="e10de-135">![Screenshot of BPF customization](media/FAQ-Customize-BPF-2.png)</span></span>

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="e10de-136">Muud tähelepanekud rakenduse Project Service versiooni 2.4.4.30 või varasema kohta platvormil 9.0</span><span class="sxs-lookup"><span data-stu-id="e10de-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="e10de-137">Rakenduse Project Service versioonis 2.4.4.30 või varasemas platvormil 9.0 ei värskendata kohandatud äriprotsessi voo puhul projekti üksuse välja **Projekti nimi**, mida kasutatakse tabelis **Projektid etappide järgi** ja projekti loendi vaadetes, sest see väli on seotud projekti etappide äriprotsessi voo vaikevariandiga.</span><span class="sxs-lookup"><span data-stu-id="e10de-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="e10de-138">Seda probleemi saate lahendada järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e10de-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="e10de-139">Lisage kohandatud väli, et hõivata praegune äriprotsessi voo etapp, mida värskendatakse siis, kui kasutaja edeneb läbi kohandatud äriprotsessi voo.</span><span class="sxs-lookup"><span data-stu-id="e10de-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="e10de-140">Muutke tabelit **Projektid etappide järgi**, et töötada vaikekonfiguratsiooni asemel oma kohandatud väljaga.</span><span class="sxs-lookup"><span data-stu-id="e10de-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="e10de-141">Juhised enda protsessi voo loomiseks projekti üksuse jaoks</span><span class="sxs-lookup"><span data-stu-id="e10de-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="e10de-142">Enda protsessi voo loomiseks projekti üksuse jaoks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e10de-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="e10de-143">Valige **Sätted** > **Protsessikeskus**.</span><span class="sxs-lookup"><span data-stu-id="e10de-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="e10de-144">Ärge kopeerige projekti etappide äriprotsessi voogu, sest sellega koos kopeeritakse ka rakenduse Project Service äriloogika.</span><span class="sxs-lookup"><span data-stu-id="e10de-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="e10de-145">![Kuvatõmmis BPF-i kohandamisest](media/FAQ-Customize-BPF-3.png)</span><span class="sxs-lookup"><span data-stu-id="e10de-145">![Screenshot of BPF customization](media/FAQ-Customize-BPF-3.png)</span></span>

2. <span data-ttu-id="e10de-146">Kasutage funktsiooni Process Designer (Protsessi kujundaja), et luua soovitud etappide nimesid.</span><span class="sxs-lookup"><span data-stu-id="e10de-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="e10de-147">Kui soovite samu funktsioone nagu vaikeetappidel **Quote** (Pakkumine), **Plan** (Plaan) ja **Close** (Sulgemine), siis peate need looma teie kohandatud äriprotsessi voo etappide nimede põhjal.</span><span class="sxs-lookup"><span data-stu-id="e10de-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="e10de-148">![Kuvatõmmis funktsiooni Protsessi kujundaja kasutamisest BPF-i kohandamiseks](media/FAQ-Customize-BPF-4.png)</span><span class="sxs-lookup"><span data-stu-id="e10de-148">![Screenshot of Process Designer used to customize BPF](media/FAQ-Customize-BPF-4.png)</span></span> 

3. <span data-ttu-id="e10de-149">Klõpsake funktsioonis Protsessi kujundaja nuppu **Protsessi voo järjestus**, et muuta kohandatud äriprotsessi voog projekti üksuse peamiseks äriprotsessi vooks, liigutades selleks seda projekti etappide äriprotsessi voo kohale loendi tippu.</span><span class="sxs-lookup"><span data-stu-id="e10de-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="e10de-150">![Kuvatõmmis protsessi voo järjestuse kasutamisest](media/FAQ-Customize-BPF-5-720.png)</span><span class="sxs-lookup"><span data-stu-id="e10de-150">![Screenshot of using Order Process Flow](media/FAQ-Customize-BPF-5-720.png)</span></span>

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="e10de-151">Järgmised juhised kehtivad rakenduse Project Service versiooni 2.4.4.30 või varasema kohta platvormil 9.0</span><span class="sxs-lookup"><span data-stu-id="e10de-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="e10de-152">Lisage projekti üksusele uus kohandatud väli, et hõivata oma kohandatud äriprotsessi voo kohandatud etapid.</span><span class="sxs-lookup"><span data-stu-id="e10de-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="e10de-153">Peate lisama äriloogika (lisandmooduli/töövoo), et värskendada seda välja siis, kui kohandatud äriprotsessi voo etappi värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="e10de-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="e10de-154">![Kuvatõmmis projekti üksuse kohandamisest](media/FAQ-Customize-BPF-6-720.png)</span><span class="sxs-lookup"><span data-stu-id="e10de-154">![Screenshot of customizing Project entity](media/FAQ-Customize-BPF-6-720.png)</span></span>

5. <span data-ttu-id="e10de-155">Muutke tabelit **Projektid etappide järgi**, et kasutada oma uut kohandatud välja etappide jaoks.</span><span class="sxs-lookup"><span data-stu-id="e10de-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="e10de-156">![Kuvatõmmis tabeli Projektid etappide järgi kasutamisest](media/FAQ-Customize-BPF-7-720.png)</span><span class="sxs-lookup"><span data-stu-id="e10de-156">![Screenshot of using the Project By Stage chart](media/FAQ-Customize-BPF-7-720.png)</span></span>

6. <span data-ttu-id="e10de-157">Muutke projekti üksuse vaateid, et need hõlmaksid teie uut kohandatud välja kõikide etappide jaoks.</span><span class="sxs-lookup"><span data-stu-id="e10de-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="e10de-158">![Kuvatõmmis projekti üksuse vaadete muutmisest](media/FAQ-Customize-BPF-8-720.png)</span><span class="sxs-lookup"><span data-stu-id="e10de-158">![Screenshot of modifying views on the Project entity](media/FAQ-Customize-BPF-8-720.png)</span></span>

