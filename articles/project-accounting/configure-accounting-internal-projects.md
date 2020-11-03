---
title: Sisemiste projektide raamatupidamise konfigureerimine
description: Selles teemas antakse teavet, kuidas seadistada Project Operationsis sisemiste projektide raamatupidamistavasid.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074890"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="aebb0-103">Sisemiste projektide raamatupidamise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="aebb0-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="aebb0-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="aebb0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="aebb0-105">Sisemised projektid lubavad ettevõtetel jälgida kulusid, mis on seotud tegevustega, mille kohta kliendile arvet ei esitata.</span><span class="sxs-lookup"><span data-stu-id="aebb0-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="aebb0-106">Sisemiste projektide näited on järgmised.</span><span class="sxs-lookup"><span data-stu-id="aebb0-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="aebb0-107">Toote, näiteks mobiilirakenduse, arendamine ja arendusega seostatud kulu jälgimine.</span><span class="sxs-lookup"><span data-stu-id="aebb0-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="aebb0-108">Eelmüügi aja ja kulu haldamine.</span><span class="sxs-lookup"><span data-stu-id="aebb0-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="aebb0-109">Selle eelmüügi sisemise projekti saab hiljem, kui hinnapakkumine on võidetud, arveldatavaks projektiks teisendada.</span><span class="sxs-lookup"><span data-stu-id="aebb0-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="aebb0-110">Mis tahes projekti, mis pole seotud Dynamics 365 Project Operationsiga, käsitletakse sisemisena.</span><span class="sxs-lookup"><span data-stu-id="aebb0-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="aebb0-111">Projekti kulu ja tulu profiile ei kasutata projekti raamatupidamise reeglite määramiseks.</span><span class="sxs-lookup"><span data-stu-id="aebb0-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="aebb0-112">Sisemise projekti kulu sisestatakse alati kasumi ja kahjumi põhimõtete abil.</span><span class="sxs-lookup"><span data-stu-id="aebb0-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="aebb0-113">Sisestuste pearaamatu kontod on määratletud lehel **Pearaamatu sisestuste seadistamise**.</span><span class="sxs-lookup"><span data-stu-id="aebb0-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="aebb0-114">Aja tehingud sisestatakse, kui debiteeritakse konto **Kulu** ja krediteeritakse konto **Palgaarvestuse jaotus**.</span><span class="sxs-lookup"><span data-stu-id="aebb0-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="aebb0-115">Kulu tehingud sisestatakse, kui debiteeritakse konto **Kulu** ja krediteeritakse konto **Kulu tasaarvelduskonto**.</span><span class="sxs-lookup"><span data-stu-id="aebb0-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="aebb0-116">Pärast seda, kui tehingud on projekti sisestatud, kui projekt on projekti lepinguga seostatud, tühistab süsteem kõik akumuleeritud tehingud ja loob uued arveldatavad tehingud.</span><span class="sxs-lookup"><span data-stu-id="aebb0-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="aebb0-117">Arveldatavad tehingud järgivad vastava projekti kulu ja tulu profiilis määratletud raamatupidamise reegleid.</span><span class="sxs-lookup"><span data-stu-id="aebb0-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


