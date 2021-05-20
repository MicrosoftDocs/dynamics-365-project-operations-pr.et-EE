---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 13, V3
description: Selles teemas antakse teavet selle kohta, mida on uut rakenduse Project Service Automation värskenduse väljaandes 13, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a4ebc2e6ca3f6be0a05a7240d762d7a8cf92d81b
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949449"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="d5b69-103">Rakenduse Project Service Automation, värskenduse väljaanne 13, v3</span><span class="sxs-lookup"><span data-stu-id="d5b69-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d5b69-104">Meil on hea meel teatada uusimast rakenduse Dynamics 365 Project Service Automation (PSA) värskendusest.</span><span class="sxs-lookup"><span data-stu-id="d5b69-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="d5b69-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="d5b69-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d5b69-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="d5b69-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d5b69-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskust ja avage värskenduse installimiseks lahenduste leht.</span><span class="sxs-lookup"><span data-stu-id="d5b69-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="d5b69-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d5b69-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d5b69-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 13 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="d5b69-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="d5b69-110">Selle versiooni järgu number on V3.10.3.18 ja see on saadaval järgmise ajakava järgi.</span><span class="sxs-lookup"><span data-stu-id="d5b69-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="d5b69-111">**Üldine saadavus (automaatvärskendus):** november 2019</span><span class="sxs-lookup"><span data-stu-id="d5b69-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="d5b69-112">**Automaatvärskendus:** detsember 2019</span><span class="sxs-lookup"><span data-stu-id="d5b69-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="d5b69-113">Värskenduste väljalase 13</span><span class="sxs-lookup"><span data-stu-id="d5b69-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="d5b69-114">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="d5b69-114">Bug fixes</span></span>

- <span data-ttu-id="d5b69-115">Aeg ja kulu</span><span class="sxs-lookup"><span data-stu-id="d5b69-115">Time and Expense</span></span>

     - <span data-ttu-id="d5b69-116">Parandatud: lehe **kulu kinnitamine** otsingu funktsionaalsus ei tööta, kui otsitakse kulu eesmärgi järgi.</span><span class="sxs-lookup"><span data-stu-id="d5b69-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="d5b69-117">Ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="d5b69-117">Resource Management</span></span>

     - <span data-ttu-id="d5b69-118">Parandatud: vastavusse viimise numbrid on värskendatud paremjoonduse olekusse.</span><span class="sxs-lookup"><span data-stu-id="d5b69-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="d5b69-119">Parandatud: nimega ressursse ei saa tööülesannetele määrata vahekaardi **ajakava** kaudu.</span><span class="sxs-lookup"><span data-stu-id="d5b69-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="d5b69-120">Projektijuhtimine</span><span class="sxs-lookup"><span data-stu-id="d5b69-120">Project Management</span></span>

     - <span data-ttu-id="d5b69-121">Parandatud: null viite erand meeskonnaliiget määrates, kui väärtusel **Tehingu tüüp** puudub **Üksuse** ja **Vaikerühma** seadistamise teave.</span><span class="sxs-lookup"><span data-stu-id="d5b69-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="d5b69-122">Sales</span><span class="sxs-lookup"><span data-stu-id="d5b69-122">Sales</span></span>

     - <span data-ttu-id="d5b69-123">Parandatud: topelt tehingutüübi kirjed annavad vea, kui luuakse rolli hinnakirjeid.</span><span class="sxs-lookup"><span data-stu-id="d5b69-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="d5b69-124">Parandatud: suvandite Müügivõimalused, Hinnapakkumised, Tellimuse tooted ja projektipõhiste ridade andmeruudustikus on nähtavad täiendavad nupud **Uus müügivõimalus**, **Hinnapakkumine**, **Tellimuse rida** ja **Lisa toode**.</span><span class="sxs-lookup"><span data-stu-id="d5b69-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]