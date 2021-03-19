---
title: Kompleksühikute haldamine tootepõhiste lepinguridade jaoks – liht
description: Selles teemas antakse teavet kordustellimusel põhinevate toodete müügi toetamise kohta.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273328"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Kompleksühikute haldamine tootepõhiste lepinguridade jaoks – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Dynamics 365 Project Operations kasutab kordustellimuse põhiste toodete müügi toetamiseks koguselisi tegureid. Kordustellimusel põhinevate toodete puhul väljendatakse lepingu või projekti lepingurea kogust kasutaja kuude arvuna.

Kordustellimuse tarkvara hind talletatakse kataloogis ühe kasutaja kuu hinnana. Müügiprotsessi jooksul on hind lepingureal tavaliselt ühe kasutaja hind kuus, mille müügiagent oli kokku leppinud ja diskonteerinud. Igal lepingul on erinev arv kasutajaid ja kordustellimuse kuude arv on erinev. Kogus, mida kasutatakse lepingurea summa arvutamiseks, on kasutajate arvu ja kordustellimuse kuude arvu toode.

Seda tüüpi müügi toetamiseks toetab rakendus Project Operations *koguseliste tegurite* kontseptsiooni. Koguselised tegurid sõltuvad toote atribuutidest. Toote teatud atribuutide konfigureerimisel saate tähistada nende atribuutide alamhulka või kõiki atribuute, näiteks koguselised tegurid.

Project Operations valideerib, et ainult arvandmed või toote atribuudid, millel on arvuline andmetüüp, märgistatakse koguse tegurina. Kui mõne konfigureeritud koguse teguriga toode lisatakse lepingureale, muutub väli **Kogus** kirjutuskaitstuks. Pärast koguseid sisaldavatele toote atribuutidele väärtuste sisestamist arvutab Project Operations lepingurea koguse.

Näiteks Dynamics 365 Sales võib omada järgmisi atribuute.

- **Kasutajate arv**: kasutajate arv.
- **Kuude arv**: kordustellimuse kuude arv.
- **Toote SKU**: toote varude arvestusühikute (SKU).

Atribuute **Kasutajate arv** ja **Kuude arv** saab märgistada koguse tegurina, redigeerides tootesarja atribuute.

Tooteatribuutidest koguseliste tegurite loomiseks tehke järgmist.

1. Valige rakenduses **Project Operations** suvand **Müük – toode**.
2. Avage toode, mille jaoks peate koguselised tegurid seadistama. Veenduge, et toote atribuudid oleks juba häälestatud.
3. Valige lehel **Projekti teave** vahekaart **Koguselised tegurid**.
4. Valige alamruudustikus suvand **+ uue välja arvutus**.
5. Sisestage **koguse teguri** nimi ja valige atribuudi väärtus, mis vastendatakse välja arvutusega.
6. Salvestage ja sulgege vorm.
7. Korrake samme 2–6 kõigi atribuutide jaoks, mis koos moodustavad tootepõhise lepingurea koguse.

Kui koguselised tegurid on häälestatud ja kasutaja loob selle toote jaoks lepingurea, siis lepingurea kogus on lukus. Kogus arvutatakse seejärel selle lepingurea atribuudi väärtuste tootena.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]