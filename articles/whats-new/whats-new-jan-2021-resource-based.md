---
title: Mis on uut jaanuaris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: See teema sisaldab teavet ressursi-/mittelaopõhiste stsenaariumite jaoks mõeldud rakenduse Project Operations 2021. aasta jaanuari väljalaskes saadaolevate kvaliteedi värskenduste kohta.
author: sigitac
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e5bfd3c790dac51895cde04e08d1fa62f4457e8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5292064"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut jaanuaris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_


See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.

  - Project Operations Dataverse’i keskkonna versioonis 4.6.0.154
  - Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.16

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| **Juurutamine ja konfiguratsioon** | 2106818 | Parandatud on veebiressursi ümbernimetamine, mis põhjustas lehe kohandamise probleeme. |
| **Arveldamine ja hinnakujundus** | 2091908 | Parandatud on suvandite **Lukusta hinnakujundus** ja **Kasuta praegust hinnakujundust** nähtavus lehel **Arve**, kui Project Operations on installitud koos rakendusega Dynamics 365 Field Service. |
| **Arveldamine ja hinnakujundus** | 2103058 | Värskendatud on **Projekti kokkuvõtteid**, et need saaksid hakkama tööülesande tegeliku kulu puhul nullväärtustega. |
| **Arveldamine ja hinnakujundus** | 2116100 | Täiustatud on funktsionaalsusega kasutatud tõrketeateid, **Parandage tegelike näitajate kirjed**. |
| **Arveldamine ja hinnakujundus** | 2116129 | Täiustatud kuluprognooside nähtavust vahekaardil **Prognoosid** lehel **Projektid**. |
| **Arveldamine ja hinnakujundus** | 2119112 | Parandatud on tegeliku müügi ja tegeliku kulu koondamine, kui kasutatakse erinevaid vahetuskursse. |
| **Arveldamine ja hinnakujundus** | 2134705 | Parandatud on tõrge "Ei saa lugeda määratlemata atribuuti **getResourceString**, kui leht **Arve** on avatud ja Field Service on installitud. |
| **Müügivõimaluse haldus** | 2022195 | Ülesandepõhine arveldusruudustik lehel **Projekt** sisaldab ikooni, mis näitab, et selle tööülesandega on soetud lepingu või hinnapakkumise rida. |
| **Müügivõimaluse haldus** | 2029135 | Parandatud on äriprotsessi tõrge, mis tekib juhul, kui kasutaja proovib avada kinnitatud arve rida, millel on arveldatud ettemaksu summa. |
| **Müügivõimaluse haldus** | 2040713 | Parandatud on skripti tõrge, mis tekib lepingust arve loomisel kui Field Service on installitud. |
| **Projekti plaanimine ja jälgimine** | 2090202 | Märgitud on ärireeglid, mida ei kasutata enam kui **Iganenuid**. |
| **Aeg ja kulu** | 2091249 | Süvendati kontrolli, et kasutajad ei saaks muuta esitatud või kinnitatud ajakirje tööülesannet. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektihaldus ja raamatupidamine rakenduses Dynamics 365 Finance

| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| **Projektihaldus ja raamatupidamine** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Vale lepingusumma mitme rahastamisallikaga fikseeritud hinnaga projekti lehel **Kontol**. |
| **Projektihaldus ja raamatupidamine** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Kohatäide **Invoiceproposal.PSAnfRefProjId** ei kuvata töövoo **Projekti arve ettepanekute ülevaatamine** projekti ID-d. |
| **Projektihaldus ja raamatupidamine** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Projekti arve ettepanekute sisestamisel kasutatakse vale rahalise allahindluse kuupäeva. |
| **Projektihaldus ja raamatupidamine** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Ressursi määramise eemaldamine ja lugemine Project Operationsis kahekordistab rakenduses Finance projekti prognoosi kirjeid. |
| **Projektihaldus ja raamatupidamine** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | Project Operationsis ei saa luua projektiprognoose Dataverse'is ilma projekti lepingurida omamata. |
| **Projektihaldus ja raamatupidamine** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Projekti kulutehingu finantsdimensiooni ei sünkroonita seotud kandega ja kuluaruande arvestuse jaotusega, kui kulusid saldosse sisestatakse. |
| **Projektihaldus ja raamatupidamine** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Fikseeritud hinnaga projektide sisestatud projektitehingute filter **Arve olek** ei tööta. |
| **Projektihaldus ja raamatupidamine** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Pöördprognoosi eemaldamine ei tööta jaotises **Perioodiline**. |
| **Projektihaldus ja raamatupidamine** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Arve ettepaneku ridu saab Project Operationsis kustutada, kui see on Dataverse'iga integreeritud. |
| **Projektihaldus ja raamatupidamine** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Takistage mitme lepingurea funktsiooni libamist ilma teenuse Dataverse integreerimiseta. |
| **Projektihaldus ja raamatupidamine** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Kui kontol arveldamine on võrdne kasumi ja kahjumiga, esitatakse arveldatud tulu lehel Prognoosid nullina. |
| **Projektihaldus ja raamatupidamine** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Arve parandused ei tööta integreeritud keskkondades. |
| **Projektihaldus ja raamatupidamine** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | WIP-müügiväärtuse sisestamisel kontsernisisese projekti arveldusele valitakse vale konto. |
| **Projektihaldus ja raamatupidamine** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | Project Operationsis ei saa Dataverse'is prognoositavate ülesannete sõltuvusi värskendada. |
| **Projektihaldus ja raamatupidamine** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Project Operationsi integratsiooni töölehtede korduv kustutamine Finance'is viib andmete kaotamiseni. |
| **Projektihaldus ja raamatupidamine** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Projekti arve ettepaneku sisestamisel ilmneb järgmine tõrge: "Tehing ei ole aruandlusvaluutas tasakaalus, kui lisatakse mahavõetud ettemaksuarve". |
| **Projektihaldus ja raamatupidamine** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Mahaarvamistega kaasatakse pärast projekti vaikelepingu värskendamist Project Operationsis vale projekti ID. |
| **Projektihaldus ja raamatupidamine** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Kui Project Operations on lubatud, ei saa prognoosi ja tulude kajastamist lõpule viia. |
| **Projektihaldus ja raamatupidamine** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Project Operationsis ei lähtesta projekti eemaldamine lepingult lepingu vaikeprojekti. |
| **Projektihaldus ja raamatupidamine** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Project Operationsis kuvatakse kontsernidevahelise arve puhul loendis **Rea lisamine** valed kuluread. |
| **Reisimine ja kulu** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Kuluridu ei saa sisestada, kuna lepingureal puudub tunni seadistamine. |
| **Reisimine ja kulu** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Kui projekti/kategooria kinnitamine on kohustuslik, ei kuvata projektiga seostatud kulukategooriaid kuluaruandes. |
| **Reisimine ja kulu** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Avansimakse saldot ei värskendata, kui kui kuluaruanne sisestatakse rea kaupa. |
| **Reisimine ja kulu** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Ülesanne **Makseteabe värskendamine** nurjub pärast selliste tasumiste tagasipööramist, kus arve tasuti kahe või enama maksetehinguga. |
| **Reisimine ja kulu** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Esineb probleem viimase päeva toidukorra allahindluse arvutamisega päevapõhise kulukategooria korral. |
| **Reisimine ja kulu** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Aruanne **Kulutüüp töötaja kohta** ei näita üksikasjalikke kulusid, kui kasutaja esimene ühendus oli keeles es-MX. |
| **Reisimine ja kulu** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Hankija makse kuluaruande arve jaoks kasutab valet kokkuvõttekontot tasumise sisestamiseks. |
| **Reisimine ja kulu** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Valikutega **Luba tehingute rühmitamine viivituse maksekonto põhjal** ja **Arveldamiskuupäeva korrigeerimine kirjendamise ajal** sisse lülitatud kirjendatav kuluaruanne näitab, et raamatupidamise kuupäevad ei ole tabelis **Arvestuse jaotus** rühmitatud, mis mõjutab käibemaksu kirjeid. |
| **Reisimine ja kulu** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Kulu alamkategooria vastendus eemaldatakse, kui ruut Kasuta kulus tühjendatakse ja uuesti valitakse. |
| **Reisimine ja kulu** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Kontsernisisest kuluaruannet ei saa luua, kui projekti ID lisatakse päise tasemel. |
| **Reisimine ja kulu** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Esineb kulu eest tasumise probleem, kui kulusumma on suurem kui avansimakse summa. |
| **Reisimine ja kulu** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Kui kasutajaroll on määratud konkreetsele organisatsioonile, on väli **Projekti ID** kontsernisiseses kuluaruandes tühi. |
| **Reisimine ja kulu** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kulukategooria lukustatakse uue kulurea lisamisel. |
| **Reisimine ja kulu** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Juba jaotatud kuluaruande ridade üksikasjadeks jaotamisel tekib lõpetamata sisestatud ostureskontro/pearaamatu kanne. **TRVEXPTRANS.SOURCEDOCUMENTLINE** paljundamise tõttu on ka raamatupidamise allika uurija katki. |
| **Reisimine ja kulu** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Tabelile **TRVREQUISITIONLINE** lisatud register, mille kohta kliendil on duplikaadid, põhjustab värskendamisel tõrke. |
| **Reisimine ja kulu** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Project Operationsis ei saa kontsernisiseste ülesannete kellaaega Dataverse'is luua ega kinnitada. |

## <a name="regulatory-updates"></a>Regulatiivsed uuendused

Lisateavet teenuse Finance and Operations rakenduste regulatiivsete uuenduste kohta vaadake teemast [Regulatiivsed uuendused](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Saate ka LCS-i sisse logida ja vaadata kavandatud regulatiivseid värskendusi, kasutades probleemi otsimise tööriista. Probleemi otsing võimaldab teil otsida riigi, funktsiooni tüübi ja väljalaske põhjal.


[!INCLUDE[footer-include](../includes/footer-banner.md)]