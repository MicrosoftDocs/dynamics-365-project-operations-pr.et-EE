---
title: Projekti mallide arendamine funktsiooniga Kopeeri projekt
description: Selles teemas antakse teavet selle kohta, kuidas kohandatud toimingut Kopeeri projekt kasutades projekti malle luua.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131608"
---
# <a name="develop-project-templates-with-copy-project"></a>Projekti mallide arendamine funktsiooniga Kopeeri projekt

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations toetab võimalust kopeerida projekt ja ennistada kõik tööülesanded tagasi üldistele ressurssidele, mis rolli esindavad. Kliendid saavad seda funktsiooni kasutada põhiliste projekti mallide loomiseks.

Kui valite suvandi **Kopeeri projekt**, värskendatakse sihtprojekti olekut. Kasutage suvandit **Oleku põhjus**, et määratleda, millal kopeerimise toiming lõpetada. Suvandi **Kopeeri projekt** valimine värskendab projekti alguskuupäeva praegusele alguskuupäevale, kui sihtprojekti olemis ei tuvastata sihtkuupäeva.

## <a name="copy-project-custom-action"></a>Kohandatud toiming Kopeeri projekt 

### <a name="name"></a>Nimetus 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Sisendparameetrid
Olemas on kolm sisendparameetrit.

| Parameeter          | Tüüp   | Väärtused                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** või **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Olemi viide | Algne projekt |
| Sihtmärk             | Olemi viide | Sihtprojekt |


- **{"clearTeamsAndAssignments":true}**: veebi projekti vaikekäitumine ja see eemaldab kõik ülesanded ja meeskonnaliikmed.
- **{"removeNamedResources":true}** Project Operationsi vaikekäitumine ja see ennistab määramised üldistele ressurssidele.

Lisateavet toimingute vaikeväärtuste kohta leiate teemast [Veebi API toimingute kasutamine](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Määrake kopeeritavad väljad 
Kui tegevus valitakse, vaatav suvand **Kopeeri projekt** projektivaadet **Kopeeri projekti veerud**, et määratleda, millised väljad projekti kopeerimisel kopeeritakse.
