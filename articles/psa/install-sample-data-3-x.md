---
title: Näidisandmete installimine
description: Selles teemas antakse teavet Project Service Automationis näidisandmete installimise kohta.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 01e2f1f6b29e040d5c72af402031e13a867736405c4ee161e49b74a30e4b506e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985541"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Näidisandmete installimine Project Service’i rakendusele

[!include [banner](../includes/psa-now-project-operations.md)]

Selleks et aidata teil luua oma demokeskkondi, pakub Microsoft allalaaditavaid näidisandmete pakette, mis näitavad teie rakenduste võimeid. Näidisandmete pakette on kaht tüüpi:
- viiteandmed/seadistusandmed
- demoandmed (viite-/seadistusandmed ja tehingu andmed, nt töökäsud ja projektid)

**Viiteandmete** näidispaketid on allalaaditavad kolme eraldi paketina, nii et saate andmeid installida ainult Project Service’i või Field Service’i jaoks või installida näidisandmed mõlema rakenduse jaoks korraga.

Seadistus-/viiteandmete näidispaketid on järgmised:

- [**V902PSMasterData** – ainult Project Service’i versioon 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** – ainult Field Service’i versioon 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** – Field Service 8.x ja Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Uusi **demoandmete** pakett on järgmine:

 - [**FPSDemoData** – Field Service 8.x ja Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Installijuhised erinevad veidi kasutajate loomise ja konfigureerimise osas, aga ülejäänu on sama kui eelmises [**ajaveebipostituses**](https://aka.ms/fpsdemodatablog). Selles paketis on vähendatud demoandmete pakett ja selle installimine kestab umbes 3 tundi.

Need näidisandmete paketid on saadaval ainult inglise keeles.

> [!IMPORTANT]
> **Näidisandmeid pole võimalik desinstallida.** Installige need paketid vaid demo-, hindamis-, õppe- või katsesüsteemidesse. Peale selle pange tähele, et ei toetata üksiku paketi ja seejärel teise üksiku paketi installimist. (Teisisõnu pole teil võimalik installida paketti **FSMasterData** ja seejärel paketti **PSMasterData** või vastupidi.) Kui näete, et teil võib kunagi vaja minna mõlema rakenduse näidisandmeid, installige pakett **v902FPSMasterData**.

Kui installite mõne näidisandmete pakettidest, toimub installimisprotsessi käigus järgmine.

- Luuakse või seadistatakse vaikeparameetrid Project Service’i, Field Service’i või mõlema rakenduse kasutamiseks (kui on olemas).

- Imporditakse rakenduste näidisandmed, nt broneeritavad ressursid, rakendusepõhised rollid, müügi ja kulu hinnakirjad, organisatsiooniüksused, müügiprotsessi kirjed ja muud üksused põhivõimaluste näitamiseks.  

**Demoandmete** paketiga saate ülaltoodud täiendavad tehingu andmed, nt töökäsud ja projektid.

Kas mõtlete, milliseid võimalusi saate näidisandmetega demonstreerida? Vaadake jaotisest [Tehnilised märkused](#technical-notes) väljamõeldud näidet ettevõttest Fabrikam Robotics.

Kui teil on küsimusi nende näidisandmete pakettide installimise kohta, [saatke meile meil aadressil fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Nõuded

Installimisprotokoll eeldab teie sihteksemplari (organisatsiooni) kohta järgmist.

- Põhikeel on inglise keel ja põhivaluuta USA dollar (USD, $).

- Organisatsioonil pole veel Project Service’i või Field Service’i andmeid või on ainult minimaalsed vaikeandmed, mis on kaasas iga uue organisatsiooniga.

- Installitud on juba ärirakenduse õige versioon.
       
    - **FPSDemoData või v902FPSMasterData jaoks:** organisatsiooni on installitud Field Service’i versioon 8.x ja Project Service’i versioon 3.x.

    - **v902PSMasterData jaoks:** organisatsiooni on installitud Project Service’i versioon 3.x.

    - **v902FSMasterData jaoks:** organisatsiooni on installitud Field Service’i versioon 8.x.

> [!NOTE]
> Kui peate installima näidisandmed lisaks olemasolevale Project Service’i ja Field Service’i proovi- või demokeskkonnale, milles juba on andmeid (pole soovitatav), peate seiskama installija tehtavad ohutuse kontrollid. Lisateavet vt allolevatest tehnilistest märkustest.

## <a name="prepare-for-installation"></a>Installimise ettevalmistamine

Peate käivitama installija arvutis, millel on Windowsi uusim versioon (eelistatult Windows 10).

Plaanige nii, et arvuti oleks võrku ühendatud ja **seadistus-/viiteandmete** installimine kestaks kuni **1 tund**. (Tavaliselt kestab **FPSMasterData** installimine umbes 30 minutit, see hõlmab mõlema rakenduse näidisandmeid.) **FPSDemoData** installimine kestab umbes **3 tundi**.

Arvuti ekraanisäästja funktsioon peab olema välja lülitatud. Muidu võivad installimise seansi mandaadid ekraanisäästja rakendumisel kaduma minna (kui te ei hoia seanssi pidevalt aktiivsena).

> [!div class="mx-imgBorder"]
> ![Ekraanisäästja sätete kuvatõmmis, kui ekraanisäästja on välja lülitatud.](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Allalaadimine ja lahtipakkimine

Project Service’i ja Field Service’i näidisandmete installijat levitatakse ise lahtipakkiva täitmisfailina. Failinimed võivad näidisandmete paketist olenevalt olla erinevad, aga etapid on samad, olenemata sellest, millise paketi installite.

Pärast paketi allalaadimist käivitage EXE-fail ja tihendatud ZIP-faili lahtipakkimiseks nõustuge tingimustega. Peate faili sisu lahti pakkima mõnda kausta arvutis.

Operatsioonisüsteemist ja turvasätetest olenevalt võivad pärast ZIP-faili lahtipakkimist vajalikud olla järgmised sammud.

1. Otsige üles fail **FPSDemoData.dll** ja paremklõpsake sellel kaustas **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Valige suvand **Tühista blokeerimine**.

3. Valige suvand **Rakenda**.

4. Valige **OK**.


## <a name="create-or-configure-users"></a>Kasutajate loomine või konfigureerimine

**FPSDemoData** pakett nõuab kuut kasutajat, **FPSMasterData** paketid nõuavad üht kasutajat. Kasutage oma näidisandmete paketi jaoks sobivat varianti.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Kasutajate loomine või konfigureerimine – seadistus-/viiteandmete paketid

Pakett **FPSMasterData** on mõeldud ühe kasutaja nimega Spencer Low installimiseks siin kirjeldatud sätetega. Paketi õigesti installimiseks peate looma (või ajutiselt ümber nimetama) kasutajad teie keskkonnas, et need ühtiks sissetulevate näidisandmete konfiguratsiooniga.

Kasutajate loomiseks või konfigureerimiseks valige **Sätted** > **Turve** > **Kasutajad** ja tehke järgmist.

1. Määrake suvand UserFullname="Spencer Low" kasutajanimega "spencerl" (**väiketähed**) Project Manageri ja Practice Manageri rollidele.

2. Valige kasutaja **Spencer Low** ja seejärel suvand **Rollide haldamine**. Otsige üles ja valige roll **Süsteemiadministraator** ning seejärel valige nupp **OK**, et anda kasutajale Spencer Low administraatori täielikud õigused. See etapp on vajalik tagamaks, et näidiskirjed luuakse õige kasutaja omandusega ja seega vaated täidetakse õigesti.

3. Allalaadimispaketist peate värskendama andmete vastendamise faili vaikimisi kasutaja konteksti meiliaadressidega. Selleks avage kaust **PkgFolder** ning otsige üles ja avage fail **ImportUserMapFile.xml** Notepadis (või Visual Studios või muus XML-redaktoris). Määrake välja **DefaultUserToMapTo=** väärtuseks kasutaja Spencer Low meiliaadress.

4. Kui te ei kasuta kasutajat Spencer Low kasutajanimega **spencerl**, peate värskendama lisafaili. Avage fail **DemoDataPreImportConfig.xml** ja otsige üles silt **userstocreateandconfigure**. Värskendage silti **\<login\>** kasutaja Mart Ilves kasutajanimega. Üksikasju vaadake jaotisest [Tehnilised märkused](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Kasutajate loomine või konfigureerimine – demoandmete pakett

Demoandmete paketi jaoks on vaja kuut kasutajat. Selleks et pakett õigesti installitaks, tehke järgmist.

 1. Looge kasutajad või nimetage ajutiselt ümber olemasolevad kasutajad, nii et need ühtiks sissetulevate näidisandmete konfiguratsiooniga, valides **Sätted** > **Turve** > **Kasutajad**.
 
    Neid rolle on vaja ainult isiklike demode jaoks.  
    - Väliteeninduse tehnik, kasutaja täisnimi = "David So"   
    - Klienditeeninduse ja väliteeninduse dispetšer, kasutaja täisnimi = "Jamie Reding"   
    - Kontohaldur, kasutaja täisnimi = "Molly Clark"   
    - Praktika- ja projektijuht, kasutaja täisnimi = "Spencer Low"  
    - Meeskonnaliige, kasutaja täisnimi = "Veronica Quek"   
    - Kasutaja täisnimi = Erik Contoso
  
2. Demoandmete importimiseks määrake ülaltoodud kuuele kasutajale administraatori roll, et näidiskirjed õigesti imporditaks. 

3. Avage **PkgFolder** ning otsige üles ja avage fail **ImportUserMapFile.xml**. Värskendage väljad **New=** süsteemis vastavate kasutajate meiliaadressidega.

   > [!div class="mx-imgBorder"]
   > ![UserMapFile’i kuvatõmmis.](media/sample-data-7.png)

4. Kui kasutajal täisnimega Spencer Low on muu kasutaja ID kui **"spencerl"**, peate värskendama täiendavat faili. Avage fail **DemoDataPreImportConfig.xml** ja otsige üles silt **userstocreateandconfigure**. Värskendage silti **\<login\>** sisselogimise ID-ga (tõstutundlik). 

5. Esimese kasutaja kalendrit (sildil **userstocreateandconfigure**) kasutatakse kõikide broneeritavate ressursside tööaja väljade täitmiseks demoandmete importimisel. Valige **Sätted** > **Turve** > **Kasutajad**, otsige üles kasutaja Spencer Low ja avage suvand Tööaeg. Muutke tööaega, valides suvandi **Terve korduv nädalaajakava algusest lõpuni**. Kontrollige, kas **tööaeg on 8.00–17.00 (9 tundi), esmaspäevast reedeni, ja ajavöönd on määratud Vaikse ookeani ajale (USA ja Kanada)**. Seda on vaja projekti- ja ajakavapaneeli õigesti kuvamiseks.

**Soovitus.** Kaaluge organisatsioonist varukoopia loomist juhuks, kui peate minema tagasi lähtekohta, kui näidisandmete installimisel midagi valesti läheb. Lisateavet vt teemast [Eksemplaride varundamine ja taastamine](/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Käivitage Package Deployer

1. Otsige üles ja käivitage fail **PackageDeployer.exe** kaustas **v902FPSMasterData** VÕI **PackageDeployer_FPSDemoData**.

2. Nõustuge nõuete ja tingimustega.

3. Järgmises aknas

   a. Valige juurutustüübiks **Office 365**.

   b. Kasutage jaotises „Create or configure users” kasutaja konfigureeritud süsteemiadministraatori kasutajanime ja parooli (kasutaja Spencer Low kasutajanimi spencerl).

   c. Veenduge, et valitud oleks suvand **Saadaolevate organisatsioonide loendi kuvamine**.

      > [!div class="mx-imgBorder"]
      > ![Kuvatõmmis aknast Package Deployer – valitud suvand Saadaolevate organisatsioonide loendi kuvamine](media/sample-data-2.png)

4. Valige organisatsioon, kuhu soovite näidisandmed installida.

5. Valige nupp **Edasi**, kuni näete dialoogi **Demoandmete seadistamine**.

   > [!div class="mx-imgBorder"]
   > ![Demoandmete installija olekuakna kuvatõmmis.](media/sample-data-3.png)

6. Enne jätkamist pange tähele, et näidisandmete installimine võib kesta kuni ühe tunni (tavaliselt ~10 minutit). Peate veenduma, et arvuti oleks kogu installimisprotsessi aja sees ja võrku ühendatud ning seanss oleks pidevalt aktiivne.   

7. Kui olete valmis, klõpsake nuppu **Edasi**, et alustada näidisandmete installimisega. Pärast näidisandmete laadimist klõpsake nuppu **Lõpeta**.

## <a name="verify-the-sample-data-installation"></a>Näidisandmete installimise kontrollimine

Õigsuse kontrollimiseks kontrollige, kas ettevõtte Fabrikam Robotics väljamõeldud stsenaariumis loendatud kirjete arv ja üksuste tüübid kuvatakse ootuspäraselt.

Kui näidisandmed on täielikult laaditud, logige sisse kasutajana Spencer Low ja kinnitage järgmist.

- Kui installitud on Project Service’i rakendus, valige suvandid **Project Service** > **Sätted** > **Hinnakirjad**. Kinnitage, et andmekogumis oleks olemas iga riigi/piirkonna jaoks sobivas valuutas arveldus- ja kulumäärad.

- Kui Project Service’i rakendus on installitud, valige suvandid **Universal Resource Scheduling** > **Sätted** > **Organisatsiooniüksused**. Kinnitage, et iga organisatsiooniüksusega (v.a linnakirjed) oleks seotud sobivas valuutas omahindade loend. Kui mõni on puudu, otsige üles ja seostage õige omahindade loend.

- Kui Field Service’i rakendus on installitud, valige suvandid **Project Service** > **Sätted** > **Hinnakirjad**. Kinnitage, et olemas oleks arveldus- ja kulumäärad. Valige **Field Service** > **Sätted** > **Hinnakirjad** ning kontrollige, et andmekogumis oleks olemas iga riigi/piirkonna jaoks sobivas valuutas arveldus- ja kulumäärad.

  > [!div class="mx-imgBorder"]
  > ![Aktiivsete hinnakirjade kuvatõmmis.](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Aktiivsete organisatsiooniüksuste kuvatõmmis.](media/sample-data-5.png)

## <a name="technical-notes"></a>Tehnilised märkused

Nende andmete tehniliste üksikasjade nägemiseks vaadake teavet allpool.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Näidisandmete installimine lisaks olemasolevatele andmetele (pole soovitatav)

Kui peate installima näidisandmed lisaks olemasolevale Field Service’i või Project Service’i proovi- või demokeskkonnale, milles juba on andmeid, peate seiskama installija tehtavad ohutuse kontrollid.

Selleks minge kausta **PkgFolder** ning otsige üles ja avage fail **DemoDataPreImportConfig.xml** Notepadis (või muus XML-redaktoris).

Otsige üles järgmine väärtus ja muutke säte õigest valeks.

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Selle muudatuse tõttu jätab installija vahele mõned olulised ohutuskontrolli, sh järgmised.

- Kinnitamine, et pole rohkem kui üks aktiivne kirje **Organisatsiooniüksus**, ja sellele nime **Fabrikam US** andmine.

- Kinnitamine, et pole rohkem kui üks aktiivne kirje **Töömall**.

- Kinnitamine, et pole rohkem kui üks aktiivne kirje **Projekti parameeter**, ja sellele kandele nime **Parameetrid** andmine.

### <a name="configuration-components"></a>Konfiguratsioonikomponendid

Selles eelnevalt imporditud konfiguratsioonifailis on hulk muid konfiguratsioonikomponente. Tehniliste kasutajate korral on osa neist järgmised.

- **\<RequiredSolutions\>** määrab eeltingimuse lahenduse installid ja nende versiooninumbrid.

- **\<InstallSampleData\>** kontrollib, kas kasutusvalmis näidisandmed on rakenduse jaoks installitud.

    - väär – jätab nende sisseehitatud andmete (mis on eemaldatavad) installimise vahele

    - tõene – installib sisseehitatud andmed koos FS-i ja PSA näidisandmete installimisega

- **\<PreImportDataCollection\>** määrab lamefaili andmekaardid ja seostatud kirjed, mis imporditakse enne peamiste näidisandmete installimist.

- **\<EntitiesToEnableScheduling\>** määrab, millised olemid tuleks broneerimiseks lubada rakenduses Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** määrab broneeritavad ressursid, mis luuakse (kui neid veel pole) enne näidisandmete importimist. Pange tähele, et lähtesüsteemi näidisandmete broneeritav ressurss ühtib sihtsüsteemi broneeritava ressursi kirjetega iga ressursi täieliku nime ja sisselogimisandmete osas. Seega EI OLE võimalik selles eelkonfiguratsioonifailis nimesid muuta, kui te ei impordi kõigepealt näidisandmeid sihtsüsteemi, kasutades neid nimesid, seejärel nimetate broneeritavad ressursid ümber sobiva nimega, mis on määratud koos lubatud kasutaja kirjetega, ja seejärel ekspordite andmed uuesti importimiseks lõplikku sihtsüsteemi (värskendades vastavalt faili **ImportUserMapFile.xml** vanu ja uusi kirjeid).

- **\<PluginsToDisable\>** määrab väga diskreetsed rea kauba lisandmoodulid, mis tuleb näidisandmete importimisel keelata ja seejärel hiljem uuesti lubada.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Ettevõtte Fabrikam Robotics väljamõeldud stsenaarium

Field Service’i ja Project Service’i viiteandmete näidispaketid installivad **lahenduse Fabrikam Manufacturing Master Data (v3.0.0.0)** koos umbes 4000 kirjega ja umbes 40 eri üksusega. Field Service’i või Project Service’i eraldi näidisandmete paketid sisaldavad selle rakenduse näidisandmete **v902FPSMasterData** alamkogumit. **Demoandmete** pakett installib **lahenduse Fabrikam Manufacturing Demo Data (v3.0.0.7)** umbes 22 000 kirjega 148 üksuses.

Väljamõeldud ettevõte Fabrikam Robotics toodab elektroonikaseadme koosteliini roboteid ja on tuntud oma toodete kvaliteedi, uuendusmeelsuse ning tugeva klienditeeninduse poolest, sh installimiste planeerimine, rakendamine ja jooksvad hooldusteenused. Fabrikami peakorter asub Ameerika Ühendriikides (Fabrikam US) ja sellel on neli projektipõhist teenusetoimingut Prantsusmaal, Indias, Ühendkuningriigis ja Šveitsis.

Väliteeninduse toimingud on koondunud Ühendriikidesse, peamiselt Seattle’i piirkonda. Ettevõte keskendub asjade Interneti (IoT) connectivity parandamisele, et jälgida kliendi vara jõudlust ja pakkuda üha rohkem ennetavat kohapealset hooldust.

Näidisandmete põhjalik ülevaade on järgmine.

- Üldised näidisandmete elemendid (lisatud mõlema rakenduse jaoks)

    - 1 kasutaja

    - 71 kontot

    - 137 kontakti

    - Mitmesugused kandetüübid ja -kategooriad

    - 50 toodet 1 toote hinnakirjaga

    - 14 hinna-/kulukirja

    - 31 näitajat (ressursioskused) 2 hindamismudelis 3 tasemega (hindamisväärtused)

- Project Service

    - 8 organisatsiooniüksust

    - 6 rollipõhist kasutustaset

    - Üle 2800 rolli-hinna spetsifikatisooni

- Field Service

    - 4 territooriumi

    - 5 töökäsu tüüpi

    - 22 kliendivara

    - 9 juhtumi tüüpi valiku seotud ressursi näitajate (9), teenuste (13) ja hooldustoimingutega (13)
   
**Demoandmete** pakett installib umbes 179 töökäsku, 12 projekti ja seotud tehingu andmed. 

### <a name="change-the-work-hours-for-sample-resources"></a>Näidisressursside töötundide muutmine

Vaikimisi on kõigil broneeritavatel ressurssidel 24-tunnine töökalender.

Kui peate muutma broneeritava näidisressursi töötunde, valige **Universal Resource Scheduling** > **Plaanimine** > **Ressursid**.

Valige kasutaja (nt Spencer Low) ja muutke tema töötunnid tundidele, mida soovite rakendada mitmele kasutajale. Valige **Universal Resource Scheduling** > **Sätted** > **Töötundide mallid** ja muutke kirjet **Vaikimisi töömall**. Väljas **Malli ressurss** valige kasutaja töötundidega, mida soovite rakendada teistele ressurssidele. Valige **Universal Resource Scheduling** > **Plaanimine** > **Ressursid** > **Aktiivsed broneeritavad ressursid**. Valige ressursid, mida soovite muuta, ja seejärel valige suvand **Kalendri määramine**. Ripploendist **Töömall** valige mall **Vaikimisi töötund** või muu õige ressursiga mall. Kui lähete plaanimistahvlile, peaksite nägema, et ressursside töötunde on nüüd värskendatud.

> [!div class="mx-imgBorder"]
> ![Aktiivsete broneeritavate ressursside kuvatõmmis.](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]