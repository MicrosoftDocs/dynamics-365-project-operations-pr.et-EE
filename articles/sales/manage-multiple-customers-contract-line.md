---
title: Mitme kliendi projektipõhistel lepinguridadel haldamine
description: See teema sisaldab teavet mitut klienti sisaldavate lepinguridade ja lepingutega töötamise kohta.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1efa9e5b5ad432e1564fb3d8db0405134a4dc73
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584913"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a>Mitme kliendi projektipõhistel lepinguridadel haldamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Projektipõhised lepinguread võivad sisaldada maksmise eest vastutavate klientide loendit. See projektipõhise lepingurea klientide loend võib olla sama, mis lepingu klientide loend, kuid see pole nõutav. Projekti hinnapakkumise võitmisel ja projekti lepingu loomisel kopeeritakse hinnapakkumise rea klientide loend vastavale lepingurea. Hinnapakkumise kliendid kopeeritakse lepingusse.

Projektilepingu eest arve esitamisel on projektipõhise lepingurea klientide loend tähtsam kui lepingu klientide loend. Projektilepingu klientide loendit kasutatakse ainult uute lepinguridade vaikeväärtuste jaoks.

Kõik projektilepingu jaoks loodavate uute lepinguridade projektilepingu vahekaardi **Kliendid** lepinguliste klientide vaikeväärtused pärinevad lepingurea klientidelt. Ükski olemasolevatest lepinguridadest ei päri pärast neid loodud uusi lepingu kliendikirjeid.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Lepingurea kliendikirje loomine, värskendamine või kustutamine

Lepingurea kliendi saab luua, värskendada või kustutada **projektipõhise lepingurea** lehe **lepingurea kliendi** vahekaardilt. Kui projektipõhisele lepingureale lisatakse uus klient, lisatakse need lepingu kliendina ka üldisesse lepingusse koos vaikimisi arveldamisega jagatuna nulliks protsendiks. Lepingu üldine arveldamise jaotatud protsent kopeeritakse uutele lepinguridadele ja projekti lõplikule lepingule. Samas lepingu alusel arveldades kasutatakse lepingurea tasemel arveldamise jaottaud protsenti ja mitte lepingu üldisel tasemel arveldamise jaotatud protsenti. 

Allpool on projektipõhise lepingurea projektirea kliendi kirje väljad, et neid töötades meeles pidada.

| Väli | Asukoht | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- | --- |
| Ettevõte | Lepingurea kliendi vahekaardi **Lepingurea kliendid** ning vormide Peamine ja Kiirloomine redigeeritav ruudustik | Kõik aktiivsed kontod. Pärast kirje loomist see väli lukustatakse. Välja värskendamiseks kustutage kirje ja looge uus kirje. Kui olete salvestanud mis tahes tegelikke näitajaid, siis te ei saa kirjet kustutada. Samas saate märkida selle konto arveldamise jaotuse protsendiks null. Kui kirje on märgitud nullina, mõjutab see kõiki tulevasi kulu ja tulu tegelikke näitajaid, mis selle kliendiga on seostatud või jagatud. | Kui valite kontode põhiloendist lisamiseks ja salvestamiseks konto, lisatakse lepingurea klient samuti lepingu kliendina. Lepingurea kliente kasutatakse arvete loomisel. |
| Arveldamise jagamise protsent | Lepingurea kliendi vahekaardi **Lepingurea kliendid** ning vormide Peamine ja Kiirloomine redigeeritav ruudustik | See väli näitab iga arveldamata müügitehingu protsenti, mis on selle lepingurea kliendile omistatud. | Lepingurea kliente ja arveldamise jaotamise protsente kasutatakse pärast kinnitamist tegelike näitajate loomisel ja arve genereerimisel. |
| Mitteületatav limiit | Lepingurea kliendi vahekaardi **Lepingurea kliendid** ning vormide Peamine ja Kiirloomine redigeeritav ruudustik | Näitab, kas on olemas kogusumma kokkulepitud piir või ülempiir, mis sellele kliendile lepingurea eest arveldatakse. | Lepingurea kliendi mitteületatavat limiiti kasutatakse tegelike näitajate loomisel ja arvete genereerimisel. |
| Omanikust ettevõte | Hinnapakkumise rea kliendi vahekaardi **Hinnapakkumise rea kliendid** ning vormide Peamine ja Kiirloomine redigeeritav ruudustik | Juriidiline olem, kus see klient on häälestatud. See väli on kirjutuskaitstud ja see on määratud hinnapakkumise omanikust ettevõttele. Väljale **Konto** lisatavate klientide loend on juba fikltreeritud selle omanikust ettevõtte loendile. | Omanikust ettevõtte mõiste võrdub juriidilise isiku mõistega. Kõik sellest projektist tulenevad kulud ja tulud loetletakse omanikust ettevõtte pearaamatus. |
| On ümardamine | Lepingurea kliendi vahekaardi **Lepingurea kliendid** ning vormide Peamine ja Kiirloomine redigeeritav ruudustik | See väli näitab, kas see klient on selle projektipõhise lepingurea jaoks vaikimisi ümardatav klient. | Kui te loote arveldamise jaotamise protsendi põhjal tegeliku näitaja, võib esineda ümardamise erinevusi. Praegusel juhul omistatakse ümardamise erinevused sellele kliendile. |

## <a name="edit-billing-split-percentages"></a>Arveldamise jagamise protsentide muutmine

Arveldamise jaotumise protsente saab redigeerida ruudustikus. Kui arveldamise jaotumise protsentide kogusumma ei ole 100 protsenti, ilmneb tõrge. Pärast arveldamise jaotumise protsentide muutmist värskendage leht tõrke eemaldamiseks.

Võite ka proovida valida lepingurea kliendi andmeruudustikus suvandi **Jaota ühtlaselt**. See toiming omistab arvelduse jaotused ühtlaselt kõikidele lepingurea klientidele. Kui esineb mis tahes ümardamise tegur, lisatakse see ümardamise kliendile. Üks lepingurea klient märdistatakse alati **ümardamise** kliendina koos lipuga **Ümardamine** seatud valikule **Jah**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]