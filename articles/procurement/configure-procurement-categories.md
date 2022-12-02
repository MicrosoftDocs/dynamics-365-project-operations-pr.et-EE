---
title: Kasutage hankekategooriaid projekti ostutellimuste ja ootel hankija arvetega
description: See artikkel kirjeldab, kuidas konfigureerida hankekategooriaid, mida saab kasutada projekti ostutellimuste ja ootel hankija arvetega.
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
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Kasutage hankekategooriaid projekti ostutellimuste ja ootel hankija arvetega

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Ostuspetsialistid saavad luua ja hallata kaupade ja teenuste katalooge, mida saab kasutada projekti ostutellimustes ja ootel hankija arvetes. [Hankekataloogid](/dynamics365/supply-chain/procurement/procurement-catalogs) annavad teile lihtsa võimaluse oste kategoriseerida, ilma et peaksite välja antud tootekataloogi konfigureerima ja kasutama. Iga hankekategooria saab aja-, kulu- või kaubatehingute jaoks vastendada projektikategooriaga. Pärast hankekategooriat kasutava ootel hankija arve postitamist loob süsteem aja-, kulu- või materjaliprojekti tegelikud näitajad, projektitehingud ja alammooduli kanded.

## <a name="minimum-version-requirements"></a>Versiooni miinimumnõued

Teenuse Microsoft Dynamics 365 Project Operations logimata/ressursipõhiste stsenaariumide projekti ostutellimustega hankekategooriate kasutamiseks on vaja järgmisi versioone:

- Rakenduse Project Operations Dataverse lahenduse versioon 4.41.0.45 või uuem versioon
- Finants- ja äritoimingute keskkonna versioon 10.0.26 või uuem versioon

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Käivitage hankekategooria toe jaoks kahekordselt kirjutatud kaardid

Veenduge, et **Project Operationsi integratsiooniprojekti hankija arve rea ekspordiolem msdyn\_projectvendorinvoicelines** vastendus kasutaks versiooni 1.0.0.4 või uuemat versiooni.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Lubage hankekategooriate funktsioonivõti

Projekti ostutellimustega hankekategooriate kasutamise funktsiooni lubamiseks järgige neid etappe.

1. Teenuses Dynamics 365 Finance avage tööruum **Funktsioonihaldus**.
1. Leidke funktsioonide nimekirjast funktsioon **Kasuta hankekategooriaid rakenduses Project Operations ressursipõhiste/mittelaopõhiste stsenaariumide puhul** ja valige seejärel **Luba**.

> [!IMPORTANT]
> Selle eeltingimusena tuleb lubada ka funktsioon **Luba ootel hankija arved rakenduse Project Operations ressursipõhiste/mittelaopõhiste stsenaariumide jaoks**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Vastendage projekti kategooriad hankekategooria hierarhias

Järgige järgmisi etappe, et seostada projektikategooriad hankekategooriatega **Hankekategooria** hierarhias.

1. Minge jaotisesse **Hanked ja hankimine \> Hankekategooriad**.
1. Valige **Redigeeri kategooriahierarhiat**.
1. Valige soovitud kategooria hierarhiasõlm ja seejärel seostage vahekaardil **Projekti kategooriate määramine** sõlme projektikategooriaga kategooriast **Aeg**, **Kulu** või **Üksuse projekt** (st kategooriast **Vaikeaeg** või **Vaikekulu**).
1. Valige **Salvesta**.
1. Sulgege leht.

> [!NOTE]
> Hankekategooria seostamine projektikategooriaga on valikuline. Kui hankekategooriat ei ole vastendatud, kasutab süsteem väärtust, mis on määratud **Üksuse** väljal **Projekti kategooria vaikimisi** jaotises **Project Operations on Dynamics 365 Customer engagement** vahekaardil **Projektijuhtimise ja raamatupidamise parameetrid**.
