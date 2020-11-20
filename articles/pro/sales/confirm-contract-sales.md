---
title: Projekti lepingu kinnitamine
description: Selles teemas antakse teavet, kuidas Project Operationsis lepingut kinnitada.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128278"
---
# <a name="confirm-a-project-contract"></a>Projekti lepingu kinnitamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Projekti lepingu võib rakenduses Dynamics 365 Project Operations olla aktiivne, mille põhjuseks on **Kinnitatud** või suletud, mille põhjus on **Kaotatud**. Kui kinnitate projekti lepingu, siis muutub olek olekust **Mustand** olekuks **Aktiivne** ja oleku põhjus on **Kinnitatud**. Aktiivset või suletud lepingut ei saa redigeerida ega uuesti avada. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Projekti lepingu kinnitamise finantsmõju

Pärast projekti lepingu kinnitamist arvutab rakendus kulud ümber, pöörates tagasi vanemad tegelikud kulud ja luues uued tegelikud kulud. Uusi tegelikke kulusid töödeldakse, võttes aluseks seotud projekti lepingurea arveldusmeetodi. Kui tegelikud kulud viitavad aja ja materjali lepingureale, loob rakendus automaatselt vastavad arveldamata tegelikud müüginäitajad uuesti. Kui tegelikud kulud viitavad fikseeritud hinna lepingureale, peatab rakendus tegelike kulude ümbertöötlemise.

Mitteületatavad limiite, arveldatavuse seadistamist ning tegelikke hindu ja kulusid hinnatakse ning seejärel värskendatakse kinnituste osana.

## <a name="close-a-project-contract-as-lost"></a>Projekti lepingu sulgemine kaotatuna

Kui sulgete projekti lepingu kaotatuna, muudetakse lepingu olekuks **Suletud** ja oleku põhjuseks on **Kaotatud**. Projekti leping muutub kirjutuskaitstuks. Enne muudatuste lõpuleviimist kuvatakse kinnituse dialoog, kuna suletud projekti lepingut ei saa uuesti avada.

Kui projekti leping, mis on suletud kui kaotatud, viitab projekti ridadele, siis on ka see projekt suletuks märgitud. Kõik ressursi broneeringud alates sellest päevast edasi on tühistatud. Kõik projekti lepingusse kuuluvad arveldamata tegelikud müüginäitajad, mida veel arvele pole lisatud, tühistatakse.

> [!NOTE]
> Rakenduses Dynamics 365 Project Operations ei mõjuta projekti lepingu sulgemine seostatud müügivõimaluse olekut. Müügivõimalus jääb avatuks ja see tuleb käsitsi sulgeda.
