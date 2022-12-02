---
title: Projekti hinnapakkumise aktiveerimine ja kontrollimine
description: See artikkel annab teavet hinnapakkumiste aktiveerimise ja läbivaatamise kohta teenuses Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410366"
---
# <a name="activate-and-revise-a-project-quote"></a>Projekti hinnapakkumise aktiveerimine ja kontrollimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Aktiveerimis- ja läbivaatamisvõimalused aitavad teil hinnata projektipõhiste hinnapakkumiste versioonide loomist hindamis- ja läbirääkimisfaasis. Kui hinnapakkumise mustand on aktiveeritud, muutub see kirjutuskaitstuks.

Aktiveerimis- ja läbivaatamisvõimalused võimaldavad teil täita järgmisi toiminguid.

- Hinnapakkumiste võitmine või kaotamine alles pärast aktiveerimist.
- Hinnapakkumise läbivaatamine, et teha muudatusi olemasolevasse pakkumisse või luua uus versioon.

> [!NOTE]
> Pärast hinnapakkumiste aktiveerimis- ja läbivaatamisfunktsiooni lubamist ei saa seda keelata.

Projektipõhiste hinnapakkumiste aktiveerimise ja läbivaatamise võimaluse sisselülitamiseks toimige järgmiselt.

1. Minge jaotisse **Sätted** \> **Parameetrid**.
1. Avage kirje **Parameetrid**.
1. Valige toimingupaani vahekaardil **Funktsiooni juhtimine** suvand **Luba hinnapakkumiste aktiveerimine ja muutmine**.
1. Valige kinnitusdialoogis **OK**.
1. Mõne hetke pärast värskendage oma brauserit. Aktiveerimis- ja läbivaatamisvõimalused peaksid nüüd saadaval olema. Teate, et need võimalused on lubatud, kui nuppu **Luba hinnapakkumiste aktiveerimine ja muutmine** enam toimingupaanil ei kuvata.

## <a name="activating-a-quote"></a>Hinnapakkumise aktiveerimine

Kui hinnapakkumiste aktiveerimis- ja läbivaatamisfunktsioon on lubatud, ei ole tegevuspaanil olevad nupud **Sule pakkumine võidetuna** ja **Sule pakkumine kaotatuna** projekti hinnapakkumiste mustandite jaoks saadaval. Need on saadaval ainult pärast hinnapakkumise aktiveerimist.

Aktiveerimine tähistab hinnapakkumise protsessi etappi, mil soovite hinnapakkumises rohkem muudatusi vältida. Selles etapis saadetakse hinnapakkumine ettevõttesiseseks ülevaatuseks või kliendile.

Aktiveeritud hinnapakkumiste jaoks on saadaval toimingupaanil olevad nupud **Sule pakkumine võidetuna** ja **Sule pakkumine kaotatuna**. Sõltuvalt ettevõtte või kliendi ülevaatuse tulemustest saate aktiveeritud hinnapakkumise sulgemiseks kasutada ühte nendest nuppudest. Aktiveeritud hinnapakkumiste osas saate läbirääkimisi pidada ja muudatusi teha, valides **Vaata hinnapakkumine läbi**.

## <a name="revising-a-quote"></a>Hinnapakkumise läbivaatamine

Kui peate aktiveeritud hinnapakkumises muudatusi tegema, valige **Vaata hinnapakkumine läbi**. Hinnapakkumine on suletud ja kasutatakse põhjuskoodi **läbi vaadatud**. Seejärel luuakse uus hinnapakkumine, millel on sama ID ja suurendatud läbivaatamise number. Kõik algse hinnapakkumise üksikasjad kopeeritakse uude hinnapakkumisse. Uus hinnapakkumine on mustandi olekus ja seda saab vastavalt vajadusele muuta.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
