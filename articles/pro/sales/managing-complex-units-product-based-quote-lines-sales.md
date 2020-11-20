---
title: Keeruliste ühikute, nt ühe kasutaja või kuu kohta, haldamine tootelpõhise hinnapakkumise ridadel – liht
description: Selles teemas antakse teavet tootepõhiste hinnapakkumise ridade kompleksühikute halduse kohta.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ee46da2f663ef4f5f8fc7f9f89b6fcfd09a1798
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175571"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Keeruliste ühikute, nt ühe kasutaja või kuu kohta, haldamine tootelpõhise hinnapakkumise ridadel – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Dynamics 365 Project Operations kasutab kordustellimuse põhiste toodete müügi toetamiseks koguse tegureid. Kordustellimusel põhinevate toodete puhul väljendatakse hinnapakkumise või projekti lepingurea kogust kasutaja kuude arvuna.

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
