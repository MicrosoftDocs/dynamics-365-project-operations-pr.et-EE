---
title: Projektipõhiste hinnapakkumiste ridadel mitme kliendi haldamine
description: See teema sisaldab teavet, kuidas hallata projektipõhistel hinnapakkumiste ridadel mitut klienti.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea7f0a8207fc78914783f5b9c919b3243a0bb5a4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074832"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Projektipõhiste hinnapakkumiste ridadel mitme kliendi haldamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Projektipõhised hinnapakkumise read toetavad stsenaariumeid, kus igal hinnapakkumise real on selle eest makstavate klientide loend. See projektipõhise hinnapakkumise rea klientide loend võib olla sama, mis hinnapakkumise klientide loend. Saate muuta ka klientide loendit, et see oleks erinev. Projekti hinnapakkumise võitmisel projekti lõpliku lepingu loomiseks kopeeritakse projektipõhise hinnapakkumise rea klientide loend vastavasse projektipõhisele lepingureale. Projektipõhise hinnapakkumise kliendid kopeeritakse projekti lepingusse.

Projekti lõpliku lepingu arveldamisel on projektipõhise lepingurea klientide loendil eelis projekti lepingu loendi ees. Projekti lepingu kliendiloendit kasutatakse ainult uue projekti lepinguridade vaikeväärtuseks.

Kõik hinnapakkumise vahekaardil **Kliendid** olevad hinnapakkumise kliendid on vaikimisi hinnapakkumise rea kliendid mis tahes projekti hinnapakkumise jaoks loodava uue projektipõhise hinnapakkumise ridade puhul. Kõik olemasolevad projektipõhised hinnapakkumise read ei päri pärast neid loodud uusi hinnapakkumise kliendikirjeid.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Hinnapakkumise rea kliendi kirje loomine, värskendamine või kustutamine

Hinnapakkumise rea kliendi saate luua, uuendada või kustutada lehe **Projektipõhine hinnapakkumise rida** vahekaardil **Hinnapakkumise rea kliendid**. Kui lisate projektipõhisele hinnapakkumise reale uue kliendi, lisatakse klient ka üldisessehinnapakkumisse hinnapakkumise kliendina koos üldise hinnapakkumise vaikimisi arveldamise jaotamise protsendiga 0%. Üldise hinnapakkumise arveldamise jaotamise protsent kopeeritakse uue hinnapakkumise ridadele ja lõplikusse projekti lepingusse. Samas kui esitate arve lepingu järgi, kasutatakse hinnapakkumise rea tasemel arveldamise jagamise protsenti, mitte üldise lepingu taseme arveldamise jagamise protsenti. 

Järgmises tabelis on toodud projektipõhise hinnapakkumise rea hinnapakkumise rea kliendikirje väljad.

| Väli | Asukoht | Kirjeldus ja juhis | Allavoolu mõjud |
| --- | --- | --- | --- |
| **Ettevõte** | Vahekaardi **Hinnapakkumise rea kliendid** redigeeritav ruudustik, põhivorm ja hinnapakkumise rea kliendi kiirloomise vorm. | Loetleb kõik aktiivsed kontod. Pärast kirje loomist see väli lukustatakse. Kui peate välja värskendama, kustutage kirje ja looge see uuesti. Kui olete salvestanud kõik tegelikud andmed, ei saa te kirjet kustutada. | Kui valite lisamiseks konto kontode põhiloendist, lisatakse hinnapakkumise rea klient samuti kui hinnapakkumise klient. Hinnapakkumise rea kliendid kopeeritakse hinnapakkumise võitmisel projekti lepingurea klientidele. |
| **Arveldamise jagamise protsent** | Vahekaardi **Hinnapakkumise rea kliendid** redigeeritav ruudustik, põhivorm ja hinnapakkumise rea kliendi kiirloomise vorm. | Esindab iga arveldamata müügitehingu protsenti, mis omistatakse selle hinnapakkumise rea kliendile. | Kopeeritud üle projekti lepingurea klientidele. |
| **Mitteületatav limiit** | Vahekaardi **Hinnapakkumise rea kliendid** redigeeritav ruudustik, põhivorm ja hinnapakkumise rea kliendi kiirloomise vorm. | Näitab, kas sellele kliendile esitatakse selle hinnapakkumise rea eest arve summas, millel on läbiräägitud limiit või ülempiir. | Kopeeritud üle hinnapakkumise võitmisel projekti lepingurea klientidele. |
| **Omanikust ettevõte** | Vahekaardi **Hinnapakkumise rea kliendid** redigeeritav ruudustik, põhivorm ja hinnapakkumise rea kliendi kiirloomise vorm. | Juriidiline olem, kus klient seadistatakse moodulis **Projektihaldus ja raamatupidamine**. See väli on kirjutuskaitstud ja määratud hinnapakkumise enda omanikust firmale. Väljale **Konto** lisatavate klientide loend on juba rakenduse Project Operations moodulis **Projektihaldus ja raamatupidamine** omanikust ettevõtte loendist filtreeritud. | Omanikust ettevõte võrdsustub juriidilise olemi kontseptsiooniga. Kõik sellest projektist tulenevad kulud ja tulud arvestatakse omanikust ettevõtte pearaamatus. |
| **Ümardab** | Vahekaardi **Hinnapakkumise rea kliendid** redigeeritav ruudustik, põhivorm ja hinnapakkumise rea kliendi kiirloomise vorm. | Näitab, kas see klient on selle projektipõhise hinnapakkumise rea vaikimisi ümardav klient. | Kopeeritud üle hinnapakkumise võitmisel projekti lepingu klientidele. |

## <a name="edit-billing-split-percentages"></a>Arveldamise jagamise protsentide muutmine

Saate arvedamise jaotamise protsente muuta rea sees. Kui arvelduse jagamise protsentide summa ei ole kokku 100%, esineb tõrge. Pärast arveldamise jagamise protsentide muutmist värskendage hinnapakkumise rea lehte, et viga eemaldada.

Kasutage hinnapakkumise rea alamruudustikus ühtlaselt jaotamise toimingut, et jaotada arvelduse jaotused kõigile hinnapakkumise rea klientidele. Kui esineb ümardamise tegur, lisatakse see ümardamise kliendile. Üks hinnapakkumise rea kliente on alati märgitud ümardava kliendina, mis tähendab, et hinnapakkumise rea kliendi kirjel on ümardamise lipu väärtuseks määratud **Jah**. 
