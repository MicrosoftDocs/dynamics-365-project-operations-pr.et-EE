---
title: Mustandist projekti arve ettepanekute raamatupidamise parandamine
description: Selles teemas selgitatakse, kuidas muuta mustandist arve ettepanekul raamatupidamisega seotud teavet.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251201"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a><span data-ttu-id="203fa-103">Mustandist projekti arve ettepanekute raamatupidamise parandamine</span><span class="sxs-lookup"><span data-stu-id="203fa-103">Correct the accounting on draft project invoice proposals</span></span>

<span data-ttu-id="203fa-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="203fa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="203fa-105">Projekti arvete *toimingu üksikasju* haldab projektijuht näidisarvel.</span><span class="sxs-lookup"><span data-stu-id="203fa-105">*Operational details* for project invoices are maintained by the project manager on a pro forma invoice.</span></span> <span data-ttu-id="203fa-106">Need üksikasjad hõlmavad otsuseid tundide, kulude, materjalide või vahe-eesmärkide kohta, mille eest tuleb esitada arve, hindade ning avansi- ja honorarisummade taotlemise kohta.</span><span class="sxs-lookup"><span data-stu-id="203fa-106">These details include the decision about the hours, expenses, materials, or milestones that must be invoiced, the rates, and the application of advance and retainer amounts.</span></span> <span data-ttu-id="203fa-107">Pärast algse näidisarve kinnitamist saate toimingu üksikasju muuta, luues ja kinnitades [korrigeeriva näidisarve](../proforma-invoicing/corrective-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="203fa-107">After you confirm the original pro forma invoice, you can adjust the operational details by creating and confirming a [corrective pro forma invoice](../proforma-invoicing/corrective-invoices.md).</span></span>

<span data-ttu-id="203fa-108">Projekti arvete *raamatupidamise üksikasju* hallatakse kliendile suunatud arvedokumendis.</span><span class="sxs-lookup"><span data-stu-id="203fa-108">*Accounting details* for project invoices are maintained in a customer-facing invoice document.</span></span> <span data-ttu-id="203fa-109">Need üksikasjad hõlmavad arvele rakendatud käibemaksu arvutamist ja finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="203fa-109">These details include the sales tax calculation and the financial dimensions that are applied to the invoice.</span></span> <span data-ttu-id="203fa-110">Selles teemas on toodud üksikasjad selle kohta, kuidas neid raamatupidamise üksikasju saab mustandi projekti arve ettepanekus muuta.</span><span class="sxs-lookup"><span data-stu-id="203fa-110">This topic provides details about how these accounting details can be adjusted on a draft project invoice proposal.</span></span>

## <a name="adjust-sales-tax"></a><span data-ttu-id="203fa-111">Käibemaksu muutmine</span><span class="sxs-lookup"><span data-stu-id="203fa-111">Adjust sales tax</span></span>

<span data-ttu-id="203fa-112">Vaikimisi arveldamise käibemaksurühmasid ja eseme käibemaksurühmasid saab muuta otse arve ettepaneku dokumendis.</span><span class="sxs-lookup"><span data-stu-id="203fa-112">Default billing sales tax groups and item sales tax groups can be adjusted directly on the invoice proposal document.</span></span> <span data-ttu-id="203fa-113">Nende rühmade muutmiseks valige **Redigeeri** ja sisestage seejärel igal projekti arve ettepaneku real väljale **Käibemaksurühm** või **Eseme käibemaksurühm**.</span><span class="sxs-lookup"><span data-stu-id="203fa-113">To adjust these groups, select **Edit**, and then, on each project invoice proposal line, enter a new value in the **Sales tax group** or **Item sales tax group** field.</span></span>

## <a name="adjust-financial-dimensions"></a><span data-ttu-id="203fa-114">Finantsdimensioonide muutmine</span><span class="sxs-lookup"><span data-stu-id="203fa-114">Adjust financial dimensions</span></span>

<span data-ttu-id="203fa-115">Finantsdimensioone ei saa muuta otse projekti arve ettepaneku real.</span><span class="sxs-lookup"><span data-stu-id="203fa-115">Financial dimensions can't be edited directly on a project invoice proposal line.</span></span> <span data-ttu-id="203fa-116">Selle asemel järgige neid samme, et kohandada projekti arve ettepaneku finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="203fa-116">Instead, follow these steps to adjust financial dimensions on a project invoice proposal.</span></span>

1. <span data-ttu-id="203fa-117">Valige arve ettepanekul suvand **Kustuta kõik**, et eemaldada projekti arve ettepaneku read.</span><span class="sxs-lookup"><span data-stu-id="203fa-117">On the project invoice proposal, select **Delete all** to remove the project invoice proposal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="203fa-118">Nupp **Kustuta kõik** on saadaval alles pärast seda, kui süsteemiadministraator lubab funktsiooni **Kustuta arve ettepaneku read ressursipõhiste/mittelaopõhiste stsenaariumide jaoks Project Operationsi kasutamise ajal** tööruumis **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="203fa-118">The **Delete all** button is available only after the system administrator enables the **Delete invoice proposal lines when using Project Operations for resource based/ non-stocked scenarios** feature in the **Feature management** workspace.</span></span>

2. <span data-ttu-id="203fa-119">Muutke dinantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="203fa-119">Adjust the financial dimensions:</span></span>

    - <span data-ttu-id="203fa-120">**Ettemaksukanded (arvelduse vahe-eesmärgid):** avage **Kõik projektid** \> **Haldamine** \> **Ettemaksukanded** ja valige muutmist vajav vahe-eesmärk.</span><span class="sxs-lookup"><span data-stu-id="203fa-120">**On-account transactions (billing milestones):** Go to **All projects** \> **Manage** \> **On-account transactions**, and select the milestone that requires adjustment.</span></span> <span data-ttu-id="203fa-121">Seejärel värskendage vahekaardil **Finantsdimensioonid** vastavalt vajadusele väärtuseid.</span><span class="sxs-lookup"><span data-stu-id="203fa-121">Then, on the **Financial dimensions** tab, update the values as required.</span></span>
    - <span data-ttu-id="203fa-122">**Aja-, kulu- ja materjali kanded:** valige lehel **Kirjendatud projekti kanded** suvand **Raamatupidamise muutmine**, et värskendada finantsmõõtmeid.</span><span class="sxs-lookup"><span data-stu-id="203fa-122">**Time, expense, and material transactions:** On the **Posted project transactions** page, select **Adjust accounting** to update the financial dimensions.</span></span>

3. <span data-ttu-id="203fa-123">Pärast finantsdimensiooni väärtuste kohandamist avage **Projektihaldus ja raamatupidamine** \> **Perioodiline** \> **Project Operationsi integreerimine** ja valige perioodilise toimingu käitamiseks suvand **Impordi koondtabelist**.</span><span class="sxs-lookup"><span data-stu-id="203fa-123">After you've finished adjusting the financial dimension values, go to **Project management and accounting** \> **Periodic** \> **Project Operations integration**, and select **Import from staging table** to run the periodic process.</span></span> <span data-ttu-id="203fa-124">See protsess kasutab projekti arve ettepaneku ridade uuesti loomiseks värskendatud finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="203fa-124">That process uses the updated financial dimension values to re-create the project invoice proposal lines.</span></span> <span data-ttu-id="203fa-125">Värskendatud väärtusi kasutatakse seejärel projekti arve kirjendamisel projekti alampearaamatus ja pearaamatus.</span><span class="sxs-lookup"><span data-stu-id="203fa-125">The updated values are then used in the project subledger and general ledger when the project invoice is posted.</span></span>
