---
title: Üksuse nõuded mitme rahastamise allikaga projektilepingutele
description: Selles artiklis antakse teavet selle kohta, kuidas konfigureerida ja kasutada kauba nõudeid mitme rahastamisallikaga.
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

Mõned projektipõhiste tulemuste lepingulised kokkulepped võivad nõuda mitut rahastamisallikat. Selles artiklis selgitatakse, kuidas valida ja konfigureerida soovitud rahastamisallikaid, kui projekti või projekti lepingu jaoks on vaja mitut allikat.

## <a name="terminology"></a>Mõisted

- **Rahastamisallikas** – projekti rahastav üksus, kes teeb lepingulist tööd. See üksus võib olla sisemine organisatsioon või väline arvekonto (klient või grant).
- **Projekti klient** – olem, kuhu projektitöö toimetatakse.
- **Arvekonto** – väline üksus, mis maksab projektitöö eest.

## <a name="example"></a>Näide

Contoso on võitnud seadmete uuendamise lepingu kahe oma kliendiga: Adatum US ja Adatum Corporate. Leping sisaldab riistvara- ja paigaldusteenuseid, mis tarnitakse Adatum US-le (projekti klient). Riistvara finantseerib Adatum Corporate (arvekonto 1) ja paigaldustöid Adatum US (arvekonto 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Arvekonto vaikereeglite seadistamine kaubanõuete jaoks

### <a name="prerequisites"></a>eeltingimused

- Microsoft Dynamics 365 Finance'i **versioon 10.0.27 või uuem** versioon on nõutav kaubanõuete kasutamiseks, millel on mitu arvekontot.
- Teie süsteemiadministraator peab tööruumis **Funktsioonihaldus** lubama **funktsiooni Luba kaubanõuded mitme rahastamisallikaga Project Operationsi varutud/tootmispõhiste stsenaariumide** jaoks.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Arvekonto vaikereeglite seadistamine

Arvekonto vaikereeglite seadistamiseks toimige järgmiselt.

1. Avage jaotis **Projektijuhtimine ja raamatupidamine** \> **Seadistamine** \> **Projektijuhtimise ja raamatupidamise parameetrid**.
1. **Määrake vahekaardi** Üldine **jaotises** Müügitellimused ja Kaubanõuded **suvandi Luba mitme rahastamisallikaga** projektide puhul väärtuseks **Jah**.
1. Määrake väljal **Vaikeklient**, kust kaubavajaduse projekti tarneklient vaikimisi pärineb.

    - **Rahastamisallikast** – projekti kohaletoimetamise vaikeklient pärineb rahastamisallikast. Kui projektilepinguga on seotud mitu rahastamisallikat, kasutatakse loendis esimest rahastamisallikat.
    - **Projektist** – projekti kohaletoimetamise vaikeklient pärineb kliendilt, kes on valitud väljal **Projekti kirje konto**.

1. Valikuline: määrake või muutke projekti kirjetes vaikearvekontot.

    1. Avage **Jaotis Projektihaldus ja raamatupidamine** \> **Projektid** \> **Kõik projektid** ja avage projektikirje üksikasjad.
    2. **Vahekaardil Üldine** määrake või värskendage **välja Vaikearve konto**. Teie määratud kontot kasutatakse projekti jaoks loodud uute kaubanõuete vaikearvekontona. Kui jätate välja tühjaks, kasutatakse vaikimisi esimese projektilepingu rahastamise allika arvekontot. Kuid kasutajad saavad kirje salvestamisel kontot muuta.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Kaubavajaduse loomisel kasutatava arvekonto valimine

Kaubavajaduse loomisel kasutatava arvekonto valimiseks toimige järgmiselt.

1. Avage **Jaotis Projektihaldus ja raamatupidamine** \> **Projektid** \> **Kõik projektid** ja valige projekti kirje.
1. **Valige vahekaardil Plaan** suvand **Kaubanõuded**.
1. Looge uus kaubavajaduse kirje.

    - Vaikimisi **on kirje välja Arvekonto** väärtuseks määratud projektile määratud arvekonto. Saate muuta välja Arvekonto **väärtust** ja seejärel kirje salvestada. Pärast kirje salvestamist ei saa te enam arvekonto **väärtust värskendada**. Kui peate kaubanõude arvekonto **väärtust värskendama**, kustutage olemasolev kaubanõue ja looge seejärel uus, millel on soovitud väärtus.
    - Vaikimisi **määratakse kaubavajaduse väli Klient** kliendi vaikeväärtuse **põhjal**, mis on määratud lehel **Projektihalduse ja raamatupidamise parameetrid**.

    Kui kaubavajaduse kirje on salvestatud, seostab süsteem selle kaubavajaduse müügitellimuse **päise kirjega**. Kui ühelgi avatud müügitellimuse päisel pole valitud arvekontot, loob süsteem selle ja seostab sellega kaubavajaduse rea.

> [!NOTE]
> Kaubavajadused arveldatakse alati täielikult kirjes määratud arvekontole. Süsteem ei toeta praegu kaubanõuetega rahastamise eraldamisreegleid ega tükelda sisestamist rahastamise eraldamisreeglite seadistuse alusel.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Kaubavajaduse loomine kaubaprognoosi kirjest

Kaubavajaduse loomiseks kaubaprognoosi kirjest toimige järgmiselt.

1. Avage **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Kõik projektid** ja valige projekti kirje.
1. **Valige vahekaardil** Plaan **suvand Üksuse prognoosid**.
1. Looge uus üksuse prognoosikirje.
1. Valikuline: **valige vahekaardil Projekt** väljal **Rahastamise allikas** soovitud arvekonto.
1. Valige **Üksuse nõude** loomine ja kinnitage saadud sõnum.

    > [!NOTE]
    > Süsteem kopeerib **rahastamise lähteväärtuse** kauba prognoosi kirjest vastloodud kaubavajaduse kirjesse.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Vaikearvekonto, kui süsteem loob kaubavajaduse automaatselt ostutellimuse realt

**Kui suvand Loo kaubavajadus** on lehel Projektihalduse ja raamatupidamise parameetrid **seatud väärtusele** Jah **·**, loob süsteem uue projekti ostutellimuse rea salvestamisel automaatselt kaubavajaduse. Vaikimisi **on väljade Arvekonto** ja **Kaubavajadus** väärtuseks seatud projektikirje välja Vaikearvekonto **väärtus**. Süsteem ei toeta praegu seda tüüpi kirjete arvekonto värskendamist ega muutmist.
