---
title: Mis on uut või muutunud Project Operationsi ressursi-/tootmispõhiste stsenaariumite jaoks septembris 2021
description: See artikkel annab teavet lao-/tootmispõhiste stsenaariumite jaoks mõeldud rakenduse Project Operations 2021. aasta septembri väljalaskes saadaolevate kvaliteedi värskenduste kohta.
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
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Mis on uut või muutunud Project Operationsi ressursi-/tootmispõhiste stsenaariumite jaoks septembris 2021

_**Kehtib järgmiste puhul:** Project Operations ladustamise-/tootmispõhiste stsenaariumide jaoks_

See artikkel kehtib rakenduse Microsoft Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.21
 
## <a name="quality-updates"></a>Kvaliteedi värskendused

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
|---|---|---|
| Projektihaldus ja raamatupidamine | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Kui ostujuhi rollile antakse juurdepääs ühele juriidilisele isikule, saab see juurdepääsu ka kõikidele projektidele kõigis juriidilistes olemites. |
| Projektihaldus ja raamatupidamine | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Kui kreeditarve tasaarveldatakse projekti algse arve alusel, ilmneb käibemaksu (KM) ümardamise probleem. |
| Projektihaldus ja raamatupidamine | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Kasutage eelarve kontrollimiseks alternatiivset projekti eelarvet. |
| Projektihaldus ja raamatupidamine | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Hinnarühma **Müügihinna tund** ei arvestata projektipakkumiste tööjaotuse struktuuris. |
| Projektihaldus ja raamatupidamine | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Prognoosi eemaldamine nurjub, kui **Luba projektilepingu valuuta prognoosimise arvutamiseks** funktsioon on lubatud. |
| Projektihaldus ja raamatupidamine | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Käibemaksu faktoriseerimine koguse järgi lisatakse müügihinna summale, kui projekti kulutöölehe käibemaksurühmas kasutatakse kasutusmaksu. |
| Projektihaldus ja raamatupidamine | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Tingimuslikku maksu ei arvutata viimase makse jaoks õigesti, kui ostutellimuse arvetele rakendati hankijalt kinnipidamine ja ettemakse. |
| Projektihaldus ja raamatupidamine | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Reguleerimisjälg ei tööta algsaldo töölehtede puhul. |
| Projektihaldus ja raamatupidamine | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Projekti eelarve läbivaatamise jaotus perioodide kaupa** on jagatud kõikide eelarveperioodide vahel. Jaotuse esitamisel kirjet ei kustutata. |
| Projektihaldus ja raamatupidamine | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Pearaamatu pooleli töö (WIP) kirjetel on vale summa. |
| Projektihaldus ja raamatupidamine | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Projekti tunnitööölehe kinnitamine ei toimi. |
| Projektihaldus ja raamatupidamine | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Projekti korrigeerimise müügihinda ei värskendata kaudsete kuludega, kui rahastamislimiiti pole märgitud. |
| Projektihaldus ja raamatupidamine | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Üksuse nõuet ei saa luua, kui müügitabeli päises on arve ja olemasolevate ridade varuostutellimus on vormistatud. |
| Projektihaldus ja raamatupidamine | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Arveldusreegli säilitamise summat, mis on erineva projekti etapiga, ei postitata vastavasse projekti ID-sse, mis on etapi jaoks valitud. Selle asemel on see postitatud koos esimese projektiga. |
| Projektihaldus ja raamatupidamine | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Kui valite arve ettepanekul valiku **Finantsidimensioonide komplekt**, ilmneb järgmine tõrge: „Ei saa üle kanda 'Dynamics.AX.Application.FormIntControl' tüüpi objekti 'Dynamics.AX.Application.FormStringControl' tüüpi.“ |
| Projektihaldus ja raamatupidamine | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Aruanne **Projekti arve** jätab read vahele. |
| Projektihaldus ja raamatupidamine | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Investeerimisprojekti kulukontrolli arvutamisel ilmneb tõrge. |
| Projektihaldus ja raamatupidamine | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Meetod **ProjTable::InitFromCustTable - canDeletePostalAddress** põhjustab jõudlusprobleeme. |
| Projektihaldus ja raamatupidamine | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Tõrketeade peaks olema selgem kui „Ootamatu tõrge“. |
| Projektihaldus ja raamatupidamine | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Projekti arvete kirjendamise partiitöö töötleb ja postitab arveettepaneku isegi siis, kui arve ridu pole loodud. |
| Projektihaldus ja raamatupidamine | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Kui avaliku sektori litsentsi konfiguratsioonivõti on välja lülitatud, ilmneb ümardamisprobleem. Mitme alusallikaga lepingute ajatabeli tundides luuakse vale kulu- või müügihind. |
| Projektihaldus ja raamatupidamine | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Projekti müügihind arveldatud projekti ostutellimusel on valesti arvutatud, kui müügihinna mudeliks on **Osakaal**. |
| Projektihaldus ja raamatupidamine | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Süsteem ei arvesta töötaja tegeliku tööjõumäära arvutamisel vahepealseid aktiivseid päevi. |
| Projektihaldus ja raamatupidamine | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Kontsernivahelisel ajatabelil ilmneb postitamistõrge järgmise kinnitamistõrke tõttu: „Juriidilise isiku jaoks pole kaubanduspartnerit seadistatud“. |
| Projektihaldus ja raamatupidamine | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Kulukategooriaga ostutellimuse kirjeldust ei leita postitatud projekti tehingute loendist. |
| Projektihaldus ja raamatupidamine | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Projekti postitatud üksuse töölehel on vale teisendus. |
| Projektihaldus ja raamatupidamine | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Ostutellimuse saate kinnitada ka siis, kui rahastamislimiit on ületatud. |
| Projektihaldus ja raamatupidamine | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Projekti ID valimisel kaob vabatekstiarvete jaotis **Parandus/arve tühistamine**. |
| Projektihaldus ja raamatupidamine | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Kui projekti arve ettepanek postitatakse projekti müügitellimusest, mis sisaldab laokaupa, esineb toimivusprobleeme. |
| Projektihaldus ja raamatupidamine | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Projekti ostuarveid ei saa postitada, kuna ilmneb järgmine tõrge: „Funktsiooni AccDistProcessorProjectExtension.createForProjectRevenueLine on valesti kutsutud“. |
| Projektihaldus ja raamatupidamine | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Projekti prognooside partiitööde loomise värskendus, et toetada mitme alamülesande täitmist. |
| Projektihaldus ja raamatupidamine | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Tööajatabeli olekut ei saa värskendada olekusse **Mustand**, kui töövoog on jäänud olekusse **Tühistatud**. |
| Projektihaldus ja raamatupidamine | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Mitme rea olemasolul ei arvutata kinnipidamissummasid kreeditarve ettepanekus. |
| Projektihaldus ja raamatupidamine | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Kui proovite muuta ostutellimusest koostatud arvel olevat summat, ilmneb järgmine tõrge: „Kandel olevad tehingud ei ole XX/XX/XXXX seisuga tasakaalus. (raamatupidamisvaluuta: 0.00 – aruandlusvaluuta: 0.01)“. |
| Projektihaldus ja raamatupidamine | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Kui projekti arve ettepanek postitatakse partiirežiimis, tekib toimivusprobleem, kuna see on ühendatud **GeneralJournalAccountEntry**-ga. |
| Projektihaldus ja raamatupidamine | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Ajatabeli postitamisel on jõudlusega probleeme. |
| Projektihaldus ja raamatupidamine | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Tööjaotuse struktuuri kuluhinnangute hierarhia ei ole pärast kõigi ülesannete laiendamist või ühe ülesande käsitsi laiendamist õigesti joondatud. |
| Projektihaldus ja raamatupidamine | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Projekti pakkumise Exceli malli ei saa lisada menüüsse **Ava Excelis**. |
| Projektihaldus ja raamatupidamine | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Prinditud projektiarve ei sisalda juriidilise isiku maksuvaba numbrit. |
| Projektihaldus ja raamatupidamine | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Laoüksuse tõrkes finantsandmeid ei uuendata, kui projekti korrigeeritakse krediidiridade suhtes. |
| Projektihaldus ja raamatupidamine | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Pärast KB 461935 rakendamist ei saa te hinnanguid postitada, kui lülitute pidevatele numbrijadadele. |
| Projektihaldus ja raamatupidamine | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** põhjustab projekti ajatabeli Android mobiilirakenduse reageerimise lõpetamise. |
| Projektihaldus ja raamatupidamine | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Arve konteerimisel saadud WIP-i ümberpööratud väärtus erineb ajakirje algselt konteeritud WIP-väärtusest. |
| Projektihaldus ja raamatupidamine | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Rakendatud kinnipidamisjuhtumite puhul ei ole kandel olevad tehingud projekti arveldatud tulu postitamisel tasakaalus. |
| Projektihaldus ja raamatupidamine | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Kui funktsioon **Projekti ressursside ajastamise jõudluse parandamine** on lubatud, ümardatakse kümnendväärtused ressursside saadavuse ja võimsuse jaoks valesti. |
| Projektihaldus ja raamatupidamine | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Kui funktsioon **Loo projektiprognoosid, kasutades mitut partiiülesannet** on lubatud, töötab prognooside loomine mitut alamülesannet sisaldavas partiis ainult praeguse perioodi kohta. |
| Reisimine ja kulu | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Reisitaotluse poliitikat eiratakse ja töövoog kinnitatakse tõrgeteta. |
| Reisimine ja kulu | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Mobiilikulude rakendus ei salvesta kulureale järgmist teavet:</p><ul><li>Projekti ID</li><li>Kas kulu on arveldatav</li><li>Tegevuse number</li></ul> |
| Reisimine ja kulu | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Välja **Lisatud kviitungid** on seatud väärtusele **Jah**, isegi kui kulureale pole kviitungit lisatud. |
| Reisimine ja kulu | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Kui muudate kulukategooriaks **Isiklik**, ilmneb tõrge. |
| Reisimine ja kulu | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Pärast krediitkaarditehingu jagamist isiklikuks kuluks ei saa kviitungit manustada ega vanemkulusid muuta. |
| Reisimine ja kulu | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Projekti ID-ga kontsernivaheliste tehingute kulupoliitika ei tööta õigesti. |
| Reisimine ja kulu | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Postitatud kuluaruannete puhul puudub postitamiskuupäeva teave. |
| Reisimine ja kulu | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Kulu mobiilirakenduses on probleeme maksemeetodiga. |
| Reisimine ja kulu | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Ühe töötaja jaoks loodud reisitaotlust saab kasutada teise töötaja kuluaruande jaoks enne delegeeritud kuupäeva. |
| Reisimine ja kulu | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Kulu loomisel ei värskendata tööruumi **Kuluhaldus** raamatupidamise jaotustasemel finantsdimensiooni väärtuste muudatusi õigesti. |
| Reisimine ja kulu | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Peamise kulurea kinnitusolekut ei sünkroonita üksikasjaliku rea töövoo kinnitusolekuga. |
| Reisimine ja kulu | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Tõrge ilmneb, kui postitate kuluaruande ja maksude tagastamine on lubatud. |
| Reisimine ja kulu | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Delegaat ei saa lõpetatud lepinguga töötaja kuludokumente kustutada. |
| Reisimine ja kulu | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Kulurea kustutamine võtab oodatust kauem aega ja mõjutab jõudlust. |
| Reisimine ja kulu | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** põhjustab orvuks jäänud kirje **TaxUncommitted**, kuna kustutatakse ainult **SourceDocumentLine**. |
| Reisimine ja kulu | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** ei austa **trvExpTrans.ReferenceDataAreaId** uue numbrijada loomiseks. |

## <a name="regulatory-updates"></a>Regulatiivsed uuendused

Lisateavet finants- ja äritoimingute rakenduste regulatiivsete värskenduste kohta, vt [Regulatiivsed värskendused](/dynamics365/finance/localizations/regulatory-updates). Samuti saate logida sisse teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja kasutada probleemide otsingutööriista, et vaadata kavandatud regulatiivseid värskendusi. Probleemi otsing võimaldab teil otsida riigi või piirkonna, funktsiooni tüübi ja väljalaske põhjal.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
