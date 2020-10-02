---
title: Hinnakujunduse dimensioonide ülevaade
description: Selles teemas antakse teavet Dynamics 365 Project Operationsi hinnakujunduse dimensioonide kohta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898211"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="4f9e0-103">Hinnakujunduse dimensioonide ülevaade</span><span class="sxs-lookup"><span data-stu-id="4f9e0-103">Pricing dimensions overview</span></span>

<span data-ttu-id="4f9e0-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="4f9e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4f9e0-105">Dimensioonid, mida kasutatakse inimressurssides hinnakujunduse ja kulude seadistamiseks, kuuluvad kahte kategooriasse.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="4f9e0-106">Inimesed</span><span class="sxs-lookup"><span data-stu-id="4f9e0-106">People</span></span>
- <span data-ttu-id="4f9e0-107">Plaanitud töö</span><span class="sxs-lookup"><span data-stu-id="4f9e0-107">Planned work</span></span>

<span data-ttu-id="4f9e0-108">Seetõttu on olemas kahte tüüpi hinnakujunduse dimensiooniväärtusi.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="4f9e0-109">**Suvandikomplektid**: dimensioonid, mis on väärtuste kogumi jaoks fikseeritud loendites.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="4f9e0-110">**Olemil põhinevad väärtused**: dimensioonid, mis võivad olla vaheldusrikkad väärtuste kogumid.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="4f9e0-111">Hinnakujunduse dimensioonid</span><span class="sxs-lookup"><span data-stu-id="4f9e0-111">Pricing dimensions</span></span>

<span data-ttu-id="4f9e0-112">Dynamics 365 Project Operations tuleb vaikimisi seatud hinnakujunduse dimensioonidega.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="4f9e0-113">Neid hinnakujunduse dimensioone saate vaadata, kui avate **Project Operations** > **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="4f9e0-114">Veenduge, et parameetri kirjel on vahekaardil **Summal põhinevad hinnakujunduse dimensioonid**, et selle rollide **msdyn_resourcecategory** ja ressursi organisatsiooniüksus **msdyn_organizationalunit** väljad **Kehtib müügi kohta** ja **Kehtib kulu kohta** oleks seatud väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="4f9e0-115">Kui need väljad on lubatud, saate seadistada iga rolli ja organisatsiooniüksuse kombinatsiooni hinna ja maksumuse.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="4f9e0-116">Kui teil on vaja ressursside hinda või kulu, kasutades täiendavaid atribuute, saate luua kohandatud välju, olemeid ja dimensioone.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="4f9e0-117">Inimressursside aja hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="4f9e0-117">Pricing human resource time</span></span>
<span data-ttu-id="4f9e0-118">Organisatsiooni hindade arvestamine inimressursside aja järgi on sageli oluline strateegiline kaalutlus, mis mõjutab otseselt organisatsiooni tasuvust.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="4f9e0-119">Kui teie organisatsioon on valmis tuvastama, kuidas ta soovib arve ja kulumäära inimressursside aja järgi seadistada, saate tööd rahastada meeskondade ja tavadega.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="4f9e0-120">Muud kaalutlused hinna osas hõlmavad seda, kas uuesti kasutada välju või olemeid, mis pole praegu hinnakujunduse dimensioonid, kuid mida kohaldatakse teie organisatsiooni hinnakujunduse dimensioonina.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="4f9e0-121">Väljad, nagu **Tehingu kategooria** (**msdyn_transactioncategory**) ja **broneeritav ressurss**(**bookableresource**), on näited kandidaadi dimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="4f9e0-122">Kaaluge, kas teie hinnakujunduse dimensioon peaks olema tabel või suvandikomplekt.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="4f9e0-123">Kui teil on ette nähtud sellise dimensiooni väärtuste muudatused, mis ületavad 10 või 12 ja vajate nende väärtuste jaoks lisaatribuute, võite luua suvandikomplekti asemel olemi.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="4f9e0-124">Suvandikomplekti haldamine, näiteks väärtuste lisamine või eemaldamine, nõuab administraatorilt või arendajalt, et enamikul kasutajatel oleks võimalik tabelisse uusi ridu lisada.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="4f9e0-125">Järgmises näites on toodud arve määrad, mis on seadistatud vastavalt rollile ja selle ressursside eralduse organisatsiooni üksusele, kuhu ressurss kuulub.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="4f9e0-126">Kulumäära aluseks on tavaliselt töötaja ja organisatsiooni ühik, kuhu nad kuuluvad.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="4f9e0-127">Selles näites näevad arve intressimäära ja kulumäära tabelid välja nagu järgmised.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="4f9e0-128">**Näidishinnad**</span><span class="sxs-lookup"><span data-stu-id="4f9e0-128">**Sample bill rates**</span></span>

| <span data-ttu-id="4f9e0-129">Roll</span><span class="sxs-lookup"><span data-stu-id="4f9e0-129">Role</span></span>        | <span data-ttu-id="4f9e0-130">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="4f9e0-130">Org Unit</span></span>    |<span data-ttu-id="4f9e0-131">Ühik</span><span class="sxs-lookup"><span data-stu-id="4f9e0-131">Unit</span></span>      |<span data-ttu-id="4f9e0-132">Hind</span><span class="sxs-lookup"><span data-stu-id="4f9e0-132">Price</span></span>      |<span data-ttu-id="4f9e0-133">Valuuta</span><span class="sxs-lookup"><span data-stu-id="4f9e0-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="4f9e0-134">Arendaja</span><span class="sxs-lookup"><span data-stu-id="4f9e0-134">Developer</span></span>   | <span data-ttu-id="4f9e0-135">Jõgi US</span><span class="sxs-lookup"><span data-stu-id="4f9e0-135">Contoso US</span></span>  |<span data-ttu-id="4f9e0-136">Hour</span><span class="sxs-lookup"><span data-stu-id="4f9e0-136">Hour</span></span> | <span data-ttu-id="4f9e0-137">200</span><span class="sxs-lookup"><span data-stu-id="4f9e0-137">200</span></span>|<span data-ttu-id="4f9e0-138">USD</span><span class="sxs-lookup"><span data-stu-id="4f9e0-138">USD</span></span>     |
| <span data-ttu-id="4f9e0-139">Arendaja</span><span class="sxs-lookup"><span data-stu-id="4f9e0-139">Developer</span></span>   | <span data-ttu-id="4f9e0-140">Jõgi India</span><span class="sxs-lookup"><span data-stu-id="4f9e0-140">Contoso India</span></span> |<span data-ttu-id="4f9e0-141">Hour</span><span class="sxs-lookup"><span data-stu-id="4f9e0-141">Hour</span></span>|   <span data-ttu-id="4f9e0-142">112</span><span class="sxs-lookup"><span data-stu-id="4f9e0-142">112</span></span>|<span data-ttu-id="4f9e0-143">USD</span><span class="sxs-lookup"><span data-stu-id="4f9e0-143">USD</span></span>     |


<span data-ttu-id="4f9e0-144">**Kulumäära näidis**</span><span class="sxs-lookup"><span data-stu-id="4f9e0-144">**Sample cost rates**</span></span>

| <span data-ttu-id="4f9e0-145">Palgavahemik</span><span class="sxs-lookup"><span data-stu-id="4f9e0-145">Salary Band</span></span>     | <span data-ttu-id="4f9e0-146">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="4f9e0-146">Org Unit</span></span>    |<span data-ttu-id="4f9e0-147">Ühik</span><span class="sxs-lookup"><span data-stu-id="4f9e0-147">Unit</span></span>      |<span data-ttu-id="4f9e0-148">Hind</span><span class="sxs-lookup"><span data-stu-id="4f9e0-148">Price</span></span>      |<span data-ttu-id="4f9e0-149">Valuuta</span><span class="sxs-lookup"><span data-stu-id="4f9e0-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="4f9e0-150">Minu company_Band1</span><span class="sxs-lookup"><span data-stu-id="4f9e0-150">My company_Band1</span></span> | <span data-ttu-id="4f9e0-151">Jõgi US</span><span class="sxs-lookup"><span data-stu-id="4f9e0-151">Contoso US</span></span>  |<span data-ttu-id="4f9e0-152">Hour</span><span class="sxs-lookup"><span data-stu-id="4f9e0-152">Hour</span></span> | <span data-ttu-id="4f9e0-153">145</span><span class="sxs-lookup"><span data-stu-id="4f9e0-153">145</span></span>|<span data-ttu-id="4f9e0-154">USD</span><span class="sxs-lookup"><span data-stu-id="4f9e0-154">USD</span></span>     |
| <span data-ttu-id="4f9e0-155">Minu company_Band2</span><span class="sxs-lookup"><span data-stu-id="4f9e0-155">My company_Band2</span></span> | <span data-ttu-id="4f9e0-156">Jõgi India</span><span class="sxs-lookup"><span data-stu-id="4f9e0-156">Contoso India</span></span> |<span data-ttu-id="4f9e0-157">Hour</span><span class="sxs-lookup"><span data-stu-id="4f9e0-157">Hour</span></span>|   <span data-ttu-id="4f9e0-158">67</span><span class="sxs-lookup"><span data-stu-id="4f9e0-158">67</span></span>|<span data-ttu-id="4f9e0-159">USD</span><span class="sxs-lookup"><span data-stu-id="4f9e0-159">USD</span></span>     |
