---
title: Lisandmooduli atribuutide värskendamine uute hinnakujunduse dimensioonidega
description: Selles teemas kirjeldatakse, kuidas värskendada hinnakujunduse dimensioonide jaoks lisandmooduli atribuute.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 54b87a993929edbf89ef48741ba0a06c6c42ec4e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004616"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="20bd0-103">Lisandmooduli atribuutide värskendamine uute hinnakujunduse dimensioonidega</span><span class="sxs-lookup"><span data-stu-id="20bd0-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="20bd0-104">Selles teemas kirjeldatakse, kuidas värskendada hinnakujunduse dimensioonide jaoks lisandmooduli atribuute.</span><span class="sxs-lookup"><span data-stu-id="20bd0-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="20bd0-105">See teema kehtib ainult rakenduse Dynamics 365 Project Operations hinnapakkumise ja lepingu funktsioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="20bd0-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="20bd0-106">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="20bd0-106">Prerequisites</span></span>
<span data-ttu-id="20bd0-107">Enne selles teemas toodud juhiste täitmist peate viima lõpule toimingud järgmistes teemades.</span><span class="sxs-lookup"><span data-stu-id="20bd0-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="20bd0-108">Kohandatud väljade ja olemite loomine</span><span class="sxs-lookup"><span data-stu-id="20bd0-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="20bd0-109">Kohandatud väljade lisamine hinna seadistusele ja ülekande olemitele </span><span class="sxs-lookup"><span data-stu-id="20bd0-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="20bd0-110">[Kohandatud väljade seadistamine hinnakujunduse dimensioonidena](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="20bd0-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="20bd0-111">Kui te pole neid toiminguid lõpetanud, viige need lõpuni ja seejärel tulge selle teema juurde tagasi.</span><span class="sxs-lookup"><span data-stu-id="20bd0-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="20bd0-112">Lisandmooduli registreerimine</span><span class="sxs-lookup"><span data-stu-id="20bd0-112">Register a plug-in</span></span>
<span data-ttu-id="20bd0-113">Kui projekti hinnapakkumise rea jaoks luuakse lehel **Hinnapakkumise rida** hinnapakkumise rea üksikasi, loob süsteem kaks hinnangu rida.</span><span class="sxs-lookup"><span data-stu-id="20bd0-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="20bd0-114">Üks rida on hinnangu kulupoole jaoks ja teine rida on müügipoole jaoks.</span><span class="sxs-lookup"><span data-stu-id="20bd0-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="20bd0-115">Sama kehtib ka projekti lepinguridade kohta.</span><span class="sxs-lookup"><span data-stu-id="20bd0-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="20bd0-116">Kui muudate kulupoole kogust või välja, tehase see muudatus ka müügipoolel.</span><span class="sxs-lookup"><span data-stu-id="20bd0-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="20bd0-117">See on võimalik, kuna atribuudi Quotelinedetail lisnadmoodulid PreOperation ja lepingurea üksikasja olemis ühendavad kulupoole kindlad atribuudid tehingu müügipoolega.</span><span class="sxs-lookup"><span data-stu-id="20bd0-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="20bd0-118">Kui soovite, et müügipoole hinnakujunduse dimensiooni väärtustele tehtavad muudatused tehtaks ka kulupoolel, tuleb pärast hinnakujunduse dimensioonile muudatuste tegemist registreerida uuesti järgmised lisandmoodulid.</span><span class="sxs-lookup"><span data-stu-id="20bd0-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="20bd0-119">Järgmised lisandmoodulid tuleb värskendada ja uuesti registreerida.</span><span class="sxs-lookup"><span data-stu-id="20bd0-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="20bd0-120">PreOperationContractLineDetailUpdate – **värskendab üksuse msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="20bd0-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="20bd0-121">PreOperationQuoteLineDetailUpdate - **värskendab üksuse msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="20bd0-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="20bd0-122">Lisandmoodulite värskendamiseks ja uuesti registreerimiseks peate tegema järgmist.</span><span class="sxs-lookup"><span data-stu-id="20bd0-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="20bd0-123">Avage **PluginRegistrationTool** ja ühendage oma Project Operationsi teenuse Dataverse keskkond.</span><span class="sxs-lookup"><span data-stu-id="20bd0-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="20bd0-124">Valige **Otsing** ja sisendage värskendatava lisandmooduli esimesed tähed.</span><span class="sxs-lookup"><span data-stu-id="20bd0-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="20bd0-125">Pärast lisandmooduli leidmist valige see ja valige seejärel suvand **Vali Põhivormil**.</span><span class="sxs-lookup"><span data-stu-id="20bd0-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="20bd0-126">Valige etapp **Üksuse msdyn_orderlinetransaction värskendamine**, tehke paremklõps ja valige seejärel **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="20bd0-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="20bd0-127">Dialoogilehel **Värskendus** valige filtreerimise atribuutides kolmikpunkt (**...**).</span><span class="sxs-lookup"><span data-stu-id="20bd0-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="20bd0-128">Avaneb filtreerimise atribuutide aken ja kuvab loendi kõikidest olemi atribuutidest ja hinnakujunduse dimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="20bd0-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="20bd0-129">Märkige hinnakujunduse dimensiooni atribuutide märkeruudud.</span><span class="sxs-lookup"><span data-stu-id="20bd0-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="20bd0-130">Lehe sulgemiseks valige **OK** ja valige seejärel käsk **Värskenda etappi**.</span><span class="sxs-lookup"><span data-stu-id="20bd0-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="20bd0-131">Korrake etappe 2–7 teise lisandmooduli **PreOperationQuoteLineDetail** jaoks.</span><span class="sxs-lookup"><span data-stu-id="20bd0-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="20bd0-132">Selle lisandmooduli jaoks peate värskendama etappi **Üksuse msdyn_quotelinetransaction värskendamine**.</span><span class="sxs-lookup"><span data-stu-id="20bd0-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="20bd0-133">Sulgege tööriist **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="20bd0-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]