---
title: Projekti eelarvetele prognoosimudeli loomine
description: Selles teemas antakse teavet, kuidas luua järelejäänud eelarvete jaoks prognoosimudel.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
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
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075092"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="771aa-103">Projekti eelarvetele prognoosimudeli loomine</span><span class="sxs-lookup"><span data-stu-id="771aa-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="771aa-104">Selles teemas antakse teavet, kuidas luua järelejäänud eelarvete jaoks prognoosimudel.</span><span class="sxs-lookup"><span data-stu-id="771aa-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="771aa-105">Projekt, mille suhtes rakendatakse eelarve kontrolli, kasutab kahte tüüpi eelarveid: algne ja järelejäänud.</span><span class="sxs-lookup"><span data-stu-id="771aa-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="771aa-106">Projekti eelarve loomisel tuleb määrata algsed ja järelejäänud eelarve prognoosimudelid, mis on loodud rakenduse lehel **Prognoosimudel**.</span><span class="sxs-lookup"><span data-stu-id="771aa-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="771aa-107">Määratud mudelitel põhinevad projekti eelarved luuakse projekti eelarve täitmisel.</span><span class="sxs-lookup"><span data-stu-id="771aa-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="771aa-108">Prognoosimudel, mida kasutatakse eelarve kontrollimisel, ei saa olla allmudeliga ning seda ei saa kasutada allmudelina.</span><span class="sxs-lookup"><span data-stu-id="771aa-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="771aa-109">Valige **Projekti haldamine ja raamatupidamine** > **Seadistamine** > **Prognoosid**  > **Prognoosimudelid**.</span><span class="sxs-lookup"><span data-stu-id="771aa-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="771aa-110">Uue prognoosimudeli loomiseks valige suvand **Uus** ning seejärel sisestage uue mudeli ID-number ja nimi.</span><span class="sxs-lookup"><span data-stu-id="771aa-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="771aa-111">Seadke suvandi **Peatatud** väärtuseks **Jah** , et vältida prognoosimudeli prognoosiridade muutmist.</span><span class="sxs-lookup"><span data-stu-id="771aa-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="771aa-112">Kui selle mudeliga seotud prognoosiread peaksid tekitama pearaamatus rahavoogude prognoose, määrake suvandi **Kaasa rahavoo prognoosid** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="771aa-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="771aa-113">Projekti kuupäeva kasutamiseks arve kuupäevana seadke suvandi **Prognoosi arve kuupäev** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="771aa-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="771aa-114">Valige väljal **Eelarve tüüp** üks järgmistest mudeli tüüpidest.</span><span class="sxs-lookup"><span data-stu-id="771aa-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="771aa-115">**Algne eelarve** : kasutage algse eelarve loomisel ja kinnitamisel kulutatud algse eelarve summasid.</span><span class="sxs-lookup"><span data-stu-id="771aa-115">**Original budget** : Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="771aa-116">**Järelejäänud eelarve** : kasutage projekti kasutusea jooksul järelejäänud eelarve summasid.</span><span class="sxs-lookup"><span data-stu-id="771aa-116">**Remaining budget** : Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="771aa-117">Selle prognoosimudeli saldosid vähendatakse tegelike tehingute võrra ning suurendatakse või vähendatakse eelarvete läbivaatamisel.</span><span class="sxs-lookup"><span data-stu-id="771aa-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="771aa-118">**Ülekandmine** : kasutage projekti jaoks ülekantud eelarve summasid.</span><span class="sxs-lookup"><span data-stu-id="771aa-118">**Carry-forward** : Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="771aa-119">Ülekandmine on valikuline protsess, mida saab käitada kasutamata eelarve summade ülekandmiseks ühest finantsaastast teise.</span><span class="sxs-lookup"><span data-stu-id="771aa-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="771aa-120">Määrake vajaduse järgi järgmised suvandid.</span><span class="sxs-lookup"><span data-stu-id="771aa-120">Set the following options as required:</span></span>

   - <span data-ttu-id="771aa-121">Projekti kuupäeva kasutamiseks arve kuupäevana lubage suvand **Prognoosi arve kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="771aa-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="771aa-122">Lubage poolelioleval tööl (WIP )põhinevaks prognoosimiseks suvand **Prognoosimine WIP-iga** , seejärel valige WIP-i tüüp.</span><span class="sxs-lookup"><span data-stu-id="771aa-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="771aa-123">Saate suvandi **Eelarve tüüp** vaikeväärtuseks jätta väärtuse **Pole** või sisestada uue tüübi.</span><span class="sxs-lookup"><span data-stu-id="771aa-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="771aa-124">Pärast kirje muutmist ei saa eelarve tüüpi muuta.</span><span class="sxs-lookup"><span data-stu-id="771aa-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="771aa-125">Kui muudate eelarve vaiketüübi, muutuvad kõik muud suvandid värskenduste jaoks kättesaamatuks ning seda prognoosimudelit ei saa uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="771aa-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

