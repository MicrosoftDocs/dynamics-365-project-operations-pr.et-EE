---
title: Mis on uut septembris 2021 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: Selles teemas kirjeldatakse kvaliteedivärskendusi, mis on saadaval ressursipõhiste/mittelaopõhiste stsenaariumite jaoks mõeldud Project Operationsi 2021. aasta septembri väljalaskes.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 842ea95892fa4f7a29a778cfd2c33a66e84f676c
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547149"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut septembris 2021 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

*Kehtib: ressursipõhiste/mitteladustatavate stsenaariumite jaoks*

See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.

   - Project Operations Microsoft Dataverse’i keskkonna versioonis 4.14.0.99.
   - Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Selles väljaandes ei ole Project Operationsi topeltkirjutuse kaartide jaoks värskendusi. Project Operationsi topeltkijrutusega kaartide praeguse loendi ja versioonide jaoks vaadake teemat [Project Operationsi topeltkirjutamise kaardi versioonid](../environment/resource-dual-write-maps.md).

Käitage oma keskkonnas alati kaardi uusimat versiooni ja lubage kõik seotud tabelikaardid oma Project Operationsi lahenduse Dataverse ja Finance versiooni värskendamisel. Kui kaardi uusim versioon pole aktiveeritud, ei pruugi teatud funktsioonid ja võimalused õigesti töötada. Kaardi aktiivset versiooni saate vaadata lehe **Topeltkirjutamine** veerus **Versioon**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kasutusvalmis tabelikaardi, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui kaardi käivitamisel ilmneb probleeme, järgige topeltkirjutuse tõrkeotsingu juhise jaotises [Puuduvate tabeli veergude probleem vastendustes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) toodud juhiseid.

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| Aeg ja kulu | 1811407 | Muudetud on projekti kinnitaja turberolli kulukirjete kinnitamiseks. |
| Aeg ja kulu | 1811438 | Muudetud on projekti kinnitaja turberolli ajakirjete kinnituse tühistamiseks. |
| Aeg ja kulu | 2370126 | Uuendatud on ikoone **Projektiülesanne** ja **Roll** olemis **Ajakirje**. |
| Aeg ja kulu | 2379879 | Parandati ajakirje funktsiooni **Kopeeri nädal** telefoni jaoks mõeldud rakenduse Dynamics 365 kasutamisel. |
| Arveldamine ja hinnakujundus | 2371906 | Näidisarve kogusumma ei tohi ressursipõhiste juurutuste Project Operationsis olla muudetav. |
| Arveldamine ja hinnakujundus | 2385802 | Lahendatud on tõrge, mis ilmneb projekti kogusummade värskendamisel negatiivsete tegelike tundide korral. |
| Arveldamine ja hinnakujundus | 2389675 | Täiustatud näidisarve kinnitamise käitumine. Pikkade töötööde olem peab arvestama tegevusega, mida on vaja raamatupidamisandmete kinnitamise tulemuste sisestamiseks. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektihaldus ja raamatupidamine rakenduses Dynamics 365 Finance

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Reisimine ja kulu | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Hankija ja käibemaksu kannetes olevad summad, mis sisestatakse krediitkaarditehingust loodud kulust, on valed. |
| Reisimine ja kulu | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Makse töölehe genereerimisel luuakse valed tasakaalustamise read. |
| Reisimine ja kulu | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Käibemaksu kannetes olevad summad, mis sisestatakse krediitkaarditehingust loodud kulust, on valed. |
| Reisimine ja kulu | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Kulurea kustutamine võib võtta kaua aega. |
| Projekti raamatupidamine | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Pärast teabebaasi artikli 4619395 rakendamist ei toetata numbrijada muutmist valikule **Pidev** ja kui sisestate prognoosi, esineb järgmine tõrge: „Süsteem ei toeta Proj_X numbrijärjestuse seadmist pidevale“. |
| Projekti raamatupidamine | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Hankija arve sisestamine võib nurjuda järgmise tõrketeatega: „Vautšerite tehinguid ei tasakaalustata kui 5/17/2021. (raamatupidamisvaluuta: 0.00 – aruandlusvaluuta: 0.01)“. |
