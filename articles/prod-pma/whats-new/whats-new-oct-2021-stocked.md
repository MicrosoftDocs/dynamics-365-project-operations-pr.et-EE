---
title: Mis on uut või muutunud rakenduse Project Operations lao-/tootmispõhiste stsenaariumite jaoks oktoobris 2021
description: See artikkel annab teavet lao-/tootmispõhiste stsenaariumite jaoks mõeldud rakenduse Project Operations 2021. aasta oktoobri väljalaskes saadaolevate kvaliteedivärskenduste kohta.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029938"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Mis on uut või muutunud rakenduse Project Operations lao-/tootmispõhiste stsenaariumite jaoks oktoobris 2021

_**Kehtib järgmiste puhul:** Project Operations ladustamise-/tootmispõhiste stsenaariumide jaoks_

See artikkel kehtib rakenduse Microsoft Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.22
 
## <a name="quality-updates"></a>Kvaliteedi värskendused

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
|--------------|------------------|----------------|
| Projektihaldus ja raamatupidamine | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Pooleli oleva projektitöö (WIP) ja kogunenud tulude summasid ei tühistata õigesti, kui kontsernisisese kliendi arve postitatakse. |
| Projektihaldus ja raamatupidamine | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Funktsioon **Projekti sulgemise vältimine avatud tehingute olemasolul** ei tööta. |
| Projektihaldus ja raamatupidamine | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Vabatekstiarvete arveldusklassifikatsioon ei täida automaatselt projektide dimensioone, kui see funktsioon on lubatud. |
| Projektihaldus ja raamatupidamine | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Mittekontsernivaheliste stsenaariumide puhul ei ole WIP ja viitlaekumiste summad korrektselt ümberpööratud, kui projektiarve on postitatud. |
| Projektihaldus ja raamatupidamine | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Deebet- ja kreeditväärtusi vahetatakse, kui Microsoft Exceli lisandmoodulit kasutatakse projekti kulutöölehe ja välja **Tasaarvestuskonto tüüp** väärtuseks on määratud **Projekt**. |
| Projektihaldus ja raamatupidamine | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Projektitehingutesse kirjendatud summa on projekti ostutellimusel, mis sisaldab laos olevaid kaupu ja millel on mahaarvamatuid maksusummasid, suurem, kui on märgitud jaotises **UseTax**. |
| Projektihaldus ja raamatupidamine | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Süsteem jagab summa projekti kasumi ja kahjumi aruannete ja projekti WIP aruannete vahel. |
| Projektihaldus ja raamatupidamine | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Olemasolevad varud on pärast osaliselt tagastatud üksuse nõude korrigeerimist valed. |
| Projektihaldus ja raamatupidamine | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Ressursinimed dubleeritakse rakenduses Project Operations, kui neid Microsoft Projectis redigeeritakse. |
| Projektihaldus ja raamatupidamine | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Kontsernivahelised kuluaruanded, millel on ostureskontro võlgnevuste kontsernisisesed hankija arve kulud, postitatakse esmalt **Projekti WIP kulu** konteerimistüübile. Töötlemise käigus postitatakse kalkulatsiooniga seotud kulud siiski postitamisliigile **Projekti kulud** oodatava postitamisliigi **Kontsernisisese kulu** asemel. |
| Projektihaldus ja raamatupidamine | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Hankija kinnipidamise tulemusi projektikulutehingutes ei näidata. |
| Projektihaldus ja raamatupidamine | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Ajatabel peab ümardama tehingu summa tehinguvaluutas kindlaksmääratud arvu kümnendkohtadeni kõigi raamatupidamislike jaotuste ja üldtööelehe jaotuskirjete puhul. |
| Projektihaldus ja raamatupidamine | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Projektiüksuse nõuete kogused ajakohastatakse automaatselt, kui planeeritud tellimused kinnitatakse. |
| Projektihaldus ja raamatupidamine | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Ostutellimuse ettemaksuarvel ei saa kande numbrit, tehingu tüüpi hankija saldot ega kontonumbrit tühistada. |
| Projektihaldus ja raamatupidamine | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Kui hankija arvete integreerimine on sisse lülitatud, on kontsernisisese hankija arve katki. |
| Projektihaldus ja raamatupidamine | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Projekti kulutöölehe loomisel kuvatakse kulusumma väljal **Krediit**. |
| Projektihaldus ja raamatupidamine | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projektiarvete maksetingimused ei toimi ootuspäraselt. |
| Projektihaldus ja raamatupidamine | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Ajatabeli kandeid võidakse uuesti kasutada, kui numbrijada on seadistatud pidevaks. |
| Projektihaldus ja raamatupidamine | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | PRANTSUSMAA: The **Käsitsi säilitatav summa** loogika ei ühti projektilepingu arve ettepanekus **Automaatselt säilitatava summa** loogikaga. |
| Projektihaldus ja raamatupidamine | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kui hankija säilitamine vabastatakse, on kande postitamisel valed lisaread. |
| Projektihaldus ja raamatupidamine | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Kui väli **Arve kuupäev** lehel **Loo arve ettepanek** muudetakse, võib tekkida järgmine tõrge: „Objekti viide ei ole määratud objekti eksemplarile.“ |
| Projektihaldus ja raamatupidamine | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Kui proovite kinnitada töövoo **TSLine** alusel ajatabelit, ilmneb tõrge ning laupäeval ja pühapäeval kehtivad ajatabeli eeskirjad. |
| Projektihaldus ja raamatupidamine | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Algbilansi projekti artikli tüüp jäetakse välja **Arve ettepaneku tehingukokkuvõtted**, kui arvutatakse arve ettepaneku arve kogusumma. |
| Projektihaldus ja raamatupidamine | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Kui projekti tootmistellimuse tarbimiskulu on 0 (null), ilmneb prognoosimisel järgmine tõrge: „Prooviti jagada nulliga“. |
| Projektihaldus ja raamatupidamine | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Projekti ajatabeli mobiilirakendus Androidile lakkab reageerimast. Probleem on seotud **TimeEntryDataManager ArgumentNullException**-ga. |
| Projektihaldus ja raamatupidamine | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Rakenduse Project Operations integratsioonitööleht nurjub selle postitamisel, kuna kontol puuduvad dimensioonid. Konto, millel puuduvad mõõtmed, ei ole aga konto, kuhu postitate. |
| Projektihaldus ja raamatupidamine | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Filtrit **ToDate** otsingutes ei tühjendata, kui see eemaldatakse dialoogiboksist **Vali** leht **Postituskulu**. |
| Projektihaldus ja raamatupidamine | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Kogu levitamise lähtestamine** ebaõnnestub ja kuvab tõrke ajatabelites, mis on loodud **Ainult aeg** tüüpi projekti jaoks. |
| Projektihaldus ja raamatupidamine | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Vahekaarti **Projekt** ei saa muuta ootel hankija arvel, kui kaubale on määratud hankekategooria. |
| Projektihaldus ja raamatupidamine | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigeerimispaan puudub, kui te pole rakendusse Project Operations Dataverse sisse logitud. |
| Projektihaldus ja raamatupidamine | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Kontsernisiseste projektide kohandamise tehingute puhul on probleeme sihtettevõttes. |
| Projektihaldus ja raamatupidamine | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Projekti kulukohustused arvutavad vale koguse ja omahinna, kui ostutellimus töödeldi pearaamatus **Ostutellimuse aastalõpu protsessiga**. |
| Projektihaldus ja raamatupidamine | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Kui projekti tootmistellimus, millel on kvaliteeditellimused, teatatakse lõpetatuks, ilmneb järgmine tõrge: „Laotehinguga pole märgitud virtuaalset tehingut“. |
| Projektihaldus ja raamatupidamine | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Projektiga seotud tasumisele kuuluva arve postitamisel ilmneb järgmine viga: „Loetletud teksti projekt - kulu - üksust ei ole olemas“. |
| Projektihaldus ja raamatupidamine | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Kaudsed kulud kahekordistuvad, kui kogute tulu käsitsi. |
| Projektihaldus ja raamatupidamine | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Tulu kogumine ja WIP-i postitamine ei tooda tehinguid. |
| Projektihaldus ja raamatupidamine | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Ootel oleva hinna aktiveerimine standardse kuluartikli puhul ebaõnnestub, kui vastuvõetud projekti ostutellimus on olemas. |
| Projektihaldus ja raamatupidamine | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Arve postitamisel saadud WIP-i ümberpööratud väärtus erineb ajakirje algsest konteeritud WIP-väärtusest. |
| Projektihaldus ja raamatupidamine | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Rakendatud säilitamisjuhtudel, kus kandel olevad tehingud ei ole tasakaalus, on projekti arveldatud tulu postitamise probleem. |
| Projektihaldus ja raamatupidamine | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Prognoosi koostamine pärast arve ettepaneku postitamist blokeerib parandusridade importimise rakendusse Project Operations. |
| Projektihaldus ja raamatupidamine | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Täielikult arveldatud vahekokkuvõtte kirje muutmine ei tohiks olla võimalik. |
| Projektihaldus ja raamatupidamine | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Automaatsete tasude kasutamisel ei saa ajatabeli kontsernisisest kliendi arvet postitada ja kuvatakse tõrketeade. |
| Projektihaldus ja raamatupidamine | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Alamprojekti aadressi ei ole õigesti värskendatud. |
| Projektihaldus ja raamatupidamine | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Kaubanõuete omahinda värskendatakse koos ostuhinnaga konsolideeritud ostutellimuste puhul. |
| Projektihaldus ja raamatupidamine | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Postitatud maksumus ei ole õige pärast ostuhinna värskendamist ja parameeter **Muudatuste haldamise aktiveerimine** on lubatud. |
| Reisimine ja kulu | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Kõik kasutajakulud on näha, kui otsite Kulu mobiilirakenduses kategooriat. |
| Reisimine ja kulu | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Hankija tehingute ja maksu tehingute valed summad on postitatud kulust, mis loodi krediitkaarditehingust. |
| Reisimine ja kulu | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Kuluaruande lehtede värskendamisel kuvatakse asjakohatu hoiatusteade. |
| Reisimine ja kulu | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Ajutise kinnitaja kustutamisel ja seejärel töövoo kaudu uuesti esitamisel kasutatakse vale ajutist kinnitajat. |
| Reisimine ja kulu | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ilmub postitamistõrge, mis on seotud läbisõidu seadistusega. |
| Reisimine ja kulu | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Jaotus ei värskenda juriidilist isikut, kui sidumata tehing lisatakse uuesti kontsernisisese kulu kuluaruandesse. |

### <a name="regulatory-updates"></a>Regulatiivsed uuendused

Lisateavet finants- ja äritoimingute rakenduste regulatiivsete värskenduste kohta, vt [Regulatiivsed värskendused](/dynamics365/finance/localizations/regulatory-updates). Samuti saate logida sisse teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja kasutada probleemide otsingutööriista, et vaadata kavandatud regulatiivseid värskendusi. Probleemi otsing võimaldab teil otsida riigi või piirkonna, funktsiooni tüübi ja väljalaske põhjal.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
