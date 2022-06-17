---
title: Üleminek projecti teenuse automatiseerimiselt projektitoimingutele
description: Selles artiklis antakse ülevaade rakendusest Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.openlocfilehash: 30eb02240de6617d4c550ce59db2a454eee36f5b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912971"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Üleminek projecti teenuse automatiseerimiselt projektitoimingutele

Meil on hea meel teatada esimesest kolmest etapist, et uuendada alates rakendusest Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations. See artikkel annab ülevaate klientidele, kes alustavad seda põnevat teekonda. Tulevased artiklid sisaldavad arendaja kaalutlusi ja üksikasju funktsioonide täiustamise kohta. Need mitte ainult ei anna juhiseid, mis aitavad teil valmistuda project Operationsile üleminekuks, vaid selgitavad ka seda, mida võite oodata pärast täiendamist.

Täienduse tarneprogramm jagatakse kolme etappi.

| Täienduse kohaletoimetamine | 1. etapp (jaanuar 2022) | 2. etapp (aprilli laine 2022) | 3. etapp  |
|------------------|------------------------|---------------------------|---------------------------|
| Projektide puhul ei sõltuta tööjaotuse struktuurist (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS projektitoimingute praegu toetatud piirides | | :heavy_check_mark: | :heavy_check_mark: |
| WBS väljaspool projektitoimingute praegu toetatud piiranguid, sh projekti töölauakliendi tugi | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Täiendusprotsessi funktsioonid 

Täiendusprotsessi osana oleme saidi kaardile lisanud täienduslogid, et administraatorid saaksid tõrkeid hõlpsamini diagnoosida. Lisaks uuele liidesele lisatakse uued valideerimisreeglid, et tagada andmete terviklikkus pärast täiendamist. Täiendusprotsessi lisatakse järgmised valideerimised.

| Valideerimised | 1. etapp (jaanuar 2022) | 2. etapp (aprilli laine 2022) | 3. etapp  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS valideeritakse levinud andmete terviklikkuse rikkumiste (nt ressursimäärangud, mis on seotud sama põhiülesandega, kuid millel on erinevad emaprojektid) vastu. | | :heavy_check_mark: | :heavy_check_mark: |
| WBS kinnitatakse [vastavalt Project for the Web teadaolevatele piirangutele](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS valideeritakse projekti töölauakliendi teadaolevate piirangute alusel. | |  | :heavy_check_mark: |
| Broneeritavaid ressursse ja projektikalendreid hinnatakse levinud kokkusobimatute kalendrireegli erandite alusel. | | :heavy_check_mark: | :heavy_check_mark: |

2. etapis uuendatakse Project Operationsile üle läinud klientidel oma olemasolevad projektid projekti planeerimiseks kirjutuskaitstud kogemuseks. Selles kirjutuskaitstud kogemuses on kogu WBS nähtav jälgimisvõrgustikus. WBS-i redigeerimiseks saavad projektijuhid valida **põhiprojektide** **lehel Teisenda**. Seejärel värskendab taustaprotsess projekti nii, et see toetab project for the Webi uut projekti planeerimise kogemust. See etapp sobib klientidele, kellel on projekte, mis sobivad [Project for the Webi](/project-for-the-web/project-for-the-web-limits-and-boundaries) teadaolevatesse piiridesse.

3. etapis lisatakse Projecti töölauakliendi tugi klientide kasuks, kes soovivad jätkata oma projektide redigeerimist sellest rakendusest. Kui aga olemasolevad projektid teisendatakse uude veebikogemuse projekti, keelatakse juurdepääs lisandmoodulile iga teisendatud projekti puhul.

## <a name="prerequisites"></a>eeltingimused

1. etapi versiooniuuenduse saamiseks peab klient vastama järgmistele kriteeriumidele.

- Sihtkeskkond ei tohi sisaldada olemi msdyn_projecttask **kirjeid**.
- Kehtivad projektitoimingute litsentsid tuleb määrata kõigile kliendi aktiivsetele kasutajatele. 
- Klient peab täiendusprotsessi valideerima vähemalt ühes tootmisvälises keskkonnas, millel on esinduslik andmekogum, mis on joondatud tootmisandmetega.
- Sihtkeskkond tuleb värskendada versioonile Project Service Automation Update Release 41 (3.10.62.162) või uuemale.

2. ja 3. etapi eeltingimusi ajakohastatakse üldise kättesaadavuse kuupäevade lähenemisviisina.

## <a name="licensing"></a>Litsentsimine

Kui teil on project service automationi jaoks aktiivsed litsentsid, saate installida ja kasutada Project Operationsi, mis hõlmab kõiki Project Service Automationi ja muu võimalusi. Sel viisil saate testida Project Operationsi võimalusi, kui jätkate projektiteenuste automatiseerimise kasutamist tootmises. Pärast projektiteenuse automatiseerimise litsentside aegumist peate üle minema projektitoimingutele. Selle ülemineku kavandamisel peate arvestama asjaoluga, et Project Operationsi litsents ei sisalda projektiteenuse automatiseerimise litsentsi.

## <a name="testing-and-refactoring-customizations"></a>Kohanduste testimine ja ümberlükkamine

Lähtepunktina importige kõik kohandused puhtasse projektitoimingute (lite) keskkonda, et kinnitada, et import on edukas ja et äritoimingud käituvad ootuspäraselt.

Siin on mõned asjad, mida jälgida:

- Importimine võib puuduvate sõltuvuste tõttu nurjuda. Teisisõnu, kohanduste viiteväljad või muud komponendid, mis on Project Operationsis eemaldatud. Sellisel juhul eemaldage need sõltuvused arengukeskkonnast.
- Kui teie mittehallatavad ja hallatavad lahendused sisaldavad komponente, mida pole kohandatud, eemaldage need komponendid lahendusest. Näiteks kui kohandate **olemi Project**, lisage lahendusele ainult olemipäis. Ärge lisage kõiki välju. Kui olete varem kõik alamkomponendid lisanud, peate võib-olla looma käsitsi uue lahenduse ja lisama sellele asjakohased komponendid.
- Vormid ja vaated ei pruugi ootuspäraselt ilmuda. Mõnel juhul, kui olete kohandanud mõnda kastivälist vormi või vaadet, võivad kohandused takistada Project Operationsi uute värskenduste jõustumist. Nende probleemide tuvastamiseks soovitame teil teha kõrvuti ülevaade Project Operationsi puhtast installimisest ja Project Operationsi installimisest, mis sisaldab teie kohandusi. Võrrelge oma ettevõtte kõige sagedamini kasutatavaid vorme, et kinnitada, et teie vormi versioon on endiselt mõttekas ja vormi puhtast versioonist pole midagi puudu. Tehke kohandatavate vaadete puhul sama tüüpi kõrvutiülevaatust.
- Äriloogika võib käitusajal ebaõnnestuda. Kuna viited teie lisandmoodulite väljadele ei ole importimise ajal valideeritud, võib äriloogika nurjuda viidete tõttu väljadele, mida enam ei eksisteeri, ja võite saada tõrketeate, mis sarnaneb järgmise näitega: olem "Project" ei sisalda atribuuti nimega = "msdyn_plannedhours" ja "NameMapping = 'Loogiline". Sellisel juhul muutke oma kohandusi nii, et need kasutaksid uusi välju. Kui kasutate pistikprogrammi loogikas automaatselt genereeritud puhverserveriklasse ja tugeva tüübi viiteid, kaaluge nende puhverserverite taastamist puhtast installist. Sel viisil saate hõlpsasti tuvastada kõik kohad, kus teie lisandmoodulid sõltuvad aegunud väljadest.

Pärast kohanduste värskendamist projektitoimingute puhtaks importimiseks liikuge järgmiste juhiste juurde.

## <a name="end-to-end-testing-in-development-environments"></a>Otsast lõpuni testimine arenduskeskkondades

### <a name="initiate-upgrade"></a>Täienduse algatamine 

1. Power Platform Otsige ja valige halduskeskuses oma keskkond. Seejärel otsige rakendustest üles ja valige **Dynamics 365 Project Operations**.
2. Täienduse alustamiseks valige **Installi**. Halduskeskus Power Platform esitab selle installi uue installina. Siiski tuvastatakse Project Service Automationi varasema versiooni olemasolu ja uuendatakse olemasolevat installimist.

    Pärast versioonitäienduse lõpuleviimist peaks keskkond näitama, et Project Operations on installitud ja et Project Service Automation pole installitud.

    > [!NOTE]
    > Sõltuvalt keskkonna andmete hulgast võib uuendamine võtta mitu tundi. Põhimeeskond, kes uuendamist haldab, peaks vastavalt planeerima ja käivitama versioonitäienduse väljaspool tööaega. Mõnel juhul, kui andmemaht on suur, tuleks uuendamine käivitada nädalavahetusel. Ajakava otsus peaks põhinema madalamate keskkondade testimistulemustel.

3. Vajadusel täiendage kohandatud lahendusi. Sel hetkel juurutage kõik kohandustes [tehtud muudatused selle artikli jaotises Kohandamiste testimine ja refactoring](#testing-and-refactoring-customizations).
4. **Avage sätete** \> **lahendused** ja valige, et desinstallida **lahendus Project Operations Deprecated Components.**

    See lahendus on ajutine lahendus, mis sisaldab olemasolevat andmemudelit ja komponente, mis on versioonitäienduse ajal olemas. Selle lahenduse eemaldamisega eemaldate kõik väljad ja komponendid, mida enam ei kasutata. Sel viisil aitate liidest lihtsustada ning muuta integreerimine ja laiendamine lihtsamaks.
    
### <a name="validate-common-scenarios"></a>Levinud stsenaariumide kinnitamine

Kui kinnitate oma konkreetsed kohandused, soovitame teil üle vaadata ka rakendustes toetatud äriprotsessid. Need äriprotsessid hõlmavad muu hulgas müügiüksuste (nt pakkumiste ja lepingute) loomist ning selliste projektide loomist, mis sisaldavad WBS-e ja tegelike kinnitust.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Suured muudatused projektiteenuste automatiseerimise ja projektitoimingute vahel

See jaotis annab kokkuvõtte peamistest muudatustest, mida võite projektiteenuste automatiseerimise ja projektitoimingute vahel oodata.

### <a name="project-planning"></a>Projekti kavandamine

Project Operationsi projektiplaneerimise võimalused ei tugine enam kliendipoolsele loogikale ja serveripoolsele loogikale. Selle asemel kasutab Project Operations Project for the Webi plaanimismootorina. See plaanimisvõimaluste muudatus võimaldab mitmeid uusi funktsioone ( nt Boardi ja Gantti vaated, ressursipõhine planeerimine, [ülesande kontroll-loendi üksused](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) ja projekti planeerimise režiimid). Uusi sõiduplaanimisvõimalusi toetab ka rikkalik hulk uusi [rakenduste programmeerimisliidest (API-sid)](../project-management/schedule-api-preview.md). Nende API-de eesmärk on tagada, et ükski programmiline toiming olemi loomiseks, värskendamiseks või kustutamiseks WBS-is ei riku ajakava arvutatud välju.

## <a name="billing-and-pricing"></a>Arveldamine ja hinnakujundus

Osana jätkuvatest investeeringutest Project Operationsi on arvelduses ja hinnakujunduses saadaval mitmed uued võimalused. Järgmiselt on toodud mõned näited.

- [Materjalikasutuse salvestamine projektides ja projektiülesannetes](../material/material-usage-log.md)
- [Alltöövõtu haldamine](../pro/subcontracting/managing-subcontracts-overview.md)
- [Ettemaksud või honoraril põhinevad lepingud](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Leping, mis ei ületa olekut ja valideerimisi](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Ülesandepõhine arveldamine

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Milliseid juurutustüüpe praegu täiendamiseks toetatakse?

| Lähtekeel                                                 | Sihtkeel                                                    | Olek                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Projektitoimingute Lite juurutus                        | Toetatud               |
| Dynamics 365 Finance projektijuhtimine ja raamatupidamine | Projektitoimingute Lite juurutus                        | Praegu ei toetata |
| Finantsprojekti juhtimine ja raamatupidamine              | Project Operations ressursi/mitteaktsia stsenaariumite jaoks     | Praegu ei toetata |
| Projektiteenuse automatiseerimine 3.x                         | Project Operations ressursi/mitteaktsia stsenaariumite jaoks     | Praegu ei toetata |
| Veebiprojekt (spetsiaalne keskkond)            | Projektitoimingute Lite juurutus                        | Praegu ei toetata |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kuidas installida Project Operationsi enne täiendustööriista saadavalolekut?

Project Operationsi installimiseks on enne täiendustööriista saadavalolekut kaks võimalust.

- Uue keskkonna loomine.
- Juurutage projektitoimingud eraldi mis tahes müügiorganisatsioonis, kus Project Service Automationit pole.

> [!NOTE]
> Kui Project Service Automation on organisatsiooni installitud, kuid seda ei kasutatud, saab selle desinstallida. Pärast projekti teenuse automatiseerimise täielikku eemaldamist saab project Operationsi installida samasse organisatsiooni.
