---
title: Logimata materjalide ostmine ootel oleva hankija arve abil
description: Selles teemas kirjeldatakse, kuidas kirjendada ootel hankija arveid.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880636"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="17686-103">Logimata materjalide ostmine ootel oleva hankija arve abil</span><span class="sxs-lookup"><span data-stu-id="17686-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="17686-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="17686-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="17686-105">Kuna ettevõttes kasutatakse projekti jaoks logimata materjale, saab kulud kohe projekti kohta kirjendada.</span><span class="sxs-lookup"><span data-stu-id="17686-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="17686-106">Näiteks teeb ettevõte Contoso Robotics US tarkvara uuendamise projekti ja vajab tarkvaralitsentse.</span><span class="sxs-lookup"><span data-stu-id="17686-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="17686-107">Need litsentsid on pärit kolmandalt osapoolelt.</span><span class="sxs-lookup"><span data-stu-id="17686-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="17686-108">Funktsiooni Dynamics 365 Finance kasutamisel fikseerib ostureskontro ametnik ootel oleva hankija arve dokumendi ja omistab litsentsikulud otse seadmete uuendamise projektile.</span><span class="sxs-lookup"><span data-stu-id="17686-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="17686-109">Enne selles teemas kirjeldatud funktsioonide kasutamist vaadake üle ja rakendage nõutavad konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="17686-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="17686-110">Lisateavet leiate teemast [Logimata materjalide ja ootel hankija arvete lubamine](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="17686-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="17686-111">Projektiga seotud ootel hankija arve postitamine</span><span class="sxs-lookup"><span data-stu-id="17686-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="17686-112">Ootel hankija arved saab registreerida lehel **Ootel tarnija arved** (**Ostureskontro** > **Arved** > **Ootel hankijate arved**).</span><span class="sxs-lookup"><span data-stu-id="17686-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="17686-113">Projektiga seotud ootel hankija arve postitamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="17686-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="17686-114">Minge jaotisesse **Ostureskontro** > **Arved** ja valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="17686-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="17686-115">Valige väljal **Arve konto** soovitud tarnija ja sisestage väljal **Number** hankija arve ID.</span><span class="sxs-lookup"><span data-stu-id="17686-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="17686-116">Lisage rida hankija arvele ja valige väljal **Üksuse number** tarnijalt ostetud logimata üksus.</span><span class="sxs-lookup"><span data-stu-id="17686-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="17686-117">Hankija arve ridu, mis põhinevad hankekategoorial, ei saa projekti suhtes registreerida.</span><span class="sxs-lookup"><span data-stu-id="17686-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="17686-118">Lisage ostetud kogus.</span><span class="sxs-lookup"><span data-stu-id="17686-118">Add the quantity purchased.</span></span> <span data-ttu-id="17686-119">Süsteem asustab ühikuhinna logimata üksuse hinna konfiguratsiooni kohaselt.</span><span class="sxs-lookup"><span data-stu-id="17686-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="17686-120">Kontrollige real kogusummat ja muid nõutud üksikasju.</span><span class="sxs-lookup"><span data-stu-id="17686-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="17686-121">Valige rea üksikasjade vahekaardil **Projekt** selle projekti ID, kus see üksus registreeritakse.</span><span class="sxs-lookup"><span data-stu-id="17686-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="17686-122">Soovi korral valige tegevuse number ning värskendage projekti kategooriat ja rea atribuuti.</span><span class="sxs-lookup"><span data-stu-id="17686-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="17686-123">Sisestage ootel hankija arve.</span><span class="sxs-lookup"><span data-stu-id="17686-123">Post pending vendor invoice.</span></span> <span data-ttu-id="17686-124">Arve sisestamisel salvestab süsteem järgmised andmed.</span><span class="sxs-lookup"><span data-stu-id="17686-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="17686-125">Hankija saldosumma.</span><span class="sxs-lookup"><span data-stu-id="17686-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="17686-126">Käibemaksu summa.</span><span class="sxs-lookup"><span data-stu-id="17686-126">The sales tax amount.</span></span>
    - <span data-ttu-id="17686-127">Projektiga seotud kulud kirjendatakse hanke integreerimise kontole.</span><span class="sxs-lookup"><span data-stu-id="17686-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="17686-128">Projekti tegelik kande väärtus Dataverse’is.</span><span class="sxs-lookup"><span data-stu-id="17686-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="17686-129">Seda tehingut töödeldakse edasi, kasutades [Project Operationsi integreerimise töölehte](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="17686-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="17686-130">Selle töölehe sisestamine teisaldab summa hanke integreerimise kontolt projekti kulu kontole.</span><span class="sxs-lookup"><span data-stu-id="17686-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
