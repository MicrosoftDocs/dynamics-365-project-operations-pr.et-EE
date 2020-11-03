---
title: Soovitatavate ressursside ülevaade
description: Selles teemas kirjeldatakse projektile ressursside pakkumist.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074923"
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

## <a name="billable-utilization"></a>Tasustatav kasutus

Ressurssidel võib olla tasustatav sihtkasutus. See sihtkasutus on määratletud kas ressursi vaikerolli atribuudina või määratud iga broneeritava ressursi kirjele. Kasutuse arvutused põhinevad tegelikel tundidel, mida ressursid on kinnitatud ajakandeid kasutades edastanud.

Kasutuse arvutamiseks kasutatakse järgmiseid valemeid.

- Tasustatav kasutus = arveldatavad tegelikud tunnid ÷ ressursivõimsus
- Mittetasustatav kasutus = tegelik aeg koos arveldustüübi ID-ga = mittetasustatav, täiendav või pole saadaval ÷ ressursivõimsus
- Sisemine = tegelik aeg ilma müügilepinguta ÷ ressursivõimsus
- Ressursivõimsus = ressursi töötunnid – kontorist väljasolek – puhkepäevad

Vaate **Ressursikasutus** leiate paanilt **Ressursid**.

Iga ruudustiku lahter esindab perioodis (nt päev, nädal või kuu) oleva ressursi tasustatavat kasutusprotsenti. Lahtrite värvimiseks kasutatakse järgmisi valemeid.

- **Roheline:** tasustatav kasutus \>= ressursi sihtkasutus
- **Kollane:** sihtkasutus – 20 \<= tasustatav kasutus \< sihtkasutus
- **Punane:** tasustatav kasutus \< sihtkasutus – 20

Kuna vaade **Ressursikasutus** põhineb ajakavapaneelil, saate oma tulemuste filtreerimiseks kasutada ajakavapaneeli filtreerimise võimalusi.

Ruudustik nõuab, et määraksite sihtkasutuse kas rollile või konkreetsele ressursile. Selle seadistamiseks tehke valikud **Ressursid** \> **Ressursi rollid**.

Peale selle tuleb igale broneeritavale ressursile määrata vaikeroll. Avage **Ressursid** \> **Ressursid**. Kontrollige vahekaardil **Project Service** , et ressursi roll oleks määratletud ja selle väli **On vaikimisi** oleks määratud väärtusele **Jah**. Saate lisada veel rolle, kus väärtus **On vaikimisi = Ei**. Roll, kus väärtust **On vaikimisi = Jah** , kasutatakse ressursi kasutuse hindamiseks selle rolli eesmärgi suhtes.

Vahekaardil **Project Service** saate ressursi jaoks määrata ka eraldi sihtkasutuse. Seejärel kasutab kasutuse arvutus seda sihtkasutust, et hinnata ressursi sihti, mitte ressursi vaikerolli sihti.

Ressursi jaoks kuvatakse kasutus ainult juhul, kui sellel ressursil on ruudustikus kuvatud perioodi jooksul kinnitatud, arveldatavat aega.

## <a name="resource-availability"></a>Ressursi saadavus

On ülioluline, et ressursihaldurid saaksid vaadata ressursside saadavust ja värskendada broneeringuid. Mõnel juhul ametlik nõudlus puudub (ressursitaotlus), kuid ressursihaldur peab vastama kavandamata nõudlusele, mis esitatakse selliste kanalite nagu meil, telefonikõne või kiirsõnumid kaudu. Ressursihaldurid kasutavad ajakavapaneeli ressursside ja broneeringute värskendamiseks.

Ressurssi töötundide alusel arvutatakse ressursi saadavust. Ressursibroneeringud tarbivad ressursside võimsust.

Ajakavapaneel kasutab broneeringute, saadavuse ja ülebroneerimiste ning ka broneeringute oleku kuvamiseks värve ja varjustust. Ajakavapaneeli üks säte võimaldab teil kuvada legendi.

Kui ajakavapaneelil kuvatakse konkreetse broneeritava ressursi kõrval parempoole suunatud nool, saab ressurssi laiendada, et kuvada selle töö üksikasju, millele ressurss on broneeritud.

Kuna rakendus Dynamics 365 Project Operations kasutab mootorit Universal Resource Scheduling, ja kui teil on installitud ka rakendus Dynamics 365 Field Service, saate vaadata üksikasju projektide ressursibroneeringute, töötellimuste ja muude olemite kohta, millele olete kavandamise laiendanud.

Konkreetse ressursi kohta lisateabe saamiseks paremklõpsake seda, et avada ressursikaart.

