---
title: Kinnituste arendaja märkmed
description: Selles teemas antakse täiendavat arendaja teavet kinnitustega töötamise kohta.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290264"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="23970-103">Kinnituste arendaja märkmed</span><span class="sxs-lookup"><span data-stu-id="23970-103">Developer notes for Approvals</span></span>

<span data-ttu-id="23970-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="23970-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="23970-105">Dynamics 365 Project Operations sisaldab valideerimise loogikat, mis tagab õige kirje liikumise läbi kinnitamise etappide.</span><span class="sxs-lookup"><span data-stu-id="23970-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="23970-106">Kirjete õige üleminek tagab järgneva.</span><span class="sxs-lookup"><span data-stu-id="23970-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="23970-107">Seotud tabelites luuakse kõik toetavad read (nt töölehed ja tegelikud näitajad).</span><span class="sxs-lookup"><span data-stu-id="23970-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="23970-108">Kinnitaja märgitakse projektis enne jätkamist kui **Projekti kinnitaja**.</span><span class="sxs-lookup"><span data-stu-id="23970-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]