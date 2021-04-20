---
title: Projektipõhiste lepinguridade ülevaade
description: See teema sisaldab teavet projektipõhiste lepinguridadega töötamise kohta.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858153"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="fe6f1-103">Projektipõhiste lepinguridade ülevaade</span><span class="sxs-lookup"><span data-stu-id="fe6f1-103">Project-based contract lines overview</span></span>

<span data-ttu-id="fe6f1-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="fe6f1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fe6f1-105">Rakenduse Dynamics 365 Project Operations projektipõhised lepinguread on loodud sisaldama suhtluse projekti töö konkreetsete komponentide prognoose ja arvelduse kokkuleppeid.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="fe6f1-106">Projektipõhise lepingurea struktuur on laiendatud projekti prognooside ja arveldamise stsenaariumide jaoks järgmiste kontseptsioonidega.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="fe6f1-107">Arveldusmeetod</span><span class="sxs-lookup"><span data-stu-id="fe6f1-107">Billing method</span></span>
- <span data-ttu-id="fe6f1-108">Projekti ja ülesannete vastendamine</span><span class="sxs-lookup"><span data-stu-id="fe6f1-108">Project and task mapping</span></span>
- <span data-ttu-id="fe6f1-109">Kaasatud tehingu klassid</span><span class="sxs-lookup"><span data-stu-id="fe6f1-109">Included transaction classes</span></span>
- <span data-ttu-id="fe6f1-110">Mitteületatav limiit</span><span class="sxs-lookup"><span data-stu-id="fe6f1-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="fe6f1-111">Arveldatavuse seadistus</span><span class="sxs-lookup"><span data-stu-id="fe6f1-111">Chargeability setup</span></span>
- <span data-ttu-id="fe6f1-112">Lepingurea üksikasju kasutavad prognoosid</span><span class="sxs-lookup"><span data-stu-id="fe6f1-112">Estimates using contract line details</span></span>
- <span data-ttu-id="fe6f1-113">Lepingurea kliendid</span><span class="sxs-lookup"><span data-stu-id="fe6f1-113">Contract line customers</span></span>

<span data-ttu-id="fe6f1-114">Järgmises tabelis on toodud projektopõhiste lepinguridade vahekaardi **Üldine** väljad, mis aitavad häälestada projektipõhise töö üksikasjaliku algusest lõpuni prognoosi ja arvelduse korraldusi.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="fe6f1-115">Väli</span><span class="sxs-lookup"><span data-stu-id="fe6f1-115">Field</span></span> | <span data-ttu-id="fe6f1-116">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="fe6f1-116">Description</span></span> | <span data-ttu-id="fe6f1-117">Allavoolu mõjud</span><span class="sxs-lookup"><span data-stu-id="fe6f1-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fe6f1-118">**Nimi**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-118">**Name**</span></span> | <span data-ttu-id="fe6f1-119">Lepingure nimi.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-119">Name of the contract line.</span></span> <span data-ttu-id="fe6f1-120">See määratleb prognoositava lepingu diskreetse komponendi.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="fe6f1-121">Hinnapakkumise põhjal loodud projektilepingu puhul kopeeritakse see väärtus projektipõhise hinnapakkumise rea vastavast väärtusest.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="fe6f1-122">Projekti arvereale kopeeritav nimi, mis luuakse arve loomise ajal lepingureast.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="fe6f1-123">**Arveldusmeetod**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-123">**Billing Method**</span></span> | <span data-ttu-id="fe6f1-124">Hinnapakkumise põhjal loodud projektilepingu puhul kopeeritakse see väärtus projektipõhise hinnapakkumise rea vastavalt väljalt.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="fe6f1-125">See on suvandikomplekt, mis tähistab rakenduse Project Operations kahte peamist toetatavat lepingumudelit.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="fe6f1-126">- **Fikseeritud hind**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-126">- **Fixed Price**</span></span></br><span data-ttu-id="fe6f1-127">- **Aeg ja materjal**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-127">- **Time and Material**</span></span> | <span data-ttu-id="fe6f1-128">Vastavalt viidatud lepingurea arveldusmeetodile käsitletakse tegelikku kannet.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="fe6f1-129">Kui tegeliku näitaja poolt viidatud lepungureal on aja ja materjali arveldusmeetod, luuakse kulu ja arveldamata müügi tegelike näitajate kirjed.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="fe6f1-130">Kui tegeliku näitaja viidatud lepingureal on fikseeritud arveldusmeetod, luuakse ainult tegelik kulu.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="fe6f1-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-131">**Project**</span></span> | <span data-ttu-id="fe6f1-132">Selle välja abil saate tuvastada projekti, mida kasutatakse selle tegevusega seotud tööde pakkumiseks.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="fe6f1-133">Seda väärtust kasutatakse koos suvanditega **Kaasatud tööülesanded** ja **Kaasatud tehinguklassid**, et lahendada tegelikul või prognoositud reakirjel lepingurea viide.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="fe6f1-134">**Kaasatud ülesanded**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-134">**Included Tasks**</span></span> | <span data-ttu-id="fe6f1-135">Näitab, kas see lepingurida sisaldab valitud projekti kõiki projekti ülesandeid või ainult ülesannete alamhulka.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="fe6f1-136">See on suvandikomplekt, millel on järgmised võimalikud väärtused.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="fe6f1-137">- **Kõik projekti ülesanded**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-137">- **All Project Tasks**</span></span></br><span data-ttu-id="fe6f1-138">- **Ainult valitud projekti ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="fe6f1-139">Selle välja tühi väärtus võrdub suvandi **Kõik projekti ülesanded** valimisega.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="fe6f1-140">Kui valitud on suvand **Aiult valitud ülesanded**, saate valida konkreetsed ülesanded ja seostada need vahekaardil **Ülesande arvelduse seadistus** lehel **Projekt** selle lepingureaga.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="fe6f1-141">Väärtust kasutatakse koos klassidega **Projekt** ja **Kaasatud tehingud**, et lahendada lepingurea viidet tegelikule või prognoositavale rea kirjele.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="fe6f1-142">**Kaasa aeg**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-142">**Include Time**</span></span> | <span data-ttu-id="fe6f1-143">Väärtus **Jah**/**Ei** näitab, kas valitud projekti tehingu või tööjõu maksumused lisatakse sellele lepingureale.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="fe6f1-144">Väärtus **Ei** näitab, et ajakandeid ega tööjõukulusid ei kaasata sellele lepingureale.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="fe6f1-145">Väärtus **Jah** näitab, et kaasatakse.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="fe6f1-146">Seda väärtust kasutatakse seoses projektiga, et lahendada lepingurea kirje tegelikul või prognoositud rea kirjel.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="fe6f1-147">**Kaasa kulu**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-147">**Include Expense**</span></span> | <span data-ttu-id="fe6f1-148">Väärtus **Jah**/**Ei** näitab, kas valitud projekti kulu maksumused lisatakse sellele lepingureale.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="fe6f1-149">Väärtus **Ei** näitab, et kulude maksumust ei kaasata sellele lepingureale.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="fe6f1-150">Väärtus **Jah** näitab, et kaasatakse.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="fe6f1-151">Seda väärtust kasutatakse seoses projektiga, et lahendada lepingurea kirje tegelikul või prognoositud rea kirjel.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="fe6f1-152">**Kaasa materjalid**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-152">**Include Materials**</span></span> | <span data-ttu-id="fe6f1-153">Väärtus **Jah**/**Ei** näitab, kas valitud projekti materjali maksumused lisatakse sellele lepingureale.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="fe6f1-154">Väärtus **Ei** näitab, et materjali maksumust ei lisata sellele lepingureale.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="fe6f1-155">Väärtus **Jah** näitab, et kaasatakse.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="fe6f1-156">Seda väärtust kasutatakse seoses projektiga, et lahendada lepingurea kirje tegelikul või prognoositud rea kirjel.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="fe6f1-157">**Kaasa tasu**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-157">**Include Fee**</span></span> | <span data-ttu-id="fe6f1-158">Väärtus **Jah**/**Ei** näitab, kas valitud projekti tasud lisatakse sellele lepingureale.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="fe6f1-159">Väärtus **Ei** näitab, et tasusid ei kaasata sellele lepingureale.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="fe6f1-160">Väärtus **Jah** näitab, et kaasatakse.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="fe6f1-161">Seda väärtust kasutatakse seoses projektiga, et lahendada lepingurea kirje tegelikul või prognoositud rea kirjel.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="fe6f1-162">**Lepingu summa**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-162">**Contracted Amount**</span></span> | <span data-ttu-id="fe6f1-163">Fikseeritud hinnaga lepingurea puhul on see summa kokkulepitud väärtus, mille eest saadetakse kliendile arve kõikide selle lepingureaga seostatud töökomponentide eest.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="fe6f1-164">Aja ja materjali lepingurea puhul on see summa prognoositav väärtus, mille eest saadetakse kliendile arve kõikide selle lepingureaga seostatud töökomponentide eest.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="fe6f1-165">Hinnapakkumisest loodud loodud projektilepingu puhul kopeeritakse see väärtus projektipõhise hinnapakkumise rea vastavalt väljalt.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="fe6f1-166">Kui projektipõhisel lepingureal on rea üksikasjad, lukustatakse see väli redigeerimiseks ja see summeeritakse lepingurea üksikasjade summa põhjal.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="fe6f1-167">Kui lepingureal on rea üksikasjad olemas, saab seda väärtust muuta, muutes rea üksikasjade summasid.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="fe6f1-168">Fikseeritud hinnaga lepingurea korral kasutatakse seda väärtust perioodilise arvelduse vahe-eesmärkide maksueelse summa loomiseks.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="fe6f1-169">**Hinnanguline maks**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-169">**Estimated Tax**</span></span> | <span data-ttu-id="fe6f1-170">Kasutaja saab seda välja redigeerida, et sisestada lepingurea eeldatav maksusumma.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="fe6f1-171">Kui projektipõhisel lepingureal on rea üksikasjad, lukustatakse see väli redigeerimiseks ja see summeeritakse lepingurea üksikasjade maksusumma põhjal.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="fe6f1-172">Kui lepingureal on rea üksikasjad olemas, saab seda väärtust muuta, muutes rea üksikasjade maksusummasid.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="fe6f1-173">Fikseeritud hinnaga lepingurea korral kasutatakse seda väärtust perioodilise arvelduse vahe-eesmärkide maksusumma loomiseks.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="fe6f1-174">**Lepingu summa pärast maksu mahaarvamist**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="fe6f1-175">Lepingu summa pärast maksu mahaarvamist.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-175">The contract line amount after tax.</span></span> <span data-ttu-id="fe6f1-176">See väli on kirjutuskaitstud ja arvutatakse järgnevalt: **lepingu summa + maks**.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="fe6f1-177">Fikseeritud hinnaga lepingurea korral kasutatakse seda väärtust perioodilise arvelduse vahe-eesmärkide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="fe6f1-178">**Mitteületatav limiit**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="fe6f1-179">Kasutaja saab seda välja redigeerida ja see on saadaval ainult projektipõhistel lepinguridadel, millel on määratud aja ja materjali põhjal arvete esitamise meetod.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="fe6f1-180">Kasutaja saab seda välja redigeerida.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-180">The user can edit this field.</span></span> <span data-ttu-id="fe6f1-181">Kui aja- ja materjalikulu tegelikud näitajad viitavad selle lepingurea ajale ja materjalile, hinnatakse tegeliku näitaja summa lepingurea mitte ületatava limiidiga võrreldes.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="fe6f1-182">See hindamine lõpetatakse pärast juba kulutatud ja kinnitatud summade arvestamist.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="fe6f1-183">**Kliendi eelarve**</span><span class="sxs-lookup"><span data-stu-id="fe6f1-183">**Customer Budget**</span></span> | <span data-ttu-id="fe6f1-184">See väli on redigeeritav ja kopeeritakse hinnapakkumise rea vastavalt väljalt, kui lepingu loodi hinnapakkumisest.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="fe6f1-185">Seda välja kasutatakse ainult teavitamiseks ja sellel pole allavoolu tähtsust.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="fe6f1-186">Projektipõhiste lepinguridade vahekaardi Üldine valikute valideerimisreeglid</span><span class="sxs-lookup"><span data-stu-id="fe6f1-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="fe6f1-187">1. reegel: kui väli **Kaasatud ülesanded** on tühi või määratud väärtusele **Kõik projekti ülesanded**, kaasatakse lepingureale kõik projekti ülesanded.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="fe6f1-188">2. reegel: kui väli **Kaasatud ülesanded** on tühi või otse määratud valikule **Kõik projekti ülesanded**, saab projekti ja teatud tehinguklassid kaasata ainult ühele lepingu projektipõhisele lepingureale.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="fe6f1-189">3. reegel: kui väli **Kaasatud ülesanded** on määratud valikule **Ainult valitud projekti ülesanded**, saab projekti ja teatud tehinguklassid kaasata mitmele lepingu projektipõhisele lepingureale.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="fe6f1-190">
                    <strong>Leping</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fe6f1-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fe6f1-191">
                    <strong>Lepingurida</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fe6f1-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fe6f1-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fe6f1-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="fe6f1-193">
                    <strong>Kaasatud ülesanded</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fe6f1-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="fe6f1-194">
                    <strong>Kaasa aeg</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fe6f1-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="fe6f1-195">
                    <strong>Kaasa kulu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fe6f1-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fe6f1-196">
                    <strong>Kaasa materjalid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fe6f1-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fe6f1-197">
                    <strong>Kaasamine</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fe6f1-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="fe6f1-198">
                    <strong>Tasu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fe6f1-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="fe6f1-199">
                    <strong>Kehtiv/kehtetu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fe6f1-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="fe6f1-200">
                    <strong>Põhjus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fe6f1-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fe6f1-201">C1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fe6f1-202">CL1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-203">P1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fe6f1-204">Tühi</span><span class="sxs-lookup"><span data-stu-id="fe6f1-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-205">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-206">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-207">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-208">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fe6f1-209">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="fe6f1-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fe6f1-210">Reegli nr 2 rikkumine.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-210">Violation of Rule #2.</span></span> <span data-ttu-id="fe6f1-211">P1-projekti aeg, kulu, materjalid ja tasud on kaasatud nii lepingureale CL1 kui ka CL2.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fe6f1-212">C1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fe6f1-213">CL2</span><span class="sxs-lookup"><span data-stu-id="fe6f1-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-214">P1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fe6f1-215">Tühi</span><span class="sxs-lookup"><span data-stu-id="fe6f1-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-216">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-217">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-218">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-219">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fe6f1-220">C1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fe6f1-221">CL1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-222">P1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fe6f1-223">Tühi</span><span class="sxs-lookup"><span data-stu-id="fe6f1-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-224">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-225">No</span><span class="sxs-lookup"><span data-stu-id="fe6f1-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-226">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-227">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fe6f1-228">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="fe6f1-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fe6f1-229">Reegli nr 2 rikkumine.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-229">Violation of Rule #2.</span></span> <span data-ttu-id="fe6f1-230">P1-projekti aeg, materjalid ja tasud on kaasatud nii lepingureale CL1 kui ka CL2.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fe6f1-231">C1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fe6f1-232">CL2</span><span class="sxs-lookup"><span data-stu-id="fe6f1-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-233">P1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fe6f1-234">Tühi</span><span class="sxs-lookup"><span data-stu-id="fe6f1-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-235">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-236">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-237">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-238">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fe6f1-239">C1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fe6f1-240">CL1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-241">P1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fe6f1-242">Tühi</span><span class="sxs-lookup"><span data-stu-id="fe6f1-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-243">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-244">No</span><span class="sxs-lookup"><span data-stu-id="fe6f1-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-245">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-246">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fe6f1-247">Sobiv</span><span class="sxs-lookup"><span data-stu-id="fe6f1-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fe6f1-248">P1-projekti aeg, materjale ja tasud on kaasatud reale CL1.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="fe6f1-249">P1-projekti kulu on kaasatud reale CL2.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="fe6f1-250">Igal lepingureal sisalduv ei kattu ja on seetõttu kehtiv.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fe6f1-251">C1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fe6f1-252">CL2</span><span class="sxs-lookup"><span data-stu-id="fe6f1-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-253">P1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fe6f1-254">Tühi</span><span class="sxs-lookup"><span data-stu-id="fe6f1-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-255">No</span><span class="sxs-lookup"><span data-stu-id="fe6f1-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-256">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-257">No</span><span class="sxs-lookup"><span data-stu-id="fe6f1-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-258">No</span><span class="sxs-lookup"><span data-stu-id="fe6f1-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fe6f1-259">C1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fe6f1-260">CL1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-261">P1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fe6f1-262">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="fe6f1-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-263">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-264">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-265">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-266">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fe6f1-267">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="fe6f1-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fe6f1-268">Reegli nr 2 rikkumine</span><span class="sxs-lookup"><span data-stu-id="fe6f1-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="fe6f1-269">C1 sisaldab aega, materjale, kulusid ja tasusid P1-projekti ülesannete alamhulgas.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fe6f1-270">CL2 hõlmab kogu projektiga P1 seotud aega, materjale, kulutusi ja tasusid ning seega kattub see sellega, mis on kaasatud C1-te.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fe6f1-271">C1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fe6f1-272">CL2</span><span class="sxs-lookup"><span data-stu-id="fe6f1-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-273">P1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fe6f1-274">Tühi</span><span class="sxs-lookup"><span data-stu-id="fe6f1-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-275">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-276">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-277">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-278">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fe6f1-279">C1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fe6f1-280">CL1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-281">P1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fe6f1-282">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="fe6f1-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-283">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-284">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-285">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-286">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fe6f1-287">Sobiv</span><span class="sxs-lookup"><span data-stu-id="fe6f1-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fe6f1-288">Reegli nr 3 kohta</span><span class="sxs-lookup"><span data-stu-id="fe6f1-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="fe6f1-289">C1 sisaldab aega, kulusid, materjale ja tasusid P1-projekti ülesannete alamhulgas.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fe6f1-290">CL2 sisaldab aega, kulusid, materjale ja tasusid P1-projekti ülesannete alamhulgas.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fe6f1-291">Ainus täiendav valideerimine on CL1 toimingute alamhulga ümber, mis erineb CL2 tööülesannete alamhulgast, tagamaks, et seal poleks kattumisi.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="fe6f1-292">Seda teeb süsteem ülesannete sidumisel.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fe6f1-293">C1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fe6f1-294">CL2</span><span class="sxs-lookup"><span data-stu-id="fe6f1-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-295">P1</span><span class="sxs-lookup"><span data-stu-id="fe6f1-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fe6f1-296">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="fe6f1-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-297">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fe6f1-298">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-299">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fe6f1-300">Ja</span><span class="sxs-lookup"><span data-stu-id="fe6f1-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
