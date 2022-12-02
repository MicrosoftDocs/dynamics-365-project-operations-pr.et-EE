---
title: Tegelikud näitajad
description: See artikkel annab teavet tegelike näitajate töötamise kohta rakenduses Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924793"
---
# <a name="actuals"></a>Tegelikud näitajad

_**Rakendub:** Project Operationsi ressursipõhiste/mittelaopõhiste stsenaariumide korral, lihtjuurutamine – tehing näidisarveldusele_

Tegelikud andmed esindavad projekti läbivaadatud ja kinnitatud finantsilist ning ajakava edenemist. Need luuakse siis, kui aja-, kulu- ja materjalikasutuse kanded, päevikukanded ja arved on kinnitatud.

> [!IMPORTANT]
> Tegelikke näitajaid ei tohiks süsteemis redigeerida ega süsteemist kustutada. Vastasel juhul võib see kahjustada finantsilist terviklikkust ja integratsiooni teiste finants- ja raamatupidamissüsteemidega. Microsoft Dynamics 365 Project Operations võimaldab teil kasutada tegelike näitajate ümberpööramist ja asendamist, et muuta tegelikke näitajaid oma projektide äriprotsessi elutsükli eri punktides.

## <a name="recording-actuals-based-on-project-events"></a>Projektisündmustel põhinevate tegelike andmete kirjendamine

Project Operations kirjendab projektiga seotud elutsükli jooksul toimuvad finantstehingud tegelike näitajateks. Tegelike näitajate koostamine elutsükli eri etappidel on erinev, sõltuvalt sellest, kas projekti puhul kasutatakse aja ja materjalide arvete esitamise mudelit või fikseeritud hinnaga arvete esitamise mudelit ning kas tegemist on müügieelse või sisemise projektiga.

Järgmistes artiklites selgitatakse mõju tegelike näitajate tabelile erinevatel sündmustel erinevate variatsioonide puhul:

- [Tegelike näitajate mõju aja ja materjalide kaasamisel](ActualsonTM.md)
- [Tegelike näitajate mõju fikseeritud hinna kaasamises](ActualonFP.md)
- [Tegelike näitajate mõju kaasamise müügieelse etapi ajal](ActualonPreSales.md)
- [Tegelike näitajate mõju sisemise projekti jaoks](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
