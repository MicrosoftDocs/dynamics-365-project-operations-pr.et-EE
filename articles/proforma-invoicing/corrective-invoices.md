---
title: Parandatud arved
description: Selles teemas antakse teavet parandatud arvete kohta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122383"
---
# <a name="corrected-invoices"></a>Parandatud arved

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Kinnitatud arveid saab muuta. Kinnitatud arve muutmisel luuakse parandatud arve mustand. Kuna eeldame, et soovite kõik kanded ja kogused algsest arvest ümber pöörata, kaasatakse selle parandatud arve kõik algse arve tehingud ja kõik selle kogused on null (0).

Kui mõni kanne ei vaja korrigeerimist, saate need korrigeeriva arve mustandist eemaldada. Ainult osalise koguse ümber pööramiseks või tagastamiseks, saate rea üksikasjade välja Kogus redigeerida. Arve rea üksikasjade avamisel näete algse arve kogust. Seejärel saate praegust arve kogust redigeerida nii, et see on algse arve kogusest väiksem või suurem.

Korrigeeriva arve kinnitamisel tühistatakse algselt arvestatud müügi tegelik väärtus ja luuakse uus tegelik arve. Kui kogust on vähendatud, põhjustab erinevus uue arveldamata müügi tegeliku loomise. Näiteks kui algne arvestatud müük oli kaheksa tundi ja parandatud arverea üksikasjadel on vähendatud kogust kuus tundi, pööratakse algne arvestatud müügirida ümber ja luuakse kaks uut tegelikku väärtust.

- Arvestatud müük on tegelikult kuus tundi.
- Ülejäänud kahe tunni eest arveldamata müügi tegelik väärtus. See tehing võib olla kas hiljem arvestatud või märgitud mitte-tasuna, olenevalt läbirääkimistest kliendiga.


[!INCLUDE[footer-include](../includes/footer-banner.md)]