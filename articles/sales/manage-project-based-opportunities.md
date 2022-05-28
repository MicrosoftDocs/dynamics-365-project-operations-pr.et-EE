---
title: Projektipõhiste müügivõimaluste haldamine
description: Selles teemas antakse teave projektidega seotud müügivõimalustega töötamise kohta.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f39940ac063a8c202f33797ed649518907563e31
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600415"
---
# <a name="manage-project-based-opportunities"></a>Projektipõhiste müügivõimaluste haldamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Projektipõhiste ettevõtetel on tarne toimingud tavaliselt hajutatud mitmesse riiki ja geograafilisse piirkonda. Projekti täitmise ja tarnimise kulu võib varieeruda vastavalt sellele, milline geograafiline piirkond või allüksustel tarnet haldab. See võib omakorda mõjutada tehingu marginaale. Projektipõhiste teenuste tarne tähendab tavaliselt suurt hulka inimressursi aega, märkimisväärseid kulusid reisidele, materiaalseid kulusid ja muid kulusid.

Projektipõhised müügivõimalused rakenduses Dynamics 365 Project Operations on kujundatud laiendustega rakendusele Dynamics 365 Sales. Teemas antakse teavet erinevate väljade ja äriloogikate kohta, mis sisaldub täiendavas funktsionaalsuses, mida projektipõhised ettevõtted vajavad projektipõhiste müügivõimaluste haldamiseks.

## <a name="view-all-project-based-opportunities"></a>Kõigi projektipõhiste müügivõimaluste vaatamine

Kõigi projektipõhiste müügivõimaluste loend kuvatakse lehel **Müügivõimalused**. 

1. Minge jaotisse **Müük** > **Müügivõimalused**.
2. Kasutage suvandit **Vaate vahetaja**, et valida müügivõimaluste jaoks teine filtreeritud vaade. Nende vaadete ja navigeerimisvalikute konfigureerimiseks saate luua oma vaated kohandatud filtrikriteeriumidega.

Projekti müügivõimalusi saab luua või kustutada selle loendi lehelt või üksikasjade lehelt.

## <a name="business-process-flow-for-project-based-deals"></a>Projektipõhiste tehingute äriprotsessi voog

Project Operationsi projektipõhistes tehingutes toetatakse järgmisi äriprotsessi voogusid.

- Müügivihjest müügivõimaluseni äriprotsess
- Müügivõimaluse müügiprotsess

### <a name="lead-to-opportunity-business-process"></a>Müügivihjest müügivõimaluseni äriprotsess 
Müügivihjest müügivõimaluseni äriprotsess toetab järgmisi etappe.

| Etapp | Vastendatud olem | Funktsionaalsus |
| --- | --- | --- |
| Sobivaks kinnitamine | Müügivihje | Konto, kontakti ja müügivõimaluse loomiseks müügivihje kvalifitseerimine. |
| Arendage | Müügivõimalus | Müügivõimaluse arendamine, et lisada lisateavet seotud töö, peamiste sidusrühmade ja konkurentide kohta. |
| Soovita | Müügivõimalus | Ettepaneku väljaarendamine ja sisemise läbivaatuse meeskonnalt heakskiidu saamine. |
| Saate dialoogiakna sulgeda | Müügivõimalus | Tehingu sulgemiseks müügivõimaluse võitmine. |

### <a name="opportunity-sales-process"></a>Müügivõimaluse müügiprotsess
Project Operationsi müügivõimaluse müügiprotsess on müügivõimaluse müügiprotsessi ärivoo laiendus rakenduses Sales. See äriprotsess on loodud valmislahendusena, et toetada projektipõhise müügivõimaluse järgmisi etappe.

| Etapp | Vastendatud olem | Funktsionaalsus |
| --- | --- | --- |
| Sobivaks kinnitamine | Müügivõimalus | Konto, kontakti ja müügivõimaluse loomiseks müügivihje kvalifitseerimine. |
| Soovita | Hinnapakkumine | Ettepaneku väljaarendamine projekti hinnapakkumist kasutades ja sisemise läbivaatuse meeskonnalt heakskiidu saamine. |
| Leping | Projekti leping | Hinnapakkumise võitmiseks looge leping ja alustage projekti täitmist ja tarnimist. |
| Saate dialoogiakna sulgeda | Projekti leping | Lõpetage töö edukalt ja sulgege projekti leping. |

> [!NOTE]
> Kui teie projektipõhine tehing algas müügivihjega, on müügivihjest müügivõimaluseks äriprotsess tähtsam.
>
> Kui teie projektipõhine tehing algas müügivõimalusega, on müügivõimaluse müügiprotsess tähtsam.

Saate toote äriprotsessi voog redigeerida või luua oma äriprotsessi voogusid, et vajaduse kohaselt müügiprotsessi jälgida. Lisateavet äriprotsessi voo kohta leiate jaotisest [Äriprotsessi voogude ülevaade](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]