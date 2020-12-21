---
title: Perioodi tüübid
description: See teema sisaldab teavet selle kohta, kuidas häälestada tulukalkulatsiooni perioodi tüübid.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531407"
---
# <a name="period-types"></a><span data-ttu-id="7106a-103">Perioodi tüübid</span><span class="sxs-lookup"><span data-stu-id="7106a-103">Period types</span></span>

<span data-ttu-id="7106a-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="7106a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7106a-105">Perioodi tüüp määratleb, kui sageli projekti tulusid arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="7106a-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="7106a-106">See teema sisaldab teavet selle kohta, kuidas häälestada tulukalkulatsiooni perioodi tüübid.</span><span class="sxs-lookup"><span data-stu-id="7106a-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="7106a-107">Perioodi tüüpide loomine ja nendega töötamine</span><span class="sxs-lookup"><span data-stu-id="7106a-107">Create and work with period types</span></span>
<span data-ttu-id="7106a-108">Perioodi tüüpide loomiseks ja nendega töötamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="7106a-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="7106a-109">Avage oma rakenduse Dynamics 365 Finance keskkonnas suvand **Projektihaldus ja raamatupidamine** > **Häälestus** > **Kalkulatsioonid** > **Perioodi tüübid**.</span><span class="sxs-lookup"><span data-stu-id="7106a-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="7106a-110">Uue perioodi tüübi loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7106a-110">Select **New** to create new period type.</span></span> <span data-ttu-id="7106a-111">Sisestage nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="7106a-111">Enter a name and description.</span></span>
3. <span data-ttu-id="7106a-112">Väljal **Sagedus** valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="7106a-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="7106a-113">Kui valite väärtuse **Nädal**, **Kaks korda nädalas**, **Kaks korda kuus**, **Nädal**, **Päev**, **Kvartal** või **Aasta**, kasutatakse perioodide loomiseks kalendrit.</span><span class="sxs-lookup"><span data-stu-id="7106a-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="7106a-114">Kui valite suvandi **Pearaamatu periood**, kasutatakse perioodide loomiseks pearaamatu perioode pearaamatu konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="7106a-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="7106a-115">Kui valite **Piiramatu**, saate määrata kohandatud perioodid.</span><span class="sxs-lookup"><span data-stu-id="7106a-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="7106a-116">Valige perioodi tüübi kirje ja seejärel valige käsk **Loo perioodid**, et luua perioodi tüübi jaoks perioodid.</span><span class="sxs-lookup"><span data-stu-id="7106a-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="7106a-117">Valitud perioodi sageduse põhjal võib teil olla valik määratleda alguskuupäev või loodavate perioodide arv.</span><span class="sxs-lookup"><span data-stu-id="7106a-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="7106a-118">Loodud perioodide läbivaatamiseks valige **Perioodid**.</span><span class="sxs-lookup"><span data-stu-id="7106a-118">Select **Periods** to review generated periods.</span></span>

