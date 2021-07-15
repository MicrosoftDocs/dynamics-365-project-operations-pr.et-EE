---
title: Project Operationsi registreerumine eelvaate kordustellimusele ressursside/mitte laosolevate stsenaariumite jaoks
description: Selles teemas antakse teavet Project Operationsi tellimise ja juurutamise kohta ressursi-/mitte laosolevate stsenaariumite jaoks.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334822"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="6eb19-103">Project Operationsi registreerumine eelvaate kordustellimusele ressursside/mitte laosolevate stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="6eb19-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="6eb19-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="6eb19-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6eb19-105">Selles teemas kirjeldatakse, kuidas tellida prooviversiooni ja juurutada Project Operationsi keskkonda ressursipõhistes/mittelaopõhistes stsenaariumides.</span><span class="sxs-lookup"><span data-stu-id="6eb19-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6eb19-106">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="6eb19-106">Prerequisites</span></span>
- <span data-ttu-id="6eb19-107">Kasutajal, kes eelvaate juurutab, peab olema Azure'i rentniku globaalse administraatori õigused.</span><span class="sxs-lookup"><span data-stu-id="6eb19-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="6eb19-108">Rentniku saate luua esimese pakkumise lunastamise ajal.</span><span class="sxs-lookup"><span data-stu-id="6eb19-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="6eb19-109">Finance'i keskkonna juurutamiseks on vaja kehtivat Azure'i tellimust, mida arveldatakse keskkonna põhiselt.</span><span class="sxs-lookup"><span data-stu-id="6eb19-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="6eb19-110">Alustamiseks võite kasutada oma organisatsiooni olemasolevat kordustellimust või kasutada [Azure'i prooviversiooni](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="6eb19-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="6eb19-111">CDS-i keskkonda pakutakse piiratud 30-päevase perioodi jooksul tasuta.</span><span class="sxs-lookup"><span data-stu-id="6eb19-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6eb19-112">Selle toimingu peab organisatsioonis tegema ainult üks inimene, rentniku administraator.</span><span class="sxs-lookup"><span data-stu-id="6eb19-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="6eb19-113">Kui te pole selle väljalaske tellija, oodake, kuni teie organisatsioon on registreeritud ja teile on saadetud kasutaja mandaat.</span><span class="sxs-lookup"><span data-stu-id="6eb19-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="6eb19-114">Prooviversioonid on rentnikus ühekordselt kasutatav.</span><span class="sxs-lookup"><span data-stu-id="6eb19-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="6eb19-115">Prooviversiooni saab käitada ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="6eb19-115">You can only run a trial one time.</span></span> <span data-ttu-id="6eb19-116">Soovitame teil luua prooviversiooni eesmärgil uus rentnik.</span><span class="sxs-lookup"><span data-stu-id="6eb19-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="6eb19-117">Dynamics 365 Project Operations (CE) – eelversiooni prooviversioon</span><span class="sxs-lookup"><span data-stu-id="6eb19-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="6eb19-118">Enne alustamist veenduge, et oleksite brauseris sisse logitud kasutaja töökontoga rentnikusse, kus soovite Project Operationsi eelvaadet näha.</span><span class="sxs-lookup"><span data-stu-id="6eb19-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="6eb19-119">Lunastage esimene pakkumise kood **Dynamics 365 Project Operations** siin [Project Operationsi prooviversioon](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="6eb19-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="6eb19-120">Kinnitage oma tellimus.</span><span class="sxs-lookup"><span data-stu-id="6eb19-120">Confirm your order.</span></span>

  <span data-ttu-id="6eb19-121">Näete, et kinnituse pakkumine on edukalt lunastatud.</span><span class="sxs-lookup"><span data-stu-id="6eb19-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="6eb19-122">Dynamics 365 Finance'i eelversiooni prooviversioon</span><span class="sxs-lookup"><span data-stu-id="6eb19-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="6eb19-123">Minge jaotisse [Dynamics 365 for Finance eelversiooni prooviversioon](https://aka.ms/trypoche) ja korrake pakkumisega eelmise jaotise juhiseid, registreeruge pilvmajutusega keskkondade jaoks.</span><span class="sxs-lookup"><span data-stu-id="6eb19-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="6eb19-124">Litsentside määramine</span><span class="sxs-lookup"><span data-stu-id="6eb19-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6eb19-125">Järgmiste toimingute lõpuleviimiseks on teil vaja oma organisatsiooni Microsoft 365 portaali administraatori juurdepääsu.</span><span class="sxs-lookup"><span data-stu-id="6eb19-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="6eb19-126">Oma kasutajatele litsentside määramiseks avage [Microsofti 365 halduskeskus](https://portal.office.com/).</span><span class="sxs-lookup"><span data-stu-id="6eb19-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="6eb19-127">Valige lehel **Aktiivsed kasutajad** need kasutajad, kellele soovite litsentsi määrata.</span><span class="sxs-lookup"><span data-stu-id="6eb19-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="6eb19-128">Kontrollige, kas litsents **Dynamics 365 Project Operations** on valitud, ja valige käsk **Salvesta muudatused**.</span><span class="sxs-lookup"><span data-stu-id="6eb19-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="6eb19-129">Finance'i prooviversiooni pakkumist ei pea kasutajale määrama.</span><span class="sxs-lookup"><span data-stu-id="6eb19-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="6eb19-130">LCS-is uue projekti alustamine</span><span class="sxs-lookup"><span data-stu-id="6eb19-130">Start a new project in LCS</span></span>

<span data-ttu-id="6eb19-131">Looge uus LCS-i projekt, nagu kirjeldatud teemas [LCS-is uue projekti alustamine](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="6eb19-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="6eb19-132">Azure’i kordustellimuse lisamine LCS-i projektile</span><span class="sxs-lookup"><span data-stu-id="6eb19-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="6eb19-133">Selle toimingu lõpuleviimiseks järgige juhiseid teemas [Azure'i tellimuse lisamine LCS-i projektile](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="6eb19-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="6eb19-134">Finance'i demokeskkonna juurutamine Project Operationsiga ressursi/mitte laosoleva stsenaariumide jaoks</span><span class="sxs-lookup"><span data-stu-id="6eb19-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="6eb19-135">Juurutuse lõpuleviimiseks järgige juhiseid teemas [Uue keskkonna ettevalmistamine](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="6eb19-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="6eb19-136">Kasutage eelversiooni korral [demokeskkonna](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) juurutuse tüüpi.</span><span class="sxs-lookup"><span data-stu-id="6eb19-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="6eb19-137">CDS-i seadistuse ja konfiguratsiooniandmete installimine</span><span class="sxs-lookup"><span data-stu-id="6eb19-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="6eb19-138">Installige teemas kirjeldatud CDS-i seadistuse ja konfiguratsiooni andmed, [Seadistage ja rakendage konfiguratsiooni andmeid rakenduses Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="6eb19-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="6eb19-139">Viige see etapp lõpule alles pärast teenuse Finance juurutamist ja kui demoandmed on valmis.</span><span class="sxs-lookup"><span data-stu-id="6eb19-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
