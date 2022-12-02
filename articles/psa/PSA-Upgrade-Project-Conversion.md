---
title: Projekti plaanimise teisendustoiming rakenduselt Project Service Automation üleminekul rakendusele Project Operations
description: See artikkel annab ülevaate rakenduse Microsoft Dynamics 365 Project Service Automation funktsioonide muudatustest rakendusele Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642563"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Projekti plaanimise teisendustoiming rakenduselt Project Service Automation üleminekul rakendusele Project Operations

Pärast projekti edukat versiooni Microsoft Dynamics 365 Project Service Automation 3.X versioonile Dynamics 365 Project Operations Lite üleviimist ei ole projektiülesannete redigeerimine ülesannete ruudustiku tööjaotuse struktuuris (WBS) võimalik. Kliendid saavad jälgida WBS-e jälgimisruudustikus, kuhu on lisatud uued väljad, et edastada kõik ülesandega seotud üksikasjad. Projektide puhul, mille puhul on vaja WBS-i muudatusi, saate sobilikud projektid valikuliselt teisendada uue Project for the webi ajastamise kogemuse jaoks.

## <a name="project-conversion-process"></a>Projekti teisendamise protsess

Projekti teisendamiseks järgige neid etappe.

1. Avage projekti avaleht ja valige toimingupaanil **Teisenda**.
1. Projekti teisendamise alustamiseks valige kinnitusteatekastis **OK**. Toimuvad järgmised toimingud:

    1. Projekti avalehel kuvatav teateriba teatab: „Projekti ajakava teisendatakse. Te ei saa projektis muudatusi teha enne, kui teisendamine on lõppenud“.
    1. Teid suunatakse ümber projektiloendisse.

    Pärast projekti teisendamise lõpetamist toimuvad järgmised toimingud:

    1. Määratud projektijuht saab rakenduse paremas servas teate.
    1. Teateriba, mis teatab, et teisendamine on pooleli, eemaldatakse.
    1. Vahekaardil **Ajakava** kuvatakse Project for the Webi uus ajastamiskogemus. Kõik kasutajad, kellel on sobivad litsentsid ja turberollid, saavad WBS-i redigeerida.
    1. Välja **Ajastamismootor** on värskendatud väärtuseks **Project for the web**.
    1. Nupp **Teisalda** eemaldatakse toimingupaanilt.

> [!IMPORTANT]
> Projektide hulgikonverteerimine ei ole lubatud. Kõik katsed värskendada korraga suurt hulka projekte pidurdatakse. See piirang aitab tagada kõrge jõudluse kõigile klientidele.

## <a name="manual-tasks-vs-automatic-tasks"></a>Käsitsi ülesanded vs automaatsed ülesanded

Kui keskkond viiakse rakenduselt Project Service Automation üle rakendusele Project Operations, loetakse kõik WBS-i ülesanded automaatselt ajastatuks. Käsitsi ajastatud toimingute kontseptsioon pole rakenduses Project for the Web saadaval. Siiski saate määrata oma projektide jaoks eelistatud ajakava käitumise, kasutades uute projektide loomisel sätet [ajastamisrežiim](/project-management/scheduling-modes.md).

## <a name="restricted-operations-for-pre-conversion-projects"></a>Piiratud toimingud konversioonieelsete projektide jaoks

Selles jaotises kirjeldatakse funktsionaalseid erinevusi, mida võite oodata, kui projekte pole teisendatud.

### <a name="copy-project"></a>Kopeerige projekt

Toimingut **Kopeeri** toetatakse ainult teisendatud projektide puhul. Täiendatud projekte ei saa enne teisendamist kopeerida.

### <a name="move-project"></a>Teisaldage projekt

Projekti alguskuupäeva muutmine ei nihuta proportsionaalselt ülesannete algust, välja arvatud juhul, kui projekt on teisendatud.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Mille poolest erinevad teisendatud projektid uutest projektidest, mis luuakse pärast täienduse lõpetamist?

Projektide puhul, mis teisendatakse pärast keskkonna täiendamist, määratakse lipp, mis juhendab ajakava järgima ainult projekti kalendrit. See käitumine ühtib Project Service Automationi käitumisega. Uute projektide jaoks, mis luuakse pärast täiendamist, lippu siiski ei määrata. Seetõttu arvestab ajakava ressursside töötunde, kui need ülesandele määratakse.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Mida peaksin tegema, kui minu projekti ei õnnestu teisendada?

Kui teie projekti ei õnnestu teisendada, vaadake esimese sammuna üle tõrkelogid, et tuvastada teie WBS-iga seotud levinud probleemid. Kui logid ei viita konkreetsele veale, mille lahendamiseks saaksite midagi ette võtta, võtke ühendust klienditoega, et teie juhtumi läbivaatamine saaks edasi minna.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kuidas käsitletakse ettevõtte sulgemisi rakenduses Project for the Web?

Project for the Web ei arvesta ettevõtete sulgemistega, mille ettevõte määrab organisatsiooni tasandil. Siiski arvestab see teist tüüpi puhkepäevi, mis on määratletud antud töötunnimallis.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Millised on Project for the Webi piirangud?

Vaadake artiklit [Tööjaotuse struktuuri loomine: Projekti piirangud](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Kas on oodata muutusi oma kulu- ja müügiprognoosides?

Harvadel juhtudel, kui ressursi määramise kontuurid arvutatakse ümber või kui need langevad lähteprojektist erinevale kuupäevapiirile, võite müügi- ja kuluprognoosides näha erinevusi. Täiendusprotsessi osana eeldatakse, et kliendid testivad esinduslikku projektide näidiskomplekti, et nad mõistaksid võimalikke ajakava muudatusi.
