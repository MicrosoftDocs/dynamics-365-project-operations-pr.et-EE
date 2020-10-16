---
title: Project Operationsi registreerumine eelvaate kordustellimusele ressursside/mitte laosolevate stsenaariumite jaoks
description: Selles teemas antakse teavet Project Operationsi tellimise ja juurutamise kohta ressursi-/mitte laosolevate stsenaariumite jaoks.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948832"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="eee82-103">Project Operationsi registreerumine eelvaate kordustellimusele ressursside/mitte laosolevate stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="eee82-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="eee82-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="eee82-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="eee82-105">Selles teemas selgitatakse, kuidas tellida eelvaadet/partneri pakkumist ja juurutada Project Operationsi keskkonda ressursi/mitte laosoleva põhiste stsenaariumide jaoks.</span><span class="sxs-lookup"><span data-stu-id="eee82-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eee82-106">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="eee82-106">Prerequisites</span></span>

- <span data-ttu-id="eee82-107">Teile saadetakse meil, mis kutsub teid eelvaates osalema.</span><span class="sxs-lookup"><span data-stu-id="eee82-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="eee82-108">Eelvaadet saate taotleda [Project Operationsi veebisaidilt](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="eee82-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="eee82-109">Kasutajal, kes eelvaate juurutab, peab olema Azure'i rentniku globaalse administraatori õigused.</span><span class="sxs-lookup"><span data-stu-id="eee82-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="eee82-110">Finance'i keskkonna juurutamiseks on vaja kehtivat Azure'i tellimust, mida arveldatakse keskkonna põhiselt.</span><span class="sxs-lookup"><span data-stu-id="eee82-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="eee82-111">Alustamiseks võite kasutada oma organisatsiooni olemasolevat kordustellimust või kasutada [Azure'i prooviversiooni](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="eee82-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="eee82-112">CDS-i keskkonda pakutakse piiratud 30-päevase perioodi jooksul tasuta.</span><span class="sxs-lookup"><span data-stu-id="eee82-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="eee82-113">Telli</span><span class="sxs-lookup"><span data-stu-id="eee82-113">Subscribe</span></span>

<span data-ttu-id="eee82-114">Kui teie [eelvaate taotlus](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) kinnitatakse, saadab Microsoft teile maili teel kaks pakkumist.</span><span class="sxs-lookup"><span data-stu-id="eee82-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="eee82-115">Need pakkumised võimaldavad teil juurutada Project Operationsi eelvaate.</span><span class="sxs-lookup"><span data-stu-id="eee82-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="eee82-116">Dynamics 365 Project Operations - Eelversiooni prooviversioon</span><span class="sxs-lookup"><span data-stu-id="eee82-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="eee82-117">Dynamics 365 for Finance and Operationsi eelversiooni prooviversioon.</span><span class="sxs-lookup"><span data-stu-id="eee82-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eee82-118">Selle toimingu peab organisatsioonis tegema ainult üks inimene, rentniku administraator.</span><span class="sxs-lookup"><span data-stu-id="eee82-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="eee82-119">Kui te pole selle väljalaske tellija, oodake, kuni teie organisatsioon on registreeritud ja teile on saadetud kasutaja mandaat.</span><span class="sxs-lookup"><span data-stu-id="eee82-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="eee82-120">Dynamics 365 Project Operations - Eelversiooni prooviversioon</span><span class="sxs-lookup"><span data-stu-id="eee82-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="eee82-121">Lunastage esimene pakkumine, **Dynamics 365 Project Operationsi prooviversioon**, mille URL on antud teie tervitusmeilis.</span><span class="sxs-lookup"><span data-stu-id="eee82-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Esimene pakkumine](./media/1FirstOffer.png)

2. <span data-ttu-id="eee82-123">Veenduge, et olete sisse logitud kasutajana, kes kuulub organisatsiooni, kes teenust tellib.</span><span class="sxs-lookup"><span data-stu-id="eee82-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="eee82-124">Jätkake pakkumise lunastamisega.</span><span class="sxs-lookup"><span data-stu-id="eee82-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="eee82-125">Valige **Jah, lisage see minu kontole**.</span><span class="sxs-lookup"><span data-stu-id="eee82-125">Select **Yes, add it to my account**.</span></span>

![Lunasta pakkumine](./media/2RedeemFirstOffer.png)

![Kinnita pakkumine](./media/3ConfirmFirstOffer.png)

![Pakkumine lunastatud](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="eee82-129">Dynamics 365 Finance'i eelversiooni prooviversioon</span><span class="sxs-lookup"><span data-stu-id="eee82-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="eee82-130">Korrake samu samme tervitusmeili teise pakkumisega.</span><span class="sxs-lookup"><span data-stu-id="eee82-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="eee82-131">Litsentside määramine</span><span class="sxs-lookup"><span data-stu-id="eee82-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eee82-132">Järgmiste toimingute lõpuleviimiseks on teil vaja oma organisatsiooni Office 365 portaali administraatori juurdepääsu.</span><span class="sxs-lookup"><span data-stu-id="eee82-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="eee82-133">Oma kasutajatele litsentside määramiseks avage [Microsofti 365 halduskeskus](https://portal.office.com/).</span><span class="sxs-lookup"><span data-stu-id="eee82-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Office'i haldusportaal](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="eee82-135">Valige lehel **Aktiivsed kasutajad** need kasutajad, kellele soovite litsentsi määrata.</span><span class="sxs-lookup"><span data-stu-id="eee82-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Litsentside määramine](./media/6AssignLicenses.png)

3. <span data-ttu-id="eee82-137">Kontrollige, kas Project Oprationsi litsents on valitud ja valige **Salvesta muudatused**.</span><span class="sxs-lookup"><span data-stu-id="eee82-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="eee82-138">Finance'i prooviversiooni pakkumist ei pea kasutajale määrama.</span><span class="sxs-lookup"><span data-stu-id="eee82-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="eee82-139">LCS-is uue projekti alustamine</span><span class="sxs-lookup"><span data-stu-id="eee82-139">Start a new project in LCS</span></span>

<span data-ttu-id="eee82-140">Looge uus LCS-i projekt, nagu kirjeldatud teemas [LCS-is uue projekti alustamine](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="eee82-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="eee82-141">Azure’i kordustellimuse lisamine LCS-i projektile</span><span class="sxs-lookup"><span data-stu-id="eee82-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="eee82-142">Selle toimingu lõpuleviimiseks järgige juhiseid teemas [Azure'i tellimuse lisamine LCS-i projektile](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="eee82-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="eee82-143">Finance'i demokeskkonna juurutamine Project Operationsiga ressursi/mitte laosoleva stsenaariumide jaoks</span><span class="sxs-lookup"><span data-stu-id="eee82-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="eee82-144">Juurutuse lõpuleviimiseks järgige juhiseid teemas [Uue keskkonna ettevalmistamine](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="eee82-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="eee82-145">Kasutage eelversiooni korral [demokeskkonna](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) juurutuse tüüpi.</span><span class="sxs-lookup"><span data-stu-id="eee82-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="eee82-146">CDS-i seadistuse ja konfiguratsiooniandmete installimine</span><span class="sxs-lookup"><span data-stu-id="eee82-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="eee82-147">Installige teemas kirjeldatud CDS-i seadistuse ja konfiguratsiooni andmed, [Seadistage ja rakendage konfiguratsiooni andmeid rakenduses Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="eee82-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

