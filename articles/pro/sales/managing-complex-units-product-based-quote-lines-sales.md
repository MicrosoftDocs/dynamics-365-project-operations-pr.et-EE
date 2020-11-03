---
title: Tootepõhiste hinnapakkumise ridade kompleksühikute haldus, näiteks kasutaja kohta või kuu kohta
description: Selles teemas antakse teavet tootepõhiste hinnapakkumise ridade kompleksühikute halduse kohta.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074888"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a>Tootepõhiste hinnapakkumise ridade kompleksühikute haldus, näiteks kasutaja kohta või kuu kohta

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Dynamics 365 Project Operations kasutab kordustellimuse põhiste toodete müügi toetamiseks koguse tegureid. Kordustellimusel põhinevate toodete puhul väljendatakse hinnapakkumise või projekti lepingurea kogust kasutaja kuude arvuna.

Tavaliselt talletatakse kordustellimuse tarkvara hinda kataloogis ühe kasutaja kuu hinnana. Müügiprotsessi jooksul on hind hinnapakkumise real tavaliselt ühe kasutaja hind kuus, mille IT müügiagent oli kokku leppinud ja diskonteerinud. Igal lepingul on erinev arv kasutajaid ja kordustellimuse kuude arv on erinev. Kogus, mida kasutatakse hinnapakkumise rea arvutamiseks, on kasutajate arvu ja kordustellimuse kuude arvu korrutis.

Seda tüüpi müügi toetamiseks võttis Project Operations kasutusele koguse tegurite kontseptsiooni. Koguselised tegurid sõltuvad toote atribuutidest rakenduses Dynamics 365. Toote teatud atribuutide konfigureerimisel võimaldab Project Operations teil tähistada nende atribuutide alamhulka või kõiki atribuute koguse teguritena.

Project Operations valideerib, et ainult arvandmed või toote atribuudid, millel on arvuline andmetüüp, märgistatakse koguse tegurina. Kui lisate hinnapakkumise reale koguse teguritega toote, muutub väli **Kogus** kirjutuskaitstuks. Pärast koguse teguritest toote atribuutidele väärtuste sisestamist arvutab Project Operations hinnapakkumise rea koguse.

Näiteks Dynamics 365 Sales võib omada järgmisi atribuute.

- **Kasutajate arv** : kasutajate arv
- **Kuude arv** : kordustellimuse kuude arv
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
