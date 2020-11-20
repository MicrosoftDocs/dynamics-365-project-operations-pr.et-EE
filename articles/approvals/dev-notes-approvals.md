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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483943"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="09258-103">Kinnituste arendaja märkmed</span><span class="sxs-lookup"><span data-stu-id="09258-103">Developer notes for Approvals</span></span>

<span data-ttu-id="09258-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="09258-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="09258-105">Dynamics 365 Project Operations sisaldab valideerimise loogikat, mis tagab õige kirje liikumise läbi kinnitamise etappide.</span><span class="sxs-lookup"><span data-stu-id="09258-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="09258-106">Kirjete õige üleminek tagab järgneva.</span><span class="sxs-lookup"><span data-stu-id="09258-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="09258-107">Seotud tabelites luuakse kõik toetavad read (nt töölehed ja tegelikud näitajad).</span><span class="sxs-lookup"><span data-stu-id="09258-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="09258-108">Kinnitaja märgitakse projektis enne jätkamist kui **Projekti kinnitaja**.</span><span class="sxs-lookup"><span data-stu-id="09258-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
