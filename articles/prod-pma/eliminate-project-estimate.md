---
title: Projekti prognoosi eemaldamine
description: Selles teemas antakse teavet projekti prognoosi eemaldamise kohta pärast selle valmimist.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 267b5ffab7ef3a6776c31100deea81fb523752b6
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684085"
---
# <a name="eliminate-a-project-estimate"></a>Projekti prognoosi eemaldamine

[!include [banner](../includes/banner.md)]

Projekti prognoosid annavad finantsülevaate töö kohta, mis on projekti jaoks prognoositud ja plaanitud. Projekti prognoosidega töötamiseks peate projekti prognoositud projektiga siduma. Prognoositav projekt põhineb alati olemasoleval projektil, kuid mitme projekti puhul võib viidata ühele prognoositavale projektile. Prognoositavatele projektidele saab lisada ainult fikseeritud hinnaga ja investeerimisprojekte ning need projektid peavad kuuluma samasse projekti rühma, kuhu kuulub prognoositav projekt.

Prognoositava projekti eemaldamiseks tuleb see valmis saada. Järgmised juhised selgitavad, kuidas prognoosi eemaldada.

1. Minge jaotisse **Projekti haldamine ja raamatupidamine** > **Kõik projektid** ja avage projekt. 
2. Valige vahekaardil **Halda** väärtus **Prognoosid** ja lehel **Hinnang** suvand **Eemalda**.
3. Seadke vahekaardil **Üldine** lehel **Prognoosi eemaldamine** järgmised suvandid.

   - **Perioodi kood**: valige sobiva prognoositava projektide valimiseks perioodi kood. 
   - **Prognoosi kuupäev**: valige eemaldamiseks sobiv prognoosi kuupäev.
   - **Eemalda WIP-i hoiatustega**: lubage see suvand teatamiseks, kui poolelioleva tööga seotud prognoos eemaldatakse. Kui see suvand pole lubatud, ei saa eemaldamist jätkata, kui olemas on mitte-prognoositavad tehingud. 
   > [!NOTE]
   > See suvand on saadaval ainult siis, kui prognoositavale projektile on rakendatud eemaldamine. See pole saadaval, kui kasutate perioodilist sisestust. See säte töötab lehe **Projekti parameetrid** vahekaardi **Prognoos** sätetega, mis asub välja rühmas **Luba eemaldamine, kui olemas on mitte-prognoositavad tehingud**.
   - **Sea etapi väärtuseks Lõpetatud**: lubage see suvand, et seada prognoositava projekti etapi väärtuseks **Lõpetatud**, kui olete eemaldamise lõpetanud.
   - **Prindi prognooside loend**: valige teave, mis kaasatakse prognooside loendi printimisel.
   - **Kuva teabelogi**: lubage see suvand teabelogi kuvamiseks.
   - **Sisestamise kuupäev**: valige prognoosi pearaamatusse sisestamise kuupäev.

4.  Valige **OK**.
5. Kui eemaldamise protsess on valmis, kuvatakse eemaldatud prognoositav projekt negatiivse väärtusega. 

Kui te ei soovinud prognoosi eemaldada, saate valida eemaldatud prognoosi ja valida suvandi **Tühista eemaldamine**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]