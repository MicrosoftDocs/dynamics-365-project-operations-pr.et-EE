---
title: Demoseadistamise ja konfiguratsiooniandmete rakendamine
description: Selles teemas kirjeldatakse, kuidas rakendada demoseadistamist ja konfiguratsiooni andmeid Project Operationsis.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948827"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Project Operations Lite’i juurutusele – tehing näidisarveldusele demoseadistamise või konfiguratsiooniandmete rakendamine

_**Lite’i juurutamine – tehing näidisarveldusele_

1. Laadige alla [Master Data pakett](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Liikuge kausta *ProjOpsDemoDataSetupAndMaster – integreeritud CMT* ja käitage käivitatav fail *DataMigrationUtility*.
3. Valige Common Data Service'i konfiguratsiooni migreerimise viisardi (CMT) 1. lehel käsk **Impordi andmed** ja seejärel valige **Jätka**.

![Konfiguratsiooni migreerimine](./media/1ConfigurationMigration.png)

4. Valige CMT viisardi lehel 2 **Office 365** **Juurutuse tüübiks**.
5. Valige märkeruudud **Saadaolevate asutuste loendi kuvamine** ja **Kuva täpsemad**.
6. Valige oma rentniku piirkond, sisestage oma mandaat ja valige seejärel **Logi sisse**.

![Konfiguratsioon Sisselogimine](./media/2ConfigurationSignin.png)

7. Valige 3. lehel rentniku organisatsioonide loendist organisatsioon, kuhu soovite demo andmed importida ja valige seejärel **Logi sisse**.
8. Valige lahtipakitud kaustast leheküljel 4 zip fail *MasterAndSetupData*, *ProjOpsDemoDataSetupAndMaster – integreeritud CMT*.

![Zip-fail](./media/3ZipFile.png)

![Faili valimine](./media/4SelectAFile.png)

9. Pärast ZIP-faili valimist valige käsk **Impordi andmed**.

![Importimise andmed](./media/5ImportData.png)

10. Importimine töötab umbes kaks kuni kümme minutit, olenevalt teie võrguühenduse kiirusest. Pärast selle lõpuleviimist väljuge CMT-i viisardist. 
11. Kontrollige organisatsioonist järgmise 20 olemi andmeid.

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
- Arve sageduse üksikasjad
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
