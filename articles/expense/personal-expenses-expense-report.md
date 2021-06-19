---
title: Töö kuluaruande isiklike kuludega
description: Selles teemas antakse teavet selle kohta, kuidas toimida töötajate poolt äri eesmärgil reisides tekkinud isiklike kuludega.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025679"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="56596-103">Töö kuluaruande isiklike kuludega</span><span class="sxs-lookup"><span data-stu-id="56596-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="56596-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="56596-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="56596-105">Töötaja võib ärireisi ajal tasuda ettevõtte krediitkaarida isiklike kulude eest.</span><span class="sxs-lookup"><span data-stu-id="56596-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="56596-106">Kui isiklike kulude käsitlemiseks pole toiminguid määratletud, võib see, kui töötaja esitab oma üksikasjaliku kuluaruande, häirida kuluaruande kinnitamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="56596-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="56596-107">Töötaja isiklike kuludega töötamiseks võib kasutada kahte meetodit.</span><span class="sxs-lookup"><span data-stu-id="56596-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="56596-108">**Maksab töötaja**: teie organisatsioon ei tasu ettevõtte krediitkaardil kuvatavaid isiklikke kulusid.</span><span class="sxs-lookup"><span data-stu-id="56596-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="56596-109">Selle asemel maksate töötaja kulude eest otse krediitkaardi väljastajale.</span><span class="sxs-lookup"><span data-stu-id="56596-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="56596-110">**Maksab ettevõte:** teie ettevõte maksab ettevõtte krediitkaardi kogu arve ja seejärel võtab isiklike kulude summa maha töötaja kontolt.</span><span class="sxs-lookup"><span data-stu-id="56596-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="56596-111">Saate valida meetodi, mida teie ettevõte kasutab, lehel **Kulu haldamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="56596-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="56596-112">Tükeldatud kulufunktsiooni lubamine, kui isikliku summa väljal on väärtus määratletud</span><span class="sxs-lookup"><span data-stu-id="56596-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="56596-113">Funktsioon **Luba tükeldatud kulufunktsioon, kui isikliku summa väljal on väärtus määratletud** rakendub ainult kuluaruannetele, mis on reataseme töövoo abil kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="56596-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="56596-114">Aruanded kinnitatakse, kui minnakse jaotiss **Kuluaruannete töötlemine** > **Mulle määratud kuluaruanded** > **Ava kuluaruanne**.</span><span class="sxs-lookup"><span data-stu-id="56596-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="56596-115">Selle funktsiooni lubamiseks avage **Tööruumid** > **Funktsioonihaldus**, valige **Luba tükeldatud kulufunktsioon, kui isikliku summa väljal on väärtus määratletud** ja valige seejärel **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="56596-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="56596-116">Kui funktsioon on lubatud, genereerivad seda funktsiooni kasutavad kuluread aruande esitamisel kaks rida.</span><span class="sxs-lookup"><span data-stu-id="56596-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="56596-117">Luuakse kaks rida, et kinnitaja saaks iga rea eraldi kinnitada.</span><span class="sxs-lookup"><span data-stu-id="56596-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
