---
title: Kulumallide seadistamine
description: See teema sisaldav teavet selle kohta, kuidas luua ja kasutada rakenduses Project Operations kulumalle.
author: sigitac
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 786b2b9b140f82d406044c2ed05761d7f46ee9e0
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642718"
---
# <a name="set-up-cost-templates"></a>Kulumallide seadistamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_


See teema sisaldav teavet selle kohta, kuidas luua ja kasutada rakenduses Project Operations kulumalle. Kulumall määratleb järgneva.

- Prognoosi projektikategooriad ja tegelikud tehingud, mis kaasatakse projekti lõpuleviimise arvutamise protsenti. Lõpuleviimise väärtuse protsenti kasutatakse seejärel arvutamiseks, kui palju tulu on kajastatud.
- Kas lõpuleviimise protsenti saab muuta, kui see on automaatselt arvutatud.
- Kas lõpuleviimise protsent arvutatakse summade või ühikute põhjal.

## <a name="cost-template-example"></a>Kulumalli näide

Töötate veebisaidi kujundamise projekti kallal kliendi jaoks, kellelt võtate kindla tasu 10 000 eurot. Te prognoosite, et projekti lõpuleviimiseks kulub 100 tundi (5000 eurot). Lisaks prognoosite, et kasutate kahte lennupiletit ja nelja ööd hotellis, et külastada klienti kohapeal (1800 eurot). Selle tulemuseks on prognoositav kulu summas 6800 eurot.

Kui käivitate kuu lõpus fikseeritud hinnaga tulu kajastamise protsessi hinnangu loomiseks, saate teada, et olete töötanud projekti kallal 35 tundi. See ei hõlma lende ega hotelli kulu. Teil oli lisaks assistent, kes tegi viis tundi uurimistööd projekti jaoks, mille maksumus oli 100 eurot, mida te ei olnud plaaninud.

Kui arvutate selle projekti lõpuleviimise protsendi väärtust, on teil võimalik teha kaks valikut.

- Kas soovite kaasata kõik kulud (tunnid ja kulutused) või ainult tunnid?
- Kas soovite kaasata kõik tunnid ja ainult plaanitud tunnid?
- Kas soovite arvutada lõpuleviimise protsendi planeeritud tundide kulu põhjal eurodes (5000 eurot) või ainult tundide arvu põhjal (100)?

Teie vastused nendele küsimustele määratlevad valikud, mille määrate kulumallis, ja kategooriad, mille valite kulumalli ridadel.

Järgmises tabelis on esitatud selle stsenaariumi lõpuleviimise protsendi väärtuse arvutamise erinevate meetodite tulemused.

| Lõpuleviimine põhineb järgneval | Kulu eurodes või ühikud | Lõpuleviimisprotsent | Arvutus |
| --- | --- | --- | --- |
| Kõik tunnid, kulud puuduvad | Kulu eurodes | 37% 35 × EUR 50 + EUR 100 = EUR 1850 EUR 1850 / EUR 5000 |
| Kõik tunnid, kulud puuduvad | Ühikud | 40% | 40 tundi / 100 tundi (sh viis plaanivälist tundi) |
| Plaanitud tunnid, kulud puuduvad | Kulu eurodes või ühik | 35% | 35/100 tundi või 35 × EUR 50 / 5000 |
| Kõik tunnid ja kulud | Kulu eurodes | 27,2% | EUR 1850 / EUR 6800 |

Otsustamine, millist lähenemisviisi kulumalli loomiseks kasutada, võib oleneda mitmest kaalutlusest.

- Kui kaasate kulumalli planeerimata tunnid, on oht jõuda lõpuleviimise 100 protsendini enne projekti lõpetamist. Selle põhjuseks on, et tegelikke tunde on rohkem kui planeeritud tunde. Kui kasutate ühte tabelis toodud kahest esimesest meetodist, peaksite muutma plaani (prognoositud ühikuid), kui saate kõrvalekalletest teada. Sellisel juhul võite liita või lahutada tunde, mis teie meelest on projekti lõpuleviimiseks nõutavad. Kui projekti lõpuleviimiseks on vaja veel 65 tundi, peate lisama plaanile viis tundi, et kokku oleks neid 105. Kui teate, et teie assistent teeb veel tundi uurimistööd, on kogusumma 110 tundi.
- Kui kasutate tabelis toodud kolmandat meetodit, värskendate ainult teie enda aja jaoks planeeritud tunde, et hoida lõpuleviimise protsendi arvutus täpsena. Teie kasumlikkus muutub, kui logite planeerimata tunde, kuid jääte teadaolevale lõpuleviimise protsendi trajektoorile.
- Kui kasutate mõlemat tabelis loetletud meetodit, on oh, et ebatavalistel aegadel esineb kulusid ja neid ei pruugi teie lõpuleviimise edenemises olla kajastatud. Seega kui kulud on kaasatud, võivad need põhjustada teie lõpuleviimise protsendi kõikumist rohkem kui see on soovitav. Näiteks kuna te veel ei lennanud, võib teie lõpuleviimise protsent olla 27%, mitte 35% või 37%, kuid see põhines ainult aja arvutamisel. Kui te oleksite ühel reisil käinud, veetnud hotellis kaks ööd ja teie lennupiletite ja hotellikulu oli õigesti prognoositud, oleks lõpuleviimise protsent 40,4% (1850 eurot töö ees ja 900 eurot kulutuste eest = EUR 2750 / EUR 6800 = 40,4%). Seega vaid ühe lennureisi kulude lisamine muudaks lõpuleviimise protsendi 27% pealt 40% peale.

## <a name="create-cost-templates"></a>Kulumallide loomine
Kulumallide loomiseks tehke järgmist.

1. Rakenduse Dynamics 365 Finance keskkonnas kulumallidele juurdepääsuks minge jaotisse **Projektihaldus ja raamatupidamine** > **Seadistamine** > **Hinnangud** > **Kulumall**.
2. Uue kulumalli loomiseks valige **Uus**. Sisestage nimi ja kirjeldus.
3. Sisestage iga kandetüübi jaoks kulurea ID.
4. Valige vaikimisi lõpuleviimise meetod.

  - **Automaatne**: lõpuleviimise protsent arvutatakse projekti jaoks automaatselt. Tulemuseks olevat väärtust ei saa muuta.
  - **Käsitsi**: lõpuleviimise protsent arvutatakse projekti jaoks automaatselt. Tulemuseks olevat väärtust saab muuta.

  > [!NOTE]
  > Käsitsi arvutamisel säilitatakse lõpuleviimise protsenti lehe **Hinnang** vahekaardil **Üldine** suvandis **Käsitsi arvutamine**.

5. Suvandis **Lõpuleviimine põhineb järgneval** valige üks järgmistest väärtustest.

  - **Summa**: arvestusvaluuta summa arvutab lõpuleviimise protsendi.
  - **Ühik**: kogus arvutab lõpuleviimise protsendi.
  - **Sirgjooneline**: süsteem arvutab lõpuleviimise protsendi proportsionaalselt, kasutades projekti algus- ja lõpukuupäevi, et määratleda projekti kestus.

6. Valige suvand **Kuluread**, et vaadata läbi kulumalli kuluread. Iga kandetüübi jaoks on nõutav vähemalt üks kulurida. Samas saate luua sama kandetüübi jaoks mitu kulurida ja määrata nende ridade jaoks soovitud atribuudid.
7. Valige vahekaardil **Kategooriad** projekti kategooriad, mille kulumalli reale kaasata.
8. Valige vahekaardil **Üldine**, kas see rida kaasatakse lõpuleviimise protsendi arvutamisse.
9. Valige kulu, et viia lõpule lõpuleviimise protsendi arvutamiseks kasutatav meetod.


[!INCLUDE[footer-include](../includes/footer-banner.md)]