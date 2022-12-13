---
title: Mitme kliendi haldamine projektipõhistes lepingutes
description: Sellest artiklist leiate teavet selle kohta, kuidas hallata mitut klienti projektipõhise lepingu alusel.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1aae178830d7b671c33295ca6d2910ee4be2f8dd
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825373"
---
# <a name="manage-multiple-customers-on-project-based-contracts"></a>Mitme kliendi haldamine projektipõhistes lepingutes

See artikkel annab teavet selle kohta, kuidas hallata projektilepingu puhul mitut klienti. Saate kasutada projektilepingut, kui tehingu rahastamiseks on vaja mitme kliendi lepingulist kokkulepet. Lehel **Projektipeling** sisaldab vahekaart **Kokkuvõte** teavet tehingu peamise kliendi kohta. Teised tehingus osalevad kliendid saab lisada vahekaardile **Kliendid**.

Kõik projektilepingu jaoks loodavate uute projektipõhiste lepinguridade projektilepingu vahekaardi **Kliendid** lepinguliste klientide vaikeväärtused pärinevad lepingurea klientidelt. Kõik olemasolevad projektipõhised lepinguread ei päri hiljem loodavaid uusi lepingu klientide kirjeid.

Saate lisada, värskendada või kustutada lepingu või lepingurea kliendid mis tahes ajal enne lepingu võitmist. Projektilepingu klient peab olema häälestatud kliendina omanikust ettevõttes või juriidilises olemis lehel **Kliendid**. Juriidilised olemid häälestatakse moodulis **Projektihaldus ja raamatupidamine** rakenduses Dynamics 365 Project Operations ja on Project Operationsi moodulites **Projekti müük** ja **Kohaletoimetamise** saadaval ettevõtetena.

## <a name="primary-customers"></a>Peamised kliendid

Potentsiaalne klient projektilepingu vahekaardil **Kokkuvõte** on lepingu peamine klient. Te ei saa peamist klienti lepingu kliendiloendist värskendada. Kui te proovite peamist klienti lepingu kliendioendist kustutada, kuvatakse tõrketeade, mis ütleb, et lepingu peamise kliendi kirjet ei saa kustutada. Selle asemel muutke klienti projektilepingu vahekaardi **Kokkuvõte** väljal **Potentsiaalne klient**. Kui te värskendate seda välja, lisatakse uus valitud klient uue lepingukliendina koos lipuga **Peamine** määratud valikule **Jah**. Eelmine peamine klient on endiselt klient lepingus, kuid nad pole enam peamine klient.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Lepingu kliendikirje loomine, värskendamine või kustutamine

Saate lepingu kliendi luua, uuendada või kustutada lehe **Leping** vahekaardil **Lepingu kliendid**. Projektilepingus on lepingu kliendi kirjesse kaasatud järgmised väljad.

| **Väli** | **Asukoht** | **Kirjeldus** | 
| --- | --- | --- | 
| Ettevõte | Lepingu kliendi vahekaardi **Lepingu kliendid** ning peamise ja kiirloomise lehtede redigeeritav ruudustik. | Loetleb kõik aktiivsed kontod. Pärast kirje loomist see väli lukustatakse. Kirje värskendamiseks peate selle kustutama ja looma siis uuesti. Kui olete salvestanud mis tahes tegelikud näitajad või kui lepingulise kliendi kirje on peamine klient, te ei saa kirjet kustutada. Kui lepingurida luuakse, kopeeritakse lepingu kliendid lepingurea klientidena. |
| Arveldamise jagamise protsent | Lepingu kliendi vahekaardi **Lepingu kliendid** ning peamise ja kiirloomise lehtede redigeeritav ruudustik. | Näitab iga arveldamata müügitehingu protsenti, mis on lepingu kliendile omistatud. Uute projekti lepinguridade loomisel kopeeritakse arveldamise jaotumise protsent kõikidele uutele loodavatele lepinguridadele ja projekti lepingurea klientidele. |
| Maksja: kontakti nimi | Lepingu kliendi vahekaardi **Lepingu kliendid** ning peamise ja kiirloomise lehtede redigeeritav ruudustik. | Seda tekstivälja tuleks kasutada kliendi jaoks arve kontakisiku tuvastamiseks. Vaikeväärtus pärineb seotud konto kirjest. Kontakti nimi kopeeritakse kliendi jaoks genereeritud arve väljale **Maksja: kontakti nimi**. |
| Maksja nimi | Lepingu kliendi vahekaardi **Lepingu kliendid** ning peamise ja kiirloomise lehtede redigeeritav ruudustik. | Kasutage seda tekstivälja kliendi jaoks arve kontakisiku tuvastamiseks. Vaikeväärtus pärineb seotud konto kirjest. Nimi kopeeritakse kliendi jaoks genereeritava arve väljale **Maksja: kontakti nimi**. |
| Maksetingimused | Lepingu kliendi vahekaardi **Lepingu kliendid** ning peamise ja kiirloomise lehtede redigeeritav ruudustik. | Vaikeväärtus pärineb seotud konto kirjest. Tingimused kopeeritakse kliendi jaoks genereeritud arve väljale **Maksja: kontakti nimi**. |
| Omanikust ettevõte | Projektilepingu kliendi vahekaardi **Projektilepingu kliendid** ning peamise ja kiirloomise lehtede redigeeritav ruudustik. | Juriidiline olem, milles klient on moodulis **Projektihaldus ja raamatupidamine** häälestatud. See väli on kirjutuskaitstud ja see on määratud projektilepingu omanikust ettevõttele.</br>Väljale **Konto** lisatavate klientide loend on juba rakenduse Project Operations moodulis **Projektihaldus ja raamatupidamine** omanikust ettevõtte loendist filtreeritud. Omanikust ettevõte on võrdne juriidilise isikuga Project Operationsi moodulis **Projektihaldus ja raamatupidamine**. Kõik sellest projektist tulenevad kulud ja tulud loetletakse omanikust ettevõtte pearaamatus. |
| On ümardamine | Lepingu kliendi vahekaardi **Lepingu kliendid** ning peamise ja kiirloomise lehtede redigeeritav ruudustik. | Näitab, kas klient on tehingu jaoks vaikimisi ümardatav klient. Projektilepingus võib olla ainult üks ümardatav klient. Kui kulu ja arveldamata müük jaotub koguse põhjal ja põhjustab ümardamise erinevusi, rakendatakse seda erinevust kliendi vastenatavatele tegelikele näitajatele. |
| Mitteületatav limiit | Lepingu kliendi vahekaardi **Lepingu kliendid** ning peamise ja kiirloomise lehtede redigeeritav ruudustik. | Näitab, kas on olemas kogusumma kokkulepitud piir või ülempiir, mis kliendile seose eest arveldatakse. Lepingu kliendi tasemel seadistatud mitteületatav limiit hinnatakse suvandis tegeliku arveldamata müügi põhjal, mis viitab lepingu kliendile. |

## <a name="edit-billing-split-percentages"></a>Arveldamise jagamise protsentide muutmine

Saate redigeerida arveldamise jaotumist redugeerides ruudustikku. Kui arveldamise jaotumise protsentide kogusumma ei ole 100 protsenti, ilmneb tõrge. Pärast arveldamise jaotumise protsendi muutmist värskendage leht **Projektileping** tõrke eemaldamiseks.

Võite ka valida projektilepingu kliendi andmeruudustikus suvandi **Jaota ühtlaselt**. Arveldamise jaotumised on jaotatud ühtlaselt kõikide projektilepingu klientide vahel. Kui esineb mis tahes ümardamise tegur, lisatakse tegur ümardamise kliendile. Ühel lepingu kliendil on alati suvandi **Ümardamine** määratud valikule **Jah**. See klient on ümardav klient. Tavaliselt on ümardatav klient ka lepingu peamine klient, kuid seda pole vaja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
