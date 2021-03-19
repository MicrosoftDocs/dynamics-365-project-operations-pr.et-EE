---
title: Arve automaatse loomise konfigureerimine
description: Selles teemas antakse teavet, kuidas konfigureerida süsteemi, et luua arveid automaatselt.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0dddd963e79f8ecd91a96a6e684ab79e1b95bd6d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287908"
---
# <a name="configure-automatic-invoice-creation"></a>Arve automaatse loomise konfigureerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_


Läbige järgmised etapid, et konfigureerida Dynamics 365 Project Operationsis automaatne arve käitamine.

1. Avage **Sätted** > **Pakett-tööd**.
2. Looge pakett-töö ja pange sellele nimeks **Projecti toimingute arvete loomine**. Pakett-töö nimi peab sisaldama sõnu „arvete loomine”.
3. Valige väljal **Töö tüüp** väärtus **Puudub**. Vaikimisi on suvandite **Sageduse päev** ja **On aktiivne** väärtuseks **Jah**.
4. Valige **Käivita töövoog**. Näete dialoogiboksis **Kirje otsimine** kolme töövoogu.

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Valige **ProcessRunCaller** ja seejärel **Lisa**.
6. Valige järgmises dialoogiboksis **OK**. **Unerežiimi** töövoole järgneb **protsessi** töövoog.

  > [!NOTE]
  > Etapis 5 saate valida ka töövoo **ProcessRunner**. Seejärel, kui valite **OK**, järgneb **protsessi** töövoole **unerežiimi** töövoog.

Töövood **ProcessRunCaller** ja **ProcessRunner** loovad arveid. **ProcessRunCaller** kutsub töövoo **ProcessRunner**. **ProcessRunner** on töövoog, mis tegelikult loob arveid. See läbib kõik lepinguread, mille jaoks tuleb arved luua, ja see loob neile ridadele arveid. Selleks et määratleda lepingu read, mille jaoks arved tuleb luua, vaatab töö lepingurea arve käivitamise kuupäevi. Kui ühele lepingule kuuluvatel lepinguridadel on sama arve käivitamise päev, kombineeritakse tehingud ühe arvega, millel on kaks arve rida. Kui arvete loomiseks pole kandeid, jätab töö arve loomise vahele.

Kui **ProcessRunner** on töö lõpetanud, kutsub see töövoo **ProcessRunCaller**, annab lõppkellaaja ja sulgub. **ProcessRunCaller** käivitab seejärel taimeri, mis kestab määratud lõppkellaajast 24 tundi. Taimeri lõpus on **ProcessRunCaller** suletud.

Arvete loomiseks kasutatav pakktöötluse töö on korduv töö. Kui seda pakktöötlust käitatakse mitu korda, luuakse mitu tööeksemplari ja need põhjustavad tõrkeid. Seetõttu peaksite pakktöötluse käivitama ainult üks kord ja selle peate uuesti käivitama ainult siis, kui see lakkab töötamast.

> [!NOTE]
> Pakett-arveldamine töötab ainult projekti lepinguridade jaoks, mis on arvegraafikute poolt konfigureeritud. Fikseeritud hinnaga arveldusmeetodiga lepingureal peavad olema seadistatud vahe-eesmärgid. Aja- ja materjalikulu arveldusmeetodiga projekti lepingurea jaoks peab olema seadistatud kuupäevapõhine ajakava. Sama kehtib ka projektipõhisele lepingureale.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]