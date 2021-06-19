---
title: Mis on uut või muudetud Project Service Automation versioonis 3?
description: Selles teemas kirjeldatakse, mis on Project Service Automationi versioonis 3 uus ja mida on muudetud.
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 26d79ff79801f8ad0f80020d49fdc80f76dd9aef
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007001"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Mis on uut või muudetud Project Service Automation versioonis 3?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles jaotises kirjeldatakse kasutajaliideses (UI), funktsionaalsuses ja terminoloogias tehtud muudatusi ning seda, kuidas need erinevad Project Service Automation versiooni 2 või 1 ja versiooni 3 vahel.

## <a name="project-scheduling"></a>Projekti ajastamine
Projekti ajakava, mis oli eelmistes versioonides tuntud tööjaotuse struktuuri (WBS) nime all, on nüüd ajakava nime all ja seda saab avada, kui klõpsate vahekaarti **Ajakava**. 

![Projekti ajakava](media/psa-schedule-01.png)

Ajakavas on nüüd suhtluseks uus pind, mis on nii kaasaegne kui ka ligipääsetav. Samas ei ole aluseks olev Project Service Automationi kavandamise mootor muutunud. Ajakava ruudustiku lindil olevate juhtnuppude abil saate töötada ajakavaga, mis on Project Service Automationi eelmise versiooniga sarnane. Ajakavale tehtud lisamuudatused on järgmised.

- **Gantti diagramm** – Gantti diagrammi pole enam olemas. Tulevases värskenduses tuuakse tagasi uus Gantti visualiseering.
- **Veerupäised** – saate ruudustikus veerupäised peita, kui klõpsate veeru pealkirja kõrval asuvat tähist Alla. 
- **Veerud** – saate kuvada peidetud veerge, kui klõpsate valikut **Lisa veerg**. 
- **Kandekategooria** – **Kandekategooria** otsing on lisatud ajakava ruudustikku ja see kuvatakse vaikimisi. 
 
## <a name="project-templates"></a>Projektimallid
Projektimallide funktsioonides on tehtud järgmised muudatused.

### <a name="create-a-project-template"></a>Projektimalli loomine 
Saate luua projektimalli versioonis 3 sarnaselt Project Service Automationi eelmiste versioonidega. Mall võib sisaldada ainult ajakava ja ajakava võib sisaldada määramisi, ent see pole kohustuslik. Kui ajakavas on määramised, saavad need olla ainult üldiste ressursside jaoks. Saate üldiste ressursside jaoks luua ressursinõudeid, ent neid ei saa mallis tegelike ressurssidega broneerida. Mallis ei saa tegelikku ressurssi meeskonnale broneerida. 

### <a name="create-a-template-from-an-existing-template"></a>Malli loomine olemasoleva malli abil
Kui loote uue projektimalli juba Project Service Automationi versioonis 3 olemasoleva malli abil, juhtub järgmine. 

- Lähteprojekti ajakava kopeeritakse malli. 
- Üldised ressursid kopeeritakse meeskonda ja kõik üldiste ressursside määramised kopeeritakse samuti üle. Üldiste ressursside kohta käivaid nõudeid ei kopeerita üle. 

### <a name="create-a-template-from-an-existing-project"></a>Malli loomine olemasoleva projekti abil
Kui loote uue projektimalli olemasoleva projekti abil, juhtub järgmine. 

- Lähteprojekti ajakava kopeeritakse malli. 
- Üldised ressursid kopeeritakse meeskonda ja kõik üldiste ressursside määramised säilitatakse. Üldiste ressursside kohta käivaid nõudeid ei kopeerita üle.    
- Nimega ressursid, nii määratud kui ka määramata, eemaldatakse meeskonnast ja asendatakse üldiste ressurssidega.
- Kui kliendi teave on olemas, eemaldatakse see. 
- Kui viited hinnapakkumistele ja lepingutele on olemas, eemaldatakse need. 

### <a name="create-a-project-from-a-template"></a>Projekti loomine mallist
Kui loote uue projektimalli Project Service Automationi versioonis 3, juhtub järgmine.

- Ajakava, meeskond ja määramised kopeeritakse uude projekti.   
- Alguskuupäev on kas kopeerimiskuupäev või kasutaja valitud kuupäev.   
- Ühegi üldise meeskonnaliikme jaoks, kellel on mallis olemas ressursinõuded, ei kopeerita ega looda nõudeid automaatselt. Peate need looma. 

## <a name="copy-a-project"></a>Projekti kopeerimine
Kui kopeerite projekti Project Service Automationi versioonis 3, juhtub järgmine. 

- Kopeeritakse eeldatav alguskuupäev, ent seda saab muuta.  
- Kopeeritakse projekti ajakava ja ülesanded. 
- Kopeeritakse üldised ressursid ja nende määramised. Üldiste ressursside kohta käivaid ressursinõudeid ei kopeerita üle. Peate need uuesti looma. 
- Tegelikke ressursse ja nende määramisi ei kopeerita. Selle asemel asendatakse need üldiste ressurssidega. 
- Tegelikke näitajaid ei kopeerita uude projekti. 

## <a name="move-a-scheduled-project"></a>Ajastatud projekti teisaldamine
Olemasoleva projekti ajakava ettepoole nihutamisel juhtub järgmine. 

- Ülesannete kuupäevad teisaldatakse automaatselt selliselt, et need vastaks perioodi teisaldamisele. 
- Määratud üldised ressursid jäävad määratuteks.   
- Kui need luuakse enne projekti teisaldamist, jäävad üldise ressursi nõuded samaks ja neid ei looda automaatselt uuesti. Ülesannete teisaldamise tõttu peate need uute ülesannete kajastamiseks uuesti looma. 
- Tegeliku ressursi määramised muutuvad vastavalt ülesande kuupäeva liikumisele. Tegelike ressursside broneeringud ei muutu. Peate broneeringuid vastavusseviimise vaate abil muutma. 
- Broneeringutega, ent määramisteta meeskonna ressursid ei muutu. 
- Tegelikke näitajaid ei teisaldata. 

## <a name="estimates"></a>Prognoosid
Prognoosid on jagatud kahe vahekaardi vahel: **Ressursi määramine** ja **Prognoosid**. Vahekaart **Ressursi määramine** sisaldab panuse prognoose ja kuvab ajafaasi vaates ülesannete ressursi määramised. Saate prognoose muuta vastavalt sellele, mida kavandamismootor on loonud.

![Ressursi määramiste vahekaart, millel on näha panuse prognoosid ja ülesannete ressursi määramised](media/resource-assignments-tab-02.png)

Vahekaardil **Prognoosid** on näha ressursi määramiste kulude ja müügi summad. Summad on kirjutuskaitstud. Kulude ja müügi hinnakujundus põhineb nüüd ajakavas olevate meeskonnaliikmete määramistel. See tähendab seda, et kui teil ilma ühegi määramiseta ülesanne, kuvatakse see ülesanne määramatute salves. See tähendab ka seda, et ilma **rollita**, mis on vaikimisi hinnakujunduse dimensioon, ei looda ka eeldatavat kulu või müüki, kui teil on projektiga seostatud klient või leping/hinnapakkumine. 

![Vahekaart Prognoosid, kus on näha kulude ja müügi summad](media/estimates-tab-03.png)
  
Kategooriat toetatakse ka ajakava vaates olevate ülesannete puhul. Kui rühmitate prognooside ajafaasi vaates kategooria järgi, saate parema kogemuse – eriti siis, kui teil on projektis olemas ka kulude prognoosid. Kulude prognoosid sisestatakse eraldi vahekaardil asuva ruudustiku abil. 

Kulude prognoosid saab sisestada ruudustikku vahekaardil **Kulude prognoosid**. 

![Kulude prognooside vahekaart, kus on näha kulude prognooside ruudustikku](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Ressursihaldus
Tänu uuele ühtsele kliendipõhisele kasutajaliidesele ning broneeringute ja määramiste vahelistes suhetes tehtud muudatustele on Project Service Automationi versioonis 3 versiooniga 2 või 1 võrreldes oluliselt muutunud projektile üldiste või tegelike ressursside määramine. Broneeritavate ressursside – nii **tegelike** kui ka **üldiste** – mõisted jäävad samas, nagu ka meeskonnaliikmed, nõuded, määramised ja broneeringud.   

![Ressursivalija kasutamine](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Tegeliku broneeritava ressursi määramine 
Project Service Automationi versioonis 3 ei ole broneeringute ja tööülesannete määramine nii tihedalt põimunud kui varasemates Project Service Automationi versioonides. Saate **tegeliku** meeskonnaliikme broneerimiseks kasutada meeskonna ruudustikku, mis sarnaneb turul olevaga.

Kui kasutate ajakavas ressursivalijat, saate valida meeskonna vaates loodud meeskonnaliikmed ja seejärel määrata nad ülesannetele. Soovi korral saate jätkata neile ülesannete määramist, isegi pärast broneeringute tegemist. Kasutage vahekaarti **Vastavusse viimine**, et viia vastavusse need meeskonnaliikmed, kellel on erinevusi broneeringute ja määramiste vahel.

Ressursivalija kuvab projekti meeskonnaliikmed. Saate ressursivalijat kasutada ka nende broneeritavate ressursside otsimiseks ja vaatamiseks, mis ei kuulu projekti meeskonda. Saate neid määrata ülesannetele ja nii saavad ka need projekti meeskonna osaks. Peate need broneerima **ajakavapaneeli** või vahekaardi **Vastavusse viimine** abil.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Määrake üldine broneeritav ressurss ülesandele ja projekti meeskonnale ning seejärel täitke ajakavapaneeli kaudu tegeliku ressursiga 
Project Service Automationi versioonis 3 ei kasutata meeskonna loomise funktsiooni üldiste ressursside jaoks. Selle asemel saate luua üldise ressursi ja selle otse määrata ajakavas, tippides ajakava ressursi lahtrisse üldise ressursi positsiooni nime. Samuti võite lahtris valida ressursi ikooni ja seejärel ressursivalija abil tippida loodava üldise ressursi nime. See avab kiirloomise paani, mis võimaldab teil määrata üldise ressursi meeskonnaliikme rolli ja organisatsiooniüksuse. Pärast ressursi loomist määratakse see ülesandele ja saate jätkata selle üldise ressursi määramist ajakavas olevatele muudele ülesannetele.    
 
Kui olete ressursi kõigile asjakohastele ülesannetele ära määranud, saate luua ressursi nõude ja seejärel selle ära täita, broneerides otse **ajakavapaneeli** abil või esitades ressursi taotluse. Saate üldisi ressursse lisada ka otse meeskonnaliikmete ruudustikku. 

Üldised ressursid lisatakse projekti meeskonda ilma ühegi ressursinõudeta ning koos projekti algus- ja lõpukuupäevaga seni, kuni luuakse ressursi nõue. Nõude loomiseks valige üldine ressurss ja klõpsake nuppu **Loo**. Nüüd kuvatakse nõude link ja nõutavad tunnid täidetakse määratud tundidega. Nõude avamiseks ja värskendamiseks saate klõpsata linki.
  
Kui broneering on valmis ja nimega ressursi poolt täielikult ära täidetud, asendatakse üldine ressurss nimega ressursiga ning ajakavas olev määramine värskendatakse nimega ressursiga. 

Nõuete jaoks soovitatavad ressursid salvestatakse nüüd eraldi jaotise asemel vahekaardile.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Mitu nimega ressurssi täidavad loodud ressurssi
Kui nõue täidetakse mitme ressursiga, jääb üldine ressurss meeskonda ja ülesandele määratuks. Broneeritud nimega meeskonnaliikmeid ei määrata positsiooni osana. Projektijuht saab tööd määrata vajaduse järgi tegelikele ressurssidele.  Vaates **Vastavusse viimine** kuvatakse mitme ülesande määramiste jaoks broneeringute liigendus üle mitme ressursi. Seda ei tehta automaatselt, sest keerulisemate stsenaariumite puhul (näiteks siis, kui nõude moodustab mitme ülesande kogum) on vaja eeldada seda, kuidas projektijuht kavatseb määrata. Kuna aga süsteem ei saa kavatsusest aru, erinevad need eeldused suure tõenäosusega sellest, mida tegelikult teha sooviti, ning seetõttu kuvatakse vale ja ettearvamatu tulemus. Prognoositav tulemus on see, et üldine ressurss jääb määratuks seni, kuni projektijuht tahtlikult määrab vaate **Vastavusse viimine** abil ressursid.

### <a name="reconciliation"></a>Vastavusse viimine
Vahekaardil **Vastavusse viimine** kuvatakse kõigi projekti meeskonnaliikmete kõik broneeringud ja ülesanded. Vaates kuvatakse tundide arv lahtrites, mis võivad esindada ajapunkte kuudest päevadeni. See vaade võimaldab projektijuhtidel oma töörühma jaoks viia vastavusse meeskonnaliikmete broneeringuid ja nende määramised. See on kasulik, sest broneeringud ja ülesanded pole omavahel tihedalt seotud ning see tagab projekti kavandamisel suurema paindlikkuse. 

![Vahekaart Vastavusse viimine, kus on näha projekti meeskonnaliikmete broneeringud ja määramised](media/resource-reconciliation-tab-06.png)

Iga ressursi puhul tehakse vaates kindlaks meeskonnaliikme broneeringute ja nende ülesannete määramiste ümberarvestuse vahe ning kuvatakse järgmised kaks erinevust, mis võivad broneeringute ja määramistega seoses projektis ette tulla. 

- **Broneeringu puudujääk** – broneeringu puudujääk ilmneb siis, kui ressursil on rohkem määramisi kui broneeringuid. Kuna seda võimsust pole broneeritud, saab projektijuht seda tingimust parandada, pikendades ressursi broneeringuid puudujäägi katteks. 
- **Liigsed broneeringud** – liigsete broneeringute juhtum leiab aset siis, kui ressurss on projektile broneeritud, aga seda pole ülesannetele määratud.  See võib olla vastuvõetav tegevusjuhtum, kui ressurss on broneeritud enne ülesande määramist. Mõnel muul juhul ei pruugita aga soovida ressurssi määrata ja projektijuht peaks kaaluma ressursi broneeringute tühistamist, et võimsust saaks kasutada mõne muu projekti jaoks. 

Kui teil on ülesannete määramised broneeringuta ressursi jaoks (broneeringu puudujääk), saate valida broneeringute puudujäägi liitväärtuse ja klõpsata käsku **Pikenda broneeringut**. Siin saate vaadata broneeringut, mis on vajalik ressursi puudujäägi lahendamiseks, selle kättesaadavust. 
 
## <a name="time-and-expense"></a>Aeg ja kulud
Selles jaotises kirjeldatakse, mis on Project Service Automation versioonis 3 muutunud aja, kulude ja kinnitamisega seoses. Dynamics 365 Project Service Automation lahenduse osana on värskendatud ka **ajakirje** funktsiooni, et kasutada ära ühtse kasutajaliidese raamistikku. See võimaldab pakkuda ühtset kasutajaliidest, mis järgib kiirelt reageeriva veebidisaini põhimõtteid, et tagada igasuguse ekraanisuuruse või seadme puhul optimaalne vaatamiskogemus. 

### <a name="landing-page"></a>Sihtleht
Mittelaiendatav kohandatud ajakirje kogemus on versioonist 3 eemaldatud. Selle asemel on nüüd laiendatav ja hõlbusfunktsioonidega algruudustiku kogemus. Saate ajakirje funktsioonile ligi, kui kasutate vasakul asuvat saidikaarti. Selle muudatuse tõttu ei saa te enam ühe nädala kaupa aega sisestada. Selle asemel peate looma ajakirje iga ruudustikus oleva päeva jaoks. Pärast paari ajakirje loomist saavad kasutajad luua ajakirjeid hulgi kaupa, kasutades funktsiooni **Kopeeri**, mida kirjeldatakse selles jaotises hiljem. 

![Ajakirje sihtleht](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Uute ajakirjete loomine 
Klõpsake lindil nuppu **Uus**, et avada ajakirje kiirloomise leht, kuhu saate sisestada kestuse minutites, tundides või päevades. Selleks alustage tähe h, m või d tippimist koos numbriga.  

![Ajakirje kiirloomine](media/quick-create-time-entry-08.png)

Süsteemivaated toetavad otsinguvälju. Näiteks pärast projektiteabe sisestamist seatakse välja **Projektiülesanne** vaikevaateks **Minu avatud projekti ülesanded**. Kui soovite luua ajakirjeid selliste ülesannete jaoks, mis pole kasutajale määratud, klõpsake otsingu otsingus valikut **Muuda vaadet** ja valige suvand **Kõik aktiivsed projektiülesanded**. Kui ajakirje on loodud ja ruudustikus kuvatud, saate redigeerida mis tahes rea väärtust otse ruudustikus.  

### <a name="bulk-createcopy"></a>Hulgi kaupa loomine/kopeerimine 
Pärast paari ajakirje loomist saate kopeerimise funktsiooni abil luua hulgi kaupa täiendavaid ajakirjeid. Klõpsake käsku **Kopeeri**, et avada **kopeerimise** dialoog. **Perioodi algus: alguskuupäev** – määrake kuupäevavahemik, millest ajaperioodid tuleb kopeerida. **Perioodi lõpp: alguskuupäev** – määrake kuupäev, mille jaoks ajakirjed tuleb luua. Klõpsake käsku **Kopeeri**, et kopeerida ajakirjed vastavasse nädalapäeva, mis on kuvatud väljal **Perioodi lõpp**. Näiteks viimase nädala esmaspäeva ajakirje kopeeritakse selle nädala esmaspäeva, mis on määratud väljal **Perioodi lõpp**. 

![Ajakirjete kopeerimine hulgi kaupa](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Andmete importimine 
Määramised ja vahetused järgivad sama kasutajaliidese mustrit ning see võimaldab kasutajal määrata kuupäevavahemiku, kust broneerimisi tuleb importida. Seejärel peate eraldi välja valima broneeringud, mis tuleks kopeerida ajakannete **mustanditesse**. Versioonis 3 ei näe te ruudustikus ega kalendris enam **soovitatud** ajakirjete mustrit.  

### <a name="change-in-calendar-control"></a>Kalendri juhtelemendi muudatus
Versioonis 3 ei kasutata nädala ajakirjete kuvamiseks enam kohandatud kalendri juhtelementi, vaid UC kalendrit. Selle kalendriga saate vaadata päeva, nädalat ja kuud. 

> [!NOTE]
> Kalendri kitsendus on see, et see juhtelement ei toeta üksikute kalendriüksuste toiminguid. Näiteks ei saa te valida ühte või mitut kalendriüksust ning neid esitada või kustutada. Kalendriüksuse klõpsamisel avatakse lisatoimingute jaoks leht **Ajakirje olem**. 

### <a name="extensibility"></a>Laiendatavus
**Ainult aja- ja kulukirjete olemites olevate kohandatud väljade andmete hõivamine** – ajakirje kasutab platvormilt redigeeritavat ruudustikku, kirjutuskaitstud ruudustikku ning kalendri juhtelemente. Kõik need juhtelemendid on algsed ja seetõttu toetavad kohandusi. Project Service Automationi versioonis 3 saate lisada kohandatud välju, seadistada otsinguvälju ja varundada need kohandatud vaadetega. Samuti saate kohandatud väljadel valitud väärtuste põhjal määrata kohandatud äriloogika.  

**Aja- ja kulukirjetes olevate kohandatud väljade andmete hõivamine ning nende levitamine esitamis- ja kinnitamisvoogu toetavate olemite kaudu** – järgmisel skeemil on näidatud ajakirjete tavaline töötlemine.

![Ajakirje voo protsess](media/process-time-entries-10.png)

Kui ärinõuetes on sätestatud, et aja ja kulu olemid peavad hõivama kohandatud hinnakujunduse dimensioonid ning levitama väärtusi, mis on määratud kohandatud hinnakujunduse dimensioonis aja ja kirje ressursi järgi kõigi eelmistel piltidel olevate olemite kaudu, vaadake jaotist [Kohandatud väljade seadistamine hinnakujunduse dimensioonidena](set-up-pricing-dimensions.md)

Selliste ärinõuete toetamiseks, kus aja ja kulu olemid peavad hõivama kohandatud mittehinnakujunduse dimensioonid ning levitama väärtusi, võite kasutada hinnakujunduse dimensioonide seadistamist ja väljendada kohandatud dimensioone ilme kulu- või arveldusmäärata. Teise variandina võite lisada igale olemile kohandatud välja, kasutades kõigis olemites sama välja nime. Luua saab kohandatud lisandmooduleid, et seostada neid olemites olevaid kirjeid, mis on esitamise/kinnitamise voos, kasutades kande päritolu ja kande seose olemeid.  

### <a name="delegate-time-and-expense-entry"></a>Aja- või kulukirjete delegeerimine
Common Data Service’i platvorm ei toeta seda, kui üks kasutaja kehastab teist, mis tähendab, et Project Service Automationi versioonis 3 ei toetata delegeeritud aja- ja kulukirjeid. Partnerid ja kliendid on aga loonud lahenduse, mis võimaldab versioonis 3 toetada delegeeritud ajakirje kogemust. See pole aga terviklik lahendus ja seetõttu on oluline aru saada ka sellega kaasnevatest kitsendustest ning kasutada seda lahendust ainult siis, kui kitsendused on vastuvõetavad. 

> [!IMPORTANT]
> Seda teavet tuleks võtta partneri/kliendi poolt väljapakutud lahendusena kohandatud juurutamise jaoks. Tootemeeskond ei paku ühegi toekanali kaudu sellele funktsioonile ametlikku tuge.

### <a name="customization-details"></a>Kohandamise üksikasjad 
Kohandamine võimaldab teil loomise ja redigeerimise kogemusse lisada **broneeritava ressursi**, mis võimaldab kasutajal tegutseda delegaadina, muutes välja **Broneeritav ressurss** mõnele muule kasutajale, kelle jaoks on aja- ja kulukirjed vaja luua. Järgmised etapid hõlmavad ajakirjete delegeerimist. Sama teave kehtib ka kulukirje delegeerimise kohta. 
 
1.  Veenduge, et delegeeritud kasutajal oleks projektidele ja projekti ülesannetele üldine turbejuurdepääs. 
1.  Kuna **broneeritavat ressurssi**, mis on olemi **Ajakirje** väli, ei kuvata lehel **Kiirloomine**, peate selle lisama.

    -või-

    Looge kohandatud vaade, mis sisaldab veergu **Broneeritav ressurss**, et vaadata ainult ressursi jaoks loodud üksikuid ajakirjeid. Avaldage rakenduse mooduli kujundaja kohandused, et see vaade kuvataks **Vaatevalijas**, mis asub lehel **Ajakirjed**. Olemas on kaks lisandmoodulit, mis tegelevad projektiga mitteseotud ajakirjete jaoks halduri seadmisega.

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Looge uus lisandmoodul, et kirjutada üle väli **Haldur** väljal **Broneeritav ressurss** määratud kasutaja halduriga. Kasutage erakorralise (OOB) lisandmooduliga (enne valideerimist) sama **täitmisetappi** ja **täitmisjärjestust**, mis on suurem kui OOB lisandmoodulid (suurem kui 1). See tagab, et kohandatud lisandmoodul käivitatakse pärast OOB lisandmooduleid.  
 
### <a name="end-user-experience"></a>Lõppkasutaja kogemus
1.  Kui loote ajakirje kiirloomise lehel, sisestage projekt ja projekti ülesande üksikasjad ning seejärel valige väljal **Broneeritav ressurss** kasutaja, kelle jaoks on ajakirjed vaja luua. 
2.  Vaikimisi kehtib see väli sisselogitud kasutaja kohta, aga arvestades, et kasutaja kirjutas selle välja üle, luuakse ajakirje nüüd valitud **broneeritava ressursi** jaoks.
3.  Kui esitate nende kirjete jaoks loodud ajakirjed, lisatakse need ootuspäraselt projekti kinnitaja jaoks järjekorda. 
4.  Kui võtate muu kasutaja jaoks loodud ajakirjed tagasi, muudetakse ajakirjete olekuks uuesti **Mustand** ja väli **Broneeritav ressurss** on määratud muule kasutajale. 
5.  Soovi korral saate muu kasutaja jaoks loodud ajakirjete filtreerimiseks kasutada kohandatud vaadet. 
 
### <a name="limitations"></a>Piirangud
Funktsioonid **Kopeeri** ja **Impordi** töötavad ainult selle kasutaja kontekstis, kes on sisse logitud. See tähendab, et kopeerida või importida ei saa neid ajakirjeid, mis on loodud kasutaja jaoks, kes on sisse logitud broneeritava ressursina.

Ajakirjed, mis pole projekti jaoks loodud, suunatakse kinnitamiseks broneeritava ressursi haldurile ainult siis, kui ülaltoodud jaotises **Kohandamise üksikasjad** kirjeldatud etapp 4 on lõpuni ära tehtud. Muidu suunatakse muu kasutaja jaoks loodud projektiga mitteseotud ajakirjed valesti sisse logitud kasutaja haldurile. 

### <a name="other-changes"></a>Muud muudatused 
Funktsioon **Broneeringud ja ülesanded** on eemaldatud. 

## <a name="multidimensional-pricing"></a>Mitmedimensiooniline hinnakujundus
Paindlikkuse maksimeerimiseks ning erinevate ärinõuete täitmiseks toetab Project Service Automation versioon 3 hinnakujunduse dimensioonikogumite diskreetset kohaldamist kulu- ja arveldusmääradele. Dimensiooniväärtusi saab määrata vaikeväärtustena ning seejärel neid levitada üle kogu kulude ja hinnakujunduse protsessi, alates ressursi profiilimisest kuni ajakirjete ning projekti tegelike näitajateni välja. Kliendipõhine konfiguratsioon ja muudatus või laiendus kasutab standardset kohandatavat infrastruktuuri.

Project Service Automation tarnitakse vaikimisi seatud hinnakujunduse dimensioonide, rollide ja ressursi üksustega ning võimaldab iga rolli ja organisatsiooniüksuse kombinatsiooni jaoks seadistada hinnakujundusi ning kulusid.

Nende Project Service Automationi klientide jaoks, kes soovivad versioonis 3 jätkata nende valmisväljade kasutamist hinnakujunduse dimensioonidena, ei ole toimunud mingeid jälgitavaid muudatusi. Saate jätkuvalt kasutada Project Service Automationi nagu tavaliselt. Kui teil on aga vaja ressursside jaoks määrata hinnakujundus või kulud muude lisaatribuutide abil, võimaldab versioon 3 teil lisada Project Service Automationisse oma kohandatud hinnakujunduse dimensioone. Kohandatud hinnakujunduse dimensioonide laiendus on keeruline konfiguratsiooni kogemus. 

## <a name="quotes-and-contracts"></a>Hinnapakkumised ja lepingud
Project Service Automationi versioonis 3 on muudetud hinnapakkumiste ja lepingute seadistamise ning haldamisega seotud aspekte. Järgmistes jaotistes antakse üksikasjalikumat teavet.

### <a name="set-up-chargeability-options"></a>Arveldatavuse valikute seadistamine
Versioonides 1 ja 2 tehti konkreetsete hinnapakkumise ning lepingute jaoks rollide ja kategooriate seadistamist vaate **Arveldatavus** abil, mis asus hinnapakkumise rea või lepingurea ülemisel navigeerimisribal. Seal sai seadistada ka hindu nende rollide ja kulude kategooriate jaoks.

Versioonis 3 seadistatakse aga rolli- või kulukategooria järgi tehtavad arveldatavuse valikud hinnapakkumise rea või lepingurea tasandil. Hinnakujunduse seadistamine on arveldatavuse seadistamisest eraldi. **Arveldatavad rollid** ja **Arveldatavad kategooriad** leiate lehtede **Hinnapakkumise rida** ja **Lepingurida** vahekaartidena, ilma et peaksite kasutama ülemist navigeerimisriba.

![Arveldatavad rollid](media/chargeable-12.png)
 
Arveldatavate rollide ja kategooriate seadistamine kasutab ka redigeeritavat valmisruudustiku juhtelementi. Iga rolli ja kategooria puhul jäävad hinnapakkumise tegemise ning lepingu sõlmimise faasis arvelduse tüübi toetatud valikud, **Arveldatav** ja **Mittearveldatav**, samaks nagu eelmistes versioonides. **Tasuta** ei ole hinnapakkumise tegemise või lepingu sõlmimise faasis toetatud tüüp. **Tasuta** tüüpi toetatakse ainult aja või kujude kinnitamise ajal.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Project Service Automationi hinnapakkumise ja projekti lepingu kohandatud hinnakujunduse loomine ja redigeerimine
Versioonides 1 ja 2 kasutati konkreetsete hinnapakkumiste ja lepingute jaoks kohandatud hinnakirja vaates **Arveldatavus** oleva suvandi **Redigeeri hindu** abil. Vaade **Arveldatavus** asus hinnapakkumise rea või lepingurea ülemisel navigeerimisribal. Seal sai seadistada ka rolli- ja kulukategooriate arveldatavuse valikud.

Versioonis 3 on Project Service Automationi hinnapakkumise ja Project Service Automationi projekti lepingu jaoks kohandatud projekti hinnakirja loomine ning selle kasutamine arveldatavuse seadistusest eraldatud. Project Service Automationi hinnapakkumise ja Project Service Automationi projekti lepingutes on uus vahekaart nimega **Projekti hinnakirjad**. Sellel vahekaardil kuvatakse seostatud vaatena kõik Project Service Automationi hinnapakkumise või projekti lepinguga seotud projekti hinnakirjad. Kui soovite luua kohandatud hinnakirja sellise olemasoleva hinnakirja abil, mis on juba projekti hinnapakkumise või lepinguga seostatud, klõpsake valikut **Loo kohandatud hinnakujundus**. See teeb koopia kõikidest seostatud hinnakirjadest ja lisab need hinnapakkumisele või lepingule. Nüüd saate hinnakirja avada ja redigeerida rolli- või kulukategooria hinda selliselt, et kõik need hinnakujunduse muudatused kohalduvad ainult sellele hinnapakkumisele või lepingule. 
  
Järgmisel pildil on kuvatud vaade enne kohandatud hinnakirjade loomist.

![Enne kohandatud hinnakirju](media/before-custom-price-lists-13.png)

Järgmisel pildil on kuvatud vaade pärast kohandatud hinnakirjade loomist.

![Pärast kohandatud hinnakirju](media/after-custom-price-lists-14.png)

> [!NOTE]
> Kui klõpsate kohandatud hinnakirja loomiseks valikut **Kohandatud hindade loomine**, võib hinnakiri ilmuda väikese viivitusajaga. Soovitame ruudustikku värskendada, mitte mitu korda klõpsata. Kohandatud hinnakiri on loodud siis, kui seostatud hinnakirja nimele on lisatud hinnapakkumise nimi või projekti lepingu nimi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]