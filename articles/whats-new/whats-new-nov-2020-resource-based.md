---
title: Mis on uut novembris 2020 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: See teema sisaldab teavet ressursi-/mittelaopõhiste stsenaariumite jaoks mõeldud rakenduse Project Operations 2020. aasta novembri väljalaskes saadaolevate kvaliteedi värskenduste kohta.
author: sigitac
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa6530a0eefb1ae6a84a662c6131182d97d49aeb
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950934"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut novembris 2020 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.

- Project Operations CDS-i keskkonna versioonis 4.4.0.70
- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Rakenduse Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks värskendused

### <a name="project-operations-on-cds"></a>Project Operations CDS-is

| Funktsiooni ala                 | Viitenumber | Kvaliteedi värskendus                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Müügivõimaluste haldus       | 2036993          | Prognoosi rida ja ressursi määramise pelinguread on võidetud hinnapakkumistel värskendatud, kui hinnapakkumise rea tüüp on **Kõik ülesanded**.                                                 |
| Arveldamine ja hinnakujundus          | 2070392          | Arve projekti lepinguread suurenevad iga kord, kui valitakse suvand **Värskenda arve tehinguid**.                                                                         |
| Projekti kavandamine             | 2043336          | Projektimeeskonna liikme kirjet ei saa kustutada.                                                                                                                                  |
| Projekti kavandamine             | 2046013          | Vastuoluline prognooside sildi veergude käitumine laadimise vs. ajafaasi tüüpi muutuse ajal.                                                                                   |
| Projekti kavandamine             | 2046647          | Algus- ja lõpuajad on tunni võrra paigast ära, kui ressursinõuded luuakse projektimeeskonna liikmetest.                                                                      |
| Projekti kavandamine             | 2053879          | (Iga eelseisva CDS-i väljastamise kohta) PublishUnassignedAssignments katkestab ülesande salvestamise proovimise vea „ConditionOperator.In-i jaoks edastatud väärtus on tühi” korral.                       |
| Projekti kavandamine             | 2055501          | Suvandi **Projekti alguskuupäev** tühjaks jätmine põhjustab ajakava tõrget.                                                                                                      |
| Projekti kavandamine             | 2066817          | Vahekaardi **Ülesanded** inimeste valijat kasutades ei saa luua üldist ressurssi.                                                                                                   |
| Projekti kavandamine             | 2067034          | Nupp **Kuva üksikasjad** pole lehel **Ülesande üksikasjad** saadaval.                                                                                                       |
| Ressursihaldus          | 2046667          | Üldisi meeskonnaliikmeid ei kustutata isegi pärast kõikide ressursside täitmist.                                                                                                    |
| Aja- ja kiirsisestuse kirje | 2047499          | Ajakirje lehe nupp **Uus** avan lehe **Uus meili signatuur**.                                                                                               |
| Aja- ja kiirsisestuse kirje | 2059859          | Kulukirje loomisel avaneb ootamatu hüpikaken.                                                                                                                         |
| Muu                        | 2044181          | (Ostutellimuse desinstallimine) Kui proovite desinstallida msdyn_ProjectServiceCore_Patch ja msdyn Projektiteenuse põhilahendusi, ilmneb tõrge „Kirje pole saadaval”.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektihaldus ja raamatupidamine rakenduses Dynamics 365 Finance

| Funktsiooni ala        | Viitenumber | Kvaliteedi värskendus                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tulu kajastamine | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Projekti prognoosi lõpetamise protsent, kui leping kasutab välisvaluutat, ja töö edenemisprotsent lõpetamise meetodil on vale.                     |
| Tulu kajastamine | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Lõpetamise meetodi **Tegelik kulu** prognoose ei saa postitada.                                                                                                    |
| Tulu kajastamine | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Kõrvaldamine nurjub kande tasaaalutuse tõttu, kui ettevõtte valuuta ja tehingu valuuta on erinevad.                                              |
| Kuluhaldus  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Mitte-administraatorist kasutajate kulurea veerdgude otsnguväärtused nagu **Projekti ID** ja **Kulukategooria** ei kuva andmekonnektori raami õigesti. |
| Kuluhaldus  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Rea atribuudi vaikeväärtus ei kuva kulukategooriaid.                                                                                                         |
| Kuluhaldus  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Kulu integreerimine peab sisaldama rea atribuuti kuluaruandest.                                                                                             |
| Arveldamine           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Projekti arve ettepanekut ei saa postitada veateate tõttu, mis ütleb, et FD kombinatsioon ei olnud valideeritud.                                                    |
| Arveldamine           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Tehingut ei ole võimalik **arve** üksikasjade lehelt vaadata.                                                                                                              |
| Arveldamine           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Arve ettepaneku ridu ei saa kustutada.                                                                                                                                  |
| Projekti raamatupidamine  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Menüü **Prognoos** üksused ei ole **projektide** loendi lehel nähtavad.                                                                                                   |
| Projekti raamatupidamine  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Suvandit **Projekti väljavõte**   > **Tehingud ja prognoos** ei saa avada.                                                                                                       |
| Projekti raamatupidamine  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Kohandatud raamatupidamine** ei ole arveldatavate projekti tehingute jaoks lubatud.                                                                                                  |
| Projekti raamatupidamine  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Raamatupidamise üksikasju ei kaasata tabelisse **ProjCDSActualsImport**, kui tööleht **Integreerimine** on postitatud.                                                  |
| Projekti raamatupidamine  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Projekti prognoosi kirje on topelt, kui eemaldate ja lisate ressursi määramise seejärel uuesti.                                                                            |
| Projekti raamatupidamine  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Projekti ID lingi valimine ei ava CDS-i süvalingi URL-i.                                                                                                         |
| Projekti raamatupidamine  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Üesannete alguskuupäeva ei ole võimalik CDS-is värskendada.                                                                                                                           |
| Projekti raamatupidamine  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Funktsiooni lubamine, mitu lepingurida ei ole ilma CDS-i integreerimiseta võimalikud.                                                                                   |

### <a name="regulatory-updates"></a>Regulatiivsed uuendused
Lisateavet teenuse Finance and Operations rakenduste regulatiivsete uuenduste kohta vaadake teemast [Regulatiivsed uuendused](/dynamics365/finance/localizations/regulatory-updates). Saate ka LCS-i sisse logida ja vaadata kavandatud regulatiivseid värskendusi, kasutades probleemi otsimise tööriista. Probleemi otsing võimaldab teil otsida riigi, funktsiooni tüübi ja väljalaske põhjal.


[!INCLUDE[footer-include](../includes/footer-banner.md)]