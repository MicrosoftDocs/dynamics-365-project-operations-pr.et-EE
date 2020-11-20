---
title: Hinnapakkumise sulgemine – liht
description: Selles teemas kirjeldatakse hinnapakkumise sulgemist Project Operationsis.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175706"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="8e1f8-103">Hinnapakkumise sulgemine – liht</span><span class="sxs-lookup"><span data-stu-id="8e1f8-103">Close a quote - lite</span></span>

<span data-ttu-id="8e1f8-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="8e1f8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8e1f8-105">Projekti hinnapakkumise saab sulgeda kui võidetu või kaotatuna.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="8e1f8-106">Rakenduses Microsoft Dynamics 365 Project Operations ei toetata aktiveerimise ja muutmise toiminguid, seega saab hinnapakkumise mustandi sulgeda.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="8e1f8-107">Hinnapakkumise sulgemine olekus Võidetud</span><span class="sxs-lookup"><span data-stu-id="8e1f8-107">Close a quote as Won</span></span>

<span data-ttu-id="8e1f8-108">Võidetud projekti hinnapakkumise sulgemine suleb hinnapakkumise olekus Suletud ja oleku põhjuseks on määratud Võidetud.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="8e1f8-109">Hinnapakkumise sulgemine muudab projekti hinnapakkumise kirjutuskaitstuks ja loob projekti lepingu mustandi, mis sisaldab hinnapakkumise teavet.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="8e1f8-110">Kuna suletud hinnapakkumist ei saa uuesti avada ja muudatused on pöördumatud, kuvatakse kinnitamise dialoogiaken.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="8e1f8-111">Kui hinnapakkumine on seotud müügivõimalusega, suletakse kõik muud müügivõimaluse projekti hinnapakkumised automaatselt kaotatud kujul.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="8e1f8-112">Hinnapakkumise võidetud olekus sulgemise finantsmõju</span><span class="sxs-lookup"><span data-stu-id="8e1f8-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="8e1f8-113">Kui projektile on salvestatud tegelikke ajanäitajaid, kui see oli veel hinnapakkumise projektile lisatud, kirjendatakse ainult aja või kulutuse kulu.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="8e1f8-114">Pärast hinnapakkumise sulgemist olekus Võidetud, refaktoorib rakendus kulud, pöörates tagasi vanemad tegelikud kulud ja luues uued tegelikud kulud.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="8e1f8-115">Rakendus töötleb need tegelikud kulud võttes aluseks seotud projekti lepingurea arveldusmeetodi.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="8e1f8-116">Kui tegelik kulu viitab aja- ja materjalikulu lepingureale, loob süsteem hinnapakkumise sulgemisel ja projekti lepingu loomisel automaatselt vastavad arveldamata müügi tegelikud näitajad.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="8e1f8-117">Kui tegelik kulu viitab fikseeritud hinnaga lepingureale, peatab rakendus projekti lepingu klientide jaoks jaotatud arvete esitamise reeglitega seotud tegelike kulude ümbertöötlemise.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="8e1f8-118">Hinnapakkumise sulgemine olekus Kaotatud:</span><span class="sxs-lookup"><span data-stu-id="8e1f8-118">Closing a quote as lost:</span></span>

<span data-ttu-id="8e1f8-119">Kaotatud projekti hinnapakkumise sulgemine seab hinnapakkumise olekuks Suletud ja oleku põhjuseks Kaotatud.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="8e1f8-120">Hinnapakkumise sulgemine teeb projekti hinnapakkumise kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="8e1f8-121">Kuna suletud hinnapakkumist ei saa uuesti avada, siis palutakse hinnapakkumise sulgemisel muudatused kinnitada.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="8e1f8-122">Kui kaotatud projekti hinnapakkumise mistahes ridadel on viidatud projektile, märgitakse ka see projekt suletuks ja mistahes ressursside broneeringud alates sellest päevast tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="8e1f8-123">Project Operationsis ei mõjuta hinnapakkumise sulgemine võidetud või kaotatud olekus müügivõimaluse seda olekut, mis jääb avatuks kuni käsitsi sulgemiseni.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
