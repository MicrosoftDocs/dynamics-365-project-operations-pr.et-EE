---
title: Mida on uut rakenduse Project Service Automation värskenduse väljaandes 13, v3
description: Selles teemas antakse teavet selle kohta, mida on uut rakenduse Project Service Automation värskenduse väljaandes 13, v3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750964"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="f7afd-103">Rakenduse Project Service Automation V3, värskenduse väljaanne 13</span><span class="sxs-lookup"><span data-stu-id="f7afd-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="f7afd-104">Meil on hea meel teatada uusimast rakenduse Dynamics 365 Project Service Automation (PSA) värskendusest.</span><span class="sxs-lookup"><span data-stu-id="f7afd-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="f7afd-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="f7afd-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f7afd-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="f7afd-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f7afd-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskust ja avage värskenduse installimiseks lahenduste leht.</span><span class="sxs-lookup"><span data-stu-id="f7afd-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="f7afd-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f7afd-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f7afd-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 13 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="f7afd-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="f7afd-110">Selle versiooni järgu number on V3.10.3.18 ja see on saadaval järgmise ajakava järgi.</span><span class="sxs-lookup"><span data-stu-id="f7afd-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="f7afd-111">**Üldine saadavus (automaatvärskendus):** november 2019</span><span class="sxs-lookup"><span data-stu-id="f7afd-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="f7afd-112">**Automaatvärskendus:** detsember 2019</span><span class="sxs-lookup"><span data-stu-id="f7afd-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="f7afd-113">Värskenduste väljalase 13</span><span class="sxs-lookup"><span data-stu-id="f7afd-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="f7afd-114">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="f7afd-114">Bug fixes</span></span>

- <span data-ttu-id="f7afd-115">Aeg ja kulu</span><span class="sxs-lookup"><span data-stu-id="f7afd-115">Time and Expense</span></span>

     - <span data-ttu-id="f7afd-116">Parandatud: lehe **kulu kinnitamine** otsingu funktsionaalsus ei tööta, kui otsitakse kulu eesmärgi järgi.</span><span class="sxs-lookup"><span data-stu-id="f7afd-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="f7afd-117">Ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="f7afd-117">Resource Management</span></span>

     - <span data-ttu-id="f7afd-118">Parandatud: vastavusse viimise numbrid on värskendatud paremjoonduse olekusse.</span><span class="sxs-lookup"><span data-stu-id="f7afd-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="f7afd-119">Parandatud: nimega ressursse ei saa tööülesannetele määrata vahekaardi **ajakava** kaudu.</span><span class="sxs-lookup"><span data-stu-id="f7afd-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="f7afd-120">Projektijuhtimine</span><span class="sxs-lookup"><span data-stu-id="f7afd-120">Project Management</span></span>

     - <span data-ttu-id="f7afd-121">Parandatud: null viite erand meeskonnaliiget määrates, kui väärtusel **Tehingu tüüp** puudub **Üksuse** ja **Vaikerühma** seadistamise teave.</span><span class="sxs-lookup"><span data-stu-id="f7afd-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="f7afd-122">Sales</span><span class="sxs-lookup"><span data-stu-id="f7afd-122">Sales</span></span>

     - <span data-ttu-id="f7afd-123">Parandatud: topelt tehingutüübi kirjed annavad vea, kui luuakse rolli hinnakirjeid.</span><span class="sxs-lookup"><span data-stu-id="f7afd-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="f7afd-124">Parandatud: täiendavad nupud **Uus müügivõimalus**, **Hinnapakkumine**, **Tellimuserida**ja **Lisa toote** on nähtavad võimaluste, hinnapakkumiste, tellimuse toodete ja projektipõhiste andmeruudustiku ridadel.</span><span class="sxs-lookup"><span data-stu-id="f7afd-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


