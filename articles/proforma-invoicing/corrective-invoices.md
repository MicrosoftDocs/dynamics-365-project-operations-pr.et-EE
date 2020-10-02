---
title: Parandatud arved
description: Selles teemas antakse teavet parandatud arvete kohta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898076"
---
# <a name="corrected-invoices"></a><span data-ttu-id="63106-103">Parandatud arved</span><span class="sxs-lookup"><span data-stu-id="63106-103">Corrected invoices</span></span>

<span data-ttu-id="63106-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="63106-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="63106-105">Kinnitatud arveid saab muuta.</span><span class="sxs-lookup"><span data-stu-id="63106-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="63106-106">Kinnitatud arve muutmisel luuakse parandatud arve mustand.</span><span class="sxs-lookup"><span data-stu-id="63106-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="63106-107">Kuna eeldame, et soovite kõik kanded ja kogused algsest arvest ümber pöörata, kaasatakse selle parandatud arve kõik algse arve tehingud ja kõik selle kogused on null (0).</span><span class="sxs-lookup"><span data-stu-id="63106-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="63106-108">Kui mõni kanne ei vaja korrigeerimist, saate need korrigeeriva arve mustandist eemaldada.</span><span class="sxs-lookup"><span data-stu-id="63106-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="63106-109">Ainult osalise koguse ümber pööramiseks või tagastamiseks, saate rea üksikasjade välja Kogus redigeerida.</span><span class="sxs-lookup"><span data-stu-id="63106-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="63106-110">Arve rea üksikasjade avamisel näete algse arve kogust.</span><span class="sxs-lookup"><span data-stu-id="63106-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="63106-111">Seejärel saate praegust arve kogust redigeerida nii, et see on algse arve kogusest väiksem või suurem.</span><span class="sxs-lookup"><span data-stu-id="63106-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="63106-112">Korrigeeriva arve kinnitamisel tühistatakse algselt arvestatud müügi tegelik väärtus ja luuakse uus tegelik arve.</span><span class="sxs-lookup"><span data-stu-id="63106-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="63106-113">Kui kogust on vähendatud, põhjustab erinevus uue arveldamata müügi tegeliku loomise.</span><span class="sxs-lookup"><span data-stu-id="63106-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="63106-114">Näiteks kui algne arvestatud müük oli kaheksa tundi ja parandatud arverea üksikasjadel on vähendatud kogust kuus tundi, pööratakse algne arvestatud müügirida ümber ja luuakse kaks uut tegelikku väärtust.</span><span class="sxs-lookup"><span data-stu-id="63106-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="63106-115">Arvestatud müük on tegelikult kuus tundi.</span><span class="sxs-lookup"><span data-stu-id="63106-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="63106-116">Ülejäänud kahe tunni eest arveldamata müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="63106-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="63106-117">See tehing võib olla kas hiljem arvestatud või märgitud mitte-tasuna, olenevalt läbirääkimistest kliendiga.</span><span class="sxs-lookup"><span data-stu-id="63106-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
