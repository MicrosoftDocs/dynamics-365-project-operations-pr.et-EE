---
title: Hankijalt kinnipidamise häälestus
description: Selles teemas selgitatakse, kuidas seadistada hankija maksete kinnipidamist.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e0cd7669c7d6b916261e2c85cce0f24ff241a075
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583699"
---
# <a name="set-up-vendor-retention"></a>Hankijalt kinnipidamise häälestus

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles teemas antakse teavet, kuidas seadistada hankija maksete kinnipidamist.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Hankijalt kinnipidamise konto häälestus pearaamatus

1. Avage Dynamics 365 **Finance** > **automaatkannete pearaamatu sisestamise häälestuskontod** > **·**.
2. Lisage uus rida.
3. Tehke väljal **Kirjendamise tüüp** valik **Hankijalt kinnipidamine**.
4. Valige hankijalt kinnipidamise sisestamise põhikonto.

## <a name="create-vendor-retention-terms"></a>Hankija makse kinnipidamise tingimuste loomine

Kasutage lehte **Hankijalt kinnipidamise tingimused**, et seadistada ja hallata hankija maksete kinnipidamise tingimusi. Sisestage kinnipeetava hankija makse protsendimäär ja vabastatavate, eelnevalt kinnipeetud summade protsendimäär. Summad peetakse automaatselt hankija arvetel kinni, kuni leping jõuab määratud olekuni. Kui hankija jaoks on määratud kinnipidamise tingimused, saate need rakendada mis tahes projektile, mille kallal hankija töötab.

1. Avage rakenduses Finance suvand **Projektihaldus ja raamatupidamine** > **Seadistus** > **Kinnipidamine** > **Hankija maksete kinnipidamise tingimused**.
2. Valige **Uus**, et lisada uus hankija kinnipidamise tingimus. Uue tingimuse välja **Reegli ID** väärtus sisestatakse automaatselt. 
3. Sisestage väljal **Kirjeldus** uue tingimuse kirjeldav nimi.
4. Vahekaardil **Tingimused** valige suvand **Lisa rida**, et sisestada hankija makse kinnipidamise aeg.
5. Väljale **Tarnitud ühikute protsendimäär** sisestage reegli täitmise protsent. Summad peetakse automaatselt hankija arvetest kinni, kuni projekti lõpuleviimine on jõudnud etappi, mis on võrdne teie sisestatud protsendimääraga. Näiteks kui sisestate 50,00, peetakse summad kinni, kuni projekt on 50 protsendi ulatuses valmis.
6. Väljale **Kinnipeetav protsendimäär** sisestage hankija arvest kinnipeetava summa protsendimäär. Näiteks kui sisestate sellele väljale 10,00, siis peetakse hankija arvetelt kinni 10 protsenti summast, kuni projekt jõuab täitmisprotsendini, mille valisite väljal **Tarnitud ühikute protsendimäär**.
7. Väljale **Vabastatav protsendimäär** sisestage mis tahes eelnevalt kinnipeetud summade protsendimäär, mida soovite vabastada valitud projekti täitmise tasemel.

> [!NOTE]
> Kui teil on projekti erinevate tasemete täitmisel mitu vahe-eesmärki, sisestage iga kinnipidamise reegli jaoks eraldi hankija makse kinnipidamise tingimus. Igale reale saate määrata erineva kinnipeetava protsendimäära ja iga projekti taseme täitmisel vabastatava protsendimäära.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Projekti jaoks hankija kokkuleppe seadistamine

Seadistage hankija makse kinnipidamise tingimused, mis projektile kehtivad. Hankija kinnipidamise tingimused kuvatakse ka ostutellimustel, mille olete hankija jaoks loonud.

1. Rakenduses Finance avage **Projektihaldus ja raamatupidamine** > **Projektid** > **Kõik projektid**. 
2. Valige projekt ja seejärel valige toimingupaanil suvand **Projekti rühm** > **Hankija lepingud**.
3. Lisage lehele **Hankija lepingud** uus rida.
4. Valige väljal **Konto kood** üks järgmistest suvanditest.
   - **Tabel**: hankija kinnipidamise tingimused rakenduvad ühele hankijale.
   - **Rühm**: hankija kinnipidamise tingimused rakenduvad kõigile hankijarühma hankijatele.
   - **Kõik**: hankija kinnipidamise tingimused rakenduvad kõikidele hankijatele.
5. Valige väljal **Hankija/hankijarühm** hankija või hankijarühm, mille jaoks hankija kinnipidamise tingimusi rakendatakse. Kui valisite eelmises etapis suvandi **Kõik**, pole see väli saadaval.
6. Valige väljal **Hankija kinnipidamise tingimused** sellele tarnijale rakendatava kinnipidamise tingimuste reegli ID.

