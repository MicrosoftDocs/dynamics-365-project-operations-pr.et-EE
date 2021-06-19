---
title: Kontsernisisesed kulud
description: Selles teemas kirjeldatakse, kuidas kasutada kontsernisiseseid kulusid töötaja kulude määramiseks juriidilisele isikule, kelle jaoks töö tehti.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005066"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="30fe1-103">Kontsernisisesed kulud</span><span class="sxs-lookup"><span data-stu-id="30fe1-103">Intercompany expenses</span></span>

<span data-ttu-id="30fe1-104">Töötaja, kelle on organisatsiooni üks juriidiline olem tööle võtnud, võib teha tööd mõne muu sama organisatsiooni juriidilise olemi jaoks.</span><span class="sxs-lookup"><span data-stu-id="30fe1-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="30fe1-105">Saate kasutada kontsernisiseseid kulusid töötaja kulude määramiseks juriidilisele isikule, kelle jaoks töö tehti.</span><span class="sxs-lookup"><span data-stu-id="30fe1-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="30fe1-106">Juriidilist olemit, mille jaoks töötaja töötab, nimetatakse laenavaks juriidiliseks olemiks.</span><span class="sxs-lookup"><span data-stu-id="30fe1-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="30fe1-107">Juriidilist olemit, mille jaoks töötaja kulusid kannab, nimetatakse laenajast juriidiliseks olemiks.</span><span class="sxs-lookup"><span data-stu-id="30fe1-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="30fe1-108">Enne töötaja saab luua ja esitada kontsernisiseseid kulusid, peate lubama kontsernisiseste kulude read.</span><span class="sxs-lookup"><span data-stu-id="30fe1-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="30fe1-109">Valige laenava juriidilise isiku lehel **Kuluhalduse parameetrid** suvand **Luba kontsernisisesed kuluread**.</span><span class="sxs-lookup"><span data-stu-id="30fe1-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="30fe1-110">Kontsernisiseste kulude maksude sisestamine</span><span class="sxs-lookup"><span data-stu-id="30fe1-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30fe1-111">Enne kui saate kuluaruandes kasutada laenava (allika) juriidilise isikuga seotud maksurühmi, mitte vastuvõtva (siht) juriidilise isiku omi, peate lubama selle funktsionaalsuse pearaamatu käibemaksu seadistuses.</span><span class="sxs-lookup"><span data-stu-id="30fe1-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="30fe1-112">Kui parameeter **Juriidiline isik kontsernisisese maksusisestuse jaoks** on määratud olekusse **Allikas** ja **Rakenda käibemaksuga maksustamise reegleid** on määratud olekusse **Ei**, kasutatakse laenava juriidilise üksuse maksukombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="30fe1-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="30fe1-113">Kui sama parameetri väärtuseks on seatud **Lähte**, kasutatakse laenajast juriidilise olemi jaoks maksu kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="30fe1-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="30fe1-114">Ameerika Ühendriikide juriidilistele olemitele, kui parameetri väärtuseks on seatud **Algne**, peab väli **käibemaks laekumata** olema konfigureeritud ka uuel lehel **Pearaamatusse sisestamise rühmad**.</span><span class="sxs-lookup"><span data-stu-id="30fe1-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="30fe1-115">Raamatupidamise mootor kasutab selle välja teavet maksuga seotud raamatupidamisandmete jaoks.</span><span class="sxs-lookup"><span data-stu-id="30fe1-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="30fe1-116">Käitumine on kooskõlas projektiga või ilma selleta sisestatud kuluaruannete jaoks.</span><span class="sxs-lookup"><span data-stu-id="30fe1-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]