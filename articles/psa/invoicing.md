---
title: Rakenduses Project Service Automation arvete esitamine
description: Selles teemas antakse teavet arvete esitamise kohta.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f8107a660f9993c7b6a32d69047a81fb7e0abef8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075020"
---
# <a name="invoicing-in-project-service-automation"></a>Rakenduses Project Service Automation arvete esitamine

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Arvete esitamine rakenduses Dynamics 365 Project Service Automation on kasulik, kuna see annab projekti juhtidele teise taseme heakskiidu, enne kui nad loovad klientidele arveid. Esimene tüübikinnituse tase lõpetatakse, kui projekti meeskonnaliikmete esitamise aja- ja kulukanded kiidetakse heaks.

PSA pole loodud kliendile suunatud arvete loomiseks järgmistel põhjustel.

- See ei sisalda teavet maksude kohta.
- See ei saa muuta muude valuutade arve valuutaks, kasutades õigesti konfigureeritud valuutakursse.
- Arveid ei saa õigesti vormindada, et neid saaks printida.

Selle asemel saate kasutada finants- või raamatupidamissüsteemi, et luua kliendiga seotud arveid, mis kasutavad rakenduses PSA saadud teavet arve ettepanekute kohta.

## <a name="creating-project-invoices-in-psa"></a>Projekti arvete koostamine PSA-s

Projekti arveid saab luua üks korraga või hulgikaupa. Neid saab luua käsitsi või konfigureerida nii, et need luuakse automatiseeritud käitamisel.

### <a name="manually-create-project-invoices-in-psa"></a>Projekti arvete käsitsi koostamine PSA-s

**Projekti lepingute** loendi lehel saate projekti arveid luua eraldi iga projekti lepingu jaoks või luua arveid hulgikaupa mitme projekti lepingu jaoks.

Konkreetse projekti lepingu jaoks arve loomiseks järgige seda etappi.

- Avage **Projekti lepingute** loendi lehel projekti leping ja seejärel valige **Loo arve**.

    ![Projekti arvete loomine konkreetse projekti lepingu jaoks](media/CreateProjectInvoicesOneByOne.png)

    Iga valitud projekti lepingu jaoks luuakse arve, mille olek on **Arveldamiseks valmis**. Need tehingud hõlmavad aega, kulusid, verstaposte ja tootepõhiseid lepinguridu.

Arvete hulgi loomiseks tehke järgmist.

1. Valige **projekti lepingute** loendilehel üks või mitu projekti lepingut, mille jaoks peate arve looma, ja seejärel valige **Loo projekti arved**.

    ![Projekti arvete koostamine hulgikaupa](media/CreateProjectInvoicesBulk.png)

    Hoiatusteade teatab, et enne arvete loomist võib olla viivitus. Protsess kuvatakse ka.

2. Seejärel valige teateboksi sulgemiseks suvand **OK**.

    Iga valitud projekti lepingu jaoks luuakse arve, mille olek on **Arveldamiseks valmis**. Need tehingud hõlmavad aega, kulusid, verstaposte ja tootepõhiseid lepinguridu.

3. Loodud arvete vaatamiseks minge jaotisse **Müügid** \> **Arveldamine** \> **Arved**. Kuvatakse üks arve iga projekti lepingu kohta.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Seadistage projekti arvete automaatne loomine PSA kaudu

Toimige järgmiselt, et konfigureerida PSA-s automatiseeritud arve.

1. Avage **Project Service** \> **Sätted** \> **Pakett-tööd**.
2. Looge pakett-töö ja nimetage see **PSA arveteloomiseks**. Pakett-töö nimi peab sisaldama terminit „arvete loomine”.
3. Valige väljal **Töö tüüp** väärtus **Puudub**. Vaikimisi on suvandite **Sageduse päev** ja **On aktiivne** väärtuseks **Jah**.
4. Valige **Käivita töövoog**. Näete dialoogiboksis **Kirje otsimine** kolme töövoogu.

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Valige **ProcessRunCaller** ja seejärel **Lisa**.
6. Valige järgmises dialoogiboksis **OK**. **Unerežiimi** töövoole järgneb **protsessi** töövoog.

    Etapis 5 saate valida ka töövoo **ProcessRunner**. Seejärel, kui valite **OK** , järgneb **protsessi** töövoole **unerežiimi** töövoog.

Töövood **ProcessRunCaller** ja **ProcessRunner** loovad arveid. **ProcessRunCaller** kutsub töövoo **ProcessRunner**. **ProcessRunner** on töövoog, mis tegelikult loob arveid. See läbib kõik lepinguread, mille jaoks tuleb arved luua, ja see loob neile ridadele arveid. Selleks et määratleda lepingu read, mille jaoks arved tuleb luua, vaatab töö lepingurea arve käivitamise kuupäevi. Kui ühele lepingule kuuluvatel lepinguridadel on sama arve käivitamise päev, kombineeritakse tehingud ühe arvega, millel on kaks arve rida. Kui arvete loomiseks pole kandeid, jätab töö arve loomise vahele.

Kui **ProcessRunner** on töö lõpetanud, kutsub see töövoo **ProcessRunCaller** , annab lõppkellaaja ja sulgub. **ProcessRunCaller** käivitab seejärel taimeri, mis kestab määratud lõppkellaajast 24 tundi. Taimeri lõpus on **ProcessRunCaller** suletud.

Arvete loomiseks kasutatav pakktöötluse töö on korduv töö. Kui seda pakktöötlust käitatakse mitu korda, luuakse mitu tööeksemplari ja need põhjustavad tõrkeid. Seetõttu peaksite pakktöötluse käivitama ainult üks kord ja selle peate uuesti käivitama ainult siis, kui see lakkab töötamast.

> [!NOTE]
> Project Service Automationi paketina arveldamine töötab ainult projekti lepinguridade jaoks, mis on arve ajakavade poolt konfigureeritud. Fikseeritud hinnaga arveldusmeetodiga lepingureal peavad olema seadistatud vahe-eesmärgid. Aja- ja materjalikulu arveldusmeetodiga projekti lepingurea jaoks peab olema seadistatud kuupäevapõhine ajakava. Hinnapakkumise real põhineva projekti kontekstis arveldamise sageduste seadistamise teave on toodud järgmises teemas: [Hinnapakkumised ja hinnapakkumise read](basic-quote-lines.md#invoice-schedule). Sama kehtib ka projektipõhisele lepingureale.      
 
### <a name="edit-a-draft-psa-invoice"></a>PSA arve mustandi redigeerimine

Projekti arve mustandi loomisel pannakse arvele kõik arveldamata müügi tehingud, mis on loodud aja-ja kuluaruannete kinnitamisel. Kui arve on alles mustand, saate teha järgmisi muudatusi.

- Kustutage või redigeerige arve rea üksikasju.
- Saate redigeerida ja kohandada koguse ja arve tüüpi.
- Arvega seotud toimingutena saate lisada otse aja, kulu ja tasu. Seda funktsiooni saate kasutada juhul, kui arve rida on vastendatud lepingureaga, mis lubab neid kandetüüpe.

Arve kinnitamiseks valige **Kinnita**. Kinnitamine on ühesuunaline toiming. Suvandi **Kinnita** valimisel teeb süsteem arve kirjutuskaitstuks ja loob iga arverea kohta iga arverea üksikasjadelt arvestatud müügi tegelikud näitajad. Kui arverea üksikasjad viitavad arveldamata müügi tegelikule näitajale, tühistab süsteem ka arveldamata müügi tegeliku näitaja. (Mis tahes aja- või kulukirje põhjal loodud arve rea üksikasjad viitavad arveldamata müügi tegelikule.) Pearaamatu integreerimise süsteemidega saab seda ümberpööramist kasutada projekti poolelioleva töö lõpetamisel (WIP) raamatupidamise jaoks.

### <a name="correct-a-confirmed-psa-invoice"></a>Kinnitatud PSA arve korrigeerimine

Kinnitatud PSA arveid saab redigeerida (parandatud). Kinnitatud arve parandamisel luuakse uus korrigeeriva arve mustand. Kuna eeldame, et soovite kõik kanded ja kogused algsest arvest ümber pöörata, kaasatakse selle korrigeeriva arve kõik algse arve tehingud ja kõik selle kogused on 0 (null).

Kui mõni kanne ei vaja korrigeerimist, saate need korrigeeriva arve mustandist eemaldada. Kui soovite ainult osalist kogust ümber pöörata või tagastada, saate rea üksikasjade välja **Kogus** redigeerida. Arve rea üksikasjade avamisel näete algse arve kogust. Seejärel saate praegust arve kogust redigeerida nii, et see on algse arve kogusest väiksem või suurem.

Korrigeeriva arve kinnitamisel tühistatakse algselt arvestatud müügi tegelik väärtus ja luuakse uus tegelik arve. Kui kogust on vähendatud, põhjustab erinevus uue arveldamata müügi tegeliku loomise. Näiteks kui algne arvestatud müük oli kaheksa tundi ja korrigeeriva arverea üksikasjadel on vähendatud kogust kuus tundi, pöörab PSA algse arvestatud müügirea ümber ja loob kaks uut tegelikku väärtust.

- Arvestatud müük on tegelikult kuus tundi.
- Ülejäänud kahe tunni eest arveldamata müügi tegelik väärtus. See tehing võib olla kas hiljem arvestatud või märgitud mitte-tasuna, olenevalt läbirääkimistest kliendiga.