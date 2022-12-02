---
title: Üksuse nõuded mitme rahastamise allikaga projektilepingutele
description: Selles artiklis kirjeldatakse, kuidas konfigureerida ja kasutada üksuste nõudeid mitme allikaga.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028468"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Üksuse nõuded mitme rahastamise allikaga projektilepingutele

_**Kehtib järgmiste puhul:** Project Operations ladustamise-/tootmispõhiste stsenaariumide jaoks_

Mõned lepingulised kokkulepped projektipõhiste tulemuste kohta võivad nõuda mitut rahastamisallikat. See artikkel selgitab, kuidas valida ja konfigureerida soovitud rahastamisallikad, kui projekti või hankelepingu jaoks on vaja mitut allikat.

## <a name="terminology"></a>Mõisted

- **Rahastamisallikas** – olem, mis rahastab projekti lepingulist tööd. See olem võib olla siseorganisatsioon või väline arvelduskonto (klient või toetus).
- **Projekti klient** – isik, kellele projektitöö üle antakse.
- **Arvelduskonto** – väline olem, kes maksab projektitööde eest.

## <a name="example"></a>Näide

Contoso on võitnud seadmete värskendamise lepingu kahe oma kliendiga: Adatum US ja Adatum Corporate. Leping hõlmab riistvara ja paigaldusteenuseid, mis tarnitakse Adatum US-le (projekti klient). Riistvara rahastab Adatum Corporate (arvelduskonto 1) ja paigaldustöid rahastab Adatum US (arvelduskonto 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Seadistage arvelduskonto vaikereeglid kaubanõuete jaoks

### <a name="prerequisites"></a>eeltingimused

- Rakenduse Microsoft Dynamics 365 Finance **versioon 10.0.27 või uuem** on nõutav, et kasutada mitut arvelduskontot sisaldavaid kaubanõudeid.
- Teie süsteemiadministraator peab lubama **Kaubanõuete lubamine mitme rahastamisallikaga Project Operations lao-/tootmispõhiste stsenaariumide jaoks** funktsiooni **Funktsioonihaldus** tööruumis.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Seadistage arvelduskonto vaikereeglid

Arvelduskonto vaikereeglite seadistamiseks järgige järgmisi samme.

1. Avage jaotis **Projektijuhtimine ja raamatupidamine** \> **Seadistamine** \> **Projektijuhtimise ja raamatupidamise parameetrid**.
1. Seadke vahekaardil **Üldine** jaotises **Müügitellimused ja kaubanõuded** valikuks **Mitme rahastamisallikaga projektidele lubamine** valikuks **Jah**.
1. Väljal **Vaikeklient** määrake, kust on vaikimisi pärit objekti tarneklient:

    - **Rahastamisallikast** – projekti tarnimise vaieklient pärineb rahastamisallikast. Kui projektilepinguga on seotud mitu rahastamisallikat, kasutatakse loendi esimest rahastamisallikat.
    - **Projektist** – vaikeprojekti tarnimise klient pärineb kliendist, mis on valitud väljal **Projektikirje konto**.

1. Valikuline: määrake või muutke projektikirjetes vaikearvelduskontot.

    1. Minge jaotisesse **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Kõik projektid** ja a avage projektikirje üksikasjad.
    2. Määrake või värskendage vahekaardil **Üldine** väli **Vaikearvelduskonto**. Teie määratud kontot kasutatakse projekti jaoks loodud uute kaubanõuete jaoks vaikearvelduskontona. Kui jätate välja tühjaks, kasutatakse vaikimisi esimese projektilepingu rahastamisallika arvelduskontot. Kasutajad saavad aga kirje salvestamisel kontot muuta.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Valige kaubanõude loomisel kasutatav arvelduskonto

Kaubanõude loomisel kasutatava arvelduskonto valimiseks toimige järgmiselt.

1. Minge jaotisesse **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Kõik projektid** ja valige projekti kirje.
1. Valige vahekaardil **Plaan** **Kaubanõuded**.
1. Looge uus kaubanõude kirje.

    - Vaikimisi on kirje väli **Arvelduskonto** seatud projektile määratud arvelduskontole. Saate muuta välja **Arvelduskonto** väärtust ja seejärel kirje salvestada. Pärast kirje salvestamist ei saa te enam väärtust **Arvelduskonto** värskendada. Kui peate värskendama kaubanõude väärtust **Arvelduskonto**, kustutage olemasolev kaubanõue ja looge seejärel soovitud väärtusega uus nõue.
    - Vaikimisi määratakse kaubanõude väli **Klient** määratud väärtuse **Vaikeklient** alusel **Projektihaldus- ja raamatupidamisparameetrid** lehel.

    Kui kaubanõude kirje on salvestatud, seostab süsteem selle päisekirjega **Kaubanõude müügitellimus**. Kui ühelgi avatud müügitellimuse päisel pole valitud arvelduskontot, loob süsteem selle ja seob sellega kaubanõude rea.

> [!NOTE]
> Kaubanõuded esitatakse alati täielikult arvelduskontole, mis on kirjes määratud. Süsteem ei toeta praegu rahastamise jaotamise reegleid, millel on kaubanõuded, ja see ei jaga postitust rahastamise jaotamise reeglite seadistuse alusel.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Kaubaprognoosi kirjest kaubanõude loomine

Kauba prognoosi kirjest kaubanõude loomiseks toimige järgmiselt.

1. Minge jaotisesse **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Kõik projektid** ja valige projekti kirje.
1. Valige vahekaardil **Plaan** **Kauba prognoosid**.
1. Looge uus kaubaprognoosi kirje.
1. Valikuline: valige vahekaardil **Projekt** väljal **Rahastamisallikas** soovitud arvelduskonto.
1. Valige **Kaubanõude loomine** ja kinnitage saadud teade.

    > [!NOTE]
    > Süsteem kopeerib **Rahastamisallika** väärtuse kaubaprognoosi kirjest vastloodud kaubanõude kirjesse.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Vaikearvelduskonto, kui süsteem loob automaatselt kaubanõude ostutellimuse realt

Kui suvand **Kaubanõude loomine** on seatud väärtusele **Jah** lehel **Projektihaldus ja raamatupidamisparameetrid**, loob süsteem uue projekti ostutellimuse rea salvestamisel automaatselt kaubanõude. Vaikimisi on väljad **Arvelduskonto** ja **Kaubanõue** seatud projektikirjes välja **Vaikearvelduskonto** väärtusele. Süsteem ei toeta praegu seda tüüpi kirjete arvelduskonto värskendamist ega muutmist.
