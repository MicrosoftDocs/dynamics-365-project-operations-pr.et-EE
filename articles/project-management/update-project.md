---
title: Projekti loomine ja värskendamine
description: Selles teemas kirjeldatakse Project Operationsis projektide värskendamist.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d0847b5343cf3e353b91eae04c94509f14213ba5
ms.sourcegitcommit: 51224cb3bf7cdeae6614d39fc8d899c83dbad5f2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/23/2021
ms.locfileid: "7678344"
---
# <a name="create-and-update-a-project"></a>Projekti loomine ja värskendamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Järgmine on kokkuvõte väljadest, mida saab projektis pärast selle loomist värskendada. See hõlmab ka kõiki kohalduvaid mõjusid, mis põhinevad neil värskendustel.

## <a name="project-detail-fields"></a>Projekti üksikasjade väljad

- **Nimi**: Projekti pealkiri.
- **Kirjeldus**: Projekti ülevaade.
- **Klient**: ettevõte, kellele projekt toimetatakse.
- **Kalendri Mall**: projekti tööaeg. Pärast välja muutmist arvutatakse kogu ajakava ümber.
- **Valuuta**: projekti valuuta. Selle välja vaikeväärtus põhineb valuutal, mis on määratletud lepingut sõlmivas üksuses. Kui lepingut sõlmivat üksust värskendatakse, värskendatakse ka seda välja.
- **Lepingut sõlmiv üksus**: organisatsiooniüksus, mis esindab ettevõtte rühma või allüksust, kes vastutab peamiselt müügi võitmise eest ja tööde ning teenuste kliendile pakkumise eest.  Kui projektijuhi organisatsiooniüksust pole määratletud, siis määratakse selle välja väärtuseks vaikimisi projekti parameetrites määratletud väärtus.
- **Projektijuht**: projekti meeskonnaliige, kellel on õigus ajakirjeid ja kulusid üle vaadata ning kinnitada.

## <a name="estimate-fields"></a>Väljade prognoosimine

- **Prognoositav alguskuupäev**: projekti alustamise kuupäev. Kui see väli on värskendatud, teisaldatakse projekti kõik tööülesanded proportsionaalselt uue alguskuupäevaga.
- **Lõppkuupäev**: kuupäev, millele on kavandatud projekti lõpetamine.
- **Tööpanus**: projekti prognoositav panus. Kui projektile lisatakse tööülesanded, siis seda välja enam muuta ei saa.
- **Eeldatav tööjõukulu**: projekti eeldatav tööjõukulu. Kui projektile lisatakse tööjõukulud, siis seda välja enam muuta ei saa.
- **Prognoositavad kulud**: projekti prognoositavad kulud. Kui projektile lisatakse kulud, siis seda välja enam muuta ei saa.

## <a name="project-actual-fields"></a>Projekti tegelike näitajate väljad
- **Tegelik algus**: projekti käivitamise päev.
- **Tegelik lõpp**: värskendatakse projekti lõpetamisel.

## <a name="project-status-fields"></a>Projekti oleku väljad

- **Projekti üldine olek**: projektijuhi antud üldine projekti tervis.
- **Kommentaarid**: projektijuhi antud narratiiv projekti praeguse tervise kohta.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
