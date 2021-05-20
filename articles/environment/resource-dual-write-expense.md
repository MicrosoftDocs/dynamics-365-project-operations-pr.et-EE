---
title: Kuluhalduse integreerimine
description: Selles teemas antakse teavet kuluaruande integreerimise kohta Project Operationsiga, kasutades topeltkirjutamist.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c347f14f3a479eb4aec951cfe4094c5581bce32
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955737"
---
# <a name="expense-management-integration"></a><span data-ttu-id="1eee7-103">Kuluhalduse integreerimine</span><span class="sxs-lookup"><span data-stu-id="1eee7-103">Expense management integration</span></span>

<span data-ttu-id="1eee7-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="1eee7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1eee7-105">Selles teemas antakse teavet kuluaruannete integreerimise kohta Project Operationsis [täielik kulujuurutus](../expense/expense-overview.md), kasutades topeltkirjutamist.</span><span class="sxs-lookup"><span data-stu-id="1eee7-105">This topic provides information about expense reports integration in Project Operations [full expense deployment](../expense/expense-overview.md) using dual-write.</span></span>

## <a name="expense-categories"></a><span data-ttu-id="1eee7-106">Kulukategooriad</span><span class="sxs-lookup"><span data-stu-id="1eee7-106">Expense categories</span></span>

<span data-ttu-id="1eee7-107">Täieliku kulujuurutuse puhul luuakse ja hallatakse kulukategooriaid rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1eee7-107">In a full expense deployment, expense categories are created and maintained in Finance and Operations apps.</span></span> <span data-ttu-id="1eee7-108">Uue kulukategooria loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="1eee7-108">To create a new expense category, complete the following steps:</span></span>

1. <span data-ttu-id="1eee7-109">Looge Microsoft Dataverse’is kategooria **Kanne**.</span><span class="sxs-lookup"><span data-stu-id="1eee7-109">In Microsoft Dataverse, create a **Transaction** category.</span></span> <span data-ttu-id="1eee7-110">Topeltkirjutamise integreerimine sünkroonib selle kannete kategooria rakendustega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1eee7-110">Dual-write integration will synchronize this transaction category to Finance and Operations apps.</span></span> <span data-ttu-id="1eee7-111">Lisateavet leiate teemadest [Projektikategooriate konfigureerimine](/dynamics365/project-operations/project-accounting/configure-project-categories) ja [Project Operationsi seadistamise ja konfigureerimise andmeintegreerimine](resource-dual-write-setup-integration.md).</span><span class="sxs-lookup"><span data-stu-id="1eee7-111">For more information, see [Configure project categories](/dynamics365/project-operations/project-accounting/configure-project-categories) and [Project Operations setup and configuration data integration](resource-dual-write-setup-integration.md).</span></span> <span data-ttu-id="1eee7-112">Selle integreerimise tulemusena loob süsteem rakendustes Finance and Operations neli ühiskategooria kirjet.</span><span class="sxs-lookup"><span data-stu-id="1eee7-112">As a result of this integration, the system creates four shared category records in Finance and Operations apps.</span></span>
2. <span data-ttu-id="1eee7-113">Minge valikusse **Kulude haldus** > **Seadistamine** > **Jagatud kategooriad** ja valige jagatud kategooria **kulutehingu** klassiga.</span><span class="sxs-lookup"><span data-stu-id="1eee7-113">In Finance, go to **Expense management** > **Setup** > **Shared categories** and select a shared category with an **Expense** transaction class.</span></span> <span data-ttu-id="1eee7-114">Määrake parameetri **Kulus kasutatav** väärtuseks **Tõene** ja määrake kasutatava kulu tüüp.</span><span class="sxs-lookup"><span data-stu-id="1eee7-114">Set the **Can be used in Expense** parameter to **True** and define the expense type to use.</span></span>
3. <span data-ttu-id="1eee7-115">Looge selle jagatud kategooria kirje abil uus kulukategooria, valides suvandid **Kuluhaldus** > **Seadistus** > **Kulukategooriad** ja uue **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1eee7-115">Using this shared category record, create a new expense category by going to **Expense management** > **Setup** > **Expense categories** and selecting **New**.</span></span> <span data-ttu-id="1eee7-116">Kirje salvestamisel kasutab topeltkirjutamine tabelikaarti **Project Operationsi integreerimine projekti kulukategooriate ekspordi olem (msdyn\_expensecategories)**, et sünkroonida see kirje Dataverse’i.</span><span class="sxs-lookup"><span data-stu-id="1eee7-116">When the record is saved, dual-write uses the table map, **Project Operations integration project expense categories export entity (msdyn\_expensecategories)** to synchronize this record to Dataverse.</span></span>

  ![Kulukategooriate integreerimine](./media/DW6ExpenseCategories.png)

<span data-ttu-id="1eee7-118">Rakenduste Finance and Operations kulukategooriad on ettevõtte või juriidilise olemi põhised.</span><span class="sxs-lookup"><span data-stu-id="1eee7-118">Expense categories in Finance and Operations apps are company- or legal entity-specific.</span></span> <span data-ttu-id="1eee7-119">Dataverse’is on eraldi vastavad juriidilise isiku kirjed.</span><span class="sxs-lookup"><span data-stu-id="1eee7-119">There are separate, corresponding legal entity-specific records in Dataverse.</span></span> <span data-ttu-id="1eee7-120">Kui projektijuht prognoosib kulusid, ei saa ta valida projekti jaoks loodud kulukategooriaid, mille omanikuks on mõni muu ettevõte kui see, mille projektiga nad töötavad.</span><span class="sxs-lookup"><span data-stu-id="1eee7-120">When a project manager estimates expenses, they can’t select expense categories that were created for a project that is owned by a different company than the company that owns the project they are working on.</span></span> 

## <a name="expense-reports"></a><span data-ttu-id="1eee7-121">Kuluaruanded</span><span class="sxs-lookup"><span data-stu-id="1eee7-121">Expense reports</span></span>

<span data-ttu-id="1eee7-122">Kuluaruanded luuakse ja kinnitatakse rakendustes Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1eee7-122">Expense reports are created and approved in Finance and Operations apps.</span></span> <span data-ttu-id="1eee7-123">Lisateavet leiate teemast [Kuluaruannete loomine ja töötlemine rakenduses Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/).</span><span class="sxs-lookup"><span data-stu-id="1eee7-123">For more information, see [Create and process expense reports in Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/).</span></span> <span data-ttu-id="1eee7-124">Pärast seda, kui projektijuht on kuluaruande kinnitanud, sisestatakse see pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="1eee7-124">After the expense report is approved by the Project manager, it's posted to the general ledger.</span></span> <span data-ttu-id="1eee7-125">Project Operationsis sisestatakse projektiga seotud kuluaruande read spetsiaalsete sisestusreeglite abil.</span><span class="sxs-lookup"><span data-stu-id="1eee7-125">In Project Operations, project-related expense report lines are posted using special posting rules:</span></span>

  - <span data-ttu-id="1eee7-126">Projektiga seotud kulusid (sealhulgas tagastamatut maksu) ei kirjendata kohe pearaamatu projekti kulukontole, vaid need kantakse kulude integreerimise kontole.</span><span class="sxs-lookup"><span data-stu-id="1eee7-126">Project-related cost (including non-recoverable tax) is not immediately posted to project cost account in general ledger, but instead is posted to expense integration account.</span></span> <span data-ttu-id="1eee7-127">See konto on konfigureeritud jaotises **Projektihaldus ja raamatupidamine** > **Seadistus** > **Projektihaldus ja raamatupidamisparameetrid**, vahekaardil **Project Operations rakenduses Dynamics 365 Customer Engagement**.</span><span class="sxs-lookup"><span data-stu-id="1eee7-127">This account is configured in **Project management and accounting** > **Setup** > **Project management and accounting parameters**, **Project Operations on Dynamics 365 Customer engagement** tab.</span></span>
  - <span data-ttu-id="1eee7-128">Topeltkirjutamine sünkroonitakse Dataverse’is, kasutades **Project Operationsi integreerimise projektikulude ekspordi olemi (msdyn\_expenses)** tabelikaarti.</span><span class="sxs-lookup"><span data-stu-id="1eee7-128">Dual-write synchronizes to Dataverse using **Project Operations integration project expenses export entity (msdyn\_expenses)** table map.</span></span>
  - <span data-ttu-id="1eee7-129">Maksude allkirjastaja, hankija allkirjastaja ja muud finantssisestused kirjendatakse kuludeklaratsiooni postitamise hetke järgi.</span><span class="sxs-lookup"><span data-stu-id="1eee7-129">Tax subledger, vendor subledger, and other financial postings are recorded as applicable at the time of expense report posting.</span></span>

  ![Kuluaruannete integreerimine](./media/DW6ExpenseReports.png)

<span data-ttu-id="1eee7-131">Kui kirje kirjutatakse üksuses **Kulu**, käivitab süsteem kirje automaatse kinnitamise Dataverse’i protsessi.</span><span class="sxs-lookup"><span data-stu-id="1eee7-131">When a record is written to the **Expense** entity in Dataverse, the system triggers the automated approval process of the record.</span></span> <span data-ttu-id="1eee7-132">Vajaduse korral saab automaatse kinnitamise protsessi oleku üle vaadata, kui avate Dataverse’i jaotise **Täpsemad sätted** > **Süsteem** > **Süsteemitööd**.</span><span class="sxs-lookup"><span data-stu-id="1eee7-132">If needed, the automated approval process status can be reviewed in Dataverse by going to **Advanced settings** > **System** > **System jobs**.</span></span> <span data-ttu-id="1eee7-133">Pärast kinnitamise lõpetamist luuakse olemis **Tegelikud andmed** kulukande klassi kirjed.</span><span class="sxs-lookup"><span data-stu-id="1eee7-133">After approval is complete, expense transaction class records are created in the **Actuals** entity.</span></span>

<span data-ttu-id="1eee7-134">Kuluga seotud tegelikke andmeid töödeldakse seejärel, kasutades topeltkirjutamise tabelikaarti **Project Operationsi integreerimise tegelike andmetega (msdyn\_actuals)**.</span><span class="sxs-lookup"><span data-stu-id="1eee7-134">Expense related actuals are then processed using the dual-write table map **Project Operations integration actuals (msdyn\_actuals)**.</span></span> <span data-ttu-id="1eee7-135">Lisateavet leiate teemast [Projekti prognoosid ja tegelikud andmed](resource-dual-write-estimates-actuals.md).</span><span class="sxs-lookup"><span data-stu-id="1eee7-135">For more information, see [Project estimates and actuals](resource-dual-write-estimates-actuals.md).</span></span>

<span data-ttu-id="1eee7-136">Perioodiline protsess **Import koondatud andmetest** loob kuluaruandega seotud töölehe read Project Operationsi integreerimise protsessis.</span><span class="sxs-lookup"><span data-stu-id="1eee7-136">The periodic process, **Import from staging** creates Expense report-related journal lines in the Project Operations Integration journal.</span></span> <span data-ttu-id="1eee7-137">Vastaskonto vaikeväärtuseks on kulude integreerimise konto.</span><span class="sxs-lookup"><span data-stu-id="1eee7-137">The offset account defaults to the expense integration account.</span></span> <span data-ttu-id="1eee7-138">Konteerimise integreerimise tööleht tühjendab kulukande kontosaldo ja teisaldab kulusumma projekti kulukontole.</span><span class="sxs-lookup"><span data-stu-id="1eee7-138">The Posting integration journal clears the account balance for the expense transaction and moves the expense amount to the project cost account.</span></span> <span data-ttu-id="1eee7-139">Süsteem loob ka projekti alamandmikukanded järelarveldamiseks ja tulude kajastamiseks.</span><span class="sxs-lookup"><span data-stu-id="1eee7-139">The system also creates project subledger transactions for downstream invoicing and revenue recognition purposes.</span></span>