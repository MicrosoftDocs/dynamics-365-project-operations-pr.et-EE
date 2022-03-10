---
title: Mitme kliendi haldamine projektipõhise hinnapakkumise ridadel – liht
description: Selles teemas kirjeldatakse, kuidas hallata projektipõhistel hinnapakkumiste ridadel mitut klienti.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d015e9107741fd496f7d3639731f33fcdcc9b9bdd5f501c9ad2617e37a707f35
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001696"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines---lite"></a>Mitme kliendi haldamine projektipõhise hinnapakkumise ridadel – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Projektipõhised hinnapakkumise read toetavad stsenaariumeid, kus igal hinnapakkumise real on selle eest makstavate klientide loend. See projektipõhise hinnapakkumise rea klientide loend võib olla sama, mis hinnapakkumise klientide loend. Saate muuta ka klientide loendit, et see oleks erinev. Kui projekti hinnapakkumine võidetakse, kopeeritakse projektipõhise hinnapakkumise rea klientide loend vastavale projektipõhisele lepingureale projekti lõpliku lepingu loomiseks. Projektipõhise hinnapakkumise kliendid kopeeritakse projekti lepingusse.

Projekti lõpliku lepingu arveldamisel on projektipõhise lepingurea klientide loendil eelis projekti lepingu loendi ees. Projekti lepingu kliendiloendit kasutatakse ainult uue projekti lepinguridade vaikeväärtuseks.

Kõik hinnapakkumise vahekaardil **Kliendid** olevad hinnapakkumise kliendid on vaikimisi hinnapakkumise rea kliendid mis tahes projekti hinnapakkumise jaoks loodava uue projektipõhise hinnapakkumise ridade puhul. Kõik olemasolevad projektipõhised hinnapakkumise read ei päri pärast neid loodud uusi hinnapakkumise kliendikirjeid.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Hinnapakkumise rea kliendi kirje loomine, värskendamine või kustutamine

Hinnapakkumise rea kliendi saate luua, uuendada või kustutada lehe **Projektipõhine hinnapakkumise rida** vahekaardil **Hinnapakkumise rea kliendid**. Kui lisate projektipõhisele hinnapakkumise reale uue kliendi, lisatakse klient ka üldisessehinnapakkumisse hinnapakkumise kliendina koos üldise hinnapakkumise vaikimisi arveldamise jaotamise protsendiga 0%. Üldise hinnapakkumise arveldamise jaotamise protsent kopeeritakse uue hinnapakkumise ridadele ja lõplikusse projekti lepingusse. Samas lepingu järgi arveldades kasutatakse hinnapakkumise rea tasemel arveldamise jagamise protsenti, mitte üldise lepingu taseme arveldamise jagamise protsenti. 

Järgmises tabelis on toodud projektipõhise hinnapakkumise rea hinnapakkumise rea kliendikirje väljad.

| Väli | Asukoht | Kirjeldus ja juhis | Allavoolu mõjud |
| --- | --- | --- | --- |
| **Ettevõte** | Vahekaardi **Hinnapakkumise rea kliendid** redigeeritav ruudustik, põhivorm ja hinnapakkumise rea kliendi kiirloomise vormid. | Loetleb kõik aktiivsed kontod. Pärast kirje loomist see väli lukustatakse. Kui peate välja värskendama, kustutage kirje ja looge see uuesti. Kui olete salvestanud kõik tegelikud andmed, ei saa te kirjet kustutada. | Kui valite lisamiseks konto kontode põhiloendist, lisatakse hinnapakkumise rea klient selle salvestamisel samuti kui hinnapakkumise klient. Hinnapakkumise võitmisel kopeeritakse hinnapakkumise rea kliendid projekti lepingurea klientidele. |
| **Arveldamise jagamise protsent** | Vahekaardi **Hinnapakkumise rea kliendid** redigeeritav ruudustik, põhivorm ja hinnapakkumise rea kliendi kiirloomise vormid. | Esindab iga arveldamata müügitehingu protsenti, mis omistatakse selle hinnapakkumise rea kliendile. | Kopeeritud üle projekti lepingurea klientidele. |
| **Mitteületatav limiit** | Vahekaardi **Hinnapakkumise rea kliendid** redigeeritav ruudustik, põhivorm ja hinnapakkumise rea kliendi kiirloomise vormid. | Näitab, kas sellele kliendile esitatakse selle hinnapakkumise rea eest arve summas, millel on läbiräägitud limiit või ülempiir. | Kopeeritud üle hinnapakkumise võitmisel projekti lepingurea klientidele. |
| **Ümardab** | Vahekaardi **Hinnapakkumise rea kliendid** redigeeritav ruudustik, põhivorm ja hinnapakkumise rea kliendi kiirloomise vormid. | Näitab, kas see klient on selle projektipõhise hinnapakkumise rea vaikimisi ümardav klient. | Kopeeritud üle hinnapakkumise võitmisel projekti lepingu klientidele. |

## <a name="edit-billing-split-percentages"></a>Arveldamise jagamise protsentide muutmine

Saate arvedamise jaotamise protsente muuta rea sees. Kui arvelduse jagamise protsentide summa ei ole kokku 100%, esineb tõrge. Pärast arveldamise jagamise protsentide muutmist värskendage hinnapakkumise rea lehte, et viga eemaldada.

Kasutage hinnapakkumise rea alamruudustikus ühtlaselt jaotamise toimingut, et jaotada arvelduse jaotused kõigile hinnapakkumise rea klientidele. Kui esineb ümardamise tegur, lisatakse see ümardamise kliendile. Üks hinnapakkumise rea kliente on alati märgitud ümardava kliendina, mis tähendab, et hinnapakkumise rea kliendi kirjel on ümardamise lipu väärtuseks määratud **Jah**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]