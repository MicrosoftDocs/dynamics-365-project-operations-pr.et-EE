---
title: Projekti näidisarved
description: See teema sisaldab teavet Project Operationsi projekti näidisarvete kohta.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3d02728ce682781eb8816e0c2239cf62f88adfa8c5d2a0aab280be053c2a5ae6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992921"
---
# <a name="proforma-project-pnvoices"></a>Projekti näidisarved

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Projekti näidisarveldamine annab projektijuhtidele teise taseme heakskiidu, enne kui nad loovad klientidele arveid. Esimene tüübikinnituse tase lõpetatakse, kui projekti meeskonnaliikmete esitamise aja-, kulu- ja materjalikanded kiidetakse heaks.

Rakenduse Dynamics 365 Project Operations lihtjuurutamine ei ole mõeldud kliendile suunatud arvete loomiseks. Järgmine loend näitab, miks arveid ei saa luua.

- Ei sisalda teavet maksude kohta.
- Muid valuutasid ei saa arveldusvaluutasse teisendada.
- Arveid ei saa printimiseks õigesti vormindada.

Selle asemel saate kasutada finants- või raamatupidamissüsteemi, et luua kliendiga seotud arveid, mis kasutavad loodud arve ettepanekutes sisalduvat teavet.

## <a name="creating-project-invoices"></a>Projekti arvete koostamine

Projekti arveid saab luua üks korraga või hulgikaupa. Neid saab luua käsitsi või konfigureerida nii, et need luuakse automatiseeritud käitamisel.

### <a name="manually-create-project-invoices"></a>Projekti arvete käsitsi koostamine 

**Projektilepingute** loendi lehel saate projekti arveid luua eraldi iga projektilepingu jaoks või luua arveid hulgikaupa mitme projektilepingu jaoks.

   - Konkreetse projektilepingu jaoks arve loomiseks lehel **Projektilepingud** avage projektileping ja valige seejärel suvand **Loo arve**.

   Iga valitud projekti lepingu jaoks luuakse arve, mille olek on **Arveldamiseks valmis**. Need tehingud hõlmavad aega, kulusid, materjale, vahe-etappe, tootepõhiseid lepinguridu ja teisi arveldamata müügi töölehe kandeid, mis võivad olla kinnitatud.

Arvete hulgi loomiseks tehke järgmist.

1. Valige **projektilepingute** loendilehel üks või mitu projektilepingut, et luua arve, ja seejärel valige **Loo projektiarved**.
2. Hoiatusteade teatab, et enne arvete loomist võib olla viivitus. Protsess kuvatakse ka. Seejärel valige teateboksi sulgemiseks suvand **OK**.

   Iga valitud projekti lepingu jaoks luuakse arve, mille olek on **Arveldamiseks valmis**. Need tehingud hõlmavad aega, kulusid, materjale, vahe-etappe, tootepõhiseid lepinguridu ja teisi arveldamata müügi töölehe kandeid, mis võivad olla kinnitatud.

3. Vaadake loodud arveid, minnes jaotisse **Müügid** \> **Arveldamine** \> **Arved**. Kuvatakse üks arve iga projekti lepingu kohta.

### <a name="set-up-automated-creation-of-project-invoices"></a>Projekti arvete automaatse loomise häälestamine 

Toimige järgmiselt, et konfigureerida automatiseeritud arve.

1. Avage **Sätted** \> **Pakett-tööd**.
2. Looge pakett-töö ja pange sellele nimeks **Project Operationsi arvete loomine**. Pakett-töö nimi peab sisaldama terminit „arvete loomine”.
3. Valige väljal **Töö tüüp** väärtus **Puudub**. Vaikimisi on suvandite **Sageduse päev** ja **On aktiivne** väärtuseks **Jah**.
4. Valige **Käivita töövoog**. Dialoogiboksis **Kirje otsimine** näete järgmisi töövoogusid.

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Valige **ProcessRunCaller** ja seejärel **Lisa**.
6. Valige järgmises dialoogiboksis **OK**. **Unerežiimi** töövoole järgneb **protsessi** töövoog.

    Etapis 5 saate valida ka töövoo **ProcessRunner**. Seejärel, kui valite **OK**, järgneb **protsessi** töövoole **unerežiimi** töövoog.

Töövood **ProcessRunCaller** ja **ProcessRunner** loovad arveid. **ProcessRunCaller** kutsub töövoo **ProcessRunner**. **ProcessRunner** on töövoog, mis loob arveid. See töövoog läbib kõik lepinguread, mille jaoks tuleb arved luua, ja loob arved. Lepinguridade määratlemiseks, mille jaoks arved tuleb luua, vaatab töövoog lepingurea arve käivitamise kuupäevi. Kui ühele lepingule kuuluvatel lepinguridadel on sama arve käivitamise päev, kombineeritakse tehingud ühe arvega, millel on kaks arve rida. Kui arvete loomiseks pole kandeid, ühtegi arvet ei looda.

Kui **ProcessRunner** on töö lõpetanud, kutsub see töövoo **ProcessRunCaller**, annab lõppkellaaja ja sulgub. **ProcessRunCaller** käivitab seejärel taimeri, mis kestab määratud lõppkellaajast 24 tundi. Taimeri lõpus on **ProcessRunCaller** suletud.

Arvete loomiseks kasutatav pakktöötluse töö on korduv töö. Kui seda pakett-töötlust käitatakse mitu korda, luuakse mitu tööeksemplari ja need võivad põhjustada tõrkeid. Probleemi lahendamiseks käivitage pakett-töö ainult üks kord ja käivitage see ainult siis, kui see lakkab töötamast.

> [!NOTE]
> Pakett-arveldamine töötab ainult projekti lepinguridade jaoks, mis on arvegraafikute poolt konfigureeritud. Fikseeritud hinnaga arveldusmeetodiga lepingureal peavad olema seadistatud vahe-eesmärgid. Aja- ja materjalikulu arveldusmeetodiga projekti lepingurea jaoks peab olema seadistatud kuupäevapõhine ajakava. Sama kehtib ka projektipõhisele lepingureale.      
 
### <a name="edit-a-draft-invoice"></a>Arve mustandi redigeerimine

Projekti arve mustandi loomisel pannakse arvele kõik arveldamata müügi tehingud, mis on loodud aja-ja kuluaruannete kinnitamisel. Kui arve on alles mustand, saate teha järgmisi muudatusi.

- Kustutage või redigeerige arve rea üksikasju.
- Saate redigeerida ja kohandada koguse ja arve tüüpi.
- Arvega seotud toimingutena saate lisada otse aja, kulu, materjali ja tasu. Seda funktsiooni saate kasutada juhul, kui arve rida on vastendatud lepingureaga, mis lubab neid kandetüüpe.

Arve kinnitamiseks valige **Kinnita**. See toiming on ühesuunaline toiming. Suvandi **Kinnita** valimisel muutub arve kirjutuskaitstuks ja loob iga arverea kohta iga arverea üksikasjadelt arvestatud müügi tegelikud näitajad. Kui arverea üksikasjad viitavad arveldamata müügi tegelikule näitajale, arveldamata müügi tegelik näitaja pööratakse ümber. Kõikidele aja, kulu või materjali kasutuskirjetele viidatakse arveldamata müügi tegelikele näitajatele. Pearaamatu integreerimissüsteemid saavad kasutada seda tagasipööramist, et pöörata projekti töö edenemine (WIP) raamatupidamise eesmärgil ümber.

### <a name="correct-a-confirmed-invoice"></a>Kinnitatud arve parandmine

Kinnitatud arveid saab muuta. Kinnitatud arve parandamisel luuakse uus korrigeeriva arve mustand. Kuna eeldame, et soovite kõik kanded ja kogused algsest arvest ümber pöörata, kaasatakse selle korrigeeriva arve kõik algse arve tehingud ja kõik selle kogused on null.

Kui leidub kandeid, mis ei vaja korrigeerimist, saate need korrigeeriva arve mustandist eemaldada. Kui soovite ainult osalist kogust ümber pöörata või tagastada, saate rea üksikasjade välja **Kogus** redigeerida. Arve rea üksikasjade avamisel näete algse arve kogust. Seejärel saate praegust arve kogust redigeerida nii, et see on algse arve kogusest väiksem või suurem.

Korrigeeriva arve kinnitamisel tühistatakse algselt arvestatud müügi tegelik väärtus ja luuakse uus tegelik arve. Kui kogust on vähendatud, põhjustab erinevus uue arveldamata müügi tegeliku loomise. Näiteks kui algne arvestatud müük oli kaheksa tundi ja parandatud arverea üksikasjadel on vähendatud kogust kuus tundi, pööratakse algne arvestatud müügirida ümber ja luuakse kaks uut tegelikku väärtust.

- Arvestatud müük on tegelikult kuus tundi.
- Ülejäänud kahe tunni eest arveldamata müügi tegelik väärtus. See tehing võib olla hiljem arvestatud või märgitud kui tasuta, olenevalt läbirääkimistest kliendiga.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
