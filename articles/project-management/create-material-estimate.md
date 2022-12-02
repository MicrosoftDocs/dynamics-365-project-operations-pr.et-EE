---
title: Projektide materjalide finantsprognoosid
description: See artikkel annab teavet projektipõhiste materjalide määratlemise ja prognoosimise kohta.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eb33c8e2ead2a558bf53256095645011212ff343
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925682"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Projektide materjalide finantsprognoosid

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations võimaldab projektijuhtidel määratleda iga projekti või ülesande jaoks projektipõhised materjalikulud. Iga materjali hinnangu saab seostada konkreetse projektiülesandega. Projektides kasutatavad materjalid võivad olla sisestatavad tooted või tooted tootekataloogist. Iga toote ja ühiku kombinatsiooni jaoks saab projekti müügihinnakirjades ja maksumuse projekti hinnakirjades määratleda hinna.  

Projekti materjali prognoosi vaatamiseks, lisamiseks või kustutamiseks tehke järgmist.

1. Avage **Projektid** ja valige projekt, mida soovite värskendada.
2. Vahekaardil **Materjali prognoosid** vaadake projekti materjalide hinnangute loendit.
3. Uue materjalide prognoosi loomiseks valige suvand **Uus materjalide prognoos**. Või valige kustutamiseks materjali prognoos ja valige seejärel **Kustuta materjali prognoos**.

Järgmine tabel sisaldab teavet väljade kohta projekti real **Materjali prognoos**. 

| **Väli** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- |
| Toiming | Projekti ülesannete loend. See hõlmab kokkuvõtte- ja lehetoiminguid. | Kui valite materjali prognoosi rea jaoks tööülesande, mõjutab see ülesande materjalikulu ja prognoositavat materjali müüki. Kui see väli on tühi, jälgitakse ja summeeritakse materjali prognoosi ainult projekti tasandil. |
| Vali toode |  Saate määrata, kas prognoosirida on olemasoleva (kataloogi) või sisestatava toote kohta. | See väli määratleb, kas valite toote kataloogist või sisestate toote. |
| Toode | Toote ID tootekataloogist. Kui valite toote ID, värskendatakse välja **Toote valimine** väärtus automaatselt valikule **Olemasolev toode**. ID-d kasutatakse hinnakirjast kulu ja müügihinna toomiseks. | Sellel väljal puudub allavoolu mõju. |
| Sisestatava toote kirjeldus | Tekstiväli, kuhu saab kirjutada toote nime. Seda välja tuleks kasutada, kui väljal **Toote valimine** on valitud **Sisestamine**.| Sellel väljal puudub allavoolu mõju. |
| Alguskuupäev | Materjali eeldatava kasutamise prognoositav kuupäev. | Sellel väljal puudub allavoolu mõju. |
| Ühikurühm | Selle välja vaikeväärtus pärineb kataloogitoote vaikimisi ühikurühmast. Saate selle välja värskendada, et valida mõne muu ühikurühma. | Sellel väljal puudub allavoolu mõju. |
| Üksus | Selle välja väärtus pärineb valitud toote vaikeühikult. Saate selle välja värskendada, et valida mõne muu ühiku. | Ühiku muutmise tulemuseks on erinev vaikimisi ühikuhind ja kulu. |
| Kogus | Projektis kasutatava toote eeldatav kogus. | Sellel väljal puudub allavoolu mõju. |
| Ühiku kulu | Valitud toote ja ühiku kombinatsiooni ühikukulu, mis on häälestatud rakendatavas kuluhinnakirjas. | Ühikukulu kuvatakse alati projekti kuluvaluutas. Kui hinnakirjas pole kombineeritud toote ühiku kulu ja ühikut häälestatud, on ühiku kuluks vaikimisi 0,00. |
| Ühiku hind | Valitud toote ja ühiku kombinatsiooni hind, mis on häälestatud rakendatavas müügi hinnakirjas. | Ühiku hind kuvatakse alati projekti müügivaluutas. Kui hinnakirjas pole kombineeritud toote ühiku hinda ja ühikut häälestatud, siis ühiku hinnaks on vaikimisi 0,00.|
| Kogukulu | Kulusumma, mis arvutatakse kui kogus \* ühikukulu.| Kulusumma kuvatakse alati projekti kuluvaluutas. |
| Müük kokku | Müügisumma, mis arvutatakse kui kogus \* ühikuhind. | Müügisumma kuvatakse alati projekti müügivaluutas. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
