---
title: Kontsernisisesed kulud
description: Töötaja, kelle on organisatsiooni üks juriidiline olem tööle võtnud, võib teha tööd mõne muu sama organisatsiooni juriidilise olemi jaoks. Sellisel juhul saate kasutada kontsernisiseste kulude funktsiooni, et määrata töötaja kulud juriidilisele olemile, mille jaoks tööd tehti.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075107"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="17611-104">Kontsernisisesed kulud</span><span class="sxs-lookup"><span data-stu-id="17611-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17611-105">Töötaja, kelle on organisatsiooni üks juriidiline olem tööle võtnud, võib teha tööd mõne muu sama organisatsiooni juriidilise olemi jaoks.</span><span class="sxs-lookup"><span data-stu-id="17611-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="17611-106">Sellisel juhul saate kasutada kontsernisiseste kulude funktsiooni, et määrata töötaja kulud juriidilisele olemile, mille jaoks tööd tehti.</span><span class="sxs-lookup"><span data-stu-id="17611-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="17611-107">Juriidilist olemit, mille jaoks töötaja töötab, nimetatakse laenavaks juriidiliseks olemiks.</span><span class="sxs-lookup"><span data-stu-id="17611-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="17611-108">Juriidilist olemit, mille jaoks töötaja kulusid kannab, nimetatakse laenajast juriidiliseks olemiks.</span><span class="sxs-lookup"><span data-stu-id="17611-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="17611-109">Enne, kui töötaja saab luua ja esitada mõne muu juriidilise olemi jaoks tehtud töö kulud, valige laenava juriidilise olemi jaoks lehel **Kuluhalduse parameetrid** suvand **Luba kontsernisiseste kulude read**.</span><span class="sxs-lookup"><span data-stu-id="17611-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="17611-110">Kontsernisiseste kulude maksude sisestamine</span><span class="sxs-lookup"><span data-stu-id="17611-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17611-111">Kui soovite oma kuluaruandes kasutada laenava (algne) juriidilise olemiga seotud maksurühmasid, mitte laenajast (lähte) juriidilise olemiga, peate selle konfigureerima pearaamatu käibemaksu seadistamisel.</span><span class="sxs-lookup"><span data-stu-id="17611-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="17611-112">Kui pearaamatu parameetriks **Kontsernisisese maksu sisestamise juriidiline olem** on seatud **Algne** ja suvandi **Rakenda käibemaksu maksustamise reegleid** väärtuseks on **Ei** , kasutatakse laenava juriidilise olemi jaoks maksu kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="17611-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="17611-113">Kui sama parameetri väärtuseks on seatud **Lähte** , kasutatakse laenajast juriidilise olemi jaoks maksu kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="17611-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="17611-114">Ameerika Ühendriikide juriidilistele olemitele, kui parameetri väärtuseks on seatud **Algne** , peab väli **käibemaks laekumata** olema konfigureeritud ka uuel lehel **Pearaamatusse sisestamise rühmad**.</span><span class="sxs-lookup"><span data-stu-id="17611-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="17611-115">Raamatupidamise mootor kasutab selle välja teavet maksuga seotud raamatupidamisandmete jaoks.</span><span class="sxs-lookup"><span data-stu-id="17611-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="17611-116">Käitumine on kooskõlas projektiga või ilma selleta sisestatud kuluaruannete jaoks.</span><span class="sxs-lookup"><span data-stu-id="17611-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
