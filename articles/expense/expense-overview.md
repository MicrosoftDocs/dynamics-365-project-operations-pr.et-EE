---
title: Kulude ülevaade
description: Selles teemas kirjeldatakse tööd rakenduse Project Operations kulufunktsioone.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6c5ef2a45e8141bda38baf3eaf0a403d6db95e48
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122825"
---
# <a name="expense-home-page"></a><span data-ttu-id="2115a-103">Kulu avaleht</span><span class="sxs-lookup"><span data-stu-id="2115a-103">Expense home page</span></span>

<span data-ttu-id="2115a-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="2115a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="2115a-105">Dynamics 365 Project Operations toetab kulude töötlemise võimalust.</span><span class="sxs-lookup"><span data-stu-id="2115a-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="2115a-106">Kulude töötlemine toimub koos või ilma projektideta, kasutades poliitikate, tehingute kategooriate ja kinnituste kohandatavaod töövoogusid.</span><span class="sxs-lookup"><span data-stu-id="2115a-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="2115a-107">Rakenduses Project Operation on kaks toetatud kulude juurutamise mudelit.</span><span class="sxs-lookup"><span data-stu-id="2115a-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="2115a-108">**Täielik**: täielik juurutus on saadaval valikule **Project Operations ressursipõhiste/mitteladustatavate stsenaariumite jaoks** või **Project Operations tootmistellimuse põhiste stsenaariumite jaoks**.</span><span class="sxs-lookup"><span data-stu-id="2115a-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="2115a-109">**Põhiline**: põhijuurutus on saadaval valikule **Project Operations ressursipõhiste/mitteaktsiapõhiste stsenaariumite jaoks** ja **Lite’i juurutamine – tehing näidisarveldusele**.</span><span class="sxs-lookup"><span data-stu-id="2115a-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="2115a-110">Täielik</span><span class="sxs-lookup"><span data-stu-id="2115a-110">Full</span></span> 
<span data-ttu-id="2115a-111">Täieliku kulude juurutamine tagab täieliku poliitika jõustamise, mis sisaldab võimalust luua poliitikaid, näiteks järgmised.</span><span class="sxs-lookup"><span data-stu-id="2115a-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="2115a-112">Kulukategooria limiidid</span><span class="sxs-lookup"><span data-stu-id="2115a-112">Expense category limits</span></span>
  - <span data-ttu-id="2115a-113">Reisi</span><span class="sxs-lookup"><span data-stu-id="2115a-113">Travel</span></span>
  - <span data-ttu-id="2115a-114">Päevaraha</span><span class="sxs-lookup"><span data-stu-id="2115a-114">Per diem</span></span>
  - <span data-ttu-id="2115a-115">Krediitkaardi importimised</span><span class="sxs-lookup"><span data-stu-id="2115a-115">Credit card imports</span></span>
  - <span data-ttu-id="2115a-116">Kviitungi optilise märgi tuvastus</span><span class="sxs-lookup"><span data-stu-id="2115a-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="2115a-117">Elementaarne</span><span class="sxs-lookup"><span data-stu-id="2115a-117">Basic</span></span> 
<span data-ttu-id="2115a-118">Põhiline kulude juurutuse stsenaarium võimaldab teil kirjendada ainult projektiga seotud põhikulusid.</span><span class="sxs-lookup"><span data-stu-id="2115a-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="2115a-119">Lisateavet leiate teemast [Kulu kirje (lite)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="2115a-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="2115a-120">Kulu juurutamise määratlemine</span><span class="sxs-lookup"><span data-stu-id="2115a-120">Determine your Expense deployment</span></span>
<span data-ttu-id="2115a-121">Et teha kindlaks, kas teil töötab põhiline kuluhalduse juurutus, veenduge, et aadressi URL-i lõpuks oleks **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="2115a-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
