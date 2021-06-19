---
title: Arve automaatse loomise konfigureerimine
description: Selles teemas antakse teavet, kuidas konfigureerida süsteemi, et luua arveid automaatselt.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dffa95c163f7f8d5074e02cd56d6f1ed429a7c72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005336"
---
# <a name="configure-automatic-invoice-creation"></a><span data-ttu-id="f68a4-103">Arve automaatse loomise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f68a4-103">Configure automatic invoice creation</span></span>

<span data-ttu-id="f68a4-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="f68a4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="f68a4-105">Läbige järgmised etapid, et konfigureerida Dynamics 365 Project Operationsis automaatne arve käitamine.</span><span class="sxs-lookup"><span data-stu-id="f68a4-105">Complete the following steps to configure an automated invoice run in Dynamics 365 Project operations.</span></span>

1. <span data-ttu-id="f68a4-106">Avage **Sätted** > **Pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="f68a4-106">Go to **Settings** > **Batch jobs**.</span></span>
2. <span data-ttu-id="f68a4-107">Looge pakett-töö ja pange sellele nimeks **Projecti toimingute arvete loomine**.</span><span class="sxs-lookup"><span data-stu-id="f68a4-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="f68a4-108">Pakett-töö nimi peab sisaldama sõnu „arvete loomine”.</span><span class="sxs-lookup"><span data-stu-id="f68a4-108">The name of the batch job must include the words "create invoices."</span></span>
3. <span data-ttu-id="f68a4-109">Valige väljal **Töö tüüp** väärtus **Puudub**.</span><span class="sxs-lookup"><span data-stu-id="f68a4-109">In the **Job Type** field, select **None**.</span></span> <span data-ttu-id="f68a4-110">Vaikimisi on suvandite **Sageduse päev** ja **On aktiivne** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f68a4-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="f68a4-111">Valige **Käivita töövoog**.</span><span class="sxs-lookup"><span data-stu-id="f68a4-111">Select **Run Workflow**.</span></span> <span data-ttu-id="f68a4-112">Näete dialoogiboksis **Kirje otsimine** kolme töövoogu.</span><span class="sxs-lookup"><span data-stu-id="f68a4-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="f68a4-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="f68a4-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="f68a4-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="f68a4-114">ProcessRunner</span></span>
    - <span data-ttu-id="f68a4-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="f68a4-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="f68a4-116">Valige **ProcessRunCaller** ja seejärel **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="f68a4-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="f68a4-117">Valige järgmises dialoogiboksis **OK**.</span><span class="sxs-lookup"><span data-stu-id="f68a4-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="f68a4-118">**Unerežiimi** töövoole järgneb **protsessi** töövoog.</span><span class="sxs-lookup"><span data-stu-id="f68a4-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

  > [!NOTE]
  > <span data-ttu-id="f68a4-119">Etapis 5 saate valida ka töövoo **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="f68a4-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="f68a4-120">Seejärel, kui valite **OK**, järgneb **protsessi** töövoole **unerežiimi** töövoog.</span><span class="sxs-lookup"><span data-stu-id="f68a4-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="f68a4-121">Töövood **ProcessRunCaller** ja **ProcessRunner** loovad arveid.</span><span class="sxs-lookup"><span data-stu-id="f68a4-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="f68a4-122">**ProcessRunCaller** kutsub töövoo **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="f68a4-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="f68a4-123">**ProcessRunner** on töövoog, mis tegelikult loob arveid.</span><span class="sxs-lookup"><span data-stu-id="f68a4-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="f68a4-124">See läbib kõik lepinguread, mille jaoks tuleb arved luua, ja see loob neile ridadele arveid.</span><span class="sxs-lookup"><span data-stu-id="f68a4-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="f68a4-125">Selleks et määratleda lepingu read, mille jaoks arved tuleb luua, vaatab töö lepingurea arve käivitamise kuupäevi.</span><span class="sxs-lookup"><span data-stu-id="f68a4-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="f68a4-126">Kui ühele lepingule kuuluvatel lepinguridadel on sama arve käivitamise päev, kombineeritakse tehingud ühe arvega, millel on kaks arve rida.</span><span class="sxs-lookup"><span data-stu-id="f68a4-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="f68a4-127">Kui arvete loomiseks pole kandeid, jätab töö arve loomise vahele.</span><span class="sxs-lookup"><span data-stu-id="f68a4-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="f68a4-128">Kui **ProcessRunner** on töö lõpetanud, kutsub see töövoo **ProcessRunCaller**, annab lõppkellaaja ja sulgub.</span><span class="sxs-lookup"><span data-stu-id="f68a4-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="f68a4-129">**ProcessRunCaller** käivitab seejärel taimeri, mis kestab määratud lõppkellaajast 24 tundi.</span><span class="sxs-lookup"><span data-stu-id="f68a4-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="f68a4-130">Taimeri lõpus on **ProcessRunCaller** suletud.</span><span class="sxs-lookup"><span data-stu-id="f68a4-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="f68a4-131">Arvete loomiseks kasutatav pakktöötluse töö on korduv töö.</span><span class="sxs-lookup"><span data-stu-id="f68a4-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="f68a4-132">Kui seda pakktöötlust käitatakse mitu korda, luuakse mitu tööeksemplari ja need põhjustavad tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="f68a4-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="f68a4-133">Seetõttu peaksite pakktöötluse käivitama ainult üks kord ja selle peate uuesti käivitama ainult siis, kui see lakkab töötamast.</span><span class="sxs-lookup"><span data-stu-id="f68a4-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="f68a4-134">Pakett-arveldamine töötab ainult projekti lepinguridade jaoks, mis on arvegraafikute poolt konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="f68a4-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="f68a4-135">Fikseeritud hinnaga arveldusmeetodiga lepingureal peavad olema seadistatud vahe-eesmärgid.</span><span class="sxs-lookup"><span data-stu-id="f68a4-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="f68a4-136">Aja- ja materjalikulu arveldusmeetodiga projekti lepingurea jaoks peab olema seadistatud kuupäevapõhine ajakava.</span><span class="sxs-lookup"><span data-stu-id="f68a4-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="f68a4-137">Sama kehtib ka projektipõhisele lepingureale.</span><span class="sxs-lookup"><span data-stu-id="f68a4-137">The same applies to a project-based contract line.</span></span>     


[!INCLUDE[footer-include](../includes/footer-banner.md)]