---
title: Projektilepingud
description: Selles teemas on toodud näited projektilepingutest, mida saate luua erinevat tüüpi projektide ja rahastamisallikate jaoks, ning seda, kuidas saate hallata lepinguid ja klientide arveprojekte.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7d15523f1b22bb8813a47f9f822f12bc4162104
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075087"
---
# <a name="project-contracts"></a>Projektilepingud

[!include [banner](../includes/banner.md)]

Selles artiklis on toodud näited projektilepingutest, mida saate luua erinevat tüüpi projektide ja rahastamisallikate jaoks, ning seda, kuidas saate hallata lepinguid ja klientide arveprojekte.

Projektilepingu jaoks loodav projektitüüp määratleb meetodi, mida kasutatakse projekti osas kliendiga arveldamiseks. Projektilepingut ja sellega seotud projekti saab muuta, kuid projektitüüpi ei saa muuta. 

Projektilepingu abil saate korraga arveldada ühe või mitu projekti. Samuti aitab projektileping tagada iga projekti struktuuri jaoks järjepideva arvete esitamise protseduuri. 

Iga arveldatav projekt tuleb seostada projektilepinguga. Projektilepingu sätted rakenduvad kõigile projektilepinguga seotud projektidele ja projektidele. 

Projektilepinguga saab määrata ühe või mitu rahastamisallikat. Seega saate jagada arvete vahel mitu rahastajat, seadistades rahastamise piirid, nii et rahastamisallikatelt ei ole arvestata rohkem kui kindlaksmääratud summa, ja konfigureerida rahastamiseeskirju maksustamise kulude osas.

## <a name="funding-for-project-contracts"></a>Projektilepingute rahastamine
Mõned projektilepingud täpsustavad, et mitu osapoolt jagavad vastutust projekti kulude rahastamise eest. Järgmiselt on toodud mõned näited.

-   Suur klient, kellel on mitu allüksust, nõuab projekti rahastamist allüksuse järgi.
-   Teie ettevõte jagab suure projekti kulusid välise organisatsiooniga.
-   Teede projekti kaasrahastavad kaks omavalitsust.
-   Sillaprojekti rahastab valitsuse toetus ja eraettevõte.

Rakenduses Dynamics 365 Finance saate jagada ühe tehingu või kogu projekti arve mitme kliendi, stipendiumi või organisatsiooni vahel. 

Mitme rahastajaga projektides nimetatakse kõiki osapooli, kes toetavad täiustatud rahastamise projekti rahastamist, rahastamisallikateks. Pärast seda, kui klient, organisatsioon või toetus on määratletud rahastamisallikana, saab selle määrata ühele või mitmele rahastamisreeglile. Rahastamise reeglid sisaldavad kriteeriume, mis määratlevad, kuidas kulud eraldatakse projekti erinevatele rahastamisallikatele. 

Kuna varutud kaupa (nt ostutellimustes ja ostutellimustes kuvatavaid kirjeid) ei saa tükeldada, ei saa kulu summat jagada mitme rahastamisallika vahel. Seega jääb rahastamisallika väärtuseks 0 (null), kuni sisestatakse varude väljaminek. Kui varude väljaminek sisestatakse, jaotatakse kulu summa vastavalt projekti konto jaotamise reeglitele.

Siin on mõned sammud, mida saate teha, et arvete jagamine oleks mitme rahastamisallika vahel hõlpsam.

-   Määrake, et kõik projekti jaoks sisestatud tehingud kasutavad projekti lepinguna sama müügivaluutat.
-   Seadistage rahastamise limiidid, nii et rahastamise allikat ei oleks arveldatud üle teatud summa projekti piires.
-   Konfigureerige iga töötaja, kauba, kategooria, kategooriagrupi ja kandetüübi (või kõigi kandetüübi) jaoks rahastamise reeglid ja rahastamise limiidid.
-   Valige valikuline algus- ja lõppkuupäev, et määratleda periood, millal mingi rahastamise reegel kehtib.
-   Määrake protsent, mille eest iga rahastamisallikas vastutab.
-   Määrake, millist rahastamisallikat rahastatakse saastekvootide eraldamise arvutustest.
-   Seadistage reeglid, mis määratlevad, kuidas projekti kulud arveldatakse välisklientidele ja mille eest tuleb tasuda sisemistele organisatsioonidele.
-   Kirjendage tehingud ootel rahastamiskontol, kuni saate täiendavaid vahendeid või kuni otsustate kulud sisemiselt kanda.

Tehinguga seostamiseks kasutatava maksurühma määratlemiseks otsitakse projekti jaoks maksurühma määramine. Kui projekti tasemel ei ole maksurühma määramist tehtud, otsitakse projekti lepingust.

### <a name="example-multiple-funding-sources-simple"></a>Näide: mitu rahastamisallikat (lihtne)

Järgmises tabelis on toodud stsenaariumid rahastamise jaotamise haldamiseks mitme rahastamisallika vahel. Need stsenaariumid põhinevad järgmistel oletustel.

-   Esmatähtsad sätted arvestatakse rahaliste vahendite eraldamiseni enne muude rahastamise reegli kriteeriumide rakendamist.
-   Ajavahemikke pole määratletud kuupäevavahemiku määratlemiseks, mil rahastamise reegel kehtib, pole kuupäevavahemik määratud.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Stsenaarium</strong></td>
<td><strong>Rahastamise allikas</strong></td>
<td><strong>Jaotamise protsent</strong></td>
<td><strong>Eraldamise prioriteet</strong></td>
</tr>
<tr class="even">
<td>Soovite kulud jaotada ühte rahastamisallikasse seni, kuni rahalised vahendid on ammendatud, eraldage kulud teisele rahastamisallikale seni, kuni rahalised vahendid on ammendatud, ning lõpuks eraldatakse ülejäänud kulud kolmandale rahastamisallikale.</td>
<td><ul>
<li>Rahastamisallikas　1</li>
<li>Rahastamisallikas　2</li>
<li>Rahastamisallikas　3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Soovite eraldada 75 protsenti kuludest ühele rahastamisallikale ja 25 protsenti teisele rahastamisallikale. Kui üks nendest rahastamisallikatest on ammendatud, soovite ülejäänud kulud maksta kolmandast rahastamisallikast.</td>
<td><ul>
<li>Rahastamisallikas　1</li>
<li>Rahastamisallikas　2</li>
<li>Rahastamisallikas　3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Soovite eraldada 75 protsenti kuludest ühele rahastamisallikale ja 25 protsenti teisele rahastamisallikale. Kui üks nendest rahastamisallikatest on ammendatud, soovite ülejäänud kulud jagada kolmanda ja neljanda rahastamisallika vahel.</td>
<td><ul>
<li>Rahastamisallikas　1</li>
<li>Rahastamisallikas　2</li>
<li>Rahastamisallikas　3</li>
<li>Rahastamisallikas　4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Soovite eraldada esimese 25 protsenti kuludest ühele rahastamisallikale ja ülejäänud teisele rahastamisallikale.</td>
<td><ul>
<li>Rahastamisallikas　1</li>
<li>Rahastamisallikas　2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Näide: mitu rahastamisallikat (keeruline)

Teil on kolm rahastamisallikat, mida soovite kasutada järgmises järjestuses.

1.  Kasutage rahastamisallikat 2 ja rahastamisallikat 3 võrdselt, kuni rahastamisallikas 2 on ammendatud.
2.  Jätkake rahastamise allika 3 kasutamist, kuni see on ammendatud.
3.  Kasuta rahastamisallikat 1, kui rahastamisallikas 3 ammendatud.

Selle eesmärgi saavutamiseks peate esmalt tegema järgmist.

-   Seadistage rahastamise piirmäärad, et rahastada allikat 2 ja allikat 3, nende vastavate summade jaoks.
-   Looge järgmine rahastamisreegel.
    -   Reegel 1 (prioriteet 1): eraldada 50 protsenti tehingutest rahastamisallikale 2 ja 50 protsenti rahastamisallikale 3.
    -   Reegel 2 (prioriteet 2): eraldage 100 protsenti tehingutest rahastamisallikale 3.
    -   Reegel 3 (prioriteet 3): eraldage 100 protsenti tehingutest rahastamisallikale 1.

See seadistus töötab, kuna kandeid kontrollitakse reeglite ja piirangute suhtes, et teha kindlaks, kas mõni nendest kannetest rakendub. Kui tehingu suhtes ei kehti mingeid erieeskirju ega piiranguid, rakendub reegel Kõik tehingud. Kõigi reegel Kõik tehingud vastab kõigile tehingutele. 

Kui leitakse reegel, mis vastab tehingule, rakendatakse esmalt selles reeglis eraldatud protsent, kuid alles pärast kõigi seadistatud piirangute kontrollimist. Kui piirmäär on täidetud ja rahastamisallika vahendid on ammendatud, eiratakse rahastamise reeglit, mis on seotud rahastamise limiidiga, ning programm kontrollib järgmist reeglit, mis kehtib. 

Mõnel juhul saab reegli alusel jaotada ainult osa tehingust. See võib juhtuda, kuna tehingu eraldamisel jõutakse limiidini. Sel juhul eraldatakse selle reegli järgi ainult teatud summa, nt 50 protsenti iga rahastamisallika kohta. See kehtib reegli 1 puhul, mida kirjeldatakse käesolevas jaotises varem. Ülejäänu jaotatakse järjekorras järgmise reegli järgi. 

Järgmises tabelis käsitletakse seda stsenaariumi üksikasjalikumalt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fookus</strong></td>
<td><strong>Üksikasjad</strong></td>
</tr>
<tr class="even">
<td>Rahastamise eeskirjad</td>
<td><ul>
<li>Eeskiri 1 (prioriteet 1): kõik tehingud. Eraldage rahastamise allikale 2 50% ja rahastamise allikale 3 50%.</li>
<li>Eeskiri 2 (prioriteet 2): kõik tehingud. Eraldage rahastamisallikale 3 100%.</li>
<li>Eeskiri 3 (prioriteet 2): kõik tehingud. Eraldage rahastamisallikale 1 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rahastamise limiidid</td>
<td><ul>
<li>Rahastamise allikas 1 piir = 10,000.00</li>
<li>Rahastamise allikas 2 piir = 500.00</li>
<li>Rahastamise allika 3 piir = 750.00</li>
</ul></td>
</tr>
<tr class="even">
<td>Kanne 1</td>
<td><strong>Tehingu summa:</strong> 100.00<strong>Rahastamine:</strong> Tehing makstakse vastavalt reeglile 1 ainult seetõttu, et kanne on pärast reegli 1 rakendamist täielikult tasutud. Tehingut rahastatakse võrdselt rahastamisallika 2 ja rahastamisallika 3 vahel.
<ul>
<li>Rahastamisallikas 2: 50.00</li>
<li>Rahastamisallikas 3: 50.00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kanne 2</td>
<td><strong>Tehingu summa:</strong>5 000 00<strong>Rahastamine:</strong> Tehing makstakse vastavalt kõigile kolmele reeglile. <strong>Eeskiri 1</strong>
<ul>
<li>Rahastamisallikas 2: 450.00</li>
<li>Rahastamisallikas 3: 450.00</li>
</ul>
<strong>Eeskiri 2</strong>
<ul>
<li>Rahastamisallikas 3: 250.00 (= 750.00 – 50.00 – 450.00)</li>
</ul>
<strong>Eeskiri 3</strong>
<ul>
<li>Rahastamisallikas 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Iga rahastamisallika jaoks jaotatud rahalised vahendid kokku</td>
<td><ul>
<li>Rahastamisallikas 1: 3,850.00</li>
<li>Rahastamisallikas 2: 500.00</li>
<li>Rahastamisallikas 3: 750.00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Arvete esitamise reeglid
Kui sõlmite kliendiga projektilepingu, saate määratleda, kuidas ja millal saate kliendile projekti eest arve esitada. Pärast projekti lepingu ja projekti seadistamist saate projekti jaoks seadistada arvete esitamise reeglid. Arvete esitamise reeglid põhinevad projekti lepingus määratud projekti tingimustel. Saate luua arvete esitamise reeglid, mis sõltuvad projekti lepingu tingimustest ja projekti tüübist (nt aja- ja materjalikulu või fikseeritud hinnaga), mida seostate arveesitamise reegliga. Projekti lepingu jaoks saate luua rohkem kui ühe arveesitamise reegli. Samuti saate määrata arvete esitamise reegli mitmele projektile, mis on seotud sama projekti lepinguga ja millel on sarnased arvete esitamise tingimused. 

Saate seadistada järgmist tüüpi arvete esitamise reegleid.

-   **Tarnitav ühik** – arve kliendile, kui olete kauba kohaletoimetamise lõpetanud. Saate määratleda lepingus tarnitavad ühikud.
-   **Edenemine** – saate kliendile arve esitada, kui olete projekti teatud protsendi lõpule viinud. Saate seadistada arvete esitamise reegli, mis arvutaks lõpule viidud töö protsendi või saate käsitsi arvutada lõpuleviidud töö protsendimäära ja kliendile arvestatud summa.
-   **Vahekokkuvõte** – arve kliendile projekti vahekokkuvõtte täielikus summas, kui vahekokkuvõte on saavutatud.
-   **Tasu** – arve kliendile teie teenuste eest, millele lisandub haldustasu, mis on tavaliselt protsent teenuste maksumusest.
-   **Aeg ja materjal** – arve kliendile aja ja materjali eest, mida kasutatakse projektis.

Igat tüüpi arvete korral saate määrata kliendiarvest lahutatud säilituse protsendi, kuni projekt jõuab kokkulepitud faasi. Makse kinnipidamise protsent on määratud projekti lepingus. Summa arvutatakse kliendi arveridade koguväärtuse põhjal ja lahutatakse sellest. 

**Aja- ja materjalikulu** ning **Edenemise** arveldamise reeglite puhul saate määrata tasustatavad kategooriad. Tasustatavad kategooriad näitavad tehinguid, mis tuleb kaasata kliendiarvetele. 

Kui olete kliendile arveesitamise lõpetanud, arvutatakse projekti jaoks arvesumma vastavalt arvereeglitele ja luuakse projektiarve soovitus. 

Järgmistes jaotistes on toodud näited, mis näitavad projektiarvete seadistamist ja haldamist.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Näide: saate luua arvete esitamise reegli, mis põhineb tarnitud ühikute arvul.

Teie organisatsioon sõlmib lepingu, et pakkuda kliendi töötajatele kokku viit koolitust hinnaga 10 000 ühe koolituse kohta. Pärast iga koolitust saate kliendile arve esitada. 

Lepingu jaoks arveesitamise reeglite seadistamisel saate kasutada järgmisi väärtusi.

-   Tarneühik on üks koolitusseanss.
-   Ühikuhind on 10 000 koolitusseansi kohta.
-   Üksuste koguarv on viis koolitusseanssi.

Kui olete ühe koolitusseansi lõpetanud, saate luua arve väärtuses 10 000, esimeste tarnüksuste kohta ja saata arve kliendile.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Näide: saate luua arveldamise reegli, mis põhineb määratud protsendil projekti lõpuleviimisest (käsitsi arvutamine)

Teie organisatsioon, tarkvara konsultatsioonifirma, sõlmib kliendiga lepingu, et töötada välja osa tootest, mida klient arendab. Teie organisatsioon nõustub edastama tarkvarakoodi kuue kuu jooksul. Klient nõustub maksma teie organisatsioonile kokku summa 100 000 töö eest. Saate luua arvete esitamise reegli, mis põhineb lepingus määratud projektiga lõpule viidud tööde protsendil.

-   Esimese kuu lõpus kohtute kliendiga, et teha kindlaks lõpuleviidud töö protsent. Pärast seda, kui teie ja klient projekti üle vaatate, otsustate, et projekt on lõpule viidud 15 protsenti.
-   Loote arve 15,000 (15 protsenti 100 000-st) ja saadate selle kliendile.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Näide: saate luua arveldamise reegli, mis põhineb määratud protsendil projekti lõpuleviimisest (automaatne arvutamine)

Teie organisatsioon, tarkvara arenduse ühing, nõustub looma kliendile palgaarvestusrakenduse väärtuses 30 000. Klient nõustub maksma teie organisatsioonile lõpetatud töö protsendi alusel. Prognoosite, et projekti kulud on 20 000. Projekti leping määratleb tööde kategooriad, mida te arveldamise protsessis kasutate. Seadistate arved, mis arvutavad automaatselt arve summad iga kategooria jaoks lõpuleviidud tööde protsendi ulatuses. Seadistate iga kategooria jaoks eelarve.

-   **Arendus** – kulu 15 000 ja müügitulu 20 000
-   **Installimine** – kulu 5000 ja müügitulu 10 000

Kui loote kliendile arve esimest korda, arvutatakse arve summa automaatselt vastavalt järgmisele teabele.

-   Pärast ühte kuud esitab projekti töötaja ajatabeli. Töötaja tööaja kulu on 5000 arenduseks ja 1000 installimiseks. Arendustöö on 33 protsendi ulatuses lõpetatud (5000 tegelik kulu / 15000 eelarveline kulu) ja installimistööd on 20 protsendi ulatuses lõpetatud (1000 tegelik kulu / 5000 eelarveline kulu).
-   Arve summa 8667 arvutatakse automaatselt (33 protsenti 20 000-st + 20 protsenti 10 000-st).
-   Loote arve summas 8667 ja saadate selle kliendile.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Näide: saate luua arveldamise reegli, mis põhineb kokkulepitud vahekokkuvõttel.

Teie organisatsioon, juhtimise konsultatsioonifirma, nõustub teostama turu-uuringuid tarbija toote kohta, mida klient kavatseb müüa. Klient on nõus kasutama teie teenuseid kolme kuu jooksul alates märtsist ja nõustub maksma teie organisatsioonile 50 000. Projektil on kolm vahekokkuvõtet.

-   1. tähtaeg: tarbijate andmete kogumine – 31. märts
-   2. tähtaeg: tarbija andmete analüüsimine – 30. aprill
-   3. tähtaeg: toote elujõulisuse ettepaneku esitamine – 31. mai

Klient nõustub maksma teie organisatsioonile 10 000 esimese etapi, 20 000 teise etapi ning 20 000 kolmanda etapi eest. 

Projekti lepingu sõlmimisel nõustute kliendi arvega, mis põhineb lõpetatud etapil. Arvete esitamise reegli seadistamine hõlmab järgmisi toiminguid.

-   Määratlege projekti etapid.
-   Määrake kliendile esitatava arve summa, kui iga etapp on lõpule jõudnud.

Kui esimene etapp lõpetatakse 31. märtsil, saate märkida, et etapp on lõpetatud ja seejärel luua arve summas 10 000 ja saata see kliendile. Etapi eest ei saa arvet luua enne, kui olete etapi lõpetatuks märkinud.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Näide: saate luua teenustel ja halduskulul põhineva arvete esitamise reegli.

Teie organisatsioon, juhtimise konsultatsioonifirma, nõustub teostama turu-uuringuid, et hinnata toote elujõulisust, mida klient, jaemüügi ettevõte arendab. Lepingu tingimused määravad, et pakute oma kolme juhtiva konsultandi teenust, kes viib läbi uurimistööd aja- ja materjalipõhiselt. Klient nõustub maksma 100 tunnis, pluss 10 protsenti haldustasu konsultatsioonide eest, mis on antud projektile. 

Projekti lepingu sõlmimisel looge arveldamise reegel, et lisada 10-protsendine haldustasu projektiga seotud konsultatsioonidele. 

Kui loote kliendile arve, on kliendile arvestatud 10-protsendise haldamise tasu pluss konsultatsioonide maksumus. Näiteks kui kolm konsultanti töötasid projekti jaoks kokku 200 tundi, luuakse järgmise arvutuse põhjal arve summas 22 000.

-   200 tundi tasuga 100 tunnis = 20 000
-   10 protsenti haldamise tasu = 2000
-   Arve kogusumma = 22 000

Kui kliendilt võetakse teenustasusid ja te valite projektilepingus käibemaksugrupi, sisestatakse käibemaksugrupp automaatselt ervete esitamise reeglile tasude osas.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Näide: saate luua arvete esitamise reegi aja ja materjalide väärtuse jaoks.

Teie organisatsioon, tarkvara konsultatsioonifirma, nõustub pakkuma teenust viie tehnilise konsultandiga, kes arendavad kliendile tarkvara järgmised kuus kuud. Klient nõustub maksma 150 iga konsultatsioonitunni eest, millele lisandub kontoritarvete maksumus. Teie organisatsioon saadab kliendile arve iga kuu lõpus. 

Projektilepingu sõlmimisel nõustute kliendile iga kuu saatma arve aja ja materjalide eest. Saate luua arvete esitamise reegli, mis sisaldab järgmist teavet.

-   Lepinguperiood on kuus kuud.
-   Konsultatsiooniaeg arvutatakse määraga 150 tunnis.
-   Kontoritarbed arveldatakse soetusmaksumuses ja projekti kogumaksumus ei tohi ületada 10 000.
-   Saate luua kliendi arve iga kalendrikuu lõpus projekti jooksul.

Esimesel kuul registreerisid projekti konsultandid kokku 800 tundi. Projektile arvestatud kontoritarvete kulud on 2000. Seetõttu saate kuu lõpus luua arve summas 122 000, mis arvutatakse 800 tunnina (150 tunnis), pluss 2000 kontoritarvete eest.





[!INCLUDE[footer-include](../includes/footer-banner.md)]