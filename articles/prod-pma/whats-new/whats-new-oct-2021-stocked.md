---
title: Mis on uut või mida on muudetud rakenduses Project Operations (2021. aasta oktoober) varutud/tootmispõhiste stsenaariumide jaoks?
description: Selles artiklis antakse teavet kvaliteedivärskenduste kohta, mis on saadaval 2021. aasta oktoobri väljaandes Project Operations for stocked/production-based scenarios.
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
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Mis on uut või mida on muudetud rakenduses Project Operations (2021. aasta oktoober) varutud/tootmispõhiste stsenaariumide jaoks?

_**Kehtib järgmiste puhul:** Project Operations ladustamise-/tootmispõhiste stsenaariumide jaoks_

See artikkel kehtib microsofti järgmiste komponentide ja versioonide kohta Dynamics 365 Project Operations:

- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnas versioon 10.0.22
 
## <a name="quality-updates"></a>Kvaliteedi värskendused

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
|--------------|------------------|----------------|
| Projektihaldus ja raamatupidamine | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Poolelioleva projektitöö (WIP) ja kogunenud tulu summasid ei tühistata kontsernisisese kliendiarve sisestamisel õigesti. |
| Projektihaldus ja raamatupidamine | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Funktsioon **Takista projekti sulgemist, kui avatud kanded on olemas**, ei tööta. |
| Projektihaldus ja raamatupidamine | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Vabas vormis arve arvelduse klassifikatsioon ei sisesta projektide dimensioone automaatselt, kui see funktsioon on lubatud. |
| Projektihaldus ja raamatupidamine | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Kontserniväliste stsenaariumide korral ei tühistata WIP-i ja kogunenud tulu summasid projektiarve sisestamisel õigesti. |
| Projektihaldus ja raamatupidamine | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Deebet- ja kreeditväärtused vahetatakse, Microsoft Excel kui lisandmoodulit kasutatakse koos projekti kulu töölehega ja **välja Vastaskonto tüüp** väärtuseks **on seatud Projekt**. |
| Projektihaldus ja raamatupidamine | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Projektikannetesse sisestatud summa on ülehinnatud projekti ostutellimusel, mis sisaldab ladustatud kaupu ja millel on UseTaxi **märkimisel mahaarvamatud maksusummad**. |
| Projektihaldus ja raamatupidamine | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Süsteem jagab summa projekti kasumiaruande ja projekti WIP-aruannete vahel. |
| Projektihaldus ja raamatupidamine | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Vaba kaubavaru on vale pärast osaliselt tagastatud kauba nõude korrigeerimist. |
| Projektihaldus ja raamatupidamine | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Ressursinimed dubleeritakse rakenduses Project Operations, kui neid redigeeritakse rakenduses Microsoft Project. |
| Projektihaldus ja raamatupidamine | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Kontsernisisesed kuluaruanded, millel on kontsernisisesed ostureskontro ootel hankija arve kulud, **sisestatakse esmalt projekti WIP-i kulu** sisestamise tüüpi. Töötlemise ajal sisestatakse **prognoosiga seotud kulud eeldatava** kontsernisisese kulu sisestamise tüübi asemel projekti kulu **sisestamise** tüüpi. |
| Projektihaldus ja raamatupidamine | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Hankija säilitustulemeid projekti kulukannetes ei kuvata. |
| Projektihaldus ja raamatupidamine | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Ajatabel peab ümardama kande summa kandevaluutas määratud arvu komakohtadeni kõigil raamatupidamislikel jaotustel ja töölehe üldistel eraldamiskirjetel. |
| Projektihaldus ja raamatupidamine | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Projekti kaubanõuete koguseid värskendatakse plaanitud tellimuste kinnitamisel automaatselt. |
| Projektihaldus ja raamatupidamine | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Kande numbrit, kandetüüpi hankija saldot ja kontonumbrit ei saa ostutellimuse ettemaksuarvel tühistada. |
| Projektihaldus ja raamatupidamine | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Kontsernisisene hankijaarve katkeb, kui hankija arve integreerimine on sisse lülitatud. |
| Projektihaldus ja raamatupidamine | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Projekti kulu töölehe loomisel kuvatakse kulusumma väljal **Krediit**. |
| Projektihaldus ja raamatupidamine | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projektiarvete maksetingimused ei tööta ootuspäraselt. |
| Projektihaldus ja raamatupidamine | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Ajatabeli vautšereid võidakse uuesti kasutada, kui numbriseeria on seadistatud pidevaks. |
| Projektihaldus ja raamatupidamine | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | PRANTSUSMAA: **Käsitsi säilitamise summa** loogika ei vasta **projekti lepinguarve ettepaneku automaatse säilitussumma** loogikale. |
| Projektihaldus ja raamatupidamine | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Hankija kinnipidamise vabastamisel on kande sisestamisel valed lisaread. |
| Projektihaldus ja raamatupidamine | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | **Kui lehel Arvesoovituse** loomine muudetakse välja **Arve kuupäev**, võib ilmneda järgmine tõrge: "Objekti viide ei ole määratud objekti eksemplarile." |
| Projektihaldus ja raamatupidamine | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Tõrge ilmneb siis, kui proovite TSLine'i **töövoost ajatabelit** kinnitada ning laupäeva ja pühapäeva jaoks on olemas ajatabeli eeskirjad. |
| Projektihaldus ja raamatupidamine | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Algsaldo projekti kauba tüüp jäetakse arvesoovituse kande kokkuvõtetest **välja**, kui arvutatakse arvesoovituse arve kogusumma. |
| Projektihaldus ja raamatupidamine | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Kui projekti tootmistellimuse tarbimiskulu on 0 (null), ilmneb hindamisel järgmine tõrge: "Prooviti jagada nulliga". |
| Projektihaldus ja raamatupidamine | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Project Timesheet Mobile'i rakendus Android lakkab reageerimast. Probleem on seotud **TimeEntryDataManager ArgumentNullExceptioniga**. |
| Projektihaldus ja raamatupidamine | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Project Operationsi integreerimise tööleht nurjub selle sisestamisel, kuna kontol puuduvad dimensioonid. Kuid konto, millel puuduvad dimensioonid, pole konto, kuhu postitate. |
| Projektihaldus ja raamatupidamine | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Otsingute **filtrit ToDate** ei tühjendata, kui see eemaldatakse **lehe Postitamiskulu** dialoogiboksist **Valimine**. |
| Projektihaldus ja raamatupidamine | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Kogu levitamise lähtestamine** nurjub ja kuvatakse tõrketeade puhul, mis on loodud ainult kellaaja **tüüpi projekti** jaoks. |
| Projektihaldus ja raamatupidamine | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Vahekaarti **Projekt** ei saa redigeerida ootel hankija arvel, kui kaubale on määratud hankekategooria. |
| Projektihaldus ja raamatupidamine | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigeerimispaan puudub, kui te pole rakendusse Project Operations Dataverse sisse logitud. |
| Projektihaldus ja raamatupidamine | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Kontsernisiseste projekti korrigeerimise kannete puhul on sihtettevõttes probleeme. |
| Projektihaldus ja raamatupidamine | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Projekti kinnitatud kulud arvutavad vale koguse ja omahinna, kui ostutellimust töödeldi ostutellimuse aastalõpu protsessiga **pearaamatus**. |
| Projektihaldus ja raamatupidamine | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Kui kvaliteettellimustega projekti tootmistellimus on lõpetatuks märgitud, ilmneb järgmine tõrge: "Laokandega märgitud virtuaalset kannet pole". |
| Projektihaldus ja raamatupidamine | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Projektiga seotud ostureskontro arve sisestamisel ilmneb järgmine tõrge: "Loetletud tekst Projekt - kulu - kaup pole olemas." |
| Projektihaldus ja raamatupidamine | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Kaudsed kulud kahekordistuvad, kui kogute tulu käsitsi. |
| Projektihaldus ja raamatupidamine | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Viitlaekumised ja WIP-i sisestamine ei tooda kandeid. |
| Projektihaldus ja raamatupidamine | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Ootel hinna aktiveerimine nurjub standardse kuluartikli puhul, kui saadud projekti ostutellimus on olemas. |
| Projektihaldus ja raamatupidamine | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Arve sisestamise WIP-i ümberpööratud väärtus erineb algsest sisestatud WIP-väärtusest ajakirjest. |
| Projektihaldus ja raamatupidamine | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Projekti arvega tulu puhul on sisestusväljaanne rakendatud käsiraha juhtudel, kui kande kanded ei saldoteeri. |
| Projektihaldus ja raamatupidamine | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Hinnangu loomine pärast arvesoovituse sisestamist blokeerib parandusridade impordi projektitoimingutes. |
| Projektihaldus ja raamatupidamine | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Täielikult arveldatud-eesmärkide kirje muutmine ei tohiks olla võimalik. |
| Projektihaldus ja raamatupidamine | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Kui kasutatakse automaatseid tasusid, ei saa ettevõttesisest kliendiarvet ajatabeli eest sisestada ja kuvatakse tõrketeade. |
| Projektihaldus ja raamatupidamine | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Alamprojekti aadressi ei värskendata õigesti. |
| Projektihaldus ja raamatupidamine | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Kaubanõuete omahinda värskendatakse konsolideeritud ostutellimuste ostuhinnaga. |
| Projektihaldus ja raamatupidamine | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Sisestatud kulu ei ole õige pärast seda, kui ostuhind on värskendatud ja parameeter **Aktiveeri muudatuste haldus** on lubatud. |
| Reisimine ja kulu | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Kõik kasutajakulud on nähtavad, kui otsite kategooriat kulu mobiilirakenduses. |
| Reisimine ja kulu | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Hankijakannete ja käibemaksukannete valed summad sisestatakse krediitkaardikandest loodud kulust. |
| Reisimine ja kulu | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Kuluaruande lehtede värskendamisel kuvatakse ebaoluline hoiatusteade. |
| Reisimine ja kulu | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Valet vahepealset kinnitajat kasutatakse siis, kui kustutate ajutise kinnitaja ja seejärel esitate selle uuesti töövoo kaudu. |
| Reisimine ja kulu | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ilmneb sisestustõrge, mis on seotud läbisõidu seadistusega. |
| Reisimine ja kulu | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Jaotus ei värskenda juriidilist isikut, kui kontsernisisese kulu kuluaruandesse lisatakse uuesti tegemata kanne. |

### <a name="regulatory-updates"></a>Regulatiivsed uuendused

Lisateavet finance and operationsi rakenduste regulatiivsete värskenduste kohta leiate teemast [Regulatiivsed värskendused](/dynamics365/finance/localizations/regulatory-updates). Samuti saate sisse logida teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja kasutada probleemiotsingu tööriista plaanitud regulatiivsete värskenduste vaatamiseks. Probleemiotsing võimaldab teil otsida riigi või piirkonna, funktsiooni tüübi ja väljalaske järgi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
