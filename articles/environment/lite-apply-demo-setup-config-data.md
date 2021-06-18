---
title: Demoseadistamise ja konfiguratsiooniandmete rakendamine – liht
description: Selles teemas kirjeldatakse, kuidas rakendada demoseadistamist ja konfiguratsiooni andmeid Project Operationsis.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997146"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Project Operationsi demoseadistamise ja konfiguratsiooniandmete rakendamine – liht 

_**Lite’i juurutamine – tehing näidisarveldusele_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Eeltingimused

Enne konfigureerimise alustamist peab teil olema teenuse Common Data Service (CDS) keskkond rakenduse Dynamics 365 Project Operations jaoks ette valmistatud.


## <a name="instructions"></a>Juhised

1. Laadige alla [Master Data pakett](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Liikuge kausta *ProjOpsSampleSetupData – CE ainult CMT* ja käivitage täitmisfail *DataMigrationUtility*.
3. Valige Common Data Service'i konfiguratsiooni migreerimise viisardi (CMT) 1. lehel käsk **Impordi andmed** ja seejärel valige **Jätka**.

    ![Konfiguratsiooni migreerimine](./media/1ConfigurationMigration.png)

4. Valige CMT viisardi lehel 2 **juurutuse tüübiks** **Microsoft 365**.
5. Valige märkeruudud **Saadaolevate asutuste loendi kuvamine** ja **Kuva täpsemad**.
6. Valige oma rentniku piirkond, sisestage oma mandaat ja valige seejärel **Logi sisse**.

   ![Konfiguratsioon Sisselogimine](./media/2ConfigurationSignin.png)

7. Valige 3. lehel rentniku organisatsioonide loendist organisatsioon, kuhu soovite demo andmed importida ja valige seejärel **Logi sisse**.
8. Valige lehel 4 lahti pakkimata kaustast ZIP-fail *SampleSetupAndConfigData*, *ProjOpsSampleSetupData – CE ainult CMT*.

   ![Zip-fail](./media/3ZipFile.png)

   ![Vali fail](./media/4SelectAFile.png)

9. Pärast ZIP-faili valimist valige käsk **Impordi andmed**.

   ![Importimise andmed](./media/5ImportData.png)

10. Importimine töötab umbes kaks kuni kümme minutit, olenevalt teie võrguühenduse kiirusest. Pärast selle lõpuleviimist väljuge CMT-i viisardist. 
11. Kontrollige organisatsioonist järgmise 18 olemi andmeid.

    -   Valuuta
    -   Kontaktettevõte
    -   Organisatsiooniüksus
    -   Kontaktandmed
    -   Üksus
    -   Ühikurühm
    -   Hinnakiri
    -   Projekti parameetrite hinnakiri 
    -   Arve sagedus
    -   Reserveeritava ressursi kategooria
    -   Kande kategooria
    -   Kulukategooria
    -   Rolli hind
    -   Kandekategooria hind
    -   Tunnus
    -   Broneeritav ressurss
    -   Broneeritava ressursi kategooria seos
    -   Reserveeritava ressursi tunnus

    ![Lõpetage importimine](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
