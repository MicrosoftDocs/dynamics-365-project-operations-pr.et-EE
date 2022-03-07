---
title: Hankija maksete kinnipidamise tingimuste loomine ja rakendamine
description: Selles teemas antakse teavet, kuidas seadistada ja hallata hankija maksete kinnipidamise tingimusi.
author: Yowelle
ms.date: 05/26/2020
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
ms.openlocfilehash: 4ff725512aa0bcc87ff4670d6bb072f3bf780786c1f71b332914887f4d4ccf13
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991211"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Hankija maksete kinnipidamise tingimuste loomine ja rakendamine

[!include [banner](../includes/banner.md)] 

Projekti jaoks hankija maksete kinnipidamise tingimuste seadistamine on kasulik juhul, kui teie organisatsioon soovib säilitada osa hankijale tehtud maksetest. Näiteks juhul, kui soovite hankija maksed ootele panna, kuni tarnitud tooted teie ootustele vastavad. Hankija maksete kinnipidamise tingimusi saab määrata hankijaga lepingu läbirääkimisi pidades.

## <a name="create-vendor-payment-retention-terms"></a>Hankija maksete kinnipidamise tingimuste loomine

Saate sisestada hankija maksete kinnipidamise protsendi ja varasemalt kinnipeetud summade, mis vabastatakse, protsendi. Summad peetakse automaatselt hankija arvetel kinni, kuni leping jõuab määratud olekuni. Pärast kinnipidamise tingimuste seadistamist saate need rakendada selle hankija mis tahes projektile.

Kasutage järgmisi juhiseid hankija maksete kinnipidamise tingimuste seadistamiseks ja haldamiseks. 

1. Minge jaotisse **Projektihaldus ja raamatupidamine** > **Kinnipidamine** > **Hankija maksete kinnipidamise tingimused**.
2. Valige **Uus**, et lisada uus hankija kinnipidamise tingimus. Uue tingimuse väärtus **Reegli ID** sisestatakse automaatselt. 
3. Sisestage lühikirjeldus väljale **Kirjeldus** ja valige seejärel FastTabilt **Tingimused** ja seejärel **Lisa rida**, et sisestada järgmisele tingimuse väärtused.

   - **Tarnitud ühikute protsent**: sisestage tingimuse täitmise protsent. Summad peetakse automaatselt hankija arvetel kinni, kuni projekti valmisoleku etapp võrdub määratud protsendiga. Näiteks kui sisestate 50,00, peetakse summad kinni, kuni projekt on 50 protsendi ulatuses valmis.
   - **Kinnipeetav protsent** : sisestage hankija arvelt kinnipeetava summa protsent. Näiteks juhul, kui sisestate 10,00, peetakse 10 protsenti hankija arve summast kinni seni, kuni projekt saavutab protsendi, mis on seatud väljal **Välja tarnitud ühikute protsent**.
   - **Vabastatav protsent**: valige suvand **Lisa rida**, et sisestada protsent varem kinnipeetud summadest, mis tuleb vabastada valitud projekti taseme saavutamisel.

> [!NOTE]
> Kui teil on projekti täitmise erinevatel tasemetel rohkem kui üks vahe-eesmärk, sisestage iga kinnipidamise tingimuse jaoks eraldi tarnija kinnipidamise tähtaeg. Iga rida saab määrata erineva kinnipidamise protsendi ja iga määratud taseme projekti lõpuleviimiseks erineva vabastamise protsendi.

Pärast hankijale hankija kinnipidamise tingimuste loomist saate need tingimused projektile rakendada.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Hankija kinnipidamise tingimuste rakendamine projektile

1. Minge jaotisesse **Projektihaldus ja raamatupidamine** > **Projektid** > **Kõik projektid** ja avage projektiloendi lehelt projekt.
2. Valige kiirvahekaardil **Hankija lepingud** käsk **Lisa rida**.
3. Valige **Konto koodi väljal** üks järgmistest suvanditest. 

   - **Tabel**: hankija kinnipidamise tingimused rakenduvad ühele hankijale.
   - **Rühm**: hankija kinnipidamise tingimused rakenduvad kõigile hankijarühma hankijatele.
   - **Kõik**: hankija kinnipidamise tingimused rakenduvad kõikidele hankijatele.

4. Valige **Hankija/hankijarühma väljalt** hankija või hankijarühm, mille jaoks hankija kinnipidamise tingimusi rakendatakse. Kui valisite eelmises etapis suvandi **Kõik**, pole see väli saadaval.
5. Valige väljal **Hankija kinnipidamise tingimused** eelmises protseduuris loodud kinnipidamise tingimused.
6. Kui projektil on ka hankija jaoks seadistatud tasulised (PWP) tingimused, sisestage projekti läviprotsent väljale **PWP läviprotsent**.

Hankija kinnipidamise tingimused kuvatakse ka ostutellimustel, mille olete hankija jaoks loonud.


[!INCLUDE[footer-include](../includes/footer-banner.md)]