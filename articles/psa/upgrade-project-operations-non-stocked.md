---
title: Üleminek rakenduselt Project Service Automation rakendusele Project Operations
description: See artikkel annab ülevaate rakendusest Microsoft Dynamics 365 Project Service Automation rakendusele Dynamics 365 Project Operations ülemineku protsessist.
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
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736661"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Üleminek rakenduselt Project Service Automation rakendusele Project Operations

Meil on hea meel teatada, et rakenduselt Microsoft Dynamics 365 Project Service Automation rakendusele Microsoft Dynamics 365 Project Operations üleminekust teisele etapile kolmest. See artikkel annab ülevaate klientidele, kes on alustamas seda põnevat teekonda. 

Täiendusprogramm jagatakse kolmeks etapiks.

| Täienduse kohaletoimetamine | 1. faas (jaanuar 2022) | 2. faas (november 2022) | 3. faas (aprilli laine, 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Ei sõltu projektide tööjaotuse struktuurist (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS praegu rakenduse Project Operations toetatud piirides | | :heavy_check_mark: | :heavy_check_mark: |
| WBS väljaspool rakenduse Project Operations praegu toetatud piire, sealhulgas Project Desktop Clienti tugi. | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Täiendusprotsessi funktsioonid 

Täiendusprotsessi osana oleme lisanud saidikaardile versioonitäienduse logid, et administraatorid saaksid rikkeid hõlpsamini diagnoosida. Lisaks uuele liidesele lisatakse uued kinnitamisreeglid, et tagada andmete terviklikkus pärast uuendamist. Täiendusprotsessile lisatakse järgmised kinnitused.

| Kinnitused | 1. faas (jaanuar 2022) | 2. faas (november 2022) | 3. faas  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS-i kontrollitakse tavaliste andmete terviklikkuse rikkumiste suhtes (nt ressursside määramised, mis on seotud sama ülemülesandega, kuid millel on erinevad emaprojektid). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS-i kontrollitakse [Project for the Webi teadaolevad piirangud](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS kinnitatakse Project Desktop Clienti teadaolevate piirangute alusel. | |  | :heavy_check_mark: |
| Broneeritavaid ressursse ja projektikalendreid hinnatakse tavaliste ühildumatute kalendrireeglite erandite alusel. | | :heavy_check_mark: | :heavy_check_mark: |

2. faasis täiendatakse rakenduse Project Operations versioonile üle läinud klientide olemasolevad projektid projektide planeerimise jaoks kirjutuskaitstud kasutuskogemuseks. Selles kirjutuskaitstud kasutuskogemuses on jälgimisruudustikus nähtav kogu WBS. WBS-i redigeerimiseks saavad projektijuhid valida projekti avalehel [**Teisenda**](/PSA-Upgrade-Project-Conversion.md). Taustaprotsess värskendab seejärel projekti nii, et see toetaks Project for the Webi uut projekti ajastamise kogemust. See faas sobib klientidele, kellel on projektid, mis mahuvad [Project for the Web teadaolevate piiride](/project-for-the-web/project-for-the-web-limits-and-boundaries).

3. faasis lisatakse Project desktop clienti tugi klientidele, kes soovivad jätkata oma projektide redigeerimist sellest rakendusest. Kui aga olemasolevad projektid teisendatakse uueks Project for the Web kogemuseks, keelatakse juurdepääs lisandmoodulile iga teisendatud projekti jaoks.

## <a name="prerequisites"></a>eeltingimused

Et saada 1. faasi versioonitäiendust, peate vastama järgmistele kriteeriumidele.

- Sihtkeskkond ei tohi sisaldada olemi **msdyn_projecttask** kirjeid.
- Kehtivad rakenduse Project Operations litsentsid peavad olema määratud kõigile aktiivsetele kasutajatele. 
- Peate täiendusprotsessi kinnitama vähemalt ühes tootmisvälises keskkonnas, mis sisaldab tüüpilist andmestikku, mis on joondatud teie tootmiskeskkonnaga.
- Sihtkeskkonda tuleb värskendada Project Service Automationi värskenduse versioonile 37 (V3.10.58.120) või uuemale versioonile.

2. faasi versioonitäienduse saamiseks peate vastama järgmistele kriteeriumidele.

- Kehtivad rakenduse Project Operations litsentsid peavad olema määratud kõigile aktiivsetele kasutajatele. 
- Peate täiendusprotsessi kinnitama vähemalt ühes tootmisvälises keskkonnas, mis sisaldab tüüpilist andmestikku, mis on joondatud teie tootmiskeskkonnaga.
- Sihtkeskkonda tuleb värskendada Project Service Automationi värskenduse versioonile 37 (V3.10.58.120) või uuemale versioonile.
- Ülesandeid (msdyn_projecttask) sisaldavaid keskkondi toetatakse ainult siis, kui ülesannete koguarv projekti kohta on 500 või vähem.

3. faasi eeltingimusi värskendatakse üldise kättesaadavuse kuupäeva lähenedes.

## <a name="licensing"></a>Litsentsimine

Kui teil on Project Service Automationi aktiivsed litsentsid, saate installida ja kasutada rakenduse Project Operations, mis hõlmab kõiki Project Service Automationi võimalusi ja palju muud. Nii saate testida rakenduse Project Operations võimalusi, samal ajal kui jätkate Project Service Automationi kasutamist tootmises. Kui teie Project Service Automationi litsentsid aeguvad, peate üle minema rakendusele Project Operations. Selle ülemineku kavandamisel peate arvestama asjaoluga, et rakenduse Project Operations litsents ei sisalda Project Service Automationi litsentsi. Kliendid, kellel on stsenaariume, kus nad on Project Service Automationi juurutanud ja peavad jätkama oma PSA litsentside kasutamist või neid suurendama, kuni nad plaanivad minna üle rakendusele Project Operations, võivad taotleda ajutisi PSA litsentse, mis põhinevad rakenduse Project Operations ostetud litsentsidel. Ühe rakenduse Project Operations litsentsi kohta väljastatakse üks Project Service Automationi litsents. Ajutisi PSA litsentse saate taotleda selle lingi kaudu: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Kohanduste testimine ja ümberkujundamine

Alustuseks importige kõik kohandused puhtasse Project Operations (Lite) keskkonda, et kinnitada, et importimine on edukas ja äritegevused käituvad ootuspäraselt.

Siin on mõned asjad, millele tähelepanu pöörata.

- Import võib puuduvate sõltuvuste tõttu ebaõnnestuda. Teisisõnu, kohanduste viiteväljad või muud komponendid, mis on rakenduses Project Operations eemaldatud. Sel juhul eemaldage need sõltuvused arenduskeskkonnast.
- Kui teie mittehallatavad ja hallatavad lahendused sisaldavad komponente, mis pole kohandatud, eemaldage need komponendid lahendusest. Näiteks kui kohandate olemit **Projekt**, lisage oma lahendusele ainult olemi päis. Ärge lisage kõiki välju. Kui olete varem lisanud kõik alamkomponendid, peate võibolla käsitsi looma uue lahenduse ja lisama sellele asjakohased komponendid.
- Vormid ja vaated ei pruugi ootuspäraselt kuvada. Mõnel juhul, kui olete kohandanud mõnda valmis vormi või vaadet, võivad kohandused takistada rakenduse Project Operations uute värskenduste jõustumist. Nende probleemide tuvastamiseks soovitame vaadata kõrvuti Project Operationsi puhta installi ja teie kohandusi sisaldava rakenduse Project Operations installi. Võrrelge oma ettevõttes kõige sagedamini kasutatavaid vorme, et veenduda, kas teie vormi versioon on ikka mõistlik ja kas vormi puhtast versioonist pole midagi puudu. Tehke sama tüüpi kõrvuti ülevaatus kõigi kohandatud vaadete jaoks.
- Äriloogika võib käitusajal ebaõnnestuda. Kuna viiteid teie pistikprogrammide väljadele ei kinnitata importimise ajal, võib äriloogika ebaõnnestuda viidete tõttu väljadele, mida enam ei eksisteeri, ja võidakse kuvada tõrketeade, mis sarnaneb järgmise näitega: „'Projekti' olem ei sisalda atribuuti Name = 'msdyn_plannedhours' ja NameMapping = 'Loogiline'.“ Sel juhul muutke oma kohandusi nii, et need kasutaksid uusi välju. Kui kasutate pistikprogrammi loogikas automaatselt genereeritud puhverserveri klasse ja tugevaid tüübiviiteid, kaaluge nende puhverserverite taastamist puhtast installist. Nii saate hõlpsasti tuvastada kõik kohad, kus teie pistikprogrammid sõltuvad aegunud väljadest.

Pärast kohanduste värskendamist, et rakendust Project Operations puhtalt importida, jätkake järgmiste sammudega.

## <a name="end-to-end-testing-in-development-environments"></a>Otsast lõpuni testimine arenduskeskkondades

### <a name="initiate-upgrade"></a>Täienduse käivitamine 

1. Otsige üles ja valige oma keskkond Power Platform halduskeskuses. Seejärel leidke ja valige rakendustes **Dynamics 365 Project Operations**.
2. Täienduse käivitamiseks valige **Installi**. Power Platform halduskeskus esitleb seda installi uue installina. Siiski tuvastatakse Project Service Automationi varasema versiooni olemasolu ja olemasolevat installi värskendatakse.

    Pärast täiendamise lõpetamist peaks keskkond näitama, et Project Operations on installitud ja Project Service Automation pole installitud.

    Olenevalt andmemahust keskkonnas võib värskendamine kesta mitu tundi. Täiendust haldav põhimeeskond peaks vastavalt planeerima ja viima täiendust läbi töövälisel ajal. Mõnel juhul, kui andmemaht on suur, tuleks versioonitäiendus läbi viia nädalavahetusel. Ajastamise otsus peaks põhinema madalamates keskkondades testimise tulemustel.

3. Täiendage kohandatud lahendusi vastavalt vajadusele. Siinkohal juurutage kõik oma kohandustes tehtud muudatused selle artikli jaotises [Kohanduste testimine ja ümberkujundamine](#testing-and-refactoring-customizations).
4. Minge saidile **make.powerapps.com**, valige portaali paremas ülanurgas rippmenüüst oma keskkond, valige vasakpoolsest menüüst **Lahendused**, valige **Project Operationsi iganenud komponendid** lahendust ja **Desinstalli**.

    See lahendus on ajutine lahendus, mis sisaldab versiooniuuenduse ajal olemasolevat andmemudelit ja komponente. Selle lahenduse eemaldamisel eemaldate kõik väljad ja komponendid, mida enam ei kasutata. Sel viisil aitate lihtsustada kasutajaliidest ning lihtsustada integreerimist ja laiendamist.
    
### <a name="upgrade-to-project-operations-lite"></a>Täiendage rakendusele Project Operations Lite

Järgnevad sammud kirjeldavad täiendusprotsessi ja sellega seotud tõrkeprotokollide koostamist:

1. **PSA versiooni kontroll:** Rakenduse Project Operations paigaldamiseks peab teil olema versioon V3.10.58.120 või uuem.
1. **Eelkinnitus:** Kui administraator algatab versiooniuuenduse, käivitab süsteem eelvalideerimise toimingu iga olemi puhul, mis on rakenduse Project Operations lahenduse tuum. See samm kontrollib, kas kõik olemite viited on kehtivad, ja tagab, et WBS-iga seotud andmed jäävad Project for the Webi avaldatud piiridesse.
1. **Metaandmete täiendus:** Pärast edukat eelkinnitamist algatab süsteem skeemi muudatused ja loob aegunud komponentide lahenduse. Saate selle aegunud lahenduse eemaldada pärast seda, kui olete täitnud kõik vajalikud kohandused. See samm on täiendusprotsessi pikim osa ja selle lõpuleviimiseks võib kuluda kuni neli tundi.
1. **Andmete täiendus:** Kui metaandmete täiendamise etapis on kõik nõutavad skeemi muudatused tehtud, migreeritakse teie andmed uude skeemi ning kõik vajalikud vaikesätted ja ümberarvutused tehakse.
1. **Projekti ajastamismootori värskendus** Pärast edukat andmete värskendamist on avalehe vahekaart **Ajakava** ümber märgistatud **Ülesanded**. Kui kasutaja valib pärast täiendamist selle vahekaardi, suunatakse ta WBS-i kirjutuskaitstud versiooni vaatamiseks jälgimisruudustikule navigeerima. WBS-i muutmiseks peavad nad algatama ajakava [konversiooniprotsess](/PSA-Upgrade-Project-Conversion.md). Kõik projektid, millel puudub eelnev WBS, saavad uut ajastamiskogemust kasutada otse ilma teisendamata.
 
### <a name="validate-common-scenarios"></a>Levinud stsenaariumite kinnitamine

Kui valid oma konkreetsed kohandused, soovitame üle vaadata ka äriprotsessid, mida kõik rakendused toetavad. Need äriprotsessid hõlmavad (kuid mitte ainult) müügiüksuste (nt hinnapakkumiste ja lepingute) loomist ning projektide loomist, mis hõlmavad WBS-e ja tegelike näitajate kinnitamist.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Suured muudatused Project Service Automationi ja Project Operationsi vahel

See jaotis annab kokkuvõtte peamistest muudatustest, mida Project Service Automationi ja Project Operationsi vahel oodata võib.

### <a name="project-planning"></a>Projekti kavandamine

Project Operationsi projekti planeerimise võimalused ei tugine enam kliendipoolsele ja serveripoolsele loogikale. Selle asemel kasutab Project Operations oma ajastamismootorina programmi Project for the Web. See ajastamisvõimaluste muudatus võimaldab mitmeid uusi funktsioone, nagu tahvli ja Gantti vaated, ressursipõhine planeerimine, [ülesande kontroll-loendi üksused](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) ja projekti ajastamise režiimid. Uusi ajastamisvõimalusi toetab ka rikkalik komplekt uusi [rakenduse programmeerimisliideseid (API-sid)](../project-management/schedule-api-preview.md). Nende API-de eesmärk on aidata tagada, et ükski WBS-i olemi loomise, värskendamise või kustutamise programmiline toiming ei rikuks ajakava arvutatud välju.

### <a name="billing-and-pricing"></a>Arveldamine ja hinnakujundus

Osana jätkuvatest investeeringutest rakenduses Project Operations on arvelduses ja hinnakujunduses saadaval mitu uut võimalust. Järgmiselt on toodud mõned näited.

- [Projektide ja projektiülesannete materjalikasutuse salvestamine](../material/material-usage-log.md)
- [Allhankelepingu haldus](../pro/subcontracting/managing-subcontracts-overview.md)
- [Ettemaksud või honoraril põhinevad lepingud](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Lepingu mitteületamise olek ja kinnitused](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Ülesandepõhine arveldamine

### <a name="resource-management"></a>Ressursihaldus

Project Operations pakub valikulist tuge Universal Resource Scheduling (URS) tahvlile ja ajastamisabilisele. See uus kogemus muutub kohustuslikuks 2023. aasta aprilli lainel.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Milliseid juurutamise tüüpe praegu täiendatakse?

| Lähtekeel                                                 | Sihtkeel                                                    | Olek                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operationsi lihtjuurutamine                        | Toetatud               |
| Projektihaldus ja raamatupidamine rakenduses Dynamics 365 Finance | Project Operationsi lihtjuurutamine                        | Hetkel ei toetata |
| Finantsprojektide haldus ja raamatupidamine              | Project Operations ressursi/mitteaktsia stsenaariumite jaoks     | Hetkel ei toetata |
| Project Service Automation 3.x                         | Project Operations ressursi/mitteaktsia stsenaariumite jaoks     | Hetkel ei toetata |
| Project for the Web (pühendunud keskkond)            | Project Operationsi lihtjuurutamine                        | Hetkel ei toetata |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kuidas installida Project Operations enne, kui uuendustööriistad on saadaval?

Rakenduse Project Operations installimiseks on kaks võimalust, enne kui uuendustööriistad on saadaval.

- Uue keskkonna ettevalmistamine.
- Juurutage Project Operations eraldi igas müügiorganisatsioonis, kus Project Service Automation puudub.

Kui Project Service Automation on organisatsiooni installitud, kuid seda ei kasutatud, saab selle desinstallida. Pärast Project Service Automationi täielikku eemaldamist saab Project Operationsi installida samasse organisatsiooni.
