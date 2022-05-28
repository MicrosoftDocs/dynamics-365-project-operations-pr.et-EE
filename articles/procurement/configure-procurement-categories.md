---
title: Hankekategooriate kasutamine projekti ostutellimuste ja ootel hankija arvetega
description: Selles teemas kirjeldatakse, kuidas konfigureerida hankekategooriaid, mida saab kasutada projekti ostutellimuste ja ootel hankija arvetega.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613331"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Hankekategooriate kasutamine projekti ostutellimuste ja ootel hankija arvetega

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Ostuspetsialistid saavad luua ja hallata nende kaupade ja teenuste katalooge, mida saab kasutada projekti ostutellimustes ja ootel hankija arvetes. [Hankekataloogid](/dynamics365/supply-chain/procurement/procurement-catalogs) annavad teile lihtsa viisi ostude kategoriseerimiseks, ilma et peaksite konfigureerima ja kasutama väljastatud toodete kataloogi. Aja-, kulu- või kaubakannete puhul saab iga hankekategooria vastendada projektikategooriaga. Pärast hankekategooriat kasutava ootel hankija arve konteerimist loob süsteem aja-, kulu- või materjaliprojekti tegelikud andmed, projektikanded ja alammooduli kanded.

## <a name="minimum-version-requirements"></a>Versiooni miinimumnõuded

Microsofti Dynamics 365 Project Operations ladustamata/ressursipõhiste stsenaariumide jaoks projekti ostutellimustega hankekategooriate kasutamiseks on vaja järgmisi versioone.

- Project Operationsi Dataverse lahenduse versioon 4.41.0.45 või uuem versioon
- Rahandus- ja operatsioonide keskkonnaversioon 10.0.26 või uuem versioon

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Hankekategooria toe topeltkirjutuskaartide käivitamine

Veenduge, et Project Operationsi integreerimise projekti hankija arve rea ekspordiolemi msdyn **projectvendorinvoicelines\_ vastendamine kasutaks** versiooni 1.0.0.4 või uuemat versiooni.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Hankekategooriate funktsioonivõtme lubamine

Järgige neid juhiseid hankekategooriate kasutamise funktsiooni lubamiseks projekti ostutellimustega.

1. Avage Dynamics 365 Finance **funktsioonihalduse** tööruum.
1. Otsige funktsiooniloendist üles **funktsioon Kasuta hankekategooriaid projektitoimingutes ressursipõhiste/ladustamata stsenaariumide** jaoks ja seejärel valige **Luba**.

> [!IMPORTANT]
> Eeltingimusena peate lubama **ka funktsiooni Luba ootel hankija arved Project Operationsis ressursipõhiste/ladustamata stsenaariumide** jaoks.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Projektikategooriate vastendamine kategoorias Hanked

Projektikategooriate vastendamiseks hankekategooriatega kategoorias Hange kategooria **hierarhias** tehke järgmist.

1. **Avage hanke- ja hankekategooriad \> Hanked**.
1. Valige **Redigeeri kategooriahierarhiat**.
1. Valige soovitud kategooriahierarhia sõlm ja seejärel seostage vahekaardil Projektikategooriate **määramine sõlm projektikategooriaga kategooriast Aeg**, Kulu**või **"Kaubaprojekt"** (st **kategooria Vaikeaeg** **või** Vaikekulu **).**
1. Valige **Salvesta**.
1. Sulgege leht.

> [!NOTE]
> Hankekategooria vastendamine projektikategooriaga on valikuline. Kui hankekategooriat pole vastendatud, kasutab süsteem väärtust, mis on seatud **lehe Projektihaldus- ja raamatupidamisparameetrite** **vahekaardi** Project 365 Customer engagement **jaotises Projekti kategooria vaikesätted jaotises** Projekti kategooria vaikesätted väljal **Kaup**.
