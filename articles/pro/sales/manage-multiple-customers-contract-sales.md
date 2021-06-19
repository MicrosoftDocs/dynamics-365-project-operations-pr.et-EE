---
title: Mitme kliendi haldamine projekti lepingutes – liht
description: See teema sisaldab teavet projektilepingutes mitme kliendi haldamise kohta.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 31a12e44353160dde851e2b9b06148a31fbeb167
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002830"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Mitme kliendi haldamine projekti lepingutes – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakenduse Dynamics 365 Project Operations projektilepingud toetavad stsenaariumit, kus sõlmitav kokkulepe hõlmab mitut tehingut rahastavat klienti. Vahekaart **Kokkuvõte** lehel **Projektilepingud** sisaldab välja **Klient**. See väli tuvastab tehingu peamise kliendi. Tehingu teised kliendid saab häälestada lehe **Projektileping** vahekaardil **Kliendid**.

Kõikide projektilepingus loetletud lepinguliste klientide vaikevääruseks on lepingurea kliendid kõikidel uutel projektilepingu jaoks loodavate projektipõhistel lepinguridadel. Olemasolevad projektipõhised lepinguread ei päri uute kirjete loomisel uusi lepingulisi kliente.

Tootepõhised lepinguread seostatakse automaatselt peamise kliendiga.

Lepingu kliente ja lepingurea kliente saab enne lepingu võitmist igal ajal lisada, uuendada või kustutada.

## <a name="primary-customer"></a>Peamine klient

Projektilepingu vahekaardil **Kokkuvõte** potentsiaalse kliendina loetletud klient on lepingu peamine klient. Kui te proovite peamist klientid lepingu klientide loendist kustutada, kuvatakse teile tõrketeade, et lepingu peamise kliendi kirjet ei saa kustutada.

Peamist klienti ei saa lepingu klientide loendist värskendada. Selle asemel muutke potentsiaalset klienti lepingu vahekaardil **Kokkuvõte**. Kui seda välja lehel **Lepingu kokkuvõte** uuendatakse, lisatakse uus klient uue lepingulise kliendina, määrates lipu **Peamine**. Eelmine peamine klient jääb endiselt lepingus kliendiks.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Lepingu kliendikirje loomine, värskendamine või kustutamine

Lepingu klienti saab luua, uuendada või kustutada lehe **Projektileping** vahekaardil **Kliendid**. Järgmises tabelis olevad väljad on projektilepingu lepingulise kliendi kirjes ja neid tuleb lepinguga töötades meeles pidada.

| Väli | Asukoht | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- | --- |
| **Ettevõte** | Ruudustikku saab redigeerida lepingulise kliendi vahekaardil **Lepingu kliendid** ning vormidel **Peamine** ja **Kiirloomine**. | Loetleb kõik aktiivsed kontod. Pärast kirje loomist see väli lukustatakse. Konto värskendamiseks kustutage kirje ja looge see uuesti. Kui olete salvestanud mis tahes tegelikud näitajad või kui lepingulise kliendi kirje on peamine klient, te ei saa kirjet kustutada. | Lepingu kliendid kopeeritakse lepingurea loomisel kui lepingurea kliendid. |
| **Arveldamise jagamise protsent** | Ruudustikku saab redigeerida lepingulise kliendi vahekaardil **Lepingu kliendid** ning vormidel **Peamine** ja **Kiirloomine**. | Näitab iga arveldamata müügitehingu protsenti, mis on selle lepingu kliendile omistatud. | Kopeeritakse uutel projekti lepingurdadel uutele lepinguridadele ja projekti lepingurea klientidele. |
| **Maksja: kontakti nimi** | Ruudustikku saab redigeerida lepingulise kliendi vahekaardil **Lepingu kliendid** ning vormidel **Peamine** ja **Kiirloomine**. | Seda tekstivälja tuleks kasutada selle kliendi arve kontaktisiku tuvastamiseks. Selle välja vaikeväärtus pärineb seotud konto kirjest. | Kopeeritakse selle kliendi jaoks genereeritava arve väljale **Maksja: kontakti nimi**. |
| **Maksja nimi** | Ruudustikku saab redigeerida lepingulise kliendi vahekaardil **Lepingu kliendid** ning vormidel **Peamine** ja **Kiirloomine** | Seda tekstivälja tuleks kasutada selle kliendi arve kontaktisiku tuvastamiseks. Selle välja vaikeväärtus pärineb seotud konto kirjest. | Kopeeritakse selle kliendi jaoks genereeritava arve väljale **Maksja: kontakti nimi**. |
| **Maksetingimused** | Ruudustikku saab redigeerida lepingulise kliendi vahekaardil **Lepingu kliendid** ning vormidel **Peamine** ja **Kiirloomine**. | Vaikeväärtused pärinevad seotud konto kirjest. | Kopeeritakse selle kliendi jaoks genereeritava arve väljale **Maksja: kontakti nimi**. |
| **On ümardamine** | Ruudustikku saab redigeerida lepingulise kliendi vahekaardil **Lepingu kliendid** ning vormidel **Peamine** ja **Kiirloomine**. | Näitab, kas see klient on selle tehingu jaoks vaikimisi ümardamise klient. Projektilepingus võib olla ainult üks ümardatav klient. | Kui kulu ja arveldamata müük jaotub koguse põhjal ümardamise erinevuseks, rakendatakse seda erinevust selle kliendi vastenatavatele tegelikele näitajatele. |
| **Mitteületatav limiit** | Ruudustikku saab redigeerida lepingulise kliendi vahekaardil **Lepingu kliendid** ning vormidel **Peamine** ja **Kiirloomine** | Näitab, kas on olemas kogusumma kokkulepitud piir või ülempiir, mis kliendile selle seose eest arveldatakse. | Lepingu kliendi tasemel seadistatud **Mitteületatav limiit** hinnatakse suvandis **Tegelik arveldamata müük**, mis viitab sellele lepingu kliendile. |

## <a name="edit-billing-split-percentages"></a>Arveldamise jagamise protsentide muutmine

Arveldamise jaotumise protsente saab redigeerida kasutades soisemise ruudustiku redigeerimise kasutuskogemust. Kui arveldamise jaotumise protsentide kogusumma ei ole 100 protsenti, kuvatakse teile tõrge. Pärast arveldamise jaotumise protsentide muutmist värskendage leht tõrke eemaldamiseks.

Samuti saate valida andmeruudustikus **Lepingulised kliendid** suvandi **Jaota võrdselt**, et eraldada arveldamise jaotumine võrdselt kõigile lepingu klientidele. Kui esineb ümardamise tegur, lisatakse see ümardamise kliendile. Üks lepingu klientidest on alati märgitud **ümardatava** kliendina, mis tähendab, et lepingu kliendi kirjel on ümardamise lipu väärtuseks määratud **Jah**. Tavaliselt on see lepingu peamine klient, kuid seda saab ka muuta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]