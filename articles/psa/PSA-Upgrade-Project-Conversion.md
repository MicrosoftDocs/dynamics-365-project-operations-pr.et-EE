---
title: Project Service Automation to Project Operations projekti plaanimise teisendusprotsess
description: Selles artiklis antakse ülevaade funktsioonide muudatustest Microsoft Dynamics 365 Project Service Automation kuni Dynamics 365 Project Operations.
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
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Project Service Automation to Project Operations projekti plaanimise teisendusprotsess

Kui projekt on edukalt versioonilt 3.X Microsoft Dynamics 365 Project Service Automation üle viidud Lite’ile Dynamics 365 Project Operations, pole projektiülesannete redigeerimine ülesanderuudustiku tööjaotuse struktuuris (WBS) võimalik. Kliendid saavad WBS-id üle vaadata jälgimisvõrgus, kuhu on lisatud uued väljad, et esitada kõik ülesandega seotud üksikasjad. Projektide puhul, kus on vaja WBS-i muudatusi, saate valikuliselt teisendada sobilikud projektid veebi plaanimise kogemuse jaoks uude projekti.

## <a name="project-conversion-process"></a>Projekti konversiooniprotsess

Projekti teisendamiseks toimige järgmiselt.

1. Avage projekti avaleht ja valige **tegevuspaanil käsk Teisenda**.
1. Valige **kinnitusteate väljal OK**, et alustada projekti teisendamist. Toimuvad järgmised toimingud:

    1. Projekti avalehel kuvatav teateriba ütleb: "Projekti ajakava teisendatakse. Te ei saa projektis muudatusi teha enne, kui konversioon on lõpule viidud."
    1. Teid suunatakse projektide loendisse.

    Pärast projekti teisendamise lõpuleviimist toimuvad järgmised toimingud:

    1. Määratud projektijuht saab teate taotluse paremal küljel.
    1. Teateriba, mis teatab, et konversioon on pooleli, eemaldatakse.
    1. Vahekaardil **Ajakava** kuvatakse Projecti veebirakenduse uus plaanimiskogemus. Iga kasutaja, kellel on vastavad litsentsid ja turberollid, saab WBS-i redigeerida.
    1. Väli Plaanimismootor **värskendatakse** versiooniks **Project for the web**.
    1. Nupp **Teisenda** eemaldatakse toimingupaanilt.

> [!IMPORTANT]
> Projektide hulgiteisendamine ei ole lubatud. Kõik katsed ajakohastada korraga suurt hulka projekte lükatakse tagasi. See piirang aitab tagada suure jõudluse kõigile klientidele.

## <a name="manual-tasks-vs-automatic-tasks"></a>Käsitsi tehtavad ülesanded vs automaatsed ülesanded

Kui keskkond viiakse Project Service Automationilt üle Project Operationsile, loetakse kõik WBS-i ülesanded automaatselt plaanituks. Käsitsi plaanitud ülesannete kontseptsioon pole Projecti veebirakenduses saadaval. Siiski saate määratleda oma projektide eelistatud plaanimiskäitumise, kasutades uute projektide loomisel plaanimisrežiimi [sätet.](/project-management/scheduling-modes.md)

## <a name="restricted-operations-for-pre-conversion-projects"></a>Ümberehitamiseelsete projektide piiratud toimingud

Selles jaotises kirjeldatakse funktsionaalseid erinevusi, mida võite oodata, kui projekte pole teisendatud.

### <a name="copy-project"></a>Kopeeri projekt

Kopeerimistoimingut **toetatakse** ainult teisendatud projektide puhul. Täiendatud projekte ei saa enne teisendamist kopeerida.

### <a name="move-project"></a>Teisalda projekt

Projekti alguskuupäeva muutmine ei nihuta proportsionaalselt ülesannete algust, välja arvatud juhul, kui projekt on teisendatud.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Millised on erinevused teisendatud projektide ja uute projektide vahel, mis luuakse pärast versioonitäienduse lõpuleviimist?

Projektidele, mis teisendatakse pärast keskkonna täiendamist, määratakse lipp, mis juhendab ajakava järgima ainult projekti kalendrit. See käitumine vastab Project Service Automationi käitumisele. Kuid lippu ei määrata uutele projektidele, mis luuakse pärast versioonitäiendust. Seetõttu austab ajakava ressursside tööaega, kui need on ülesandele määratud.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Mida teha, kui minu projekti ei teisendata?

Kui teie projekti teisendamine ebaõnnestub, on esimene samm tõrkelogide ülevaatamine, et tuvastada teie WBS-iga seotud levinud probleemid. Kui logid ei viita konkreetsele tõrkele, mille suhtes saate midagi ette võtta, võtke ühendust klienditoega, et teie juhtumit saaks edasi vaadata.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kuidas käsitletakse Projecti veebirakenduses ettevõtete sulgemisi?

Project for the Web ei austa ettevõtte sulgemisi, mille ettevõte määratleb organisatsiooni tasandil. Siiski austab see muud tüüpi puhkepäevi, mis on määratletud antud töötunni mallis.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Millised on Projecti veebirakenduse piirangud?

Vt teemat [Tööjaotuse struktuuri loomine: projekti piirangud](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Kas ma võin oodata muudatusi oma kulu- ja müügiprognoosides?

Harvadel juhtudel, kui ressursi määramise kontuurid arvutatakse ümber või kui need jäävad lähteprojektist erinevale kuupäevapiirile, võite näha erinevusi müügi- ja kuluprognoosides. Täiendusprotsessi osana eeldatakse, et kliendid testivad representatiivset projektide valimit, et nad saaksid aru võimalikest ajakava muudatustest.
