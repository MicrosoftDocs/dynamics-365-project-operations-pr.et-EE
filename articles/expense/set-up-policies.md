---
title: Kulupoliitika määratlemine
description: Saate määratleda kulupoliitika, mida teie töötajad peavad kuluaruandeid ja reisitellimusi esitades järgima.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fbab7fd94fa429876216ee82b716da8d847fb01a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896636"
---
# <a name="define-expense-policies"></a><span data-ttu-id="ebbe3-103">Kulupoliitika määratlemine</span><span class="sxs-lookup"><span data-stu-id="ebbe3-103">Define expense policies</span></span>

<span data-ttu-id="ebbe3-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="ebbe3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ebbe3-105">Saate määratleda poliitika, mida teie töötajad peavad kuluaruandeid ja reisitellimusi esitades järgima.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="ebbe3-106">Kulupoliitika rakendamine aitab teil tõhusalt kulusid hallata.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="ebbe3-107">Näiteks saate New York City hotellikuludele sisse seada poliitika, mis määratleb, et kulud öö kohta ei tohi ületada 250 dollarit.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="ebbe3-108">Kui töötaja esitab kuluaruande või reisitellimuse, kus toa hind ületab seda summat, teavitab süsteem sellest</span><span class="sxs-lookup"><span data-stu-id="ebbe3-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="ebbe3-109">töötajat, et kulu poliitikas olev summa on ületatud.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="ebbe3-110">Töötaja saadava sõnumi saate konfigureerida</span><span class="sxs-lookup"><span data-stu-id="ebbe3-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="ebbe3-111">poliitikat määratledes.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-111">define the policy.</span></span>      
        
<span data-ttu-id="ebbe3-112">Saate määratled kolme tüüpi poliitikaid:</span><span class="sxs-lookup"><span data-stu-id="ebbe3-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="ebbe3-113">**Hoiatus**: võimaldab töötajal kuluaruande või reisitellimuse esitada, kuid kulu märgitakse kõigile kinnitajatele ja</span><span class="sxs-lookup"><span data-stu-id="ebbe3-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="ebbe3-114">hilisemaks aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-114">for later reporting.</span></span>        

- <span data-ttu-id="ebbe3-115">**Tõrge**: nõuab, et töötaja peaks enne kuluaruande või reisitellimuse esitamist kulu üle vaatama, et see vastaks poliitikale.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="ebbe3-116">**Põhjendus**: nõuab, et töötaja või haldur sisestaks enne kuluaruande või reisitellimuse esitamist põhjenduse poliitika summa ületamise kohta.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="ebbe3-117">Poliitika näpunäited</span><span class="sxs-lookup"><span data-stu-id="ebbe3-117">Policy tips</span></span>
<span data-ttu-id="ebbe3-118">Siin on mõned soovitused, mis aitavad teil kulude haldamiseks uut poliitikat luua.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="ebbe3-119">Poliitikad ei kehti tagasiulatuvalt, mis tähendab, et poliitika ei kohaldu, kui see on loodud pärast kulu tekkimise kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="ebbe3-120">Näiteks saate luua uue poliitika täna, et kehtestada maksimaalseks toidukuluks 50 dollarit.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="ebbe3-121">Kõiki eile sisestatud kulusid ei kontrollita selle poliitika suhtes.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="ebbe3-122">Üksikasjaliku kulukategooria jaoks poliitika loomisel arvestage, et saate lisada kulurea tüübi tingimuse.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="ebbe3-123">Teatud poliitikad (nt kviitungi nõudmine) ei pruugi konkreetsete ridade jaoks mõistlik olla.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="ebbe3-124">Sellisel juhul rakendatakse seda poliitikat ainult päisereale või mitte-üksikasjalikule reale.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="ebbe3-125">Kulude haldamise poliitikaid hinnatakse vaikimisi selle allika olemi suhtes.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="ebbe3-126">Kontsernisiseste stsenaariumide puhul saate määrata poliitika, mida saab selle asemel hinnata sihtkoha olemi (laenaja olemi) suhtes.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="ebbe3-127">Et käivitada poliitikad sihtkoha olemi suhtes, lülitage sisse funktsioon **Hinda kulupoliitikat laenava juriidilise isiku suhtes** tööruumis **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="ebbe3-128">Millal poliitikaid hinnada</span><span class="sxs-lookup"><span data-stu-id="ebbe3-128">When to evaluate policies</span></span>

<span data-ttu-id="ebbe3-129">Kulude haldamise parameetrites saate valida, et hinnata kulu haldamise poliitikat rea salvestamisel või kuluaruande esitamisel.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="ebbe3-130">Kui otsustate hinnata siis, kui rida salvestatakse, kuvatakse kasutajatele varem, mida nad peavad tegema, et oma kuluaruanne korraga lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="ebbe3-131">Vastasel juhul saate poliitika hindamist edasi lükata ja aega säästa, kui valideerite end töövoo esitamise ajal lõpus.</span><span class="sxs-lookup"><span data-stu-id="ebbe3-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
