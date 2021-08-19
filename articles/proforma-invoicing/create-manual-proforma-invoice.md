---
title: Näidisarved
description: See teema sisaldab teavet Project Operationsi näidisarvete kohta.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2050a313fe530065341410d60801b13eb958cb32ae24eb4a0a71ab7ea5061881
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995621"
---
# <a name="proforma-invoices"></a>Näidisarved

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Näidisarveldamine annab projektijuhtidele teise taseme heakskiidu, enne kui nad loovad klientidele arveid. Esimene tüübikinnituse tase lõpetatakse, kui projekti meeskonnaliikmete esitamise aja-, kulu- ja materjalikanded kiidetakse heaks. Kinnitatud näidisarved on saadaval Project Operationsi projekti raamatupidamise moodulis. Projekti raamatupidajad saavad teha täiendavaid värskendusi, näiteks müügimaks, raamatupidamine ja arve paigutus.


## <a name="creating-project-invoices"></a>Projekti arvete koostamine

Projekti arveid saab luua üks korraga või hulgikaupa. Neid saab luua käsitsi või konfigureerida nii, et need luuakse automatiseeritud käitamisel.

### <a name="manually-create-project-invoices"></a>Projekti arvete käsitsi koostamine 

**Projekti lepingute** loendi lehel saate projekti arveid luua eraldi iga projekti lepingu jaoks või luua arveid hulgikaupa mitme projekti lepingu jaoks.

Konkreetse projekti lepingu jaoks arve loomiseks järgige seda etappi.

- Avage **Projekti lepingute** loendi lehel projekti leping ja seejärel valige **Loo arve**.

    Iga valitud projekti lepingu jaoks luuakse arve, mille olek on **Arveldamiseks valmis**. Need tehingud hõlmavad aega, kulusid, materjale, vahe-etappe ja teisi arveldamata müügi töölehe kandeid.

Arvete hulgi loomiseks tehke järgmist.

1. Valige **projekti lepingute** loendilehel üks või mitu projekti lepingut, mille jaoks peate arve looma, ja seejärel valige **Loo projekti arved**.

    Hoiatusteade teatab, et enne arvete loomist võib olla viivitus. Protsess kuvatakse ka.

2. Seejärel valige teateboksi sulgemiseks suvand **OK**.

    Iga valitud projekti lepingu jaoks luuakse arve, mille olek on **Arveldamiseks valmis**. Need tehingud hõlmavad aega, kulusid, materjale, vahe-etappe ja teisi arveldamata müügi töölehe kandeid.

3. Loodud arvete vaatamiseks minge jaotisse **Müügid** \> **Arveldamine** \> **Arved**. Kuvatakse üks arve iga projekti lepingu kohta.

### <a name="set-up-automated-creation-of-project-invoices"></a>Projekti arvete automaatse loomise häälestamine 

Toimige järgmiselt, et konfigureerida automatiseeritud arve.

1. Avage **Sätted** \> **Pakett-tööd**.
2. Looge pakett-töö ja pange sellele nimeks **Project Operationsi arvete loomine**. Pakett-töö nimi peab sisaldama terminit „arvete loomine”.
3. Valige väljal **Töö tüüp** väärtus **Puudub**. Vaikimisi on suvandite **Sageduse päev** ja **On aktiivne** väärtuseks **Jah**.
4. Valige **Käivita töövoog**. Näete dialoogiboksis **Kirje otsimine** kolme töövoogu.

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Valige **ProcessRunCaller** ja seejärel **Lisa**.
6. Valige järgmises dialoogiboksis **OK**. **Unerežiimi** töövoole järgneb **protsessi** töövoog.

    Etapis 5 saate valida ka töövoo **ProcessRunner**. Seejärel, kui valite **OK**, järgneb **protsessi** töövoole **unerežiimi** töövoog.

Töövood **ProcessRunCaller** ja **ProcessRunner** loovad arveid. **ProcessRunCaller** kutsub töövoo **ProcessRunner**. **ProcessRunner** on töövoog, mis tegelikult loob arveid. See läbib kõik lepinguread, mille jaoks tuleb arved luua, ja see loob neile ridadele arveid. Selleks et määratleda lepingu read, mille jaoks arved tuleb luua, vaatab töö lepingurea arve käivitamise kuupäevi. Kui ühele lepingule kuuluvatel lepinguridadel on sama arve käivitamise päev, kombineeritakse tehingud ühe arvega, millel on kaks arve rida. Kui arvete loomiseks pole kandeid, jätab töö arve loomise vahele.

Kui **ProcessRunner** on töö lõpetanud, kutsub see töövoo **ProcessRunCaller**, annab lõppkellaaja ja sulgub. **ProcessRunCaller** käivitab seejärel taimeri, mis kestab määratud lõppkellaajast 24 tundi. Taimeri lõpus on **ProcessRunCaller** suletud.

Arvete loomiseks kasutatav pakktöötluse töö on korduv töö. Kui seda pakktöötlust käitatakse mitu korda, luuakse mitu tööeksemplari ja need põhjustavad tõrkeid. Seetõttu peaksite pakktöötluse käivitama ainult üks kord ja selle peate uuesti käivitama ainult siis, kui see lakkab töötamast.

> [!NOTE]
> Pakett-arveldamine töötab ainult projekti lepinguridade jaoks, mis on arvegraafikute poolt konfigureeritud. Fikseeritud hinnaga arveldusmeetodiga lepingureal peavad olema seadistatud vahe-eesmärgid. Aja- ja materjalikulu arveldusmeetodiga projekti lepingurea jaoks peab olema seadistatud kuupäevapõhine ajakava. Sama kehtib ka projektipõhisele lepingureale.      
 
### <a name="edit-a-draft-invoice"></a>Arve mustandi redigeerimine

Projekti arve mustandi loomisel pannakse arvele kõik arveldamata müügitehingud, mis loodi aja, kulu ja materjali kasutuse kirjete kinnitamisel. Kui arve on alles mustand, saate teha järgmisi muudatusi.

- Kustutage või redigeerige arve rea üksikasju.
- Saate redigeerida ja kohandada koguse ja arve tüüpi.

Arve kinnitamiseks valige **Kinnita**. Kinnitamine on ühesuunaline toiming. Suvandi **Kinnita** valimisel teeb süsteem arve kirjutuskaitstuks ja loob iga arverea kohta iga arverea üksikasjadelt arvestatud müügi tegelikud näitajad. Kui arverea üksikasjad viitavad arveldamata müügi tegelikule näitajale, tühistab süsteem ka arveldamata müügi tegeliku näitaja. (Mis tahes aja- või kulukirje põhjal loodud arve rea üksikasjad viitavad arveldamata müügi tegelikule.) Pearaamatu integreerimise süsteemidega saab seda ümberpööramist kasutada projekti poolelioleva töö lõpetamisel (WIP) raamatupidamise jaoks.

### <a name="correct-a-confirmed-invoice"></a>Kinnitatud arve parandmine

Kinnitatud PSA arveid saab muuta (parndada). Kinnitatud arve parandamisel luuakse uus korrigeeriva arve mustand. Kuna eeldame, et soovite kõik kanded ja kogused algsest arvest ümber pöörata, kaasatakse selle korrigeeriva arve kõik algse arve tehingud ja kõik selle kogused on 0 (null).

Kui mõni kanne ei vaja korrigeerimist, saate need korrigeeriva arve mustandist eemaldada. Kui soovite ainult osalist kogust ümber pöörata või tagastada, saate rea üksikasjade välja **Kogus** redigeerida. Arve rea üksikasjade avamisel näete algse arve kogust. Seejärel saate praegust arve kogust redigeerida nii, et see on algse arve kogusest väiksem või suurem.

Korrigeeriva arve kinnitamisel tühistatakse algselt arvestatud müügi tegelik väärtus ja luuakse uus tegelik arve. Kui kogust on vähendatud, põhjustab erinevus uue arveldamata müügi tegeliku loomise. Näiteks kui algne arvestatud müük oli kaheksa tundi ja parandatud arverea üksikasjadel on vähendatud kogust kuus tundi, pööratakse algne arvestatud müügirida ümber ja luuakse kaks uut tegelikku väärtust.

- Arvestatud müük on tegelikult kuus tundi.
- Ülejäänud kahe tunni eest arveldamata müügi tegelik väärtus. See tehing võib olla kas hiljem arvestatud või märgitud mitte-tasuna, olenevalt läbirääkimistest kliendiga.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
