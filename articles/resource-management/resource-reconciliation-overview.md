---
title: Ressursi vastavusseviimise ülevaade
description: Selles teemas antakse teavet, mis aitab teil tagada, et ressursside broneeringud ja projektidele määramised on joondatud.
author: ruhercul
ms.date: 01/08/2021
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
ms.openlocfilehash: be171063c21318f517a37f3088e3f577fd4b6715
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000836"
---
# <a name="resource-reconciliation-overview"></a>Ressursi vastavusseviimise ülevaade

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Meeskonnaliikmete puhul on broneeringud ja tööülesanded lõdvalt ühendatud. Teisisõnu, ressurssidel võivad olla määramised, aga ei mingeid broneeringuid, või neil võib olla broneeringuid, aga mitte määramisi. Ideaalis tuleks reserveeringud ja ülesanded viia vastavusse, nii et ressursid on toime pannud võimsuse täitmiseks tööülesandeid. Kuid broneeringud võivad põhineda saadavusel ja tööülesande ajastused võivad projekti jätkudes muutuda. Seega pakub broneeringute ja ülesannete vaba ühendamine paindlikkust.

Vahekaart **Vastavusseviimine** lehel **Projektid** võimaldab projektijuhtidel ühitada meeskonnaliikmete reserveeringud ja nende määramised projekti meeskondadele.

Vahekaardil **Vastavusseviimine** on kuvatud reserveeringud ja ülesanded, mis on seotud iga meeskonnaliikme tööülesande määramise tasemega. Tunnid on näidatud lahtrites, mis esindavad ajavahemikke kuude ja päevade kaupa. Vahekaardil kuvatakse ka projekti üldine neto kogusumma koos veeruga **Kokku**.

Iga ressursi puhul arvutab vahekaart **Vastavusseviimine** meeskonnaliikme broneeringute ja meeskonnaliikme tööülesannete määramise vahe. Ideaalis peaks see erinevus olema 0 (null). Teisisõnu ei tohiks broneeringute ja ülesannete vahel olla vahet. Erinevused on värvitud ja varjutatud, et juhtida tähelepanu kahele tingimusele.

- **Broneeringu puudujääk** – broneeringu puudujääk ilmneb siis, kui ressursil on rohkem määramisi kui broneeringuid. Kuna seda võimsust pole reserveeritud, võib projektijuht soovida selle tingimuse parandamist, pikendades ressursi reserveeringud puudujäägi katteks.
- **Liigsed broneeringud** – üleliigsed broneeringud ilmnevad, kui ressurss on projektile broneeritud, kuid seda pole ülesannetele määratud. See tingimus võib olla vastuvõetav juhul, kui ressurss oli projektile broneeritud enne tööülesande määramise toimumist. Kuid muudel juhtudel, kui pole plaani ressurssi ülesannetele määrata, peaks projektijuht kaaluma ressursi broneeringute tühistamist. Sel viisil saab võimsust kasutada mõne muu projekti jaoks.

Mõnel juhul, kui te vaatate aega kõrgemal tasemel kui päeva tasemel (näiteks kuu tasand), võidakse kuvada ressursi neto erinevus (teisisõnu, broneerimine võrdub määramine). Kuid kui te vaatate aega nädala tasemel, võite näha, et seal on määramised null tundi ja broneeringud 40 tundi esimesel nädalal, kuid määramine 40 tundi ja broneerimine null tundi teisel nädalal. Kokkuvõttes lepitakse reserveeringud ja määramised kokku, kuid nad erinevad ühe nädala jooksul järgmisena.

Kui vaatate aega kõrgemal tasemel, on vahekaardil **Vastavusseviimine** määratud lahtrite indikaator, mis teatab, et madalamatel tasanditel on erinevusi. Lahtrit topeltklõpsates saate erinevuse vaatamiseks suumida. Seejärel saate väljasuumimiseks valida ja hoida (või paremklõpsu teha). Valides ressursi ja kasutades seejärel ruudustiku tööriistaribal juhtelementi **Järgmine erinevus**, saate minna järgmisele erinevusele selle ressursi reserveeringute ja ülesannete vahel. Seejärel saate tagasiminemiseks kasutada juhtelementi **Eelmine erinevus**. Samuti saate suvandi **Sätted** kaudu erinevuste indikaatori ja navigeerimise käitumise välja lülitada.

Kui teil on ressursi jaoks tööülesanded, kuid ei mingeid broneeringuid, valige broneeringu puudujääk vahekaardil **Vastavusseviimine** lehel **Projektid** ja seejärel valige **Pikenda broneeringut**. Kuvatav dialoogiboks **Pikenda reserveeringut** näitab broneeringut, mis on vajalik ressursi puudujäägi lahendamiseks. Dialoogiboks näitab ka ressursi olemasolevaid broneeringuid kõigis projektides või muudes kavandatud üksustes. Kui valite ressursi reserveeringu loomiseks valiku **OK**, võite selle ressursi saadavusest olenemata põhjustada ülebroneeringu.

Broneeringud, mis on loodud **Broneeringu pikendamise** toimingu kaudu seostatakse esmase projekti nõudega. Kui pikendus on algatatud, saab määratleda konkreetsed nõuded, mida tuleb pikendada, sest ressurss võib olla seotud projekti rohkem kui ühe nõudega.

Projektijuht või ressursihaldur saab seejärel kasutada ajakavapaneeli, et hallata mis tahes olukordi, kus ressurss on üle broneeritud.


[!INCLUDE[footer-include](../includes/footer-banner.md)]