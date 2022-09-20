---
title: Projekti hankija arvete kinnitamine
description: Selles artiklis selgitatakse, kuidas kinnitada projekti hankija arvet Microsoftis Dynamics 365 Project Operations, ja kirjeldatakse projekti hankija arve kinnitamise finantsmõju.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475463"
---
# <a name="confirm-project-vendor-invoices"></a>Projekti hankija arvete kinnitamine

_ **Rakendub:** Project Operations ressursipõhiste/mitteladustatavate stsenaariumite jaoks

**Kui parameeter PM-i käsitsi kinnitamine on lubatud**, on hankija arvetel Microsoft Dataverse, mis on loodud olekus **Mustand**. Sel viisil loodud hankija arved tuleb üle vaadata ja käsitsi kinnitada. **Kui parameeter PM-i käsitsi kinnitamine on nõutav**, kinnitatakse sisse Dataverse loodud hankija arved automaatselt. Täiendavaid meetmeid ei ole vaja võtta. 

Kui olete hankija arve kõik read kinnitanud, valige hankija arve Dynamics 365 Project Operations kinnitamiseks Kinnita **.**

Kui valite **hankija arvel käsu Kinnita**, toimub järgmine käitumine.

1. Hankija arve olekuks värskendatakse **kinnitatud**.
1. Kinnitatud hankija arve ja sellega seotud kirjed muutuvad kirjutuskaitstuks ning neid ei saa redigeerida ega kustutada.
1. Kui mõni tegelik kulu viitab hankija arve reale vastavusse viimise protsessi osana, tühistatakse kõik kulu tegelikud kulud, mis on seotud viidatud hankija arve reaga.
1. Uued tegelikud kuluandmed luuakse hankija arve real oleva teabe abil.
1. Te ei saa enam luua parandustöölehti, töödelda ajakirjete tagasikutsumisi ega tühistada algse aja, kulu või tühistatud tegelike andmete kinnitamist.
1. Dynamics 365 Finance **värskendatakse projekti kuluväärtust**, kasutades töölehte Projekti integratsioon, ja hangete integreerimise konto *tühistatakse* pärast töölehe Projekti integreerimine sisestamist.

> [!NOTE]
> Kui hankija arve mis tahes real on muu kinnitamise olek kui **Lõpetatud**, ei saa hankija arvet kinnitada.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
