---
title: Maksa-kui-on-makstud hankija maksete seadistamine ja kasutamine
description: Selles teemas kirjeldatakse, kuidas luua maksa-kui-on-makstud (PWP) tingimusi, et saaksite vabastada osalisi hankija makseid vastavalt kliendi maksetele.
author: RadhikaRS
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 9976dadf57f1c84bf3f295ff3c8359c16e4849a3bf887f8bd33e46a04e2a5952
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008851"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Maksa-kui-on-makstud hankija maksete seadistamine ja kasutamine

[!include [banner](../includes/banner.md)]

Kui kinnitate hankija alltöövõtjana töötamiseks, võite soovida hoida hankijale tehtavaid makseid kinni, kuini klient on teile projekti eest tasunud. Selle stsenaariumi toetamiseks saate ostutellimuse (PO) seadistamisel hankijaga seadistada maksa-kui-on-makstud (PWP) tingimused.

Näiteks kui klient maksab projekti arve summa, saate vabastada osa või kõik hankija arve summad. Lihtsalt seadistage PWP tingimused, mis määravad, et hankijale makstakse pärast seda, kui olete saanud kliendilt protsendi seotud maksest. Kui saate kliendilt osalise makse, saate käsitsi vabastada mõned seostuvad hankija arved maksmiseks.

Järgmises näites kirjeldatakse protsessi PWP tingimuste kasutamisel.

## <a name="example"></a>Näide

Teie organisatsioon nõustub pakkuma kliendile 100 arvutit, millele paigaldatakse tarkvara, hinnaga 150.00 USD arvuti kohta. Seejärel palkate hankija, kes tarnib teile installitud tarkvaraga arvutid. Vastavalt lepingule peab klient enne teie organisatsioonile tasumist kinnitama arvutite kvaliteedi. Teie organisatsiooni poliitika on hoida kinni makset hankijale seni, kuni klient on teile tasunud. Seega saate seadistada projekti nii, et selle PWP protsent on 100 protsenti.

Hankija saadab teile 100 installitud tarkvaraga arvutit koos arvega summale 10 000.00 USD. Kuna teie projekti jaoks on seadistatud PWP tingimused, ei maksa te hankijale pärast arvutite kättesaamist. Selle asemel saadate arvutid kliendile koos arvega summas 15 000.00. Klient kontrollib arvuteid ja kinnitab projekti arve kogu summa.

Pärast kliendilt täieliku makse laekumist tasute hankijale kogu hankija arve summas 10 000.00.

## <a name="set-up-pwp-terms-for-a-project"></a>Projektile PWP tingimuste seadistamine

Projektile PWP tingimuste seadistamisel peate määrama protsendina minimaalse summa, mille klient peab teile projekti eest maksma enne, kui tasute hankijale. Lävesumma arvutatakse automaatselt vastavalt projekti kliendi arvetele. PWP tingimustele läveprotsendi seadistamiseks tehke järgmist.

1. Minge jaotisse **Projektijuhtimine ja raamatupidamine** \> **Projektid** \> **Kõik projektid**.
2. Leidke ja avage projekt, mille jaoks soovite PWP tingimused seadistada.
3. Valige kiirvahekaardil **Hankija lepingud** käsk **Lisa rida**.
3. Valige väljal **Konto kood** üks järgmistest suvanditest.

    - **Tabel** - PWP tingimused rakenduvad ühele hankijale.
    - **Rühm** - hankija PWP tingimused rakenduvad kõigile hankijarühma hankijatele.
    - **Kõik** - hankija PWP tingimused rakenduvad kõikidele hankijatele.

4. Kui valisite eelmises etapis suvandi **Tabel** või **Rühm** väljal **Hankija/hankijate rühm**, valige hankija või hankijate rühm, kellele PWP tingimused rakenduvad. Kui valisite eelmises etapis suvandi **Kõik**, ei saa välja **Hankija/hankijate rühm** redigeerida.
5. Kui hankija jaoks on projektis väljal **Hankija kinnipidamise tingimused** seadistatud kinnipidamise tingimused, valige kinnipidamise tingimustele reegli ID.
6. Sisestage väljale **PWP läve protsent** projekti läve protsent. Projektile sisestatav protsent määrab minimaalse summa, mille klient peab teile maksma, enne kui teie maksate hankijale.

## <a name="create-a-po-that-has-pwp-terms"></a>PWP tingimustega ostutellimuse loomine

Kui sisestate hankija arve ja kui hankija suhtes kehtivad PWP tingimused, kuvatakse neid tingimusi ostutellimuse ridadel. PWP tingimustega ostutellimuse loomiseks toimige järgmiselt.

1. Minge jaotisse **Hanked** \> **Ostutellimused** \> **Kõik ostutellimused**.
2. Valige toimingupaanil suvand **Uus**. Seejärel sisestage dialoogiaknasse **Ostutellimuse loomine** nõutav teave ja valige **OK**.

    Teise võimalusena avage olemasolev ostutellimus loendis **Kõik ostutellimused**.

4. Vaadake lehe **Ostutellimus** kiirvahekaardil **Ostutellimuse read** üle hankija ostutellimuse rea andmed. Suvand **Maksa kui on makstud** valitakse automaatselt ja välja **PWP läve protsent** väärtus kopeeritakse automaatselt väljalt **PWP läve protsent** lehel **Projektid**.
6. Kui te ei soovi hankijale ostutellimuse rea jaoks PWP tingimusi rakendada, tühjendage valik **Maksa kui on makstud**. Sel juhul lähetestatakse ostutellimuse rea väli **PWP läve protsent** väärtusele 0 (null).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Kliendi makse värskendamine ja hankijale tasumine

Kui hankija lõpetab töö projektiga ja saadab teile arve, peate projekti oleku ja klientide arved üle vaatama, et tuvastada, kas projekti PWP tingimused on täidetud. Kui hankija PWP tingimused on täidetud, saate tuvastada, millised hankija arve read vastavalt kliendi maksetele projekti eest tuleb tasuda. Kui otsustate hankijale maksta ka juhul, kui PWP tingimusi ei täidetud, saate PWP tingimused lehel **Hankija arve maksa kui on makstud tingimustega** alistada.

1. Minge jaotisse **Projektijuhtimine ja raamatupidamine** \> **Päringud ja aruanded** \> **Kinnipidamise päringud** \> **Hankija arve maksa kui on makstud tingimustega**.
2. Sisestage lehe **Hankija arved maksa kui on makstud tingimustega** otsinguvälja väärtused, et leida hankija arve, mida soovite üle vaadata, ja seejärel valige **Otsi**.
3. Valige kiirvahekaardil **Hankija arve read** need read, mida soovite muuta.
4. Kui **Maksa kui on makstud** tingimused on arve rea kohta täidetud, valige **Vabasta hankija makse**. Valik **Maksa kui on makstud** kustutatakse ja välja **Maksmiseks valmis** väärtus muudetakse olekusse **Jah**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]