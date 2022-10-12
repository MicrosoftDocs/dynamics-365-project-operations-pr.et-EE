---
title: Project Service Automationi funktsioonimuudatused Project Operationsiks
description: Selles artiklis antakse ülevaade funktsioonimuudatustest Microsoft Dynamics 365 Project Service Automation kuni Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621317"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Project Service Automationi funktsioonimuudatused Project Operationsiks

Pärast seda, kui projekt on edukalt üle viidud versioonilt Microsoft Dynamics 365 Project Service Automation 3.X versioonile Dynamics 365 Project Operations Lite, pole projektiülesannete redigeerimine ülesanderuudustiku tööjaotuse struktuuris (WBS) võimalik. Kliendid saavad WBS-e üle vaadata jälgimisruudustikus, kuhu on lisatud uued väljad, et esitada kõik ülesandega seotud üksikasjad. Projektide puhul, mille puhul on vaja WBS-i muudatusi teha, saate veebiplaanimise kogemuse jaoks valikuliselt teisendada sobilikud projektid uueks projektiks.

## <a name="project-conversion-process"></a>Projekti teisendamise protsess

Projekti teisendamiseks toimige järgmiselt.

1. Avage projekti avaleht ja valige **tegevuspaanil Teisenda**.
1. Valige kinnitusteate väljal **projekti konversiooni alustamiseks OK**. Toimuvad järgmised toimingud:

    1. Projekti avalehel kuvataval teateribal on kirjas "Projekti ajakava teisendatakse. Te ei saa projektis muudatusi teha enne, kui teisendamine on lõpule viidud."
    1. Teid suunatakse projektide loendisse.

    Pärast projekti teisendamise lõpuleviimist toimuvad järgmised toimingud:

    1. Määratud projektijuht saab teate taotluse paremal küljel.
    1. Teateriba, mis teatab, et teisendamine on pooleli, eemaldatakse.
    1. Vahekaardil **Ajakava** kuvatakse Projecti veebirakenduse uus plaanimiskogemus. Iga kasutaja, kellel on asjakohased litsentsid ja turberollid, saab WBS-i redigeerida.
    1. Väli **Plaanimismootor** värskendatakse versiooniks **Project for the web**.
    1. Nupp **Teisenda** eemaldatakse toimingupaanilt.

> [!IMPORTANT]
> Projektide hulgikonversioon pole lubatud. Kõik katsed uuendada samal ajal suurt hulka projekte piiratakse. See piirang aitab tagada kõrge jõudluse kõigile klientidele.

## <a name="manual-tasks-vs-automatic-tasks"></a>Käsitsi tehtavad ülesanded vs automaatsed ülesanded

Kui keskkond viiakse Project Service Automationilt üle Project Operationsile, loetakse kõik WBS-i ülesanded automaatselt ajastatud. Käsitsi ajastatud ülesannete kontseptsioon pole Project for the Webis saadaval. Siiski saate määratleda oma projektide eelistatud plaanimiskäitumise, kasutades [uute projektide loomisel plaanimisrežiimi](/project-management/scheduling-modes.md) sätet.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Ümberehituseelsete projektide piiratud toimingud

Selles jaotises kirjeldatakse funktsionaalseid erinevusi, mida võite oodata, kui projekte pole teisendatud.

### <a name="copy-project"></a>Kopeeri projekt

Toimingut **Kopeeri** toetatakse ainult teisendatud projektide puhul. Täiendatud projekte ei saa enne teisendamist kopeerida.

### <a name="move-project"></a>Teisalda projekt

Projekti alguskuupäeva muutmine ei liiguta ülesannete algust proportsionaalselt, välja arvatud juhul, kui projekt on teisendatud.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Mis on teisendatud projektidel ja uutel projektidel, mis luuakse pärast versioonitäienduse lõpuleviimist?

Projektide puhul, mis teisendatakse pärast keskkonna täiendamist, seatakse lipp, mis juhendab ajakava järgima ainult projektikalendrit. See käitumine vastab Project Service Automationi käitumisele. Lippu ei määrata siiski uutele projektidele, mis luuakse pärast versioonitäiendust. Seetõttu järgib ajakava ressursside tööaega, kui need on ülesandele määratud.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Mida teha, kui minu projekti ei õnnestu teisendada?

Kui teie projekti ei teisendata, on esimene samm tõrkelogide ülevaatamine, et tuvastada teie WBS-iga seotud levinud probleemid. Kui logid ei näita konkreetset viga, mille korral saate toiminguid teha, võtke ühendust klienditoega, et teie juhtumit saaks põhjalikumalt uurida.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kuidas käsitletakse project for the webis ettevõtete sulgemisi?

Project for the Web ei austa ettevõtte poolt organisatsiooni tasandil määratletud ettevõtte sulgemisi. Kuid see austab muud tüüpi puhkepäevi, mis on määratletud antud töötunni mallis.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Millised on rakenduse Project veebiversiooni piirangud?

Vt [teemat Tööjaotuse struktuuri loomine: projekti piirangud](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Kas ma võin oodata muudatusi oma kulu- ja müügiprognoosides?

Harvadel juhtudel, kui ressursimäärangu kontuurid arvutatakse ümber või kui need langevad lähteprojektist erinevale kuupäevapiirile, võite näha müügi- ja kuluprognooside erinevusi. Täiendamisprotsessi osana eeldatakse, et kliendid testivad representatiivset projektide näidiskomplekti, et nad saaksid aru võimalikest ajakava muudatustest.
