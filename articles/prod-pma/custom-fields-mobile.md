---
title: Rakendage mobiilirakenduse Microsoft Dynamics 365 Project Timesheet iOS-i ja Androidi kohandatud väljad
description: Selles teemas kirjeldatakse kohandatud väljade juurutamiseks laienduste kasutamise ühiseid mudeleid.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075010"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="633e8-103">Rakendage mobiilirakenduse Microsoft Dynamics 365 Project Timesheet iOS-i ja Androidi kohandatud väljad</span><span class="sxs-lookup"><span data-stu-id="633e8-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="633e8-104">Selles teemas kirjeldatakse kohandatud väljade juurutamiseks laienduste kasutamise ühiseid mudeleid.</span><span class="sxs-lookup"><span data-stu-id="633e8-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="633e8-105">Käsitletakse järgmisi teemasid.</span><span class="sxs-lookup"><span data-stu-id="633e8-105">The following topics are covered:</span></span>

- <span data-ttu-id="633e8-106">Erinevad andmetüübid, mida kohandatud väljaraamistik toetab</span><span class="sxs-lookup"><span data-stu-id="633e8-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="633e8-107">Kuidas kuvada kirjutuskaitstud või redigeeritavaid välju ajatabeli kirjetesse ja salvestada kasutaja esitatud väärtused tagasi andmebaasi</span><span class="sxs-lookup"><span data-stu-id="633e8-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="633e8-108">Ajatabeli päises kirjutuskaitstud väljade kuvamine</span><span class="sxs-lookup"><span data-stu-id="633e8-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="633e8-109">Muu kohandatud äriloogika integreerimine väljadele vaikeväärtuste sisestamiseks ja täiendavaks valideerimiseks</span><span class="sxs-lookup"><span data-stu-id="633e8-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="633e8-110">Publik</span><span class="sxs-lookup"><span data-stu-id="633e8-110">Audience</span></span>

<span data-ttu-id="633e8-111">See teema on mõeldud arendajatele, kes integreerivad oma kohandatud väljad Microsoft Dynamics 365 Project Timesheeti mobiilsesse rakendusse, mis on saadaval Apple iOS-i ja Google Androidi jaoks.</span><span class="sxs-lookup"><span data-stu-id="633e8-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="633e8-112">Eeldame, et lugejad tunnevad X + + arenduse ja projekti ajatabeli funktsioone.</span><span class="sxs-lookup"><span data-stu-id="633e8-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="633e8-113">Andmete leping – TSTimesheetCustomField X++ klass</span><span class="sxs-lookup"><span data-stu-id="633e8-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="633e8-114">Klass **TSTimesheetCustomField** on X++ andmete lepingu klass, mis esindab teavet kohandatud välja kohta ajatabeli toimimise jaoks.</span><span class="sxs-lookup"><span data-stu-id="633e8-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="633e8-115">Kohandatud välja objektide loendid edastatakse nii TSTimesheetDetails kui ka TSTimesheetEntry, et kuvada mobiilirakenduse kohandatud välju.</span><span class="sxs-lookup"><span data-stu-id="633e8-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="633e8-116">**TSTimesheetDetails** – ajatabeli päise leping.</span><span class="sxs-lookup"><span data-stu-id="633e8-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="633e8-117">**TSTimesheetEntry** – ajatabeli kande leping.</span><span class="sxs-lookup"><span data-stu-id="633e8-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="633e8-118">Nende objektide rühmad, millel on sama projekti teave ja **timesheetLineRecId,** moodustavad rea.</span><span class="sxs-lookup"><span data-stu-id="633e8-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="633e8-119">fieldBaseType (Types)</span><span class="sxs-lookup"><span data-stu-id="633e8-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="633e8-120">Atribuut **FieldBaseType** objektil **TsTimesheetCustom** määratleb rakenduses kuvatava välja tüübi.</span><span class="sxs-lookup"><span data-stu-id="633e8-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="633e8-121">Toetatakse järgmisi **Tüüpide** väärtusi.</span><span class="sxs-lookup"><span data-stu-id="633e8-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="633e8-122">Tüüpide väärtus</span><span class="sxs-lookup"><span data-stu-id="633e8-122">Types value</span></span> | <span data-ttu-id="633e8-123">Tüüp</span><span class="sxs-lookup"><span data-stu-id="633e8-123">Type</span></span>              | <span data-ttu-id="633e8-124">Märkmed</span><span class="sxs-lookup"><span data-stu-id="633e8-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="633e8-125">0</span><span class="sxs-lookup"><span data-stu-id="633e8-125">0</span></span>           | <span data-ttu-id="633e8-126">String (ja loetelu)</span><span class="sxs-lookup"><span data-stu-id="633e8-126">String (and Enum)</span></span> | <span data-ttu-id="633e8-127">Väli kuvatakse tekstiväljana.</span><span class="sxs-lookup"><span data-stu-id="633e8-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="633e8-128">1</span><span class="sxs-lookup"><span data-stu-id="633e8-128">1</span></span>           | <span data-ttu-id="633e8-129">Integer</span><span class="sxs-lookup"><span data-stu-id="633e8-129">Integer</span></span>           | <span data-ttu-id="633e8-130">Väärtus kuvatakse arvuna ilma kümnendkohtadeta.</span><span class="sxs-lookup"><span data-stu-id="633e8-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="633e8-131">2</span><span class="sxs-lookup"><span data-stu-id="633e8-131">2</span></span>           | <span data-ttu-id="633e8-132">Reaalarv</span><span class="sxs-lookup"><span data-stu-id="633e8-132">Real</span></span>              | <span data-ttu-id="633e8-133">Väärtus kuvatakse arvuna, millel on kümnendkohad.</span><span class="sxs-lookup"><span data-stu-id="633e8-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="633e8-134">Tegeliku väärtuse kuvamiseks rakenduses valuutana kasutage **fieldExtenededType** atribuuti.</span><span class="sxs-lookup"><span data-stu-id="633e8-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="633e8-135">Atribuudi **numberOfDecimals** abil saate määrata kuvatavate kümnendkohtade arvu.</span><span class="sxs-lookup"><span data-stu-id="633e8-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="633e8-136">3</span><span class="sxs-lookup"><span data-stu-id="633e8-136">3</span></span>           | <span data-ttu-id="633e8-137">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="633e8-137">Date</span></span>              | <span data-ttu-id="633e8-138">Kuupäeva vormingud on määratletud kasutaja **Kuupäeva, kellaaja ja arvuvormingu** sättega, mis on määratud **Keele ja riigi/regiooni eelistuste** all **Kasutajasuvandites**.</span><span class="sxs-lookup"><span data-stu-id="633e8-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="633e8-139">4</span><span class="sxs-lookup"><span data-stu-id="633e8-139">4</span></span>           | <span data-ttu-id="633e8-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="633e8-140">Boolean</span></span>           | |
| <span data-ttu-id="633e8-141">15</span><span class="sxs-lookup"><span data-stu-id="633e8-141">15</span></span>          | <span data-ttu-id="633e8-142">GUID</span><span class="sxs-lookup"><span data-stu-id="633e8-142">GUID</span></span>              | |
| <span data-ttu-id="633e8-143">16</span><span class="sxs-lookup"><span data-stu-id="633e8-143">16</span></span>          | <span data-ttu-id="633e8-144">Int64</span><span class="sxs-lookup"><span data-stu-id="633e8-144">Int64</span></span>             | |

- <span data-ttu-id="633e8-145">Kui **stringOptions** atribuuti pole **TSTimesheetCustomField** objektil, pakutakse kasutajale vabas kirjas tekstivälja.</span><span class="sxs-lookup"><span data-stu-id="633e8-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="633e8-146">Atribuuti **stringLength** saab kasutada maksimaalse stringi pikkuse seadmiseks, mida kasutajad saavad sisestada.</span><span class="sxs-lookup"><span data-stu-id="633e8-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="633e8-147">Kui atribuut **stringOptions** on esitatud **TSTimesheetCustomField** objektil, on need loendi elemendid ainsad väärtused, mida kasutajad saavad valida valikunuppude (raadionuppude) abil.</span><span class="sxs-lookup"><span data-stu-id="633e8-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="633e8-148">Sellisel juhul võib väljal string olla loendiväärtus kasutaja kirje eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="633e8-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="633e8-149">Väärtuse salvestamiseks andmebaasi loeteluna vastendage stringi väärtus tagasi loendi väärtusele, enne kui salvestate andmebaasi, kasutades käsuliini (vt "TSTimesheetEntryService klassis käsuahela kasutamine, et salvestada ajatabeli kanne rakendusest tagasi andmebaasi" hiljem selles teemas näitena).</span><span class="sxs-lookup"><span data-stu-id="633e8-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="633e8-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="633e8-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="633e8-151">Seda atribuuti saate kasutada tegelike väärtuste vormindamiseks valuutana.</span><span class="sxs-lookup"><span data-stu-id="633e8-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="633e8-152">See lähenemine on kohaldatav ainult juhul, kui **fieldBaseType** väärtus on **Real**.</span><span class="sxs-lookup"><span data-stu-id="633e8-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="633e8-153">**TSCustomFieldExtendedType:None** – vormingut ei rakendata.</span><span class="sxs-lookup"><span data-stu-id="633e8-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="633e8-154">**TSCustomFieldExtendedType::Currency** – vormindage väärtus valuutana.</span><span class="sxs-lookup"><span data-stu-id="633e8-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="633e8-155">Kui valuutavorming on aktiivne, saab **stringValue** välja abil edastada valuutakoodi, mis tuleb rakenduses kuvada.</span><span class="sxs-lookup"><span data-stu-id="633e8-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="633e8-156">Väärtus on kirjutuskaitstud väärtus.</span><span class="sxs-lookup"><span data-stu-id="633e8-156">The value is a read-only value.</span></span>

    <span data-ttu-id="633e8-157">Välin **realValue** sisaldab rahasummat, mis tuleb andmebaasi salvestada.</span><span class="sxs-lookup"><span data-stu-id="633e8-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="633e8-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="633e8-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="633e8-159">Selle atribuudi abil saate määrata, kus rakendus peaks kuvama kohandatud välja.</span><span class="sxs-lookup"><span data-stu-id="633e8-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="633e8-160">**TSCustomFieldSection::Header** – väli kuvatakse rakenduse jaotises **Kuva rohkem üksikasju**.</span><span class="sxs-lookup"><span data-stu-id="633e8-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="633e8-161">Need väljad on alati kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="633e8-161">These fields are always read-only.</span></span>
- <span data-ttu-id="633e8-162">**TSCustomFieldSection::Line** – väli kuvatakse pärast valmis välju ajatabeli kirjetes.</span><span class="sxs-lookup"><span data-stu-id="633e8-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="633e8-163">Neid välju saavad olla redigeeritavad või kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="633e8-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="633e8-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="633e8-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="633e8-165">See atribuut määratleb välja, kui rakenduse pakutavad väärtused on andmebaasi tagasi salvestatud.</span><span class="sxs-lookup"><span data-stu-id="633e8-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="633e8-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="633e8-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="633e8-167">See atribuut määratleb välja, kui rakenduse pakutavad väärtused on andmebaasi tagasi salvestatud.</span><span class="sxs-lookup"><span data-stu-id="633e8-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="633e8-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="633e8-168">isEditable (NoYes)</span></span>

<span data-ttu-id="633e8-169">Määrake selle atribuudi väärtuseks **Jah** , kui soovite, et kasutajad saavad redigeerida välja ajatabeli kirje jaotises.</span><span class="sxs-lookup"><span data-stu-id="633e8-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="633e8-170">Määrake atribuudi väärtuseks **Ei** , et väli oleks kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="633e8-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="633e8-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="633e8-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="633e8-172">Määrake selle atribuudi väärtuseks **Jah** , kui soovite, et väli ajatabeli kirje jaotises on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="633e8-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="633e8-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="633e8-173">label (str)</span></span>

<span data-ttu-id="633e8-174">See atribuut määrab sildi, mis kuvatakse rakenduses välja kõrval.</span><span class="sxs-lookup"><span data-stu-id="633e8-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="633e8-175">stringOptions (List of Strings)</span><span class="sxs-lookup"><span data-stu-id="633e8-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="633e8-176">See atribuut rakendub ainult juhul, kui välja **fieldBaseType** väärtuseks on seatud **String**.</span><span class="sxs-lookup"><span data-stu-id="633e8-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="633e8-177">Kui **stringOptions** on seatud, siis stringi väärtused, mis on saadaval valikunuppude (raadionuppude) kaudu, määratakse loendis olevate stringide järgi.</span><span class="sxs-lookup"><span data-stu-id="633e8-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="633e8-178">Kui ühtegi stringi ei pakuta, lubatakse väljale string vabateksti sisestamine (vt jaotist "TSTimesheetEntryService klassi käsuliini kasutamine, et salvestada ajatabeli kirje rakendusest tagasi andmebaasi" edaspidi selles teemas).</span><span class="sxs-lookup"><span data-stu-id="633e8-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="633e8-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="633e8-179">stringLength (int)</span></span>

<span data-ttu-id="633e8-180">See atribuut määrab stringi välja maksimumpikkuse.</span><span class="sxs-lookup"><span data-stu-id="633e8-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="633e8-181">See rakendub ainult juhul, kui välja **fieldBaseType** väärtuseks on seatud **String**.</span><span class="sxs-lookup"><span data-stu-id="633e8-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="633e8-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="633e8-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="633e8-183">See atribuut määrab tegeliku välja jaoks kuvatavate kümnendkohtade arvu.</span><span class="sxs-lookup"><span data-stu-id="633e8-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="633e8-184">See rakendub ainult juhul, kui välja **fieldBaseType** väärtuseks on seatud **Real**.</span><span class="sxs-lookup"><span data-stu-id="633e8-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="633e8-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="633e8-185">orderSequence (int)</span></span>

<span data-ttu-id="633e8-186">See atribuut kontrollib, millises järjestuses kuvatakse kohandatud väljad rakenduses, kui määratud on rohkem kui üks kohandatud väli.</span><span class="sxs-lookup"><span data-stu-id="633e8-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="633e8-187">Väiksema arvuga väljad kuvatakse esimesena.</span><span class="sxs-lookup"><span data-stu-id="633e8-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="633e8-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="633e8-188">booleanValue (boolean)</span></span>

<span data-ttu-id="633e8-189">**Boolean** tüüpi väljade korral edastab see atribuut serveri ja rakenduse vahel oleva välja loogikaväärtuse.</span><span class="sxs-lookup"><span data-stu-id="633e8-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="633e8-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="633e8-190">guidValue (guid)</span></span>

<span data-ttu-id="633e8-191">**GUID** tüüpi väljade korral edastab see atribuut serveri ja rakenduse vahel oleva välja globaalse ainuidentifikaatori (GUID) väärtuse.</span><span class="sxs-lookup"><span data-stu-id="633e8-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="633e8-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="633e8-192">int64Value (int64)</span></span>

<span data-ttu-id="633e8-193">**Int64** tüüpi välja korral edastab see atribuut serveri ja rakenduse vahel oleva välja int64 väärtuse.</span><span class="sxs-lookup"><span data-stu-id="633e8-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="633e8-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="633e8-194">intValue (int)</span></span>

<span data-ttu-id="633e8-195">**Int** tüüpi välja korral edastab see atribuut serveri ja rakenduse vahel oleva välja int-väärtuse.</span><span class="sxs-lookup"><span data-stu-id="633e8-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="633e8-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="633e8-196">realValue (real)</span></span>

<span data-ttu-id="633e8-197">**Reaalarv** tüüpi välja korral edastab see atribuut serveri ja rakenduse vahel oleva välja reaalarvuväärtuse.</span><span class="sxs-lookup"><span data-stu-id="633e8-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="633e8-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="633e8-198">stringValue (str)</span></span>

<span data-ttu-id="633e8-199">**String** tüüpi välja korral edastab see atribuut serveri ja rakenduse vahel oleva välja stringiväärtuse.</span><span class="sxs-lookup"><span data-stu-id="633e8-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="633e8-200">Seda kasutatakse ka **Reaalarvu** tüüpi väljadel, mis on vormindatud valuutana.</span><span class="sxs-lookup"><span data-stu-id="633e8-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="633e8-201">Nende väljade jaoks kasutatakse atribuuti valuutatähise edastamiseks rakendusse.</span><span class="sxs-lookup"><span data-stu-id="633e8-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="633e8-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="633e8-202">dateValue (date)</span></span>

<span data-ttu-id="633e8-203">**Kuupäev** tüüpi välja korral edastab see atribuut serveri ja rakenduse vahel oleva välja kuupäevaväärtuse.</span><span class="sxs-lookup"><span data-stu-id="633e8-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="633e8-204">Kohandatud välja kuvamine ja salvestamine ajatabeli kirje jaotises</span><span class="sxs-lookup"><span data-stu-id="633e8-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="633e8-205">Allpool on pilt mobiilirakendusest ajatabeli kirje loomise kohta.</span><span class="sxs-lookup"><span data-stu-id="633e8-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="633e8-206">See näitab valmis välju ja kohandatud välja jaotises Ajakanne nimega Teststring, mille loeteluväärtus Teine variant on juba seatud.</span><span class="sxs-lookup"><span data-stu-id="633e8-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Testistringi kohandatud väli rakenduses](media/timesheet-entry.jpg)



<span data-ttu-id="633e8-208">Allpool on pilt mobiilirakenduse kasutajast, kes valib ühe loetelusuvanditest, mis on saadaval Testistringi kohandatud välja jaoks.</span><span class="sxs-lookup"><span data-stu-id="633e8-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="633e8-209">Kaks valikut Esimene valik ja Teine valik on kuvatud raadionuppudena.</span><span class="sxs-lookup"><span data-stu-id="633e8-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="633e8-210">Teine suvand on praegu valitud.</span><span class="sxs-lookup"><span data-stu-id="633e8-210">The second option is currently selected.</span></span>

![Testistringi kohandatud välja valikunupud (raadionupud)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="633e8-212">Laiendage TSTimesheetLine tabelit, et sellel oleks kohandatud väli</span><span class="sxs-lookup"><span data-stu-id="633e8-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="633e8-213">Tüüpilistes stsenaariumides salvestatakse tõenäoliselt ajatabeli kirje jaotises kohandatud välja andmed TSTimesheetLine tabelisse.</span><span class="sxs-lookup"><span data-stu-id="633e8-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="633e8-214">Kuid muid tabeleid saab kasutada juhul, kui andmete toomisel lähtutakse TSTimesheetTrans kirjest, mis on esitatud või millel pole kindlat kirje konteksti (näiteks juhul, kui see väli on seatud projekti parameetrites kirjutuskaitstuks).</span><span class="sxs-lookup"><span data-stu-id="633e8-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="633e8-215">Pange tähele, et kohandatud väljadel ei pea olema andmebaasi kirjete varundamist.</span><span class="sxs-lookup"><span data-stu-id="633e8-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="633e8-216">Neid saab dünaamiliselt genereerida X++ loogika põhjal.</span><span class="sxs-lookup"><span data-stu-id="633e8-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="633e8-217">See lähenemine võib olla kasulik kirjutuskaitstud stsenaariumides (vt jaotist "TSTimesheetDetails klassis käsuahela kasutamine, buildCustomFieldListForHeader meetod, et täita ajatabeli üksikasjad" dünaamiliselt loodud kohandatud väljaväärtuste näitena.)</span><span class="sxs-lookup"><span data-stu-id="633e8-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="633e8-218">Allpool on ekraanipilt Visual Studio rakendusobjektide puust.</span><span class="sxs-lookup"><span data-stu-id="633e8-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="633e8-219">See näitab TSTimesheetLine tabeli laiendust, mille väli TestLineString on lisatud kohandatud väljana.</span><span class="sxs-lookup"><span data-stu-id="633e8-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Reastring](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="633e8-221">Kasutage TSTimesheetSettings klassi buildCustomFieldList meetodi käsuahelat, et kuvada väli ajatabeli kirje jaotises</span><span class="sxs-lookup"><span data-stu-id="633e8-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="633e8-222">See kood reguleerib rakenduses välja kuvasätted.</span><span class="sxs-lookup"><span data-stu-id="633e8-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="633e8-223">Näiteks kontrollib see väljatüüpi, silti, olenemata sellest, kas väli on kohustuslik ja millises jaotises väli kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="633e8-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="633e8-224">Järgmises näites on kuvatud stringiväli ajakannetes.</span><span class="sxs-lookup"><span data-stu-id="633e8-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="633e8-225">Sellel väljal on kaks suvandit, **Esimene suvand** ja **Teine suvand** , mis on saadaval valikunuppude (raadionupud) kaudu.</span><span class="sxs-lookup"><span data-stu-id="633e8-225">This field has two options, **First option** and **Second option** , that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="633e8-226">Rakenduse väli on seostatud **TestLineString** väljaga, mis lisatakse tabelisse TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="633e8-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="633e8-227">Pange tähele **TSTimesheetCustomField::newFromMetatdata()** meetodi kasutamist kohandatud väljaatribuutide lähtestamise lihtsustamiseks: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** ja **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="633e8-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** , and **numberOfDecimals**.</span></span> <span data-ttu-id="633e8-228">Soovi korral saate need parameetrid määrata ka käsitsi.</span><span class="sxs-lookup"><span data-stu-id="633e8-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="633e8-229">Kasutage TSTimesheetEntry klassi buildCustomFieldListForEntry meetodi käsuahelat, et sisestada väärtused ajatabeli kirjesse</span><span class="sxs-lookup"><span data-stu-id="633e8-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="633e8-230">**buildCustomFieldListForEntry** meetodi abil sisestatakse mobiilirakenduses salvestatud ajatabeli ridadele väärtused.</span><span class="sxs-lookup"><span data-stu-id="633e8-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="633e8-231">See võtab TSTimesheetTrans kirjet parameetrina.</span><span class="sxs-lookup"><span data-stu-id="633e8-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="633e8-232">Selle kirje välju saab kasutada rakenduse kohandatud välja väärtuse täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="633e8-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="633e8-233">TSTimesheetEntryService klassis saate kasutada käsuliini, et salvestada ajatabeli kirje rakendusest tagasi andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="633e8-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="633e8-234">Kohandatud välja salvestamiseks tagasi andmebaasi tüüpilises kasutuses peate laiendama mitut viisi.</span><span class="sxs-lookup"><span data-stu-id="633e8-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="633e8-235">**timesheetLineNeedsUpdating** meetodit kasutatakse selleks, et teha kindlaks, kas kasutaja on rakenduses muutnud reakirjet ja see tuleb salvestada andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="633e8-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="633e8-236">Kui jõudlus pole mure, saab seda meetodit lihtsustada, et see tagastaks alati väärtuse **tõene**.</span><span class="sxs-lookup"><span data-stu-id="633e8-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="633e8-237">**populateTimesheetLineFromEntryDuringCreate** ja **populateTimesheetLineFromEntryDuringUpdate** meetodeid saab laiendada nii, et nad sisestavad väärtused TSTimesheetLine-i andmebaasikirjesse esitatud TSTimesheetEntry andmete lepingukirjest.</span><span class="sxs-lookup"><span data-stu-id="633e8-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="633e8-238">Järgnevas näites märkate, et andmebaasi välja ja kirje välja vastendamine toimub käsitsi X++ koodi kaudu.</span><span class="sxs-lookup"><span data-stu-id="633e8-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="633e8-239">**populateTimesheetWeekFromEntry** meetodit saab pikendada ka juhul, kui **TSTimesheetEntry** objektile vastendatud kohandatud väli peab kirjutama tagasi TSTimesheetLineweek andmebaasi tabelisse.</span><span class="sxs-lookup"><span data-stu-id="633e8-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="633e8-240">Järgmises näites salvestatakse **firstOption** või **secondOption** väärtus, mille kasutaja valib andmebaasile töötlemata stringi väärtusena.</span><span class="sxs-lookup"><span data-stu-id="633e8-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="633e8-241">Kui andmebaasi väli on **loendi** tüüpi väli, saab neid väärtusi käsitsi vastendada loendi väärtusega ja salvestada seejärel andmebaasi tabeli väljale loend.</span><span class="sxs-lookup"><span data-stu-id="633e8-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="633e8-242">Kohandatud välja kuvamine ajatabeli päise jaotises</span><span class="sxs-lookup"><span data-stu-id="633e8-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="633e8-243">Allpool on pilt mobiilirakenduse kasutajast, kes vaatab ajatabelit.</span><span class="sxs-lookup"><span data-stu-id="633e8-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="633e8-244">Ülemises parempoolses nurgas on valitud nupp Rohkem teavet, et kuvada suvandit Kuva rohkem üksikasju.</span><span class="sxs-lookup"><span data-stu-id="633e8-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Käsk Kuva rohkem üksikasju](media/show-more.png)

<span data-ttu-id="633e8-246">Allpool on pilt mobiilirakendusest, kus kuvatakse ajatabeli jaotist Rohkem.</span><span class="sxs-lookup"><span data-stu-id="633e8-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="633e8-247">Kohandatud väli nimega "Selle ajatabeli kasutamise määr (arvutatud kohandatud väli)" on lisatud ajatabeli päise jaotisse.</span><span class="sxs-lookup"><span data-stu-id="633e8-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="633e8-248">Kohandatud väljale seatakse kirjutuskaitstud väärtus 0,667.</span><span class="sxs-lookup"><span data-stu-id="633e8-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Jaotis Rohkem](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="633e8-250">Laiendage TSTimesheetTable tabelit, et sellel oleks kohandatud väli</span><span class="sxs-lookup"><span data-stu-id="633e8-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="633e8-251">Tüüpilistes stsenaariumides tõmmatakse tõenäoliselt päise jaotise kohandatud välja andmed TSTimesheetHeader tabelist.</span><span class="sxs-lookup"><span data-stu-id="633e8-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="633e8-252">Kuid muid tabeleid saab kasutada juhul, kui andmete toomisel lähtutakse TSTimesheetTable kirjest, mis on esitatud või millel pole kindlat kirje konteksti (näiteks juhul, kui see väli on seatud projekti parameetrites kirjutuskaitstuks).</span><span class="sxs-lookup"><span data-stu-id="633e8-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="633e8-253">Pange tähele, et kohandatud väljadel ei pea olema andmebaasi kirjete varundamist.</span><span class="sxs-lookup"><span data-stu-id="633e8-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="633e8-254">Neid saab dünaamiliselt genereerida X++ loogika põhjal.</span><span class="sxs-lookup"><span data-stu-id="633e8-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="633e8-255">Järgnev näide näitab seda lähenemist.</span><span class="sxs-lookup"><span data-stu-id="633e8-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="633e8-256">Päise jaotise väljad on rakenduses alati kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="633e8-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="633e8-257">Kasutage TSTimesheetSettings klassi buildCustomFieldList meetodi käsuliini, et kuvada väli ajatabeli päise jaotises</span><span class="sxs-lookup"><span data-stu-id="633e8-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="633e8-258">See kood reguleerib rakenduses välja kuvasätted.</span><span class="sxs-lookup"><span data-stu-id="633e8-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="633e8-259">Näiteks kontrollib see väljatüüpi, silti, olenemata sellest, kas väli on kohustuslik ja millises jaotises väli kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="633e8-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="633e8-260">Järgmises näites kuvatakse arvutatud väärtus rakenduse päisejaotises.</span><span class="sxs-lookup"><span data-stu-id="633e8-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="633e8-261">Kasutage TSTimesheetDetails klassi buildCustomFieldListForHeader meetodi käsuliini, et sisestada väärtused ajatabeli üksikasjadesse</span><span class="sxs-lookup"><span data-stu-id="633e8-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="633e8-262">**buildCustomFieldListForHeader** meetodi abil sisestatakse mobiilirakendusse ajatabeli päise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="633e8-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="633e8-263">See võtab TSTimesheetTable kirjet parameetrina.</span><span class="sxs-lookup"><span data-stu-id="633e8-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="633e8-264">Selle kirje välju saab kasutada rakenduse kohandatud välja väärtuse täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="633e8-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="633e8-265">Järgmises näites ei loeta andmebaasist ühtegi väärtust.</span><span class="sxs-lookup"><span data-stu-id="633e8-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="633e8-266">Selle asemel kasutatakse X++ loogikat, et luua arvutatud väärtus, mis kuvatakse rakenduses.</span><span class="sxs-lookup"><span data-stu-id="633e8-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="633e8-267">Muud konfigureerimise/laiendatavuse võimalused</span><span class="sxs-lookup"><span data-stu-id="633e8-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="633e8-268">Rakendusele täiendava valideerimise lisamine</span><span class="sxs-lookup"><span data-stu-id="633e8-268">Adding additional validation for the app</span></span>

<span data-ttu-id="633e8-269">Ajatabeli funktsionaalsuse andmebaasi taseme olemasolev loogika töötab endiselt ootuspäraselt.</span><span class="sxs-lookup"><span data-stu-id="633e8-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="633e8-270">Salvestamise või edastamise lõpuleviimise katkestamiseks ja kindla tõrketeate kuvamiseks saate lisada koodile **tõrketeate ("sõnum kasutajale")** käsulaienduste liini kaudu.</span><span class="sxs-lookup"><span data-stu-id="633e8-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="633e8-271">Siin on kasulike laiendusmeetodite kolm näidet.</span><span class="sxs-lookup"><span data-stu-id="633e8-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="633e8-272">Kui **validateWrite** TSTimesheetLine tabelis tagastab väärtuse **vale** ajatabeli rea salvestamisel, kuvatakse mobiilirakenduses tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="633e8-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="633e8-273">Kui **validateSubmit** TSTimesheetTable tabelis tagastab väärtuse **vale** ajatabeli rea salvestamisel rakenduses, kuvatakse kasutajale tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="633e8-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="633e8-274">Loogika, mis täidab väljad (näiteks **Reaatribuut** ) **sisestamise** meetodi ajal TSTimesheetLine tabelisse toimib ikka.</span><span class="sxs-lookup"><span data-stu-id="633e8-274">Logic that fills in fields (for example, **Line Property** ) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="633e8-275">Valmis väljade peitmine ja märkimine konfiguratsiooni kaudu kirjutuskaitstuks</span><span class="sxs-lookup"><span data-stu-id="633e8-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="633e8-276">Mobiilirakenduses saate projektiparameetrites teha valmisväljad kirjutuskaitstuks või peidetuks.</span><span class="sxs-lookup"><span data-stu-id="633e8-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="633e8-277">Seadistage suvandid jaotise **Mobiili ajatabelid** vahekaardi **Ajatabel** lehel **Projekti haldamise ja raamatupidamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="633e8-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projekti parameetrid](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="633e8-279">Laienduste kaudu valimiseks saadaolevate tegevuste muutmine</span><span class="sxs-lookup"><span data-stu-id="633e8-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="633e8-280">Projekti jaoks valimiseks saadaolevad tegevused täidetakse meetodite **getActivitiesForProject()** ja **getActivityQuery()** abil **TsTimesheetProjectService** klassis.</span><span class="sxs-lookup"><span data-stu-id="633e8-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="633e8-281">Võite kasutada käsuahelat, et muuta seda käitumist vastavalt teie äristsenaariumile tegevuste jaoks, mis on saadaval valimiseks mõne kindla projekti jaoks.</span><span class="sxs-lookup"><span data-stu-id="633e8-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="633e8-282">Vaikimisi projekti kategooria sisestamine ajatabeli kirjetele</span><span class="sxs-lookup"><span data-stu-id="633e8-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="633e8-283">Vaikimisi projekti kategooria sisestamine ajatabeli kirjetele toimub kolmel tasemel.</span><span class="sxs-lookup"><span data-stu-id="633e8-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="633e8-284">Saate kasutada käsuahelat, et laiendada käitumist mis tahes või kõigil nendel tasemetel, et saavutada soovitud käitumist.</span><span class="sxs-lookup"><span data-stu-id="633e8-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="633e8-285">Kasutatakse järgmist hierarhiat.</span><span class="sxs-lookup"><span data-stu-id="633e8-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="633e8-286">Rakendus proovib panna vaikimisi kategooria projekti ressursist.</span><span class="sxs-lookup"><span data-stu-id="633e8-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="633e8-287">See vaikekategooria seatakse **getCurrentUserResource** ja **getDelegatedResourcesForCurrentUser** meetodite kaudu klassis **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="633e8-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="633e8-288">Kui vaikekategooriat ei pakuta projektiressursi tasemel, proovib rakendus seda projektitegevusest tõmmata.</span><span class="sxs-lookup"><span data-stu-id="633e8-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="633e8-289">See vaikekategooria seatakse meetodis **getActivitiesForProject** klassis **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="633e8-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="633e8-290">Kui vaikekategooriat ei pakuta projektitegevuse tasemel, võetakse vaikekategooria projektiparameetritest.</span><span class="sxs-lookup"><span data-stu-id="633e8-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="633e8-291">See vaikekategooria seatakse meetodis **getProjectDetailsbyRule** klassis **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="633e8-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
