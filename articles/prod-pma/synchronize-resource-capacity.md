---
title: Ressursi võimsuse sünkroonimine
description: Selles teemas antakse teavet ressursi võimsuse sünkroonimise kohta kalendrites ja projektides.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288554"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="553d8-103">Ressursi võimsuse sünkroonimine</span><span class="sxs-lookup"><span data-stu-id="553d8-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="553d8-104">Ressursi sünkroonimise protsess aitab tagada, et teave kalendrist ja põhikalendrist liiguks alla projekti ressursi ajastamisse.</span><span class="sxs-lookup"><span data-stu-id="553d8-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="553d8-105">Kui kalendrit muudetakse, teevad protsessid projekti ressursside ajastamisse nõutavaid värskendusi.</span><span class="sxs-lookup"><span data-stu-id="553d8-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="553d8-106">Protsessid aitavad ka parandada jõudlust, kuna kalendri ressursi teave sünkroonitakse eelnevalt.</span><span class="sxs-lookup"><span data-stu-id="553d8-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="553d8-107">Seetõttu toimuvad ressursside kavandamise teabe värskendused kiiremini.</span><span class="sxs-lookup"><span data-stu-id="553d8-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="553d8-108">Soovitame ajastada protsessid partiidena, mitte üks korraga.</span><span class="sxs-lookup"><span data-stu-id="553d8-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="553d8-109">Vastasel juhul on oht, et keegi unustab kaasavad kuupäevad, millal teavet viimati sünkrooniti.</span><span class="sxs-lookup"><span data-stu-id="553d8-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="553d8-110">Kui kaasavaid kuupäevi ei kasutata, võib kuupäevade sünkroonimise ajal esineda vahesid.</span><span class="sxs-lookup"><span data-stu-id="553d8-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalendri sünkroonimine](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="553d8-112">Ressursi võimsuse sünkroonimise ümberarvestused</span><span class="sxs-lookup"><span data-stu-id="553d8-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="553d8-113">Sünkroniseerimisprotsess on loodud sünkroonima kogu ressursi kalendri teabe.</span><span class="sxs-lookup"><span data-stu-id="553d8-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="553d8-114">See teave hõlmab põhikalendri teavet mis tahes muudatuste kohta projekti ressursi kalendri võimsuse tabelis.</span><span class="sxs-lookup"><span data-stu-id="553d8-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="553d8-115">Kui projekti lisatakse uusi ressursse, aitab sünkroonimine tagada, et saadaval oleks värskendatud kalendri teave.</span><span class="sxs-lookup"><span data-stu-id="553d8-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="553d8-116">Seda sünkroonimist saab teha igal ajal.</span><span class="sxs-lookup"><span data-stu-id="553d8-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="553d8-117">Me soovitame kasutada partiid.</span><span class="sxs-lookup"><span data-stu-id="553d8-117">We recommend that you use a batch.</span></span> <span data-ttu-id="553d8-118">Valikud on võimsuse reserveeringute sünkroonimise ajal saadaval.</span><span class="sxs-lookup"><span data-stu-id="553d8-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="553d8-119">Valige **Projektihaldus ja raamatupidamine** &gt; **Perioodiline** &gt; **Võimsuse sünkroonimine** &gt; **Ressursside võimsuse sünkroonimise ümberarvestused**.</span><span class="sxs-lookup"><span data-stu-id="553d8-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="553d8-120">Määrake järgmises tabelis valikud.</span><span class="sxs-lookup"><span data-stu-id="553d8-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="553d8-121">Suvand</span><span class="sxs-lookup"><span data-stu-id="553d8-121">Option</span></span>      | <span data-ttu-id="553d8-122">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="553d8-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="553d8-123">Perioodi kood</span><span class="sxs-lookup"><span data-stu-id="553d8-123">Period code</span></span> | <span data-ttu-id="553d8-124">Võite ka valida pearaamatu kuupäevaintervalli koodi, et määrata sünkroniseerimisprotsessi algus- ja lõpukuupäevad ressursi võimsuse ümberarvestuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="553d8-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="553d8-125">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="553d8-125">Start date</span></span>  | <span data-ttu-id="553d8-126">Sisestage ressursi võimsuse ümberarvestuse sünkroniseerimisprotsessi alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="553d8-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="553d8-127">Lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="553d8-127">End date</span></span>    | <span data-ttu-id="553d8-128">Sisestage ressursi võimsuse ümberarvestuse sünkroniseerimisprotsessi lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="553d8-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="553d8-129">[![Sünkroonimisprotsess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="553d8-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]