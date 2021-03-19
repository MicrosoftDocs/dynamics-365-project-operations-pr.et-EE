---
title: Projekti ressursiplaanimise jõudlus
description: Selles teemas kirjeldatakse suure hulga projektide jaoks ressursside kavandamise jõudluse parandamist.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289004"
---
# <a name="project-resource-scheduling-performance"></a>Projekti ressursiplaanimise jõudlus

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Ressursside kavandamisega seotud jõudluse probleemid võib ilmneda juhul, kui projektide arv ulatub üle tuhandete. Ressursi ajastamise jõudluse parendamiseks on saadaval funktsioon, mis võimaldab kasutajatel vähendada ressursi kättesaadavuse vormi käivitamiseks kuluvat aega. Täpsemalt, see eemaldab ressursi võimsuse ümberarvestuse sünkroonimise protsessi ja kasutab tabelit **ResProjectResource** ressursi otsingu kiirendamiseks. Pange tähele, et tabelit **ResRollup** enam ei kasutata.

> [!IMPORTANT]
> Kui ressursi võimsuse ümberarvestuse sünkroonimise protsessil või tabelil **ResProjectResource** on sõltuvus, ärge seda funktsiooni kasutage.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Ressursi kavandamise jõudluse suurendamise lubamine
Ressursi ajastamise jõudluse suurendamise lubamiseks läbige järgmised etapid.

1. Minge jaotisse **Funktsioonidhaldus** > **Kõik** ja leidke funktsioonide loendist suvand **Luba projekti ressursi kavandamise jõudluse suurendamise funktsioon**.
2. Valige **Luba kohe**.

> [!NOTE]
> Kui te ei leia loendist funktsiooni, valige loendi värskendamiseks käsk **Otsi värskendusi**.

3. Värskendage oma brauserit ja seejärel minge jaotisse **Projektijuhtimine ja raamatupidamine** > **Perioodiline** > **Projekti ressursid** > **Sünkrooni ressursi kalendrite mahutavus kõigis ettevõtetes**.
4. Määrake eelnevate andmete eemaldamiseks suvand **Olemasolevate mahutavuse kirjete eemaldamine** olekusse **Jah**. Kui soovite luua täiendavaid andmeid, määrake see väärtusele **Ei**.
5. Valige väljal **Perioodi kood** ajavahemik, mille jooksul tuleks andmed luua. Kui valite perioodi koodi, ei pea algus-ja lõppkuupäeva määratlema.
6. Kui jätate välja **Perioodi kood** tühjaks, valige andmete loomiseks konkreetsed algus-ja lõppkuupäevad.
7. Valige **OK**.

 > [!NOTE]
 > See jaotab üldandmed tabelisse **ResCalendarCapacity** kõigile teie keskkonna ettevõtetele, nii et pakett-töö tuleb käivitada ainult ühes juriidilises isikus. Selle pakett-töö andmeid on vaja ressursi võimsuse arvutamiseks seostatud kalendri kaudu.

8. Minge jaotisse **Projektijuhtimine ja raamatupidamine** > **Perioodiline** > **Projekti ressursid** > **Täida projekti ressursid kõigis ettevõtetes** ja seejärel valige **OK**. See on tabelite **ResProjectResource**, **ResCalendarDateTimeRange** ja **ResEffectiveDateTimeRange** üldandmete andmevärskenduste skript. Värskendatakse ka väärtusi väljadel **PSAPRojSchedRole.RootActivity**. Kui seda ei käivitata, kuvatakse teile hoiatus, kui proovite käivitada ressursside kavandamise toiminguid.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Ressursi kavandamise jõudluse suurendamise väljalülitamine

1. Avage jaotis **Funktsioonidhaldus** > **Kõik** ja leidke suvand **Luba projekti ressursi kavandamise jõudluse suurendamise funktsioon**.
2. Valige funktsioon ja seejärel valige nupp **Keela**.
3. Värskendage oma brauser.
4. Avage jaotis **Projektijuhtimine ja raamatupidamine** > **Perioodiline** > **Võimsuse sünkroonimine** > **Ressursi võimsuse sünkroonimise ümberarvestused**.
5. Määrake eelmiste andmete eemaldamiseks lehel **Võimsuse ümberarvestuse sünkroonimine** suvand **Olemasolevate võimsuse kirjete eemaldamine** olekusse **Jah**. Kui soovite luua täiendavaid andmeid, määrake see väärtusele **Ei**.
6. Valige väljal **Perioodi kood** ajavahemik, mille jooksul tuleks andmed luua. Kui valite perioodi koodi, ei pea algus-ja lõppkuupäeva määratlema.
7. Kui jätate välja **Perioodi kood** tühjaks, valige andmete loomiseks konkreetsed algus-ja lõppkuupäevad.
8. Valige **OK**.

> [!NOTE]
> See jaotab üldandmed tabelisse **ResRollup** kõigile teie keskkonna ettevõtetele, nii et pakett-töö tuleb käivitada ainult ühes juriidilises isikus. Seda pakett-tööd on vaja kõigi **Ressursi saadavuse** vaadete jaoks. Kui seda pakett-tööd ei käivitata, siis andmed **ResRollup** luuakse lennult, mis võib võtta aega.


[!INCLUDE[footer-include](../includes/footer-banner.md)]