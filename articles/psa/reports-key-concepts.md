---
title: Põhimõisted
description: Selles teemas antakse teavet rakenduse Project Service Automation ressursihalduse põhimõistete kohta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1e5e78bbeb1086fada799cf7ac66173e5a563e2d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075180"
---
# <a name="key-concepts"></a>Põhimõisted

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Järgmises tabelis on määratletud põhimõisted, mida rakenduses Dynamics 365 Project Service Automation kasutatakse.

| Mõiste                    | Määratlus |
|----------------------------|------------|
| Projektimeeskonna liige        | Projektimeeskonda kuuluvana võib projektimeeskonna liige olla nimega ressurss, millel on broneeringud, nimega ressurss, millel pole broneeringuid või üldressurss. Üldressurssidel pole broneeringuid, need on projektis kohalikud ja neil pole projektideüleselt võimsuse piiranguid. |
| Projekti üldressurss   | Ressursi kohatäide, mis võimaldab teil luua meeskonna ja määrata projektiplaanile töötajad ilma nimega ressurssi teadmata. Üldressursi kalendrina kasutatakse projekti kalendrit. Üldressursse saab lisada projektimeeskonnale ja määrata ülesannetele. |
| Broneeritud tunnid               | Ressursi tunnid on projekti suhtes fikseeritult broneeritud, mis aitab tagada projekti töö lõpuleviimise. Broneeritud tunde tarbitakse ressursi üldvõimsusest. Broneeringud saab teha ainult nimega ressurside suhtes, mitte üldressursside suhtes. |
| Määratud tunnid             | Ressursi tunnid määratakse ülesannetele projekti ajakavas. Määramisi saab teha nii nimega ressurside kui ka üldressurside suhtes. Määramised võivad olla broneeringutest sõltumatud. |
| Nõutavad tunnid             | Võimsus, mis on nõutav, kuid mida pole nimega ressurss veel täitnud. Nõutavad tunnid on asjakohased ainult üldistele meeskonnaliikmetele, kes on loonud ressursinõudeid. |
| Nõudlus                     | Praegune ja sissetulev töökoormus. Rakenduses Project Service Automation kuvatakse nõudlus ressursinõuete või ressursitaotlustena. |
| Ressursinõue       | Olem, mida kasutatakse nõutavate ressursside jaoks nõutavate tundide, algus- ja lõppkuupäevade, oskuste, geograafia ja muude hinnakujunduse dimensioonide hõivamiseks. Ressursinõuded luuakse kas projekti meeskonnaliikmetest või eraldi. |
| Ressursitaotlus           | Olem, mida kasutatakse nö ümbrisena, et kanda ressursinõuet, mille peab täitma ressursihaldur. |
| Ressursi vaikeroll      | Roll, mille alla ressurss on kasutuse arvutamiseks rühmitatud. Eeldatakse, et ressursil on rolli jaoks vajalikud oskused ja ta vastab selle rolli sihtkasutusele. |
| Ressursi organisatsiooniüksus | Organisatsiooniüksus, millele ressurss on määratud. |
| Kontuur                    | Ülesande, nõude või määramise tunnid, kui need jagatakse igapäevaseks jaotuseks. Näiteks saab viiepäevase, 40-tunnise ülesande jagada viie päeva peale, iga päev kaheksa tundi. |
| Vastavusseviimise vaade        | Vaade, mis kuvab iga projekti meeskonnaliikme jaoks broneeringud ja määramised. See vaade võimaldab projektijuhil otsida broneeringute ja määramiste vahelist vastuolu ning võtta vastuolu ilmnemisel kasutusele parandusmeetmeid. |
| Tööaeg                 | Olem, mida kasutatakse ressursi võimsuse, töötundide ja töövälise aja tuvastamiseks. Seda olemit nimetatakse ka ressursi kalendriks. |
