---
title: Projekti hinnakirja haldamine hinnapakkumises
description: Selles artiklis antakse teavet olemi Project hinnakirja kohta.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8439a03e6557ec531405048ec4149344e283242e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933139"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Projekti hinnakirja haldamine hinnapakkumises

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Rakendus Dynamics 365 Project Operations pikendab hinnakirja olemit rakenduses Dynamics 365 Sales. 

## <a name="key-entities"></a>Võtmeolemid

Hinnakiri sisaldab teavet, mida pakuvad neli erinevat olemit.

- **Hinnakiri**: see olem talletab hinnakirja arvestamisel teavet konteksti, valuuta, kuupäeva jõustumise ja ajaühikute kohta. Kontekst näitab, kas hinnakiri väljendab kulumäära või müügihindu. 
- **Valuuta**: see olem talletab hinnakirja hindade valuuta. 
- **Kuupäev**: seda olemit kasutatakse juhul, kui süsteem proovib sisestada tehingu hinna vaikeväärtuse. Hinnakiri, millel on jõustumiskuupäev, mis hõlmab tehingu valimise kuupäeva. Kui leitakse rohkem kui ühe hinnakiri, mis on tehingu kuupäeval kehtiv ja mis on lisatud sellega seotud hinnapakkumisele, lepingule või organisatsiooniüksusele, siis hinda ei muudeta. 
- **Aeg**: see olem talletab ajaühiku, mille jooksul hinnad on väljendatud (nt päeva- või tunnitasu). 

Hinnakirja olemil on kolm seostuvat tabelit, mis talletavad hindu.

  - **Rolli hind**: see tabel talletab rolli ja organisatsiooni üksuse väärtuste kombinatsiooni määra ning seda kasutatakse inimressursside rollipõhiste hindade seadmiseks.
  - **Tehingukategooria hind**: see tabel talletab hinnad tehingukategooriate kaupa ja seda kasutatakse kulukategooriate hindade seadistamiseks.
  - **Hinnakirja üksused**: see tabel talletab kataloogis olevate toodete hindu.
 
Hinnakiri on hinnakaart. Hinnakaart on kombinatsioon hinnakirja olemist ja seotud ridadest, mis on tabelites rolli hind, tehingukategooria hind ja hinnakirja üksused.

## <a name="resource-roles"></a>Ressursirollid

Mõiste *ressursiroll* viitab oskustele, pädevustele ja tõenditele, mida peab isik omama projektiga seotud teatud toimingute läbiviimiseks.

Inimressursside aeg on noteeritud vastavalt rollile, mille ressurss täidab kindla projektiga. Inimressursside aeg, kuluarvutust ja arveldamine põhinevad ressursirollil. Aja saab arvestada mis tahes ühikus ühikurühmas **Aeg**.

Ühikurühm **Aeg** luuakse, kui installite rakenduse Project Operations. Sel on vaikeühik **Tund**. Ühikurühma **Aeg** või ühiku **Tund** atribuute ei saa kustutada, ümber nimetada ega redigeerida. Soovi korral saate aga ühikurühma **Aeg** lisada ka muid ühikuid. Kui proovite kustutada kas ühikurühma **Aeg** või ühiku **Tund**, võite äriloogikas tõrkeid põhjustada.
 
## <a name="transaction-categories-and-expense-categories"></a>Tehingukategooriad ja kulukategooriad

Reisikulud ja muud kulud, mis projektikonsultandid kannavad, arvestatakse kliendile. Kulukategooriate hinnakujundus viiakse lõpule kasutades hinnakirju. Lennupiletid, hotell ja autorent on näited kulukategooriate kohta. Iga hinnakirja rida kulude jaoks määrab kindla kulukategooria hinna. Kulukategooriate hinnakujunduseks kasutatakse järgmist kolme meetodit.

- **Omahinnaga**: kulu arvestatakse kliendile ja juurdehindlust ei rakendata.
- **Juurdehindluse protsent**: tegeliku kulu protsent on kliendile arvestatud. 
- **Ühiku hind**: iga kulukategooria ühiku kohta määratakse arve hind. Kliendile arvestatud summa arvutatakse vastavalt konsultandi aruannete ühikute arvule. Läbisõit kasutab hinna ja ühiku hinna hinnakujundusmeetodit. Näiteks läbisõidu kulukategooria saab konfigureerida 30 USA dollari eest (USD) päevas või 2 USD miili kohta. Kui konsultant teatab projektis läbisõidu, arvutatakse arve summa konsultandi teatatud miilide arvu põhjal.
 
## <a name="project-sales-pricing-and-overrides"></a>Projekti müügihind ja alistamine

Projekti hinnapakkumiste ja lepingute puhul on projekti hinnakirjas teistsugune hinna alistamise muster kui toodete hinnakirjas. Tootekataloogil põhineval hinnapakkumise real saate hinna alistada rollidele ja kategooriatele otse pakkumise real, sest iga hinnapakkumise rida osutab täpselt ühele kataloogiüksusele. Projektil põhineva hinnapakkumise ei saa te siiski otse hinnapakkumiste real olevate rollide ja kategooriate hinda alistada. Kasutage projekti hinnakirja, et toetada kahte erinevat alistamise mustrit.

> [!NOTE]
> Soovitame, et teil oleks oma projekti ressursside ja kataloogiüksuste jaoks eraldi hinnakiri nende kahe käitumise erinevuste tõttu, kui te alistate hinnakujunduse.

Kõigil järgmistest olemitest võib projekti hinnakujunduseks olla üks või mitu seotud müügi hinnakirja.

- Klient (konto) 
- Müügivõimalus 
- Hinnapakkumine 
- Projektileping

Nende olemite seotust hinnakirjaga näitavad projekti hinnakirjad. Saate seostada ühe või mitu hinnakirja kliendi, müügivõimaluse, hinnapakkumise ja projekti lepingu müügi olemitega.

Vaikimisi projekti hinnakirja ei sisestata kliendi kirjesse automaatselt. Siiski saate projekti hinnakirja käsitsi manustada kliendi kirjele. Sellegipoolest peaksite projekti hinnakirja käsitsi lisama ainult siis, kui teil on kliendiga kohandatud hinnakujunduse leping. 

Kui projekti hinnakiri on seotud müügiesindaja, valideeritakse järgmine teave.

- Hinnakirjal on kontekst **Müük**. 
- Hinnakirja valuuta ühtima kliendi valuutaga. 

Projekti lepingu järgmine järjestus, et seada seotud projekti hinnakiri automaatselt.

1. Hinnapakkumine
2. Müügivõimalus
3. Klient 
4. Globaalsätted 

Kui projekti hinnakiri on vaikimisi sisestatud, kinnitab süsteem, et valuuta vastab kliendi valuutale ja et vaikimisi määratud hinnakirjad sisaldavad konteksti **Müük**.

Saate seostada mitu projekti hinnakirja kliendi, müügivõimaluse, hinnapakkumise ja projekti lepingu olemitega. See võimalus toetab kuupäevapõhiseid vaikimisi hindu pikaajalise projektilepingu jaoks, mille puhul võib inflatsiooni tõttu tekkivate hinnavärskenduste arvestamiseks vajada mitut hinnakirja. Kui aga kliendi, müügivõimaluse, hinnapakkumise või projekti lepingu olemiga seostatud hinnakiri sisaldab kattuvat jõustumiskuupäeva, võivad vaikimisi hinnad valed olla. Seetõttu peaksite veenduma, et projekti hinnakiri, millel on kattuvad jõustumiskuupäevad, pole nende olemitega seostatud.

### <a name="deal-specific-price-overrides"></a>Tehinguga seotud hinna alistamised

Saate luua valitud projektihindadele tehingupõhised alistamised projekti hinnakirjades, mis on vaikimisi sisestatud hinnapakkumisel või projektilepingus.

Vaikimisi saab projekti lepingust alati põhimüügi hinnakirja koopia, mitte sellele otsest linki. Selline käitumine aitab tagada, et kliendiga sõlmitud hinnakiri (SOW) ei muutu, kui peahinnakiri muutub.

Kuid hinnapakkumise puhul saate kasutada põhihinnakirja. Soovi korral saate ka põhihinnakirja kopeerida ja seda redigeerida, et luua kohandatud hinnakiri, mis rakendub ainult sellele hinnapakkumisele. Hinnapakkumisega seotud uue hinnakirja loomiseks valige lehel **Hinnapakkumine** suvand **Loo kohandatud hinnakujundus**. Tehingupõhisele projekti hinnakirjale pääsete juurde ainult hinnapakkumise kaudu. 

Kohandatud projekti hinnakirja loomisel kopeeritakse ainult hinnakirja projekti komponendid. Teisisõnu uus hinnakiri, mis on loodud olemasoleva projekti hinnakirja koopiana, mis on lisatud hinnapakkumisele, ning sellel uuel hinnakirjal on ainult seotud rollihinnad ja tehingukategooriate hinnad.
  
## <a name="tracking-costs"></a>Kulude jälgimine

Project Operations jälgib kulusid inimressursside kasutamisele projektidele. Samuti jälgib see kulusid, mis on seotud muude kuludega, mis on projekti käigus ette tulnud, näiteks reisikulud.

Nagu arve määrad, seadistatakse inimressursside jaoks ka kulumäärad, kasutades hinnakirja. Peamised erinevused omahinna hinnakirja ja müügi hinnakirja käitumises on järgmised.

- Ressursi kulumäära ei saa teatud projekti, lepingu ega hinnapakkumise suhtes alistada. Kuid arve määrad saab alistada iga tehingu põhjal, kui tehakse muudatusi, mis on seotud tehingu olemusega. 

- Omahinna hinnakirja lahendamiseks kasutatakse järgmist tellimust.

    1. Organisatsiooniüksusega seotud omahinna hinnakiri.
    2. Project Operaruibsi parameetritega seotud omahinna hinnakiri. Kuna parameetritele saab lisada paljudes erinevates valuutades esitatud omahinna hinnakirju, siis viiakse valuuta vastendamine lõpuni projekti tellija organisatsiooniüksuse, lepingu või hinnakirja ja omahinna hinnakirja valuuta vahel.
    3. Kulude puhul ei rakendata omahinna ja kulu hinnalisandi hinnakujundusmeetodit omahinna hinnakirjadele. Isegi juhul, kui neid hinnakujundusmeetodeid kasutatakse tehingukategooria kulude seadistamiseks omahinna hinnakirjadel, ignoreerib süsteem neid ja ühtegi vaikimisi omahinda ei sisestata.


[!INCLUDE[footer-include](../includes/footer-banner.md)]