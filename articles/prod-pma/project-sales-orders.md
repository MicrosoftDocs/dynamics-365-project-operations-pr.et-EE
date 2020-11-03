---
title: Projekti müügitellimused aja- ja materjalikulu projektidele
description: Selles teemas selgitatakse, kuidas luua aja- ja materjalikulu projektidele projektipõhiseid müügitellimusi.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074941"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projekti müügitellimused aja- ja materjalikulu projektidele

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua projekti jaoks müügitellimust. Müügitellimusi saab luua ainult **aja- ja materjalikulu** tüüpi projektidele.

Kui aja- ja materjalikulu projektil on projekti lepingus mitu rahastamisallikat, peate lubama lehel **Projektihalduse ja raamatupidamise parameetrid** parameetri **Luba mitme rahastamisallikaga projekti jaoks müügitellimused**. 

> [!NOTE]
> - Mitme rahastamisallikaga projekti müügitellimuste tugi on saadaval alates rakenduse väljalaskest 10.0.2 ja uuemad versioonid.
> - Mitme rahastamisallikaga projekti müügitellimuste toe lubamise parameeter eemaldatakse 2020. aasta aprilli väljalaske lainest, pärast mida on funktsioon alati lubatud.

Projektipõhiseid müügitellimusi saate luua kahel viisil.

- Avage projekt ise. Valige tegevuspaanil suvand **Halda > Üksuse tööülesanded > Müügitellimus**. Projekti teave kuvatakse vaikimisi projekti müügitellimuses. Kui projekti lepingus on rohkem kui üks rahastamisallikas, peate valima rahastamisallika, et määrata müügitellimusele klient. Kui projektil on ainult üks rahastamisallikas, määratakse klient automaatselt.
- Avage loendi leht **Kõik müügitellimused** ja looge uus müügitellimus. Peate valima müügitellimuse jaoks projekti. Pärast projekti valimist määratakse klient rahastamisallikast või teil tuleb valida rahastamisallikas, kui projekti lepingus on mitu rahastamisallikat.
