---
title: Sule hinnapakkumine
description: Selles teemas kirjeldatakse hinnapakkumiste sulgemist Project Operationsis.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c429fa14b4b95420c67a91a6a59af7db2660f68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898886"
---
# <a name="close-a-quote"></a><span data-ttu-id="1c4a5-103">Sule hinnapakkumine</span><span class="sxs-lookup"><span data-stu-id="1c4a5-103">Close a quote</span></span>

<span data-ttu-id="1c4a5-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="1c4a5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1c4a5-105">Projekti hinnapakkumise saab sulgeda kui võidetu või kaotatuna.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="1c4a5-106">Kuna rakenduses Microsoft Dynamics 365 Project Operations ei toetata funktsioone Toimingud ja Muutmine, saate hinnapakkumise mustandi sulgeda.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="1c4a5-107">Hinnapakkumise sulgemine olekus Võidetud</span><span class="sxs-lookup"><span data-stu-id="1c4a5-107">Close a quote as Won</span></span>

<span data-ttu-id="1c4a5-108">Võidetud projekti hinnapakkumise sulgemine seab hinnapakkumise olekuks **Suletud** ja oleku põhjuseks **Võidetud**.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="1c4a5-109">Hinnapakkumiste sulgemine muudab selle kirjutuskaitstuks ja loob projekti lepingu mustandi koos kogu hinnapakkumise teabega.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="1c4a5-110">Kuna suletud hinnapakkumist ei saa uuesti avada, siis palutakse hinnapakkumise sulgemisel muudatused kinnitada.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="1c4a5-111">Projekti hinnapakkumise põhjal loodud projekti leping tehakse kättesaadavaks ka Project Operationsi Projektijuhtimise ja raamatupidamise moodulis.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="1c4a5-112">Kui projekti lepingut pole vastendatud projektiga ühelgi selle real, tehakse selle projekti leping passiivse projekti lepinguna saadaolevaks ja aktiveeritakse kohe, kui projekt on vastendatud vähemalt ühele selle lepingureale.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="1c4a5-113">Kui hinnapakkumine on seotud müügivõimalusega, suletakse kõik muud müügivõimaluse projekti hinnapakkumised automaatselt kaotatud kujul.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="1c4a5-114">Hinnapakkumise võidetud olekus sulgemise finantsmõju</span><span class="sxs-lookup"><span data-stu-id="1c4a5-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="1c4a5-115">Kui projektile on salvestatud tegelikke ajanäitajaid, kui see oli veel hinnapakkumise projektile lisatud, kirjendatakse ainult aja või kulutuse kulu.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="1c4a5-116">Pärast hinnapakkumise sulgemist olekus Võidetud, refaktoorib rakendus kulud, pöörates tagasi vanemad tegelikud kulud ja luues uued tegelikud kulud.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="1c4a5-117">Rakendus töötleb need tegelikud kulud võttes aluseks seotud projekti lepingurea arveldusmeetodi.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="1c4a5-118">Kui tegelik kulu viitab aja- ja materjalikulu lepingureale, loob süsteem hinnapakkumise sulgemisel ja projekti lepingu loomisel automaatselt vastavad arveldamata müügi tegelikud näitajad.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="1c4a5-119">Kui tegelik kulu viitab fikseeritud hinnaga lepingureale, peatab rakendus projekti lepingu klientide jaoks jaotatud arvete esitamise reeglitega seotud tegelike kulude ümbertöötlemise.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="1c4a5-120">Kõik ümbertöödeldud tegelikud näitajad on saadaval Projektijuhtimise ja raamatupidamise moodulis projekti raamatupidajale ülevaatamiseks, värskendamiseks ja pearaamatusse sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="1c4a5-121">Hinnapakkumise sulgemine olekus Kaotatud</span><span class="sxs-lookup"><span data-stu-id="1c4a5-121">Close a quote as Lost</span></span>

<span data-ttu-id="1c4a5-122">Kaotatud projekti hinnapakkumise sulgemine seab hinnapakkumise olekuks **Suletud** ja oleku põhjuseks **Kaotatud**.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="1c4a5-123">Hinnapakkumise sulgemine muudab selle kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="1c4a5-124">Kuna suletud hinnapakkumist ei saa uuesti avada, siis palutakse hinnapakkumise sulgemisel muudatused kinnitada.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="1c4a5-125">Kui kaotatud projekti hinnapakkumise mistahes ridadel on viidatud projektile, märgitakse ka see projekt suletuks ja mistahes ressursside broneeringud alates sellest päevast tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="1c4a5-126">Project Operationsis ei mõjuta hinnapakkumise sulgemine võidetud või kaotatud olekus müügivõimaluse seda olekut, mis jääb avatuks kuni käsitsi sulgemiseni.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
