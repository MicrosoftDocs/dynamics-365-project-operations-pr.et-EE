---
title: Projekti hinnapakkumiste analüüs
description: Selles teemas antakse teavet projekti hinnapakkumiste analüüsi kohta.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 0d9cefafcce33297146cae81d9ba7e68ab79aeb6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075072"
---
# <a name="analysis-of-project-quotes"></a>Projekti hinnapakkumiste analüüs

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