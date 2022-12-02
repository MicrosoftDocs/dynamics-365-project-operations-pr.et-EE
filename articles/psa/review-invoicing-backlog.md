---
title: Arvelduse mahajäämuse ülevaatamine projektide ja projektilepingute jaoks
description: See artikkel annab teavet aja, kulude ja toote võlgnevuste ülevaatamise ning selle kohta, kuidas neid arveldusvalmiks märkida.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 833ace7fd6285191f4b023a029286cd36b5de8f4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928887"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Arvelduse mahajäämuse ülevaatamine projektide ja projektilepingute jaoks

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kui kanne on arve koostamiseks ja töötlemiseks valmis, tuleb kanne märkida väärtusele **Arveldamiseks valmis**. See artikkel kirjeldab, millist tüüpi tehinguid saab luua.

## <a name="review-the-time-and-material-billing-backlog"></a>Ajakavast mahajäämuse ja materjali arvete võlgnevuste ülevaatamine

Kui projekti jaoks esitatakse ja kinnitatakse aja- või kulukirje, loob PSA projekti tegeliku näitaja. Kui projekti ja kande klassi kombinatsioon vastendatakse aja- ja materjalikulu projekti puhul lepingureaga, luuakse kirje kinnitamisel kaks tegelikku näitajat.

- Tegelik kulu 
- Arveldamata tegelik müük

Arveldamata tegelikud müügid näitavad arvete võlgnevust ja nende arveldamise olek tuleb määrata väärtusele **Arveldamiseks valmis**. Projekti arve loomisel kopeeritakse arveldamata tegelikud müügid, mis on märgitud kui **Arveldamiseks valmis**, arverea üksikasjadena.

Aja ja materjalide arvete võlgnevuse ülevaatamiseks tehke valikud **Müügid** \> **Arveldus** \> **Ajakavast mahajäämus ja materjali arvete võlgnevused**. Valige kõik arveldamata tegelikud müügid, mis on arveldamiseks valmis ja seejärel valige **Arveldamiseks valmis**. Nende tegelike näitajate arveldamise olek muudetakse väärtusele **Arveldamiseks valmis**.

![Ajakavast mahajäämus ja materjali arvete võlgnevused.](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Toodete arvete võlgnevuste ülevaatamine

Kui projektileping sisaldab tootepõhiseid lepinguridu, kaalutakse PSA-s neid ridu arveldamiseks iga kord, kui projektilepingule luuakse arve. Kõik tooted, millel on lepinguread väärtusega **Arveldamiseks valmis**, kopeeritakse projekti arveridadena projekti arvesse.

Toodete arvete võlgnevuse ülevaatamiseks tehke valikud **Müügid** \> **Arveldus** \> **Toodete arvete võlgnevused**. Valige kõik tootepõhised lepinguread, mis on arveldamiseks valmis ja seejärel tehke valik **Arveldamiseks valmis**. Nende ridade arveldamise olek muudetakse väärtusele **Arveldamiseks valmis**.

![Toodete arvete võlgnevused.](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Arveldamise vahe-eesmärkide ülevaatamine fikseeritud hinnaga lepingutes

Iga projekti lepingurida, millel on fikseeritud hinnaga arveldusmeetod, peab määratlema lepingu vahe-eesmärgid. Neid lepingu vahe-eesmärke saab arveldada ainult juhul, kui need on väärtusel **Arveldamiseks valmis**. 

Arveldamise vahe-eesmärkide ülevaatamiseks tehke valikud **Müügid** \> **Arveldus** \> **Fikseeritud hinna vahe-eesmärgid**. Valige vahe-eesmärgid, mis on arveldamiseks valmis ja seejärel tehke valik **Arveldamiseks valmis**. Nende vahe-eesmärkide arveldamise olek muudetakse väärtusele **Arveldamiseks valmis**.

![Fikseeritud hinna vahe-eesmärgid.](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
