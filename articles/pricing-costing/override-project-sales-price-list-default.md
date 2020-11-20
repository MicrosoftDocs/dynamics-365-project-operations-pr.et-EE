---
title: Projekti müügi hinnakirjade tühistamine
description: See teema sisaldab teavet kohandatud müügi hinnakirjade loomise kohta.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c97dca8685c2db7d256017cf4442416feb0e005b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130843"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="762d0-103">Projekti müügi hinnakirjade tühistamine</span><span class="sxs-lookup"><span data-stu-id="762d0-103">Override project sales price lists</span></span>

<span data-ttu-id="762d0-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="762d0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="762d0-105">Kliendipõhise projekti hinnakiri</span><span class="sxs-lookup"><span data-stu-id="762d0-105">Customer-specific project price lists</span></span>

<span data-ttu-id="762d0-106">Rakenduses Dynamics 365 Project Operations on võimalik seadistada kliendipõhised hinnakirja kokkulepped konto kirje projekti hinnakirjadeks.</span><span class="sxs-lookup"><span data-stu-id="762d0-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="762d0-107">Alas **Müük** kliendipõhise hinnakirja seadistamiseks liikuge konto kirjele.</span><span class="sxs-lookup"><span data-stu-id="762d0-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="762d0-108">Avage loendi leht **Kontod**.</span><span class="sxs-lookup"><span data-stu-id="762d0-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="762d0-109">Leidke ja topeltklõpsake kliendi kirjet, et avada suvandi **Konto** üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="762d0-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="762d0-110">Vahekaardil **Projekti hinnakirjad** valige \*\*+ Uus projekti hinnakiri^^.</span><span class="sxs-lookup"><span data-stu-id="762d0-110">On the **Project Price lists** tab, select \*\*+ New Project Price List^^.</span></span>
4. <span data-ttu-id="762d0-111">Valige lehel **Uus projekti hinnakiri** rippmenüüst hinnakiri.</span><span class="sxs-lookup"><span data-stu-id="762d0-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="762d0-112">Seal sisalduvad ainult hinnakirjad, mille kontekstiks on määratud **Müük** ja mille valuuta vastab konto valuutale.</span><span class="sxs-lookup"><span data-stu-id="762d0-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="762d0-113">Pange seosele nimi ja valige seejärel käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="762d0-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="762d0-114">Luuakse kliendipõhine projekti hinnakiri.</span><span class="sxs-lookup"><span data-stu-id="762d0-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="762d0-115">Seda hinnakirja kasutatakse projekti hinnapakkumistes projekti hindade või selle kliendi jaoks loodud lepingute vaikeväärtuste jaoks, kus hinnapakkumise või projektilepingu loomise kuupäev jääb hinnakirja kehtivuse kuupäevavahemikku.</span><span class="sxs-lookup"><span data-stu-id="762d0-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="762d0-116">Projekti hinnapakkumiste kohandatud hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="762d0-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="762d0-117">Projekti hinnapakkumistes võib teil olla projekti hinnakujundus, mis algab vaikimisi standardse hinnakirjaga, mile vaikeväärtused pärinevad kliendilt või projekti parameetritest.</span><span class="sxs-lookup"><span data-stu-id="762d0-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="762d0-118">Kui vajate konkreetse hinnapakkumise projektiga seotud töö jaoks kohandatud hinda, saate hankida selle seostatud olemi projekti hinnakirjadest.</span><span class="sxs-lookup"><span data-stu-id="762d0-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="762d0-119">Hinnapakkumisele spetsiifilise projekti hinnakujunduse häälestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="762d0-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="762d0-120">Avage projekti hinnapakkumine ja valige vahekaart **Projekti hinnakirjad**.</span><span class="sxs-lookup"><span data-stu-id="762d0-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="762d0-121">Valige andmeruudustikus suvand **Loo kohandatud hinnakujundus**.</span><span class="sxs-lookup"><span data-stu-id="762d0-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="762d0-122">Kõik hinnapakkumisega seotud projekti hinnakirjad kopeeritakse uutesse hinnakirjadesse.</span><span class="sxs-lookup"><span data-stu-id="762d0-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="762d0-123">Uute hinnakirjade nimed kajastavad hinnapakkumise nime koos hinnakirjade loomise ajatempliga.</span><span class="sxs-lookup"><span data-stu-id="762d0-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="762d0-124">Saate kasutada iga sellist hinnakirja ja teha kohandusi töö (rolli hind) ja kulu (kategooria hind) hindadele.</span><span class="sxs-lookup"><span data-stu-id="762d0-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="762d0-125">Need hinnad kehtivad ainult sellele projekti hinnapakkumisele.</span><span class="sxs-lookup"><span data-stu-id="762d0-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="762d0-126">Projektilepingu hinnakirjad</span><span class="sxs-lookup"><span data-stu-id="762d0-126">Price lists on a project contract</span></span>

<span data-ttu-id="762d0-127">Projektilepingus on projekti hinnakujunduse vaikeväärtused alati pärit lepingu nimega kohandatud hinnakirjast ja luuakse nimele lisatud ajatempliga.</span><span class="sxs-lookup"><span data-stu-id="762d0-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="762d0-128">See on tõene, kui leping loodi hinnapakkumise võitmise ajal või kui leping loodi nullist.</span><span class="sxs-lookup"><span data-stu-id="762d0-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="762d0-129">Vajaduse korral saate selle kohandatud hinnakirjaga seose eemaldada ja seostada selle asemel projektilepinguga standardse hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="762d0-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="762d0-130">Kui seostate hinnapakkumise või lepingu projekti hinnakirjad standardse hinnakirjaga, mõjutavad kõik hinnakirja hindade muudatused kõiki hinnapakkumisi ja lepinguid, mis seda hinnakirja kasutavad.</span><span class="sxs-lookup"><span data-stu-id="762d0-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
