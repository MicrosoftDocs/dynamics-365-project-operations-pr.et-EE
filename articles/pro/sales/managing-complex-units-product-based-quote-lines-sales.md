---
title: Keeruliste ühikute, nt ühe kasutaja või kuu kohta, haldamine tootelpõhise hinnapakkumise ridadel – liht
description: Selles artiklis antakse teavet tootepõhiste hinnapakkumisridade keerukate ühikute haldamise kohta.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 88173468cd2e898331c4aa0a398792d9a0f3df10
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929899"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Keeruliste ühikute, nt ühe kasutaja või kuu kohta, haldamine tootelpõhise hinnapakkumise ridadel – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Dynamics 365 Project Operations kasutab kordustellimuse põhiste toodete müügi toetamiseks koguselisi tegureid. Kordustellimusel põhinevate toodete puhul väljendatakse hinnapakkumise või projekti lepingurea kogust kasutaja kuude arvuna.

Tavaliselt talletatakse kordustellimuse tarkvara hinda kataloogis ühe kasutaja kuu hinnana. Müügiprotsessi jooksul on hind hinnapakkumise real tavaliselt ühe kasutaja hind kuus, mille IT müügiagent oli kokku leppinud ja diskonteerinud. Igal lepingul on erinev arv kasutajaid ja kordustellimuse kuude arv on erinev. Kogus, mida kasutatakse hinnapakkumise rea arvutamiseks, on kasutajate arvu ja kordustellimuse kuude arvu korrutis.

Seda tüüpi müügi toetamiseks võttis Project Operations kasutusele koguse tegurite kontseptsiooni. Koguselised tegurid sõltuvad toote atribuutidest rakenduses Dynamics 365. Toote teatud atribuutide konfigureerimisel võimaldab Project Operations teil tähistada nende atribuutide alamhulka või kõiki atribuute koguse teguritena.

Project Operations valideerib, et ainult arvandmed või toote atribuudid, millel on arvuline andmetüüp, märgistatakse koguse tegurina. Kui lisate hinnapakkumise reale koguse teguritega toote, muutub väli **Kogus** kirjutuskaitstuks. Pärast koguse teguritest toote atribuutidele väärtuste sisestamist arvutab Project Operations hinnapakkumise rea koguse.

Näiteks Dynamics 365 Sales võib omada järgmisi atribuute.

- **Kasutajate arv**: kasutajate arv
- **Kuude arv**: kordustellimuse kuude arv
- **Toote SKU**

Atribuute **Kasutajate arv** ja **Kuude arv** saate märgistada koguse tegurina, redigeerides tootesarja atribuute.

Toote atribuutidest koguse tegurite loomiseks toimige järgmiselt.

1. Minge Project Operationsi vasakpoolsel navigeerimispaanil jaotisse **Müük** > **Tooted**.
2. Avage toode, mille jaoks peate määrama koguse tegurid. Veenduge, et toote atribuudid on juba konfigureeritud.
3. Valige toote lehel **Projekti teave** vahekaart **Koguse tegurid**.
4. Valige alamruudustikus suvand **+ uue välja arvutus**.
5. Sisestage koguse teguri nimi ja valige atribuudi väärtus, mis vastendatakse välja arvutusega.
6. Salvestage ja sulgege vorm. Korrake neid juhiseid kõigi atribuutide jaoks, mida kasutatakse tootepõhise hinnapakkumise rea koguse arvutamiseks.

Tootepõhise hinnapakkumise rea loomisel on lukustatakse hinnapakkumise rea kogus. Kogus arvutatakse selle hinnapakkumise rea jaoks sisestatud atribuudi väärtuste korrutisena.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]