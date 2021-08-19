---
title: Projekti hinnapakkumistes mitme kliendi haldamine – liht
description: Selles teemas antakse teavet mitme projekti rahastava kliendi hinnapakkumisega töötamise kohta. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c9b3c1a1b958de0fc5d58199b8229ea5b3b221d01efe6602eecffdd100f13cae
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001651"
---
# <a name="manage-multiple-customers-on-project-quotes---lite"></a>Projekti hinnapakkumistes mitme kliendi haldamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Projekti hinnapakkumised toetavad stsenaariumit, kus ettepanek hõlmab mitut lepingut rahastavat klienti. Hinnapakkumise vahekaardil **Kokkuvõte** on väli **Potentsiaalne klient**, mis tuvastab tehingu peamise kliendi. Lepungu teisi kliente saab seadistada projekti hinnapakkumise vagekaardil **Kliendid**.

Kõik hinnapakkumise vahekaardil **Kliendid** olevad hinnapakkumise kliendid on vaikimisi hinnapakkumise rea kliendid mis tahes hinnapakkumise jaoks loodava **uue** projektipõhise hinnapakkumise ridade puhul. Kõik olemasolevad projektipõhised hinnapakkumise read ei päri pärast neid loodud uusi hinnapakkumise kliendikirjeid.

Tootepõhised hinnapakkumise read seostatakse automaatselt peamise kliendiga, kes on hinnapakkumise vahekaardi **Kokkuvõte** väljal **Potentsiaalne klient**.

Hinnapakkumise kliendid ja hinnapakkumise rea kliendid saab enne hinnapakkumise võitmist igal ajal lisada, ajakohastada või kustutada.

## <a name="concept-of-a-primary-customer"></a>Peamise kliendi kontseptsioon

Projekti hinnapakkumisel kokkuvõtte vahekaardil potentsiaalse kliendina olev klient on hinnapakkumise peamine klient. Kui proovite peamise kliendi hinnapakkumise klientide loendist kustutada, kuvatakse tõrge, et hinnapakkumise peamise kliendi kirjet ei saa kustutada.

Peamist klienti ei tuleks hinnapakkumise kliendiloendist värskendada. Samas te saate peamist klienti mõjutada, muutes hinnapakkumise vahekaardil **Kokkuvõte** potentsiaalset klienti. Kui see väli on suvandis **Hinnapakkumise kokkuvõte** värskendatud, lisatakse äsja valitud potentsiaalne klient uue hinnapakkumise kliendina, millel on määratud lipp **Peamine**. Vana potentsiaalne klient on endiselt hinnapakkumise klient.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Hinnapakkumise kliendi kirje loomine, värskendamine või kustutamine

Hinnapakkumise klienti saab luua, uuendada või kustutada lehe **Hinnapakkumine** vahekaardil **Hinnapakkumise kliendid**. Järgmises tabelis loetletud väljad on projekti hinnapakkumise kliendi kirjes.

| **Väli** | **Asukoht** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- | --- |
| Ettevõte | Vahekaardi **Hinnapakkumise kliendid** redigeeritav ruudustik ja hinnapakkumise kliendi vormid **Peamine** ja **Kiirloomine**. | Loetleb kõik aktiivsed kontod. Pärast kirje loomist see väli lukustatakse. Kui soovite seda värskendada, kustutage kirje ja looge see uuesti. Kui olete salvestanud kõik tegelikud näitajad või kui hinnapakkumise kliendi kirje on peamine klient, on teil lubatud kirje kustutada. | Hinnapakkumise kliendid kopeeritakse hinnapakkumise rea loomisel hinnapakkumise rea klientidega üle. Hinnapakkumise kliendid kopeeritakse samuti hinnapakkumise võitmisel projekti lepingu klientidele. |
| Arveldamise jagamise protsent | Vahekaardi **Hinnapakkumise kliendid** redigeeritav ruudustik ja hinnapakkumise kliendi vormid **Peamine** ja **Kiirloomine**. | Esindavad iga arveldamata müügitehingu protsenti, mis omistatakse selle hinnapakkumise kliendile. | Kopeeritud uue hinnapakkumise ridadele ja projekti lepingu klientidele. |
| Maksja: kontakti nimi | Vahekaardi **Hinnapakkumise kliendid** redigeeritav ruudustik ja hinnapakkumise kliendi vormid **Peamine** ja **Kiirloomine**. | See on tekstiväli ja seda tuleks kasutada selle kliendi arve kontaktisiku tuvastamiseks. Need tulevad vaikimisi seotud kontokirjetest | Kopeeritakse üle projekti lepingu klientidele, kui hinnapakkumine võidetakse ja omakorda arve väljale Maksja: kontakti nimi, mis on selle kliendi jaoks loodud. |
| Maksja nimi | Vahekaardi **Hinnapakkumise kliendid** redigeeritav ruudustik ja hinnapakkumise kliendi vormid **Peamine** ja **Kiirloomine**. | Seda tekstivälja tuleks kasutada selle kliendi arve kontaktisiku tuvastamiseks. | Kopeeritakse projekti lepingu klientidele, kui hinnapakkumine võidetakse ja omakorda arve väljale **Maksja: kontakti nimi**, mis on selle kliendi jaoks loodud. |
| Maksetingimused | Vahekaardi **Hinnapakkumise kliendid** redigeeritav ruudustik ja hinnapakkumise kliendi vormid **Peamine** ja **Kiirloomine**. | See on suvandikomplekt väärtusega, mis pärineb vaikimisi seostuvast kontokirjest. | Kopeeritakse projekti lepingu klientidele, kui hinnapakkumine võidetakse ja omakorda arve väljale **Maksja: kontakti nimi**, mis on selle kliendi jaoks loodud. |
| On ümardamine | Vahekaardi **Hinnapakkumise kliendid** redigeeritav ruudustik ja hinnapakkumise kliendi vormid **Peamine** ja **Kiirloomine**. | Näitab, kas see klient on selle tehingu jaoks vaikimisi ümardamise klient. | Kopeeritakse hinnapakkumise võitmisel projekti lepingu klientidele. |
| Mitteületatav limiit | Vahekaardi **Hinnapakkumise kliendid** redigeeritav ruudustik ja hinnapakkumise kliendi vormid **Peamine** ja **Kiirloomine**. | Näitab, kas sellele kliendile esitatakse selle suhtluse eest arve summas, millel on läbiräägitud limiit või ülempiir | Kopeeritakse hinnapakkumise võitmisel projekti lepingu klientidele. |

## <a name="editing-billing-split-percentages"></a>Arveldamise jagamise protsentide muutmine

Saate muuta arveldamise jagamise protsente, kasutades reasisese ruudustiku redigeerimise kogemust. Kui arvelduse jagamise protsentide summa ei ole kokku 100%, esineb tõrge. Pärast arveldamise jagamise protsentide värskendamist värskendage lehte, et viga eemaldada.

Võite proovida ka valida hinnapakkumise kliend andmeruudustikus suvand **Jaota ühtlaselt**. See toiming määrab arveldamise jaotamise kõigile hinnapakkumiste klientidele. Kui esineb ümardamise tegur, lisatakse see ümardamise kliendile. Üks hinnapakkumise klientidest on alati märgistatud kui ümardatav klient. See tähendab, et hinnapakkumise kliendi kirjel on lipu **Ümardamine** väärtuseks määratud **Jah**. Tavaliselt on see hinnapakkumise peamine klient, kuid seda saab muuta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]