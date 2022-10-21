---
title: Üleminek rakenduselt Project Service Automation rakendusele Project Operations
description: Selles artiklis antakse ülevaade protsessist, millelt versioonile Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.openlocfilehash: 2d7b372cac391fab7a81ac6ac5d2ea6d12977b5c
ms.sourcegitcommit: 9de444ae0460c8d15c77d225d0c0ad7f8445d5fc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9686970"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Üleminek rakenduselt Project Service Automation rakendusele Project Operations

Meil on hea meel teatada teisest kolmest etapist, mis on seotud üleminekuga Microsoft Dynamics 365 Project Service Automation Microsoftile Dynamics 365 Project Operations. See artikkel annab ülevaate klientidele, kes alustavad seda põnevat teekonda. 

Versiooniuuenduse kohaletoimetamise programm jaguneb kolmeks etapiks.

| Versiooniuuenduse kohaletoimetamine | 1. etapp (jaanuar 2022) | 2. etapp (november 2022) | 3. etapp (aprilli laine 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Projektide puhul puudub sõltuvus tööjaotuse struktuurist (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS projekti tegevuste praegu toetatud piirides | | :heavy_check_mark: | :heavy_check_mark: |
| WBS väljaspool Project Operationsi praegu toetatud limiite, sh Projecti töölauakliendi tugi | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Uuendamisprotsessi funktsioonid 

Täiendusprotsessi osana oleme saidikaardile lisanud täienduslogid, et administraatorid saaksid tõrkeid hõlpsamini diagnoosida. Lisaks uuele liidesele lisatakse uued valideerimisreeglid, et tagada andmete terviklikkus pärast uuendamist. Täiendusprotsessile lisatakse järgmised valideerimised.

| Valideerimine | 1. etapp (jaanuar 2022) | 2. etapp (november 2022) | 3. etapp  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS-i kontrollitakse levinud andmetervikluse rikkumiste eest (nt ressursimääramised, mis on seotud sama põhiülesandega, kuid millel on erinevad emaprojektid). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS valideeritakse Project for the Webi teadaolevate limiitide [alusel](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS valideeritakse Projecti töölauakliendi teadaolevate limiitide alusel. | |  | :heavy_check_mark: |
| Broneeritavaid ressursse ja projektikalendreid hinnatakse tavaliste ühildumatute kalendrireeglite erandite alusel. | | :heavy_check_mark: | :heavy_check_mark: |

2. etapis viiakse projektitoimingutele üle minevate klientide olemasolevad projektid projekti plaanimiseks kirjutuskaitstud kasutuskogemuseks. Selles kirjutuskaitstud keskkonnas on jälgimisruudustikus nähtav täielik WBS. WBS-i redigeerimiseks saavad projektijuhid valida projekti avalehel käsu [**Teisenda**](/PSA-Upgrade-Project-Conversion.md). Seejärel värskendatakse projekti taustprotsessiga, et see toetaks projecti veebirakendusest tulevat uut projekti plaanimise kogemust. See etapp sobib klientidele, kellel on projekte, mis mahuvad Project for the Webi [teadaolevatesse](/project-for-the-web/project-for-the-web-limits-and-boundaries) piiridesse.

3. etapis lisatakse Projecti töölauakliendi tugi, mis on kasulik klientidele, kes soovivad jätkata oma projektide redigeerimist sellest rakendusest. Kui aga olemasolevad projektid teisendatakse uude Project for the Web Experience’i, keelatakse juurdepääs lisandmoodulile iga teisendatud projekti puhul.

## <a name="prerequisites"></a>eeltingimused

1. etapi versioonitäienduse saamiseks peate vastama järgmistele kriteeriumidele.

- Sihtkeskkond ei tohi sisaldada msdyn_projecttask **olemi kirjeid**.
- Kehtivad Project Operationsi litsentsid tuleb määrata kõigile aktiivsetele kasutajatele. 
- Peate versioonitäiendusprotsessi valideerima vähemalt ühes mittetootmiskeskkonnas, mis sisaldab teie tootmiskeskkonnaga joondatud representatiivset andmekogumit.
- Sihtkeskkond tuleb värskendada versioonile Project Service Automation Update Release 37 (V3.10.58.120) või uuemale versioonile.

2. etapi versioonitäienduse saamiseks peate vastama järgmistele kriteeriumidele.

- Kehtivad Project Operationsi litsentsid tuleb määrata kõigile aktiivsetele kasutajatele. 
- Peate versioonitäiendusprotsessi valideerima vähemalt ühes mittetootmiskeskkonnas, mis sisaldab teie tootmiskeskkonnaga joondatud representatiivset andmekogumit.
- Sihtkeskkond tuleb värskendada versioonile Project Service Automation Update Release 37 (V3.10.58.120) või uuemale versioonile.
- Ülesandeid (msdyn_projecttask) sisaldavaid keskkondi toetatakse ainult siis, kui ülesannete koguarv projekti kohta on 500 või vähem.

3. etapi eeltingimusi ajakohastatakse üldise saadavuse kuupäeva lähenedes.

## <a name="licensing"></a>Litsentsimine

Kui teil on Project Service Automationi aktiivsed litsentsid, saate installida ja kasutada Project Operationsit, mis hõlmab kõiki Project Service Automationi võimalusi ja palju muud. Seejärel saate testida Project Operationsi võimalusi eraldi keskkonnas, samal ajal kui jätkate Project Service Automationi kasutamist tootmises. Pärast Project Service Automationi litsentside aegumist peate üle minema Project Operationsile. Selle ülemineku kavandamisel peate arvestama asjaoluga, et Project Operationsi litsents ei sisalda Project Service Automationi litsentsi.

## <a name="testing-and-refactoring-customizations"></a>Kohanduste testimine ja refactoring

Alustuseks importige kõik kohandused puhtasse Project Operationsi (Lite) keskkonda, et kinnitada, et importimine on edukas ja et äritegevus käitub ootuspäraselt.

Siin on mõned asjad, millele tähelepanu pöörata:

- Importimine võib nurjuda puuduvate sõltuvuste tõttu. Teisisõnu, kohanduste viiteväljad või muud komponendid, mis on Project Operationsist eemaldatud. Sel juhul eemaldage need sõltuvused arenduskeskkonnast.
- Kui teie mittehallatavad ja hallatavad lahendused sisaldavad komponente, mis pole kohandatud, eemaldage need komponendid lahendusest. Näiteks kui kohandate **olemit Projekt**, lisage lahendusele ainult olemi päis. Ärge lisage kõiki välju. Kui olete varem kõik alamkomponendid lisanud, peate võib-olla käsitsi looma uue lahenduse ja lisama sellele asjakohased komponendid.
- Vormid ja vaated ei pruugi ilmuda ootuspäraselt. Mõnel juhul, kui olete kohandanud mõnda valmisvormi või vaadet, võivad kohandused takistada Project Operationsi uute värskenduste jõustumist. Nende probleemide tuvastamiseks soovitame teil vaadata kõrvuti üle Project Operationsi puhas install ja teie kohandusi sisaldava Project Operationsi installi. Võrrelge oma ettevõttes kõige sagedamini kasutatavaid vorme veendumaks, et vormi versioon on endiselt mõistlik ega puudu vormi puhtast versioonist. Tehke sama tüüpi kõrvuti läbivaatust kõigi kohandatud vaadete kohta.
- Äriloogika võib käitusajal ebaõnnestuda. Kuna lisandmoodulite väljade viiteid importimise ajal ei valideerita, võib äriloogika nurjuda viidete tõttu väljadele, mida enam ei eksisteeri, ja võidakse kuvada tõrketeade, mis sarnaneb järgmise näitega: "’Projekti" olem ei sisalda atribuuti nimega = ’msdyn_plannedhours’ ja NameMapping = ’Loogiline’." Sellisel juhul muutke oma kohandusi nii, et need kasutaksid uusi välju. Kui kasutate lisandmooduli loogikas automaatselt loodud puhverserveriklasse ja tugeva tüübi viiteid, kaaluge nende puhverserverite taastamist puhtast installist. Sel viisil saate hõlpsasti tuvastada kõik kohad, kus teie lisandmoodulid sõltuvad aegunud väljadest.

Pärast kohanduste värskendamist projektitoimingute puhtaks importimiseks jätkake järgmiste juhistega.

## <a name="end-to-end-testing-in-development-environments"></a>Otsast lõpuni testimine arenduskeskkondades

### <a name="initiate-upgrade"></a>Versioonitäienduse algatamine 

1. Power Platform Otsige halduskeskuses üles ja valige oma keskkond. Seejärel leidke ja valige **Dynamics 365 Project Operations** rakendustes.
2. Versioonitäienduse alustamiseks valige **Installi**. Halduskeskus Power Platform esitleb seda installi uue installina. Siiski tuvastatakse Project Service Automationi varasema versiooni olemasolu ja olemasolevat installi täiendatakse.

    Pärast täiendamise lõpuleviimist peaks keskkond näitama, et Project Operations on installitud ja Project Service Automation pole installitud.

    Sõltuvalt keskkonnas olevate andmete hulgast võib versiooniuuendus võtta mitu tundi. Põhimeeskond, kes versioonitäiendust haldab, peaks vastavalt planeerima ja käitama versioonitäiendust töövälisel ajal. Mõnel juhul, kui andmemaht on suur, tuleks versiooniuuendus käivitada nädalavahetusel. Otsus ajastamise kohta peaks põhinema testimistulemustel madalamates keskkondades.

3. Täiendage kohandatud lahendusi vastavalt vajadusele. Sel hetkel juurutage kõik muudatused, mida olete oma kohandustes [teinud, selle artikli jaotises Kohanduste](#testing-and-refactoring-customizations) testimine ja refactoring.
4. Avage jaotis **Sätete** \> **lahendused** ja valige lahendusest **Project Operations Deprecated Components** desinstallimine.

    See lahendus on ajutine lahendus, mis hoiab olemasolevat andmemudelit ja komponente, mis on versiooniuuenduse ajal olemas. Selle lahenduse eemaldamisega eemaldate kõik väljad ja komponendid, mida enam ei kasutata. Sel viisil aitate liidest lihtsustada ning muuta integreerimise ja laiendamise lihtsamaks.
    
### <a name="upgrade-to-project-operations-lite"></a>Üleminek versioonile Project Operations Lite

Järgmised sammud kirjeldavad täiendusprotsessi ja sellega seotud tõrkelogimist.

1. **PSA versiooni kontroll:** Project Operationsi installimiseks peab teil olema V3.10.58.120 või uuem.
1. **Eelvalideerimine:** kui administraator algatab versioonitäienduse, käivitab süsteem iga olemi, mis on Project Operationsi lahenduse tuum, valideerimiseelse toimingu. See etapp kontrollib, kas kõik olemiviited on kehtivad, ja tagab, et WBS-iga seotud andmed jäävad Project for the Web avaldatud piiridesse.
1. **Metaandmete täiendamine:** pärast edukat eelvalideerimist algatab süsteem skeemi muudatused ja loob aegunud komponentide lahenduse. Saate selle aegunud lahenduse eemaldada pärast seda, kui olete kõik vajalikud kohandused ümber kujundanud. See samm on täiendusprotsessi pikim osa ja selle läbimiseks võib kuluda kuni neli tundi.
1. **Andmete täiendamine:** kui kõik vajalikud skeemimuudatused on metaandmete täiendamise etapis lõpule viidud, migreeritakse teie andmed uuele skeemile ning kõik vajalikud vaikeväärtused ja ümberarvutused on tehtud.
1. **Projekti ajakava mootori värskendus:** pärast edukat andmete täiendamist **märgistatakse avalehe vahekaart Ajakava** ümber **Ülesanded**. Kui kasutaja valib pärast versioonitäiendust selle vahekaardi, suunatakse ta WBS-i kirjutuskaitstud versiooni vaatamiseks navigeerima jälgimisruudustikku. WBS-i redigeerimiseks peavad nad algatama ajakava [teisendamise protsessi](/PSA-Upgrade-Project-Conversion.md). Kõik projektid, millel pole varem olemasolevat WBS-i, saavad uut plaanimiskogemust kasutada otse, ilma teisendamiseta.
 
### <a name="validate-common-scenarios"></a>Levinud stsenaariumide valideerimine

Konkreetsete kohanduste valideerimisel soovitame teil üle vaadata ka äriprotsessid, mida rakendustes toetatakse. Need äriprotsessid hõlmavad muu hulgas müügiüksuste, näiteks noteeringute ja lepingute loomist ning WBS-e sisaldavate projektide loomist ja tegelike tulemuste kinnitamist.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Suuremad muudatused Project Service Automationi ja Project Operationsi vahel

Selles jaotises on kokkuvõte peamistest muudatustest, mida võite Project Service Automationi ja Project Operationsi vahel oodata.

### <a name="project-planning"></a>Projekti kavandamine

Project Operationsi projekti plaanimise võimalused ei tugine enam kliendipoolsele loogikale ja serveripoolsele loogikale. Selle asemel kasutab Project Operations plaanimismootorina rakendust Project for the Web (Projecti veebirakendus). See plaanimisvõimaluste muudatus võimaldab mitmeid uusi funktsioone, nagu juhatuse ja Gantti vaated, ressursipõhine planeerimine, [ülesande kontroll-loendi üksused ja projekti plaanimisrežiimid](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Uusi plaanimisvõimalusi toetab ka rikkalik komplekt uusi [rakendusliideseid (API-sid).](../project-management/schedule-api-preview.md) Nende API-de eesmärk on aidata tagada, et ükski WBS-is olemi loomise, värskendamise või kustutamise programmiline toiming ei rikuks graafiku arvutatud välju.

### <a name="billing-and-pricing"></a>Arveldamine ja hinnakujundus

Osana jätkuvatest investeeringutest Project Operationsisse on arvelduse ja hinnakujunduse valdkonnas saadaval mitu uut võimalust. Järgmiselt on toodud mõned näited.

- [Materjalikasutuse salvestamine projektides ja projektiülesannetes](../material/material-usage-log.md)
- [Alltöövõtu haldamine](../pro/subcontracting/managing-subcontracts-overview.md)
- [Ettemaksud või honoraril põhinevad lepingud](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Lepingu staatus ja valideerimine](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Ülesandepõhine arveldamine

### <a name="resource-management"></a>Ressursihaldus

Project Operations pakub valikulist tuge (URS) tahvlile Universal Resource Scheduling ja plaanimisassistendile. See uus kogemus muutub kohustuslikuks 2023. aasta aprilli laines.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Milliseid juurutustüüpe praegu versioonitäienduseks toetatakse?

| Lähtekeel                                                 | Sihtkeel                                                    | Olek                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Projekti operatsioonide Lite juurutamine                        | Toetatud               |
| Dynamics 365 Finance Projektijuhtimine ja raamatupidamine | Projekti operatsioonide Lite juurutamine                        | Pole praegu toetatud |
| Finantseerige projektijuhtimist ja raamatupidamist              | Project Operations ressursi/mitteaktsia stsenaariumite jaoks     | Pole praegu toetatud |
| Project Service Automation 3.x                         | Project Operations ressursi/mitteaktsia stsenaariumite jaoks     | Pole praegu toetatud |
| Veebiprojekt (spetsiaalne keskkond)            | Projekti operatsioonide Lite juurutamine                        | Pole praegu toetatud |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kuidas installida Project Operationsi enne, kui versioonitäiendustööriistad on saadaval?

Project Operationsi installimiseks enne versioonitäiendustööriistade saadasaamist on kaks võimalust.

- Uue keskkonna pakkumine.
- Juurutage Project Operations eraldi mis tahes müügiorganisatsioonis, kus Project Service Automationit pole.

Kui Project Service Automation on organisatsiooni installitud, kuid seda ei kasutatud, saab selle desinstallida. Pärast Project Service Automationi täielikku eemaldamist saab Project Operationsi installida samasse organisatsiooni.
