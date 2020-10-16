---
title: Azure’i kordustellimuse lisamine LCS-projektile
description: See teema pakub teavet selle kohta, kuidas Azure'i tellimust LCS-i projektiga ühendada.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948831"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a><span data-ttu-id="110ec-103">Azure’i kordustellimuse lisamine LCS-projektile</span><span class="sxs-lookup"><span data-stu-id="110ec-103">Add an Azure subscription to LCS project</span></span>

<span data-ttu-id="110ec-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="110ec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="110ec-105">Pilvepõhiseid keskkondi tuleb juurutada kasutades olemasolevat Azure'i korduvtellimust.</span><span class="sxs-lookup"><span data-stu-id="110ec-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="110ec-106">See teema selgitab, kuidas olemasolevat Azure'i tellimust LCS-i projektiga ühendada.</span><span class="sxs-lookup"><span data-stu-id="110ec-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="110ec-107">Administraatori nõusoleku andmine</span><span class="sxs-lookup"><span data-stu-id="110ec-107">Grant admin consent</span></span>

1. <span data-ttu-id="110ec-108">Valige LCS projekti jaotises **Keskkonnad** suvand **Microsoft Azure'i sätted**.</span><span class="sxs-lookup"><span data-stu-id="110ec-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Microsoft Azurei Seaded](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="110ec-110">Valige lehel **Projekti sätted** vahekaardil **Azure'i konnektorid** suvand **Autoriseeri**.</span><span class="sxs-lookup"><span data-stu-id="110ec-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="110ec-111">See võimaldab sellele projektile keskkondade juurutamist.</span><span class="sxs-lookup"><span data-stu-id="110ec-111">This allows environments to be deployed to this project.</span></span>

![Azure'i konnektorid](./media/2AzureConnectors.png)

3. <span data-ttu-id="110ec-113">Administraatori nõusoleku andmiseks valige uuesti käsk **Autoriseeri**.</span><span class="sxs-lookup"><span data-stu-id="110ec-113">Select **Authorize** again to provide admin consent.</span></span>

![Administraatori nõusoleku andmine](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="110ec-115">Aktsepteerige õiguste taotlus.</span><span class="sxs-lookup"><span data-stu-id="110ec-115">Accept the permissions request.</span></span>

![Aktsepteerige õiguste taotlus](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="110ec-117">Autoriseerimine on nüüd lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="110ec-117">The authorization is now complete.</span></span> 

![Autoriseerimine oli edukas](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="110ec-119">Dynamicsi juurutamisteenustele oma Azure'i tellimuse juurdepääsu andmine</span><span class="sxs-lookup"><span data-stu-id="110ec-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="110ec-120">Avage [Microsoft Azure'i arveldus](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) ja valige oma kordustellimus.</span><span class="sxs-lookup"><span data-stu-id="110ec-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="110ec-121">Dynamicsi juurutamisteenused vajavad keskkondade juurutamiseks juurdepääsu sellele tellimusele.</span><span class="sxs-lookup"><span data-stu-id="110ec-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Azure'i tellimuse üksikasjad](./media/6AzureSubscription.png)

2. <span data-ttu-id="110ec-123">Valige navigeerimispaanil **Juurdepääsukontroll** ja seejärel valige **Rollimäärangu lisamine**.</span><span class="sxs-lookup"><span data-stu-id="110ec-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="110ec-124">Valige paremas servas asuvas liuguris **Kaasautori roll** ja leidke ning valige antud loendis jaotis **Dynamicsi juurutamisteenused**.</span><span class="sxs-lookup"><span data-stu-id="110ec-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="110ec-125">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="110ec-125">Select **Save**.</span></span>

![Tellimuse juurdepääs](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="110ec-127">LCS-i projektile tellimuse konnektori lisamine</span><span class="sxs-lookup"><span data-stu-id="110ec-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="110ec-128">Valige oma LCS-i projektis lehel **Microsoft Azure'i sätted** uue konnektori lisamiseks käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="110ec-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="110ec-129">Sisestage oma Azure'i kordustellimuse ID.</span><span class="sxs-lookup"><span data-stu-id="110ec-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="110ec-130">Oma Azure'i kordustellimuse ID leiate [Azure'i portaalis](https://ms.portal.azure.com/) ekraani alumisest vasakult nurgast jaotisest  **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="110ec-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="110ec-131">Valige väljal **Konfigureeri Azure'i ressursihalduri kasutamiseks** suvand **Jah**.</span><span class="sxs-lookup"><span data-stu-id="110ec-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="110ec-132">Veenduge, et Azure'i kordustellimuse AAD rentniku domeen ühtib kasutatava Azure'i tellimust omava domeeniga ja valige **edasi**.</span><span class="sxs-lookup"><span data-stu-id="110ec-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="110ec-133">Valige kuval **Microsoft Azure'i seadistus** kinnitamiseks käsk **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="110ec-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="110ec-134">Kui kuvatakse sellel kuval tõrge, pöörduge tagasi selle teema jaotisse [Dynamicsi juurutamisteenustele Azure'i tellimuse juurdepääsu andmine](#provide) ja veenduge, et olete kõik sammud lõpule viinud.</span><span class="sxs-lookup"><span data-stu-id="110ec-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="110ec-135">Laadige Azure'i haldussertifikaat oma arvuti kohalikku kausta ja laadige see Azure'i haldusportaali üles, minnes jaotisse **Sätted** > **Haldussertifikaadid**.</span><span class="sxs-lookup"><span data-stu-id="110ec-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="110ec-136">See sert võimaldab LCS-il teie eest Azure'iga suhelda.</span><span class="sxs-lookup"><span data-stu-id="110ec-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="110ec-137">Kui teie kasutajal on tellimusele juurdepääs, võite selle etapi vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="110ec-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="110ec-138">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="110ec-138">Select  **Next**.</span></span>
8. <span data-ttu-id="110ec-139">Valige juurutamiseks Azure'i piirkond ja valige andmekeskus, mis on lähedal sellele, kus kavatsete seda süsteemi kasutada.</span><span class="sxs-lookup"><span data-stu-id="110ec-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="110ec-140">Valige käsk **Ühenda**.</span><span class="sxs-lookup"><span data-stu-id="110ec-140">Select  **Connect**.</span></span>

<span data-ttu-id="110ec-141">Olete Azure'i kordustellimuse edukalt ühendanud.</span><span class="sxs-lookup"><span data-stu-id="110ec-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="110ec-142">Nüüd saate juurutada Dynamics 365 Finance'i pilvepõhiseid keskkondi.</span><span class="sxs-lookup"><span data-stu-id="110ec-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>


