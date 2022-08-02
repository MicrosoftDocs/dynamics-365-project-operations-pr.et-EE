---
title: Mis on uut või mida on muudetud rakenduses Project Operations (september 2021) varutud/tootmispõhiste stsenaariumide jaoks?
description: Selles artiklis antakse teavet kvaliteedivärskenduste kohta, mis on saadaval 2021. aasta septembri väljaandes Project Operations laos/tootmispõhiste stsenaariumide jaoks.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: be0f397df4a3e1973e1f5546e43b2cf9578950a0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029847"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Mis on uut või mida on muudetud rakenduses Project Operations (september 2021) varutud/tootmispõhiste stsenaariumide jaoks?

_**Kehtib järgmiste puhul:** Project Operations ladustamise-/tootmispõhiste stsenaariumide jaoks_

See artikkel kehtib microsofti järgmiste komponentide ja versioonide kohta Dynamics 365 Project Operations:

- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnas versioon 10.0.21
 
## <a name="quality-updates"></a>Kvaliteedi värskendused

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
|---|---|---|
| Projektihaldus ja raamatupidamine | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Kui ostuhalduri rollile antakse juurdepääs ühele juriidilisele isikule, saab see juurdepääsu ka kõigile projektidele kõigis juriidilistes isikutes. |
| Projektihaldus ja raamatupidamine | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Käibemaksu (KM) ümardamise probleem tekib kreeditarve tasakaalustamisel algse projektiarvega. |
| Projektihaldus ja raamatupidamine | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Kasutage eelarve kinnitamiseks alternatiivset projekti eelarvet. |
| Projektihaldus ja raamatupidamine | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Hinnagruppi **Müügihind tunnis** ei arvutata projektipakkumiste tööjaotuse struktuuri põhjal. |
| Projektihaldus ja raamatupidamine | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Prognoosi eemaldamine nurjub, **kui funktsioon Luba projekti lepingu valuuta prognoosi arvutamiseks** on lubatud. |
| Projektihaldus ja raamatupidamine | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Käibemaksu faktooring koguse järgi lisatakse müügihinna summale, kui projekti kulu töölehe käibemaksugrupis kasutatakse kasutusmaksu. |
| Projektihaldus ja raamatupidamine | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Tingimuslikku maksu ei arvutata õigesti viimase makse eest, kui hankija kinnipidamine ja ettemaks rakendatakse ostutellimuse arvetele. |
| Projektihaldus ja raamatupidamine | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Korrigeerimise jälitus ei tööta algsaldo töölehtede puhul. |
| Projektihaldus ja raamatupidamine | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Projekti eelarve muutmise eraldamine perioodi** järgi jagatakse kõigi eelarveperioodide vahel. Eraldamise edastamisel kirjet ei tühjendata. |
| Projektihaldus ja raamatupidamine | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Tööprotsesside (WIP) sisestustel pearaamatusse on vale summa. |
| Projektihaldus ja raamatupidamine | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Projekti tunni töölehe kinnitamine ei toimi. |
| Projektihaldus ja raamatupidamine | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Projekti korrigeerimise müügihinda ei värskendata kaudsete kuludega, kui rahastamislimiit on märkimata. |
| Projektihaldus ja raamatupidamine | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Kaubavajadust ei saa luua, kui müügitabeli päise eest esitatakse arve ja olemasolevate ridade aluseks olev ostutellimus on lõpule viidud. |
| Projektihaldus ja raamatupidamine | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Sellise arveldusreegli säilitussummat, millel on mõne muu projekti verstapost, ei sisestata vastavasse-eesmärgi jaoks valitud projekti ID-sse. Selle asemel postitatakse see koos esimese projektiga. |
| Projektihaldus ja raamatupidamine | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Kui valite **arvesoovituses määratud** finantsdimensiooni, ilmneb järgmine tõrge: "Ei saa üle kanda objekti tüübiga 'Dynamics.AX. Application.FormIntControl" tippimiseks "Dynamics.AX. Application.FormStringControl'." |
| Projektihaldus ja raamatupidamine | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Projektiarve **aruandes** jäetakse read vahele. |
| Projektihaldus ja raamatupidamine | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Tõrge ilmneb siis, kui arvutate investeerimisprojekti kulukontrolli. |
| Projektihaldus ja raamatupidamine | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | **ProjTable:: InitFromCustTable - canDeletePostalAddress** meetod põhjustab jõudlusprobleemi. |
| Projektihaldus ja raamatupidamine | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Veateade peaks olema selgem kui "Ootamatu tõrge". |
| Projektihaldus ja raamatupidamine | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | PakettProjekti arve sisestamine töötleb ja sisestab arvesoovituse isegi siis, kui arveridu pole loodud. |
| Projektihaldus ja raamatupidamine | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Ümardamisprobleem ilmneb siis, kui avaliku sektori litsentsi konfiguratsioonivõti on välja lülitatud. Vale kulu või müügihind genereeritakse ajatabeli tundides lepingute puhul, millel on mitu leiuallikat. |
| Projektihaldus ja raamatupidamine | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Projekti müügihind arveldatud projekti ostutellimusel arvutatakse valesti, kui müügihinna mudeliks on **Sissemakse suhe**. |
| Projektihaldus ja raamatupidamine | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Süsteem ei võta arvesse vahepealseid aktiivseid päevi, kui ta arvutab töötaja tegeliku tööjõu määra. |
| Projektihaldus ja raamatupidamine | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Kontsernisisesel ajatabelil ilmneb sisestustõrge järgmise valideerimisvea tõttu: "Juriidilise isiku jaoks pole ühtegi kaubanduspartnerit konfigureeritud." |
| Projektihaldus ja raamatupidamine | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Kulukategooriaga ostutellimuse kirjeldust ei tooda sisestatud projektikannete loendisse. |
| Projektihaldus ja raamatupidamine | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Projekti postitatud kaubatöölehtedel on vale konversioon. |
| Projektihaldus ja raamatupidamine | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Ostutellimuse saate kinnitada ka siis, kui rahastamislimiit on ületatud. |
| Projektihaldus ja raamatupidamine | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Vabas **vormis arvel** olev arvete parandamise/tühistamise jaotis kaob, kui on valitud projekti ID. |
| Projektihaldus ja raamatupidamine | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Jõudlusprobleeme esineb siis, kui projekti arvesoovitus sisestatakse projekti müügitellimusest, mis sisaldab ladustatud kaupa. |
| Projektihaldus ja raamatupidamine | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Projekti ostuarveid ei saa sisestada, kuna ilmneb järgmine tõrge: "Funktsioon AccDistProcessorProjectExtension.createForProjectRevenueLine on valesti kutsutud." |
| Projektihaldus ja raamatupidamine | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Värskendage projekti hinnanguliste pakett-tööde loomist, et toetada mitme alamülesande täitmist. |
| Projektihaldus ja raamatupidamine | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Ajatabeli olekut ei saa värskendada olekuks **Mustand,** kui töövoog on olekus **Tühistatud**. |
| Projektihaldus ja raamatupidamine | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Säilitussummasid ei arvutata kreeditarvesoovituses, kui on mitu rida. |
| Projektihaldus ja raamatupidamine | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Kui proovite ostutellimusest genereeritud arvel olevat summat muuta, ilmneb järgmine tõrge: "Kande kanded ei saldo vastavalt XX/XX/XXXX andmetele. (raamatupidamisvaluuta: 0.00 – aruandlusvaluuta: 0.01)“. |
| Projektihaldus ja raamatupidamine | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Projektiarvesoovituse sisestamisel pakettrežiimis on jõudlusprobleem, kuna see on ühendatud rakendusega **GeneralJournalAccountEntry**. |
| Projektihaldus ja raamatupidamine | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Ajatabeli postitamisel on jõudlusprobleeme. |
| Projektihaldus ja raamatupidamine | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Tööjaotuse struktuuri kuluprognooside hierarhia ei ole pärast kõigi ülesannete laiendamist või ühe ülesande käsitsi laiendamist õigesti joondatud. |
| Projektihaldus ja raamatupidamine | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Projektipakkumise Exceli malli ei saa lisada menüüsse **Ava Excelis**. |
| Projektihaldus ja raamatupidamine | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Prinditud projektiarvele ei lisata juriidilise isiku maksuvabastuse numbrit. |
| Projektihaldus ja raamatupidamine | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Inventariühiku veas finantsandmeid ei uuendata, kui projekti korrigeeritakse krediidiliinide suhtes. |
| Projektihaldus ja raamatupidamine | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Pärast KB 461935 rakendamist ei saa te pidevatele numbriseeriatele lülitudes prognoose postitada. |
| Projektihaldus ja raamatupidamine | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** põhjustab projekti ajatabeli mobiilirakenduse Android reageerimast lakkamise. |
| Projektihaldus ja raamatupidamine | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Arve sisestamise WIP-i ümberpööratud väärtus erineb algselt sisestatud WIP-i väärtusest sisestamise hetkest. |
| Projektihaldus ja raamatupidamine | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Rakendatud käsirahade puhul ei saldo kanded projekti eest arveldatud tulu sisestamisel. |
| Projektihaldus ja raamatupidamine | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | **Kui projekti ressursside plaanimise jõudluse täiustamise** funktsioon on lubatud, ümardatakse kümnendväärtused ressursi saadavuse ja võimsuse osas valesti. |
| Projektihaldus ja raamatupidamine | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | **Kui funktsioon Projektiprognooside loomine mitme pakett-ülesande** abil on lubatud, töötab prognooside loomine partiis, millel on mitu alamülesannet, ainult praegusel perioodil. |
| Reisimine ja kulu | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Reisitaotluse poliitikat ignoreeritakse ja töövoog kinnitatakse vigadeta. |
| Reisimine ja kulu | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Mobiilirakendus Mobiilikulu ei salvesta kulureale järgmist teavet:</p><ul><li>Projekti ID</li><li>Kas kulu on arveldatav</li><li>Tegevuse number</li></ul> |
| Reisimine ja kulu | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Väli **Manustatud laekumised** on seatud väärtusele Jah **isegi siis,** kui kulureale pole lisatud ühtegi kviitungit. |
| Reisimine ja kulu | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Tõrge ilmneb siis, kui muudate kulukategooria väärtuseks **Isiklik**. |
| Reisimine ja kulu | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Te ei saa lisada kviitungit ja muuta emakulu pärast seda, kui krediitkaardikanne on jagatud isiklikuks kuluks. |
| Reisimine ja kulu | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Projekti ID-ga kontsernisiseste kannete kulupoliitika ei tööta õigesti. |
| Reisimine ja kulu | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Sisestatud kuluaruannete puhul puudub sisestatud kuupäeva teave. |
| Reisimine ja kulu | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Kulu mobiilirakenduses on makseviisiga probleeme. |
| Reisimine ja kulu | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Ühe töötaja jaoks loodud siirdetaotlust saab kasutada teise töötaja kuluaruande jaoks enne delegeerimiskuupäeva. |
| Reisimine ja kulu | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Kulu loomisel ei värskendata finantsdimensiooni väärtuste muudatusi õigesti tööruumi Kuluhaldus **raamatupidamise** jaotuse tasemel. |
| Reisimine ja kulu | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Peamise kulurea kinnitamise olekut ei sünkroonita reapõhise rea kinnitamise olekuga. |
| Reisimine ja kulu | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Tõrge ilmneb siis, kui sisestate kuluaruande ja maksude sissenõudmine on lubatud. |
| Reisimine ja kulu | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Delegaat ei saa lõpetatud lepinguga töötaja kuludokumente kustutada. |
| Reisimine ja kulu | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Kulurea kustutamine võtab oodatust kauem aega ja mõjutab tulemuslikkust. |
| Reisimine ja kulu | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** põhjustab orvuks jäänud **TaxUncommitted** kirje, kuna kustutatakse ainult **SourceDocumentLine**. |
| Reisimine ja kulu | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** ei austa **trvExpTrans.ReferenceDataAreaId** uue numbriseeria loomist. |

## <a name="regulatory-updates"></a>Regulatiivsed uuendused

Lisateavet finance and operationsi rakenduste regulatiivsete värskenduste kohta leiate teemast [Regulatiivsed värskendused](/dynamics365/finance/localizations/regulatory-updates). Samuti saate sisse logida teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja kasutada probleemiotsingu tööriista plaanitud regulatiivsete värskenduste vaatamiseks. Probleemiotsing võimaldab teil otsida riigi või piirkonna, funktsiooni tüübi ja väljalaske järgi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
