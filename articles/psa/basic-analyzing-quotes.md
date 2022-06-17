---
title: Projekti hinnapakkumiste analüüs
description: See artikkel annab teavet projektipakkumiste analüüsi kohta.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9db924c16c5eca17e7962ff1d88b09e581347fa5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919273"
---
# <a name="analysis-of-project-quotes"></a>Projekti hinnapakkumiste analüüs

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Rakendus Dynamics 365 Project Service Automation analüüsib projekti hinnapakkumisi, et hinnata kasumlikkust. Samuti analüüsitakse, kui hästi hinnapakkumine on joondatud kliendi ootustega tarnekuupäeva või lõpuleviimise kuupäeva ja eelarve kohta.

## <a name="profitability-analysis"></a>Kasumlikkuse analüüs

Rakendus Project Service Automation analüüsib kasumlikkust, kasutades kogutulu ja korrigeeritud kogutulu.

- Kogutulu arvutatakse järgmise valemi abil.

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Korrigeeritud kogutulu arvutatakse järgmise valemi abil.

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Kui kogutulu ja korrigeeritud kogutulu väärtused erinevad suurel määral, loetakse suur osa hinnapakkumise töödest tasumata.

## <a name="analysis-of-customer-expectations"></a>Kliendi ootusteanalüüs

Saate analüüsida hinnapakkumisi ja luua graafikuid klientide ootustele ajakava ja eelarve kohta, kui sisestate järgmistele väljadele väärtusi.

- Hinnapakkumise päise väli **Nõutav tarnekuupäev**.
- Iga hinnapakkumise rea (projektil ja tootel põhinevad read) väli **Kliendi eelarve**.

Ajakavaga seotud klientide ootuste analüüs tehakse võrreldes hinnapakkumise rea lõppkuupäeva üksikasju ja nõutavat tarnekuupäeva kõigis hinnapakkumise ridades.

Eelarvega seotud klientide ootuste analüüs tehakse võrreldes kõigi hinnapakkumiste ridasid pakutava summaga kõigis hinnapakkumise ridades.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
