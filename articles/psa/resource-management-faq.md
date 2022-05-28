---
title: Ressursihalduse KKK
description: Selles teemas antakse vastused ressursihalduse korduma kippuvatele küsimustele.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c8ce1edf7d7c535271fa8076befd26f092fbd495
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587489"
---
# <a name="resource-management-faq"></a>Ressursihalduse KKK

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Mis on meeskonnaliikme ja ressursinõude vahe?

Projekti meeskonnaliiget saab määrata ülesannetele (broneeritud või ülebroneeritud) ja määrata kinnitajaks. Ressursinõue võib eksisteerida ilma projekti meeskonnaliikmeta, mustandmärkusena või nõudena. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Mis on pakutud ja esialgselt broneeritud tundide vahe?

Pakutud tundide ja esialgselt broneeritud tundide erinevuseks on nähtavus. Pakutud tunnid on nähtavad ainult ressursihalduritele ja projektijuhile, kes nõudluse ressursitaotluse kasutamise kaudu algatas. Esialgselt broneeritud tunnid on nähtavad kõigile, kellel on ajakavapaneelile juurdepääs.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Kuidas vaadata meeskonna ressursside jaoks esialgselt broneeritud tunde?

Esialgseid broneerimisi saab teha ressursinõude broneerimisel. Ressursid, mis on projektimeeskonnas esialgselt broneeritud kuvatakse meeskonnaliikmetena, kellel on esialgselt broneeritud tunnid. Need kuvatakse ka ajakavapaneelil.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Kuidas muuta broneeritud ressursi (üldised või nimega) nõutavaid tunde ja algus- ning lõppkuupäevi?

Pärast ressursside broneerimist valige soovitud muudatuste tegemiseks **Halda broneeringuid**.

## <a name="what-resources-types-does-project-service-automation-support"></a>Milliseid ressursitüüpe Project Service Automation toetab?

**Kasutaja** ja **Kontakt** on ainsad ressursitüübid, mida rakendus Dynamics 365 Project Service Automation toetab. Kuigi saate luua muid tüüpi ressursse (nt **Varustus** ja **Rühm**), ei toetata nende puhul ühtegi terviklikku kasutusjuhtumit.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Mis on määramise ja broneeringu vahe?

Määramised on projekti ajakavas tehtud ressursside määramised projekti ülesannetele. Ressursid võivad olla kas tegelikud või üldised ressursid. Broneeringud on ressursside fikseeritud või esialgsed projektile eraldamised. Fikseeritud broneeringud tarbivad ressursivõimsust. Ideaalis peaksid tegelike ressursside puhul broneeringud ja määramised ühtima, kuna need ei erine üksteisest. Kuid PSA ei jõusta seda kokkulepet. Vaates Vastavusseviimine kuvatakse projektijuhile kohti, kus ressursi broneeringud ja määramised ei ühti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
