---
title: Lisandmooduli atribuutide värskendamine uute hinnakujunduse dimensioonide lisamiseks
description: Selles teemas kirjeldatakse hinnakujunduse dimensioonide jaoks lisandmooduli atribuutide värskendamist.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 603b0e9a10dc2fe23c9fa0fa7065bc3f500dc540
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147063"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="77b6c-103">Lisandmooduli atribuutide värskendamine uute hinnakujunduse dimensioonide lisamiseks</span><span class="sxs-lookup"><span data-stu-id="77b6c-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="77b6c-104">Kui te ei kasuta Project Service Automation (PSA) hinnapakkumise tegemise ja lepingute sõlmimise funktsioone, võite selle teema vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="77b6c-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="77b6c-105">See teema eeldab, et olete lõpetanud toimingud teemades [Kohandatud väljade ja olemite loomine](create-custom-fields-entities.md), [Kohandatud väljade lisamine hinna seadistamisele ja ülekande olemitele](field-references.md) ning [Kohandatud väljade seadistamine hinnakujunduse dimensioonidena](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="77b6c-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="77b6c-106">Kui te pole neid toiminguid lõpetanud, minge tagasi, viige need lõpuni ja seejärel tulge selle teema juurde tagasi.</span><span class="sxs-lookup"><span data-stu-id="77b6c-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="77b6c-107">Kui projekti hinnapakkumise rea jaoks luuakse hinnapakkumise rea üksikasjad lehel **Hinnapakkumise rida**, loob süsteem taustal kaks prognoosirida: üks rida prognoosi kulu poolele ja teine müügi poolele.</span><span class="sxs-lookup"><span data-stu-id="77b6c-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="77b6c-108">Sama kehtib ka projekti lepinguridade kohta.</span><span class="sxs-lookup"><span data-stu-id="77b6c-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="77b6c-109">Kui muudate kulupoole kogust või välja, kantakse see muudatus üle ka müügipoolele.</span><span class="sxs-lookup"><span data-stu-id="77b6c-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="77b6c-110">See on võimalik tänu järgnevatele lisandmoodulitele, mida tuleb pärast hinnakujunduse dimensioonide muutmist uuesti registreerida.</span><span class="sxs-lookup"><span data-stu-id="77b6c-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="77b6c-111">PreOperationContractLineDetailUpdate – värskendused **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="77b6c-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="77b6c-112">PreOperationQuoteLineDetailUpdate – värskendused **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="77b6c-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="77b6c-113">Järgmised etapid selgitavad teile lisandmoodulite registreerimise protsessi.</span><span class="sxs-lookup"><span data-stu-id="77b6c-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="77b6c-114">Avage **PluginRegistrationTool** ja looge ühendus oma võrguühendusega eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="77b6c-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="77b6c-115">Klõpsake käsku **Otsi** ja otsige üles lisandmoodul, mida soovite värskendada.</span><span class="sxs-lookup"><span data-stu-id="77b6c-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Otsingupuu kuvatõmmis](media/PRT-1.png)

3. <span data-ttu-id="77b6c-117">Pärast lisandmooduli leidmist valige see ja klõpsake valikut **Vali Põhivormil**.</span><span class="sxs-lookup"><span data-stu-id="77b6c-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="77b6c-118">Valige lisandmooduli etapp, mida soovite värskendada, paremklõpsake seda ja valige seejärel käsk **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="77b6c-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Kuvatõmmis värskendatavast lisandmoodulist](media/PRT-2.png)
 
5. <span data-ttu-id="77b6c-120">Klõpsake värskendamise aknas filtreerimise atribuutides kolmikpunkti (**...**).</span><span class="sxs-lookup"><span data-stu-id="77b6c-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Kuvatõmmis olemasoleva etapi värskendamise konfiguratsiooniteabest](media/PRT-3.png)
 
6. <span data-ttu-id="77b6c-122">Valige hinnakujunduse atribuudi märkeruudud.</span><span class="sxs-lookup"><span data-stu-id="77b6c-122">Select the pricing attribute check boxes.</span></span>

 ![Kuvatõmmis, kus on näha hinnakujunduse atribuutide märkeruutude valikut](media/PRT-4.png)

7. <span data-ttu-id="77b6c-124">Lehe sulgemiseks klõpsake nuppu **OK** ja seejärel käsku **Värskenda etappi**.</span><span class="sxs-lookup"><span data-stu-id="77b6c-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Kuvatõmmis, kus on näha nuppu „Värskenda etappi”](media/PRT-5.png)
 
8. <span data-ttu-id="77b6c-126">Korrake seda protsessi ka teise lisandmooduli puhul, **PreOperationQuoteLineDetail – msdyn_quotelinetransaction-i värskendamine**.</span><span class="sxs-lookup"><span data-stu-id="77b6c-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="77b6c-127">Sulgege lisandmooduli registreerimistööriist.</span><span class="sxs-lookup"><span data-stu-id="77b6c-127">Close the plug-in registration tool.</span></span>

