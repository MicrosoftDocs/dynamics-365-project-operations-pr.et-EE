---
title: Soovitatavate ressursside ülevaade
description: Selles teemas kirjeldatakse projektile ressursside pakkumist.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401168"
---
# <a name="review-proposed-resources"></a>Soovitatavate ressursside ülevaade

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Ressursihaldurid saavad projektijuhile ressursi pakkuda ressursitaotluse kaudu.

1. Tehke taotluse ruudustikust või taotlusest endast valik **Ressursside leidmine**
2. Valige lehel **Ajakava abimees** ressurss ja seejärel tehke paani **Ressursi broneeringu loomine** väljal **Broneeringu olek** valik **Broneeri**.

Ilmnevad järgmised olekuvärskendused.

- Lehel **Ajakava abimees** värskendatakse olekuindikaatoreid näitamaks, et broneering on soovituslik, mitte fikseeritult broneeritud.
- Ressursitaotluses muudetakse olekuks **Vajab ülevaatamist**.
- Projekti vahekaardil **Meeskond** muudetakse üldiste meeskonnaliikmete väärtus **Taotluse olek** väärtusele **Vajab ülevaatamist**.

Projektijuht saab ettepaneku vastu võtta või tagasi lükata.

Ressursihaldurid saavad ressursitaotluste töötlemisel kasutada kõiki järgmiseid meetodeid.

- Pakkuda nõudluse rahuldamiseks mitmeid ressursse, kui nõutavate tundide täitmiseks pole saadaval ühte ainukest ressurssi. Seejärel jaotatakse pakutud tunnid mitme ressursi vahel, mis suudavad nõutavate tundide nõudlust rahuldada. Selle stsenaariumi korral ei saa tunnid kattuda.
- Pakkuda vähem ressursse, kui on vaja. Selle stsenaariumi korral on pakutud ressursi võimsus väiksem kui nõutavad tunnid, mille taotleja määras. Seega, kui taotleja võtab pakutud ressursid vastu, luuakse ülejäänud nõudluse hõivamiseks täitmata ressursi nõue.
- Broneerida nõudluse rahuldamiseks mitmeid ressursse, kui töö lõpule viimiseks pole saadaval ühte ainukest ressurssi.
- Broneerida vähem ressursse, kui on vaja. Sel juhul on broneeritud tunde vähem kui nõutud tunde. Süsteem juhendab teid, et pakuksite broneeringute asemel ressursse, et taotleja saaks järelejäänud nõudlust kontrollida ja jälgida.

## <a name="resource-availability"></a>Ressursi saadavus

On ülioluline, et ressursihaldurid saaksid vaadata ressursside saadavust ja värskendada broneeringuid. Mõnel juhul ametlik nõudlus puudub (ressursitaotlus), kuid ressursihaldur peab vastama kavandamata nõudlusele, mis esitatakse selliste kanalite nagu meil, telefonikõne või kiirsõnumid kaudu. Ressursihaldurid kasutavad ajakavapaneeli ressursside ja broneeringute värskendamiseks.

Ressurssi töötundide alusel arvutatakse ressursi saadavust. Ressursibroneeringud tarbivad ressursside võimsust.

Ajakavapaneel kasutab broneeringute, saadavuse ja ülebroneerimiste ning ka broneeringute oleku kuvamiseks värve ja varjustust. Ajakavapaneeli üks säte võimaldab teil kuvada legendi.

Kui ajakavapaneelil kuvatakse konkreetse broneeritava ressursi kõrval parempoole suunatud nool, saab ressurssi laiendada, et kuvada selle töö üksikasju, millele ressurss on broneeritud.

Kuna rakendus Dynamics 365 Project Operations kasutab mootorit Universal Resource Scheduling, ja kui teil on installitud ka rakendus Dynamics 365 Field Service, saate vaadata üksikasju projektide ressursibroneeringute, töötellimuste ja muude olemite kohta, millele olete kavandamise laiendanud.

Konkreetse ressursi kohta lisateabe saamiseks paremklõpsake seda, et avada ressursikaart.

