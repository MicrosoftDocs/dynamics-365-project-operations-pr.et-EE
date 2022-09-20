---
title: Üleminek Project Service Automationilt Project Operationsile
description: Selles artiklis antakse ülevaade protsessist, millelt Microsoft Dynamics 365 Project Service Automation üle minna versioonile Dynamics 365 Project Operations.
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
ms.openlocfilehash: 43ea29aeafb62f3ecd69b316f2c0a5b791707da5
ms.sourcegitcommit: bc21fbe8547534d2644269f873eb05d509840f23
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446030"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Üleminek Project Service Automationilt Project Operationsile

Meil on hea meel teatada esimesest kolmest etapist, mis on mõeldud uuendamiseks alates Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations. See artikkel annab ülevaate klientidele, kes alustavad seda põnevat teekonda. Tulevased artiklid sisaldavad arendaja kaalutlusi ja üksikasju funktsioonide täiustuste kohta. Need mitte ainult ei anna juhiseid, mis aitavad teil project operationsile üleminekuks valmistuda, vaid selgitavad ka seda, mida võite pärast versioonitäiendust oodata.

Versiooniuuenduse kohaletoimetamise programm jagatakse kolme etappi.

| Tarne uuendamine | 1. etapp (jaanuar 2022) | 2. etapp (november 2022) | 3. etapp (aprilli laine 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Projektide puhul puudub sõltuvus tööjaotuse struktuurist (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS praegu toetatud projektitoimingute piirides | | :heavy_check_mark: | :heavy_check_mark: |
| WBS väljaspool project operationsi praegu toetatud limiite, sh Projecti töölauakliendi tugi | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Uuendamisprotsessi funktsioone 

Täiendamisprotsessi osana oleme saidikaardile lisanud täienduslogid, et administraatorid saaksid tõrkeid hõlpsamini diagnoosida. Lisaks uuele liidesele lisatakse uued valideerimiseeskirjad, et tagada andmete terviklikkus pärast versioonitäiendust. Täiendamisprotsessile lisatakse järgmised valideerimised.

| Valideerimine | 1. etapp (jaanuar 2022) | 2. etapp (november 2022) | 3. etapp  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS-i valideeritakse levinud andmetervikluse rikkumiste eest (nt ressursimäärangud, mis on seostatud sama emaülesandega, kuid millel on erinevad emaprojektid). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS valideeritakse Project for the [Webi teadaolevate piiride suhtes](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS valideeritakse Projecti töölauakliendi teadaolevate limiitide suhtes. | |  | :heavy_check_mark: |
| Broneeritavaid ressursse ja projektikalendreid hinnatakse tavaliste ühildumatute kalendrireeglite erandite alusel. | | :heavy_check_mark: | :heavy_check_mark: |

2. etapis uuendatakse klientidel, kes lähevad üle versioonile Project Operations, oma olemasolevad projektid projekti planeerimiseks kirjutuskaitstud kogemuseks. Selles kirjutuskaitstud kogemuses on kogu WBS jälgimisruudustikus nähtav. WBS-i redigeerimiseks saavad projektijuhid põhilehel Projektid valida **teisendamise**.**·** Seejärel värskendatakse projekti taustprotsessiga, et see toetaks uut projekti plaanimise kogemust Project for the Webist. See etapp sobib klientidele, kellel on projekte, mis mahuvad [project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries) teadaolevatesse piiridesse.

3. etapis lisatakse Projecti töölauakliendi tugi, mis on kasulik klientidele, kes soovivad jätkata oma projektide redigeerimist selles rakenduses. Kui aga olemasolevad projektid teisendatakse uueks veebikogemuse projektiks, keelatakse juurdepääs lisandmoodulile iga teisendatud projekti puhul.

## <a name="prerequisites"></a>eeltingimused

1. etapi versioonitäienduse saamiseks peab klient vastama järgmistele kriteeriumidele.

- Sihtkeskkond ei tohi sisaldada msdyn_projecttask **olemi kirjeid**.
- Kehtivad Project Operationsi litsentsid tuleb määrata kõigile kliendi aktiivsetele kasutajatele. 
- Klient peab täiendusprotsessi valideerima vähemalt ühes mittetootmiskeskkonnas, millel on esinduslik andmestik, mis on tootmisandmetega vastavusse viidud.
- Sihtkeskkond peab olema värskendatud versioonile Project Service Automation Update Release 41 (3.10.62.162) või uuem.

2. ja 3. etapi eeltingimusi ajakohastatakse üldiste saadavuskuupäevade lähenedes.

## <a name="licensing"></a>Litsentsimine

Kui teil on Project Service Automationi aktiivsed litsentsid, saate installida ja kasutada Project Operationsi, mis sisaldab kõiki Project Service Automationi võimalusi ja palju muud. Sel viisil saate testida Project Operationsi võimalusi, kui jätkate Project Service Automationi kasutamist tootmises. Pärast Project Service Automationi litsentside aegumist peate üle minema versioonile Project Operations. Ülemineku kavandamisel peate arvestama asjaoluga, et Project Operationsi litsents ei sisalda Project Service Automationi litsentsi.

## <a name="testing-and-refactoring-customizations"></a>Kohanduste testimine ja refactoring

Alustuseks importige kõik kohandused puhtasse Project Operationsi (Lite) keskkonda, et veenduda, et importimine õnnestub ja äritoimingud käituvad ootuspäraselt.

Siin on mõned asjad, millele tähelepanu pöörata.

- Importimine võib puuduvate sõltuvuste tõttu nurjuda. Teisisõnu, kohanduste viiteväljad või muud komponendid, mis on Project Operationsis eemaldatud. Sellisel juhul eemaldage need sõltuvused arenduskeskkonnast.
- Kui teie mittehallatavad ja hallatavad lahendused sisaldavad komponente, mida pole kohandatud, eemaldage need komponendid lahendusest. Näiteks kui kohandate **projekti** olemit, lisage lahendusele ainult olemi päis. Ärge lisage kõiki välju. Kui olete varem kõik alamkomponendid lisanud, peate võib-olla uue lahenduse käsitsi looma ja sellele asjakohased komponendid lisama.
- Vormid ja vaated ei pruugi ilmuda ootuspäraselt. Mõnel juhul, kui olete kohandanud mõnda valmisvormi või vaadet, võivad kohandused takistada Project Operationsi uute värskenduste jõustumist. Nende probleemide tuvastamiseks soovitame teil teha kõrvuti ülevaate Project Operationsi puhtast installist ja project operationsi installist, mis sisaldab teie kohandusi. Võrrelge oma ettevõttes kõige sagedamini kasutatavaid vorme veendumaks, et vormi teie versioonil on endiselt mõtet ja vormi puhtast versioonist pole midagi puudu. Tehke sama tüüpi kõrvuti läbivaatus kõigi kohandatud vaadete kohta.
- Äriloogika võib käitusajal ebaõnnestuda. Kuna lisandmoodulite väljadele viidasid importimise ajal ei valideerita, võib äriloogika nurjuda, kuna viiteid väljadele enam ei eksisteeri, ja võite saada tõrketeate, mis sarnaneb järgmise näitega: "Projekti" olem ei sisalda atribuute nimega Name = ’msdyn_plannedhours’ ja NameMapping = ’Logical’." Sellisel juhul muutke kohandusi nii, et need kasutaksid uusi välju. Kui kasutate pistikprogrammi loogikas automaatselt loodud puhverserveriklasse ja tugevaid tüübiviiteid, kaaluge nende puhverserverite taastamist puhtast installist. Nii saate hõlpsalt tuvastada kõik kohad, kus teie lisandmoodulid sõltuvad aegunud väljadest.

Pärast kohanduste värskendamist Project Operationsi puhtaks importimiseks jätkake järgmiste juhistega.

## <a name="end-to-end-testing-in-development-environments"></a>Otspunkttestimine arenduskeskkondades

### <a name="initiate-upgrade"></a>Versioonitäienduse algatamine 

1. Power Platform Otsige halduskeskuses üles ja valige oma keskkond. Seejärel leidke ja valige **Dynamics 365 Project Operations** rakendustes.
2. Täiendamise alustamiseks valige **Installi**. Halduskeskus Power Platform esitleb seda installi uue installina. Siiski tuvastatakse Project Service Automationi varasema versiooni olemasolu ja olemasolevat installi uuendatakse.

    Kui versioonitäiendus on lõpule viidud, peaks keskkond näitama, et Project Operations on installitud ja Project Service Automation pole installitud.

    > [!NOTE]
    > Sõltuvalt keskkonnas olevate andmete hulgast võib versioonitäiendus võtta mitu tundi. Versioonitäiendust haldav põhimeeskond peaks vastavalt planeerima ja käivitama täienduse töövälisel ajal. Mõnel juhul, kui andmemaht on suur, tuleks versiooniuuendus käivitada nädalavahetusel. Otsus ajastamise kohta peaks põhinema madalamates keskkondades testimise tulemustel.

3. Täiendage kohandatud lahendusi vastavalt vajadusele. Juurutage sel hetkel kõik muudatused, mille tegite oma kohandustes [selle artikli jaotises Kohanduste testimine ja refaktoriseerimine](#testing-and-refactoring-customizations).
4. Avage **Sätete** \> **lahendused** ja valige lahenduse Project Operations Deprecated Components desinstallimine.**·**

    See lahendus on ajutine lahendus, mis hoiab olemasolevat andmemudelit ja komponente, mis on versiooniuuenduse ajal olemas. Selle lahenduse eemaldamisega eemaldate kõik väljad ja komponendid, mida enam ei kasutata. Sel viisil aitate liidest lihtsustada ning muuta integreerimise ja laiendamise lihtsamaks.
    
### <a name="validate-common-scenarios"></a>Levinud stsenaariumide valideerimine

Konkreetsete kohanduste valideerimisel soovitame teil üle vaadata ka äriprotsessid, mida kõigis rakendustes toetatakse. Need äriprotsessid hõlmavad muu hulgas müügiüksuste loomist, nagu noteeringud ja lepingud, ning WBS-e sisaldavate projektide loomist ja tegelike tehingute kinnitamist.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Suuremad muudatused Project Service Automationi ja Project Operationsi vahel

Selles jaotises on kokkuvõte suurematest muudatustest, mida võite oodata Project Service Automationi ja Project Operationsi vahel.

### <a name="project-planning"></a>Projekti kavandamine

Project Operationsi projekti plaanimise võimalused ei tugine enam kliendi- ja serveripoolse loogika kombinatsioonile. Selle asemel kasutab Project Operations plaanimismootorina Project for the Webi. See plaanimisvõimaluste muudatus võimaldab mitmeid uusi funktsioone, nagu tahvli- ja Ganttivaated, ressursipõhine planeerimine, [ülesande kontroll-loendi üksused](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) ja projekti plaanimisrežiimid. Uusi plaanimisvõimalusi toetavad ka rikkalikud uued [rakenduse programmeerimisliidesed (API-d).](../project-management/schedule-api-preview.md) Nende API-de eesmärk on aidata tagada, et ükski programmiline toiming olemi loomiseks, värskendamiseks või kustutamiseks WBS-is ei riku graafiku arvutatud välju.

## <a name="billing-and-pricing"></a>Arveldamine ja hinnakujundus

Osana jätkuvatest investeeringutest project operationsisse on arvelduses ja hinnakujunduses saadaval mitu uut võimalust. Järgmiselt on toodud mõned näited.

- [Materjalikasutuse salvestamine projektides ja projektiülesannetes](../material/material-usage-log.md)
- [Alltöövõtu haldamine](../pro/subcontracting/managing-subcontracts-overview.md)
- [Ettemaksud või honoraril põhinevad lepingud](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Lepingu mitteületamise staatus ja valideerimised](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Ülesandepõhine arveldamine

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Milliseid juurutustüüpe versioonitäienduseks praegu toetatakse?

| Lähtekeel                                                 | Sihtkeel                                                    | Olek                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite’i juurutamine                        | Toetatud               |
| Dynamics 365 Finance Projektijuhtimine ja raamatupidamine | Project Operations Lite’i juurutamine                        | Pole praegu toetatud |
| Finants projektijuhtimine ja raamatupidamine              | Project Operations ressursi/mitteaktsia stsenaariumite jaoks     | Pole praegu toetatud |
| Project Service Automation 3.x                         | Project Operations ressursi/mitteaktsia stsenaariumite jaoks     | Pole praegu toetatud |
| Projekt veebi jaoks (spetsiaalne keskkond)            | Project Operations Lite’i juurutamine                        | Pole praegu toetatud |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kuidas installida Project Operations enne, kui versioonitäienduse tööriist on saadaval?

Project Operationsi installimiseks enne versioonitäiendustööriistade kasutamist on kaks võimalust.

- Valmistage ette uus keskkond.
- Juurutage Project Operations eraldi mis tahes müügiorganisatsioonis, kus Project Service Automationi pole.

> [!NOTE]
> Kui Project Service Automation on organisatsiooni installitud, kuid seda ei kasutatud, saab selle desinstallida. Pärast Project Service Automationi täielikku eemaldamist saab Project Operationsi installida samasse organisatsiooni.
