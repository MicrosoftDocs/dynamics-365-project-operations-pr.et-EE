---
title: Mis on uut augustis 2021 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: Selles teemas antakse teavet Project Operationsi 2021. aasta augusti väljaandes olevate kvaliteedivärskenduste kohta ressursipõhiste/mittelaopõhiste stsenaariumite jaoks.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26861472d3af20c58b3d01142b834d535cf99715
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501366"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut augustis 2021 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

*Kehtib: ressursipõhiste/mitteladustatavate stsenaariumite jaoks*

See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.

   - Project Operations Microsoft Dataverse’i keskkonna versioonis 4.13.0.152.
   - Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.20.

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

Selles väljaandes sisalduvad järgmised funktsioonid.

- **Kinnitamiskomplektid**: kinnitamiskomplektid rühmitavad aja, kulu või materjalide kasutuse kinnitustaotlused kokku väiksemateks toimingute alamhulkadeks. See rühmitamine võimaldab kindlas järjekorras kinnitusi projekti kaupa töödelda ja võimaldab uusi katseid ning järjestamist. Taotluste rühmitamine parandab kinnitamise töötlemise usaldusväärsust ja jälgitavust suure kinnitute mahu töötlemiseks. Lisateavet leiate teemast [Kinnitamiskomplektid](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Selles väljaandes ei ole Project Operationsi topeltkirjutuse kaartide jaoks värskendusi.

Project Operationsi topeltkijrutusega kaartide praeguse loendi ja versioonide jaoks vaadake teemat [Project Operationsi topeltkirjutamise kaardi versioonid](../environment/resource-dual-write-maps.md).

Käitage oma keskkonnas alati kaardi uusimat versiooni ja lubage kõik seotud tabelikaardid oma Project Operationsi lahenduse Dataverse ja Finance versiooni värskendamisel. Kui kaardi uusim versioon pole aktiveeritud, ei pruugi teatud funktsioonid ja võimalused õigesti töötada. Kaardi aktiivset versiooni saate vaadata lehe **Topeltkirjutamine** veerus **Versioon**. Aktiveerige kaardi uus versioon, valides suvandi **Tabelikaardi versioonid**, valides uusima versiooni ja salvestades seejärel valitud versiooni. Kui olete kohandanud kasutusvalmis tabelikaardi, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui kaardi käivitamisel esineb probleem, järgige jaotises [Probleem kaartidel puuduvate tabeli veergudega](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) topeltkirjutamise tõrkeotsingu juhendis.

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2295625 | Vahe-eesmärgi nimi tuleb kopeerida arve ajakavast arve rea üksikasjadesse. |
| Arveldamine ja hinnakujundus | 2316323 | Ressursipõhiste stsenaariumide korral ei tohiks allahindlus Project Operationsis näidisarvel redigeeritav olla. |
|   Müügivõimaluste haldus | 2338619 | **Müügivõimaluse** ja **Hinnapakkumise** ärireeglid tuleb käivitada ainult lehtedel. |
| Ressursihaldus | 2316523 | Manustatud rolliga ressursinõudest käsu **Saada taotlus** kasutamine ei tohiks kuvada tõrget. |
| Ressursihaldus | 2326885 | Ressursinõude loomine projekti kaudu ei tohiks kuvada tõrget. |
| Aeg ja kulu | 2335584 | Iganenud ülesandevood ajakirjes. |
| Aeg ja kulu | 2336884 | Ajakirje nupp Nupp **Kopeeri nädal** ei tohi toimida rohkem, kui vaid praeguse kasutaja jaoks. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektihaldus ja raamatupidamine rakenduses Dynamics 365 Finance

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Reisimine ja kulu | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Sisestatakse valed hankija tehingu ja käibemaksu tehingu summad, kui kulu luuakse krediitkaarditehingust. |
| Reisimine ja kulu | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Valed tasumised on makse töölehe loomisel loodud read. |
| Reisimine ja kulu | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Sisestatakse valed käibemaksu tehingu summad, kui kulu luuakse krediitkaarditehingust. |
| Reisimine ja kulu | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Kulurea kustutamine võib võtta kaua aega. |
| Projekti raamatupidamine | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Süsteem ei toeta jätkuvat arvude järjestamist prognoosi sisestamisel pärast teabebaasi 4619395 rakendamist. |
| Projekti raamatupidamine | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Hankija arve sisestamine võib nurjuda, andes tõrketeate "Vautšeri tehingud 05.17.2021 kohta ei ole tasakaalus. (raamatupidamisvaluuta: 0.00 – aruandlusvaluuta: 0.01)" |
