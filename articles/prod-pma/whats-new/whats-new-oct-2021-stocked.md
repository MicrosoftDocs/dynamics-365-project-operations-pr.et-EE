---
title: Mis on uut või muudetud Project Operationsis, oktoober 2021 ladustatud / tootmispõhiste stsenaariumide puhul
description: Selles artiklis antakse teavet kvaliteedivärskenduste kohta, mis on saadaval 2021. aasta oktoobri väljaandes Project Operations ladustatud/tootmispõhiste stsenaariumide jaoks.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: ba88268e74269c774b41396a8b6574e5bab477b9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933671"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Mis on uut või muudetud Project Operationsis, oktoober 2021 ladustatud / tootmispõhiste stsenaariumide puhul

_**Kehtib järgmiste puhul:** Project Operations ladustamise-/tootmispõhiste stsenaariumide jaoks_

See artikkel kehtib järgmiste Microsofti Dynamics 365 Project Operations komponentide ja versioonide kohta.

- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnaversioonis 10.0.22
 
## <a name="quality-updates"></a>Kvaliteedi värskendused

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
|--------------|------------------|----------------|
| Projektihaldus ja raamatupidamine | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Pooleliolev projektitöö (WIP) ja viittulusummasid ei tühistata kontsernisisese kliendiarve konteerimisel õigesti. |
| Projektihaldus ja raamatupidamine | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Avatud **kannete olemasolul** projekti sulgemise vältimine funktsioon ei tööta. |
| Projektihaldus ja raamatupidamine | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Vabas vormis arvel olev arveldusklassifikatsioon ei täida automaatselt projektide dimensioone, kui see funktsioon on lubatud. |
| Projektihaldus ja raamatupidamine | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Kontserniväliste stsenaariumide korral ei tühistata WIP-i ja kogunenud tulusummasid projektiarve konteerimisel õigesti. |
| Projektihaldus ja raamatupidamine | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Deebet- ja kreeditväärtused vahetatakse, kui lisandmoodulit Microsoft Excel kasutatakse koos projekti kulužurnaaliga ja **välja Vastaskonto liik** väärtuseks **on seatud Projekt**. |
| Projektihaldus ja raamatupidamine | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Projektikannetesse sisestatud summa on ülehinnatud projekti ostutellimusel, mis sisaldab ladustatud kaupu ja millel on UseTaxi **märkimisel** mahaarvatavad maksusummad. |
| Projektihaldus ja raamatupidamine | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Süsteem jagab summa projekti kasumiaruande ja projekti lõpetamata toodangu aruannete vahel. |
| Projektihaldus ja raamatupidamine | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Vaba kaubavaru on pärast osaliselt tagastatud kaubanõude korrigeerimist vale. |
| Projektihaldus ja raamatupidamine | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Ressursinimed dubleeritakse Project Operationsis, kui neid Microsoft Projectis redigeeritakse. |
| Projektihaldus ja raamatupidamine | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Kontsernisisesed kuluaruanded, millel on ostureskontro kontsernisisesed kontod hankija arve kulude ootel, sisestatakse esmalt projekti LÕPETAMATA kulu **konteeringu liigile**. Töötlemise ajal sisestatakse hinnangulised kulud eeldatava **kontsernisisese kulu** konteeringu tüübi asemel projekti kulu **konteeringu liigile**. |
| Projektihaldus ja raamatupidamine | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Projekti kulukannete hankija säilitamistulemusi ei kuvata. |
| Projektihaldus ja raamatupidamine | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Ajatabel peab ümardama kandesumma kande valuutas määratud arvu kümnendkohtadeni kõigil raamatupidamisjaotustel ja peažurnaali eraldamiskannetel. |
| Projektihaldus ja raamatupidamine | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Projekti kauba nõuete kogused uuendatakse automaatselt, kui plaanitud tellimused on kinnitatud. |
| Projektihaldus ja raamatupidamine | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Ostutellimuse ettemaksuarvel ei saa kande numbrit, kande tüüpi hankija saldot ja kontonumbrit tühistada. |
| Projektihaldus ja raamatupidamine | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Kontsernisisene hankija arve katkeb hankija arve integreerimise sisselülitamisel. |
| Projektihaldus ja raamatupidamine | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Projekti kulužurnaali loomisel kuvatakse kulusumma väljal **Kreedit**. |
| Projektihaldus ja raamatupidamine | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projektiarvete maksetingimused ei tööta ootuspäraselt. |
| Projektihaldus ja raamatupidamine | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Ajatabeli kanded võidakse uuesti kasutada, kui numbriseeria on seadistatud pidevaks. |
| Projektihaldus ja raamatupidamine | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | Prantsusmaa: käsitsi **kinnipidamise summa** loogika ei vasta **projekti lepinguarve ettepaneku automaatse säilitamise summa** loogikale. |
| Projektihaldus ja raamatupidamine | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Hankija kinnipidamise vabastamisel on kande konteerimisel valed lisaread. |
| Projektihaldus ja raamatupidamine | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | **Kui lehe Arvesoovituse** loomine välja **Arve kuupäev** muudetakse, võib ilmneda järgmine tõrge: "Objekti viidet ei seata objekti eksemplarile". |
| Projektihaldus ja raamatupidamine | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | TSLine'i **töövoo ajatabeli** kinnitamisel ilmneb tõrge ning laupäevaks ja pühapäevaks on ajatabeli poliitika. |
| Projektihaldus ja raamatupidamine | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Algsaldo projekti kauba tüüp jäetakse arvesoovituse kande kokkuvõtetest **välja**, kui arvutatakse arvesoovituse arve kogusumma. |
| Projektihaldus ja raamatupidamine | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Kui projekti tootmistellimuse tarbimiskulu on 0 (null), ilmneb hindamisel järgmine tõrge: "Katse jagada nulliga." |
| Projektihaldus ja raamatupidamine | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Project Timesheet Mobile'i rakendus Android lõpetab reageerimise. Probleem on seotud **TimeEntryDataManageri argumendigaNullException**. |
| Projektihaldus ja raamatupidamine | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Projektitoimingute integratsioonitööleht nurjub selle konteerimisel, kuna kontol puuduvad dimensioonid. Kuid konto, millel puuduvad dimensioonid, ei ole konto, kuhu konteerite. |
| Projektihaldus ja raamatupidamine | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Otsingute **todate-filtrit** ei tühjendata, kui see eemaldatakse lehe Konteeri kulu **dialoogiboksist** **Vali**. |
| Projektihaldus ja raamatupidamine | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Lähtestage kogu levitamine** nurjub ja kuvatakse tõrge ajatabelite puhul, mis on loodud ainult tüübi **Aja projekti** jaoks. |
| Projektihaldus ja raamatupidamine | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Vahekaarti **Projekt** ei saa redigeerida ootel hankija arvel, kui hankekategooria on kaubale määratud. |
| Projektihaldus ja raamatupidamine | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigeerimispaan puudub, kui te pole Project Operationsi Dataverse sisse logitud. |
| Projektihaldus ja raamatupidamine | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Kontsernisiseste projekti korrigeerimiskannete puhul on sihtettevõttes probleeme. |
| Projektihaldus ja raamatupidamine | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Projekti kooskõlastatud kulud arvutavad vale koguse ja omahinna, kui ostutellimust töötles **ostutellimuse aastalõpu protsess** pearaamatus. |
| Projektihaldus ja raamatupidamine | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Kui projekti tootmistellimustega projekti tootmistellimus kinnitatakse lõpetatuks, ilmneb järgmine tõrge: "Laokandega pole märgitud virtuaalset kannet." |
| Projektihaldus ja raamatupidamine | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Projektiga seotud ostureskontro arve konteerimisel ilmneb järgmine tõrge: "Loendatud tekst Projekt - kulu - kaupa pole olemas." |
| Projektihaldus ja raamatupidamine | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Kaudsed kulud kahekordistuvad tulu käsitsi kogumisel. |
| Projektihaldus ja raamatupidamine | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Tulu kogumine ja lõpetamata toodangu sisestamine ei tooda kandeid. |
| Projektihaldus ja raamatupidamine | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Ootel hinna aktiveerimine nurjub standardomahinna kauba puhul, kui vastuvõetud projekti ostutellimus on olemas. |
| Projektihaldus ja raamatupidamine | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Lõpetamata toodanguga ümberpööratud väärtus arve konteerimisest erineb algsest konteeritud WIP väärtusest ajakandest. |
| Projektihaldus ja raamatupidamine | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Projekti arveldatud tulu sisestamisväljamine on rakendatud laopidajate puhul, kus kande kanded ei saldot. |
| Projektihaldus ja raamatupidamine | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Hinnangu loomine pärast arvesoovituse konteerimist blokeerib parandusridade impordi projektitoimingutes. |
| Projektihaldus ja raamatupidamine | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Täielikult arveldatud vahe-eesmärgi kirje muutmine ei tohiks olla võimalik. |
| Projektihaldus ja raamatupidamine | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Automaatsete tasude kasutamisel ei saa ajatabeli kontsernisisest kliendiarvet konteerida ja kuvatakse tõrketeade. |
| Projektihaldus ja raamatupidamine | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Alamprojekti aadressi pole õigesti värskendatud. |
| Projektihaldus ja raamatupidamine | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Kaubanõuete omahinda uuendatakse konsolideeritud ostutellimuste ostuhinnaga. |
| Projektihaldus ja raamatupidamine | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Sisestatud kulu pole õige pärast ostuhinna värskendamist ja parameeter **Aktiveeri muudatuste haldamine** on lubatud. |
| Reisimine ja kulu | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Kõiki kasutajakulusid saab vaadata, kui otsite kategooriat mobiilirakendusest Kulu. |
| Reisimine ja kulu | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Hankijakannete ja käibemaksukannete valed summad sisestatakse krediitkaardikandest loodud kulust. |
| Reisimine ja kulu | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Kuluaruande lehtede värskendamisel kuvatakse ebaoluline hoiatusteade. |
| Reisimine ja kulu | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Ajutise kinnitaja kustutamisel ja seejärel töövoo kaudu uuesti esitamisel kasutatakse valet ajutist kinnitajat. |
| Reisimine ja kulu | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ilmneb sisestusviga, mis on seotud läbisõidu häälestusega. |
| Reisimine ja kulu | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Jaotus ei värskenda juriidilist isikut, kui kontsernisisese kulu kuluaruandesse lisatakse uuesti sidumata kanne. |

### <a name="regulatory-updates"></a>Regulatiivsed uuendused

Finance and Operationsi rakenduste regulatiivsete värskenduste kohta leiate teavet teemast [Regulatiivsed värskendused](/dynamics365/finance/localizations/regulatory-updates). Samuti saate sisse logida elutsükli teenustesse Microsoft Dynamics (LCS) ja kasutada plaanitud regulatiivsete värskenduste vaatamiseks otsingutööriista Issue. Probleemiotsing võimaldab teil otsida riigi või piirkonna, funktsiooni tüübi ja vabastamise järgi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
