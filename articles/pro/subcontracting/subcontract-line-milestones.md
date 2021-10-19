---
title: Allhankelepingu rea vahe-eesmärgid
description: Selles teemas kirjeldatakse, kuidas luua ja hallata vahe-eesmärkidel põhinevat arve ajakava hankijaga sõlmitud allhankelepingu korral.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7f99853f5f649f96225b7d72580db97bb92de7c5
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558497"
---
# <a name="subcontract-line-milestones"></a>Allhankelepingu rea vahe-eesmärgid

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakenduses Dynamics 365 Project Operations saab fikseeritud hinnaga arveldusmeetodiga allhankelepingu rida määrata vahe-eesmärkidel põhineva arve ajakava hankijaga.

Hankija arvelduse vahe-eesmärgid saab luua automaatselt, kasutades määratud sagedust, või saate luua need käsitsi.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Allhankelepingu reale vahe-eesmärgil põhineva arve ajakava automaatne loomine

Läbige järgmised etapid automaatseks võrdselt jaotatud vahe-eesmärkide fikseeritud komplektile vahe-eesmärgil põhineva arve ajakava loomiseks.

1. Avage **Sätted** > **Arve sagedused** ja seadistage arve sagedus allhankelepingu ridade jaoks.
2. Avage leht **Allhankelepingud**, avage see allhankeleping, millega soovite töötada, ning seejärel avage fikseeritud hinnaga allhankelepingu rida, mille jaoks kavatsete vahe-eesmärkide ajakava luua.
3. Tehke vahekaardil **Allhankelepingu rea vahe-eesmärgid** valik **Loo perioodilised vahe-eesmärgid**.
4. Sisestage või valige dialoogiboksis kuupäevavahemik, vahe-eesmärkide arv ja arvete sagedus. Võite valida alguskuupäeva, või võite valida vahe-eesmärkide arvu ja arve sageduse või alguskuupäeva, või võite valida lõpukuupäeva ja arve sageduse. Võite valida lõpukuupäeva ja vahe-eesmärkide arvu.
Selle teabe abil loob süsteem vahe-eesmärgid ja kirjed, mida kuvatakse ruudustikus **Vahe-eesmärgid**.

   - **Vahe-eesmärgi nimi** - vahe-eesmärgi nimi seadistatakse vahe-eesmärgi kuupäevale vastavalt arve sagedusele.
   - **Vahe-eesmärgi kuupäev** – kuupäev vastavalt arve sagedusele.
   - **Vahe-eesmärgi summa** - arvutatamiseks jagatakse allhankelepingu rea vahesumma väärtus vahe-eesmärkide arvuga.

Kui allhankelepingu real on väärtus väljal **Hinnanguline maksusumma**, liidetakse see väärtus perioodiliste vahe-eesmärkide loomisel igale vahe-eesmärgile võrdselt.

Allhankelepingu rea vahe-eesmärkide summade summa peab olema võrdne allhankelepingu rea väärtusega. Kui need pole võrdsed, võib esineda tõrge. Saate vea parandada ja kontrollida, et vahe-eesmärkide summa on võrdne allhankelepingu rea väärtusega vahe-eesmärke ja maksusummasid luues, redigeerides või kustutades. Pärast muudatuste tegemist salvestage ja värskendage lehte, et veenduda täiendavate tõrgete puudumises.

## <a name="manually-create-subcontract-line-milestones"></a>Allhankelepingu vahe-eesmärkide loomine käsitsi

Allhankelepingu fikseeritud hinnaga vahe-eesmärke saab luua käsitsi, kui need ei jagune perioodiliselt. Allhankelepingu rea vahe-eesmärgi käsitsi loomiseks läbige järgmised etapid.

1. Valige navigeerimispaanil **Allhankelepingud** ja avage see allhankeleping, millega soovite töötada.
2. Avage fikseeritud hinnaga allhankelepingu rida, millele tahate vahe-eesmärki luua.
3. Valige vahekaardi **Allhankelepingu rea vahe-eesmärgid** andmeruudustikus **+ Uus allhankelepingu vahe-eesmärk**.
4. Sisestage lehel **Uus allhankelepingu rea vahe-eesmärk** nõutav teave vastavalt järgmisele tabelile.

    | Väli | Kirjeldus |Funktsionaalne mõju|
    | --- | --- |----------------------|
    | Vahekokkuvõtte nimi | Vahe-eesmärgi nimi. |See kuvatakse kõigis otsingutes allhankelepingu ridade vahe-eesmärkide põhjal esimese veeruna. Selle vahe-eesmärgi põhjal loodud hankija arverida kasutab hankija arve vaikimisi nimena ka allhankelepingu rea vahe-eesmärgi nime.|
    | Kirjeldus | Vahe-eesmärgi kirjeldus. |Selle vahe-eesmärgi põhjal loodud hankija arverida kasutab hankija arve vaikimisi kirjeldusena ka allhankelepingu rea vahe-eesmärgi kirjeldust.|
    | Vahekokkuvõtte kuupäev | Kuupäev, millal arve automaatse loomise protsess peaks vaatama selle vahe-eesmärgi olekut, et kaaluda selle arveldamist.| Seda väärtust kasutatakse selle allhankelepingu rea jaoks arve esitamisel hankija arverea vaikimisi kuupäevana. |
    | Summa | Vahe-eesmärgi summa või väärtus, mille eest esitatakse kliendile arve. |Seda väärtust kasutatakse selle allhankelepingu rea jaoks arve esitamisel hankija arverea vaikimisi summana. |
    | Maks | Vahe-eesmärgile rakendatav maksusumma.| Seda väärtust kasutatakse selle allhankelepingu rea jaoks arve esitamisel hankija arverea vaikimisi maksusummana. |
    | Summa pärast maksude mahaarvamist | Seda kirjutuskaitstud välja arvutatakse kui summa + maks.|Seda väärtust kasutatakse selle allhankelepingu rea jaoks arve esitamisel hankija arverea vaikeväärtusena. |
    | Arve olek | Vahe-eesmärgi loomisel on selleks olekuks alati määratud **Pole arveldamiseks valmis**.|  Kui olekuks on **Arveldamiseks valmis**, sisaldab hankija arve loomine hankija arvel seda vahe-eesmärki. |

5. Valige **Salvesta ja sule**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
