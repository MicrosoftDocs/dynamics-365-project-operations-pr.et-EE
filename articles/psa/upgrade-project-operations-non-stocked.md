---
title: Üleminek projekti teenuse automatiseerimiselt projecti operatsioonidele
description: See teema annab ülevaate protsessist, millelt versioonile üle Microsoft Dynamics 365 Project Service Automation minna Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/05/2022
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
ms.openlocfilehash: 9363fd5a06b6b1ba023961b03228e13a53a82002
ms.sourcegitcommit: 5789766efae1e0cb513ea533e4f9ac1e553158a5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/10/2022
ms.locfileid: "7954290"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Üleminek projekti teenuse automatiseerimiselt projecti operatsioonidele

Meil on hea meel teatada esimesest kolmest etapist, mille uuendamiseks Microsoft Dynamics 365 Project Service Automation versioonile Dynamics 365 Project Operations. See teema annab ülevaate klientidele, kes alustavad seda põnevat teekonda. Tulevased teemad hõlmavad arendaja kaalutlusi ja üksikasju funktsioonide täiustuste kohta. Need mitte ainult ei anna juhiseid, mis aitavad teil project operationsile üleminekuks valmistuda, vaid selgitavad ka seda, mida võite pärast täiendamist oodata.

Täienduse tarneprogramm jagatakse kolme etappi.

| Tarne täiendamine | 1. etapp (jaanuar 2022) | 2. etapp (aprillilaine 2022) | 3. etapp (aprillilaine 2022) |
|------------------|------------------------|---------------------------|---------------------------|
| Projektide puhul puudub sõltuvus tööjaotuse struktuurist | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS praegu toetatavates Project Operationsi piirides | | :heavy_check_mark: | :heavy_check_mark: |
| WBS väljaspool Project Operationsi praegu toetatud piiranguid, sealhulgas projecti töölauakliendi tugi | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Täiendusprotsessi funktsioonid 

Täiendusprotsessi osana oleme saidikaardile lisanud täienduslogid, et administraatorid saaksid tõrkeid kergemini diagnoosida. Lisaks uuele liidesele lisatakse uued valideerimisreeglid, et tagada andmete terviklikkus pärast täiendamist. Täiendusprotsessi lisatakse järgmised valideerimised.

| Valideerimised | 1. etapp (jaanuar 2022) | 2. etapp (aprillilaine 2022) | 3. etapp (aprillilaine 2022) |
|-------------|------------------------|---------------------------|---------------------------|
| WBS kinnitatakse tavaliste andmete terviklikkuse rikkumiste vastu (nt ressursimääramised, mis on seotud sama peamise ülesandega, kuid millel on erinevad emaprojektid). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS kinnitatakse [veebiprojekti teadaolevate piiridega](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS kinnitatakse Projecti töölauakliendi teadaolevate limiitide suhtes. | | :heavy_check_mark: | :heavy_check_mark: |
| Broneeritavaid ressursse ja projektikalendreid hinnatakse tavaliste kokkusobimatute kalendrireeglite erandite alusel. | | :heavy_check_mark: | :heavy_check_mark: |

2. etapis uuendatakse Project Operationsile üle läinud kliendid oma olemasolevad projektid projekti planeerimiseks kirjutuskaitstud kasutuskogemuseks. Selles kirjutuskaitstud kogemuses on kogu WBS jälgimisvõrgus nähtav. WBS-i redigeerimiseks saavad projektijuhid põhiprojektide lehel **valida** **Teisenda**. Seejärel uuendatakse projekti taustaprotsessiga nii, et see toetaks projekti veebiprojekti uut projekti planeerimise kogemust. See etapp sobib klientidele, kellel on projektid, mis sobivad [veebiprojekti teadaolevate piiridega](/project-for-the-web/project-for-the-web-limits-and-boundaries).

3. etapis lisatakse projecti töölauakliendi tugi klientide kasuks, kes soovivad jätkata oma projektide redigeerimist sellest rakendusest. Kui aga olemasolevad projektid teisendatakse veebikogemuse uueks projektiks, keelatakse juurdepääs lisandmoodulile iga teisendatud projekti puhul.

## <a name="prerequisites"></a>eeltingimused

1. etapi täienduse saamiseks peab klient vastama järgmistele kriteeriumidele.

- Sihtkeskkond ei tohi sisaldada **msdyn_projecttask** olemi kirjeid.
- Kehtivad Project Operationsi litsentsid tuleb määrata kõigile kliendi aktiivsetele kasutajatele. 
- Klient peab täiendusprotsessi kinnitama vähemalt ühes tootmisvälises keskkonnas, millel on esinduslik andmekogum, mis on joondatud tootmisandmetega.
- Sihtkeskkond tuleb värskendada project Service Automation Update Release 38 või uuemale versioonile.

2. ja 3. etapi eeltingimusi ajakohastatakse üldiste saadavuskuupäevade lähenedes.

## <a name="licensing"></a>Litsentsimine

Kui teil on aktiivsed litsentsid Project Service Automationi jaoks, saate installida ja kasutada Project Operationsi, mis sisaldab kõiki Project Service Automationi võimalusi ja palju muud. Sel viisil saate testida Project Operationsi võimalusi, kui jätkate projekti teenuse automatiseerimise kasutamist tootmises. Pärast projekti teenuse automatiseerimise litsentside aegumist peate üle minema Project Operationsile. Selle ülemineku kavandamisel peate arvestama asjaoluga, et Project Operationsi litsents ei sisalda Project Service Automationi litsentsi.

## <a name="testing-and-refactoring-customizations"></a>Kohanduste testimine ja ümberesindamine

Lähtepunktina importige kõik kohandused puhtasse Project Operationsi (lite) keskkonda, et kinnitada, et import on edukas ja et äritoimingud käituvad ootuspäraselt.

Siin on mõned asjad, mida tuleb jälgida:

- Importimine võib puuduvate sõltuvuste tõttu nurjuda. Teisisõnu, kohandused viitavad väljadele või muudele komponentidele, mis on Project Operationsis eemaldatud. Sellisel juhul eemaldage need sõltuvused arengukeskkonnast.
- Kui teie mitte hallatud ja hallatavad lahendused sisaldavad komponente, mida pole kohandatud, eemaldage need komponendid lahendusest. Näiteks kui kohandate **olemit** Project, lisage lahendusele ainult olemipäis. Ärge lisage kõiki välju. Kui olete varem lisanud kõik alamkomponendid, peate võib-olla käsitsi looma uue lahenduse ja lisama sellele asjakohased komponendid.
- Vormid ja vaated ei pruugi tunduda ootamatud. Mõnel juhul, kui olete kohandanud mõnda kastivälist vormi või vaadet, võivad kohandused takistada Project Operationsi uute värskenduste jõustumist. Nende probleemide tuvastamiseks soovitame teil teha kõrvuti ülevaade Project Operationsi puhtast installist ja Project Operationsi installimisest, mis sisaldab teie kohandusi. Võrrelge oma ettevõtte kõige sagedamini kasutatavaid vorme, et kinnitada, et vormi versioon on endiselt mõttekas ja vormi puhtast versioonist midagi ei puudu. Tehke kohandatud vaadete puhul sama tüüpi kõrvuti ülevaade.
- Äriloogika võib käitusajal ebaõnnestuda. Kuna viiteid lisandmoodulite väljadele ei kinnitata importimise ajal, võib äriloogika nurjuda viidete tõttu väljadele, mida enam pole, ja võite saada tõrketeate, mis sarnaneb järgmise näitega: olem "Project" pole atribuut nimega = "msdyn_plannedhours" ja Nimemagumine = 'Loogiline'. Sellisel juhul muutke oma kohandusi nii, et need kasutaksid uusi välju. Kui kasutate pistikprogrammi loogikas automaatselt loodud puhverserveriklasse ja tugevaid tüübiviiteid, kaaluge nende puhverserverite taastamist puhtast installist. Sel viisil saate hõlpsasti tuvastada kõik kohad, kus teie lisandmoodulid sõltuvad aegunud väljadest.

Pärast kohanduste värskendamist Project Operationsi puhtaks importimiseks liikuge edasi järgmistele juhistele.

## <a name="end-to-end-testing-in-lower-environments"></a>Otsast otsa testimine madalamates keskkondades

### <a name="run-the-upgrade-in-production"></a>Versioonitäienduse käivitamine tootmises

1. Otsige Power Platform halduskeskuses üles ja valige oma keskkond. Seejärel leidke ja valige rakendustes **Dynamics 365 Project Operations**.
2. **Täienduse** alustamiseks valige Installi. Power Platform Halduskeskus esitleb seda installi uue installina. Siiski tuvastatakse Projekti teenuse automatiseerimise varasema versiooni olemasolu ja olemasolevat installi uuendatakse.

    Pärast versioonitäienduse lõpuleviimist peaks keskkond näitama, et Project Operations on installitud ja projekti teenuse automatiseerimist pole installitud.

    > [!NOTE]
    > Sõltuvalt keskkonnas olevate andmete kogusest võib versioonitäiendus võtta mitu tundi. Põhimeeskond, kes versiooniuuendust haldab, peaks vastavalt planeerima ja käivitama versiooniuuenduse mitte-tööajal. Mõnel juhul, kui andmemaht on suur, tuleks uuendamine käivitada nädalavahetusel. Otsus ajakava kohta peaks põhinema madalamate keskkondade testitulemustel.

3. Vajadusel täiendage kohandatud lahendusi. Siinkohal juurutage kõik kohandustes tehtud muudatused selle [teema jaotises Kohanduste testimine ja ümberesindamine.](#testing-and-refactoring-customizations)
4. Avage **Settings** \> **Solutions** ja valige project **Operationsi aegunud komponentide lahenduse desinstallimine.**

    See lahendus on ajutine lahendus, mis hoiab olemasolevat andmemudelit ja täiendamise ajal esinevaid komponente. Selle lahenduse eemaldamisega eemaldate kõik väljad ja komponendid, mida enam ei kasutata. Sel viisil aitate liidest lihtsustada ning integratsiooni ja laiendamist lihtsamaks muuta.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Suured muudatused projektiteenuste automatiseerimise ja projektitoimingute vahel

Selles jaotises on kokkuvõte suurtest muudatustest, mida võite oodata projekti teenuse automatiseerimise ja projektitoimingute vahel.

### <a name="project-planning"></a>Projekti kavandamine

Project Operationsi projekti planeerimise võimalused ei tugine enam kliendipoolsele loogikale ja serveripoolsele loogikale. Selle asemel kasutab Project Operations project for the Webi, kuna see on plaanimismootor. See plaanimisvõimaluste muutmine võimaldab mitmeid uusi funktsioone( nt tahvli ja Gantti vaated, ressursipõhine planeerimine, [ülesannete kontroll-loendi üksused](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) ja projekti planeerimise režiimid). Uusi sõiduplaanivõimalusi toetavad ka rikkalikud uued [rakendusliidesed (API-d).](../project-management/schedule-api-preview.md) Need API-d on mõeldud tagamaks, et ükski programmiline toiming olemi loomiseks, värskendamiseks või kustutamiseks WBS-is ei riku ajakava arvutatud välju.

## <a name="billing-and-pricing"></a>Arveldamine ja hinnakujundus

Project Operationsi jätkuvate investeeringute osana on arvelduses ja hinnakujunduses saadaval mitu uut võimalusi. Järgmiselt on toodud mõned näited.

- [Materjalikasutuse salvestamine projektidele ja projektiülesannetele](../material/material-usage-log.md)
- [Alltöövõtu haldus](../pro/subcontracting/managing-subcontracts-overview.md)
- [Ettemaksud või honoraril põhinevad lepingud](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Lepingu ületamisstaatus ja valideerimised](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Ülesandepõhine arveldamine

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Milliseid juurutustüüpe praegu täiendamiseks toetatakse?

| Lähtekeel                                                 | Sihtkeel                                                    | Olek                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite juurutamine                        | Toetatud               |
| Dynamics 365 Finance Projektijuhtimine ja raamatupidamine | Project Operations Lite juurutamine                        | Hetkel ei toetata |
| Finantsprojekti juhtimine ja raamatupidamine              | Project Operations ressursi/mitteaktsia stsenaariumite jaoks     | Hetkel ei toetata |
| Finantsprojekti juhtimine ja raamatupidamine              | Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks | Hetkel ei toetata |
| Projekti teenuse automatiseerimine 3.x                         | Project Operations ressursi/mitteaktsia stsenaariumite jaoks     | Hetkel ei toetata |
| Veebiprojekt (spetsiaalne keskkond)            | Project Operations Lite juurutamine                        | Hetkel ei toetata |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kuidas installida Project Operations enne täiendustööriista olemasolu?

Enne täiendustööriista kättesaadavaks installimist on Project Operationsi installimiseks kaks võimalust.

- Uue keskkonna loomine.
- Juurutage Project Operations eraldi mis tahes müügiorganisatsioonis, kus project service automation pole olemas.

> [!NOTE]
> Kui projekti teenuse automatiseerimine on organisatsiooni installitud, kuid seda ei kasutatud, saab selle desinstallida. Pärast Project Service Automationi täielikku eemaldamist saab Project Operationsi installida samasse organisatsiooni.
