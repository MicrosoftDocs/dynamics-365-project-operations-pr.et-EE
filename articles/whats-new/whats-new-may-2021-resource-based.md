---
title: Mis on uut mais 2021 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: See teema annab teavet Project Operationsi ressursipõhiste/mittelaopõhiste stsenaariumite jaoks 2021. a mai väljalaskes saadaolevate kvaliteedivärskenduste kohta.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26d4d9feb386075fec2b5c0854e0762604a74d36c90068e35d351e52d95165d4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994676"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut mais 2021 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.

- Project Operations rakenduse Dynamics 365 Dataverse keskkonna versioonis 4.10.0.186
- Projektijuhtimine ja raamatupidamine Finance and Operationsi rakenduste keskkondade versioonis 10.0.18

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

Selles väljaandes sisalduvad järgmised funktsioonid.

- [Ajastamisrežiimid](../project-management/scheduling-modes.md): projektijuhid saavad määratleda, kas projekti tuleks hallata fikseeritud kestuse, fikseeritud töö või fikseeritud ühikute ajastamisrežiimis.
- [Läbisõidu seadistamine läbisõidu määra astmeid kasutades](../expense/set-up-mileage.md): saate värskendada töötaja kuluaruannete läbisõidu määra astmed.

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Järgmises loendis on näidatud Project Operationsi 2021. aasta mais väljalaskes muudetud või lisatud topeltkirjutuse kaarti.

| Olemikaart | Värskendatud versioon | Kommentaarid |
| --- | --- | --- |
| Projekti rahastamisallikas (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Projektilepingu kliendi maksetingimuste sünkroonimine. |
| Projektiarve ettepanek V2 (arved) | 1.0.0.3 | Näidisarve maksetingimuste sünkroonimine. |
| Project Operationsi integratsiooni projekti hankija arve ekspordirea olem (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Kvaliteedi värskendused |
| Projektid V2 (msdyn\_projects) | 1.0.0.2 | Kvaliteedi värskendused |

Käitage oma keskkonnas alati kaardi uusimat versiooni ja lubage oma Project Operationsi Dataverse’i lahenduse ja Finance and Operationsi rakenduste lahenduse versiooni värskendamisel kõik seotud tabelivastendused. Kui kaardi uusim versioon pole aktiveeritud, ei pruugi teatud funktsioonid ja võimalused õigesti töötada. Kaardi aktiivset versiooni saate vaadata veerus **Versioon**, mis asub lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kasutusvalmis tabelikaardi, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management.md)

Kui teil tekib kaardi käivitamisel probleeme, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises [Probleem kaardilt puuduvate tabeli veergudega](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2227635 | Väljadel **Ühikurühm** ja **Ühik** olevad väärtused pärinevad vaikimisi toote ruudustikust **Materjalid**. |
| Arveldamine ja hinnakujundus | 2234127 | Väli **Ülesande ID** on nüüd Dataverse’i projekti tegelike näitajatega õigesti integreeritud, kui hankija arve sisestatakse. |
| Arveldamine ja hinnakujundus | 2235564 | Töölehe rea salvestamine tagab, et töölehe rea kirjel kuvatud valuuta ühtiks pärast salvestamist rea vaikevaluutaga. |
| Arveldamine ja hinnakujundus | 2246671 | Tehingu arveldamise ajal mittearveldustavaks muutmine tühistab algse arveldamata müügikirje ja loob uue arveldamata müügikirje mittearveldatavana. |
| Arveldamine ja hinnakujundus | 2264042 | Kui leidub arve paranduse üksikasi, mis keskkonnas ei kehti, ei tohi kehtivat arve parandust blokeerida. |
| Arveldamine ja hinnakujundus | 2146367 | Projekti arve päise topeltkirjutuse vastendust on laiendatud hõlmama maksetingimusi. |
|   Müügivõimaluste haldus | 2086888 | Ärge lisage rolle ega kategooriaid, mis on inaktiveeritud enne hinnapakkumise kopeerimist äsja kopeeritud hinnapakkumise tasustavatele rollidele ja kategooriatele. |
|   Müügivõimaluste haldus | 2234376 | Kirjutuskaitstud väljad on ruudustikus **Materjalide prognoosid** hallid. |
|   Müügivõimaluste haldus | 2238337 | Kontaktil põhineva hinnapakkumise saab salvestada isegi juhul, kui see pole seostatud projekti hinnakirjaga. |
|   Müügivõimaluste haldus | 2239810 | Hinnapakkumise kaotatult sulgemisel suletakse ka seostatud projekt ja tühistatakse kõik broneeringud. |
| Projekti plaanimine ja jälgimine | 2099559 | Lisanud süsteemi seisundi jaoks täiendavad valideerimised enne ruudustiku **Projekti ülesanded** avanemist. |
| Projekti plaanimine ja jälgimine | 2178987 | Lahendatud on ajutine tõrge, mis ilmneb siis, kui valite lehel **Projekt** suvandi **Järgmine etapp**. |
| Ressursihaldus | 2224817 | Funktsioon, mille abil on võimalik laiendada broneeringute vaikeolekud õigele broneeringule. |
| Ajakirje | 2202476 | Leht **Ajakirje** kasutab nüüd reageerimisruudustiku juhtelementi ja lahendab probleeme, nagu ruudustiku vastuolu. |
| Ajakirje | 2223377 | Ajakirje peidetakse jaotisest **Seotud** lehel **Broneeritav ressurss**, et vältida kasutatavusega segamini ajamist. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektihaldus ja raamatupidamine rakenduses Dynamics 365 Finance

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Projektihaldus ja raamatupidamine | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Ressursipõhiste stsenaariumite jaoks mõeldud Project Operations: hinnapakkumist ei saa integreerimisvea tüttu võidetuks teisendada. |
| Projektihaldus ja raamatupidamine | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: kuvatakse lepinguridade ja tehingutüüpide kattuvuse kontrolli tõttu lepingurea projekti ID-ga seostamise proovimisel tõrge. |
| Projektihaldus ja raamatupidamine | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | Olem **ProjCDSProjectContractEntity** määrab rahastamisallika arve aadressi erinevalt kliendilt. |
| Reisimine ja kulu | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Esineda võib kirjendamise tõrge, mis on seotud läbisõidu häälestamisega. |
| Reisimine ja kulu | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Funktsioon **Jaota isiklikuks** ei tööta välisvaluuta kulukannetes. |
| Reisimine ja kulu | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Kulukategooria ripploendi väärtused kuvavad delegaatide jaoks valed kategooriad, olenemata sellest, kas nad on ressursiks. |
| Reisimine ja kulu | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Ressurssidevahelise kuluaruannet ei saa tõrke **Ressursi/kategooria valideerimine** tõttu salvestada. |
| Reisimine ja kulu | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Kuluaruande sisestamisel on vale tasumäära arvutus tükeldatud ridadega. |
| Reisimine ja kulu | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Ettevõttesisest kuluaruannet ei saa sisestada, kui käibemaks on lisatud ja makseviisiks nihke kontotüübiks on **Töötaja**. |
| Reisimine ja kulu | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Andmeolemi **TrvRequisitionLine** ja seostatud ainulaadse registri tagasipööramine on seotud. |
| Reisimine ja kulu | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Kuluaruanne toetab lähtedokumendi rea loomist ja värskendamist. |
| Reisimine ja kulu | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Kui käibemaks kirjendatakse sihtkoha juriidilises olemis, kuvatakse vale alammooduli tööleht. |
| Reisimine ja kulu | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: kuluprognoosu ei kustutata rakendusest Finance, kui see on Dataverse’ist kustutatakse. |
| Reisimine ja kulu | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Kui kulukategooria on mitte projektipõhisest kategooriast, ei kopeerita lehel **Kulud** valitud finantsdimensioone kuluaruandesse. |
