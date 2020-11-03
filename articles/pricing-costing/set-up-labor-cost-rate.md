---
title: Tööjõukulu määrade seadistamine
description: Selles teemas kirjeldatakse tööjõukulu määrade seadistamist Project Operationsis.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d17f266b6e34fc2a2743fe19fd18b15fb992ceef
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074853"
---
# <a name="set-up-labor-cost-rates"></a>Tööjõukulu määrade seadistamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_


Igale hinnakirjale on seadistatud tööjõu määrad (rolli hinnad), mis joonduvad hinnakirja sisu ja kehtiva kuupäevaga.

1. Looge hinnakiri ja valige vahekaardi **Rolli hind** andmeruudustikus **Uus roll**.
2. Valige lehel **Kiirloomine** roll ja organisatsiooniüksus.
3. Sisestage kõik muu nõutav välja teave.

Järgmises tabelis on toodud mõned väljad, mis on olulised omahinnakirjas tööjõumäärade loomiseks.

| Väli | Asukoht | Asjakohasus, eesmärk ja juhised | Allavoolu mõjud |
| --- | --- | --- | --- |
| Roll | Vahekaart **Üldine** ja lehed **Kiirloomine** | Valige roll, millele kulumäär rakendub. | Sissetuleva prognoosi või tegeliku näitaja roll vastendatakse rolli vaikekulu saamiseks selle reaga. |
| Ressursiettevõte | Vahekaart **Üldine** ja lehed **Kiirloomine** | Valige juriidiline olem, millele roll on määratud. Näiteks Fabrikam India arendaja või Fabrikam USA arendaja. | Sissetuleva prognoosi või tegeliku näitaja ressursiettevõte vastendatakse rolli vaikimisi kulumäära saamiseks selle reaga. |
| Ressursi üksus | Vahekaart **Üldine** ja lehed **Kiirloomine** | Valige ettevõtte organisatsiooniüksus või allüksus, kust seda rolli kasutatakse. Näiteks Fabrikam India robootika allüksuse arendaja või Fabrikam USA tarkvara allüksuse arendaja. | Sissetuleva prognoosi või tegeliku näitaja ressursiüksus vastendatakse rolli vaikekulu saamiseks selle reaga. |
| Hind | Vahekaart **Üldine** ja lehed **Kiirloomine** | Seadistage rollile, ressursiettevõttele ja ressursiüksuse kombinatsioonile kulumäär. Näiteks Fabrikam India arendaja kulud 1000 INR või Fabrikam USA kulud 150 USD. | Hind on kulumäär, mille vaikeväärtuseks on sissetuleva prognoosi või tehinguklassi **Aeg** tegeliku rea ühiku kulu. |
| Valuuta | Vahekaart **Üldine** ja lehed **Kiirloomine** | Vaikimisi tuleb valuuta väärtus omahinnakirja päises olevast valuutast, kuid seda saab tühistada. Näiteks Fabrikam India arendaja kulu on 1000 INR-i. Fabrikam USA arendaja kulu on 150 USD. | Selle valuuta vaikeväärtuseks on tehinguklassi **Aeg** sissetuleva tegeliku kulurea ühiku kulu. Projekti prognoosil teisendatakse valuuta väärtus projekti valuutaks ja kuvatakse prognoosi ajafaasi vaates. |
| Üksuse ajakava | Vahekaart **Üldine** ja lehed **Kiirloomine** | Ühiku ajakavaks on vaikimisi Aeg ja seda ei saa rolli hinna olemis muuta, sest seda kasutatakse määrade ajaühikute kaupa väljendamiseks. | Allavoolu mõju puudub. |
| Üksus | Vahekaart **Üldine** ja lehed **Kiirloomine** | Vaikimisi tuleb väärtus omahinnakirja päise väljalt **Ajaüksus**. Selle väärtuse saab tühistada. Näiteks Fabrikam India arendaja kulu on 1000 INR-i **India päeva** kohta. Fabrikam USA arendaja kulu on 150 USD **USA päeva** kohta. | Süsteem kasutab ühikute süsteemi ja teisendamist põhiühikutes, et arvutada ühiku omahinna järgi sissetuleva prognoosi või tegeliku rea ühiku vaikehinna. Näiteks on prognoos 10 **India päeva** võrra tööd India arendajale ja üksus **India päev** on määratletud kui 10 tundi. Selle prognoosi rea kuluarvutuses arvutab rakendus prognoosi ühiku kulu järgmiselt: 1000 INR/10 hours = 100 INR tunnis, mis teisendatakse dollaritesse ja kuvatakse ühiku kuluna lehel **Projekti prognoosid**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Allüksusest või juriidilisest isikust hindade ja kulude väljapoole ülekandmine.

Projektipõhistes ettevõtetes on tavapärane kasutada projektideks erinevate juriidiliste isikute või allüksuste töötajaid. Projekti võib täita üks juriidiline isik, kuid projektiga töötavad töötajad või konsultandid võivad pärineda kas samast juriidilisest isikust või mõnest muust, või võib esineda nende mõlema kombinatsioon. Dynamics 365 Project Operationsis on juriidiline üksus, millele kuulub projekti kättetoimetamine **Omanikust ettevõtte** ja allüksus, millele kuulub täitmine, on **Lepingut sõlmiv üksus**. Muud juriidilised isikud, mis pakuvad ressursse, on **Ressursiettevõtted** ja ressursse pakkuvad allüksused on **Ressursiüksused**. Enamikus riikides on ettevõtted kohustatud tagama, et juriidiline isiku või allüksus võtavad ressursside kasutamise eest omanikust ettevõttelt ja lepingut sõlmivalt üksuselt tasu.

Näiteks peab Fabrikami ettevõte tagama, et Fabrikam India-Robotics on leppinud Fabrikam US-Roboticsi või Fabrikam UK-Roboticsiga kokku kulumäära kaardis.

Fabrikam India-Roboticsi arendaja tasu on 100 USD kui teda laenatakse Fabrikam US-Roboticsile ja 150 USD, kui teda laenatakse Fabrikam U-Roboticsile.

### <a name="set-up-costs-for-outside-resources"></a>Kulude seadistamine välistele ressurssidele

1. Looge omahinnakiri nimega *Fabrikam US-Roboticsi kulumäärad* ja seadistage kehtivuskuupäevade vahemik.
2. Määrake omahinnakirja määrad, kasutades järgmises tabelis toodud teavet. 

| Roll | Ressursiettevõte | Ressursi üksus | Kulumäär |
| --- | --- | --- | --- |
| Arendaja | Fabrikam India | Fabrikam India-Robotics | 100 dollarit |
| Arendaja | Fabrikam Philippines | Fabrikam Philippines-Robotics | 90 USD |
| Arendaja | Fabrikam US | Fabrikam US-Robotics | 150 USD |

3. Lisage see omahinnakiri Fabrikam USA-Roboticsi organisatsiooniüksusele.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Seadistage ressursi ülekandmise hinnad sobivad valuutas 

Project Operationsis saab ressursi hindu seadistada mis tahes valuutas. Valuuta vaikeväärtus on see, mis on hinnakirja päises, kuid seda saab muuta.

Kasutades näite ülekandmise hinna seadistust, võib teavet muuta järgmiselt.

Fabrikami ettevõte peab tagama, et Fabrikam India-Robotics on leppinud Fabrikam US-Roboticsi või Fabrikam UK-Roboticsiga kulumääras kokku.

Fabrikam India-Roboticsi arendaja tasu on 5000 INR-i kui teda laenatakse Fabrikam US-Roboticsile ja 5500 INR-i, kui teda laenatakse Fabrikam UK-Roboticsile.

Fabrikam US-Roboticsi omahinnakirjas saab kulumäärasid väljendada järgmiselt.

| Roll | Ressursiettevõte | Kulu |
| --- | --- | --- |
| Arendaja | Fabrikam India | 5000 INR |
| Arendaja | Fabrikam US | 115 USD |

Fabrikam UK-Roboticsi omahinnakirjas saab kulumäärasid väljendada järgmiselt.

| Roll | Ressursiettevõte | Kulu |
| --- | --- | --- |
| Arendaja | Fabrikam India | 5500 INR |
| Arendaja | Fabrikam UK | 115 GBP |

Omahinnakiri võib pakkuda tööjõukulu määrasid mitmes valuutas. Projekti kuluprognoosi loomisel teisendab Project Operations need kulumäärad projekti valuutasse ja kuvab need kasutajale. Kui ajakirje kinnitatakse ja luuakse tegelik kulu, hinnastatakse tegelik kulu omahinnakirja vastava rolli hinnarea valuutas. Ühe projekti aja tegeliku kulu saab kirjendada mitmes valuutas. Kuid projekti tasandil tegeliku tööjõu kulu ümberarvestamisel või summeerimisel teisendab Project Operations kõik tööjõukulu summad projekti valuutasse, mida kasutaja saab vaadata.