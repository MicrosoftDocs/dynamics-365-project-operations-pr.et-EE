---
title: Projektipõhistel lepinguridadel mitme kliendi haldamine – liht
description: See teema sisaldab teavet projektipõhistel lepinguridadel mitme kliendi haldamise kohta.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 23bb4cebd16bd1e8ae572d3e54538756547ae39e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002997"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Projektipõhistel lepinguridadel mitme kliendi haldamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Projektipõhised lepinguread võivad sisaldada maksmise eest vastutavate klientide loendit. See projektipõhise lepingurea klientide loend võib olla sama, mis lepingu klientide loend, kuid see pole nõutav. Projekti hinnapakkumise võitmisel ja projekti lepingu loomisel kopeeritakse hinnapakkumise rea klientide loend vastavale lepingurea. Hinnapakkumise kliendid kopeeritakse lepingusse.

Projektilepingu eest arve esitamisel on projektipõhise lepingurea klientide loend tähtsam kui lepingu klientide loend. Projektilepingu klientide loendit kasutatakse ainult uute lepinguridade vaikeväärtuste jaoks.

Kõik projektilepingu jaoks loodavate uute lepinguridade projektilepingu vahekaardi **Kliendid** lepinguliste klientide vaikeväärtused pärinevad lepingurea klientidelt. Ükski olemasolevatest lepinguridadest ei päri pärast neid loodud uusi lepingu kliendikirjeid.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Lepingurea kliendikirje loomine, värskendamine või kustutamine

Lepingurea kliendi saab luua, värskendada või kustutada projektipõhise lepingurea lehe lepingurea kliendi vahekaardilt. Kui projektipõhisele lepingureale lisatakse uus klient, lisatakse need lepingu kliendina ka üldisesse lepingusse koos vaikimisi arveldamisega jagatuna nulliks protsendiks. Lepingu üldine arveldamise jaotatud protsent kopeeritakse uutele lepinguridadele ja projekti lõplikule lepingule. Samas lepingu alusel arveldades kasutatakse lepingurea tasemel arveldamise jaottaud protsenti ja mitte lepingu üldisel tasemel arveldamise jaotatud protsenti.

Allpool on projektipõhise lepingurea kliendikirje rea **Leping** väljad, et neid töötades meeles pidada.

| Väli | Asukoht | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- | --- |
| **Ettevõte** | Lepingu kliendi vahekaardi **Lepingu kliendid** ning vormide **Peamine** ja **Kiirloomine** redigeeritav ruudustik. | Kõik aktiivsed kontod. Pärast kirje loomist see väli lukustatakse. Välja värskendamiseks kustutage kirje ja looge uus kirje. Kui olete salvestanud mis tahes tegelikke näitajaid, siis te ei saa kirjet kustutada. Samas saate märkida selle konto arveldamise jaotuse protsendiks null. Kui kirje on märgitud nullina, mõjutab see kõiki tulevasi kulu ja tulu tegelikke näitajaid, mis selle kliendiga on seostatud või jagatud. | Kui valite kontode põhiloendist lisamiseks ja salvestamiseks konto, lisatakse lepingurea klient samuti lepingu kliendina. Lepingurea kliente kasutatakse arvete loomisel. |
| **Arveldamise jagamise protsent** | Lepingu kliendi vahekaardi **Lepingu kliendid** ning vormide **Peamine** ja **Kiirloomine** redigeeritav ruudustik. | See väli näitab iga arveldamata müügitehingu protsenti, mis on selle lepingurea kliendile omistatud. | Lepingurea kliente ja arveldamise jaotamise protsente kasutatakse pärast kinnitamist tegelike näitajate loomisel ja arve genereerimisel. |
| **Mitteületatav limiit** | Lepingu kliendi vahekaardi **Lepingu kliendid** ning vormide **Peamine** ja **Kiirloomine** redigeeritav ruudustik. | Näitab, kas on olemas kogusumma kokkulepitud piir või ülempiir, mis sellele kliendile lepingurea eest arveldatakse. | Lepingurea kliendi mitteületatavat limiiti kasutatakse tegelike näitajate loomisel ja arvete genereerimisel. |
| **On ümardamine** | Lepingurea kliendi vahekaardi **Lepingu kliendid** ning vormide **Peamine** ja **Kiirloomine** redigeeritav ruudustik. | See väli näitab, kas see klient on selle projektipõhise lepingurea jaoks vaikimisi ümardatav klient. | Kui te loote arveldamise jaotamise protsendi põhjal tegeliku näitaja, võib esineda ümardamise erinevusi. Praegusel juhul omistatakse ümardamise erinevused sellele kliendile. |

## <a name="edit-billing-split-percentages"></a>Arveldamise jagamise protsentide muutmine

Arveldamise jaotumise protsente saab redigeerida ruudustikus. Kui arveldamise jaotumise protsentide kogusumma ei ole 100 protsenti, ilmneb tõrge. Pärast arveldamise jaotumise protsentide muutmist värskendage leht tõrke eemaldamiseks.

Võite ka valida lepingurea kliendi andmeruudustikus suvandi **Jaota ühtlaselt**. See toiming omistab arvelduse jaotused ühtlaselt kõikidele lepingurea klientidele. Kui esineb mis tahes ümardamise tegur, lisatakse see ümardamise kliendile. Üks lepingurea klient märdistatakse alati **ümardamise** kliendina koos lipuga **Ümardamine** seatud valikule **Jah**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]