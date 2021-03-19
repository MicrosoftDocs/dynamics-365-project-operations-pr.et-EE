---
title: Hinnakujunduse dimensioonide ülevaade
description: See teema sisaldab teavet hinnakujunduse dimensioonide kohta rakenduses Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ff675823d84c6e2b83be1e313f881bd672e53981
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275398"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="c289e-103">Hinnakujunduse dimensioonide ülevaade</span><span class="sxs-lookup"><span data-stu-id="c289e-103">Pricing dimensions overview</span></span>

<span data-ttu-id="c289e-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="c289e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c289e-105">Dimensioonid, mida kasutatakse inimressurssides hinnakujunduse ja kulude seadistamiseks, kuuluvad kahte kategooriasse.</span><span class="sxs-lookup"><span data-stu-id="c289e-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="c289e-106">Inimesed</span><span class="sxs-lookup"><span data-stu-id="c289e-106">People</span></span>
- <span data-ttu-id="c289e-107">Plaanitud töö</span><span class="sxs-lookup"><span data-stu-id="c289e-107">Planned work</span></span>

<span data-ttu-id="c289e-108">Seetõttu on olemas kahte tüüpi hinnakujunduse dimensiooniväärtusi.</span><span class="sxs-lookup"><span data-stu-id="c289e-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="c289e-109">**Suvandikomplektid**: dimensioonid, mis on väärtuste kogumi jaoks fikseeritud loendites.</span><span class="sxs-lookup"><span data-stu-id="c289e-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="c289e-110">**Olemil põhinevad väärtused**: dimensioonid, mis võivad olla vaheldusrikkad väärtuste kogumid.</span><span class="sxs-lookup"><span data-stu-id="c289e-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="c289e-111">Hinnakujunduse dimensioonid</span><span class="sxs-lookup"><span data-stu-id="c289e-111">Pricing dimensions</span></span>

<span data-ttu-id="c289e-112">Rakenduses Dynamics 365 Project Operations tarnitakse vaikimisi seatud hinnakujunduse dimensioonidega.</span><span class="sxs-lookup"><span data-stu-id="c289e-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="c289e-113">Neid hinnakujunduse dimensioone saate vaadata, kui avate **Project Operations** > **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="c289e-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="c289e-114">Veenduge, et parameetri kirjel on vahekaardil **Summal põhinevad hinnakujunduse dimensioonid**, et selle rollide **msdyn_resourcecategory** ja ressursi organisatsiooniüksus **msdyn_organizationalunit** väljad **Kehtib müügi kohta** ja **Kehtib kulu kohta** oleks seatud väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="c289e-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="c289e-115">Kui need väljad on lubatud, saate seadistada iga rolli ja organisatsiooniüksuse kombinatsiooni hinna ja maksumuse.</span><span class="sxs-lookup"><span data-stu-id="c289e-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

![Esiletõstetud projektiteenuse parameetrite kuvatõmmis, millel on esile tõstetud „Kehtib müügi kohta”](media/PS-OOB-parameters.png)

<span data-ttu-id="c289e-117">Kui teil on vaja ressursside hinda või kulu, kasutades täiendavaid atribuute, saate luua kohandatud välju, olemeid ja dimensioone.</span><span class="sxs-lookup"><span data-stu-id="c289e-117">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="c289e-118">Lisateabe saamiseks vaadake järgmisi teemasid.</span><span class="sxs-lookup"><span data-stu-id="c289e-118">For more information, see the following topics.</span></span> 
  
  > [!NOTE]
  > <span data-ttu-id="c289e-119">Toimingud tuleb teha loendamise järjekorras.</span><span class="sxs-lookup"><span data-stu-id="c289e-119">The procedures must be completed in the order they are listed.</span></span>

1. [<span data-ttu-id="c289e-120">Lahenduse loomine kohandatud hinnakujunduse dimensioonide jaoks</span><span class="sxs-lookup"><span data-stu-id="c289e-120">Create a solution for custom pricing dimensions</span></span>](../sales/create-solution-custompd.md)
2. [<span data-ttu-id="c289e-121">Kohandatud väljade ja olemite loomine</span><span class="sxs-lookup"><span data-stu-id="c289e-121">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md)
3. [<span data-ttu-id="c289e-122">Kohandatud väljade lisamine hinna seadistusele ja ülekande olemitele </span><span class="sxs-lookup"><span data-stu-id="c289e-122">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
4. [<span data-ttu-id="c289e-123">Kohandatud väljade seadistamine hinnakujunduse dimensioonidena </span><span class="sxs-lookup"><span data-stu-id="c289e-123">Set up custom fields as pricing dimensions</span></span>](set-up-custom-fields-pricing-dimensions.md)
5. [<span data-ttu-id="c289e-124">Lisandmooduli atribuutide värskendamine uute hinnakujunduse dimensioonide lisamiseks</span><span class="sxs-lookup"><span data-stu-id="c289e-124">Update plug-in attributes to include new pricing dimensions</span></span>](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a><span data-ttu-id="c289e-125">Inimressursside aja hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="c289e-125">Pricing human resource time</span></span>
<span data-ttu-id="c289e-126">Organisatsiooni hindade arvestamine inimressursside aja järgi on sageli oluline strateegiline kaalutlus, mis mõjutab otseselt organisatsiooni tasuvust.</span><span class="sxs-lookup"><span data-stu-id="c289e-126">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="c289e-127">Kui teie organisatsioon on valmis tuvastama, kuidas ta soovib arve ja kulumäära inimressursside aja järgi seadistada, saate tööd rahastada meeskondade ja tavadega.</span><span class="sxs-lookup"><span data-stu-id="c289e-127">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="c289e-128">Muud kaalutlused hinna osas hõlmavad seda, kas uuesti kasutada välju või olemeid, mis pole praegu hinnakujunduse dimensioonid, kuid mida kohaldatakse teie organisatsiooni hinnakujunduse dimensioonina.</span><span class="sxs-lookup"><span data-stu-id="c289e-128">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="c289e-129">Väljad, nagu **Tehingu kategooria** (**msdyn_transactioncategory**) ja **broneeritav ressurss**(**bookableresource**), on näited kandidaadi dimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="c289e-129">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="c289e-130">Kaaluge, kas teie hinnakujunduse dimensioon peaks olema tabel või suvandikomplekt.</span><span class="sxs-lookup"><span data-stu-id="c289e-130">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="c289e-131">Kui teil on ette nähtud sellise dimensiooni väärtuste muudatused, mis ületavad 10 või 12 ja vajate nende väärtuste jaoks lisaatribuute, võite luua suvandikomplekti asemel olemi.</span><span class="sxs-lookup"><span data-stu-id="c289e-131">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="c289e-132">Suvandikomplekti haldamine, näiteks väärtuste lisamine või eemaldamine, nõuab administraatorilt või arendajalt, et enamikul kasutajatel oleks võimalik tabelisse uusi ridu lisada.</span><span class="sxs-lookup"><span data-stu-id="c289e-132">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="c289e-133">Järgmises näites on toodud arve määrad, mis on seadistatud vastavalt rollile ja selle ressursside eralduse organisatsiooni üksusele, kuhu ressurss kuulub.</span><span class="sxs-lookup"><span data-stu-id="c289e-133">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="c289e-134">Kulumäära aluseks on tavaliselt töötaja ja organisatsiooni ühik, kuhu nad kuuluvad.</span><span class="sxs-lookup"><span data-stu-id="c289e-134">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="c289e-135">Selles näites näevad arve intressimäära ja kulumäära tabelid välja nagu järgmised.</span><span class="sxs-lookup"><span data-stu-id="c289e-135">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="c289e-136">**Näidishinnad**</span><span class="sxs-lookup"><span data-stu-id="c289e-136">**Sample bill rates**</span></span>

| <span data-ttu-id="c289e-137">Roll</span><span class="sxs-lookup"><span data-stu-id="c289e-137">Role</span></span>        | <span data-ttu-id="c289e-138">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="c289e-138">Org Unit</span></span>    |<span data-ttu-id="c289e-139">Ühik</span><span class="sxs-lookup"><span data-stu-id="c289e-139">Unit</span></span>      |<span data-ttu-id="c289e-140">Hind</span><span class="sxs-lookup"><span data-stu-id="c289e-140">Price</span></span>      |<span data-ttu-id="c289e-141">Valuuta</span><span class="sxs-lookup"><span data-stu-id="c289e-141">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="c289e-142">Arendaja</span><span class="sxs-lookup"><span data-stu-id="c289e-142">Developer</span></span>   | <span data-ttu-id="c289e-143">Jõgi US</span><span class="sxs-lookup"><span data-stu-id="c289e-143">Contoso US</span></span>  |<span data-ttu-id="c289e-144">Hour</span><span class="sxs-lookup"><span data-stu-id="c289e-144">Hour</span></span> | <span data-ttu-id="c289e-145">200</span><span class="sxs-lookup"><span data-stu-id="c289e-145">200</span></span>|<span data-ttu-id="c289e-146">USD</span><span class="sxs-lookup"><span data-stu-id="c289e-146">USD</span></span>     |
| <span data-ttu-id="c289e-147">Arendaja</span><span class="sxs-lookup"><span data-stu-id="c289e-147">Developer</span></span>   | <span data-ttu-id="c289e-148">Jõgi India</span><span class="sxs-lookup"><span data-stu-id="c289e-148">Contoso India</span></span> |<span data-ttu-id="c289e-149">Hour</span><span class="sxs-lookup"><span data-stu-id="c289e-149">Hour</span></span>|   <span data-ttu-id="c289e-150">112</span><span class="sxs-lookup"><span data-stu-id="c289e-150">112</span></span>|<span data-ttu-id="c289e-151">USD</span><span class="sxs-lookup"><span data-stu-id="c289e-151">USD</span></span>     |


<span data-ttu-id="c289e-152">**Kulumäära näidis**</span><span class="sxs-lookup"><span data-stu-id="c289e-152">**Sample cost rates**</span></span>

| <span data-ttu-id="c289e-153">Palgavahemik</span><span class="sxs-lookup"><span data-stu-id="c289e-153">Salary Band</span></span>     | <span data-ttu-id="c289e-154">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="c289e-154">Org Unit</span></span>    |<span data-ttu-id="c289e-155">Ühik</span><span class="sxs-lookup"><span data-stu-id="c289e-155">Unit</span></span>      |<span data-ttu-id="c289e-156">Hind</span><span class="sxs-lookup"><span data-stu-id="c289e-156">Price</span></span>      |<span data-ttu-id="c289e-157">Valuuta</span><span class="sxs-lookup"><span data-stu-id="c289e-157">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="c289e-158">Minu company_Band1</span><span class="sxs-lookup"><span data-stu-id="c289e-158">My company_Band1</span></span> | <span data-ttu-id="c289e-159">Jõgi US</span><span class="sxs-lookup"><span data-stu-id="c289e-159">Contoso US</span></span>  |<span data-ttu-id="c289e-160">Hour</span><span class="sxs-lookup"><span data-stu-id="c289e-160">Hour</span></span> | <span data-ttu-id="c289e-161">145</span><span class="sxs-lookup"><span data-stu-id="c289e-161">145</span></span>|<span data-ttu-id="c289e-162">USD</span><span class="sxs-lookup"><span data-stu-id="c289e-162">USD</span></span>     |
| <span data-ttu-id="c289e-163">Minu company_Band2</span><span class="sxs-lookup"><span data-stu-id="c289e-163">My company_Band2</span></span> | <span data-ttu-id="c289e-164">Jõgi India</span><span class="sxs-lookup"><span data-stu-id="c289e-164">Contoso India</span></span> |<span data-ttu-id="c289e-165">Hour</span><span class="sxs-lookup"><span data-stu-id="c289e-165">Hour</span></span>|   <span data-ttu-id="c289e-166">67</span><span class="sxs-lookup"><span data-stu-id="c289e-166">67</span></span>|<span data-ttu-id="c289e-167">USD</span><span class="sxs-lookup"><span data-stu-id="c289e-167">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]