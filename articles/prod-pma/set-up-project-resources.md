---
title: Projekti ressursside seadistamine
description: Selles teemas antakse teavet projekti ressursside seadistamise või taotlemise kohta.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c8e4373da50999a0cc57f4eab672a98e7cf21edcfa5a5589d87691603a777de
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995711"
---
# <a name="set-up-project-resources"></a>Projekti ressursside seadistamine

[!include [banner](../includes/banner.md)]

Peate seadistama kalendri ja seostama selle töövõtja või töötajaga. Kalendrit kasutatakse projekti kavandamiseks ja projekti jaoks reserveeritavate ressursside tööaegade jaoks. Kalendri seadistamisel saavad projektijuhid ressursi optimeerimise raames teha ressursi tasandamist. Kalendri ajakava põhjal saab ressurssidele lisada piiranguid. Kalendri saate seadistada lehel **Kalendrid**.

Kui te seadistate projekti ressursina töötaja, saate valida töötajate seast, kes töötavad ettevõttes, kelle jaoks ressurssi seadistate. Teise võimalusena saate valida töötajad teistest ettevõtetest oma organisatsioonis. Neid töötajaid nimetatakse kontsernisisesteks ressurssideks.

Järgmised protseduurid selgitavad, kuidas seadistada töötajat oma ettevõttes projekti ressursina ja kuidas seadistada kontsernisisene projekti ressurss.

## <a name="set-up-a-worker-as-a-project-resource"></a>Töötaja seadistamine projekti ressursina

1. Lehel **Töötajad** loendis **Töötajad** valige töötaja, kelle projekti ressursina lisate, ja avage töötaja kirje.
2. Paanil Toiming valige **Projekt** &gt; **Seadistamine** &gt; **Projekti seadistamine**.
3. Valige kalender ja sulgege seejärel leht.

Saate määrata ka ressursi jaoks eelmääramise tüübina vaikeprojektid. Eelmääramisi saab kasutada juhul, kui ressursihaldur või projektijuht teab ette, milliste projektidega ressurss hakkab tööle. Eelmääramised võivad põhineda ka projekti sponsori või kliendi taotlusel. Projekti eelmääramiseks lehel **Projektide määramine** vahekaardil **Projektid** loendis **Ülejäänud projektid** valige vastav projekt.

## <a name="set-up-an-intercompany-resource"></a>Kontsernisisese ressursi seadistamine

Kui seadistate töötaja kontsernisisese ressursina, peate seadistamise lõpetama nii laenu andvale ettevõttele kui ka laenavale ettevõttele.

### <a name="in-the-lending-company"></a>Laenu andvas ettevõttes

1. Rakenduses Finance kontrollige, kas laenu andev ettevõte on valitud, ja täitke seejärel toiming eelmises jaotises „Töötaja projekti ressursina häälestamine”.
2. Valige lehel **Kontsernisisene raamatupidamine** suvand **Uus**.
3. Valige väljal **Juriidilise üksuse ID** laenu andev ettevõte. Täitke ülejäänud väljad vajaduse järgi ja valige käsk **Salvesta**.
4. Valige lehel **Ülekandehind** suvand **Uus**.
5. Valige väljal **Laenu võttev juriidiline olem** vastav ettevõte.
6. Laenavale ettevõttele ainult selle jaotise alguses loodud ressursi laenamiseks valige väljal **Ressurss** loodud ressursi nimi. Laenavas ettevõttes laenavala ettevõttele kõikide ressursside kättesaadavaks tegemiseks jätke väli **Ressurss** tühjaks.
7. Lehel **Projektihalduse ja raamatupidamise parameetrid** vahekaardil **Kontsernisisesed** määrake suvand **Luba kontsernisisesed ressursiplaneerimine ja ajatabelid** valikule **Jah**.

### <a name="in-the-borrowing-company"></a>Laenu võtvas ettevõttes

- Sisestage lehel **Ressursside loend** otsingufiltrisse ressursi nimi, mille laenava ettevõtte jaoks lõite, et kontrollida, kas nimi sisaldub laenu võtva ettevõtte ressursside loendis.

## <a name="request-project-resources"></a>Projekti ressursside taotlemine
Projekti ressursi ajastamise funktsioon võimaldab ressursihalduritel levitada töötajate ressursse kaasamistele või projektidele. Selle funktsiooni lubamiseks täitke järgmised tööülesanded või veenduge, et need oleks täidetud.

- Seadistage numriseeriad.
- Seadistage projektihalduse ja raamatupidamise töövood.
- Lubage ressursitaotluste töövood.

Pärast eelnevate toimingute lõpuleviimist saate vastavalt vajadusele täita järgmisi ülesandeid.

- Looge ressursi taotlus esialgselt broneeritud personali ressursilt.
- Jälgige ressursitaotlusi.
- Täitke ressursitaotlusi.
- Taotlege personali ressurssi WBS-ilt.
- Broneerige ressursid projektile ilma personaliga ressursi taotlust.


[!INCLUDE[footer-include](../includes/footer-banner.md)]