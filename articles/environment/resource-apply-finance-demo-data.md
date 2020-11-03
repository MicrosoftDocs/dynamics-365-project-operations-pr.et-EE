---
title: Project Operationsi demoandmete rakendamine rakenduse Finance pilvepõhises keskkonnas
description: Selles teemas kirjeldatakse Project Operationsi demoandmete rakendamist Dynamics 365 Finance pilvepõhisesse keskkonda.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b9af6c71b61840f4ffdf2892d8e7e5bbf0f8df67
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096617"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a>Project Operationsi demoandmete rakendamine rakenduse Finance pilvepõhises keskkonnas

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

> [!IMPORTANT]
> See teema on rakendatav ainult Microsoft Dynamics 365 Finance'i versiooniga 10.0.13 ja seda saab teha ainult pilvepõhises keskkonnas. **ENNE** keskkonnale kvaliteedivärskenduste rakendamist viige lõpule selle teema etapid.

1. Avage oma LCS-i projektis leht **Keskkonna üksikasjad**. Pange tähele, et see sisaldab Remote Desktop Protocoli (RDP) abil keskkonnaga ühenduse loomiseks vajalikke üksikasju.

![i keskkonna üksikasjad](./media/1EnvironmentDetails.png)

Esimene esiletõstetud mandaatide komplekt on kohaliku ettevõtte mandaat ja sisaldab hüperlinki kaugtöölaua ühendusele. Mandaat sisaldab keskkonna administraatori kasutajanime ja parooli. Teist mandaatide kogumit kasutatakse selles keskkonnas SQL-i serverisse sisselogimiseks.

2. Liikuge keskkonda läbi hüperlingi jaotises **Kohalikud kontod** ja kasutage autentimiseks **Kohaliku konto mandaati**.
3. Minge jaotisse **Interneti infoteenused** > **Rakenduste kogumid** > **AOSService** ja peatage teenus. Peatate praegu teenuse, et saaksite minna edasi SQL-i andmebaasi asendamisega.

![AOS-i peatamine](./media/2StopAOS.png)

4. Minge jaotisse **Teenused** ja peatage järgmised kaks üksust.

- Microsoft Dynamics 365 Unified Operations: paketthalduse teenus
- Microsoft Dynamics 365 Unified Operations: andmete importimise eksportimise raamistik

![Peatage teenused](./media/3StopServices.png)

5. Avage Microsoft SQL Server Management Studio. Logige sisse SQL serveri mandaadiga ja kasutage axdbadmin kasutajat ja parooli LCS-i lehelt **Keskkondade üksikasjad**.

![SQL Server Management Studio](./media/4SSMS.png)

6. Avage Object Exploereris **Andmebaasid** ja otsige üles **AXDB**. Andmebaasi asendate uue andmebaasiga, mis asub [allalaadimiskeskuses](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Kopeerige ZIP-fail VM-i, millesse oled kaugelt sisenenud, ja pakkige zip-faili sisu lahti.
8. Paremklõpsake SQL Server Management Studios valikul **AxDB** ja seejärel valige **Tööülesanded** > **Taasta** > **Andmebaas**.

![Andmebaasi taastamine](./media/5RestoreDatabase.png)

9. Valige **Lähteseade** ja liikuge kopeeritud zip-failist lahtipakitud faili juurde.

![Lähteseadmed](./media/6SourceDevice.png)

10. Valige **Suvandid** ja seejärel valige **Kirjuta olemasolev andmebaas üle** ja **Sulge olemasolevad ühendused sihtkoha andmebaasiga**. 
11. Valige **OK**.

![Sätete taastamine](./media/7RestoreSetting.png)

Teile saadetakse kinnitus, et AXDB-i taastamine õnnestus. Pärast selle kinnituse saamist saate SQL Services Management Studio sulgeda.

12. Minge tagasi jaotisse **Interneti infoteenused** > **Rakenduste kogumid** > **AOSService** ja käivitage AOSService.
13. Minge jaotisse **Teenused** ja käivitage kaks teenust, mille varem peatasite.

14. Otsige üles selle VM-i AdminUserProvisioning tööriist. Vaadake asukohta K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Käivitage .ext-faili kasutades oma kasutaja aadressi väljal **Meiliaadress**. 
16. Valige käsk **Esita**.

![Administraatori ettevalmistamine](./media/8AdminUserProvisioning.png)

Selle lõpuleviimiseks kulub mõni minut. Peaksite saama kinnituse, et administraatori kasutaja värskendamine õnnestus.

17. Lõpuks käivitage administraatorina käsuviip ja tehke iisreset

![IIS reset](./media/9IISReset.png)

18. Sulgege kaugtöölaua seanss ja kasutage LCS-i lehte **Keskkonna üksikasjad** , et logida keskkonda sisse ja kontrollida, et see töötab ootuspäraselt.

![Finance and Operations](./media/10FinanceAndOperations.png)
