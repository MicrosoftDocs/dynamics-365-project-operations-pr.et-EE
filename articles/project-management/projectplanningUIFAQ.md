---
title: Tööülesande ruudustikus töötamise tõrkeotsing
description: Selles teemas kirjeldatakse tõrkeotsingu teavet, mida on vaja tööülesande ruudustikus töötamisel.
author: ruhercul
ms.date: 08/02/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 07e7bd42db48842edee17fdfdd22fdcd8207644c1751f453ec29c3194aac625e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989096"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Tööülesande ruudustikus töötamise tõrkeotsing 

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Selles teemas kirjeldatakse, kuidas parandada probleeme, mis võivad ilmneda kuluhaldusega töötamisel.

## <a name="enable-cookies"></a>Küpsiste lubamine

Project Operations vajab, et kolmanda osapoole küpsised oleksid lubatud, et tööjaotuse struktuuri renderdada. Kui kolmanda osapoole küpsised pole lubatud, näete toimingute nägemise asemel tühja lehte, kui valite vahekaardi **Tööülesanded** lehel **Projekt**.

![Tühi vahekaart, kui kolmanda osapoole küpsised pole lubatud.](media/blankschedule.png)


### <a name="workaround"></a>Lahendus
Brauserite Microsoft Edge või Google Chrome korral kirjeldavad järgmised toimingud seda, kuidas oma brauserisätteid värskendada ja lubada kolmanda osapoole küpsiseid.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Avage brauser Edge.
2. Valige paremas ülanurgas **kolmikpunkt** (...) ja seejärel valige **Sätted**.
3. Valige jaotises **Küpsised ja saidiõigused** suvand **Küpsised ja saidiandmed**.
4. Lülitage **Kolmanda osapoole küpsiste blokeerimine** välja.

#### <a name="google-chrome"></a>Google Chrome

1. Avage brauser Chrome.
2. Valige paremas ülanurgas kolm vertikaalset punkti ja seejärel valige **Sätted**.
3. Valige jaotises **Privaatsus ja turvalisus** suvand **Küpsised ja muud saidiandmed**.
4. Valige **Luba kõik küpsised**.

> [!IMPORTANT]
> Kui te blokeerite kolmanda osapoole küpsised, blokeeritakse kõik muude saitide küpsised ja saidiandmed, isegi kui see sait on lubatud teie erandite loendis.

## <a name="pex-endpoint"></a>PEX-i lõpp-punkt

Project Operations vajab, et projekti parameeter viitaks PEX-i lõpp-punktile. See lõpp-punkt on nõutav, et suhelda teenusega, mida kasutatakse tööjaotuse struktuuri renderdamiseks. Kui parameeter pole lubatud, kuvatakse tõrketeade "Projekti parameeter ei ole kehtiv". 

### <a name="workaround"></a>Lahendus

1. Lisage **PEX-i lõpp-punkti** väli lehele **Projekti parameetrid**.
2. Tuvastage, millist tüüpi toodet kasutate. Seda väärtust kasutatakse PEX-i lõpp-punkti seadmisel. Allalaadimisel on tootetüüp juba PEX-i lõpp-punktis määratletud. Hoidke see väärtus alles. 
   
    ![PEX-i lõpp-punkti väli projekti parameetris.](media/pex-endpoint.png)

3. Lisage väljale järgmine väärtus: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`.

   
   | Toote tüüp                         | Tüübi parameeter |
   |--------------------------------------|----------------|
   | Project for the Web vaikeorganisatsioonis   | tüüp=0         |
   | Project for the Web CDS-i nimetatud organisatsioonis | tüüp=1         |
   | Project Operations                   | tüüp=2         |
   
4. Eemaldage väli lehelt **Projekti parameetrid**.

## <a name="privileges-for-project-for-the-web"></a>Projekti õigused veebi jaoks

Project Operations sõltub välisest ajastamisteenusest. Teenuse kasutamiseks peab kasutajale olema määratud mitu rolli, et lugeda ja kirjutada tööjaotuse struktuuriga seotud olemeid. Nende olemite hulka kuuluvad projektiülesanded, ressursi määramised ja ülesande sõltuvused. Kui kasutaja ei saa tööjaotuse struktuuri renderdada, kui ta läheb vahekaardile **Tööülesanded**, on see tõenäoliselt sellepärast, et projekt pole Project Operationsi jaoks lubatud. Kasutaja võib saada kas turberolliga või juurdepääsu keelamisega seotud tõrke.


## <a name="workaround"></a>Lahendus

1. Avage **Sätted > Turvalisus > Kasutajad > Rakenduse kasutajad**.  

   ![Rakenduse lugeja.](media/applicationuser.jpg)
   
2. Topeltklõpsake rakenduse kasutajakirjet, et kontrollida järgmist.

 - Kasutajal on projektile juurdepääs. Seda kontrolli tehakse tavaliselt kinnitades, et kasutajal on **Projektijuhi** turberoll.
 - Microsoft Projecti rakenduse kasutaja on olemas ja on õigesti konfigureeritud.
 
3. Kui kasutajat pole olemas, saate luua uue kasutajakirje. Valige **Uued kasutajad**. Muutke sisestusvormiks **Rakenduse kasutaja** ja seejärel lisage **Rakenduse ID**.

   ![Rakenduse kasutaja üksikasjad.](media/applicationuserdetails.jpg)

4. Kontrollige, et kasutajale on määratud õige litsents ja et teenus on litsentsi teenuseplaani üksikasjades lubatud.
5. Veenduge, et kasutaja saab avada lehe project.microsoft.com.
6. Kontrollige läbi projekti parameetrite, et süsteem osutab õigele projekti lõpp-punktile.
7. Kontrollige, kas projekti rakenduse kasutaja on loodud.
8. Rakendage kasutajale järgmised turberollid.

  - Dataverse'i kasutaja
  - Project Operationsi süsteem
  - Projekti süsteem

## <a name="error-when-updating-the-work-breakdown-structure"></a>Tõrge tööjaotuse struktuuri värskendamisel

Kui tööjaotuse struktuurile tehakse üks või mitu värskendust, siis muudatused lõpuks nurjuvad ja neid ei salvestata. Ajakavaruudustikus kuvatakse tõrge, et "Teie hiljutisi muudatusi ei saanud salvestada".

### <a name="workaround"></a>Lahendus

1. Kontrollige, et kasutajale on määratud õige litsents ja et teenus on litsentsi teenuseplaani üksikasjades lubatud.
2. Veenduge, et kasutaja saab avada lehe project.microsoft.com.
3. Kontrollige, et süsteem osutab õigele projekti lõpp-punktile.
4. Kontrollige, kas projekti rakenduse kasutaja on loodud.
5. Rakendage kasutajale järgmised turberollid.
  
  - Dataverse'i kasutaja või baaskasutaja
  - Project Operationsi süsteem
  - Projekti süsteem
  - Project Operationsi topeltkirjutamise süsteem (see roll on vajalik, kui kasutate Project Operationsi ressursipõhist/mittelaopõhist stsenaariumi.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
