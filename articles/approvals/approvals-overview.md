---
title: Kinnituste ülevaade
description: Selles teemas kirjeldatakse tööd, mis on seotud rakenduse Project Operations kinnitustega.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961161"
---
# <a name="approvals-overview"></a><span data-ttu-id="4944d-103">Kinnituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="4944d-103">Approvals overview</span></span>

<span data-ttu-id="4944d-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="4944d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4944d-105">Aja ja kulu esitamised liiguvad läbi kinnitamise töövoo.</span><span class="sxs-lookup"><span data-stu-id="4944d-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="4944d-106">Pärast kirjete kinnitamist kirjendatakse tehingud tegelikes näitajates või ajakavas broneeritakse aeg.</span><span class="sxs-lookup"><span data-stu-id="4944d-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="4944d-107">Kinnituste töövoog</span><span class="sxs-lookup"><span data-stu-id="4944d-107">Approvals workflow</span></span>
<span data-ttu-id="4944d-108">Kui te loote ja esitate aja- või kulukirje, luuakse kinnitamise kirje.</span><span class="sxs-lookup"><span data-stu-id="4944d-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="4944d-109">Projekti kinnitaja või teie juht vaatab teie kirje läbi ja kinnitab selle.</span><span class="sxs-lookup"><span data-stu-id="4944d-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="4944d-110">Kui kirje on seotud projektiga, siis selle kinnitamisel luuakse tegelikud näitajad.</span><span class="sxs-lookup"><span data-stu-id="4944d-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="4944d-111">See võimaldab kulu ja arvelduse jälgimist.</span><span class="sxs-lookup"><span data-stu-id="4944d-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="4944d-112">Kirje kinnitamine</span><span class="sxs-lookup"><span data-stu-id="4944d-112">Approve an entry</span></span>
<span data-ttu-id="4944d-113">Vorm **Kinnitamised** võimaldab teil vahetada erinevate vaadete vahel, et saaksite vaadata erinevat tüüpi kinnitusi.</span><span class="sxs-lookup"><span data-stu-id="4944d-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="4944d-114">Avage vorm **Kinnitused** ja valige suvand **Kulud**, **Aeg** või **Tagasikutsumised**.</span><span class="sxs-lookup"><span data-stu-id="4944d-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="4944d-115">Vaadake kõik kinnitamised läbi ja valige need, mida soovite kinnitada.</span><span class="sxs-lookup"><span data-stu-id="4944d-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="4944d-116">Valitud kirjete kinnitamiseks valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="4944d-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="4944d-117">Süsteem töötleb neid kirjeid ja loob tegelikud näitajad või broneeringu.</span><span class="sxs-lookup"><span data-stu-id="4944d-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="4944d-118">Kirje tagasi lükkamine</span><span class="sxs-lookup"><span data-stu-id="4944d-118">Reject an entry</span></span>
<span data-ttu-id="4944d-119">Projekti kinnitajana võib juhtuda, et peate saatma kirje kasutajale parandamiseks tagasi.</span><span class="sxs-lookup"><span data-stu-id="4944d-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="4944d-120">Avage vorm **Kinnitused** ja valige tagasi lükkamiseks kirje.</span><span class="sxs-lookup"><span data-stu-id="4944d-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="4944d-121">Valige **Keeldu**.</span><span class="sxs-lookup"><span data-stu-id="4944d-121">Select **Reject**.</span></span>
3. <span data-ttu-id="4944d-122">Valikuline – lisage dialoogi **Tagasilükkamise kommentaarid** kommentaar, et teavitada kasutajat kirje tagasi lükkamise põhjusest.</span><span class="sxs-lookup"><span data-stu-id="4944d-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="4944d-123">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="4944d-123">Select **OK**.</span></span> <span data-ttu-id="4944d-124">Kirje tagastatakse kasutajale.</span><span class="sxs-lookup"><span data-stu-id="4944d-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="4944d-125">Kirjete tagasivõtmine</span><span class="sxs-lookup"><span data-stu-id="4944d-125">Recall entries</span></span>
<span data-ttu-id="4944d-126">Mingi hetk võib teil olla vaja esitatud kirje tagasi kutsuda.</span><span class="sxs-lookup"><span data-stu-id="4944d-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="4944d-127">Kui kirjet pole kinnitatud, siis tagastatakse see kohe.</span><span class="sxs-lookup"><span data-stu-id="4944d-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="4944d-128">Kinnitatud kirjel võib samas olla materjaalne mõju.</span><span class="sxs-lookup"><span data-stu-id="4944d-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="4944d-129">Projekti kinnitaja peab tagasikutsumise heaks kiitma, et tagastada tehing suvandisse Tegelikud näitajad.</span><span class="sxs-lookup"><span data-stu-id="4944d-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="4944d-130">Projekti kinnitajate määratlemine</span><span class="sxs-lookup"><span data-stu-id="4944d-130">Specify Project approvers</span></span>
<span data-ttu-id="4944d-131">Igal projektil on mitu projekti meeskonnaliiget.</span><span class="sxs-lookup"><span data-stu-id="4944d-131">Each project has a number of project team members.</span></span> <span data-ttu-id="4944d-132">Saate määrata, millised meeskonnaliikmed on ka projekti kinnitajad.</span><span class="sxs-lookup"><span data-stu-id="4944d-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="4944d-133">Avage vorm **Projektid** ja avage loendist projekt.</span><span class="sxs-lookup"><span data-stu-id="4944d-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="4944d-134">Valige vahekaardil **Meeskond** meeskonnaliige, kellest saab projekti kinnitaja, ja valige seejärel nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="4944d-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="4944d-135">Määrake väli **Projekti kinnitaja** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="4944d-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="4944d-136">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4944d-136">Select **Save**.</span></span>
5. <span data-ttu-id="4944d-137">Täiendavate projekti kinnitajate lisamiseks korrake samme 2–4.</span><span class="sxs-lookup"><span data-stu-id="4944d-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="4944d-138">Kasutaja juhi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="4944d-138">Configure the user's manager</span></span>

1. <span data-ttu-id="4944d-139">Valige **Sätted** > **Turve** > **Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="4944d-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="4944d-140">Valige kasutaja, kellele määrate juhi rolli, ja valige piirkonnas **Organisatsiooni teave** loendist juht.</span><span class="sxs-lookup"><span data-stu-id="4944d-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="4944d-141">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4944d-141">Select **Save**.</span></span>


