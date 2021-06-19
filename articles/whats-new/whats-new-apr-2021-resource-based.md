---
title: Mis on uut aprillis 2021 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: See teema annab teavet Project Operationsi ressursipõhiste/mittelaopõhiste stsenaariumite jaoks 2021. a aprilli väljalaskes saadaolevate kvaliteedivärskenduste kohta.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 518d795cf7fd2e172a1ce54e2483881d35cea1da
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012671"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut aprillis 2021 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.

- Project Operations Dataverse’i keskkonna versioonis 4.9.0.221
- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.17

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

Selles väljaandes sisalduvad järgmised funktsioonid.

- Projektide mittelaopõhised materjalid. Peamised võimalused on järgmised.
  - Mittelaopõhiste materjalide projekti müügitsükli ajal prognoosimine ja hinnakujundus. Lisateavet vaadake teemast [Kataloogitoodete oma- ja müügihindade seadistamine – liht](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Mittelaopõhiste materjalide jälgimine projekti kohaletoimetamisel. Lisateavet vaadake teemast [Projektides ja projektiülesannetes materjali kasutuse kirjendamine](../material/material-usage-log.md).
  - Kasutatud mittelaopõhiste materjalide kulude arveldamine. Lisateavet vaadake teemast [Arvete võlgnevuste haldamine](../proforma-invoicing/manage-billing-backlog.md).
  - Lisateavet selle funktsiooni konfigureerimise kohta leiate teemast [Logimata materjalide ja ootel hankija arvete konfigureerimine](../procurement/configure-materials-nonstocked.md)
- Ülesandepõhine arveldamine: lisatud on võimalus seostada projekti ülesandeid projekti lepinguridadega, allutades need samadele arveldusmeetoditele, arveldussagedusele ja lepingureal olevatele klientidele. See seostamine tagab täpse arveldamise, raamatupidamise, tuluprognoosi ja tuvastuse töötada projekti ülesannetel vastavalt antud häälestusele.
- Dynamics 365 Dataverse’i uued API-d võimaldavad luua, värskendada ja kustutada toiminguid suvandiga **Olemite ajastamine**. Lisateavet vaadake teemast [Ajakava API-de kasutamine kavandamise olemitega toimingute tegemiseks](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Järgmises loendis kuvatakse topeltkirjutusega kaardid, mida on muudetud või lisatud Project Operationsi 2021. a aprilli versioonis.

| **Olemikaart** | **Värskendatud versioon** | **Kommentaarid** |
| --- | --- | --- |
| Project Operationsi integreerimise tegelikud andmed (msdyn\_actuals) | 1.0.0.14 | Materjali projekti tegelike andmete sünkroonimiseks on kaarti muudetud. |
| Project Operationsi integreerimisolem kuluprognooside jaoks (msdyn\_estimateslines) | 1.0.0.2 | Lisatud on projekti lepingurea sünkroonimine rakendusega Finance and Operations ülesandepõhise arveldustoe jaoks. |
| Project Operationsi integreerimisolem tunniprognooside jaoks (msdyn\_resourceassignments) | 1.0.0.5 | Lisatud on projekti lepingurea sünkroonimine rakendusega Finance and Operations ülesandepõhise arveldustoe jaoks. |
| Project Operationsi integreerimistabel materjaliprognooside jaoks (msdyn\_estimatelines) | 1.0.0.0 | Uus tabelikaart, mille abil saab sünkroonida materjalprognoose Dataverse’ist rakendusse Finance and Operations. |
| Project Operationsi integratsiooni projekti hankija arve ekspordi olem (msdyn\_projectvendorinvoices) | 1.0.0.0 | Uus tabelikaart, mille abil saab sünkroonida hankija arvete päiseid rakendusest Finance and Operations rakendusse Dataverse. |
| Project Operationsi integratsiooni projekti hankija arve ekspordirea olem (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Uus tabelikaart, et sünkroonida hankija arve read rakendusest Finance and Operations rakendusse Dataverse. |

Project Operationsi rakenduse Dataverse lahenduse ja rakenduse Finance and Operations lahenduse versiooni värskendamisel peaksite alati käitama oma keskkonnas kaardi uusimat versiooni ja lubama kõik seotud tabelikaardid. Kui kaardi uusim versioon pole aktiveeritud, ei pruugi teatud funktsioonid ja võimalused õigesti töötada. Kaardi aktiivset versiooni saate vaadata veerus **Versioon**, mis asub lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelikaardi versioonid** valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kasutusvalmis tabelikaardi, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui kaardi käivitamisel ilmneb probleem, järgige suuniseid topeltkirjutamise tõrkeotsingu juhendi teemas [Kaardil puuduvad tabeliveerud](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations teenuses Dynamics 365 Dataverse

| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2124532 | Kui algsel arvel on honorari summa või rakendatud honorari summa, kuvatakse näidisarvel nupp **Paranda arvet**. See nupp kuvatakse ainult nendes keskkondades, milles rakenduse Finance versioon on 10.0.19 või uuem. |
| Arveldamine ja hinnakujundus | 2224568 | Lisatud on loogika, et lubada kohandused, mis hõlmavad arve kinnitamise lisandmooduli käivitamist. |
| Arveldamine ja hinnakujundus | 2101098 | Näidisarve vaikeväljade loogikat on parandatud: **Maksja aadress**, **Maksja nimi** ja **Maksetingimused** pärinevad nüüd vaikimisi vastavatest projektilepingu kliendikirjetest. |
| Arveldamine ja hinnakujundus | 2021413 | Väljasid **Tegeliku kulu** ja **Müük** uuendati olemis **Ülesanne**, et kaasata ülesande arveldamata ja arveldatud kulude müügiväärtus. |
| Arveldamine ja hinnakujundus | 2182110 | Projektilepingu kopeerimisel luuakse lepingurea ID sihtprojekti lepingus, et tagada selle kordumatus. |
| Müügivõimaluse haldus | 2186741 | Lisatud valideerimised tagamaks, et olemasoleva hinnapakkumise rea üksikasjades ei saaks välja **Päritolu** ja **Tehingu tüüp** värskendada. |
| Müügivõimaluse haldus | 2191353 | Vahe-eesmärke ei tohi aja ja materjali lepingureal luua. |
| Müügivõimaluse haldus | 2216956 | Lahendati probleem suvandiga **Värskenda hindu**. |
| Plaanimine ja jälgimine | 2182979 | Projekti kopeerimise funktsiooni on täiustatud, et tagada kuluprognoosi ridade kopeerimine algsest projektist. |
| Plaanimine ja jälgimine | 2184144 | Projekti kopeerimise funktsiooni on täiustatud, et tagada ressursi positsiooni nime kopeerimine algsest projektist. |
| Plaanimine ja jälgimine | 2184799 | Projekti koopia: tihendati kontrolli tagamaks, et hinnangulist alguskuupäeva ei saaks poolelioleva kopeerimise ajal muuta. |
| Plaanimine ja jälgimine | 2185134 | Projekti koopia: sihtprojekti eeldatavaks alguskuupäevaks seatakse tänane kuupäev. |
| Plaanimine ja jälgimine | 2196373 | Projekti koopia: veenduge, et projektijuhi ja meeskonnaliikme kirjeid ei dubleeritaks projektimeeskonnas. |
| Plaanimine ja jälgimine | 2211833 | Projekti koopia: ressursi määramised kopeeritakse lähteprojekti tööülesandest sihtprojekti. |
| Plaanimine ja jälgimine | 2186541 | Parandati probleem ressursside rühmitamise ajal ruudustikus **Prognoosid**. |
| Plaanimine ja jälgimine | 2166906 | Ülesande tehingu kategooria tuleb kopeerida olemisse **Ressursi määramine**. |
| Ressursihaldus | 2125362 | Lahendati probleemid üldise meeskonnaliikme loomisega tunnipõhist jaotamismeetodit kasutades. |
| Aeg ja kulu | 2113603 | Parandati kohandamisega seotud probleem koos atribuutide eemaldamisega lehelt **Ajakirje**. Süsteem kontrollib nüüd enne atribuudile skripti abil juurde pääsemist, kas atribuut on lehel olemas. |
| Aeg ja kulu | 2204377 | Kopeeritud ajatabelid peavad olema automaatselt kuvatud, kui valite aja kirjendamise ajal suvandi **Kopeeri nädal**. |
| Aeg ja kulu | 2209059 | Välja **Olek** saab ajakirjete Dynamics 365 Field Service jaoks muuta. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektihaldus ja raamatupidamine rakenduses Dynamics 365 Finance

| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| Projektihaldus ja raamatupidamine | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Pöördprognoosi eemaldamine ei tööta jaotises **Perioodiline**.  |
| Projektihaldus ja raamatupidamine | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Funktsioon **Raamatupidamise kohandamine** tekitab probleemi pearaamatu kontodega, kus on valitud suvand **Ära luba käsitsi sisestamist**. |
| Projektihaldus ja raamatupidamine | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Lisatud on äriloogika parandusarvete töötlemiseks (sh honorari summa või rakendatud honorari summa). |
| Projektihaldus ja raamatupidamine | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | WIP - müügiväärtuse kirjendamine kontsernisisese projekti arveldamisel valib ootamatu konto. |
| Projektihaldus ja raamatupidamine | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Kui töötate Project Operationsis honoraridega, põhjustab lepingu vaikeprojekti muutmine pärast ettemaksete arveldamist probleeme sissetulevate mahaarvamistega. |
| Projektihaldus ja raamatupidamine | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Project Operationsis peaks projektilepingust eemaldamine vajaduse korral lähtestama lepingu vaikeprojekti. |
| Projektihaldus ja raamatupidamine | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Project Operationsis kuvatakse kontsernisisese arve loendis **Lisa rida** valed kuluread. |
| Projektihaldus ja raamatupidamine | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Project Operationsis ei ole leht **Ostuleping** pole Project Operationsiga integreeritud teenuse Finance juriidiliste olemite jaoks nähtav. |
| Projektihaldus ja raamatupidamine | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Dataverse’i integratsiooni vea tõttu ei saa te teisendada hinnapakkumist Project Operationsis võidetud hinnapakkumiseks. |
| Projektihaldus ja raamatupidamine | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | Olem **ProjCDSProjectContractEntity** saab määrata rahastamisallika arve aadressi erinevalt kliendilt.  |
| Projektihaldus ja raamatupidamine | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Teenuses Project Operations ei valita kannete jaoks arve sisestamisel prognoose. |
| Reisimine ja kulu | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Sularaha ettemakse saldot ei uuendada kuluaruande puhu, kui see kinnitatakse ja kirjendadakse ridade kaupa. |
| Reisimine ja kulu | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Üksikasjalike kontsernisiseste kuluaruannete makse ei arvutata õigesti. |
| Reisimine ja kulu | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Ümberkujundatud lehel **Kontsernisisesed kuluaruanded** kuvatakse projektidega seotud lisaväljad. |
| Reisimine ja kulu | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Kuluaruannete päise vastuvõtmisel kuvatakse vale tõrketeade. |
| Reisimine ja kulu | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Kui müügimaks kirjendatakse sihtkoha juriidilises olemis, on kuluaruanne kontsernisiseses stsenaariumis valesti kirjendatud. |
| Reisimine ja kulu | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Aruande esitamise kuupäevi ei prindita kinnitatud kuluaruannetele. |
| Reisimine ja kulu | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Väljasid **Kinnitamise kuupäev** ja **Tagasi lükkamise kuupäev** ei täideta pärast kulu kinnitamist. |
| Reisimine ja kulu | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Ühe töötaja jaoks loodud reisitellimust saab kasutada teise töötaja kuluaruande jaoks. |
| Reisimine ja kulu | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kulukategooriad on uue kulurea lisamisel lukustatud. |
| Reisimine ja kulu | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Juba tükeldatud kuluaruande ridade täpsustamise tulemuseks on vautšeri Ostureskonto\pearaamat mittetäielik kirjendamine ja see rikub raamatupidamisallika avastaja, kuna **TRVEXPTRANS.SOURCEDOCUMENTLINE** on dubleeritud. |
| Reisimine ja kulu | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Reisitellimuse poliitika ei tööta ootuspäraselt. |
| Reisimine ja kulu | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Hankija konto nime ei kuvata kuluaruannete kirjendatud projektitehingutes. |
| Reisimine ja kulu | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Te ei saa Project Operationsis kinnitada kontsernisisese projekti ülesande aega. |
| Reisimine ja kulu | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Sularaha avansi tagastuspoliitika ei värskenda kirjendamisel sularaha avansi saldosid. |
| Reisimine ja kulu | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Müügihind arvutatakse valesti kuluaruannetes, mis loodi välisvaluutas, kasutades imporditud krediidikaardi tehinguid, ja mis on projektiga seostatud. |
| Reisimine ja kulu | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Andmeolem **TrvRequisitionLine** ja seostatud ainulaadne register pöörati tagasi. |
| Reisimine ja kulu | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Olemi **SOURCEDOCUMENTLINE** loomisele lisati instrumendid. |
| Reisimine ja kulu | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Kui müügimaks kirjendatakse sihtkoha juriidilises olemis, kuvatakse vale alammooduli tööleht. |
| Reisimine ja kulu | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operationsis ei kustutata kuluprognoose rakendusest Finance, kui need Dataverse’ist kustutatakse. |
| Reisimine ja kulu | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Kui kulukategooria on mitte projektipõhisest kategooriast, ei kopeerita lehel **Kulu** valitud finantsdimensioone kuluaruandesse. |
