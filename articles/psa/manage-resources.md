---
title: Halda ressursse
description: Selles teemas antakse teavet ressursside haldamise kohta.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 548595e3951f824e1c79a641d3f336e381fcaaf9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132328"
---
# <a name="manage-resources"></a>Halda ressursse

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation sisaldab ressursihalduri armatuurlauda, mis pakub visuaalset ülevaadet ressursi nõudlusest ja kasutamisest kogu ettevõttes. Armatuurlaua diagramme saate kasutada järgmise teabe visualiseerimiseks.

- **Ressursi nõudlus** – **aktiivse ressursi taotluse** diagramm kuvab edastatud ressursid. Ressursid on koondatud kas rolli või projekti kaudu.
- **Esitamata ressursi nõudmised** – **määramata ressursi nõudluse** diagramm näitab kõiki ressursinõudeid, mida pole veel esitatud. See aitab ressursihalduril vaadata nõudlust, mis pole kindel ja mida võidakse esitada ressursitaotluse kaudu.
- **Viimase nädala tasustatav kasutamine** – **kasutuse roll** diagrammil näitab organisatsiooni tegeliku arvete kasutamise protsenti rolli poolt, mis on seotud selle sihtmärgiga.

    > [!NOTE]
    > Selleks et teha **kasutuse rolli** diagramm saadavaks, looge töövoogu UpdateRoleUtilization käivitav töö. Seda korduvat tööd käitatakse iga seitsme päeva järel, et arvutada viimase seitsme päeva jooksul tasustatav kasutamine. Tulemused on koondatud rolli järgi.

## <a name="manage-project-team-members"></a>Projekti meeskonnaliikmete haldamine

Projekti haldurid saavad kasutada ressursi halduri armatuurlauda, et hallata projektide ressursse. Näiteks saavad nad lisada meeskonnaliikme otse projekti ja broneerida meeskonnaliikme, kes vastab üldise ressursi kogutud ressursinõuetele.

### <a name="add-a-team-member-directly-to-a-project"></a>Meeskonnaliikme lisamine otse projektile

Meeskonnaliikme lisamiseks otse projektile valige lehel **Projektid** vahekaardil **Meeskond** suvand **Uus**. Kuvatakse dialoogiboks **Kiirloomine: projekti meeskonnaliige**. Selles dialoogiboksis saate teha järgmisi toiminguid.

- **Broneerige nimega ressurss** – valige väljal **Broneeritav ressurss** ressursi nimi. Seejärel valige roll, määrake periood ja valige jaotamise meetod. Teie valitud nimega ressurss lisatakse projektile valitud jaotamise meetodi ja ressursside kalendri abil.
- **Üldise ressursi lisamine** – jätke **Reserveeritava ressursi** väli tühjaks ja valige seejärel roll, määrake periood ja valige soovitud jaotuse meetod. Üldine ressurss lisatakse meeskonda kohatäitena, et talletada nõudluse mudelit, mida kasutatakse meeskonnas nimega ressursside broneerimiseks. Nõue esitatakse vastavalt projekti kalendrile.
- **Nimega ressursi lisamine meeskonnale, rakendamata ressursi võimsust** – valige väljal **Broneeritav ressurss** ressurss. Seejärel valige periood ja valige jaotamise meetodiks **Puudub**. Ressurss lisatakse meeskonda, kuid ressursi võimsust ei tarbita broneerimise kaudu.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Reserveerige meeskonnaliige, et täita ressursinõudeid üldise ressursi jaoks

Rakenduses PSA saate broneerida üldise ressursi projekti meeskonnas ning määrata rolli, nõutava võimsuse ja võimsuse jaotamise viisi. Ressursinõudes saate määrata üldiste ressurssidega seotud atribuudid. Need atribuudid hõlmavad nõutavaid oskusi, eelistatud organisatsiooniüksust ja eelistatud ressursse.

Järgige neid juhiseid, et määrata arendaja jaoks üldise ressursi nõutavad oskused.

1. Valige lehel **Projektid** vahekaardil **Meeskond** käsk **Uus**, et broneerida üldine ressurss.

    ![Meeskonnas broneeritud üldine ressurss](media/Resource-Management-image9.png)

2. Valige vaates **Kõik meeskonnaliikmed** veerus **Ressursinõue** vastav link, et lisada üldisele ressursile nõutavad oskused.

    ![Nõude link](media/Resource-Management-image10.png)

3. Valige lehel **Ressursinõue**, mis kuvatakse **oskuste** ruudustikus, kolmikpunkt (**…**) ja seejärel valige **Lisa uus nõude omadus**, et lisada arendajale vajalikke oskusi.

    ![Uue nõude tunnuse käsu lisamine](media/Resource-Management-image11.png)

4. Valige dialoogiboksis **Kiirloomine: nõude tunnused** väljal **Tunnused** soovitud oskus. Seejärel valige väljal **Hinnangu väärtus** selle oskuse jaoks oskuse tase. Lõpuks määrake väljal **Ressursinõue** nõue, et ressursid pärineks organisatsiooniüksustest või isegi nimega ressurssidest. Kui olete lõpetanud, valige **Save**.

    ![Kiirloomine: dialoogiboks Nõude tunnus](media/Resource-Management-image12.png)

5. Valige lehel **Ressursinõue** käsk **Broneeri**, et täita ressursinõue.

    ![Nupp Broneeri lehel Ressursinõue](media/Resource-Management-image13.png)

    Saate valida üldise ressursi ka ruudustikus **Kõik meeskonnaliikmed** ja seejärel valige **Reserveeri**.

    ![Nupp Broneeri kõigi meeskonnaliikmete ruudustiku kohal](media/Resource-Management-image14.png)

    > [!NOTE]
    > Selles näites on 40 nõutavat tundi, kuid tegelikke broneeritud tunde ei kuvata, kuna üldistel ressurssidel pole reserveeringuid. Lisaks pole määratud tunde, kuna üldine ressurss lisati otse meeskonnale. Seda ei lisatud tööülesande määramise abil.

    Lehel **Plaanimisabimees** saate saadaolevaid ressursse filtreerida ressursinõudes määratud nõuete järgi. Ressursid sorditakse vastavalt ajakavapaneelil määratud sortimise parameetritele.

    ![Ajakavaabilise leht](media/Resource-Management-image15.png)

    Siin on mõned filtrid, mida kasutatakse sageli.

    - **Tunnused koos hinnanguga** – filtreerimine oskuste, sertifitseerimise ja muude ressursside omaduste alusel ning lisaks oskustaseme alusel.
    - **Rollid** – filtreeritakse vaikimisi kasutatavate rollide järgi, mis on määratud broneeritud ressurssidele.
    - **Organisatsiooniüksused** – filtreerige arvestuslikke ressursse nende organisatsiooniüksuste järgi, kellele nad on määratud.

6. Kui te pole algse nõude otsingu tulemustega rahul, saate filtri kriteeriume muuta. Laiendage vasakul olevat paani **Filtri vaade** ja seejärel valige **Otsi**, et leida täiendavaid ressursse.

    ![Filtri vaate paan](media/Resource-Management-image16.png)

7. Tulemuste sortimise muutmiseks valige **Sordi**.

    ![Sortimise käsk](media/Resource-Management-image17.png)

8. Valige ressursid vastavalt vajadusele määratud nõudmisele, nagu on näidatud ruudustiku ülaosas. Saate tühjendada koordinaatvõrgus olevate lahtrite valiku ja jätta selle ressursi võimsuse avatuks. Korraga saab valida ainult ühe ressursi.

9. Valige ressursi broneerimiseks **Broneeri** ja jätke ajakavapaneel avatuks, et saaksite valida täiendavad ressursid. Võite ka valitud ressursi broneerimiseks ja ajakavapaneeli sulgemiseks valida **Broneeri ja välju**.

    ![Ressursi reserveerimine](media/Resource-Management-image19.png)

    Teile kuvatakse teade broneeritud tundide kohta. Nõudluse indikaatorid näitavad, kui palju broneerimisnõudeid on vaja täita ja kui palju on jäänud. Samuti saate vaadata, kui palju valitud ressursi võimsust tarbitakse. Ressursi reserveeringute üksikasjade vaatamiseks valige **Laienda**.

9. Naaske vaatesse **Kõik meeskonnaliikmed**. Pange tähele, et üldine ressurss on asendatud nimega ressursiga ja 40 tundi on reserveeritud selle ressursi jaoks.

    ![Värskendatud kõigi meeskonnaliikmete ruudustik](media/Resource-Management-image20.png)

    > [!NOTE]
    > Määratud tunde ei kuvata, kuna nad on otse meeskonnas broneeritud. Neid ei broneeritud tööülesande määramise abil.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Üldiste ressursside määramine tööülesannetele ja ressursinõuete loomine

Rakenduses PSA saate luua tööülesandeid ja määrata neile üldiseid ressursse. Sel viisil saab ressursi nõudluse esitada kohatäitena, kui hindate oma ajakava ja finantsnumbreid. Seejärel saate luua ressursinõudeid üldistele ressurssidele ja need täita.

1. Tööülesande loomiseks valige lehel **Projektid** vahekaardil **Ajakava** **Lisa**.

    ![Uus tööülesanne loodud](media/Resource-Management-image21.png)

2. Valige väljal **Ressursid** sümbol **Ressursivalija**. Kuvatakse ressursivalija, mis kuvab projekti jaoks olemasolevad meeskonnaliikmed.

    ![Ressursivalija](media/Resource-Management-image22.png)

3. Sisestage uue üldise ressursi nimi ja seejärel valige **Loo**.

    ![Sisestatud uue üldise ressursi nimi](media/Resource-Management-image23.png)

4. Valige kuvatavas dialoogiboksis **Kiirloomine: projekti meeskonnaliikmed** väljal **Roll** üldisele ressursile roll. Valige väljalt **Ressursiühik** üldisele ressursile organisatsiooniüksus. Seejärel tehke valik **Salvesta**.

    ![Kiirloomine: dialoogiboks Projekti meeskonnaliige](media/Resource-Management-image24.png)

    Üldine meeskonnaliige on nüüd ülesandele määratud.

    ![Ülesandele määratud üldine meeskonnaliige](media/Resource-Management-image25.png)

    Vahekaardil **Meeskond** kuvatakse uus üldine meeskonnaliige. Pange tähele, et sel on määratud ainult tunde. Need tunnid on kõigi üldiste meeskonnaliikmete jaoks määratud ülesannete summa. Üldisel meeskonnaliikmel pole veel nõutavaid tunde või ressursinõuet.

    ![Üldine meeskonnaliige vahekaardil Meeskond](media/Resource-Management-image26.png)

5. Nüüd saate määrata üldise meeskonnaliikme teistele ülesannetele, kasutades ressursivalijat.

    ![Üldine meeskonnaliige ressursivalijas](media/Resource-Management-image27.png)

    Kui olete üldise ressursi määramise ülesannetele lõpetanud, saate luua ressursinõude üldise ressursi jaoks.

5. Valige vahekaardil **Meeskond** üldine ressurss ja seejärel valige **Loo nõue**.

    ![Käsk Loo nõue](media/Resource-Management-image28.png)

    Kui nõue luuakse, on üldisel meeskonnaliikmel nõutavad tunnid ja link ressursinõudele.

    ![Ressursinõude link](media/Resource-Management-image29.png)

    Pärast nimega ressursi broneerimist eemaldatakse üldine ressurss meeskonnast ja asendatakse nimega ressursiga.

    ![Üldine ressurss on asendatud nimega ressursiga](media/Resource-Management-image30.png)

    Vahekaardil **Ajakava** eemaldatakse üldise ressursi määramised ja asendatakse nimega ressursiga.

    ![Vahekaardil Ajakava üldise ressursi määramised asendatud nimega ressursiga](media/Resource-Management-image31.png)

    > [!NOTE]
    > See käitumine ilmneb ainult siis, kui nimega ressurss on täielikult broneeritud üldise ressursinõude jaoks. Kui nimega ressurss asendab osaliselt üldise ressursinõude või mitu nimega ressurssi asendavad üldise ressursinõude, on üldine ressursinõue endiselt tööülesandele määratud.

    Järgmisel illustratsioonil on 80-tunnise tööülesande kestuseks planeeritud viis päeva (16 tundi päevas üle viie päeva) ja määratud üldisele ressursile, mille nimi on **Funktsionaalne**.

    ![80-Tunnine, viiepäevane ülesanne, mis on määratud funktsionaalsele üldisele ressursile](media/Resource-Management-image32.png)

    Nõude genereerimisel on see 80 tundi viie päeva jooksul.

    ![Nõue, mis on loodud 80 tunniks viie päeva jooksul](media/Resource-Management-image33.png)

    Kuna saadaolevad ressursid töötavad ainult kaheksa tundi päevas, on nõude täitmiseks vaja kahte ressurssi.

    ![Teine ressurss](media/Resource-Management-image35.png)

    Vahekaardil **Meeskond** saate nüüd vaadata, et üldisel ressursil pole nõutavaid tunde, kuid määratud tunnid kuvatakse endiselt koos kahe nimega ressursiga, mis moodustavad täitmise.

    ![Kaks nimega ressurssi vahekaardil Meeskond](media/Resource-Management-image36.png)

    Vahekaardil **Ajakava** on üldine ressurss endiselt tööülesande jaoks määratud.

    ![Üldised ressursid vahekaardil Ajakava](media/Resource-Management-image37.png)

PSA ei määra tööülesandele mõlemat ressurssi, kuna see käitumine tekitaks vähem prognoositavat ajakava. Selles lihtsas näites on lihtne jagada tunde kahe ressursi vahel võrdselt. Kuid keerukamate stsenaariumide korral, mis hõlmavad mitut tööülesannet ja mitut ressurssi, peab PSA tegema oletusi selle kohta, kuidas see peaks jaotama reserveeringud, mis on saadud mitme ressursi jaoks üle mitme toimingu.

Seega on neil juhtudel projektijuht vastutav mitme broneeringu sõelumise ja vajaduse korral määramise eest. Broneeringute eraldamiseks määrab projektijuht tööülesanded üldistest ressurssidest nimega ressurssideks ja kasutab seejärel **vastavusseviimise** vaadet, et veenduda, kas eraldus töötab broneeringutega.

### <a name="edit-a-resource-requirement"></a>Ressursinõude redigeerimine

Pärast seda, kui ressursinõue on loodud, võib projektijuht või ressursihaldur soovida redigeerida üksikasju, et täiustada otsingukriteeriumide järgimist ajakavapaneeli kasutamisel. Ressursinõude redigeerimiseks toimige järgmiselt.

1. Valige lehel **Projektid** vahekaardil **Meeskond** mis tahes üldise ressursi nõude link.
2. Kuvataval **Ressursinõude** lehel saate värskendada mitut atribuuti. Järgmiselt on toodud mõned näited.

    - Nimi
    - Kuupäevast
    - Lõppkuupäev
    - Kestus
    - Ressursi tüüp

**Ressursinõude** lehel saab projektijuht või ressursihaldur määratleda ka järgmise teabe.

- Oskused
- Rollid
- Ressursieelistused
- Eelistatud organisatsiooniüksus

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Pärast projekti broneerimist ressursi reserveeringute värskendamine

Pärast üldise või nimega ressursi lisamist projekti meeskonda saate ressursi reserveeringuid muuta.

1. Valige meeskonnaliige lehel **Projektid** vahekaardil **Meeskond** ja seejärel **Halda broneeringuid**.

    ![Valitud meeskonnaliikme jaoks avatud ajakavapaneel](media/Resource-Management-image40.png)

    Ilmub ajakavapaneel ja kuvatakse projekti meeskonnaliikme broneeringud. Laiendage meeskonnaliikme kirjet, et vaadata selle projekti ja muude meeskonnaliikme võimsust tarbivate projektide suhtes broneeritud tunde.

2. Valige ja pukseerige broneering, et seda pikendada või lühendada. Kuvatakse dialoogiboks **Ressursi reserveeringu loomine**, mis võimaldab teil reserveeringut muuta.

    ![Ressursi reserveeringu loomine](media/Resource-Management-image41.png)

3. Tehke broneeringul paremklõps. Seejärel saate kasutada otseteemenüüd järgmiste toimingute lõpuleviimiseks.

    - Muutke broneeringu olekut.
    - Redigeerige broneeringut.
    - Asendage ressurss projekti meeskonnas.

### <a name="change-the-booking-status"></a>Broneeringu oleku muutmine

Saate muuta mis tahes vaike- või kohandatud broneeringu olekut.

![Käsk Muuda olekut](media/Resource-Management-image42.png)

PSA-s on järgmised olekud

- **Tühistatud** – see olek tühistab ressursi reserveeringu ja vabastab ressursi võimsuse.
- **Fikseeritud reserveering** – see olek kasutab ressursi võimsust. Broneerimisel on tavaliselt see olek, kui avate lehel **Projektid** ruudustikust **Kõik meeskonnaliikmed** valiku **Halda broneeringuid**.
- **Esialgne reserveerimine** – see olek lisab ressursi meeskonnale, kuid ei tarbi ressursi võimsust. See näitab, et ressurss on reserveeritud potentsiaalsele tööle, kuid sellel on siiski vaba aega, kui seda on vaja teistel töödel. Ressursside üldise kättesaadavuse vaates on esialgsetes reserveeringutes teistsugune olek kui fikseeritud reserveeringutes.
- **Pakutud** – see olek esindab ressursi juhi või projektijuhi ettepanekut ressursi kohta. Ettepanekud ei tarbi ressursi võimsust ja ressurssi ei lisata projekti meeskonda. Ressursi fikseeritult reserveerimiseks meeskonda, peab projektijuht ettepaneku vastu võtma.

### <a name="submit-resource-requests"></a>Ressursitaotluste esitamine

Ressursi taotlusi kasutatakse nõudluse (ressursinõue) täitmiseks, mille peab täitma ressursihaldur. Üldise ressursi jaoks, mis on juba meeskonnas, saate esitada ressursi taotluse otse. Ressursi taotluse saab täita kahel viisil.

- Ressursihaldur täidab taotluse otse. Sellisel juhul asendatakse üldine ressurss fikseeritud reserveeringuga, millel on nimega ressurss.
- Ressursihaldur soovitab ressursi projektijuhti ja projektijuht kinnitab või hülgab pakutud ressursi.

#### <a name="direct-fulfillment-of-resource-requests"></a>Ressursi taotluse otsene täitmine

Ressursinõude loomisel saab projektijuht esitada ressursi taotluse üldise ressursi jaoks, valides ressursi ja valides seejärel valiku **Esita taotlus**.

![Nupp Taotluse esitamine](media/Resource-Management-image45.png)

Ressursi kohta leiate teavet selle ressursi haldurilt, kes seda taotlust täidab. Pärast taotluse esitamist muudetakse meeskonnaliikme väli **Olek** väärtusele **Esitatud**.

![Valikuliste kommentaaride sisestamine](media/Resource-Management-image46.png)

Kui ressursihaldur vastab taotlusele, asendatakse üldine meeskonnaliige nimega ressursiga ruudustikus **Kõik meeskonnaliikmed**.

![Nimega ressursiga asendatud üldine meeskonnaliige ruudustikus Kõik meeskonnaliikmed](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Ressursi soovituse kasutamine ressursi taotlemisel

Ressursi taotlusele ressursi otse broneerimise asemel, saab ressursihaldur teha ressursi ettepaneku projekti juhile. Ressursihaldur võib seda suvandit kasutada juhul, kui nõuete täpne vaste pole saadaval. Kui ressursihaldur pakub ressurssi, näeb projektijuht, et üldise meeskonnaliikme väli **Olek** on muudetud väärtusele **Vaja läbivaatamist**.

![Üldise meeskonnaliikme olek muudetud väärtusele Vaja läbivaatamist](media/Resource-Management-image48.png)

Kui soovite vaadata pakutud ressurssi koos soovituse reserveeringu efektiga, topeltklõpsake meeskonnaliiget, kellel on olek **Vaja läbivaatamist**. Seejärel valige vahekaart **Pakutavad ressursid**.

![Pakutavad ressursid](media/Resource-Management-image49.png)

Valige **Aktsepteeri kõik ettepanekud**, et nõustuda kõigi pakutud ressurssidega või **Hülga kõik ettepanekud** nende tagasilükkamiseks. Kui nõustute pakutavate ressurssidega, on nad projektis meeskonnaliikmena fikseeritult reserveeritud ja asendavad üldiseid ressursse.

> [!NOTE]
> Kõik pakutavad ressursid tuleb kas aktsepteerida või hüljata. Neid ei saa osaliselt aktsepteerida või hüljata.

### <a name="substitute-a-resource-on-the-project-team"></a>Asendage ressurss projekti meeskonnas

Vahel peab projektijuht asendama broneeritud meeskonnaliikme projektis.

1. Valige lehel **Projektid** vahekaardil **Meeskond** soovitud ressurss, mis vajab asendamist, ja seejärel valige käsk **Halda reserveeringud**.
2. Laiendage ressurssi, et kuvada neile määratud projekte.

    ![Ressurss on laiendatud, et kuvada määratud projekte](media/Resource-Management-image50.png)

3. Paremklõpsake projekti ja seejärel valige käsk **Asenda ressurss**.
4. Kui teate ressurssi, mida soovite praeguse ressursi jaoks asendada, valige või tippige nimi ja seejärel valige **Uuesti määramine**.

    ![Asendava ressursi määramine](media/Resource-Management-image51.png)

    Ressursi otsimiseks tehke ka järgmist.

    1. Valige **Leia asendus**.

        ![Asendava ressursi otsimine](media/Resource-Management-image52.png)

        Ajakava abimees tagastab saadaolevate asendajate loendi. Ajakava abimehes saate kättesaadavaid ressursse täiendavalt filtreerida sobiva asenduse leidmiseks.

        ![Saadaolevate näidiste loend](media/Resource-Management-image53.png)

    2. Ressursi asendamiseks valige ressurss, mida te soovite, ja seejärel valige **Asenda**.

        ![Asendusressurss valitud](media/Resource-Management-image54.png)

    Broneeringud ja määramised asendatakse uue ressursiga.

    ![Broneeringud ja määramised asendatakse uue ressursiga](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Meeskonnaliikmete broneeringute ja määramiste vastavusse viimine

Meeskonnaliikmete puhul on broneeringud ja tööülesanded lõdvalt ühendatud. Teisisõnu, ressurssidel võivad olla määramised, kuid ei mingeid broneeringuid, või neil võib olla broneeringuid, kuid mitte määramisi. Ideaalis tuleks reserveeringud ja ülesanded viia vastavusse, nii et ressursid on toime pannud võimsuse täitmiseks tööülesandeid. Kuid broneeringud võivad põhineda saadavusel ja tööülesande ajastused võivad projekti jätkudes muutuda. Seega pakub broneeringute ja ülesannete vaba ühendamine paindlikkust.

PSA-l on vahekaart **Vastavusseviimine**, mis võimaldab projekti juhtidel ühitada meeskonnaliikmete reserveeringud ja nende määramised projekti meeskondadele.

![Vahekaart Vastavusseviimine](media/Resource-Management-image56.png)

Vahekaardil **Vastavusseviimine** on kuvatud reserveeringud ja ülesanded, mis on seotud iga meeskonnaliikme tööülesande määramise tasemega. See näitab tunde lahtrites, mis esindavad ajavahemikke kuude ja päevade kaupa.

Vahekaardil kuvatakse ka projekti üldine neto kogusumma koos veeruga kokku.

Iga ressursi puhul arvutab vahekaart meeskonnaliikme reserveeringute ja meeskonnaliikme tööülesannete määramise vahe. Ideaalis peaks see erinevus olema 0 (null). Teisisõnu ei tohiks broneeringute ja ülesannete vahel olla vahet. Erinevused on värvitud ja varjutatud, et juhtida tähelepanu kahele tingimusele.

- **Broneeringu puudujääk** – broneeringu puudujääk ilmneb siis, kui ressursil on rohkem määramisi kui broneeringuid. Kuna seda võimsust pole reserveeritud, võib projektijuht soovida selle tingimuse parandamist, pikendades ressursi reserveeringud puudujäägi katteks.
- **Liigsed broneeringud** – üleliigsed broneeringud ilmnevad, kui ressurss on projektile broneeritud, kuid seda pole ülesannetele määratud. See tingimus võib olla vastuvõetav juhul, kui ressurss oli projektile broneeritud enne tööülesande määramise toimumist. Kuid teistel juhtudel ressurssi ei kavandata tööülesannetele määrata. Sellisel juhul peaks projektijuht kaaluma ressursi broneeringute tühistamist, et võimsust saaks kasutada mõne muu projekti jaoks.

Mõnel juhul, kui te vaatate aega kõrgemal tasemel kui päeva tasemel (näiteks kuu tasand), võidakse kuvada ressursi neto erinevus (teisisõnu, broneerimine = määramine). Kuid kui te vaatate aega nädala tasemel, võite näha, et seal on määramised null tundi ja broneeringud 40 tundi esimesel nädalal, kuid määramine 40 tundi ja broneerimine null tundi teisel nädalal. Kokkuvõttes lepitakse reserveeringud ja määramised kokku, kuid nad erinevad ühe nädala jooksul järgmisena.

Kui vaatate aega kõrgemal tasemel, on vahekaardil **Vastavusseviimine** määratud lahtrite indikaator, mis teatab, et madalamatel tasanditel on erinevusi. Lahtrit topeltklõpsates saate erinevuse vaatamiseks suumida. Seejärel saate väljasuumimiseks paremklõpsu teha. Valides ressursi ja kasutades seejärel ruudustiku tööriistaribal juhtelementi **Järgmine erinevus**, saate minna järgmisele erinevusele selle ressursi reserveeringute ja ülesannete vahel. Seejärel saate tagasiminemiseks kasutada juhtelementi **Eelmine erinevus**. Samuti saate suvandi **Sätted** kaudu erinevuste indikaatori ja navigeerimise käitumise välja lülitada.

![Erinevuse indikaator](media/Resource-Management-image57.png)

Kui teil on ressursi jaoks tööülesanded, kuid ei mingeid broneeringuid,valige lehel **Projektid** vahekaardil **Vastavusseviimine** broneeringu puudujääk, seejärel valige käsk **Pikenda reserveeringut**. Kuvatakse dialoogiboks **Pikenda reserveeringut** ja kuvatakse broneering, mis on vajalik ressursi puudujäägi lahendamiseks. See näitab ka ressursi olemasolevaid broneeringuid kõigis projektides või muudes kavandatud üksustes. Kui valite ressursi reserveeringu loomiseks valiku **OK**, võite selle ressursi saadavusest olenemata põhjustada ülebroneeringu.

![Dialoogiboks Pikenda reserveeringut](media/Resource-Management-image58.png)

Projektijuht või ressursihaldur saab seejärel kasutada ajakavapaneeli, et hallata mis tahes olukordi, kus ressurss on üle broneeritud.
