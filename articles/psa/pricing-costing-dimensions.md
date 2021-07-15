---
title: Hinnakujunduse ja kuluarvestuse dimensioonide avaleht
description: Selles teemas antakse ülevaade hindade dimensioonidest.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5c8c28839f5e7b3259afbea4ab400d0c4fca95fd
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368876"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="f4aa5-103">Hinnakujunduse ja kuluarvestuse dimensioonide avaleht</span><span class="sxs-lookup"><span data-stu-id="f4aa5-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f4aa5-104">Projektipõhiseöt tegutsevates organisatsioonides tööjõu hinna ja kulude määramiseks kasutatavaid dimensioone mõjutavad järgmised atribuudid:</span><span class="sxs-lookup"><span data-stu-id="f4aa5-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="f4aa5-105">Inimesed, kes teevad vastavalt nende kogemusele, rollile või geograafilisele asukohale tööd sarnaselt</span><span class="sxs-lookup"><span data-stu-id="f4aa5-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="f4aa5-106">Töö, mis tuleb teha vastavalt selle keerulisusele ja ajale sarnaselt</span><span class="sxs-lookup"><span data-stu-id="f4aa5-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="f4aa5-107">Arvestades nende töö tüüpilisi atribuute ja töö tegemiseks vajalikke inimesi, on rakenduses Project Service Automation saadaval järgmised kaks hinnakujunduse dimensiooni väärtuse tüüpi.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="f4aa5-108">**Suvandikomplektid** – atribuudid, mis on väärtuste kogumi jaoks fikseeritud loendites.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="f4aa5-109">**Olemil põhinevad väärtused** – atribuudid, mis võivad omada vaheldusrikkaid väärtuste kogumeid, mis on lõplikud, kuid võivad aja jooksul muutuda.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="f4aa5-110">Hinnakujunduse dimensioonid</span><span class="sxs-lookup"><span data-stu-id="f4aa5-110">Pricing dimensions</span></span>

<span data-ttu-id="f4aa5-111">PSA tarnitakse vaikimisi seatud hinnakujunduse dimensioonidega.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="f4aa5-112">Neid saate vaadata, kui avate **Project Service** > **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="f4aa5-113">Veenduge, et parameetri kirjel on vahekaardil **Summal põhinevad hinnakujunduse dimensioonid**, et selle rollide **msdyn_resourcecategory** ja ressursi organisatsiooniüksus **msdyn_organizationalunit** väljad **Kehtib müügi kohta** ja **Kehtib kulu kohta** oleks seatud väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="f4aa5-114">See võimaldab teil seadistada iga rolli ja organisatsiooniüksuse kombinatsiooni hinna ja maksumuse.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Esiletõstetud projektiteenuse parameetrite kuvatõmmis, millel on esile tõstetud „Kehtib müügi kohta”](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="f4aa5-116">Kui olete kasutanud valmiskujul rolli välju ja organisatsiooniüksust hinnakujunduse mõõtmetena enne PSA versiooni 3, ei ole mingeid jälgitavaid muudatusi.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="f4aa5-117">Saate jätkuvalt kasutada Project Service nagu tavaliselt.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="f4aa5-118">Kui teil on vaja ressursside hinda või kulu, kasutades täiendavaid atribuute, saate luua kohandatud välju, olemeid ja dimensioone.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="f4aa5-119">Lisateavet leiate järgmistest teemadest, kuid pange tähele, et protseduurid tuleb lõpule viia allpool toodud järjekorras.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="f4aa5-120">Kohandatud väljade ja olemite loomine</span><span class="sxs-lookup"><span data-stu-id="f4aa5-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="f4aa5-121">Kohandatud väljade lisamine hinna seadistusele ja ülekande olemitele</span><span class="sxs-lookup"><span data-stu-id="f4aa5-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="f4aa5-122">Kohandatud väljade seadistamine hinnakujunduse dimensioonidena </span><span class="sxs-lookup"><span data-stu-id="f4aa5-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="f4aa5-123">Lisandmooduli atribuutide värskendamine uute hinnakujunduse dimensioonide lisamiseks</span><span class="sxs-lookup"><span data-stu-id="f4aa5-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="f4aa5-124">Inimressursside aja hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="f4aa5-124">Pricing human resource time</span></span>
<span data-ttu-id="f4aa5-125">Organisatsiooni hindade arvestamine inimressursside aja järgi on sageli oluline strateegiline kaalutlus, mis mõjutab otseselt organisatsiooni tasuvust.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="f4aa5-126">Kui teie organisatsioon on valmis tuvastama, kuidas ta soovib arve ja kulumäära inimressursside aja järgi seadistada, saate tööd rahastada meeskondade ja tavadega.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="f4aa5-127">Muud kaalutlused hinna osas hõlmavad seda, kas uuesti kasutada välju või olemeid, mis pole praegu hinnakujunduse dimensioonid, kuid mida kohaldatakse teie organisatsiooni hinnakujunduse dimensioonina.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="f4aa5-128">Väljad, nagu **Tehingu kategooria** (**msdyn_transactioncategory**) ja **broneeritav ressurss**(**bookableresource**), on näited kandidaadi dimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="f4aa5-129">Kaaluge, kas teie hinnakujunduse dimensioon peaks olema tabel või suvandikomplekt.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="f4aa5-130">Kui teil on ette nähtud sellise dimensiooni väärtuste muudatused, mis ületavad 10 või 12 ja vajate nende väärtuste jaoks lisaatribuute, looge suvandikomplekti asemel olem.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="f4aa5-131">Suvandikomplekti haldamine, näiteks väärtuste lisamine või eemaldamine, nõuab administraatorilt või arendajalt, et enamikul ärikasutajatel oleks võimalik tabelisse uusi ridu lisada.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="f4aa5-132">Järgmises näites on toodud arve määrad, mis on seadistatud vastavalt rollile ja selle ressursside eralduse organisatsiooni üksusele, kuhu ressurss kuulub.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="f4aa5-133">Kulumäära aluseks on tavaliselt töötaja ja organisatsiooni ühik, kuhu nad kuuluvad.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="f4aa5-134">Selles näites näevad arve intressimäära ja kulumäära tabelid välja nagu järgmised.</span><span class="sxs-lookup"><span data-stu-id="f4aa5-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="f4aa5-135">**Näidishinnad**</span><span class="sxs-lookup"><span data-stu-id="f4aa5-135">**Sample bill rates**</span></span>

| <span data-ttu-id="f4aa5-136">Roll</span><span class="sxs-lookup"><span data-stu-id="f4aa5-136">Role</span></span>        | <span data-ttu-id="f4aa5-137">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="f4aa5-137">Org Unit</span></span>    |<span data-ttu-id="f4aa5-138">Üksus</span><span class="sxs-lookup"><span data-stu-id="f4aa5-138">Unit</span></span>      |<span data-ttu-id="f4aa5-139">Hind</span><span class="sxs-lookup"><span data-stu-id="f4aa5-139">Price</span></span>      |<span data-ttu-id="f4aa5-140">Valuuta</span><span class="sxs-lookup"><span data-stu-id="f4aa5-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f4aa5-141">Arendaja</span><span class="sxs-lookup"><span data-stu-id="f4aa5-141">Developer</span></span>   | <span data-ttu-id="f4aa5-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="f4aa5-142">Contoso US</span></span>  |<span data-ttu-id="f4aa5-143">tund</span><span class="sxs-lookup"><span data-stu-id="f4aa5-143">Hour</span></span> | <span data-ttu-id="f4aa5-144">200</span><span class="sxs-lookup"><span data-stu-id="f4aa5-144">200</span></span>|<span data-ttu-id="f4aa5-145">USD</span><span class="sxs-lookup"><span data-stu-id="f4aa5-145">USD</span></span>     |
| <span data-ttu-id="f4aa5-146">Arendaja</span><span class="sxs-lookup"><span data-stu-id="f4aa5-146">Developer</span></span>   | <span data-ttu-id="f4aa5-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="f4aa5-147">Contoso India</span></span> |<span data-ttu-id="f4aa5-148">tund</span><span class="sxs-lookup"><span data-stu-id="f4aa5-148">Hour</span></span>|   <span data-ttu-id="f4aa5-149">112</span><span class="sxs-lookup"><span data-stu-id="f4aa5-149">112</span></span>|<span data-ttu-id="f4aa5-150">USD</span><span class="sxs-lookup"><span data-stu-id="f4aa5-150">USD</span></span>     |


<span data-ttu-id="f4aa5-151">**Kulumäära näidis**</span><span class="sxs-lookup"><span data-stu-id="f4aa5-151">**Sample cost rates**</span></span>

| <span data-ttu-id="f4aa5-152">Palgavahemik</span><span class="sxs-lookup"><span data-stu-id="f4aa5-152">Salary Band</span></span>     | <span data-ttu-id="f4aa5-153">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="f4aa5-153">Org Unit</span></span>    |<span data-ttu-id="f4aa5-154">Üksus</span><span class="sxs-lookup"><span data-stu-id="f4aa5-154">Unit</span></span>      |<span data-ttu-id="f4aa5-155">Hind</span><span class="sxs-lookup"><span data-stu-id="f4aa5-155">Price</span></span>      |<span data-ttu-id="f4aa5-156">Valuuta</span><span class="sxs-lookup"><span data-stu-id="f4aa5-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f4aa5-157">Minu company_Band1</span><span class="sxs-lookup"><span data-stu-id="f4aa5-157">My company_Band1</span></span> | <span data-ttu-id="f4aa5-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="f4aa5-158">Contoso US</span></span>  |<span data-ttu-id="f4aa5-159">tund</span><span class="sxs-lookup"><span data-stu-id="f4aa5-159">Hour</span></span> | <span data-ttu-id="f4aa5-160">145</span><span class="sxs-lookup"><span data-stu-id="f4aa5-160">145</span></span>|<span data-ttu-id="f4aa5-161">USD</span><span class="sxs-lookup"><span data-stu-id="f4aa5-161">USD</span></span>     |
| <span data-ttu-id="f4aa5-162">Minu company_Band2</span><span class="sxs-lookup"><span data-stu-id="f4aa5-162">My company_Band2</span></span> | <span data-ttu-id="f4aa5-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="f4aa5-163">Contoso India</span></span> |<span data-ttu-id="f4aa5-164">tund</span><span class="sxs-lookup"><span data-stu-id="f4aa5-164">Hour</span></span>|   <span data-ttu-id="f4aa5-165">67</span><span class="sxs-lookup"><span data-stu-id="f4aa5-165">67</span></span>|<span data-ttu-id="f4aa5-166">USD</span><span class="sxs-lookup"><span data-stu-id="f4aa5-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]