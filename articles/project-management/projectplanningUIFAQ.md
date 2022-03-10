---
title: Tööülesande ruudustikus töötamise tõrkeotsing
description: Selles teemas kirjeldatakse tõrkeotsingu teavet, mida on vaja tööülesande ruudustikus töötamisel.
author: ruhercul
ms.date: 09/22/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 67136229d84a09886fffe9677b10f671aea3c393
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547194"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Tööülesande ruudustikus töötamise tõrkeotsing 


_**Kehtiv järgnevale:** Project Operations ressursi-/mitteressursipõhised stsenaariumid, lihtjuurutus – tehing näidisarveldusele, Project for the web_

Teenuse Dynamics 365 Project Operations kasutatav ülesande ruudustik on teenuses Microsoft Dataverse majutatud iFrame. Selle kasutamise tulemusena peavad autentimise ja autoriseerimise õigeks toimimiseks olema täidetud erinõuded. Selles teemas antakse ülevaade levinumatest probleemidest, mis võivad mõjutada ruudustiku renderdamist või tööülesannete haldamist tööjaotuse struktuuris (WBS).

Levinud probleemide hulka kuulub järgnev.

- Vahekaart **Ülesanne** on ülesande ruudustikus tühi.
- Projekti avamisel projekti ei laadita ja kasutajaliides (UI) jääb spinnerile pidama.
- **Project for the Webi** õiguste haldus.
- Ülesande loomisel, uuendamisel või kustutamisel muudatusi ei salvestata.

## <a name="issue-the-task-tab-is-empty"></a>Probleem: vahekaart Ülesanne on tühi

### <a name="mitigation-1-enable-cookies"></a>1. kohandus: lubage küpsised

Tööjaotuse struktuuri renderdamiseks nõuab Project Operations, et kolmanda osapoole küpsised oleksid lubatud. Kui kolmanda osapoole küpsised pole lubatud, näete toimingute nägemise asemel tühja lehte, kui valite vahekaardi **Tööülesanded** lehel **Projekt**.

Brauserite Microsoft Edge või Google Chrome korral kirjeldavad järgmised toimingud seda, kuidas oma brauserisätteid värskendada ja lubada kolmanda osapoole küpsiseid.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Avage brauser Edge.
2. Valige paremas ülanurgas **kolmikpunkt** (...) ja seejärel valige **Sätted**.
3. Valige jaotises **Küpsised ja saidiõigused** suvand **Küpsised ja saidiandmed**.
4. Lülitage **Kolmanda osapoole küpsiste blokeerimine** välja.
5. Värskendage oma brauser. 

#### <a name="google-chrome"></a>Google Chrome

1. Avage brauser Chrome.
2. Valige paremas ülanurgas kolm vertikaalset punkti ja seejärel valige **Sätted**.
3. Valige jaotises **Privaatsus ja turvalisus** suvand **Küpsised ja muud saidiandmed**.
4. Valige **Luba kõik küpsised**.
5. Värskendage oma brauser. 

> [!NOTE]
> Kui te blokeerite kolmanda osapoole küpsised, blokeeritakse kõik muude saitide küpsised ja saidiandmed, isegi kui see sait on lubatud teie erandite loendis.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>2. leevendus: kontrollige, kas PEX-i lõpp-punkt on õigesti konfigureeritud

Project Operations vajab, et projekti parameeter viitaks PEX-i lõpp-punktile. See lõpp-punkt on vajalik teenusega suhtlemiseks, mida kasutatakse tööjaotuse struktuuri renderdamiseks. Kui parameeter pole lubatud, kuvatakse tõrketeade "Projekti parameeter ei ole kehtiv". PEX-i lõpp-punkti uuendamiseks tehke järgmist.

1. Lisage **PEX-i lõpp-punkti** väli lehele **Projekti parameetrid**.
2. Tuvastage, millist tüüpi toodet kasutate. Seda väärtust kasutatakse PEX-i lõpp-punkti seadmisel. Allalaadimisel on tootetüüp juba PEX-i lõpp-punktis määratletud. Hoidke see väärtus alles.
3. Lisage väljale järgmine väärtus: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Järgmises tabelis on toodud tüübiparameeter, mida tuleks tootetüübi põhjal kasutada.

      | **Toote tüüp**                     | **Tüübi parameeter** |
      |--------------------------------------|--------------------|
      | Project for the Web vaikeorganisatsioonis   | tüüp=0             |
      | Project for the Web CDS-i nimetatud organisatsioonis | tüüp=1             |
      | Project Operations                   | tüüp=2             |

4. Eemaldage väli lehelt **Projekti parameetrid**.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Probleem: projekti ei laadita ja kasutajaliides jääb spinnerile kinni

Ülesande ruudustiku laadimiseks peavad autentimise jaoks olema hüpikaknad lubatud. Kui hüpikaknad ei ole lubatud, jääb ekraan laadimisspinneri peale kinni. Järgmisel pildil on näidatud URL, millel aadressiribal on blokeeritud hüpikaken, mille tulemusena jääb spinner lehe laadimise proovimisel toppama. 

   ![Toppama jäänud spinner ja blokeeritud hüpikaken.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>1. kohandus: lubage hüpikaknad

Kui teie projekt jääb spinneri peale toppima, on võimalik, et hüpikaknad ei ole lubatud.

#### <a name="microsoft-edge"></a>Microsoft Edge

Edge’i brauseris on võimalik hüpikaknaid lubada kahel viisil.

1. Valige Edge’i brauseris selle parempoolses ülanurgas teatis.
2. Valige konkreetse teenuse Dataverse keskkonna jaoks suvand **Luba hüpikaknad ja ümbersuunamised alati**.
 
     ![Blokeeritud hüpikute aken.](media/enablepopups.png)

Teise võimalusena saate teha järgmised toimingud.

1. Avage brauser Edge.
2. Valige ülemises parempoolses nurgas **kolmiknupp** (…) ja seejärel valige **Sätted** > **Saidiõigused** > **Hüpikaknad ja ümbersuunamised**.
3. Hüpikakende blokeerimiseks lülitage suvand **Hüpikaknad ja ümbersuunamised** välja või lülitage see sisse, et lubada oma seadmes hüpikud.
4. Pärast hüpikakende lubamist värskendage brauserit. 

#### <a name="google-chrome"></a>Google Chrome
1. Avage brauser Chrome.
2. Liikuge lehele, kus hüpikaknad on blokeeritud.
3. Valige aadressiribalt suvand **Hüpikaken blokeeritud**.
4. Valige hüpikakna link, mida soovite näha.
5. Pärast hüpikakende lubamist värskendage brauserit. 

> [!NOTE]
> Kui soovite saidi hüpikaknaid alati näha, valige suvand **Luba said [site] hüpikud ja ümbersuunamised alati** ja seejärel valige **Valmis**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Probleem 3: Project for the Webi õiguste haldus

Project Operations sõltub välisest ajastamisteenusest. Teenuse jaoks on vaja, et kasutajale oleks määratud mitu rolli, mis võimaldaks tal WBS-iga seotud olemeid lugeda ja kirjutada. Nende olemite hulka kuuluvad projektiülesanded, ressursi määramised ja ülesande sõltuvused. Kui kasutaja ei saa WBS-i vahekaardile **Ülesanded** liikumisel renderdada, on see arvatavasti seetõttu, et suvandi **Project Operations** valik **Projekt** pole lubatud. Kasutaja võib saada kas turberolliga või juurdepääsu keelamisega seotud tõrke.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>1. leevendus: valideerige rakenduse kasutaja ja lõppkasutaja turberollid

1. Avage **Sätted** > **Turvalisus** > **Kasutajad** > **Rakenduse kasutajad**.  

   ![Rakenduse lugeja.](media/applicationuser.jpg)
   
2. Topeltklõpsake rakenduse kasutajakirjet, et kontrollida järgnevat.

     - Kasutajal on projektile juurdepääs. Saate seda teha kontrollides, kas kasutajal on turberoll **Projektihaldur**.
     - Microsoft Projecti rakenduse kasutaja on olemas ja on õigesti konfigureeritud.
 
3. Kui seda kasutajat pole olemas, looge uus kasutajakirje. 
4. Valige **Uued kasutajad**, muutke kirjevormiks **Rakenduse kasutaja** ja lisage seejärel **Rakenduse ID**.

   ![Rakenduse kasutaja üksikasjad.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Probleem 4: ülesande loomisel, uuendamisel või kustutamisel muudatusi ei salvestata

Kui teete WBS-is vähemalt ühe värskenduse, siis muudatused nurjuvad ja neid ei salvestata. Ajakavaruudustikus esineb tõrge teatega „Teie hiljutisi muudatusi ei saanud salvestada“.

### <a name="mitigation-1-validate-the-license-assignment"></a>1. leevendus: valideerige litsentsi määramine

1. Kontrollige, et kasutajale on määratud õige litsents ja et teenus on litsentsi teenuseplaani üksikasjades lubatud.  
2. Veenduge, et kasutaja saaks avada lehe **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>2. leevendus: rakenduse Project kasutaja valideerimise konfiguratsioon
1. Kontrollige, kas rakenduse Project kasutaja on loodud.
2. Rakendage kasutajale järgmised turberollid.
  
  - Teenuse Dataverse kasutaja või baaskasutaja
  - Project Operationsi süsteem
  - Projekti süsteem
  - Project Operationsi topeltkirjutuse süsteem. See roll on nõutav Project Operationsi ressursi-/mittelaopõhise juurutamise stsenaariumi jaoks.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
