---
title: Ressursikasutuse ülevaade
description: Selles teemas antakse teavet ressursi kasutamise kohta rakenduses Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000791"
---
# <a name="resource-utilization-overview"></a>Ressursikasutuse ülevaade

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Ressurssidel võib olla tasustatav sihtkasutus. See sihtkasutus on määratletud ressursi vaikerolli atribuudina või määratud iga broneeritava ressursi kirjele. Kasutuse arvutused põhinevad tegelikel tundidel, mida ressursid on kinnitatud ajakandeid kasutades edastanud.

Kasutuse arvutamiseks kasutatakse järgmiseid valemeid.

  - Tasustatav kasutus = arveldatavad tegelikud tunnid ÷ ressursivõimsus
  - Mittetasustatav kasutus = tegelik aeg koos arveldustüübi ID-ga = mittetasustatav, täiendav või pole saadaval ÷ ressursivõimsus
  - Sisemine = tegelik aeg ilma müügilepinguta ÷ ressursivõimsus
  - Ressursivõimsus = ressursi töötunnid – kontorist väljasolek – puhkepäevad

Vaate **Ressursikasutus** leiate paanilt **Ressursid**.

Iga ruudustiku lahter esindab perioodis (nt päev, nädal või kuu) oleva ressursi tasustatavat kasutusprotsenti. Lahtrite värvimiseks kasutatakse järgmisi valemeid.

  - **Roheline**: arveldatav kasutus > = ressursi eesmärgiks seatud kasutus
  - **Kollane**: eesmärgiks seatud kasutus – 20 < = arveldatav kasutus < eesmärgiks seatud kasutus
  - **Punane**: arveldatav kasutus < = eesmärgiks seatud kasutus – 20

Kuna vaade **Ressursikasutus** põhineb ajakavapaneelil, saate oma tulemuste filtreerimiseks kasutada ajakavapaneeli filtreerimise võimalusi.

Ruudustik nõuab, et määraksite sihtkasutuse kas rollile või konkreetsele ressursile. Selle seadistamiseks tehke valikud **Ressursid** > **Ressursi rollid**.

Peale selle tuleb igale broneeritavale ressursile määrata vaikeroll. Avage **Ressursid** > **Ressursid**. Kontrollige vahekaardil **Project Service**, et ressursi roll oleks määratletud ja väli **On vaikimisi** oleks määratud väärtusele **Jah**. Saate lisada veel rolle, kus väärtus **On vaikimisi** = **Ei**. Roll, kus väärtust **On vaikimisi** = **Jah**, kasutatakse ressursi kasutuse hindamiseks selle rolli eesmärgi suhtes.

Vahekaardil **Project Service** saate ressursi jaoks määrata ka eraldi sihtkasutuse. Seejärel kasutab kasutuse arvutus seda sihtkasutust, et hinnata ressursi sihti, mitte ressursi vaikerolli sihti.

Ressursi jaoks kuvatakse kasutus ainult juhul, kui selle ressursi ruudustikus kuvatakse perioodi jooksul kinnitatud, arveldatav aeg.


[!INCLUDE[footer-include](../includes/footer-banner.md)]