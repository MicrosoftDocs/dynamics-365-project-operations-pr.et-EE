---
title: Demoseadistamise ja konfiguratsiooniandmete rakendamine – liht
description: See artikkel kirjeldab, kuidas rakendada demoseadistamist ja konfiguratsiooni andmeid rakenduses Project Operations.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811020"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Project Operationsi demoseadistamise ja konfiguratsiooniandmete rakendamine – liht 

_**Lite’i juurutamine – tehing näidisarveldusele_



## <a name="prerequisites"></a>eeltingimused

Enne konfigureerimise alustamist peab teil olema teenuse Dataverse keskkond rakenduse Dynamics 365 Project Operations jaoks ette valmistatud.


## <a name="instructions"></a>Juhised

1. Laadige alla [häälestusandmete pakett](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Liikuge kausta *ProjOpsSampleSetupData – CE ainult CMT* ja käivitage täitmisfail *DataMigrationUtility*.
1. Valige Common Data Service'i konfiguratsiooni migreerimise viisardi (CMT) 1. lehel käsk **Impordi andmed** ja seejärel valige **Jätka**.

    ![Konfiguratsiooni migreerimine.](./media/1ConfigurationMigration.png)

1. Valige CMT viisardi lehel 2 **Microsoft 365** **Juurutuse tüübiks**.
1. Valige märkeruudud **Saadaolevate asutuste loendi kuvamine** ja **Kuva täpsemad**.
1. Valige oma rentniku piirkond, sisestage oma mandaat ja valige seejärel **Logi sisse**.

   ![Konfiguratsiooni sisselogimine.](./media/2ConfigurationSignin.png)

1. Valige 3. lehel rentniku organisatsioonide loendist organisatsioon, kuhu soovite demo andmed importida ja valige seejärel **Logi sisse**.
1. Valige lehel 4 lahti pakkimata kaustast ZIP-fail *SampleSetupAndConfigData*, *ProjOpsSampleSetupData – CE ainult CMT*.

   ![Zip-fail.](./media/3ZipFile.png)

   ![Vali fail.](./media/4SelectAFile.png)

1. Pärast ZIP-faili valimist valige käsk **Impordi andmed**.

   ![Importimise andmed.](./media/5ImportData.png)

1. Importimine töötab umbes kaks kuni kümme minutit, olenevalt teie võrguühenduse kiirusest. Pärast selle lõpuleviimist väljuge CMT-i viisardist. 
1. Kontrollige organisatsioonist järgmise 18 olemi andmeid.

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
