---
title: Ressursi vastavusseviimise ülevaade
description: See teema pakub teavet ressursi broneeringute ja projektide määramise sobimise tagamise kohta.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 1b60ed9d15f51ff01f27bcc231f5db27513a838f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897446"
---
# <a name="resource-reconciliation-overview"></a>Ressursi vastavusseviimise ülevaade

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Meeskonnaliikmete puhul on broneeringud ja tööülesanded lõdvalt ühendatud. Teisisõnu, ressurssidel võivad olla määramised, kuid ei mingeid broneeringuid, või neil võib olla broneeringuid, kuid mitte määramisi. Ideaalis tuleks reserveeringud ja ülesanded viia vastavusse, nii et ressursid on toime pannud võimsuse täitmiseks tööülesandeid. Kuid broneeringud võivad põhineda saadavusel ja tööülesande ajastused võivad projekti jätkudes muutuda. Seega pakub broneeringute ja ülesannete vaba ühendamine paindlikkust.

Vormi **Projekt** vahekaart **Vastavusseviimine** võimaldab projektijuhtidel ühitada meeskonnaliikmete reserveeringud ja nende määramised projekti meeskondadele.

Vahekaardil **Vastavusseviimine** on kuvatud ka reserveeringud ja ülesanded, mis on seotud iga meeskonnaliikme tööülesande määramise tasemega. Tunde kuvatakse lahtrites, mis esindavad ajavahemikke kuude ja päevade kaupa.

Vahekaardil kuvatakse ka projekti üldine neto kogusumma koos veeruga **Kokku**.

Iga ressursi puhul arvutab vahekaart meeskonnaliikme reserveeringute ja meeskonnaliikme tööülesannete määramise vahe. Ideaalis peaks see erinevus olema 0 (null). Teisisõnu ei tohiks broneeringute ja ülesannete vahel olla vahet. Erinevused on värvitud ja varjutatud, et juhtida tähelepanu kahele tingimusele.

- **Broneeringu puudujääk** – broneeringu puudujääk ilmneb siis, kui ressursil on rohkem määramisi kui broneeringuid. Kuna seda võimsust pole reserveeritud, võib projektijuht soovida selle tingimuse parandamist, pikendades ressursi reserveeringud puudujäägi katteks.
- **Liigsed broneeringud** – üleliigsed broneeringud ilmnevad, kui ressurss on projektile broneeritud, kuid seda pole ülesannetele määratud. See tingimus võib olla vastuvõetav juhul, kui ressurss oli projektile broneeritud enne tööülesande määramise toimumist. Kuid teistel juhtudel ressurssi ei kavandata tööülesannetele määrata. Sellisel juhul peaks projektijuht kaaluma ressursi broneeringute tühistamist, et võimsust saaks kasutada mõne muu projekti jaoks.

Mõnel juhul, kui te vaatate aega kõrgemal tasemel kui päeva tasemel (näiteks kuu tasand), võidakse kuvada ressursi neto erinevus (teisisõnu, broneerimine = määramine). Kuid kui te vaatate aega nädala tasemel, võite näha, et seal on määramised null tundi ja broneeringud 40 tundi esimesel nädalal, kuid määramine 40 tundi ja broneerimine null tundi teisel nädalal. Kokkuvõttes lepitakse reserveeringud ja määramised kokku, kuid nad erinevad ühe nädala jooksul järgmisena.

Kui vaatate aega kõrgemal tasemel, on vahekaardil **Vastavusseviimine** määratud lahtrite indikaator, mis teatab, et madalamatel tasanditel on erinevusi. Lahtrit topeltklõpsates saate erinevuse vaatamiseks suumida. Seejärel saate väljasuumimiseks paremklõpsu teha. Valides ressursi ja kasutades seejärel ruudustiku tööriistaribal juhtelementi **Järgmine erinevus**, saate minna järgmisele erinevusele selle ressursi reserveeringute ja ülesannete vahel. Seejärel saate tagasiminemiseks kasutada juhtelementi **Eelmine erinevus**. Samuti saate suvandi **Sätted** kaudu erinevuste indikaatori ja navigeerimise käitumise välja lülitada.


Kui teil on ressursi jaoks tööülesanded, kuid ei mingeid broneeringuid,valige lehel **Projektid** vahekaardil **Vastavusseviimine** broneeringu puudujääk, seejärel valige käsk **Pikenda reserveeringut**. Kuvatakse dialoogiboks **Pikenda reserveeringut** ja kuvatakse broneering, mis on vajalik ressursi puudujäägi lahendamiseks. See näitab ka ressursi olemasolevaid broneeringuid kõigis projektides või muudes kavandatud üksustes. Kui valite ressursi reserveeringu loomiseks valiku **OK**, võite selle ressursi saadavusest olenemata põhjustada ülebroneeringu.

Projektijuht või ressursihaldur saab seejärel kasutada ajakavapaneeli, et hallata mis tahes olukordi, kus ressurss on üle broneeritud.

