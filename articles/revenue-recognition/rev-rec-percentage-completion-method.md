---
title: Fikseeritud hinnaga tulukalkulatsiooniga projektid
description: Selles teemas antakse teavet projektide fikseeritud hinnaga prognoosi kohta.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278908"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="94924-103">Fikseeritud hinnaga tulukalkulatsiooniga projektid</span><span class="sxs-lookup"><span data-stu-id="94924-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="94924-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="94924-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="94924-105">Kui te loote rakenduses Dynamics 365 Project Operations teenuses Microsoft Dataverse järgmiste atribuutidega projekti lepingurea, loob süsteem automaatselt fikseeritud hinnaga tulukalkulatsiooniga projekti.</span><span class="sxs-lookup"><span data-stu-id="94924-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="94924-106">Selle projekti teave põhineb järgneval.</span><span class="sxs-lookup"><span data-stu-id="94924-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="94924-107">Fikseeritud hinnaga arveldusmeetod.</span><span class="sxs-lookup"><span data-stu-id="94924-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="94924-108">Seostatud projekt.</span><span class="sxs-lookup"><span data-stu-id="94924-108">An associated project.</span></span>
  - <span data-ttu-id="94924-109">Vähemalt üks vahe-eesmärk, mis on määratletud vahekaardil **Arve ajakava** lehel **Projekti lepingurida**.</span><span class="sxs-lookup"><span data-stu-id="94924-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="94924-110">Fikseeritud hinnaga tulukalkulatsioonidega projektide läbivaatamine</span><span class="sxs-lookup"><span data-stu-id="94924-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="94924-111">Fikseeritud hinnaga tulukalkulatsioonidega projektide läbivaatamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="94924-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="94924-112">Avage rakenduse Dynamics 365 Finance keskkonnas suvand **Projektihaldus ja raamatupidamine** > **Projektid** > **Fikseeritud hinnaga tulukalkulatsiooniga projektid**.</span><span class="sxs-lookup"><span data-stu-id="94924-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="94924-113">Valige projekt, mida soovite vaadata, ja topeltklõpsake suvandit **Hinnangu projekti ID**, et avada kirje ja vaadata läbi projekti üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="94924-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="94924-114">Laiendage vahekaarti **Projekt**. Näete ruudustikus **Valitud projektid** ühte projekti.</span><span class="sxs-lookup"><span data-stu-id="94924-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="94924-115">Süsteem kasutab seda vaikimisi projektina, kuna see on projekti lepingureaga seostatud projekt.</span><span class="sxs-lookup"><span data-stu-id="94924-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="94924-116">Seose muutmiseks valige täiendavad projektid ja lisage need ruudustikku **Valitud projektid**.</span><span class="sxs-lookup"><span data-stu-id="94924-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="94924-117">Kui selles ruudustikus on valitud mitu projekti, siis projekti lõpuleviimise protsent ja tulukalkulatsioonid arvutatakse kõikide valitud projektide jaoks koos.</span><span class="sxs-lookup"><span data-stu-id="94924-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="94924-118">Projekti kulu, tuluprofiili, kulumalli ja perioodi koodi saab määrata käsitsi.</span><span class="sxs-lookup"><span data-stu-id="94924-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="94924-119">Kui neid käsitsi ei määrata, lisatakse väärtuste vaikeväärtused projekti esimese hinnangu arvutamise ajal, mis kasutab projektikulu ja tuluprofiilide jaoks konfigureeritud reegleid.</span><span class="sxs-lookup"><span data-stu-id="94924-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]