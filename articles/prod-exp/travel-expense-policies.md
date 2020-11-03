---
title: Kulupoliitikate seadistamine
description: Saate rakenduses Microsoft Dynamics 365 Finance seadistada kulupoliitikad, mida teie töötajad peavad kuluaruandeid ja reisitellimusi esitades järgima.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075103"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="9e5b1-103">Kulupoliitikate seadistamine</span><span class="sxs-lookup"><span data-stu-id="9e5b1-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e5b1-104">Saate määratleda poliitika, mida teie töötajad peavad kuluaruandeid ja reisitellimusi esitades järgima.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="9e5b1-105">Kulupoliitika rakendamine aitab teil tõhusalt kulusid hallata.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="9e5b1-106">Näiteks saate New York City hotellikuludele sisse seada poliitika, mis määratleb, et kulud öö kohta ei tohi ületada 250 dollarit.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="9e5b1-107">Kui töötaja esitab kuluaruande või reisitellimuse, kus toa hind ületab seda summat, teavitab süsteem sellest</span><span class="sxs-lookup"><span data-stu-id="9e5b1-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="9e5b1-108">töötajat, et kulu poliitikas olev summa on ületatud.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="9e5b1-109">Töötaja saadava sõnumi saate konfigureerida</span><span class="sxs-lookup"><span data-stu-id="9e5b1-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="9e5b1-110">poliitikat määratledes.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-110">define the policy.</span></span>      
        
<span data-ttu-id="9e5b1-111">Saate määratled kolme tüüpi poliitikaid:</span><span class="sxs-lookup"><span data-stu-id="9e5b1-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="9e5b1-112">Hoiatus - võimaldab töötajal kuluaruande või reisitellimuse esitada, kuid kulu märgitakse kõigile kinnitajatele ja</span><span class="sxs-lookup"><span data-stu-id="9e5b1-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="9e5b1-113">hilisemaks aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-113">for later reporting.</span></span>        

- <span data-ttu-id="9e5b1-114">Tõrge - nõuab, et töötaja peaks enne kuluaruande või reisitellimuse esitamist kulu üle vaatama, et see vastaks poliitikale.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="9e5b1-115">Põhjendus - nõuab, et töötaja või haldur sisestaks enne kuluaruande või reisitellimuse esitamist põhjenduse poliitika summa ületamise kohta.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="9e5b1-116">Poliitika näpunäited</span><span class="sxs-lookup"><span data-stu-id="9e5b1-116">Policy tips</span></span>
<span data-ttu-id="9e5b1-117">Siin on mõned soovitused, mis aitavad teil kulude haldamiseks uut poliitikat luua.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="9e5b1-118">Poliitikad ei kehti tagasiulatuvalt ja poliitika ei kohaldu, kui see on loodud pärast kulu tekkimise kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="9e5b1-119">Näiteks kui loote täna uue poliitika, et jõustada maksimaalseks eine kuluks 50 USD, siis ei kontrollita selle poliitika suhtes mistahes olemasolevaid kulusid, mis on sisestatud eile seisuga.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="9e5b1-120">Üksikasjaliku kulukategooria jaoks poliitika loomisel arvestage, et saate lisada kulurea tüübi tingimuse.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="9e5b1-121">Mõni poliitika, näiteks kviitungi nõudmine, ei pruugi olla üksikasjalike ridade jaoks otstarbekas ja seda peaks rakendama ainult päisereale või mitte-üksikasjalikule reale.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="9e5b1-122">Kulude haldamise poliitikaid hinnatakse vaikimisi selle allika olemi suhtes.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="9e5b1-123">Kontsernisiseste stsenaariumide puhul saate määrata poliitika, mida saab selle asemel hinnata sihtkoha olemi (laenaja olemi) suhtes.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="9e5b1-124">Et käivitada poliitikad sihtkoha olemi suhtes, lülitage sisse funktsioon "Hinda kulupoliitikat laenava juriidilise isiku suhtes" tööruumis **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="9e5b1-125">Millal poliitikaid hinnada</span><span class="sxs-lookup"><span data-stu-id="9e5b1-125">When to evaluate policies</span></span>

<span data-ttu-id="9e5b1-126">Kulude haldamise parameetrites on võimalus hinnata kulu haldamise poliitikat rea salvestamisel või kuluaruande esitamisel.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="9e5b1-127">Kui otsustate hinnata siis, kui rida salvestatakse, kindlustab see, et kasutajatele kuvatakse varem, mida nad peavad tegema, et oma kuluaruanne korraga lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="9e5b1-128">Vastasel juhul saate poliitika hindamist edasi lükata ja aega säästa, kui valideerite end töövoo esitamise ajal lõpus.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
