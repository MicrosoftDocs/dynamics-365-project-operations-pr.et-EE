---
title: Mis on uut juunis 2021 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: Selles teemas antakse teavet Project Operationsi 2021. aasta juuni väljaandes olevate kvaliteedivärskenduste kohta ressursipõhiste/mittelaopõhiste stsenaariumite jaoks.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 483992768f8b8a02dd0d56b9479c7d591fa676d1eca41161e68b7cf3f97107af
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003856"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut juunis 2021 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.

- Project Operations Dynamics 365 Dataverse’i keskkonna versioonis 4.11.0.156 või 4.11.0.164.
- Projektihaldus ja raamatupidamine Finance and Operationsi rakenduste keskkondade versioonis 10.0.19.

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

Selles väljaandes sisalduvad järgmised funktsioonid.

- Võimalus kustutada [muutmisstsenaariumite jaoks projekti arve ettepaneku ridu](../invoicing/correct-project-invoice-proposals.md).
- Täpsustatud kuluread kajastavad alamkategooria nimesid kuluaruandes [Ümberkujundatud kuluaruanded – uues funktsioonid](../expense/expense-reports-reimagined.md#new-features).
- Makseviis on uue kulu loomisel saadaval uuel kulupaanil.

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Selles väljaandes ei ole Project Operationsi topeltkirjutuse kaartide jaoks värskendusi. 

Project Operationsi topeltkijrutusega kaartide praeguse loendi ja versioonide jaoks vaadake teemat [Project Operationsi topeltkirjutamise kaardi versioonid](../environment/resource-dual-write-maps.md).

Käitage oma keskkonnas alati kaardi uusimat versiooni ja lubage oma Project Operationsi Dataverse’i lahenduse ja Finance and Operationsi rakenduste lahenduse versiooni värskendamisel kõik seotud tabelivastendused. Kui kaardi uusim versioon pole aktiveeritud, ei pruugi teatud funktsioonid ja võimalused õigesti töötada. Kaardi aktiivset versiooni saate vaadata lehe **Topeltkirjutamine** veerus **Versioon**. Aktiveerige kaardi uus versioon, valides suvandi **Tabelikaardi versioonid**, valides uusima versiooni ja salvestades seejärel valitud versiooni. Kui olete kohandanud kasutusvalmis tabelikaardi, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui kaardi käivitamisel esineb probleem, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises [Probleem kaartidel puuduvate tabeli veergudega](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2281417 | Lahendatud on probleem seoses automaatse arve loomise nurjumisega arve ajakava kaudu. |
| Arveldamine ja hinnakujundus | 2287835 | Täiustatud on arve kinnitamise jõudlust. |
| Müügivõimaluse haldus | 2222555 | Materjalide hinnangute tasutavus tuleb **projekti prognoosist importimise** kasutamisel hinnapakkumise rea üksikasjadesse õigesti kopeerida. |
| Müügivõimaluse haldus | 2223427 | Toimingu **GenerateRetainersFromRetainerScheduleOptions** jaoks on nüüd lubatud kohandamised. |
| Müügivõimaluse haldus | 2277528 | Fikseeritud arvelduse vahe-eesmärgi väärtuse arvutamine mitme kliendiga projekti lepinguridade jaoks. |
| Projekti plaanimine ja jälgimine | 2226110 | Lahendatud on hooti esinev probleem funktsiooniga **Nõude loomine** ruudustikus **Projektimeeskond**. |
| Projekti plaanimine ja jälgimine | 2208109 | Kasutajad ei saa projekti luua ühes valuutas ja seotud ülesandeid teises valuutas. |
| Projekti plaanimine ja jälgimine | 2258228 | Ajakava API-d kasutades olemitega **Ajastamine** muutmiseks lubatud väljade loendit on uuendatud. |
| Projekti plaanimine ja jälgimine | 2293989 | Ruudustikus **Projektiülesanded** tuleb edastada õiged keele ja regiooni seadistused. |
| Ressursihaldus | 2220493 | Lahendatud on ruudustiku **Ülesanne** kasutajakogemus, kus ressursitaotlus märgitakse kiiresti lõpetatuks. |
| Ressursihaldus | 2330496 | Lahendatud on **ajakavapaneeli** laadimise probleem. (Kvaliteedivärskendus on saadaval versioonis 4.11.0.164) |
| Aeg ja kulu | 2194431 | Ruudustik **Ajakirje** peab arvestama algusnädalat, mis on määratud **süsteemi sätetes**. |
| Aeg ja kulu | 2277311 | Pärast ruudustikus **Ajakirje** lahtris väärtuse kustutamist jääb kursor ruusustikku. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektihaldus ja raamatupidamine rakenduses Dynamics 365 Finance

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Projektihaldus ja raamatupidamine | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Vormi märkmed** ja **Vormi seadistus** ei ole **projektihalduse häälestuses** rakenduse Finance juriidilistes olemites nähtavad, mis on teenusega Project Operations integreeritud. |
| Projektihaldus ja raamatupidamine | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Vaikimisi kirjeldus on käibemaksu jaoks tühi, kui **Kirjendamise tüüp** = **Müügimaks** projekti arve vautšerite jaoks. |
| Projektihaldus ja raamatupidamine | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Kui Dataverse’is koos Project Operationsi integratsiooniga kasutatakse ülesandepõhist arveldamist, kirjendatakse tehingud topelt. |
| Projektihaldus ja raamatupidamine | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Project Operationsi integratsiooni kasutamisel on tulu tuvastamise lõpetamise protsent vale. |
| Projektihaldus ja raamatupidamine | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Tulu laekumine on Project Operatsisi integreeritud stsenaariumis ootel hankija arvel topelt. |
| Projektihaldus ja raamatupidamine | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Integratsiooni töölehte ei saa kirjendada, kui tuluprofiiliks on määratud seadistus **Rühm**. |
| Projektihaldus ja raamatupidamine | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Ostuarvet ei saa kirjendada projektitellimuste suhtes, mille ridadel on mitu mõõtühikut. |
| Projektihaldus ja raamatupidamine | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Projekti vaikimisi finantsprognoosi ei saa värskendada kasutades projektide andmeolemit **V2**. |
| Projektihaldus ja raamatupidamine | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Projekti prognoosi loomise partiiprotsessi lõpetamine võtab liiga kaua aega. |
| Projektihaldus ja raamatupidamine | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Lepingu kustutamine kustutab ka kliendiga seotud aadressi. |
| Reisimine ja kulu | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Kuluaruande kinnitamise töövootingimust ei hinnata õigesti. |
| Reisimine ja kulu | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Kuluaruande poliitika ei hinda projekti ID-d õigesti. |
| Reisimine ja kulu | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Toiming **Tükelda kontsernisisesed kulutehingud isiklikeks** ei tööta õigesti. |
| Reisimine ja kulu | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Teatudreisitellimuste kustutamisel kuluaruande rea selgitused kustutatakse kogemata. See esineb siis, kui kuluaruande recID ja reisitellimus on samad. |
| Reisimine ja kulu | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Kulu mobiilirakendusega esineb probleem, kui väli **Projekti ID** on kuluaruande poliitikate poolt nõutav. |
| Reisimine ja kulu | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Projektiga seostatud kontsernisiseseid kulusid ei saa redigeerida. Selle asemel kuvatakse järgmine tõrketeade: „Objekti viide pole objekti eksemplarile määratud”. |
| Reisimine ja kulu | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Pärast kuluaruande kirjendamist loetletakse panga alampearaamatus vale valuuta ja summa. |
| Reisimine ja kulu | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Täiustati funktsiooni *Kustuta krediitkaarditehingud*.  |
| Reisimine ja kulu | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Kuluaruandes sisalduvat käibemaksu ei arvutata järjepidevalt, kui juriidilises olemis on määratletud erinev aruandlusvaluuta. |
| Reisimine ja kulu | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Uue sularahas reisikulu lisamisel on jõudlus mõjutatud. |
| Reisimine ja kulu | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Kulupoliitika reegleid ei käivitata kuluaruandes. |
| Reisimine ja kulu | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Uue ühiskategooria andmehalduse raamistiku abil üleslaadimine eemaldab kõigi ühiskategooriate kõik alamkategooriad. |
| Reisimine ja kulu | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Kulurea ja valitud kategooria loomisel kuvatakse järgmine tõrketeade: „Käibemaksugrupi DOM ja kauba käibemaksugrupi STD kombinatsioon ei kehti”. |
| Reisimine ja kulu | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Kulu mobiilirakenduses on probleeme sünkroonimisega. |
