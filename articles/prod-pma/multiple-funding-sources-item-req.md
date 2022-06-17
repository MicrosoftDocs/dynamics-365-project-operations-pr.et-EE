---
title: Üksuse nõuded mitme rahastamise allikaga projektilepingutele
description: Selles artiklis antakse teavet selle kohta, kuidas konfigureerida ja kasutada kaubavajadusi mitme rahastamisallikaga.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a54ca1ec5e78d9d0af7b67914f6a63154c7347d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931187"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Üksuse nõuded mitme rahastamise allikaga projektilepingutele

_**Kehtib järgmiste puhul:** Project Operations ladustamise-/tootmispõhiste stsenaariumide jaoks_

Mõned lepingulised kokkulepped projektipõhiste tulemuste kohta võivad vajada mitut rahastamisallikat. Selles artiklis selgitatakse, kuidas valida ja konfigureerida soovitud rahastamisallikaid, kui projekti- või projektilepingu jaoks on vaja mitut allikat.

## <a name="terminology"></a>Mõisted

- **Rahastamisallikas** – projekti lepingulist tööd rahastav üksus. See olem võib olla sisemine organisatsioon või väline arvekonto (klient või toetus).
- **Projekti klient** – olem, kuhu projektitöö toimetatakse.
- **Arvekonto** – väline olem, mis maksab projektitöö eest.

## <a name="example"></a>Näide

Contoso on võitnud seadmete uuendamise lepingu kahe oma kliendiga: Adatum US ja Adatum Corporate. Leping sisaldab riistvara- ja paigaldusteenuseid, mis tarnitakse Adatum US-le (projekti klient). Riistvara rahastab Adatum Corporate (arvekonto 1) ja paigaldustöid rahastab Adatum US (arvekonto 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Saate häälestada kaubanõuete arvekonto vaikereegleid.

### <a name="prerequisites"></a>eeltingimused

- Microsoft Dynamics 365 Finance and Operations **versioon 10.0.27 või uuem** on vajalik kaubanõuete kasutamiseks, millel on mitu arvekontot.
- Teie süsteemiadministraator peab funktsioonihalduse **tööruumis lubama** funktsioonihalduse tööruumis project Operationsi ladustatud/tootmispõhiste stsenaariumide **jaoks** mitme rahastamisallikaga nõuded.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Arvekonto vaikereeglite häälestamine

Arvekonto vaikereeglite seadistamiseks tehke järgmist.

1. Avage jaotis **Projektijuhtimine ja raamatupidamine** \> **Seadistamine** \> **Projektijuhtimise ja raamatupidamise parameetrid**.
1. **Seadke** vahekaardi **Üldine** jaotises Müügitellimused ja Kaubanõuded **suvand Luba mitme rahastamisallikaga** projektidele väärtuseks **Jah**.
1. Määrake **väljal Vaikeklient**, kust on vaikimisi pärit projekti tarneklient kaubavajadusel.

    - **Rahastamisallikast** – projekti kohaletoimetamise vaikeklient pärineb rahastamisallikast. Kui projektilepinguga on seostatud mitu rahastamisallikat, kasutatakse loendi esimest rahastamisallikat.
    - **Projektist** – projekti kohaletoimetamise vaikeklient pärineb kliendilt, kes on valitud väljal **Projekti kirjekonto**.

1. Valikuline: saate määrata või muuta projektikirjete arve vaikekontot.

    1. **Avage projektihalduse ja raamatupidamise** \> **projektid Kõik** \> **projektid** ja avage projekti kirje üksikasjad.
    2. Määrake **või värskendage vahekaardil Üldine** välja Arve **vaikekonto**. Teie määratud kontot kasutatakse projekti jaoks loodud uute kaubanõuete vaikearvekontona. Kui jätate välja tühjaks, kasutatakse vaikimisi esimese projektilepingu rahastamisallika arvekontot. Kuid kasutajad saavad kirje salvestamisel kontot muuta.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Valige arvekonto, mida kaubanõude loomisel kasutada.

Kaubavajaduse loomisel kasutatava arvekonto valimiseks tehke järgmist.

1. **Avage projektihaldus- ja raamatupidamisprojektid** \> **·** \> **Kõik projektid** ja valige projektikirje.
1. Valige vahekaardil **Plaan** suvandi **Kaubanõuded**.
1. Looge uus kaubavajaduse kirje.

    - Vaikimisi **on kirje väli Arve konto** seatud projekti jaoks määratud arvekontole. Saate muuta välja Arvekonto **väärtust** ja seejärel kirje salvestada. Pärast kirje salvestamist ei saa te enam arvekonto **väärtust värskendada**. Kui peate kaubanõude väärtust Arve konto **väärtust värskendama**, kustutage olemasolev kaubanõue ja looge uus, millel on soovitud väärtus.
    - Vaikimisi **on kaubanõude väli Klient** seatud **lehel Projekti haldus- ja raamatupidamisparameetrite** määratud **vaikekliendi** väärtuse alusel.

    Kaubavajaduse kirje salvestamisel seostab süsteem selle kaubavajaduse müügitellimuse **päise kirjega**. Kui ühelgi avatud müügitellimuse päisel pole valitud arvekontot, loob süsteem selle ja seostab sellega kaubavajaduse rea.

> [!NOTE]
> Kaubanõuded arveldatakse alati täielikult kirjes määratud arvekontole. Süsteem ei toeta praegu rahastamise eraldamise reegleid, millel on kaubanõuded, ja see ei jaga konteerimist rahastamise eraldamise reeglite seadistuse alusel.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Kaubavajaduse loomine kaubaprognoosi kirjest

Kaubavajaduse loomiseks kaubaprognoosi kirjest tehke järgmist.

1. **Avage projektihaldus- ja raamatupidamisprojektid** \> **·** \> **Kõik projektid** ja valige projektikirje.
1. Valige vahekaardil **Plaan** suvand **Kaubaprognoosid**.
1. Looge uus kaubaprognoosi kirje.
1. Valikuline: **valige vahekaardi Projekt** väljal **Rahastamise allikas** soovitud arvekonto.
1. Valige **Loo kauba nõue** ja kinnitage saadud sõnum.

    > [!NOTE]
    > Süsteem kopeerib **rahastamisallika** väärtuse kaubaprognoosi kirjest vastloodud kaubavajaduse kirjesse.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Arve vaikekonto, kui süsteem loob ostutellimuse realt automaatselt kaubavajaduse

**Kui suvand Loo kaubavajadus** on lehel Projektihaldus- ja raamatupidamisparameetrid **seatud väärtusele** **Jah**, loob süsteem uue projekti ostutellimuse rea salvestamisel automaatselt kaubavajaduse. Vaikimisi **seatakse väljad Arvekonto** ja **Kauba nõue** projektikirje välja Vaikearvekonto **väärtuseks**. Süsteem ei toeta praegu seda tüüpi kirjete arvekonto värskendamist või muutmist.
