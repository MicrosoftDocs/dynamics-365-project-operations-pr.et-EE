---
title: Uue keskkonna ettevalmistamine
description: Selles teemas antakse teavet uue Project Operationsi keskkonna ettevalmistamise kohta.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642961"
---
# <a name="provision-a-new-environment"></a>Uue keskkonna ettevalmistamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas antakse teavet selle kohta, kuidas juurutada uut rakenduse Dynamics 365 Project Operations keskkonda ressursi-/mittelaopõhiste stsenaariumide jaoks.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Project Operationsi automaatse ettevalmistamise lubamine LCS projektis

Kasutage järgmisi samme, et lubada Project Operationsi automaatse ettevalmistamise voog oma LCS projekti jaoks.

1. Minge jaotisse [LCS](https://lcs.dynamics.com/v2) ja valige paan **Funktsioonide halduse eelvaade**.
2. Valige loendis **Eelvaate funktsioon** jaotis **Project Operationsi funktsioon** ja valige Project Operationsi lubamiseks suvand **Eelvaate funktsioon lubatud**.

> [!NOTE]
> Seda sammu teostatakse iga LCS projekti kohta vaid ühe korra.

## <a name="provision-a-project-operations-environment"></a>Project Operationsi keskkonna ettevalmistamine

1. Avage uue Dynamics 365 Finance [eelvaatekeskkonna](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) või [liivakasti-/töökeskkonna](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) juurutamine. 
2. Läbige **Keskkonna ettevalmistamise** viisard. 

> [!IMPORTANT]
> Veenduge, et valitud rakenduse versioon on 10.0.13 või uuem.

3. Project Operationsi ettevalmistamiseks valige jaotises **Täpsemad sätted** suvand **Common Data Service**. 
4. **Common Data Service seadistuse** lubamiseks valige **Jah** ja sisestage seejärel nõutavatele väljadele teave.

  - Nimetus
  - Regioon
  - Keel
  - Valuuta
 
5. Valige **Common Data Service malli** väljal suvand **Project Operations** 

6. Valige juurutamiseks keskkonna tüüp. Kordustellimusel põhinev prooviversioon võimaldab teil kasutada CDS-keskkonda 30 päeva jooksul. 

![Juurutamise sätted](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Kasutustingimuste tunnustamiseks valige suvand **Nõustun** ja seejärel valige juurutamise sätetesse naasmiseks **Valmis**.

![Juurutuse nõusolek](./media/2DeploymentConsent.png)

7. Täitke viisardi ülejäänud nõutavad väljad ja kinnitage juurutus. Keskkonna ettevalmistamise aeg varieerub vastavalt keskkonna tüübile. Ettevalmistamine võib kesta kuni kuus tundi.

  Pärast juurutuse edukat lõpuleviimist kuvatakse keskkonna olekuks **Juurutatud**.

8. Kontrollimaks, et keskkond on edukalt juurutatud, valige **Logi sisse** ja logige kontrollimiseks keskkonda sisse.

![i keskkonna üksikasjad](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Project Operations Finance'i demoandmete rakendamine (valikuline etapp)

Project Operations Finance'i demoandmete rakendamine 10.0.13 teenuseväljalaske pilvepõhisele keskkonnale, nagu on kirjeldatud [selles artiklis](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Värskenduste rakendamine Finance'i keskkonnale

Project Operations nõuab Finance'i keskkonda, mille rakenduse versioon on **10.0.13 (10.0.569.20009)** või uuem.

Võimalik, et peate selle versiooni saamiseks rakendama oma Finance'i keskkonnale kvaliteedivärskendusi.

1. Valige LCS-s lehel **Keskkonna üksikasjad** jaotises **Saadaolevad värskendused** suvand **Kuva värskendus**.

![Kuva värskendused](./media/5ViewUpdates.png)

2. Valige lehel **Binaarsed värskendused** suvand **Salvesta pakett**.

![Salvesta pakett](./media/6SavePackage.png)

3. Valige suvand **Vali kõik** ja seejärel **Salvesta pakett**.

![Vaadake üle ja salvestage värskendused](./media/7ReviewAndSaveUpdates.png)

4. Sisestage paketi nimi ja kirjeldus ning seejärel valige **Salvesta**. Olenevalt Internetiühendusest, võib see protsess võtta aega.

![Laadiga pakett varateeki üles](./media/8UploadPackageToAssetsLibrary.png)

5. Kui pakett on salvestatud, valige **Valmis** ja salvestage see pakett oma LCS projekti varateeki.

Paketi salvestamine ja valideerimine võib võtta ~ 15 minutit.

6. Värskenduse rakendamiseks navigeerige LCS-s lehele **Keskkonna üksikasjad** ja valige **Haldus** > **Rakenda värskendused**.

![Keskkondade haldamine](./media/9MaintainEnvironment.png)

7. Valige värskenduste loendist oma loodud pakett ja valige **Rakenda**.

![Värskenduste rakendamine](./media/10ApplyUpdates.png)

Keskkonna teenindamine võtab aega. Kui see on lõpule viidud, naaseb keskkond juurutatud olekusse.

![Keskkond juurutatud](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Topeltkirjutuse ühenduse loomine 

1. Minge oma LCS-i projektis lehele **Keskkonna üksikasjad**.
2. Tehke jaotises **Common Data Service'i keskkonnateave** valik **Lingi lahendusele CDS rakenduste jaoks**.
3. Kui link on valmis, valige uuesti **Lingi lahendusele CDS rakenduste jaoks**. Teid suunatakse ümber Finance'i topeltkirjutusse.

![Link CDS-le](./media/12LinktoCDS.png)

4. Valige **Rakenda lahendus**, et avada integreerimisel vastendatavad olemid.

![Rakenda lahendused](./media/13ApplySolutions.png)

5. Valige mõlemad lahendused, **Rakenduse Dynamics 365 Finance and Operations topeltkirjutamise olemikaart** ja **Rakenduse Dynamics 365 Project Operations topeltkirjutamise olemikaardid** ja valige seejärel suvand **Rakenda**.

![Lahenduste kinnitamine](./media/14ConfirmSolutions.png)

Pärast lahenduste rakendamist rakendatakse topeltkirjutusolemid keskkonnale.

![Lahenduste rakendamine](./media/15ApplyingSolutions.png)

Pärast olemite rakendamist loetletakse keskkonnas kõik saadaolevad vastendused.

![Topeltkirjutuse kaardid](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Värskendage andmeüksused pärast värskendamist

1. Minge Finance'i tööruumi **Andmehaldus**.

![Andmehalduse tööruum](./media/16DataManagement.png)

2. Valige paan **Raamistiku parameetrid**.

![Raamistiku parameetrid](./media/17FrameworkParameters.png)

3. Valige lehel **Olemi sätted** suvand **Värskenda olemiloendit**.

![Värskenda olemiloendit](./media/18RefreshEntityList.png)

Värskendamine võtab aega umbes 20 minutit. Teile kuvatakse teade, kui see on valmis.

![Värskendamise kinnitamine](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Käivitage Project Operationsi topeltkirjutuse kaardid

1. Minge oma LCS-i projektis lehele **Keskkonna üksikasjad**.
2. Tehke jaotises **Common Data Service'i keskkonnateave** valik **Lingi lahendusele CDS rakenduste jaoks**. Pärast lingi valimist suunatakse teid vastenduste olemite loendisse.
3. Käivitage kaardid vastavalt järgmises tabelis kirjeldatule. Veenduge, et järgite loendis kuvatavat jada.

| **Olemikaart** | **Värskenda olemit** | **Algne sünkroonimine** | **Algse sünkroonimise ülem** | **Käivita eeltingimused** | **Eeltingimuste esialgne sünkroonimine** |
| --- | --- | --- | --- | --- | --- |
| **Projekti ressursside rollid kõigile ettevõtetele (bookableresourcecategories)** | No | Ja | Common Data Service | No | Puudub |
| **Juriidilised isikud (cdm\_companies)** | No | Ja | Finance and Operationsi rakendused | No | Puudub |
| **Pearaamat (msdyn_ledgers)** | No | Ja | Finance and Operationsi rakendused | Ja | Jah, teenuse Finance and Operations rakendused |
| **Project Operationsi integratsiooni tegelikud näitajad (msdyn\_tegelikud)** | No | No | Puudub | Ja | No |
| **Projekti lepinguread (salesorderdetails)** | No | No | Puudub | No | No |
| **Projekti kande seoste integratsiooni olem (msdyn\_transactionconnections)** | No | No | Puudub | No | Puudub |
| **Project Operationsi integreerimise lepingurea vahe-eesmärgid (msdyn\_contractlinesscheduleofvalues)** | No | No | Puudub | No | Puudub |
| **Project Operationsi integratsiooni olem kuluprognooside jaoks (msdyn\_estimateslines)** | No | No | Puudub | No | Puudub |
| **Project Operationsi integreerimise projekti kulukategooriate ekspordi olem (msdyn\_expensecategories)** | No | No | Puudub | No | Puudub |
| **Project Operationsi integreerimise projekti kulude ekspordi olem (msdyn\_kulud)** | Ja | No | Puudub | No | Puudub |
| **Project Operationsi integratsiooni olem kestuse prognooside jaoks (msdyn\_resourceassignments)** | Ja | No | Puudub | No | Puudub |


4. Olemi värskendamiseks valige vastenduse nimi ja seejärel valige **Värskenda olemid**. 


![Kaardi värskendamine](./media/20RefreshMapping.png)

5. Pärast värskenduse lõpetamist käivitage vastendus. Enne järgmise vastenduse lubamist veenduge, et tabelis olev kaart oleks olekus **Töötab**. Suurema hulga eeltingimustega kaartide käitamine võib võtta aega.

Eeltingimustega kaartide käivitamiseks lubage ümberlülitusnupp **Kuva seostuvad olemikaardid**. Kui tabel näitab, et **Eeltingimuste esialgne sünkroonimine** on **Ei**, veenduge, et lipp **Esialgne sünkroonimine** oleks enne käivitamist kõigil eeltingimuse kaartidel **Väljas**.

![Käita kaart](./media/21RunMap.png)

6. Kontrollige, et kõik projektiga seotud kaardid oleksid töötavad olekus.

![Kõik kaardid töötavad](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>CDS-is konfiguratsiooniandmete rakendamine rakenduses Project Operations (valikuline)

Kui olete rakenduse Finance keskkonnale rakendanud demoandmeid, lugege jaotist [Teenuse Common Data Service rakenduses Project Operations konfiguratsiooniandmete seadistamine ja rakendamine](resource-apply-pro-setup-config-data.md), et rakendada CDS-i keskkonnale demoandmeid.


Teie Project Operationsi keskkond on nüüd ettevalmistatud ja konfigureeritud. 
