---
title: Mis on Project Operationsis ressursi-/tootmispõhiste stsenaariumite jaoks 2021. a juulis uut või muutunud
description: Selles teemas antakse teavet Project Operationsi 2021. aasta juuli väljaandes olevate kvaliteedivärskenduste kohta ressursi-/tootmispõhiste stsenaariumite jaoks.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: db5bb27650d65bb68f45f95cb2562f4b773ddcea
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597057"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Mis on Project Operationsis ressursi-/tootmispõhiste stsenaariumite jaoks 2021. a juulis uut või muutunud

_**Kehtib järgmiste puhul:** Project Operations ladustamise-/tootmispõhiste stsenaariumide jaoks_

See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.

- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnaversioonis 10.0.20
 
### <a name="quality-updates"></a>Kvaliteedi värskendused
                                                                                                                                                                                  
| Funktsiooni ala                      | Viitenumber| Kvaliteedi värskendus                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektihaldus ja raamatupidamine | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Ostutellimuse kulukohustuste kirjed kustutatakse kohe, kui ostutellimus vabastatakse ostutellimuse probleemist.                                                                           |
| Projektihaldus ja raamatupidamine | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Eelarve kinnitamine toimub ostutellimuses kaks korda. See dubleerimine tähendab, et tellimust ei saa sulgeda ja vastavat ostutellimust ei looda.                                                                                                                        |
| Projektihaldus ja raamatupidamine | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Arveldusreeglit **Arveldamisepõhine protsent** ei saanud ümardamisprobleemi tõttu lõpule viia.                                                                              |
| Projektihaldus ja raamatupidamine | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Kui muudate tehingut ja protsendil on kümnendkohti, ei korrigeerita kulu ja müügihinna õigesti.                                      |
| Projektihaldus ja raamatupidamine | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Raamatupidamisallika uurija kuvab erinevate tegevustega mitme ajatabeli ridade jaoks ühe ajatabeli.                                      |
| Projektihaldus ja raamatupidamine | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Salvestatud vaadete ja ajatabeli rea üksikasjade isikupärastamine põhjustab ajatabeli avamise proovimisel, et süsteem avab alati loendi esimese ajatabeli üksikasjad.  |
| Projektihaldus ja raamatupidamine | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Projekti juursõlm kaob ja tööjaotuse struktuurikirjed kustutatakse pärast importimist.                                                                                             |
| Projektihaldus ja raamatupidamine | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Kui üksused võetakse vastu ja väljastatakse osaliselt üksuse nõudest, värskendab süsteem vale eelarve kasutuse saldo. |
| Projektihaldus ja raamatupidamine | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Projekti säilitamise müügitellimused ei kuva paanil **Kogusummad** või ruudustikus **Ootel arve** kogusummasid õigesti.                                                                  |
| Projektihaldus ja raamatupidamine | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Varude sulgemisel kirjendatakse projektiüksuse kulude korrigeerimine saldokontole, mitte kulu- ja tulukontole.                                                            |
| Projektihaldus ja raamatupidamine | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Projekti kirjendatud tehingu vautšer ja prognoosi vautšer kasutavad arvestusvaluutana USD-d, kuid summa näitab, mis oleks CAD ekvivalent.              |
| Projektihaldus ja raamatupidamine | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Kinnitatud kulud koos üksuse nõudega ja ostutellimusega on ostutellimuse arve protsessis valed koos osa toote kviitungi ja osa arveldamisega.       |
| Projektihaldus ja raamatupidamine | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Projekti korrigeerimine ei värskenda kaudsete kulude müügisummat õigesti.                                                                                    |
| Projektihaldus ja raamatupidamine | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Tabelis **Ajatabel** puudub määratletud seos vaatega **Töötaja/ressurss**.                                                                                   |
| Projektihaldus ja raamatupidamine | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Välja **Tegevuse number** ei sa atäita, kui valite selle kontsernisisese ajatabeli rippmenüüst.                                                                 |
| Projektihaldus ja raamatupidamine | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Isikupärastatud välja **Eesmärk** ega **Tegevuse kirjeldus** ei saa lisada järgmistele lehtedele: **Projekti kirjendatud tehing**, **Arve ettepaneku loomine** või **Arve ettepanek**.  |
| Projektihaldus ja raamatupidamine | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Kui loote üksuse nõuded kasutades andmehaldust (**ProjSalesItemRequirementEntity**), esitatakse vale tarnekuupäeva juhtelement.                                              |
| Projektihaldus ja raamatupidamine | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Kui valite soovitud projekti lepingu ID rakenduses Finance, siis olemasoleva projektielepingu asemel avab Project Operationsi integreeritud keskkond lehe, et luua uus kirje.                                                                                                                 |
| Projektihaldus ja raamatupidamine | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Silti „@SYS4083080” („Sisestatud väärtusele vastavat unikaalset töötaja kirjet ei leita”) ei tõlgita taani keelde.                                |
| Projektihaldus ja raamatupidamine | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Väli **Üksuse käibemaksu rühm** pole arve ettepanekus redigeeritav.                                                                               |
| Projektihaldus ja raamatupidamine | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Kinnitatud kulu suurendatakse mitte-mahaarvatavate maksusummadega.                                                                                                    |
| Projektihaldus ja raamatupidamine | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Kontsernisisese ajatabeli kirjendamine koos mitme projektiga ja erinevate finantsmõõtmetega loob pearaamatus ootamatud väärtused.                             |
| Projektihaldus ja raamatupidamine | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Arve ettepaneku read dubleeritakse samal ajal töötava perioodilise protsessi **Koondamisest importimine** mitme eksemplari tõttu.                                      |
| Projektihaldus ja raamatupidamine | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Krediidiarve ettepaneku kirjendamisel esine tõrge, seega ei vautšeri tehingud tasakaalus.    |
| Projektihaldus ja raamatupidamine | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Projekti kinnitatud kulud muutuvad pärast ootel arvete vabastamist valeks.                                                                             |
| Projektihaldus ja raamatupidamine | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Kui maks asub ettevõtte valuutast erinevas valuutas, ei saa te projekti müügitellimust luua.                                      |
| Projektihaldus ja raamatupidamine | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Lepingu kustutamine kustutab ka kliendiga seotud aadressi.                                                                                     |
| Projektihaldus ja raamatupidamine | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Negatiivse ajakande paranduse tulemuseks olevat arve ettepanekut ei saa kirjendada.                                                                    |
| Reisimine ja kulu                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Maks arvutatakse kuluaruannetes erinevalt.                                                                                                                  |
| Reisimine ja kulu                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Väljaande värskendus **DB72_Expense.updateTrvExpTransProjTransId()** ei luba atribuudil **trvExpTrans.ReferenceDataAreaId** uut numrbi järjestust.                    |
| Reisimine ja kulu                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Töidetud summat ei näidata kohustuslikul väljal.                                                                                                             |
| Reisimine ja kulu                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Parandatud on kulu manustamise jõudlust kuluaruandele, kasutades kasutajaliidest Ümberkujundatud kulu.                                                            |
| Reisimine ja kulu                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Saate sisestatud kuluaruanded kustutada.                                                                                           |
| Reisimine ja kulu                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Kulupoliitika sõnum kuvatakse mitu korda.                                                                                                       |
| Reisimine ja kulu                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Väli **Makseviis** on kaasatud paanil **Uus kulu**.                                                                                                      |
| Reisimine ja kulu                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Kui töövoogu ei leitud, peaks tööriist **Kuludokumendi oleku lähtestamine** lähtestama kuluaruande olekule **Mustand**. 

### <a name="regulatory-updates"></a>Regulatiivsed uuendused
Finance and Operationsi rakenduste regulatiivsete värskenduste kohta leiate teavet teemast [Regulatiivsed värskendused](/dynamics365/finance/localizations/regulatory-updates). Samuti saate logida sisse teenusesse Lifecycle Services (LCS) ja vaadata plaanitud regulatiivseid värskendusi, kasutades probleemi otsingutööriista. Probleemi otsing võimaldab teil otsida riigi, funktsiooni tüübi ja väljalaske põhjal.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
