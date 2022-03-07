---
title: Projekti lepingu kinnitamine
description: Selles teemas antakse teavet, kuidas Project Operationsis lepingut kinnitada.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0ca43eb6005948f440fca16e98a6d05db3493c82e518441bb50f9413da91ead
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989816"
---
# <a name="confirm-a-project-contract"></a>Projekti lepingu kinnitamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Projektileping rakenduses Dynamics 365 Project Operations võib olla aktiivne põhjusega **Kinnitatud** või suletud põhjusega **Kaotatud**. Kui kinnitate projekti lepingu, siis muutub olek olekust **Mustand** olekuks **Aktiivne** ja oleku põhjus on **Kinnitatud**. Aktiivset või suletud lepingut ei saa redigeerida ega uuesti avada. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Projekti lepingu kinnitamise finantsmõju

Pärast projekti lepingu kinnitamist arvutab rakendus kulud ümber, pöörates tagasi vanemad tegelikud kulud ja luues uued tegelikud kulud. Uusi tegelikke kulusid töödeldakse, võttes aluseks seotud projekti lepingurea arveldusmeetodi. Kui tegelikud kulud viitavad aja ja materjali lepingureale, loob rakendus automaatselt vastavad arveldamata tegelikud müüginäitajad uuesti. Kui tegelikud kulud viitavad fikseeritud hinna lepingureale, peatab rakendus tegelike kulude ümbertöötlemise.

Mitteületatavad limiite, arveldatavuse seadistamist ning tegelikke hindu ja kulusid hinnatakse ning seejärel värskendatakse kinnituste osana.

## <a name="close-a-project-contract-as-lost"></a>Projekti lepingu sulgemine kaotatuna

Kui sulgete projekti lepingu kaotatuna, muudetakse lepingu olekuks **Suletud** ja oleku põhjuseks on **Kaotatud**. Projekti leping muutub kirjutuskaitstuks. Enne muudatuste lõpuleviimist kuvatakse kinnituse dialoog, kuna suletud projekti lepingut ei saa uuesti avada.

Kui projekti leping, mis on suletud kui kaotatud, viitab projekti ridadele, siis on ka see projekt suletuks märgitud. Kõik ressursi broneeringud alates sellest päevast edasi on tühistatud. Kõik projekti lepingusse kuuluvad arveldamata tegelikud müüginäitajad, mida veel arvele pole lisatud, tühistatakse.

> [!NOTE]
> Projekti lepingu sulgemine rakenduses Dynamics 365 Project Operations kaotatuna ei mõjuta seostatud müügivõimaluse olekut. Müügivõimalus jääb avatuks ja see tuleb käsitsi sulgeda.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]