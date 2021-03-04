---
title: Föderaalse rahastamise kulude ajakava päring
description: Selles teemas antakse teavet föderaalse rahastamise päringu kulude ajakava kohta.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074940"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Föderaalse rahastamise kulude ajakava päring

[!include [banner](../includes/banner.md)]

Vastavalt Office of Management and Budgeti ringkirjale A-133, kohaldatakse föderaalseid rahalisi vahendeid saanud agentuuridele auditeerimise nõudeid, mida nimetatakse ka ühekordseteks audititeks. Auditeerimise protsessi abil antakse regulaarselt ülevaade föderaalsete toetuste tuludest ja kuludest. Ühekordse auditi aruande osa sisaldab föderaalse rahastamise kulude ajakava (SEFA).

Föderaalse rahastamise kulude ajakava päring sisaldab Föderaalse riigiabi kataloogi (CFDA) pealkirja ja numbrit, toetuse numbrit, toetuse aastat, vahendeid pakkuva föderaalagentuuri nime ja vaheüksuse nime. Päring on määratud perioodi kohta. Tavaliselt on see periood sama, kui finantsaruande periood, milleks on finantsaasta.

Päring hõlmab toetusi, mille kavandatavad kuupäevad on valitud kuupäevavahemikus. Päringu veerg **Väljastav agentuur** näitab toetuse klienti või vahendatava toetuse korral väljastavat agentuuri. Vahendatava toetuse puhul kuvatakse veerus **Vahendav agentuur** toetuse klienti. Kui toetus ei ole vahendatav toetus, on veerg **Vahendav agentuur** tühi.

## <a name="set-up-the-cfda-clusters"></a>CFDA klastrite seadistus

Peate föderaalse rahastamise kulude ajakava päringus seadistama CFDA klastrid, mida saab seostada CFDA numbritega.

1. Minge jaotisse **Projektijuhtimine ja raamatupidamine \> Seadistamine \> Toetused \> Föderaalse riigiabi kataloogi klastrid**.
2. CFDA klastri loomiseks valige **Uus**.
3. Sisestage klastri nimi.
4. Muudatuste salvestamiseks valige nupp **Salvesta**.

## <a name="set-up-cfda-numbers"></a>CFDA numbrite seadistamine

Peate föderaalse rahastamise kulude ajakava päringus seadistama CFDA numbrid, mida saab toetustele lisada.

1. Minge jaotisse **Projektijuhtimine ja raamatupidamine \> Seadistamine \> Toetused \> Föderaalse riigiabi kataloogi numbrid**.
2. CFDA numbri loomiseks valige **Uus**.
3. Sisestage CFDA number veergu **Number**.
4. Vajutage tabeldusklahvi **Tab**.
5. Sisestage CFDA pealkiri veergu **Kirjeldus**.
6. Vajutage tabeldusklahvi **Tab**.
7. Valikuline: sisestage sobiv CFDA klaster väljale **Programmi klaster**.
8. Muudatuste salvestamiseks valige nupp **Salvesta**.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Föderaalse rahastamise kulude ajakava päringule aruandluseks toetuste seadistamine

1. Minge jaotisse **Projektijuhtimine ja raamatupidamine \> Toetused \> Toetused** ning valige olemasolev toetus.
2. Määrake kiirvahekaardil **Seadistamine** väljal **Föderaalse riigiabi kataloog** CFDA-le number. Toetuse CFDA number määratleb aruandluse jaoks CFDA klastri.
3. Sisestage kiirvahekaardile **Kontaktteave** väljastaja andmed, toimides järgmiselt.

    1. Sisestage väljale **Toetuse klient** toetuse eest vastutav klient. Olemasoleva toetuse puhul võib see teave olla juba sisestatud.
    2. Määrake, kas toetuse klient on rahastaja. Kui toetuse klient on rahastaja, jätke märkeruut **Vahendaja** tühjaks. Kui mõni teine klient on rahastaja ja toetuse klient vastutab raha kulutamise ja jälgimise eest, valige märkeruut **Vahendaja**.

4. Kui valisite eelmises etapis märkeruudu **Vahendaja** sisestage väljale **Väljastav agentuur** toetuse andnud klient. Väljastav agentuur ja toetuse klient ei saa olla sama klient.

Siin on näide vahendatava toetuse kohta.

Föderaalvalitsus rahastas riigi jaoks infrastruktuuri projekti. Föderaalvalitsus andis raha riigile kulutamiseks. Sellel juhul on föderaalvalitsus väljastavaks agentuuriks ja riik on toetuse klient.

> [!NOTE] 
> Funktsiooni esmakordsel sisselülitamisel sisestatakse esialgsed CFDA numbrid, kasutades toetustel olemasolevaid numbreid.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>SEFA aruandlusest toetuste välja jätmine vastavalt toetuse tüübile

1. Minge jaotisse **Projektijuhtimine ja raamatupidamine \> Seadistamine \> Toetused \> Toetuste tüübid**.
2. Valige kiirvahekaardil **Vaiketeave** märkeruut **Jäta föderaalse rahastamise kulude ajakavast välja**.
3. Muudatuste salvestamiseks valige nupp **Salvesta**.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Föderaalse rahastamise kulude ajakava päringu käivitamine

1. Minge jaotisse **Projektijuhtimine ja raamatupidamine \> Päringud ja aruanded \> Toetuse päring \> Föderaalsete rahastamise kulude ajakava**.
2. Järgige jaotises **Parameetrid** järgmisi etappe.

    1. Valige väljal **Kuupäevaintervall** kuupäevaintervalli kood. Teise võimalusena määratlege kuupäevaintervall väljadel **Alguskuupäev** ja **Lõpukuupäev**.
    2. Valikuline: kui soovite päringusse tuluna kaasata ainult arveldatud tehinguid, määrake suvand **Kaasa ainult arveldatud tulud** olekusse **Jah**.

## <a name="columns"></a>Tulbad

Föderaalse rahastamise kulude ajakava päring sisaldab järgmisi veerge.

- Föderaalse riigiabi kataloogi klastri nimi
- Väljastav agentuur
- Vahendav agentuur
- Toetuse nimi
- Toetuse ID
- Toetuse taotluse ID
- Föderaalse riigiabi kataloogi
- Kviitungid
- Kulutused


[!INCLUDE[footer-include](../includes/footer-banner.md)]