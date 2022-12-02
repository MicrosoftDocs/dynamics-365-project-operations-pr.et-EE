---
title: Projekti oleku sünkroonimine suletud projektidega seotud kirje vältimiseks
description: See artikkel selgitab, kuidas sünkroonida projekti olekut, et vältida sisenemist passiivsetesse või suletud projektidesse.
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
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Projekti oleku sünkroonimine suletud projektidega seotud kirje vältimiseks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

## <a name="scenario"></a>Stsenaarium

Contoso on reaalajas koos rakenduse Microsoft Dynamics 365 Project Operations ressursi/mittelaopõhiste stsenaariumide jaoks. Tavalise äritegevuse osana võidakse projekte lõpetada või ootele panna. Saate projekti passiivseks muuta tagamaks, et kulusid ega arveid ei teki.

## <a name="solution"></a>Lahendus

### <a name="prerequisites"></a>eeltingimused

-   Rakendus Microsoft Dynamics 365 Finance 10.0.29 või uuem versioon peab olema installitud.
-   Topeltkirjutuskaart 1.0.0.3 projektide V2 (msdyn\_projektid) jaoks tuleb installida või käsitsi konfigureerida, nagu allpool kirjeldatud.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Looge rakenduse Project Operations integratsiooniprojektide V2 topeltkirjutuskaardi värskendatud versioon

Rakenduse Project Operations projektide V2 topeltkirjutuskaardi värskendamiseks tehke järgmist.

1. Minge tööruumi **Andmehaldus** ja valige **Topeltkirjutus**.
2. Valige paan **Topeltkirjutus**.
3. veerust T **Tabelikaart** leidke ja valige **Projekt V2 (msdyn\_projektid)** ning seejärel valige Stop.
4. Valige kaardi avamiseks kaardi nimi ja seejärel **[Puudub]**.
5. Valige dialoogiboksis Veeru valimine **olekukood \[Projekti olek\]** ja seejärel OK. Loendi kitsendamiseks võite filtri väärtusesse sisestada **olek**.
6.  Teisenduse muutmiseks valige veerus **Transformeerimise lisamine või redigeerimine** veerus **kaardi tüüp**.
7.  Valige jaotisest **Transformeerimise tüüp** **ValueMap**.
8.  Valige **Väärtuse vastendamise lisamine** ja seejärel lisage järgmised **Võtmed** ja **Väärtused**:

   Klahv       | Väärtus 
   ----------|-------
   InProcess | 0     
   Lõpule viidud | 1     

![Kuvatõmmis, mis näitab topeltkirjutuse vastendamist](media/projectstage-dw-mapping.png)

9. Valige **Salvesta**.
10. Valige lehe **Topeltkirjutus > Projektid V2 (msdyn_projektid)** ülaosast **Salvesta kui**.
11. Valige **Tabeli lisamine** väljal **Väljaandja** field, select **CDS-i vaikeväljaandja**.
12. Määrake välja **Versioon** väärtuseks 1.0.0.3.
13. Sisestage **Kirjeldus** ja seejärel valige **Salvesta**.
14. Valige lehe **Topeltkirjutus > Projektid V2 (msdyn_projektid)** ülaosast kaardi käivitamiseks **Käivita** ja seejärel valige **Jah**, kui teil palutakse enne käivitamist kinnitada. 

### <a name="close-a-newly-completed-project"></a>Sulgege äsja lõpetatud projekt

Dynamics 365 Finance kasutab välja **projekti etapp**, et eristada projekte **protsessis** või **lõpetatud**. **Lõpetatud** projektid ei saa kulusid kanda ega klientidele arveid esitada.

1. Avage inaktiveerimiseks projekt.
2. Valige lindilt **Inaktiveeri**.

> [!NOTE]
> Saate projekti inaktiveerida või sulgeda, kuna need mõlemad käituvad Rahanduse kontekstis ühtemoodi.

3. Avage jaotises Rahandus leht **Kõik projektid**.
4. Veenduge, et inaktiveeritud projekti ei kuvata loendis.
5. Muutke loendi kohal olevas filtris **kuva projektid** väärtust **Aktiivne** väärtuseks **Kõik**.
6. Nüüd näete inaktiveeritud projekti.

Kui proovite selle projekti jaoks aega või kulusid Rahanduses registreerida, ei tohiks te seda projekti valimiseks näha. Kui sisestate kulule projekti numbri käsitsi, näete teadet „Projekti etapp on lõpetatud ei luba projekti salvestada“. Arveldus- ja muud arveldusfunktsioonid tuleks keelata, kuna need on suletud projekti kontekstis.

