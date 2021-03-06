---
title: Project Operationsi konfiguratsiooniandmete seadistamine rakendamine rakenduses Common Data Service
description: Selles teemas kirjeldatakse konfiguratsiooni andmete seadistamist ja rakendamist Project Operationsis.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948830"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a>Project Operationsi konfiguratsiooniandmete seadistamine rakendamine rakenduses Common Data Service

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

## <a name="install-setup-and-configuration-data"></a>Seadistuse ja konfiguratsiooniandmete installimine

1. Laadige alla, avage ja pakkige lahti [Seadistuse ja konfiguratsiooni andmepakett](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Liikuge lahtipakitud kausta ja käivitage käivitatav fail *DataMigrationUtility*.
3. Valige Common Data Service'i konfiguratsiooni migreerimise viisardi (CMT) 1. lehel käsk **Impordi andmed** ja seejärel valige **Jätka**.

![Konfiguratsiooni migreerimine](./media/1ConfigurationMigration.png)

4. Valige CMT viisardi lehel 2 **Office 365** **Juurutuse tüübiks**.
5. Valige märkeruudud **Saadaolevate asutuste loendi kuvamine** ja **Kuva täpsemad**.
6. Valige oma rentniku piirkond, sisestage oma mandaat ja valige **Logi sisse**.

![Konfiguratsioon Sisselogimine](./media/2ConfigurationSignin.png)

7. Valige 3. lehel rentniku organisatsioonide loendist see organisatsioon, kuhu soovite demo andmed importida ja valige **Logi sisse**.
8. Valige lahtipakitud kaustast leheküljel 4 zip fail *SampleSetupAndConfigData*.

![ZIP-faili valimine](./media/3ZipFile.png)

![Faili valimine](./media/4SelectAFile.png)

9. Pärast ZIP-faili valimist valige käsk **Impordi andmed**.

![Impordi andmed](./media/5ImportData.png)

10. Importimine töötab umbes kaks kuni kümme minutit, olenevalt teie võrguühenduse kiirusest. Pärast importimise lõpuleviimist väljuge CMT-i viisardist. 
11. Kontrollige organisatsioonist järgmise 19 olemi andmeid.

  - Valuuta
  - Organisatsiooniüksus
  - Kontakt
  - Maksurühm
  - Kliendirühm
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

![Lõpetage importimine](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Värskendage Project Operationsi konfiguratsioonid

1. Liikuge CE keskkonda. Selle leiate, kui avate [Power Platformi halduskeskuse](https://admin.powerplatform.microsoft.com/environments), valides keskkonna ja seejärel valides suvandi **Avatud keskkond**. 

![Avatud keskkond](./media/7OpenEnvironment.png)

2. Oma kasutajale broneeritava ressursi loomiseks minge jaotisse **Projektid** > **Ressursid** ja valige seejärel **Uus**.

![Reserveeritavad ressursid](./media/8BookableResources.png)

3. Valige administraator vahekaardil **Üldine**. Kontrollige, kas ajavöönd vastab teie asukohale. 

![Uus broneeritav ressurss](./media/9NewBookableResource.png)

4. Valige vahekaardil **Kavandamine** väljal **Ettevõte** ettevõtteks **USPM** ja seejärel valige **Salvesta**. 

![Kavandamise vahekaart](./media/10SchedulingTab.png)

5. Valige vahekaart **Töötunnid**.  

![Tööaeg](./media/11WorkHours.png)

6. Topeltklõpsake kalendris mis tahes väärtust ja valige **Redigeeri** > **Kõik sarja sündmused**. 

![Töökalender](./media/12WorkCalendar.png)

7. Muutke tööaega kaheksa (8) tunniseks tööpäevaks, märkige nädalavahetused mitte-tööpäevad ja veenduge, et ajavöönd vastab teie omale. 
8. Valige **Salvesta ja sule**.

![Kalendri värskendamine](./media/13UpdateCalendar.png)

9. Minge jaotisse **Sätted** > **Kalendri mallid** ja valige **Uus**.
 
 ![Kalendri mallid](./media/14CalendarTemplates.png)
 
 10. Sisestage nimi, valige loodud malli ressurss ja seejärel valige **Salvesta**. 
 
 ![Kalendri malli salvestamine](./media/15SaveCalendarTemplate.png)
 
 11. Minge jaotisse **Parameetrid** ja topeltklõpsake kirjel. 
 
 ![Projekti parameetrid](./media/16ProjectParameters.png)
 
12. Värskendage järgmised väljad.

 - **Vaikeettevõte**: USPM
 - **Vaike-organisatsiooniüksus**: Contoso Robotics Global
 - **Arve sagedus**: seitsmes ja viimane päev
 - **Tööaja mall**: muutke loodud malliks.

13. Valige **Salvesta**. 

![Värskendatud projekti parameetrid](./media/17UpdatedProjectParameters.png)
