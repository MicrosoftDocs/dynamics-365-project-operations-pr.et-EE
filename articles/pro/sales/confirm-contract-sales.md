---
title: Projekti lepingu kinnitamine
description: Selles teemas antakse teavet, kuidas Project Operationsis lepingut kinnitada.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d807d3631f40a93ec7dbd918b64c287fd4875c79
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273823"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="d346f-103">Projekti lepingu kinnitamine</span><span class="sxs-lookup"><span data-stu-id="d346f-103">Confirm a project contract</span></span>

<span data-ttu-id="d346f-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="d346f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d346f-105">Projektileping rakenduses Dynamics 365 Project Operations võib olla aktiivne põhjusega **Kinnitatud** või suletud põhjusega **Kaotatud**.</span><span class="sxs-lookup"><span data-stu-id="d346f-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="d346f-106">Kui kinnitate projekti lepingu, siis muutub olek olekust **Mustand** olekuks **Aktiivne** ja oleku põhjus on **Kinnitatud**.</span><span class="sxs-lookup"><span data-stu-id="d346f-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="d346f-107">Aktiivset või suletud lepingut ei saa redigeerida ega uuesti avada.</span><span class="sxs-lookup"><span data-stu-id="d346f-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="d346f-108">Projekti lepingu kinnitamise finantsmõju</span><span class="sxs-lookup"><span data-stu-id="d346f-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="d346f-109">Pärast projekti lepingu kinnitamist arvutab rakendus kulud ümber, pöörates tagasi vanemad tegelikud kulud ja luues uued tegelikud kulud.</span><span class="sxs-lookup"><span data-stu-id="d346f-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="d346f-110">Uusi tegelikke kulusid töödeldakse, võttes aluseks seotud projekti lepingurea arveldusmeetodi.</span><span class="sxs-lookup"><span data-stu-id="d346f-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="d346f-111">Kui tegelikud kulud viitavad aja ja materjali lepingureale, loob rakendus automaatselt vastavad arveldamata tegelikud müüginäitajad uuesti.</span><span class="sxs-lookup"><span data-stu-id="d346f-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="d346f-112">Kui tegelikud kulud viitavad fikseeritud hinna lepingureale, peatab rakendus tegelike kulude ümbertöötlemise.</span><span class="sxs-lookup"><span data-stu-id="d346f-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="d346f-113">Mitteületatavad limiite, arveldatavuse seadistamist ning tegelikke hindu ja kulusid hinnatakse ning seejärel värskendatakse kinnituste osana.</span><span class="sxs-lookup"><span data-stu-id="d346f-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="d346f-114">Projekti lepingu sulgemine kaotatuna</span><span class="sxs-lookup"><span data-stu-id="d346f-114">Close a project contract as lost</span></span>

<span data-ttu-id="d346f-115">Kui sulgete projekti lepingu kaotatuna, muudetakse lepingu olekuks **Suletud** ja oleku põhjuseks on **Kaotatud**.</span><span class="sxs-lookup"><span data-stu-id="d346f-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="d346f-116">Projekti leping muutub kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="d346f-116">The project contract becomes read-only.</span></span> <span data-ttu-id="d346f-117">Enne muudatuste lõpuleviimist kuvatakse kinnituse dialoog, kuna suletud projekti lepingut ei saa uuesti avada.</span><span class="sxs-lookup"><span data-stu-id="d346f-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="d346f-118">Kui projekti leping, mis on suletud kui kaotatud, viitab projekti ridadele, siis on ka see projekt suletuks märgitud.</span><span class="sxs-lookup"><span data-stu-id="d346f-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="d346f-119">Kõik ressursi broneeringud alates sellest päevast edasi on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="d346f-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="d346f-120">Kõik projekti lepingusse kuuluvad arveldamata tegelikud müüginäitajad, mida veel arvele pole lisatud, tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="d346f-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="d346f-121">Projekti lepingu sulgemine rakenduses Dynamics 365 Project Operations kaotatuna ei mõjuta seostatud müügivõimaluse olekut.</span><span class="sxs-lookup"><span data-stu-id="d346f-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="d346f-122">Müügivõimalus jääb avatuks ja see tuleb käsitsi sulgeda.</span><span class="sxs-lookup"><span data-stu-id="d346f-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]