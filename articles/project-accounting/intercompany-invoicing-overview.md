---
title: Kontsernisisese arvelduse ülevaade
description: Selles teemas on toodud teave ja näited projektide kontsernisisese arveldamise kohta.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c1dcf642f79ce64cb83285ac6dc6d7eaf815145c
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369371"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="5465b-103">Kontsernisisese arvelduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="5465b-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="5465b-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="5465b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5465b-105">Teie organisatsioonis võib olla mitu allüksust, tütarettevõtet ja muud juriidilist isikut, kes edastavad üksteisele tooteid ja teenuseid projektidele.</span><span class="sxs-lookup"><span data-stu-id="5465b-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="5465b-106">Teenust või toodet pakkuva juriidilise isiku nimi on *laenu andev juriidiline olem*.</span><span class="sxs-lookup"><span data-stu-id="5465b-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="5465b-107">Teenust või toodet saava juriidilise isiku nimi on *laenav juriidiline olem*.</span><span class="sxs-lookup"><span data-stu-id="5465b-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="5465b-108">Järgmisel pildil on kujutatud tüüpiline stsenaarium, kus kaks juriidilist üksust: Contoso Robotics USA (laenav juriidiline isik) ja Contoso Robotics UK (laenu andev juriidiline isik) jagavad ressursse projekti kohale toimetamiseks kliendile Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="5465b-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="5465b-109">Selle stsenaariumi puhul sõlmtakse ettevõttele Adventure Works töö tegemiseks leping ettevõttega Contoso Robotics USA.</span><span class="sxs-lookup"><span data-stu-id="5465b-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Kontsernisisesed arved](./media/IntercompanyScenario.png) 

<span data-ttu-id="5465b-111">Dynamics 365 Project Operations kasutab kontsernisiseste tehingute töötlemiseks järgmist voogu.</span><span class="sxs-lookup"><span data-stu-id="5465b-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="5465b-112">Laenu andva juriidilise olemi ressursid kirjendavad kontsernisisesed aja- või kulutehingud broneerides aega ja kulusid laenava juriidilise olemi projektide suhtes.</span><span class="sxs-lookup"><span data-stu-id="5465b-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="5465b-113">Aja- ja kulumaksumused kirjendatakse laenu andvas ettevõttes, kasutades laenava ettevõtte üksuse omahinnakirja.</span><span class="sxs-lookup"><span data-stu-id="5465b-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="5465b-114">Kontsernisisesed arveldamata müügitehingud kirjendatakse laenu andvas ettevõttes, kasutades laenava ettevõtte üksuse omahinnakirja.</span><span class="sxs-lookup"><span data-stu-id="5465b-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="5465b-115">Arveldamata tulu kirjendadatakse laenavas ettevõttes, kasutades projektilepingu müügihinnakirja.</span><span class="sxs-lookup"><span data-stu-id="5465b-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="5465b-116">Kliendile saab esitada arve arveldamata tulu kirjendamisel.</span><span class="sxs-lookup"><span data-stu-id="5465b-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="5465b-117">Klient ei pea ootama kontsernisiseste arvete töötlemise lõpuleviimiseni.</span><span class="sxs-lookup"><span data-stu-id="5465b-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="5465b-118">Kontsernisisesed kliendiarved luuakse laenu andvas ettevõttes perioodiliselt.</span><span class="sxs-lookup"><span data-stu-id="5465b-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="5465b-119">Arved luuakse käsitsi või perioodiliste automaatsete protsesside abil.</span><span class="sxs-lookup"><span data-stu-id="5465b-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="5465b-120">Igale laenavale juriidilise olemile saab luua ühe arve või projekti põhjal saab luua eraldi arve.</span><span class="sxs-lookup"><span data-stu-id="5465b-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="5465b-121">Kui kontsernisisene kliendiarve kirjendatakse laenu andvas juriidilises olemis, luuakse laenavas juriidilises olemis vastav ootel olev hankija arve.</span><span class="sxs-lookup"><span data-stu-id="5465b-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="5465b-122">Ootel oleva jankija arve kulud kirjendatakse projekti pearaamatus, kui arve sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="5465b-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="5465b-123">Järgmisel joonisel on toodud kontsernisisene arveldamine, kuna see on seotud raamatupidamise sündmustega ja eeldatavate pearaamatu sisestustega.</span><span class="sxs-lookup"><span data-stu-id="5465b-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Kontsernisisene voog](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="5465b-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5465b-125">Additional resources</span></span>

- [<span data-ttu-id="5465b-126">Kontsernisisese arveldamise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="5465b-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="5465b-127">Kontsernisiseste kannete kirjendamine</span><span class="sxs-lookup"><span data-stu-id="5465b-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="5465b-128">Kontsernisisese kliendi ja hankija arvete loomine</span><span class="sxs-lookup"><span data-stu-id="5465b-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]