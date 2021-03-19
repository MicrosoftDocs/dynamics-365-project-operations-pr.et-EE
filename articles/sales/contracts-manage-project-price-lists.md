---
title: Projektilepingute projekti hinnakirja haldamine
description: See teema sisaldab teavet projektilepingutes projekti hinnakirjade haldamise kohta.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2cfac6eda64d1d8e578115bba07942a7d786328f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278593"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="52409-103">Projektilepingute projekti hinnakirja haldamine</span><span class="sxs-lookup"><span data-stu-id="52409-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="52409-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="52409-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="52409-105">Projekti lepingud rakenduses Dynamics 365 Project Operations on loodud lepingus mitmel päeval kehtivate müügi hinnakirjade toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="52409-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="52409-106">Project Operationis on uus seostatud olem nimega **Projekti hinnakirjad**.</span><span class="sxs-lookup"><span data-stu-id="52409-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="52409-107">Sellel olemil on üks-mitmele-vastavuse seos projektilepinguga.</span><span class="sxs-lookup"><span data-stu-id="52409-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="52409-108">Projekti hinnakirju kasutatakse projekti aja ja kulutehingute hinnastamiseks.</span><span class="sxs-lookup"><span data-stu-id="52409-108">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="52409-109">Kui lepingul on üks või mitu projekti hinnakirja, kasutatakse neid hinnakirju aja ja kulude kalkulatsioonide ning tegelike näitajate hinna jaoks projektide puhu, mis on seostatud lepinguga lepingurea kaudu.</span><span class="sxs-lookup"><span data-stu-id="52409-109">When a contract has one or more project price lists, these price lists are used to price for time and expense estimates and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="52409-110">Kui projektilepingus ei ole projekti hinnakirju, näete hoiatussõnumit, et projekti hinnakirju pole ja teie prognoosidele, tegelikule projekti tööle ega kuludele ei lisata hinda.</span><span class="sxs-lookup"><span data-stu-id="52409-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, and expenses will not be priced.</span></span> <span data-ttu-id="52409-111">Müügiväärtustele ei lisata hinda.</span><span class="sxs-lookup"><span data-stu-id="52409-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="52409-112">Projekti hinnakirja projektilepinguga seostamine või seose tühistamine</span><span class="sxs-lookup"><span data-stu-id="52409-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a><span data-ttu-id="52409-113">Projektipõhise töö ja kulude prognoosimiseks konkreetse hinnakirja loomine või seostamine</span><span class="sxs-lookup"><span data-stu-id="52409-113">Create or associate a specific price list for estimating project-based work and expenses</span></span>

1. <span data-ttu-id="52409-114">Valige projektilepingus vahekaart **Projekti hinnakirjad**.</span><span class="sxs-lookup"><span data-stu-id="52409-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="52409-115">Valige andmeruudustikus suvand **+ Lisa uus projekti hinnakiri**.</span><span class="sxs-lookup"><span data-stu-id="52409-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="52409-116">Valige **kiirloomise** liuguril hinnakiri.</span><span class="sxs-lookup"><span data-stu-id="52409-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="52409-117">Ripploend kuvab kõik hinnakirjad, mille kontekstiks on määratud **Müük**, kus hinnakirja valuuta ühtib lepingu valuutaga.</span><span class="sxs-lookup"><span data-stu-id="52409-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="52409-118">Sisestage projekti hinnakirja seose kirjeldus, valige **Salvesta** ja seejärel sulgege **kiirloomise** liugur.</span><span class="sxs-lookup"><span data-stu-id="52409-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="52409-119">Luuakse projekti hinnakirja seos.</span><span class="sxs-lookup"><span data-stu-id="52409-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="52409-120">Korrake samme 1–4, et seostada projektilepinguga rohkem kui üks projekti hinnakiri.</span><span class="sxs-lookup"><span data-stu-id="52409-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="52409-121">Looge mitu projekti hinnakirja ainult siis, kui teie iga seostatud projekti hinnakiri jõustub erineval kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="52409-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="52409-122">Project Operations ei toeta projekti hinnakirjade kattuvaid jõustumiskuupäevi.</span><span class="sxs-lookup"><span data-stu-id="52409-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="52409-123">Kui tehingul on samaks kuupäevaks mitu projekti hinnakirja, määratakse selle tehingu hind vaikimisi nullile.</span><span class="sxs-lookup"><span data-stu-id="52409-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="52409-124">Projekti hinnakirja seostamise eemaldamine</span><span class="sxs-lookup"><span data-stu-id="52409-124">Remove a project price list association</span></span>

- <span data-ttu-id="52409-125">Valige projekti hinnakiri ja valige seejärel andmeruudustikul suvand **Kustuta lepingu projekti hinnakiri**.</span><span class="sxs-lookup"><span data-stu-id="52409-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="52409-126">Hinnakiri eemaldatakse lepingu projekti hinnakirjade seast.</span><span class="sxs-lookup"><span data-stu-id="52409-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="52409-127">Hinnakirja ennast ei kustutata.</span><span class="sxs-lookup"><span data-stu-id="52409-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="52409-128">Kustutatakse ainult lepingu seostamine.</span><span class="sxs-lookup"><span data-stu-id="52409-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="52409-129">Lepingu projekti hinnakirjade automaatsete vaikeväärtuste määramise häälestamine</span><span class="sxs-lookup"><span data-stu-id="52409-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="52409-130">Projekti hinnakirja saab häälestada projektilepingu vaikeloendina.</span><span class="sxs-lookup"><span data-stu-id="52409-130">A project price list can be set up as the default list on a project contract.</span></span> <span data-ttu-id="52409-131">See seadistus aitab tagada, et teie organisatsiooni kõik lepingud algavad konkreetsel hinnaperioodil standardse hinnakirjaga.</span><span class="sxs-lookup"><span data-stu-id="52409-131">This setup can help ensure that all contracts in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="52409-132">Projekti hinnakirjade organisatsiooni vaikeväärtuste häälestamine</span><span class="sxs-lookup"><span data-stu-id="52409-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="52409-133">Avage **Sätted** > **Üldine** ja valige seejärel suvand **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="52409-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="52409-134">Loendi lehel **Aktiivsed parameetrid** valige ja topeltklõpsake kirjel selle avamiseks.</span><span class="sxs-lookup"><span data-stu-id="52409-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="52409-135">Topeltklõpsamise ajal veenduge, et te ei klõpsaks välja väärtust, mis on hüperlink.</span><span class="sxs-lookup"><span data-stu-id="52409-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="52409-136">Valige lehel **Aktiivsed parameetrid** vahekaart **Hinnakiri**. Andmevõrgustik kuvab vaikimisi hinnakirjade loendi.</span><span class="sxs-lookup"><span data-stu-id="52409-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="52409-137">See on standardsete kulude ja müügihindade loend.</span><span class="sxs-lookup"><span data-stu-id="52409-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="52409-138">Hinnakirja **Müük** seostamine kõikide valuutadega, milles müüte, tagab et müügi hinnakiri on vaikeväärtus kõikides lepingutes, mille koostate selles valluutas tehinguid tegevatele klientidele.</span><span class="sxs-lookup"><span data-stu-id="52409-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="52409-139">Kliendipõhise projekti hinnakirja häälestamine</span><span class="sxs-lookup"><span data-stu-id="52409-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="52409-140">Kui te olete leppinud oma klientidega kokku raamhinnakokkuleppe, saate luua ka kliendipõhised projekti hinnakirjad.</span><span class="sxs-lookup"><span data-stu-id="52409-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="52409-141">Minge jaotisse **Müük** > **Kliendid**.</span><span class="sxs-lookup"><span data-stu-id="52409-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="52409-142">Valige aktiivsete kontode loendist klient, kellel on eraldi hinnakiri.</span><span class="sxs-lookup"><span data-stu-id="52409-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="52409-143">Valige avamiseks kliendi kirje ja valige seejärel vahekaart **Projekti hinnakirjad**. Andmeruudustik kuvab sellele kliendile spetsiifiliste projekti hinnakirjade loendi.</span><span class="sxs-lookup"><span data-stu-id="52409-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="52409-144">Looge siin uus hinnakirja seos, et omada sellele kliendile spetsiifilist projekti hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="52409-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="52409-145">Projektilepingu kohandatud hinnakiri</span><span class="sxs-lookup"><span data-stu-id="52409-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="52409-146">Pärast seda, kui teil on organisatsioonile ja kliendile spetsiifilised vaikimisi projekti hinnakirjad, teie projektilepingud luuakse nende projekti hinnakirja seostega automaatselt.</span><span class="sxs-lookup"><span data-stu-id="52409-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="52409-147">Samas projekti hinnakirja lepingu projekti hinnakirjad kopeeritakse alati kuupäeva ja lepingu nimega, mis on nendele lisatud.</span><span class="sxs-lookup"><span data-stu-id="52409-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="52409-148">Kontohaldurid ja projektijuhid saavad seejärel hakata nende koopiate hindasid muutma.</span><span class="sxs-lookup"><span data-stu-id="52409-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="52409-149">Need muudetud hinnad rakenduvad ainult sellele projektilepingule.</span><span class="sxs-lookup"><span data-stu-id="52409-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]