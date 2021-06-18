---
title: Hinnapakkumise sulgemine – liht
description: Selles teemas kirjeldatakse hinnapakkumise sulgemist Project Operationsis.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994131"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="fc63d-103">Hinnapakkumise sulgemine – liht</span><span class="sxs-lookup"><span data-stu-id="fc63d-103">Close a quote - lite</span></span>

<span data-ttu-id="fc63d-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="fc63d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fc63d-105">Projekti hinnapakkumise saab sulgeda kui võidetu või kaotatuna.</span><span class="sxs-lookup"><span data-stu-id="fc63d-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="fc63d-106">Hinnapakkumise mustandi saab sulgeda, kuna Microsoft Dynamics 365 Project Operations ei toeta hinnapakkumiste aktiveerimise ja muutmise toiminguid.</span><span class="sxs-lookup"><span data-stu-id="fc63d-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="fc63d-107">Hinnapakkumise sulgemine olekus Võidetud</span><span class="sxs-lookup"><span data-stu-id="fc63d-107">Close a quote as Won</span></span>

<span data-ttu-id="fc63d-108">Kui sulgete projekti hinnapakkumise olekuga Võidetud, määratakse olekuks Suletud ja olekuks oleku põhjuseks Võidetud.</span><span class="sxs-lookup"><span data-stu-id="fc63d-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="fc63d-109">Hinnapakkumise sulgemine muudab projekti hinnapakkumise kirjutuskaitstuks ja loob projekti lepingu mustandi, mis sisaldab hinnapakkumise teavet.</span><span class="sxs-lookup"><span data-stu-id="fc63d-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="fc63d-110">Kuna suletud hinnapakkumist ei saa uuesti avada, kinnitab kinnitusdialoog teie muudatused.</span><span class="sxs-lookup"><span data-stu-id="fc63d-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="fc63d-111">Kui hinnapakkumine on seotud müügivõimalusega, suletakse kõik muud müügivõimaluse projekti hinnapakkumised automaatselt kaotatud kujul.</span><span class="sxs-lookup"><span data-stu-id="fc63d-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="fc63d-112">Hinnapakkumise võidetud olekus sulgemise finantsmõju</span><span class="sxs-lookup"><span data-stu-id="fc63d-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="fc63d-113">Kui projektil on veel aja tegelikke näitajaid, kui see on hinnapakkumise mustandile lisatud, kirjendatakse ainult aja või kulu maksumust.</span><span class="sxs-lookup"><span data-stu-id="fc63d-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="fc63d-114">Pärast hinnapakkumise sulgemist olekus Võidetud, refaktoorib rakendus kulud, pöörates tagasi vanemad tegelikud kulud ja luues uued tegelikud kulud.</span><span class="sxs-lookup"><span data-stu-id="fc63d-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="fc63d-115">Rakendus töötleb need tegelikud kulud võttes aluseks seotud projekti lepingurea arveldusmeetodi.</span><span class="sxs-lookup"><span data-stu-id="fc63d-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="fc63d-116">Kui kulu tegelikud andmed viitavad aja ja materjali lepingureale, luuakse vastavad arveldamata müügi tegelikud andmed selleks ajaks, kui hinnapakkumine suletakse ja projekti leping luuakse.</span><span class="sxs-lookup"><span data-stu-id="fc63d-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="fc63d-117">Kui kulu tegelikud andmed viitavad fikseeritud hinnaga lepingureale, lõpetab rakendus nende kulu tegelike näitajate uuesti töötlemise, mis põhinevad projekti lepingu klientide jagatud arveldamise reeglitel.</span><span class="sxs-lookup"><span data-stu-id="fc63d-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="fc63d-118">Hinnapakkumise sulgemine olekus Kaotatud:</span><span class="sxs-lookup"><span data-stu-id="fc63d-118">Closing a quote as lost:</span></span>

<span data-ttu-id="fc63d-119">Kui sulgete projekti hinnapakkumise olekuga Kaotatud, määratakse olekuks Suletud ja olekuks oleku põhjuseks Kaotatud.</span><span class="sxs-lookup"><span data-stu-id="fc63d-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="fc63d-120">Hinnapakkumise sulgemine teeb projekti hinnapakkumise kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="fc63d-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="fc63d-121">Kuna suletud hinnapakkumist ei saa uuesti avada, siis palutakse hinnapakkumise sulgemisel muudatused kinnitada.</span><span class="sxs-lookup"><span data-stu-id="fc63d-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="fc63d-122">Kui projekti hinnapakkumine, mis on suletud kui Kaotatud, viitab projektile mis tahes real, märgitakse ka see projekt kui Suletud.</span><span class="sxs-lookup"><span data-stu-id="fc63d-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="fc63d-123">Kõik ressursi broneeringud alates sellest päevast edasi on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="fc63d-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="fc63d-124">Project Operationsis ei mõjuta hinnapakkumise sulgemine võidetud või kaotatud olekus müügivõimaluse seda olekut, mis jääb avatuks kuni käsitsi sulgemiseni.</span><span class="sxs-lookup"><span data-stu-id="fc63d-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]