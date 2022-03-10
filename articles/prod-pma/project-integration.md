---
title: Microsoft Project Clienti integreerimine
description: Projekti ajakava kavandamine ja haldamine võib olla keeruline, seega peavad projektijuhid kasutama tööriistu, mis aitavad neil seda tööülesannet hallata. Integreerimine rakendusega Microsoft Project Client pakub tuge projekti tööjaotuse struktuuri avamiseks ja haldamiseks.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 8ef34bc984510f23ab77cc1710c06abbcf80f721703685d696fea28eeaddd732
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988016"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project Clienti integreerimine

[!include [banner](../includes/banner.md)]

Projekti ajakava kavandamine ja haldamine võib olla keeruline, seega peavad projektijuhid kasutama tööriistu, mis aitavad neil seda tööülesannet hallata. Integreerimine rakendusega Microsoft Project Client pakub tuge projekti tööjaotuse struktuuri avamiseks ja haldamiseks. Projektijuht saab avaldada kõik muudatused uuesti rakenduse Dynamics 365 Finance projekti tööjaotuse struktuuris.

> [!NOTE]
> Kui kasutate juuli värskendust (versioon 10.0.4), peate installima versioonid KB 4054797 ja 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Lisandmooduli Microsoft Project Client konfigureerimine
Rakendusega Microsoft Project Client integreerimise lubamiseks peab lisandmoodul Microsoft Dynamics 365 olema installitud kasutaja kliendi rakendusse Microsoft Project. Seda saab teha, kui avada **Projektihalduse tööruum**.

•   Klõpsake valikut **Konfigureeri projekti kliendi lisandmoodul** tööruumi jaotises **Lingid** > **Seadistamine**.

•   Klõpsake valikut **Ava**, seejärel klõpsake käsku **Käivita**, kui teilt seda küsitakse.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Olemasoleva mustandi tööjaotuse struktuuri avamine ja redigeerimine Microsoft Project Clientis
Kui projekti jaoks on rakenduses Dynamics 365 Finance tööjaotuse struktuur loodud, saab tööjaotuse struktuuri avada rakenduses Microsoft Project Client, kui tööjaotuse struktuur on mustandi olekus. Lehelt **Projekt** avamiseks klõpsake linki **Ava rakenduses Microsoft Project** vahekaardil **Plaanimine**. Selle lehe saab avada ka rakenduse Microsoft Project Client seest, klõpsates käsku **Ava** vahekaardil **Microsoft Dynamics 365**. Valige loendist **Juriidiline üksus** ja **Projekt**.

> [!NOTE]
> Kui kasutate brauserina Internet Explorerit, peate klõpsama nuppu **Salvesta**, et avada käsitsi kohast, kuhu fail on alla laaditud. Või klõpsake nuppu **Salvesta ja ava**, et avada fail rakenduses Microsoft Project Client. Ärge nimetage faili salvestamise ajal ümber.

Enne failis mis tahes muudatuste tegemist rakendust Microsoft Project Client kasutades peate selle välja registreerima. Klõpsake valikut **Registreeri välja** vahekaardil **Microsoft Dynamics 365**. See takistab teistel kasutajatel redigeerida samaaegselt tööjaotuse struktuuri rakendusest Finance. Pärast mis tahes muudatuste tegemist tööjaotuse struktuuri avaldamiseks klõpsake valikut **Registreeri sisse** vahekaardil **Microsoft Dynamics 365**.

Kui projektile on rakenduses Finance juba projekti meeskond lisatud, täidetakse ressursi loend meeskonnaliikmetega. Kui projekti meeskonda pole veel projektile lisatud, saate valida ressursid ja luua meeskonna rakenduse Microsoft Project Client seest, klõpsates nuppu **Ressursid** vahekaardil **Microsoft Dynamics 365**. 

Sisseregistreerimise protsessi osana sünkroonitakse Finance’i järgmised andmed.

•   Ülesande nimi

•   Alguskuupäev

•   Lõpukuupäev

•   Eelkäijad

•   Ressursside nimed

•   Kategooria

•   Ressursi kategooria

•   Tööaeg

•   Märkmed

•   Prioriteet

> [!NOTE]
> Kui lisate oma rakenduse Microsoft Project Client failile mõne muu veeru, siis neid ei salvestata faili ja ei kuvata, kui fail uuesti avatakse.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Rakendust Microsoft Project Client kasutades olemasolevale projektile tööjaotuse struktuuri loomine
Rakendust Microsoft Project Client kasutades uue tööjaotuse struktuuri loomiseks tehke järgmist.


1.  Avage Microsoft Project Client.

2.  Vahekaardil **Microsoft Dynamics 365** klõpsake käsku **Ava**.

3.  Valige projekti jaoks **Juriidiline üksus**.

4.  Valige **Project**.

5.  Klõpsake valikut **Registreeri välja** vahekaardil **Microsoft Dynamics 365**.

6.  Kui olete valmis rakendust Finance avaldama, klõpsake **Registreeri sisse** vahekaardil **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Rakendust Microsoft Project Client kasutades olemasoleva projekti olemasoleva tööjaotuse struktuuri asendamine
Uue tööjaotuse struktuuri loomiseks rakendust Microsoft Project Client kasutades ja olemasoleva tööjaotuse struktuuri asendamine olemasoleva projekti jaoks tehke järgmist.

1.  Avage Microsoft Project Client.

2.  Looge rakenduses Microsoft Project Client ajakava.

3.  Vahekaardil **Microsoft Dynamics 365** klõpsake valikut **Salvesta muudatused** > **Olemasoleva projekti asendamine**.

4.  Valige projekti jaoks **Juriidiline üksus**.

5.  Valige **Project**.

6.  Klõpsake **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Uue projekti loomine rakendusest Microsoft Project Client


1.  Avage Microsoft Project Client.

2.  Looge rakenduses Microsoft Project Client ajakava.

3.  Vahekaardil **Microsoft Dynamics 365** klõpsake valikut **Salvesta muudatused** > **Salvesta uude projekti**.

4.  Valige projekti jaoks **Juriidiline üksus**.

5.  Vajaduse korral sisestage **Projekti ID**.

6.  Sisestage **Projekti nimi**.

7.  Valige suvandid **Projekti tüüp**, **Projekti rühm** ja **Projekti kontakti ID**. Teise võimalusena saate luua uue projekti lepingu, klõpsates valikud **Uus**.

8.  Valige ressurssidega kasutamiseks suvand **Kalender**.

11. Klõpsake **OK**.

> [!NOTE]
> Projecti kliendi lisandmoodul ei toeta projekti ID vormingus järgmisi tärke.
> 
>   - Allkriips
>   - Punkt
>   - Tühikuklahv
>   - Kaldkriips

[!INCLUDE[footer-include](../includes/footer-banner.md)]
