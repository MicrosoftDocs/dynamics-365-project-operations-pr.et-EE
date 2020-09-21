---
title: Projekti etapid
description: Selles teemas antakse teavet projektiga seotud etappide kohta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750939"
---
# <a name="project-stages"></a>Projekti etapid 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekti etappe värskendatakse, et kajastada projekti edenedes selle olekut. Vaikimisi äriprotsessi voog (BPF) värskendab mõnda projekti etappi automaatselt, samas kui teisi värskendab projektijuht käsitsi. 

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
