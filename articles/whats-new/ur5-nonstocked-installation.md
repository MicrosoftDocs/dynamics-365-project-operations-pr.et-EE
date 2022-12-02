---
title: Project Operationsi värskendamine Finance'i keskkonnas
description: See artikkel annab teavet selle kohta, kuidas uuendada rakendust Project Operations rakenduse Dynamics 365 Finance keskkonnas.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: aedfd815521054d58944496500aa03a27be9267b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9030030"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Project Operationsi värskendamine Finance'i keskkonnas

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_


See artikkel annab teavet selle kohta, kuidas uuendada rakendust Dynamics 365 Project Operations rakenduse Dynamics 365 Finance keskkonnas. Project Operationsi uuendamiseks värskendusele 5 (UR5) on vaja kolme toimingut.

- [Paketi importimine eelvaate projekti](#import)
- [Värskenduse rakendamine](#apply)
- [Dataverse'i keskkonna värskendamine](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importige pakett oma LCS-projekti

1. Logige teenusesse [Lifecycle Services (LCS)](https://lcs.dynamics.com/) sisse projekti omaniku või keskkonna haldurina.
2. Valige projektide loendist oma LCS-projekt.
3. Avage lehel **Projekt** rühmas **Keskkonnad** see keskkond, mida soovite värskendada.
4. Kontrollige, et keskkond töötab. Kui see pole käivitunud, käivitage keskkond.
5. Valige jaotise **Uus väljaanne** osas **Saadaolevad värskendused** 10.0.15 nägemiseks **Vaata värskendust**.

![Värskenduse vaatamise nupp.](media/view-update.png)

6. Valige lehel **Binaarsed värskendused** suvand **Salvesta pakett**.
7. Valige lehel **Värskenduste vaatamine ja salvestamine** suvand **Salvesta pakett**.
8. Sisestage paketi nimi avanevale paanile **Paketi salvestamine varateeki** ja seejärel valige **Salvesta pakett**.
9. Kui LCS on paketi salvestamise lõpetanud, lubatakse nupp **Valmis**. Valige nupp **Valmis**. LCS kontrollib paketti. Kontrollimine võib võtta paar minutit või kuni ühe tunni.


## <a name="apply-the-package-update"></a><a name="apply"></a>Paketi värskenduse rakendamine

1. Valige LCS-is lehel **Keskkonna üksikasjad** jaotis **Haldamine** > **Värskenduste rakendamine**.
2. Valige loendist varem salvestatud pakett ja seejärel valige **Rakenda**.
3. Valige **Jah**, et kinnitada oma paketi juurutamise soov.

![Paketi juurutamise dialoogiboksi kinnitamine.](media/confirm-package-deployment.png)

4. Valige **Jah**, et kinnitada oma soov rakendust värskendada.

![Rakenduse värskendamise dialoogiboksi kinnitamine.](media/confirm-application-update.png)

Juurutamine ja rakenduse värskendamine algab. 

Lehe **Keskkonna üksikasjad** parempoolses ülanurgas värskendatakse keskkonna olekuks **Hooldus**. Värskendamine lõppeb umbes kahe tunni pärast. Rakenduse väljalaske teave värskendatakse olekusse **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** ja keskkonna olek värskendatakse olekule **Juurutatud**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Dataverse'i keskkonna värskendamine

1. Logige sisse [Power Platformi halduskeskusesse](https://admin.powerplatform.com/).
2. Otsige ja avage loendist keskkond, mida kasutasite Project Operationsi installimiseks.
3. Valige lehel **Keskkonnad** jaotis **Ressurss** > **Dynamics 365 rakendused**.
4. Otsige loendist üles **Microsoft Dynamics 365 Project Operations** ja valige veerust **Olek** väärtus **Värskendus saadaval**.
5. Märkige ruut **Nõustun teenusetingimustega** ja seejärel valige **Värskenda**. Installitakse lahenduse uusim versioon.

Pärast installimise lõpule viimist on teil installitud versioon 4.5.0.134.

## <a name="configure-new-features"></a>Uute funktsioonide konfigureerimine

### <a name="enable-dual-write-mapping"></a>Topeltkirjutuse vastendamise lubamine

Pärast Finance'i ja Dataverse'i keskkondade värskendamise lõpule viimist saate lubada vajalikud topeltkirjutuse vastendused. Topletkirjutuse vastenduse lubamiseks viige lõpule järgmised toimingud.

- [Turvasätete värskendamine Customer Engagementi keskkonnas](#security)
- [Andmeolemite värskendamine](#refresh)
- [Topeltkirjutuse vastenduste värskendamine ja käivitamine](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Dataverse'i keskkonna turvasätete värskendamine

UR5-le värskendamise osana on nõutavad järgmised olemite turbeõiguste värskendused.

1. Avage Dataverse'i keskkonnas **Sätted** ja valige rühmas **Süsteem** valik **Turve**.

![Dataverse’i keskkonna sätted.](media/Picture21.png)

2. Valige suvand **Turberollid**.
3. Valige rollide loendist **topeltkirjutuse rakenduse kasutaja** ja valige vahekaart **Kohandatud olemid**. 
4. Kontrollige, et rollil oleksid õigused **Lugemine** ja **Lisamine** järgmistele üksustele.

      - **Valuuta vahetuskurssi tüüp**
      - **Kontoplaan** 
      - **Finantskalender** 
      - **Pearaamat**

5. Pärast turberoll värskendamist minge jaotisesse **Sätted** > **Turvalisus** > **Meeskonnad**. Kontrollige, et meeskonnale oleks rakendatud roll **topeltkirjutuse rakenduse kasutaja**. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Uuendusest andmeolemite värskendamine

1. Avage Finance'i keskkonnas tööruum **Andmehaldus** ja seejärel avage leht **Raamistiku parameetrid**.
2. Valige vahekaardil **Olemi sätted** suvand **Olemi loendi värskendamine**.
3. Olemi värskendamise kinnitamiseks valige **Sulge**.

 > [!NOTE]
 > Selle toimingu lõpule viimine võtab aega umbes 20 minutit. Teid teavitatakse, kui värskendamine on lõpule viidud.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Topeltkirjutuse vastenduste värskendamine

1. Valige tööruumis **Andmehaldus** valik **Topeltkirjutus**.
2. Valige **Rakenda lahendused**, valige loendist mõlemad lahendused ja seejärel valige **Rakenda**.
3. Valige lehel **Topeltkirjutus** järgmised tabelivastendused ja seejärel valige **Peata**.

    - **Project Operationsi integratsiooni tegelikud näitajad (msdyn_actuals)**
    - **Project Operationsi integratsiooni projekti kulukategooriad (msdyn_expensecategories)**
    - **Project Operationsi integratsiooni tegelike näitajate projekti kulude ekspordi olem (msdyn_expenses)**

4. Rakendage lehel **Tabelivastenduse versioon** vastenduse uus versioon kõigile kolmele olemile.
5. Valige vastenduste taaskäivitamiseks lehel **Topeltkijutamine** käsk Käivita.
6. Valige vastenduste loendist vastendus **Pearaamat (msdyn_ledgers)** koos kõige eeltingimustega ja valige märkeruut **Algne sünkroonimine**. 
7. Valige **Algse sünkroonimise ülem** väljal **Finants- ja äritoimingute rakendused** ja seejärel valige **Käivita**.
 
 ![Pearaamatu vastenduse sünkroonimine.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]