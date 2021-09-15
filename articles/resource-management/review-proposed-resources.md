---
title: Soovitatavate ressursside ülevaade
description: Selles teemas kirjeldatakse projektile ressursside pakkumist.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b3077f98052fcac9989a81b2fab12fa30d65d970
ms.sourcegitcommit: ebcaec7806ee8aee1323ef532d5b7735d27edd04
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403790"
---
# <a name="review-proposed-resources"></a>Soovitatavate ressursside ülevaade

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Ressursihaldurid saavad projektijuhile ressursi pakkuda ressursitaotluse kaudu.

Soovitatud ressursside ülevaatamiseks toimige järgmiselt.

1. Tehke ruudustikus **Taotlus** või taotlusest endast valik **Ressursside leidmine**.
2. Valige lehel **Ajakava abimees** ressurss ja seejärel kinnitage, et kõik soovitatud tunnid on soovitatud broneeringusse kaasatud.
3. Seadistage paanil **Ressursi broneeringu loomine** välja **Broneeringu olek** väärtuseks **Soovitatav** ja seejärel valige **Broneeri**.

    > [!NOTE]
    > **Broneeringu oleku** seadistamine olekusse **Soovitatav** ei broneeri ressurssi fikseeritult ja ei asenda üldist ressurssi nimetatud meeskonnaliikmega.

    Ilmnevad järgmised olekuvärskendused.

    - Lehel **Ajakava abimees** värskendatakse olekuindikaatoreid näitamaks, et broneering on soovituslik, mitte fikseeritult broneeritud.
    - Ressursitaotluses muudetakse olekuks **Vajab ülevaatamist**.
    - Projekti vahekaardil **Meeskond** muudetakse üldiste meeskonnaliikmete väärtus **Taotluse olek** väärtusele **Vajab ülevaatamist**.

Projektijuht saab ettepaneku kas vastu võtta või tagasi lükata.

Ressursihaldurid saavad ressursitaotluste töötlemisel kasutada kõiki järgmiseid meetodeid.

- Pakkuda nõudluse rahuldamiseks mitmeid ressursse, kui nõutavate tundide täitmiseks pole saadaval ühte ainukest ressurssi. Seejärel jaotatakse pakutud tunnid mitme ressursi vahel, mis suudavad nõutavate tundide nõudlust rahuldada. Selle stsenaariumi korral ei saa tunnid kattuda.
- Pakkuda vähem ressursse, kui on vaja. Selle stsenaariumi korral on pakutud ressursi võimsus väiksem kui nõutavad tunnid, mille taotleja määras. Kui taotleja võtab pakutud ressursid vastu, luuakse ülejäänud nõudluse hõivamiseks täitmata ressursi nõue.
- Broneerida nõudluse rahuldamiseks mitmeid ressursse, kui töö lõpule viimiseks pole saadaval ühte ainukest ressurssi.
- Broneerida vähem ressursse, kui on vaja. Sel juhul on broneeritud tunde vähem kui nõutud tunde. Süsteem juhendab teid, et pakuksite broneeringute asemel ressursse, et taotleja saaks järelejäänud nõudlust kontrollida ja jälgida.

## <a name="resource-availability"></a>Ressursi saadavus

Ressursihaldurid peaksid saama vaadata ressursside saadavust ja värskendada broneeringuid. Mõnel juhul pole formaalset nõudlust (ressursitaotlus). Ressursihaldur peab siiski vastama planeerimata nõudmisele, mis tuleb läbi muude kanalite, nagu meilid, telefonikõned või kiirsõnumid. Ressursihaldurid kasutavad **Ajakavapaneeli** ressursside ja broneeringute värskendamiseks.

Ressurssi töötunde kasutatakse ressursi saadavuse arvutamise alusena. Ressursibroneeringud tarbivad ressursside võimsust.

**Ajakavapaneel** kasutab broneeringute, saadavuse, ülebroneerimiste ja broneeringute oleku kuvamiseks värve ning varjustust. Seadistus **Ajakavapaneelil** võimaldab teil legendi kuvada.

Kui **Ajakavapaneelil** kuvatakse konkreetse broneeritava ressursi kõrval parempoole suunatud nool, saab ressurssi laiendada, et kuvada selle töö üksikasju, millele ressurss on broneeritud.

Kuna rakendus Dynamics 365 Project Operations kasutab mootorit Universal Resource Scheduling, ja kui teil on installitud ka rakendus Dynamics 365 Field Service, saate vaadata üksikasju projektide ressursibroneeringute, töötellimuste ja muude olemite kohta, millele olete kavandamise laiendanud.

Konkreetse ressursi kohta lisateabe saamiseks paremklõpsake seda, et avada ressursikaart.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
