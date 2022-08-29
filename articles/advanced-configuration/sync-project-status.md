---
title: Sünkrooni projekti olek, et vältida sisenemist suletud projektidesse
description: Selles artiklis selgitatakse, kuidas sünkroonida projekti olekut, et vältida mitteaktiivsete või suletud projektide sisestamist.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348098"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sünkrooni projekti olek, et vältida sisenemist suletud projektidesse

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

## <a name="scenario"></a>Stsenaarium

Contoso on ressursi-/varumata stsenaariumide jaoks Microsoftiga Dynamics 365 Project Operations reaalajas. Osana tavapärasest äritegevusest võib projektid lõpule viia või ootele panna. Saate projekti inaktiveerida, et tagada kulude või arvete loomine.

## <a name="solution"></a>Lahendus

### <a name="prerequisites"></a>eeltingimused

-   Microsoft Dynamics 365 Finance 10.0.29 või uuem versioon peab olema installitud.
-   Projektide V2 (msdyn-projektid\_) topeltkirjutuskaardi 1.0.0.3 tuleb installida või käsitsi konfigureerida, nagu allpool kirjeldatud.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Project Operationsi integreeritud projektide V2 topeltkirjutuskaardi värskendatud versiooni loomine

Project Operations Projects V2 topeltkirjutusega kaardi värskendamiseks tehke järgmist.

1. Avage **tööruum Andmehaldus** ja valige **Topeltkirjutus**.
2. Valige **paan Topeltkirjutus**.
3. Otsige veerust T-tabeli **kaart** üles ja valige **Project V2 (msdyn-projektid\_)** ning seejärel valige Peata.
4. Valige kaardi avamiseks kaardi nimi ja seejärel valige **[None]**.
5. Valige dialoogiboksis **Veeru valimine statecode \[Project Status\]** ja seejärel valige OK. Loendi kitsendamiseks saate filtri väärtusesse tippida **oleku**.
6.  Valige **teisendamise** **redigeerimiseks veerus Kaardi tüüp** käsk Lisa või redigeeri teisendust.
7.  Valige **teisendamistüübist** **Väärtusmap**.
8.  Valige **Lisa väärtuse vastendus** ja seejärel lisage järgmised **klahvid** ja **väärtused**.

   Klahv       | Väärtus 
   ----------|-------
   InProcess | 0     
   Lõpule viidud | 1     

![Kuvatõmmis, millel on kujutatud kahekordse kirjutamise vastendamine](media/projectstage-dw-mapping.png)

9. Valige **Salvesta**.
10. Valige lehe Dual-write > Projects V2 (msdyn_projects) **ülaosas** käsk **Salvesta nimega**.
11. Valige väljal Publisher **tabelist** **Add (Lisa) väärtus** CDS Default Publisher (CDS-i vaikeväljaandja **).**
12. Määrake välja **Versioon** väärtuseks 1.0.0.3.
13. Tippige **kirjeldus** ja seejärel valige **Salvesta**.
14. Valige kaardi käivitamiseks lehe Dual-write > Projects V2 (msdyn_projects) ülaosas **käsk** Run (Käivita **)** ja seejärel sekekteerige **Jah,kui** teil palutakse enne käivitamist kinnitada. 

### <a name="close-a-newly-completed-project"></a>Äsja lõpetatud projekti sulgemine

Dynamics 365 Finance kasutab **projekti etapi** välja, et eristada pooleliolevaid **või** lõpetatud **projekte**. **Lõpetatud** projektidega ei saa kaasneda kulusid ega esitada klientidele arveid.

1. Desaktiveerimiseks avage projekt.
2. Valige lindilt käsk **Inaktiveeri**.

> [!NOTE]
> Saate projekti kas inaktiveerida või sulgeda, kuna mõlemad käituvad rahanduse kontekstis ühtemoodi.

3. Avage jaotises Rahandus **loendileht** Kõik projektid.
4. Veenduge, et desaktiveeritud projekti loendis ei kuvataks.
5. Muutke loendi kohal olevas **kuvaprojektide** filtris väärtust Aktiivne **väärtuseks** **Kõik**.
6. Nüüd näete desaktiveeritud projekti.

Kui proovite rakenduses Finance selle projekti vastu aega või kulu logida, ei tohiks te projekti valiku tegemiseks näha. Kui sisestate kulule projekti numbri käsitsi, näete teadet nagu "Projekti etapp on lõpetatud, ei luba projektis salvestamist". Arveldus- ja muud arveldusfunktsioonid tuleks keelata, kuna need on suletud projekti kontekstis.

