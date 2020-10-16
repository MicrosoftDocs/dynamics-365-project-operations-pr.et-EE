---
title: Päevarahad
description: Selles teemas antakse teavet kuluhalduses kasutatavate päevarahade reeglite kohta.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908058"
---
# <a name="per-diems"></a><span data-ttu-id="b1d14-103">Päevarahad</span><span class="sxs-lookup"><span data-stu-id="b1d14-103">Per diems</span></span>

<span data-ttu-id="b1d14-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="b1d14-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="b1d14-105">Päevaraha on hüvitis, mida makstakse töötajale, kes töö tõttu reisib.</span><span class="sxs-lookup"><span data-stu-id="b1d14-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="b1d14-106">Kuluhalduses saate erinevate reisi olukordade jaoks luua päevaraha.</span><span class="sxs-lookup"><span data-stu-id="b1d14-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="b1d14-107">Päevarahade määrad võivad põhineda aastaajal, reisisihtkohal või mõlemal.</span><span class="sxs-lookup"><span data-stu-id="b1d14-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="b1d14-108">Päevarahade reegli loomisel saate määrata, et teatud protsent päevarahade hinnast jäetakse maksmata, kui töötaja saab tasuta einet või teenust.</span><span class="sxs-lookup"><span data-stu-id="b1d14-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="b1d14-109">Samuti saate määrata minimaalse ja maksimaalse tundide arvu, mille võrra päevaraha töötaja reisile rakendada saab.</span><span class="sxs-lookup"><span data-stu-id="b1d14-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="b1d14-110">Konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="b1d14-110">Configuration</span></span> 

1. <span data-ttu-id="b1d14-111">Päevarahade sihtkohtade lisamiseks minge jaotisse **Seadistus** > **Arvutused ja koodid** > **Päevarahade sihtkohad**.</span><span class="sxs-lookup"><span data-stu-id="b1d14-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="b1d14-112">Valige iga ülaltoodud asukoha kohta päevarahade määr ja valuuta, mis kehtib hotelli, toitlustuse ja muude kulude tarbeks kindla algus-ja lõppkuupäeva vahel.</span><span class="sxs-lookup"><span data-stu-id="b1d14-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="b1d14-113">Päevarahade määrad ja valuutad konfigureeritakse jaotises **Seadistus** > **Arvutused ja koodid** > **Päevarahad**.</span><span class="sxs-lookup"><span data-stu-id="b1d14-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="b1d14-114">Konfigureerige lehel **Päevarahade sihtkohad** päevarahade määra tasemed.</span><span class="sxs-lookup"><span data-stu-id="b1d14-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="b1d14-115">Päevarahade määra tasemed võimaldavad teil määratleda hotelli-, eine- ja muude kulude päevaraha jagamise protsendi.</span><span class="sxs-lookup"><span data-stu-id="b1d14-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="b1d14-116">Hommikusöögi, lõunasöögi või õhtusöögi jaoks söögikorra protsentuaalse vähendamise määramiseks värskendage lehe **Kuluhalduse parameetrid** vahekaardi **Päevarahad** välju.</span><span class="sxs-lookup"><span data-stu-id="b1d14-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="b1d14-117">Kulude esitamine päevarahade abil</span><span class="sxs-lookup"><span data-stu-id="b1d14-117">Submit expenses using per diem</span></span>
<span data-ttu-id="b1d14-118">Päevarahade kasutamiseks kulude esitamiseks kasutage kuluaruande loomisel kulukategooriat **Päevarahad**.</span><span class="sxs-lookup"><span data-stu-id="b1d14-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="b1d14-119">Sisestage **Päevarahad alates kuupäevast**, **Päevarahad kuupäevani** ja **Päevarahade sihtkoht**.</span><span class="sxs-lookup"><span data-stu-id="b1d14-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="b1d14-120">Summa arvutatakse vastavalt päevarahade määradele valitud asukoha jaoks ja eine vähendamine arvutatakse päevaraha määrade tasemete põhjal.</span><span class="sxs-lookup"><span data-stu-id="b1d14-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
