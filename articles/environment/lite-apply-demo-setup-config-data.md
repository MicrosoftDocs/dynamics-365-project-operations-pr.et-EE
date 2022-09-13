---
title: Demoseadistamise ja konfiguratsiooniandmete rakendamine – liht
description: Sellest artiklist leiate teavet selle kohta, kuidas rakendada Project Operationsi jaoks demohäälestust ja konfiguratsiooniandmeid.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9a3a99c326b7ebbdfa859c3298b35e910af0eb2a
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9409985"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Project Operationsi demoseadistamise ja konfiguratsiooniandmete rakendamine – liht 

_**Lite’i juurutamine – tehing näidisarveldusele_



## <a name="prerequisites"></a>eeltingimused

Enne konfigureerimise alustamist peab teil Dataverse olema ette valmistatud keskkond Dynamics 365 Project Operations.


## <a name="instructions"></a>Juhised

1. Laadige alla [Master Data pakett](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Liikuge kausta *ProjOpsSampleSetupData – CE ainult CMT* ja käivitage täitmisfail *DataMigrationUtility*.
3. Valige Common Data Service'i konfiguratsiooni migreerimise viisardi (CMT) 1. lehel käsk **Impordi andmed** ja seejärel valige **Jätka**.

    ![Konfiguratsiooni migreerimine.](./media/1ConfigurationMigration.png)

4. Valige CMT viisardi lehel 2 **Microsoft 365** **Juurutuse tüübiks**.
5. Valige märkeruudud **Saadaolevate asutuste loendi kuvamine** ja **Kuva täpsemad**.
6. Valige oma rentniku piirkond, sisestage oma mandaat ja valige seejärel **Logi sisse**.

   ![Konfiguratsiooni sisselogimine.](./media/2ConfigurationSignin.png)

7. Valige 3. lehel rentniku organisatsioonide loendist organisatsioon, kuhu soovite demo andmed importida ja valige seejärel **Logi sisse**.
8. Valige lehel 4 lahti pakkimata kaustast ZIP-fail *SampleSetupAndConfigData*, *ProjOpsSampleSetupData – CE ainult CMT*.

   ![Zip-fail.](./media/3ZipFile.png)

   ![Vali fail.](./media/4SelectAFile.png)

9. Pärast ZIP-faili valimist valige käsk **Impordi andmed**.

   ![Importimise andmed.](./media/5ImportData.png)

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

    ![Lõpetage importimine.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
