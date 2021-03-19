---
title: Projekti etappide tüübid
description: Selles teemas antakse teavet projektiga seotud etappide kohta.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3503b17e54fc0b321582c30ce534e4cb3f497a5f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283678"
---
# <a name="project-stage-types"></a>Projekti etappide tüübid 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekti etapid kujundatakse, et kajastada projekti edenedes selle olekut. Kohandusi saab kasutada äriprotsessi voogude, Power Automate’i või lisandmooduli laiendite etappide automaaseks värskendamiseks.

Järgmised etapid on määratletud vaikimisi BPF-is.

- Uus
- Hinnapakkumine
- Plaan
- Üleandmine
- Lõpuleviimine
- Sule 

## <a name="new"></a>Uus

Projekti loomisel määratakse selle olekuks **Uus**. Kui projekt loodi mallist, võivad sellel olemas olla ajakava, prognoosi ja meeskonna andmed. Muul juhul on tegemist lihtsalt projekti kavandiga ja ülejäänud komponendid tuleb sisestada.

## <a name="quote"></a>Hinnapakkumine

Kui seostate projekti hinnapakkumisega või kui loote projekti hinnapakkumise põhjal, määratakse projekti olekuks **Hinnapakkumine**, ja eeldatavaid algus- ning lõppkuupäevi värskendatakse. Kuniks projekt on etapis **Hinnapakkumine**, kuvab lehe **Projektiolem** vahekaart **Müügid** hinnapakkumise üksikasjad.

## <a name="plan"></a>Plaan

Kui võidate projektiga seotud hinnapakkumise ja projekt jõuab etappi **Leping**, värskendatakse projekt olekule **Plaan**. Kuniks projekt on etapis **Plaan**, kuvab leht **Projektiolem** lepingu üksikasjad.

## <a name="deliver"></a>Üleandmine

Kui olete projektiplaani lõpule viimisel projekti käivitamiseks valmis, peab projektijuht värskendama projekti etapile **Üleandmine**, näitamaks, et projektiga on alustatud.

## <a name="complete"></a>Lõpuleviimine 

Kui projekti töö on lõpule viidud, saab projektijuht värskendada projekti etapile **Lõpuleviimine**. Projekti määramisega etapile **Lõpuleviimine** näitab projektijuht, et töö on 100% lõpetatud, kuid projekti hoitakse avatuna, et mis tahes ootelolevaid aja- või kulukirjeid saaks talletada.

## <a name="close"></a>Sule

Kui projekti jaoks on kõik kanded talletatud, saab projektijuht värskendada projekti etapile **Sule**. Sel hetkel ei saa kandeid enam talletada ja projekt on seatud kirjutuskaitstuks.


[!INCLUDE[footer-include](../includes/footer-banner.md)]