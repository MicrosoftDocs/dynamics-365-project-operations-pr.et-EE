---
title: Projekti värskendamine
description: Selles teemas kirjeldatakse Project Operationsis projektide värskendamist.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: b0ec03a2c4dd7bc833b22b7a93fed810b4998a2788f4ff40234e3dd163bd9eb6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000886"
---
# <a name="update-a-project"></a>Projekti värskendamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Allpool on kokkuvõte väljadest, mida saab projektis värskendada pärast selle loomist ja mis tahes värskendustega seotud tagajärgedest.

## <a name="project-detail-fields"></a>Projekti üksikasjade väljad

- **Nimi**: Projekti pealkiri.
- **Kirjeldus**: Projekti ülevaade.
- **Klient**: ettevõte, kellele projekt toimetatakse.
- **Kalendri Mall**: projekti tööaeg. Pärast välja muutmist arvutatakse kogu ajakava ümber.
- **Valuuta**: projekti valuuta. See väli vaikeväärtus põhineb lepingut sõlmiva üksuse määratletud valuutal. Kui lepingut sõlmivat üksust värskendatakse, värskendatakse ka seda välja.
- **Lepingut sõlmiv üksus**: organisatsiooniüksus, mis esindab ettevõtte rühma või allüksust, kes vastutab peamiselt müügi võitmise eest ja tööde ning teenuste kliendile pakkumise eest. 
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