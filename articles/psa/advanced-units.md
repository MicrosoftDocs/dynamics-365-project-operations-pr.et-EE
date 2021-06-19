---
title: Ühikurühmad ja ühikud
description: Selles teemas antakse teavet ühikurühmade ja ühikute kohta.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e981f39bbb6ca4277778382a5816952df2a8a1fb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009566"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="2c598-103">Ühikurühmad ja ühikud</span><span class="sxs-lookup"><span data-stu-id="2c598-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2c598-104">Ühikurühmad ja ühikud on rakenduses Microsoft Dynamics 365 põhiolemid.</span><span class="sxs-lookup"><span data-stu-id="2c598-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="2c598-105">Ühik on üks mõõtühik ja mitu ühikut saab rühmitada ühikute rühmadesse.</span><span class="sxs-lookup"><span data-stu-id="2c598-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="2c598-106">Ühikurühma nimetatakse vahel ka rakenduse Dynamics 365 kasutajaliideses (UI) üksuse ajakavaks.</span><span class="sxs-lookup"><span data-stu-id="2c598-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="2c598-107">Siin on mõned näited ühikutest ja ühikurühmadest.</span><span class="sxs-lookup"><span data-stu-id="2c598-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="2c598-108">**Ühikurühm**: vahemaa</span><span class="sxs-lookup"><span data-stu-id="2c598-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="2c598-109">**Ühikud**: miil, kilomeeter jne.</span><span class="sxs-lookup"><span data-stu-id="2c598-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="2c598-110">**Ühikurühm**: aeg</span><span class="sxs-lookup"><span data-stu-id="2c598-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="2c598-111">**Ühikud**: tund, päev, nädal jne.</span><span class="sxs-lookup"><span data-stu-id="2c598-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="2c598-112">Kui seadistate ühikurühmas mitu ühikut, peate seadistama ka nende vahel teisendusteguri, määrates esimese ühiku, mille olete seadistanud ühikurühma vaike-või põhiühikuna.</span><span class="sxs-lookup"><span data-stu-id="2c598-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="2c598-113">Näiteks ühikurühmas **Aeg**, kui seadistate esimeseks ühikuks **Tund**, määrab süsteem ühiku **Tund** vaikeühikuks.</span><span class="sxs-lookup"><span data-stu-id="2c598-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="2c598-114">Kui teie järgmine seadistatud ühik on **Päev**, peate määrama teisendusteguri ühikust **Päev** ühikuks **Tund**.</span><span class="sxs-lookup"><span data-stu-id="2c598-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="2c598-115">Kui lisate kolmanda ühikuna **Nädal**, peate seadistama teisendusteguri ühikule **Nädal** ühikute **Päev** või **Tund** osas.</span><span class="sxs-lookup"><span data-stu-id="2c598-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="2c598-116">Järgmisel pildil on toodud näiteks ühiku **Päev** seadistus, kus väljal **Kogus** kuvatakse tundide arv, mis on päevas, ja ühiku **Nädal** seadistus, kus väljal **Kogus** kuvatakse päevade arv, mis on nädalas.</span><span class="sxs-lookup"><span data-stu-id="2c598-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Ühikurühm: teabeleht](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="2c598-118">Ühikute ja ühikurühmade kasutamine</span><span class="sxs-lookup"><span data-stu-id="2c598-118">Using units and unit groups</span></span>

<span data-ttu-id="2c598-119">Rakendus Dynamics 365 Project Service Automation kasutab ühikuid ja ühikurühmasid, et töödelda nii kulu kui ka aja hinnanguid ja kirjeid.</span><span class="sxs-lookup"><span data-stu-id="2c598-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="2c598-120">Kulude puhul on igal kulukategooria vaikimisi ühikurühm ja ühik.</span><span class="sxs-lookup"><span data-stu-id="2c598-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="2c598-121">Need väärtused sisestatakse kulukategooriate hinnakirja kirjetesse vaikeväärtustena.</span><span class="sxs-lookup"><span data-stu-id="2c598-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="2c598-122">Näiteks on teil kulukategooria, mis on nimega **Läbisõit**.</span><span class="sxs-lookup"><span data-stu-id="2c598-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="2c598-123">Sel on ühikrühm, mis on nimega **Vahemaa** ja vaikimisi ühik, mis on nimega **Miil**.</span><span class="sxs-lookup"><span data-stu-id="2c598-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="2c598-124">Kui seadistate ühikurühma **Vahemaa** nii, et sellel on kaks ühikut (**Miil** ja **Kilomeeter**), saate kategooria **Läbisõit** jaoks määrata ühes hinnakirjas kaks müügihinda: üks hind miili ja teine kilomeetri kohta.</span><span class="sxs-lookup"><span data-stu-id="2c598-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="2c598-125">Kulukategooria</span><span class="sxs-lookup"><span data-stu-id="2c598-125">Expense category</span></span>  | <span data-ttu-id="2c598-126">Ühikurühm</span><span class="sxs-lookup"><span data-stu-id="2c598-126">Unit group</span></span>  | <span data-ttu-id="2c598-127">Ühik</span><span class="sxs-lookup"><span data-stu-id="2c598-127">Unit</span></span>      | <span data-ttu-id="2c598-128">Hinnakujundusmeetod</span><span class="sxs-lookup"><span data-stu-id="2c598-128">Pricing method</span></span>  | <span data-ttu-id="2c598-129">Ühiku hind</span><span class="sxs-lookup"><span data-stu-id="2c598-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="2c598-130">Läbisõit</span><span class="sxs-lookup"><span data-stu-id="2c598-130">Mileage</span></span>           | <span data-ttu-id="2c598-131">Kaugus</span><span class="sxs-lookup"><span data-stu-id="2c598-131">Distance</span></span>      | <span data-ttu-id="2c598-132">Miil</span><span class="sxs-lookup"><span data-stu-id="2c598-132">Mile</span></span>      | <span data-ttu-id="2c598-133">Ühiku hind</span><span class="sxs-lookup"><span data-stu-id="2c598-133">Price per unit</span></span>    | <span data-ttu-id="2c598-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="2c598-134">10 USD</span></span>            |
| <span data-ttu-id="2c598-135">Läbisõit</span><span class="sxs-lookup"><span data-stu-id="2c598-135">Mileage</span></span>           | <span data-ttu-id="2c598-136">Kaugus</span><span class="sxs-lookup"><span data-stu-id="2c598-136">Distance</span></span>      | <span data-ttu-id="2c598-137">Kilomeeter</span><span class="sxs-lookup"><span data-stu-id="2c598-137">Kilometer</span></span> | <span data-ttu-id="2c598-138">Ühiku hind</span><span class="sxs-lookup"><span data-stu-id="2c598-138">Price per unit</span></span>    |  <span data-ttu-id="2c598-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="2c598-139">6 USD</span></span>            |

<span data-ttu-id="2c598-140">Projektile kulu sisestamisel määratleb süsteem kategooria ja kulul oleva ühiku kombinatsiooni kaudu hinna.</span><span class="sxs-lookup"><span data-stu-id="2c598-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="2c598-141">Kulu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2c598-141">Expense description</span></span>        | <span data-ttu-id="2c598-142">Kulukategooria</span><span class="sxs-lookup"><span data-stu-id="2c598-142">Expense category</span></span>  | <span data-ttu-id="2c598-143">Ühik</span><span class="sxs-lookup"><span data-stu-id="2c598-143">Unit</span></span>  | <span data-ttu-id="2c598-144">Kogus</span><span class="sxs-lookup"><span data-stu-id="2c598-144">Quantity</span></span>  | <span data-ttu-id="2c598-145">Ühiku hind</span><span class="sxs-lookup"><span data-stu-id="2c598-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="2c598-146">Sõida kliendi asukohta</span><span class="sxs-lookup"><span data-stu-id="2c598-146">Drive to client location</span></span> | <span data-ttu-id="2c598-147">Läbisõit</span><span class="sxs-lookup"><span data-stu-id="2c598-147">Mileage</span></span>             | <span data-ttu-id="2c598-148">Miil</span><span class="sxs-lookup"><span data-stu-id="2c598-148">Mile</span></span>  | <span data-ttu-id="2c598-149">10</span><span class="sxs-lookup"><span data-stu-id="2c598-149">10</span></span>        | <span data-ttu-id="2c598-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="2c598-150">10 USD</span></span>         |

<span data-ttu-id="2c598-151">Iga hinnakirja päises on aja jaoks väli **Vaikimisi ajaühik**.</span><span class="sxs-lookup"><span data-stu-id="2c598-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="2c598-152">Väärtus seatakse hinnakirja päise loomisel.</span><span class="sxs-lookup"><span data-stu-id="2c598-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="2c598-153">Seda üksust kasutatakse seejärel selle hinnakirja kõigi rollipõhiste hindade seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="2c598-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="2c598-154">Välja **Hinnapakkumise aeg** hinnapakkumise ridu saab väljendada mis tahes ajaühikus.</span><span class="sxs-lookup"><span data-stu-id="2c598-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="2c598-155">Projektidele määratud projektide hinnangu read ja ajakirjed saavad kasutada ainult ajaühikut **Tund**.</span><span class="sxs-lookup"><span data-stu-id="2c598-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="2c598-156">Kui ajakirjes või hinnangu real olev ühik ei vasta selle rolli hinnakirja real olevale ühikule, teisendab süsteem hinna ühikuteks, mis on määratletud projekti hinnangus või projekti tegelikus tehingus.</span><span class="sxs-lookup"><span data-stu-id="2c598-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="2c598-157">Järgmises näites kirjeldatakse, kuidas PSA kasutab ühikurühma, ühikuid ja teisendustegureid.</span><span class="sxs-lookup"><span data-stu-id="2c598-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="2c598-158">Ühikud</span><span class="sxs-lookup"><span data-stu-id="2c598-158">Units</span></span>

   - <span data-ttu-id="2c598-159">**Ühikurühm**: aeg</span><span class="sxs-lookup"><span data-stu-id="2c598-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="2c598-160">**Ühikud**: tund</span><span class="sxs-lookup"><span data-stu-id="2c598-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="2c598-161">**Päev** – teisendustegur: 8 tundi</span><span class="sxs-lookup"><span data-stu-id="2c598-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="2c598-162">**Nädal** – teisendustegur: 40 tundi</span><span class="sxs-lookup"><span data-stu-id="2c598-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="2c598-163">Hinnakirja seadistus projektile A.</span><span class="sxs-lookup"><span data-stu-id="2c598-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="2c598-164">**Nimi**: UK müügihinnad 2016</span><span class="sxs-lookup"><span data-stu-id="2c598-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="2c598-165">**Vaikimisi ajaühik**: päev</span><span class="sxs-lookup"><span data-stu-id="2c598-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="2c598-166">**Valuuta**: GBP</span><span class="sxs-lookup"><span data-stu-id="2c598-166">**Currency**: GBP</span></span>

| <span data-ttu-id="2c598-167">Roll</span><span class="sxs-lookup"><span data-stu-id="2c598-167">Role</span></span>      | <span data-ttu-id="2c598-168">Ühikurühm</span><span class="sxs-lookup"><span data-stu-id="2c598-168">Unit group</span></span> | <span data-ttu-id="2c598-169">Üksus</span><span class="sxs-lookup"><span data-stu-id="2c598-169">Unit</span></span> | <span data-ttu-id="2c598-170">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="2c598-170">Organizational unit</span></span> | <span data-ttu-id="2c598-171">Hind</span><span class="sxs-lookup"><span data-stu-id="2c598-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="2c598-172">Arendaja</span><span class="sxs-lookup"><span data-stu-id="2c598-172">Developer</span></span> | <span data-ttu-id="2c598-173">Aeg</span><span class="sxs-lookup"><span data-stu-id="2c598-173">Time</span></span>       | <span data-ttu-id="2c598-174">päev</span><span class="sxs-lookup"><span data-stu-id="2c598-174">Day</span></span>  | <span data-ttu-id="2c598-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="2c598-175">Contoso UK</span></span>          | <span data-ttu-id="2c598-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="2c598-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="2c598-177">Ajakirje</span><span class="sxs-lookup"><span data-stu-id="2c598-177">Time entry</span></span>

<span data-ttu-id="2c598-178">Järgmises tabelis on toodud tulemuseks saadud müügiga seotud tehing, mille PSA on loonud kolmetunnine projekti jaoks.</span><span class="sxs-lookup"><span data-stu-id="2c598-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="2c598-179">Projekt</span><span class="sxs-lookup"><span data-stu-id="2c598-179">Project</span></span>   | <span data-ttu-id="2c598-180">Tööülesanne</span><span class="sxs-lookup"><span data-stu-id="2c598-180">Task</span></span>    | <span data-ttu-id="2c598-181">Roll</span><span class="sxs-lookup"><span data-stu-id="2c598-181">Role</span></span>      | <span data-ttu-id="2c598-182">Kogus</span><span class="sxs-lookup"><span data-stu-id="2c598-182">Quantity</span></span> | <span data-ttu-id="2c598-183">Ühik</span><span class="sxs-lookup"><span data-stu-id="2c598-183">Unit</span></span>  | <span data-ttu-id="2c598-184">Ühiku hind</span><span class="sxs-lookup"><span data-stu-id="2c598-184">Unit price</span></span> | <span data-ttu-id="2c598-185">Arveldamata müügisumma</span><span class="sxs-lookup"><span data-stu-id="2c598-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="2c598-186">Projekt A</span><span class="sxs-lookup"><span data-stu-id="2c598-186">Project A</span></span> | <span data-ttu-id="2c598-187">Kujundus</span><span class="sxs-lookup"><span data-stu-id="2c598-187">Design</span></span>  | <span data-ttu-id="2c598-188">Arendaja</span><span class="sxs-lookup"><span data-stu-id="2c598-188">Developer</span></span> | <span data-ttu-id="2c598-189">3</span><span class="sxs-lookup"><span data-stu-id="2c598-189">3</span></span>        | <span data-ttu-id="2c598-190">Hour</span><span class="sxs-lookup"><span data-stu-id="2c598-190">Hour</span></span>  | <span data-ttu-id="2c598-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="2c598-191">100 GBP</span></span>    | <span data-ttu-id="2c598-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="2c598-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="2c598-193">Ajaühiku KKK</span><span class="sxs-lookup"><span data-stu-id="2c598-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="2c598-194">Kas PSA teisendab kulude puhul erinevateks ühikuteks?</span><span class="sxs-lookup"><span data-stu-id="2c598-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="2c598-195">Ei.</span><span class="sxs-lookup"><span data-stu-id="2c598-195">No.</span></span> <span data-ttu-id="2c598-196">Ühiku teisendus töötab ainult aja puhul.</span><span class="sxs-lookup"><span data-stu-id="2c598-196">Unit conversion works only for time.</span></span> <span data-ttu-id="2c598-197">Kulude puhul, kui süsteem ei leia kulude kategooria ja ühiku kombinatsiooni hinda, on vaikimisi hinnaks seatud 0,00.</span><span class="sxs-lookup"><span data-stu-id="2c598-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="2c598-198">Miks PSA ajaühikuid teisendab?</span><span class="sxs-lookup"><span data-stu-id="2c598-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="2c598-199">Mõnes riigis või piirkonnas on juriidiline nõue, et arveldusmäärad oleksid seadistatud päevades.</span><span class="sxs-lookup"><span data-stu-id="2c598-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="2c598-200">Hinnapakkumise tsükli ajal toimuvad hinna läbirääkimised ja allahindlused tehakse kasutades iga tasustatava rolli jaoks päeva hindasid.</span><span class="sxs-lookup"><span data-stu-id="2c598-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="2c598-201">Ajakava hinnang ja aja sisestamine toimub tundides.</span><span class="sxs-lookup"><span data-stu-id="2c598-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="2c598-202">Kui soovite seda erinevust ajaühikutes toetada, teisendab PSA ajaühikud.</span><span class="sxs-lookup"><span data-stu-id="2c598-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="2c598-203">Kas ajaühikuid saab projekti hinnangutes muuta?</span><span class="sxs-lookup"><span data-stu-id="2c598-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="2c598-204">Ei.</span><span class="sxs-lookup"><span data-stu-id="2c598-204">No.</span></span> <span data-ttu-id="2c598-205">Ajakava hinnang on praegu piiratud tundidega ja seda ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="2c598-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="2c598-206">Kas ühikuid ja ühikurühmi saab redigeerida, kustutada ja lisada?</span><span class="sxs-lookup"><span data-stu-id="2c598-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="2c598-207">Jah.</span><span class="sxs-lookup"><span data-stu-id="2c598-207">Yes.</span></span> <span data-ttu-id="2c598-208">Peale ühikurühma **Aeg** ja ühikut **Tund**, saab kõiki ühikuid kustutada või redigeerida ning uusi ühikuid saab lisada.</span><span class="sxs-lookup"><span data-stu-id="2c598-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="2c598-209">PSA-s ei saa ühikurühma **Aeg** ja ühikut **Tund** kustutada.</span><span class="sxs-lookup"><span data-stu-id="2c598-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="2c598-210">Neid saab siiski värskendada tõlgitud tekstiga väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="2c598-210">However, they can be updated with a translated text for the **Name** field.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]