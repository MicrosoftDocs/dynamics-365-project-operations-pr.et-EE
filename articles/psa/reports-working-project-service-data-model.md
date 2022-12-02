---
title: Project Service Automation andmemudeliga töötamine
description: See artikkel annab teavet andmemudeliga töötamise kohta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 67932eea78048c09f5f836d1330f412466622c6a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926679"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Project Service Automation andmemudeliga töötamine

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Dynamics 365 Project Service Automation laiendab teiste rakenduste olemeid ja tutvustab oma mudeleid teenuses Common Data Service. See artikkel kirjeldab mõningaid olemeid, millega tavalistes PSA aruandluse stsenaariumites kokku puutute.

## <a name="reporting-on-opportunities"></a>Müügivõimaluste aruandlus

Project Service Automation laiendab Dynamics 365 Sales olemit **Müügivõimalus**, lisades välju, mis võimaldavad projektipõhiseid stsenaariume. Neid välju tuvastatakse skeeminime alusel, mille eesliiteks on **msdyn\_**. Üks uus väli, mis on PSA müügivõimaluste aruandluse puhul oluline, on **Tellimuse tüüp**. Kui selle välja väärtuseks on **Tööpõhine**, on müügivõimalus PSA müügivõimalus. Muud olemile lisatud väljad on nt **Lepingut sõlmiv organisatsioon**, mis hõlmab müügivõimalust hoidvat organisatsiooni ja **Kontohaldur**, mis hõlmab selle kontohalduri nime, kes müügivõimaluse eest vastutab.

Olem **Müügivõimaluse rida** hõlmab ka välju, mis on seotud Project Service’iga. Väli **Arveldusmeetod** näitab, kas müügivõimaluse rea eest tuleks tasuda aja- ja materjalikulu või fikseeritud hinna alusel ning väli **Projekt** hõlmab müügivõimalust toetava projekti nime. Muud väljad, mille kohta saate aruandeid luua, hõivavad reaüksuse jaoks kulusid ja kliendi eelarvesummasid.

## <a name="reporting-on-quotes"></a>Hinnapakkumiste aruandlus

PSA laiendab rakenduse Sales olemit **Hinnapakkumine**, lisades projektiga seotud välju. Väli **Tellimuse tüüp** eristab PSA hinnapakkumisi mitte-PSA hinnapakkumistest. Kui selle välja väärtuseks on **Tööpõhine**, on hinnapakkumine PSA hinnapakkumine. Muud väljad, mis võivad PSA hinnapakkumise aruandluse joaks olulised olla, hõlmavad summavälju nagu **Arveldatavad kulud**, **Mittearveldatavad kulud**, **Kogutulu**, **Hinnangud** ja **Eelarve**. Muud kasulikud väljad näitavad, kas hinnapakkumine on tulutoov, kas see täidetakse ajakava kohaselt ja kas see vastab kliendi eelarve ootustele.

PSA laiendab ka rakenduse Sales olemit **Hinnapakkumise rida**. Üks väli, mille PSA lisab, on **Arveldusmeetod**, mis näitab, kuidas hinnapakkumise rea eest arve esitatakse (aja- ja materjalikulu või fikseeritud hind). Muud olemile lisatud väljad hõlmavad seotud projekti, mis toetab hinnapakkumise rida, arveldust, kulusid ja eelarvet.

PSA lisab Dynamics 365 andmemudelisse ka uusi hinnapakkumisega seotud olemeid. Järgmiselt on toodud mõned näited.

- **Hinnapakkumise rea üksikasjad** – see olem sisaldab hinnapakkumise rea projektiprognoosi üksikasju. Sellel on iga hinnapakkumise rea kohta kaks kirjet. Üks kirje talletab hinnapakkumise rea kulusid ja kulude üksikasju ning teine kirje talletab hinnapakkumise rea müügisummasid ja müügi üksikasju.
- **Hinnapakkumise rea arve ajakava** – see olem sisaldab hinnapakkumise rea arvete esitamise ajakava. See ajakava luuakse hinnapakkumise reale määratud arvete esitamise sageduse põhjal.
- **Hinnapakkumise rea vahe-eesmärk** – see olem sisaldab fikseeritud hinnaga hinnapakkumiste ridade arvete esitamise vahe-eesmärke.
- **Hinnapakkumise rea analüüsi jaotus** – see olem sisaldab hinnapakkumise rea finantsandmeid. Need andmed võivad kasuks tulla müügi hinnapakkumiste ja prognoositavate kulusummade esitamisel mitmesuguste dimensioonide alusel.

Muud olemid, mille PSA hinnapakkumistele lisab on **Hinnapakkumise rea projekti hinnakiri**, **Hinnapakkumise rea ressursikategooria** ja **Hinnapakkumise rea kande kategooria**.

![Diagramm, mis näitab hinnapakkumist, hinnapakkumise rida ja projekti seoseid.](media/PS-Reporting-image2.png "Diagramm, mis näitab hinnapakkumist, hinnapakkumise rida ja projekti seost")

## <a name="reporting-on-project-contracts"></a>Projektilepingute aruandlus

PSA laiendab rakenduse Sales olemit **Tellimus**, mida kasutatakse projektilepingute talletamisel. See lisab olulise uue välja, **Tellimuse tüüp**, mis tuvastab lepingu müügitellimuse asemel PSA projekti lepinguna. Kui selle välja väärtuseks on **Tööpõhine**, on tellimus PSA projektileping. Muud uued väljad, mis lisatakse olemile **Tellimus**, hõlmavad kulude, PSA lepingu oleku ja lepingut omava organisatsiooni üksikasju.

PSA laiendab ka olemit **Müügitellimuse rida**. Lisatavate väljade hulgas on väljad, mis hõlmavad arveldamise viisi (aja- ja materjalikulu või fikseeritud hind), kliendi eelarvesummasid ja aluseks olevat projekti.

PSA lisab ka uusi olemeid, mis on mõeldud projektilepingute jaoks. Järgmiselt on toodud mõned näited.

- **Projekti lepingurea üksikasjad** – see olem sisaldab reatasemel andmeid, mis on ümber arvestatud lepingurea summasse. Need võivad olla sama üksikasjalikud kui reaüksused, mis on loodud ülesande tasemel projekti ajakavast.
- **Lepingurea arve ajakava** – see olem sisaldab arvete esitamise ajakava, mis on loodud lepingureale määratud arvete esitamise sageduse põhjal.
- **Lepingu vahe-eesmärk** – see olem sisaldab nende lepinguridade arveldamise vahe-eesmärke, millel on fikseeritud hinnaga arvete esitamise tähtaeg.

Muud olemid, mille PSA lepingutele lisab on **Projekti lepingurea projekti hinnakiri**, **Projekti lepingurea ressursikategooria** ja **Projekti lepingurea kande kategooria**.

![Diagramm, mis näitab tellimust, tellimuse rida ja projekti seoseid.](media/PS-Reporting-image3.png "Diagramm, mis näitab tellimust, tellimuse rida ja projekti seost")

## <a name="reporting-on-projects"></a>Projektide aruandlus

Olem **Projektid** ja sellega seotud olemid on PSA jaoks eksklusiivsed. **Projekt** on kõrgeima taseme olem, mida kasutatakse tegevuste töö ja kulude külje hõivamiseks. Järgneb seotud olemite loend.

- **Projektimeeskonna liige** – see olem sisaldab andmeid projektile määratud broneeritavate ressursside kohta. Need ressursid võivad olla üldised broneeritavad ressursid või need võivad olla nimega broneeritavad ressursid, mille on sisestanud kas projektijuht või mis on loodud projekti ajakavast.
- **Projekti ülesanne** – see olem sisaldab ülesandeid, mis moodustavad projekti plaani või ajakava.
- **Ressursi määramine** – see olem sisaldab broneeritava ressursi ülesande määramist.
- **Ressursinõue** – see olem sisaldab mis tahes üldressursi meeskonnaliikmetele mõeldud nõudeid.
- **Hinnang** ja **Hinnangurida** – nendel olemitel on seos päis/rida ja need sisaldavad projekti kuluhinnanguid. Ülesande prognoose talletatakse olemis **Ressursi prognoos**.

![Diagramm, mis näitab ressursinõude ja projekti seoseid.](media/PS-Reporting-image4.png "Diagramm, mis näitab ressursi nõude ja projekti seost")

## <a name="reporting-on-resources"></a>Ressursside aruandlus

Projektiressursid kasutavad rakendusest Universal Resource Scheduling (URS) pärinevaid olemeid **Broneeritav ressurss**, mis on teiste rakendustega (nt Microsoft Dynamics 365 Field Service) ühiskasutuses. Järgmisena on toodud loend olemitest, mida peate võib-olla projektiressursside aruandluse puhul kasutama.

- **Broneeritav ressurss** – see olem esindab kasutajat, kontakti, üldressurssi, kontot, rühma või varustust, mida projektimeeskonnas kasutatakse.
- **Broneeritava ressursi tunnused** – see olem sisaldab ressursi oskusi, serte või haridust. Tunnustel võivad olla hindamisväärtused, mis on määratletud hindamismudelis.
- **Broneeritava ressursi kategooria** – see olem tähistab broneeritava ressursi rolli.
- **Broneeritava ressursi broneeringud** – see olem tähistab aega, mis on projektides ressursi jaoks broneeritud. Igal broneeringul on nii päise olem kui ka reaolemid ja igal real on olek, mis tähistab broneeringu olekut.

![Diagramm, mis näitab broneeritava ressursi omaduste seoseid.](media/PS-Reporting-image5.png "Diagramm, mis näitab broneeritava ressursi omaduste seoseid")

## <a name="reporting-on-actual-transactions"></a>Tegelike kannete aruandlus

Kui kinnitate ajatabeli või kulu või esitate rakenduses PSA lepingu eest arve, talletatakse äritehing olemis **Tegelik**. See olem võib PSA-s olla peaaegu kõigi finantstegevustega seotud aruannete aluseks. Olem **Tegelik** hõivab ärisündmuse kulu- ja müügikandeid. Samuti hõivab see mitmeid olulisi atribuute.

Kui töötate olemiga **Tegelik**, on oluline mõista, millised kanded on olemisse talletatud ja millal need kanded on talletatud. Siin on toodud tavaline voog ajakirjetega töötamisel (kulukirjete voog on sellega sarnane).

1. Ajakirje salvestamisel ei looda olemis **Tegelik** ühtegi kirjet.
2. Ajakirje esitamisel ei looda olemis **Tegelik** ühtegi kirjet.
3. Ajakirje kinnitamisel luuakse olemis **Tegelik** üks kirje ja samuti saab luua ka teise kirje. Esimene kirje talletab ajakirje kulu. Teine kirje talletab ajakirje arveldamata müügisumma. Teine kirje sõltub sellest, kas projektile on määratud klient, hinnapakkumine või lepingurida.

    | Dokumendi kuupäev | Tehingu tüüp | Tehingu klass | Klient         | Leping   | Ressurss     | Ressursi roll | Arvelduse tüüp | Kogus | Ühiku hind | Summa |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Kulu             | Time              | Alpine Ski House | Alpine CRM | Airi Saar | Projektijuht   | Arveldatav   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Arveldamata müük   | Time              | Alpine Ski House | Alpine CRM | Airi Saar | Projektijuht   | Arveldatav   | 8.0      | 100.00     | 800.00 |

    Need kaks kirjet on eraldiseisvad, kuid seostuvad kirjed. Need pole ei deebetid ega krediidid.

4. Kui projektiga on seotud leping, luuakse ajakirje eest arve esitamisel olemis **Tegelik** veel kaks kirjet. Esmalt luuakse arveldamata müügikirjele negatiivne summa. See kirje põhiliselt tühistab arveldamata müügi. Teiseks luuakse arveldatud müügi kanne. Jällegi on need kirjed eraldiseisvad, kuid seostuvad kirjed, mitte deebetid ega krediidid.

    | Dokumendi kuupäev | Tehingu tüüp | Tehingu klass | Klient         | Leping   | Ressurss     | Ressursi roll | Arvelduse tüüp | Kogus | Ühiku hind | Summa   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Arveldamata müük   | Time              | Alpine Ski House | Alpine CRM | Airi Saar | Projektijuht   | Arveldatav   | - 8.0    | 100.00     | - 800.00 |
    | 2/4/18        | Arveldatud müük     | Time              | Alpine Ski House | Alpine CRM | Airi Saar | Projektijuht   | Arveldatav   | 8.0      | 100.00     | 800.00   |

Olem **Kande päritolu** talletab kirje **Tegelik** päritolu ja olem **Kande seos** talletab kirjega **Tegelik** seotud kirjed. Peale selle sisaldab kirje **Tegelik** viiteid projektile, projekti lepingule (tellimus), broneeritavale ressursile ja kliendile.

![Diagramm, mis näitab kande ühendust, päritolu ja tegelikke seoseid.](media/PS-Reporting-image6.png "Diagramm, mis näitab kande ühendust, päritolu ja tegelikke seoseid")


[!INCLUDE[footer-include](../includes/footer-banner.md)]
