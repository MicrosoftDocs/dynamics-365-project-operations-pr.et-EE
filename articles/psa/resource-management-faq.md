---
title: Ressursihalduse KKK
description: Selles teemas antakse vastused ressursihalduse korduma kippuvatele küsimustele.
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
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075167"
---
# <a name="resource-management-faq"></a>Ressursihalduse KKK

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

**Kasutaja** ja **Kontakt** on ainsad ressursitüübid, mida rakendus Dynamics 365 Project Service Automation toetab. Kuigi saate luua muid tüüpi ressursse (nt **Varustus** ja **Rühm** ), ei toetata nende puhul ühtegi terviklikku kasutusjuhtumit.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Mis on määramise ja broneeringu vahe?

Määramised on projekti ajakavas tehtud ressursside määramised projekti ülesannetele. Ressursid võivad olla kas tegelikud või üldised ressursid. Broneeringud on ressursside fikseeritud või esialgsed projektile eraldamised. Fikseeritud broneeringud tarbivad ressursivõimsust. Ideaalis peaksid tegelike ressursside puhul broneeringud ja määramised ühtima, kuna need ei erine üksteisest. Kuid PSA ei jõusta seda kokkulepet. Vaates Vastavusseviimine kuvatakse projektijuhile kohti, kus ressursi broneeringud ja määramised ei ühti.
