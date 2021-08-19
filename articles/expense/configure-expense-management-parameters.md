---
title: Kuluhalduse parameetrite konfigureerimine
description: Selles teemas kirjeldatakse kuluhalduse üldist käitumist juhtivaid parameetreid.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1cabb0be624f7f6c12761e4fb6d5a095396a5940a37616bb3a304798e1f97808
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007771"
---
# <a name="configure-expense-management-parameters"></a>Kuluhalduse parameetrite konfigureerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles teemas kirjeldatakse kuluhalduse üldist käitumist juhtivaid parameetreid.

## <a name="general"></a>Üldist

| Väli                                                    | Kirjeldus |
|----------------------------------------------------------|-------------|
| Läbisõidu tavamäär                                 | Sisestage läbisõidu kulude hüvitamise määr. See määr korrutatakse läbisõidua, mis sisestatakse kulu jaoks, et arvutada summa, mis sõidukulude eest tagastatakse. |
| Kulu eesmärgi valideerimine                                 | Lülitage see valik sisse, et piirata kasutajad olemasolevate väärtuste kogumiga, mis on konfigureeritud väljal **Kuluaruande eesmärk**, kui nad loovad kuluaruandeid. |
| Isiklike kulude maksja                                | Valige, kes vastutab kõikide isiklikuks liigitatud krediitkaardimaksete summade tasumise eest. |
| Uurimises kogu kuluaruande kuvamine               | Valige see suvand, et kuvada kuluaruande kõik kulud, kui algse dokumendi üksikasju vaadatakse konkreetse vautšeri jaoks, mis loodi kuluaruande postitamise ajal. |
| Reisimise eelnev lubamine on kohustuslik                 | Valige see suvand, kui soovite nõuda, et enne kui töötaja saab esitada kuluaruande, peab olema esitatud ja kinnitatud reisitellimus. |
| Luba enne postitamist muuta jaotisi            | Saate valida, kas kuluaruande jaotusi saab enne postitamist redigeerida. |
| Hinda kuluhalduse poliitikaid                     | Valige kulude hindamise aeg, et teha kindlaks, kas kulupoliitikat on rikutud. Kulude rikkumisi saab hinnata, kui kulukirje sisestatakse ja salvestatakse või kui kuu esitatakse kinnitamiseks. Kviitungite nõutavaid poliitikareegleid hinnatakse, kui kulurida salvestatakse. |
| Luba etttevõttesisesed kuluread                         | Saate valida, kas kuluaruandesse saab sisestada teiste juriidiliste olemite kulusid. |
| Luba krediitkaardi kulude vahetuskurssi muuta | Valige see suvand, kui soovite lubada kasutajal redigeerida imporditud krediitkaardiga seotud kulude vahetuskurssi. |
| Mitmetasandilised hierarha väljad kuvamiseks                  | Valige, millised kinnitaja väljad kuvatakse, kui töövoo määramise tüüp on seatud hierarhiaks ja valik **Hierarhia** on määratud kasutama kinnitamise hierarhiat, kulu mitmetasandilist kinnitamist. Kui töövoo jaoks kasutatakse mitmetasandilise kinnitamise hierarhiat, kuvatakse kuluaruandes valitud väljad ja neid saab redigeerida. |
| Töötaja krediitkaardi sisestamine                        | Valige, kas 15-kohalise või 16-kohalise numbri saab sisestada ja salvestada töötaja lehe **Krediitkaardid** väljale **Kaardi ID**. |
| Reisitellimuse eesmärgi kinnitamine                      | Lülitage see valik sisse, et piirata kasutajad olemasolevate väärtuste kogumiga, mis on konfigureeritud väljal **Kuluaruande eesmärk**, kui nad loovad reisitellimusi. |

## <a name="financial"></a>Rahandustegevus

| Väli                                                                                    | Kirjeldus |
|------------------------------------------------------------------------------------------|-------------|
| Pearaamatu päeva töölehe nimi                                                                | Valige pearaamatu töölehe nimi, kuhu kinnitatud kuluaruanded sisestatakse. |
| Kulude maksutagastuse lubamine                                                        | Valige see suvand, et lubada sobilike kulude jaoks kulude maksutagastus. Seda suvandit ei saa valida juhul, kui USA käibemaks ja kasutusmaksu reeglid on lubatud. |
| Avansimaksete kohene postitamine                                                           | Valige see suvand, kui soovite maksmise ja edastamise toimingu lõpetamisel postitada kinnitatud avansimakse kohe. Kui see suvand pole valitud, loob maksmise ja edastamise protsess registreerimata pearaamatu töölehe. |
| Postitamise ajal arvestuskuupäeva korrigeerimine                                                   | Valige see suvand, et värskendada kulude postitamise ajal arvestuskuupäeva, kui pragune periood on ootel või suletud. Arvestusperiood seatakse järgmisele avatud perioodile. |
| Luba tehingute rühmitamine maksemeetodid määratud tasaarvelduskonto põhjal       | Valige see suvand, kui soovite kulude maksemeetodid määratyd tasaarvelduskonto põhjal summeerida kuluaruande jaoks tehtud kulukanded. |
| Maks kaasatud                                                                             | Valige see suvand, et kaasata vaikimisi kulusummasse käibemaks. |
| Vabasta reisitellimuste sulgemisel koormatis                                      | Valige see suvand, et vabastada koormatud vahendid, kui kinnitatud reisitellimus suletakse. |
| Luba eelarve registri ja projekti eelarve puhul eelarve ületamisel reisitellimuse esitamine | Valige see suvand, et lubada töötajatel esitada kinnitamiseks reisitellimusi, isegi kui nad lubatud eelarvet ületavad, mis on määratud eelarve registris, või projekti lubatud eelarvet. |
| Luba eelarve registri ja projekti eelarve puhul eelarve ületamisel kuluaruande esitamine     | Valige see suvand, et lubada töötajatel esitada kinnitamiseks kuluaruandeid, isegi kui nad lubatud eelarvet ületavad, mis on määratud eelarve registris, või projekti lubatud eelarvet. |
| Luba ainult eelarve registri puhul eelarve ületamisel kuluaruande kinnitamine                 | Valige see suvand, kui soovite lubada kinnitajatel kinnitada kuluaruandeid, mis ületavad eelarveregistris määratud lubatud eelarvet. |

## <a name="per-diem"></a>Päevaraha

| Väli                                 | Kirjeldus |
|---------------------------------------|-------------|
| Päevarahade minimaalne tööaeg            | Sisestage minimaalne tundide arv, palju töötaja peab päeva jooksul töötama, et see oleks kõlblik reisiga seotud kulude seas päevaraha saamiseks. Seda väärtust kasutatakse vaikeväärtusena ainult päevarahade määra tasemete välja **Minimaalsed töötunnid** jaoks. |
| Toidukorra protsent                          | Sisestage reisiga seotud kulude esmesel ja viimasel päeval kasutatav toidu päevaraha vaikeprotsent, kui väli **Toidukorra päevaraha vähendamise arvutamine** on seatud kas valikule **Päevase toidukorra tüüp** või **Toidukordade arv päevas**. Esimese ja viimase päeva tööpäev võib olla tavalisest tööpäevast lühem. Seega võib nendel päevadel päevaraha summa erineda standardsest summast. Kui protsendi väärtuseks on seatud **0** (null), on esimese ja viimase päeva mahaarvamised 0,00. |
| Hotelli protsenti                         | Sisestage hotellide päevaraha vaikeprotsent, mida kasutatakse reisimisega seotud kulu esimesel ja viimasel päeval. Esimese ja viimase päeva tööpäev võib olla tavalisest tööpäevast lühem. Seega võib nendel päevadel päevaraha summa erineda standardsest summast. Kui protsendi väärtuseks on seatud **0** (null), on esimese ja viimase päeva mahaarvamised 0,00. |
| Muud protsendid                         | Sisestage erinevate kulude päevaraha vaikeprotsent, mida kasutatakse reisimisega seotud kulu esimesel ja viimasel päeval. Esimese ja viimase päeva tööpäev võib olla tavalisest tööpäevast lühem. Seega võib nendel päevadel päevaraha summa erineda standardsest summast. Kui protsendi väärtuseks on seatud **0** (null), on esimese ja viimase päeva mahaarvamised 0,00. |
| Hommikusöögi protsendi vähendamine | Sisestage summa, palju päevaraha on vähendatud hommikusöögi jaoks. Näiteks kui töötaja saab tasuta hommikusöögi, võite soovida vähendada päevaraha summat 10 protsendi võrra. |
| Lõunasöögi protsendi vähendamine     | Sisestage summa, palju päevaraha on vähendatud lõunasöögi jaoks. Näiteks kui töötaja saab tasuta lõunasöögi, võite soovida vähendada päevaraha summat 15 protsendi võrra. |
| Õhtusöögi protsendi vähendamine    | Sisestage summa, palju päevaraha on vähendatud õhtusöögi jaoks. Näiteks kui töötaja saab tasuta õhtusöögi, võite soovida vähendada päevaraha summat 25 protsendi võrra. |
| Toidukorra päevaraha vähendamise arvutamine           | Määrake, kuidas süsteem peaks arvutama päevarahade vähendamist, valides, kas vähendus põhineb söögikorra tüübil reisi või päeva kohta või kas see põhineb päeval lubatud einete arvul. |
| Päevaraha ümardamine                     | Valige ümardamise tüüp, mida kasutatakse päevarahade kulude jaoks. Kui valite tavalise ümardamise, ümardatakse iga päevarahade kulu alates summast 0,50 üles 1,00 peale, ja kõik päevarahade kulud, mille summa on väiksem kui 0,50, ümardatakse allapoole 0,00 peale. |
| Päevarahade arvutamise alus          | Saate valida, kas päevarahade summa põhineb kalendripäeva või 24-tunnise ajavahemiku põhjal. |

## <a name="fax-cover-pages"></a>Faksi tiitellehed

| Väli                          | Kirjeldus |
|--------------------------------|-------------|
| Juhised                   | Sisestage juhised, mida töötajad peavad järgima, kui nad loovad faksi tiitellehe, mida kasutatakse kuluaruandega seotud kviitungite saatmiseks. Kindlas keeles kuvatava teksti sisestamiseks, mis põhineb kasutaja keelel, valige suvand **Tõlked**. |
| Kasutaja ID (vöötkoodi teave) | Valige see suvand, kui soovite talletada töötaja kordumatu ID vöötkoodis, mida kasutatakse faksi tiitellehel. |
| Vöötkood                       | Valige vöötkood, mida kasutatakse faksi tiitellehel. Kuluhalduses on toetatud vöötkoodid 39 ja 128. |

## <a name="anti-corruption"></a>Korruptsioonivastane võitlus

| Väli                                 | Kirjeldus |
|---------------------------------------|-------------|
| Kuva korruptsioonivastane tõend   | Valige see suvand, kui soovite, et aruande loomisel näidatakse korruptsioonivastane tekst. Seejärel saab lubada teatud kulukategooria, mille puhul on nõutav, et kuluaruande jaoks saaks valida korruptsioonivastase tõendi. Näiteks võib valitsuse ametliku kuluga seotud kingituste kategooria nõuda, et töötaja kinnitaks, et kulu vastab valitsuse ametnikega seotud ettevõtte poliitikale. |
| Esitaja korruptsioonivastane sõnum | Sisestage tekst, mis näidatakse kuluarunnet koostavale töötajale. Kindlas keeles kuvatava teksti sisestamiseks, mis põhineb kasutaja keelel, valige suvand **Tõlked**. |
| Kinnitaja korruptsioonivastane sõnum  | Sisestage tekst, mis näidatakse kinnitajale kuluarunde koostamise ajal. Kindlas keeles kuvatava teksti sisestamiseks, mis põhineb kasutaja keelel, valige suvand **Tõlked**. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]