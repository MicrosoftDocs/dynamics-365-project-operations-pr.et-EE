---
title: Meeskonnaliikmete lisamine meeskonnaliikmete ruudustikust
description: Selles teemas antakse teavet meeskonnaliikmete ressursside haldamise kohta.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: de73dac28046ec98ed201e129be6511f894223fd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121528"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Meeskonnaliikmete lisamine meeskonnaliikmete ruudustikust

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Rakendus Dynamics 365 Project Operations sisaldab ressursihalduri armatuurlauda, mis pakub visuaalset ülevaadet ressursi nõudlusest ja kasutamisest kogu ettevõttes. Armatuurlaua diagramme saate kasutada järgmise teabe visualiseerimiseks.

- **Ressursi nõudlus**: diagramm **Aktiivne ressursitaotlus** kuvab esitatud ressursid. Ressursid on koondatud kas rolli või projekti kaudu.
- **Esitamata ressursi nõudmised**: diagramm **Määramata ressursi nõudlus** näitab kõiki ressursinõudeid, mida pole veel esitatud. See diagramm aitab ressursihalduritel vaadata nõudlust, mis pole kindel ja mida võidakse esitada ressursitaotluse kaudu.
- **Viimase nädala tasustatav kasutamine**: diagramm **Kasutamine rolli järgi** näitab organisatsiooni tegeliku arvete kasutamise protsenti rolli poolt, mis on seotud selle sihtmärgiga.

    > [!NOTE]
    > Selleks et teha diagramm **Kasutamine rolli järgi** kättesaadavaks, looge töövoogu **UpdateRoleUtilization** käitav töö. Seda korduvat tööd käitatakse iga seitsme päeva järel, et arvutada viimase seitsme päeva jooksul tasustatav kasutamine. Tulemused on koondatud rolli järgi.

## <a name="manage-project-team-members"></a>Projekti meeskonnaliikmete haldamine

Projektihaldurid saavad kasutada ressursihalduri armatuurlauda, et hallata projektide ressursse. Näiteks saavad nad lisada meeskonnaliikme otse projekti ja broneerida meeskonnaliikme, kes vastab üldise ressursi kogutud ressursinõuetele.

### <a name="add-a-team-member-directly-to-a-project"></a>Meeskonnaliikme lisamine otse projektile

Meeskonnaliikme lisamiseks otse projektile valige vormil **Projektid** vahekaardil **Meeskond** suvand **Uus**. Kuvatakse dialoogiboks **Kiirloomine: projekti meeskonnaliige**. Selles dialoogiboksis saate teha järgmisi toiminguid.

- **Nimega ressursi broneerimine**: valige väljal **Broneeritav ressurss** ressursi nimi. Seejärel valige roll, määrake periood ja valige jaotamise meetod. Teie valitud nimega ressurss lisatakse projektile valitud jaotamise meetodi ja ressursside kalendri abil.
- **Üldise ressursi lisamine**: jätke väli **Reserveeritav ressurss** tühjaks ja valige seejärel roll, määrake ajavahemik ja valige soovitud jaotuse meetod. Üldine ressurss lisatakse kohatäitena meeskonnale. Kohatäide sisaldab nõudluse mustrit, mida kasutatakse meeskonnas nimega ressursside broneerimiseks. Nõue esitatakse vastavalt projekti kalendrile.
- **Nimega ressursi lisamine meeskonnale, rakendamata ressursi võimsust**: valige väljal **Broneeritav ressurss** ressurss. Valige ajavahemik ja valige seejärel jaotamise meetodiks **Puudub**. Ressurss lisatakse meeskonda, kuid ressursi võimsust ei tarbita broneerimise kaudu.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Reserveerige meeskonnaliige, et täita ressursinõudeid üldise ressursi jaoks

Rakenduses Project Operations saate broneerida projektimeeskonnas üldise ressursi. Samuti saate määrata rolli, nõutava võimsuse ja võimsuse jaotumise viisi. Ressursinõudes saate määrata üldiste ressurssidega seotud atribuudid. Need atribuudid hõlmavad nõutavaid oskusi, eelistatud organisatsiooniüksust ja eelistatud ressursse.

Täitke järgmised etapid, et määrata arendaja jaoks üldise ressursi nõutavad oskused.

1. Valige vormi **Projektid** vahekaardil **Meeskond** käsk **Uus**, et broneerida üldine ressurss.
2. Valige vaates **Kõik meeskonnaliikmed** veerus **Ressursinõue** vastav link, et lisada üldisele ressursile nõutavad oskused.
3. Valige vormil **Ressursinõue** ruudustikus **Oskused** ruudustikus kolmikpunkt (**…**) ja seejärel valige **Lisa uus nõude omadus**, et lisada arendajale vajalikud oskused.
4. Valige dialoogivormil **Kiirloomine: nõude tunnused** väljal **Tunnused** soovitud oskus.
5. Valige väljal **Hinnangu väärtus** selle oskuse jaoks oskuse tase. 
6. Määrake väljal **Ressursinõue** nõue, et ressursid pärineks organisatsiooniüksustest või isegi nimega ressurssidest. Kui olete lõpetanud, valige **Save**.
7. Valige vormil **Ressursinõue** käsk **Broneeri**, et täita ressursinõue. Saate valida üldise ressursi ka ruudustikus **Kõik meeskonnaliikmed** ja seejärel valige **Reserveeri**.

    > [!NOTE]
    > Selles näites on 40 nõutavat tundi, kuid tegelikke broneeritud tunde ei kuvata, kuna üldistel ressurssidel pole reserveeringuid. Lisaks pole määratud tunde, kuna üldine ressurss lisati tööülesande määramise abil lisamise asemel otse meeskonnale.

    Vormil **Plaanimisabimees** saate saadaolevaid ressursse filtreerida ressursinõudes määratud nõuete järgi. Ressursid sorditakse vastavalt ajakavapaneelil määratud sortimise parameetritele.

   Mõned kõige sagedamini kasutatavad filtrid on järgmised.

    - **Tunnused koos hinnanguga**: filtreerimine oskuste, sertifitseerimise ja muude ressursside omaduste alusel ning lisaks oskustaseme alusel.
    - **Rollid**: filtreeritakse vaikimisi kasutatavate rollide järgi, mis on määratud broneeritud ressurssidele.
    - **Organisatsiooniüksused**: filtreerige arvestuslikke ressursse nende organisatsiooniüksuste järgi, kellele nad on määratud.

8. Kui te pole algse nõude otsingu tulemustega rahul, saate filtri kriteeriume muuta. Laiendage vasakul olevat paani **Filtri vaade** ja seejärel valige **Otsi**, et leida täiendavaid ressursse. Tulemuste sortimise muutmiseks valige **Sordi**.
9. Valige ressursid vastavalt vajadusele määratud nõudmisele, nagu on näidatud ruudustiku ülaosas. Saate tühjendada koordinaatvõrgus olevate lahtrite valiku ja jätta selle ressursi võimsuse avatuks. Korraga saab valida ainult ühe ressursi.
10. Valige ressursi broneerimiseks **Broneeri** ja jätke ajakavapaneel avatuks, et saaksite valida täiendavad ressursid. Võite ka valitud ressursi broneerimiseks ja ajakavapaneeli sulgemiseks valida **Broneeri ja välju**.
11. Naaske vaatesse **Kõik meeskonnaliikmed**. Pange tähele, et üldine ressurss on asendatud nimega ressursiga ja 40 tundi on reserveeritud selle ressursi jaoks.

    > [!NOTE]
    > Määratud tunde ei kuvata, kuna nad on otse meeskonnas broneeritud. Neid ei broneeritud tööülesande määramise abil.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Üldiste ressursside määramine tööülesannetele ja ressursinõuete loomine

Rakenduses Project Operations saate luua tööülesandeid ja määrata neile üldiseid ressursse. Ressursi nõudluse saab seejärel esitada kohatäitena, kui hindate oma ajakava ja finantsnumbreid. Seejärel saate luua ressursinõudeid üldistele ressurssidele ja need täita.

1. Tööülesande loomiseks valige vormil **Projektid** vahekaardil **Ajakava** **Lisa**.
2. Valige väljal **Ressursid** sümbol **Ressursivalija**. Kuvatakse ressursivalija, mis kuvab projekti jaoks olemasolevad meeskonnaliikmed.
3. Sisestage uue üldise ressursi nimi ja seejärel valige **Loo**.
4. Valige kuvatavas dialoogiboksis **Kiirloomine: projekti meeskonnaliikmed** väljal **Roll** üldisele ressursile roll. 
5. Valige väljalt **Ressursiühik** üldisele ressursile organisatsiooniüksus. Seejärel tehke valik **Salvesta**. Üldine meeskonnaliige on nüüd ülesandele määratud.

   Vahekaardil **Meeskond** kuvatakse uus üldine meeskonnaliige. Pange tähele, et sel on määratud ainult tunde. Need tunnid on kõigi üldiste meeskonnaliikmete jaoks määratud ülesannete summa. Üldisel meeskonnaliikmel pole nõutavaid tunde ega ressursinõuet.

6. Nüüd saate määrata üldise meeskonnaliikme teistele ülesannetele, kasutades ressursivalijat.

   Kui olete üldise ressursi määramise ülesannetele lõpetanud, saate luua ressursinõude üldise ressursi jaoks.

7. Valige vahekaardil **Meeskond** üldine ressurss ja seejärel valige **Loo nõue**. Kui nõue luuakse, on üldisel meeskonnaliikmel nõutavad tunnid ja link ressursinõudele.

  Pärast nimega ressursi broneerimist eemaldatakse üldine ressurss meeskonnast ja asendatakse nimega ressursiga. Vahekaardil **Ajakava** eemaldatakse üldise ressursi määramised ja asendatakse nimega ressursiga.

  > [!NOTE]
  > See käitumine ilmneb ainult siis, kui nimega ressurss on täielikult broneeritud üldise ressursinõude jaoks. Kui nimega ressurss asendab osaliselt üldise ressursinõude või mitu nimega ressurssi asendavad üldise ressursinõude, on üldine ressursinõue endiselt tööülesandele määratud.

Rakendus Project Operations ei määra tööülesandele mõlemat ressurssi, kuna see käitumine tekitaks vähem prognoositavat ajakava. Selles lihtsas näites on lihtne jagada tunde kahe ressursi vahel võrdselt. Kuid keerukamate stsenaariumide korral, mis hõlmavad mitut tööülesannet ja mitut ressurssi, peab PSA tegema oletusi selle kohta, kuidas see peaks jaotama reserveeringud, mis on saadud mitme ressursi jaoks üle mitme toimingu.

Seega on neil juhtudel projektijuht vastutav mitme broneeringu sõelumise ja vajaduse korral määramise eest. Broneeringute eraldamiseks määrab projektijuht tööülesanded üldistest ressurssidest nimega ressurssideks ja kasutab seejärel **vastavusseviimise** vaadet, et veenduda, kas eraldus töötab broneeringutega.

### <a name="edit-a-resource-requirement"></a>Ressursinõude redigeerimine

Pärast seda, kui ressursinõue on loodud, võib projektijuht või ressursihaldur soovida redigeerida üksikasju, et täiustada otsingukriteeriumide järgimist ajakavapaneeli kasutamisel. Ressursinõude redigeerimiseks toimige järgmiselt.

1. Valige vormil **Projektid** vahekaardil **Meeskond** mis tahes üldise ressursi nõude link.
2. Sisestage kuvataval vormil **Ressursinõue** vajalik välja teave

   Vormil **Ressursinõue** saab projektijuht või ressursihaldur määratleda ka oskusi, rolle, ressursi eelistusi ja eelistatud organisatsiooni üksust.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Pärast projekti broneerimist ressursi reserveeringute värskendamine

Pärast üldise või nimega ressursi lisamist projekti meeskonda saate ressursi reserveeringuid muuta.

1. Valige meeskonnaliige vormil **Projektid** vahekaardil **Meeskond** ja seejärel **Halda broneeringuid**.
 
   Ilmub ajakavapaneel ja kuvatakse projekti meeskonnaliikme broneeringud. Laiendage meeskonnaliikme kirjet, et vaadata selle projekti ja muude meeskonnaliikme võimsust tarbivate projektide suhtes broneeritud tunde.

2. Valige ja pukseerige broneering, et seda pikendada või lühendada. Kuvatakse dialoogiboks **Ressursi reserveeringu loomine**, mis võimaldab teil reserveeringut muuta.
3. Tehke broneeringul paremklõps. Seejärel saate kasutada otseteemenüüd järgmiste toimingute lõpuleviimiseks.

    - Broneeringu oleku muutmine
    - Broneeringu redigeerimine
    - Asendage ressurss projekti meeskonnas

### <a name="change-the-booking-status"></a>Broneeringu oleku muutmine

Saate muuta mis tahes vaike- või kohandatud broneeringu olekut.

Project Operationsis on järgmised olekud.

- **Tühistatud**: tühistab ressursi reserveeringu ja vabastab ressursi võimsuse.
- **Fikseeritud broneering**: tarbib ressrursivõimsus. Broneerimisel on tavaliselt see olek, kui avate vormil **Projektid** ruudustikust **Kõik meeskonnaliikmed** valiku **Halda broneeringuid**.
- **Esialgne reserveerimine**: lisab ressursi meeskonnale, kuid ei tarbi ressursi võimsust. See olek näitab, et ressurss on reserveeritud potentsiaalsele tööle, kuid sellel on siiski vaba aega, kui seda on vaja teistel töödel. Ressursside üldise kättesaadavuse vaates on esialgsetes reserveeringutes teistsugune olek kui fikseeritud reserveeringutes.
- **Pakutud**: esindab ressursihalduri või projektijuhi ressursi ettepanekut. Ettepanekud ei tarbi ressursi võimsust ja ressurssi ei lisata projekti meeskonda. Ressursi fikseeritult reserveerimiseks meeskonda, peab projektijuht ettepaneku vastu võtma.

### <a name="submit-resource-requests"></a>Ressursitaotluste esitamine

Ressursi taotlusi kasutatakse nõudluse või ressursinõude täitmiseks, mille peab täitma ressursihaldur. Üldise ressursi jaoks, mis on juba meeskonnas, saate esitada ressursi taotluse otse. Ressursi taotluse saab täita kahel viisil.

- Ressursihaldur täidab taotluse otse. Sellisel juhul asendatakse üldine ressurss fikseeritud reserveeringuga, millel on nimega ressurss.
- Ressursihaldur soovitab ressursi projektijuhile ja projektijuht kinnitab või hülgab pakutud ressursi.

#### <a name="direct-fulfillment-of-resource-requests"></a>Ressursi taotluse otsene täitmine

Ressursinõude loomise ajal saab projektijudt esitada üldisele ressursile ressursitaotluse, valides ressursi ja valides seejärel suvandi **Esita taotlus**. Ressursi kohta leiate teavet selle ressursihaldurilt, kes seda taotlust täidab. Pärast taotluse esitamist muudetakse meeskonnaliikme väli **Olek** väärtusele **Esitatud**. Kui ressursihaldur vastab taotlusele, asendatakse üldine meeskonnaliige nimega ressursiga ruudustikus **Kõik meeskonnaliikmed**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Ressursi soovituse kasutamine ressursi taotlemisel

Ressursi taotlusele ressursi otse broneerimise asemel saab ressursihaldur soovitada ressurssi projektijuhile. Ressursihaldur võib seda suvandit kasutada juhul, kui nõuete täpne vaste pole saadaval. Kui ressursihaldur pakub ressurssi, näeb projektijuht, et üldise meeskonnaliikme väli **Olek** on muudetud väärtusele **Vaja läbivaatamist**.

Saate vaadata pakutud ressurssi koos ettepaneku broneerimise mõju visualiseerimisega. 

1. Topeltklõpsake meeskonnaliikmel, kelle olek on **Vajab läbivaatust**. 
2. Valige vahekaart **Pakutavad ressursid**.
3. Valige **Aktsepteeri kõik ettepanekud**, et nõustuda kõigi pakutud ressurssidega või **Hülga kõik ettepanekud** nende tagasilükkamiseks. Kui nõustute pakutavate ressurssidega, on nad projektis meeskonnaliikmena fikseeritult reserveeritud ja asendavad üldiseid ressursse.

> [!NOTE]
> Kõik pakutavad ressursid tuleb kas aktsepteerida või hüljata. Neid ei saa osaliselt aktsepteerida või hüljata.

### <a name="substitute-a-resource-on-the-project-team"></a>Asendage ressurss projekti meeskonnas

Vahel peab projektijuht asendama projektid broneeritud meeskonnaliikme.

1. Valige vormil **Projektid** vahekaardil **Meeskond** soovitud ressurss, mis vajab asendamist, ja seejärel valige käsk **Halda reserveeringuid**.
2. Laiendage ressurssi, et kuvada neile määratud projekte.
3. Paremklõpsake projekti ja seejärel valige käsk **Asenda ressurss**.
4. Kui teate ressurssi, millega soovite praeguse ressursi asendada, valige või tippige nimi ja seejärel valige **Määra uuesti**.

Või. kui peate ressurssi otsima, tehke järgmist.

1. Valige **Leia asendus**.

   Ajakava abimees tagastab saadaolevate asendajate loendi. Ajakava abimehes saate kättesaadavaid ressursse täiendavalt filtreerida sobiva asenduse leidmiseks.

2. Ressursi asendamiseks valige ressurss, mida te soovite, ja seejärel valige **Asenda**.   

   Broneeringud ja määramised asendatakse uue ressursiga.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Meeskonnaliikmete broneeringute ja määramiste vastavusse viimine

Meeskonnaliikmete puhul on broneeringud ja tööülesanded lõdvalt ühendatud. Teisisõnu, ressurssidel võivad olla määramised, kuid ei mingeid broneeringuid, või neil võib olla broneeringuid, kuid mitte määramisi. Ideaalis tuleks reserveeringud ja ülesanded viia vastavusse, nii et ressursid on toime pannud võimsuse täitmiseks tööülesandeid. Kuid broneeringud võivad põhineda saadavusel ja tööülesande ajastused võivad projekti jätkudes muutuda. Seega pakub broneeringute ja ülesannete vaba ühendamine paindlikkust.

Rakenduses Project Operations on vahekaart **Vastavusseviimine**, mis võimaldab projektijuhtidel ühitada meeskonnaliikmete reserveeringud ja nende määramised projekti meeskondadele.

Vahekaardil **Vastavusseviimine** on kuvatud reserveeringud ja ülesanded, mis on seotud iga meeskonnaliikme tööülesande määramise tasemega. See näitab tunde lahtrites, mis esindavad ajavahemikke kuude ja päevade kaupa.

Vahekaardil kuvatakse ka projekti üldine neto kogusumma koos veeruga kokku.

Iga ressursi puhul arvutab vahekaart meeskonnaliikme reserveeringute ja meeskonnaliikme tööülesannete määramise vahe. Ideaalis peaks see erinevus olema 0 (null). Teisisõnu ei tohiks broneeringute ja ülesannete vahel olla vahet. Erinevused on värvitud ja varjutatud, et juhtida tähelepanu kahele tingimusele.

- **Broneeringu puudujääk**: ilmneb siis, kui ressursil on rohkem määramisi kui broneeringuid. Kuna seda võimsust pole reserveeritud, võib projektijuht soovida selle tingimuse parandamist, pikendades ressursi reserveeringud puudujäägi katteks.
- **Liigsed broneeringud**: ilmnevad, kui ressurss on projektile broneeritud, kuid seda pole ülesannetele määratud. See tingimus võib olla vastuvõetav juhul, kui ressurss oli projektile broneeritud enne tööülesande määramise toimumist. Kuid teistel juhtudel ressurssi ei kavandata tööülesannetele määrata. Sellisel juhul peaks projektijuht kaaluma ressursi broneeringute tühistamist, et võimsust saaks kasutada mõne muu projekti jaoks.

Mõnel juhul, kui te vaatate aega kõrgemal tasemel kui päeva tasemel (näiteks kuu tasand), võidakse kuvada ressursi neto erinevus. Teisisõnu broneerimine = määramine. Kuid kui te vaatate aega nädala tasemel, võite näha, et seal on määramised null tundi ja broneeringud 40 tundi esimesel nädalal, kuid määramine 40 tundi ja broneerimine null tundi teisel nädalal. Kokkuvõttes lepitakse reserveeringud ja määramised kokku, kuid nad erinevad ühe nädala jooksul järgmisena.

Kui vaatate aega kõrgemal tasemel, on vahekaardil **Vastavusseviimine** määratud lahtrite indikaator, mis teatab, et madalamatel tasanditel on erinevusi. Erinevuse vaatamiseks topeltklõpsake lahtril, et sisse suumida. Seejärel saate väljasuumimiseks teha paremklõpsu. Valides ressursi ja valides seejärel ruudustiku tööriistaribal **Järgmine erinevus**, saate minna järgmisele erinevusele selle ressursi reserveeringute ja ülesannete vahel. Tagasi liikumiseks valige suvand **Eelmine erinevus**. Samuti saate suvandi **Sätted** kaudu erinevuste indikaatori ja navigeerimise käitumise välja lülitada.

Kui teil on ressursi jaoks tööülesanded, kuid ei ühtegi broneeringut, valige vormi **Projektid** vahekaardil **Vastavusseviimine** broneeringu puudujääk, seejärel valige käsk **Pikenda reserveeringut**. Kuvatakse dialoogiboks **Pikenda reserveeringut** ja kuvatakse broneering, mis on vajalik ressursi puudujäägi lahendamiseks. Dialoogiboks näitab ka ressursi olemasolevaid broneeringuid kõigis projektides või muudes kavandatud üksustes. Kui valite ressursi reserveeringu loomiseks valiku **OK**, võite selle ressursi saadavusest olenemata põhjustada ülebroneeringu.

Projektijuht või ressursihaldur saab seejärel kasutada ajakavapaneeli, et hallata mis tahes olukordi, kus ressurss on üle broneeritud.
