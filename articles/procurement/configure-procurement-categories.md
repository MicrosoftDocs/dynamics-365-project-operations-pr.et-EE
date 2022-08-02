---
title: Hankekategooriate kasutamine projekti ostutellimuste ja ootel hankija arvetega
description: Selles artiklis kirjeldatakse, kuidas konfigureerida hankekategooriaid, mida saab kasutada projekti ostutellimuste ja ootel hankija arvetega.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028605"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Hankekategooriate kasutamine projekti ostutellimuste ja ootel hankija arvetega

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Ostuspetsialistid saavad luua ja hallata katalooge kaupadest ja teenustest, mida saab kasutada projekti ostutellimustes ja ootel hankija arvetes. [Hankekataloogid](/dynamics365/supply-chain/procurement/procurement-catalogs) annavad teile lihtsa viisi ostude kategoriseerimiseks, ilma et peaksite väljastatud toodete kataloogi konfigureerima ja kasutama. Iga hankekategooria saab vastendada aja-, kulu- või kaubakannete projektikategooriaga. Pärast hankekategooriat kasutava ootel hankija arve sisestamist loob süsteem aja-, kulu- või materjaliprojekti tegelikud, projektikanded ja alammooduli kirjed.

## <a name="minimum-version-requirements"></a>Minimaalsed versiooninõuded

Järgmised versioonid on vajalikud hankekategooriate kasutamiseks projekti ostutellimustega Microsofti Dynamics 365 Project Operations varudeta/ressursipõhiste stsenaariumide korral.

- Project Operationsi Dataverse lahenduse versioon 4.41.0.45 või uuem
- Finance and Operationsi keskkonna versioon 10.0.26 või uuem

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Hankekategooria toe jaoks kahe kirjutisega kaartide käitamine

Veenduge, et vastendamisel **Project Operationsi integreerimise projekti hankija arve rea ekspordi olem msdyn\_ projectvendorinvoicelines** kasutab versiooni 1.0.0.4 või uuemat versiooni.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Hankekategooriate funktsioonivõtme lubamine

Järgige neid juhiseid, et lubada hankekategooriate kasutamise funktsioon projekti ostutellimustega.

1. Avage Dynamics 365 Finance **tööruum Funktsioonihaldus**.
1. Otsige funktsioonide loendist üles **funktsioon Kasuta hankekategooriaid rakenduses Project Operations ressursipõhiste/varumata stsenaariumide** jaoks ja seejärel valige **Luba**.

> [!IMPORTANT]
> Eeltingimusena peate lubama **ka funktsiooni Luba ootel hankija arved project operationsis ressursipõhiste/ladustamata stsenaariumide** jaoks.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Projektikategooriate vastendamine hankekategooriate hierarhias

Järgige neid juhiseid projektikategooriate vastendamiseks hankekategooriatega hankekategooriatega **hankekategooriate** hierarhias.

1. Avage **Hanked ja hanked \> Hankekategooriad**.
1. Valige **Kategooriahierarhia** redigeerimine.
1. Valige soovitud kategooriahierarhia sõlm ja seejärel seostage vahekaardil Projektikategooriate määramine sõlm **projektikategooriaga kategooriast Aeg**, **Kulu** või **Üksus Projekt** (**st kategooria Vaikeaeg** **või** Vaikekulu **).**
1. Valige **Salvesta**.
1. Sulgege leht.

> [!NOTE]
> Hankekategooria vastendamine projektikategooriaga on valikuline. Kui hankekategooriat ei vasteta, kasutab süsteem väärtust, mis on määratud väljal **Kaup** vahekaardil Projektitoimingud Dynamics 365 Customer engagement **vahekaardil** Projektihalduse ja raamatupidamise parameetrid jaotises **Projektikategooria vaikeväärtused** **.**
