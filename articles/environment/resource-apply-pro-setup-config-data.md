---
title: Konfiguratsiooniandmete häälestamine ja rakendamine teenuses Microsoft Dataverse
description: See artikkel kirjeldav konfiguratsiooni andmete seadistamist ja konfiguratsiooni rakendamist rakenduses Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b09d3ea7348082a0467fd7b47918c9e00d1f1e8c
ms.sourcegitcommit: 8edd24201cded2672cec16cd5dc84c6a3516b6c2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9230232"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Konfiguratsiooniandmete häälestamine ja rakendamine teenuses Common Data Service 

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_



## <a name="prerequisites"></a>eeltingimused

Enne andmete konfigureerimise alustamist teenuses Microsoft Dataverse peavad olema täidetud järgmised eeltingimused.

1.  Valmistage Dataverse keskkond ja rakenduse Dynamics 365 Finance’i keskkond Project Operationsi jaoks ette.
2.  Rakenduse Dynamics 365 Finance juriidilise isiku teavet jagatakse Dataverse keskkonnaga. See tähendab, et **Ettevõte** olemil rakenduses Dataverse on järgmised ettevõtte kirjed.
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Seadistuse ja konfiguratsiooniandmete installimine

1. Laadige alla, avage ja pakkige lahti [Seadistuse ja konfiguratsiooni andmepakett](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).
2. Liikuge lahtipakitud kausta ja käivitage käivitatav fail *DataMigrationUtility*.
3. Valige Common Data Service'i konfiguratsiooni migreerimise viisardi (CMT) 1. lehel käsk **Impordi andmed** ja seejärel valige **Jätka**.

![Konfiguratsiooni migreerimine.](./media/1ConfigurationMigration.png)

4. Valige CMT viisardi lehel 2 **Microsoft 365** **Juurutuse tüübiks**.
5. Valige märkeruudud **Saadaolevate asutuste loendi kuvamine** ja **Kuva täpsemad**.
6. Valige oma rentniku piirkond, sisestage oma mandaat ja valige **Logi sisse**.

![Konfiguratsiooni sisselogimine.](./media/2ConfigurationSignin.png)

7. Valige 3. lehel rentniku organisatsioonide loendist see organisatsioon, kuhu soovite demo andmed importida ja valige **Logi sisse**.
8. Valige lahtipakitud kaustast leheküljel 4 zip fail *SampleSetupAndConfigData*.

![ZIP-faili valimine.](./media/3ZipFile.png)

![Vali fail.](./media/4SelectAFile.png)

9. Pärast ZIP-faili valimist valige käsk **Impordi andmed**.

![Importimise andmed.](./media/5ImportData.png)

10. Importimine töötab umbes kaks kuni kümme minutit, olenevalt teie võrguühenduse kiirusest. Pärast importimise lõpuleviimist väljuge CMT-i viisardist. 
11. Kontrollige organisatsioonist järgmise 26 olemi andmeid.

  - Valuuta
  - Kontoplaan
  - Finantskalender
  - Valuuta vahetuskursside tüübid
  - Maksmise päev
  - Maksegraafik
  - Maksetähtaeg
  - Organisatsiooniüksus
  - Kontaktandmed
  - Maksurühm
  - Kliendirühm
  - Hankijate rühm
  - Üksus
  - Ühikurühm
  - Hinnakiri
  - Projekti parameetrite hinnakiri
  - Arve sagedus
  - Reserveeritava ressursi kategooria
  - Kande kategooria
  - Kulukategooria
  - Rolli hind
  - Kandekategooria hind
  - Tunnus
  - Broneeritav ressurss
  - Broneeritava ressursi kategooria seos
  - Reserveeritava ressursi tunnus

![Lõpetage importimine.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Värskendage Project Operationsi konfiguratsioonid

1. Liikuge CE keskkonda. Selle leiate, kui avate [Power Platformi halduskeskuse](https://admin.powerplatform.microsoft.com/environments), valides keskkonna ja seejärel valides suvandi **Avatud keskkond**. 

![Avatud keskkond.](./media/7OpenEnvironment.png)

2. Oma kasutajale broneeritava ressursi loomiseks minge jaotisse **Projektid** > **Ressursid** ja valige seejärel **Uus**.

![Broneeritavad ressursid.](./media/8BookableResources.png)

3. Valige administraator vahekaardil **Üldine**. Kontrollige, kas ajavöönd vastab teie asukohale. 

![Uus broneeritav ressurss.](./media/9NewBookableResource.png)

4. Valige vahekaardil **Kavandamine** väljal **Ettevõte** ettevõtteks **USPM** ja seejärel valige **Salvesta**. 

![Kavandamise vahekaart.](./media/10SchedulingTab.png)

5. Valige vahekaart **Töötunnid**.  

![Töötunnid.](./media/11WorkHours.png)

6. Topeltklõpsake kalendris mis tahes väärtust ja valige **Redigeeri** > **Kõik sarja sündmused**. 

![Töökalender.](./media/12WorkCalendar.png)

7. Muutke tööaega kaheksa (8) tunniseks tööpäevaks, märkige nädalavahetused mitte-tööpäevad ja veenduge, et ajavöönd vastab teie omale. 
8. Valige **Salvesta ja sule**.

![Kalendri värskendamine.](./media/13UpdateCalendar.png)

9. Minge jaotisse **Sätted** > **Kalendri mallid** ja valige **Uus**.
 
 ![Kalendrimallid.](./media/14CalendarTemplates.png)
 
 10. Sisestage nimi, valige loodud malli ressurss ja seejärel valige **Salvesta**. 
 
 ![Kalendrimalli salvestamine.](./media/15SaveCalendarTemplate.png)
 
 11. Minge jaotisse **Parameetrid** ja topeltklõpsake kirjel. 
 
 ![Projekti parameetrid.](./media/16ProjectParameters.png)
 
12. Värskendage järgmised väljad.

 - **Vaikeettevõte**: USPM
 - **Vaike-organisatsiooniüksus**: Contoso Robotics Global
 - **Arve sagedus**: seitsmes ja viimane päev
 - **Tööaja mall**: muutke loodud malliks.

13. Valige **Salvesta**. 

![Värskendatud projekti parameetrid.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
