---
title: Kinnituste arendaja märkmed
description: Selles teemas antakse täiendavat arendaja teavet kinnitustega töötamise kohta.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996786"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="e5785-103">Kinnituste arendaja märkmed</span><span class="sxs-lookup"><span data-stu-id="e5785-103">Developer notes for Approvals</span></span>

<span data-ttu-id="e5785-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="e5785-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e5785-105">Dynamics 365 Project Operations sisaldab valideerimise loogikat, mis tagab õige kirje liikumise läbi kinnitamise etappide.</span><span class="sxs-lookup"><span data-stu-id="e5785-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="e5785-106">Kirjete õige üleminek tagab järgneva.</span><span class="sxs-lookup"><span data-stu-id="e5785-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="e5785-107">Seotud tabelites luuakse kõik toetavad read (nt töölehed ja tegelikud näitajad).</span><span class="sxs-lookup"><span data-stu-id="e5785-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="e5785-108">Kinnitaja märgitakse projektis enne jätkamist kui **Projekti kinnitaja**.</span><span class="sxs-lookup"><span data-stu-id="e5785-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]