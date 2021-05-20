---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 20, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 20, v3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 124dad5438f9489d1ddbc952cecaee977b6b7f01
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949089"
---
# <a name="project-service-automation-update-release-20-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 20, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 20 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgu number on V 3.10.31.37 ja on üldiselt saadaval 2020. a juuni enesevärskenduse kaudu.

## <a name="update-release-20"></a>Värskenduste väljalase 20

### <a name="bug-fixes"></a>Veaparandused

**Projektijuhtimine**

Lahendatud on järgmised probleemid.

- Projekti meeskonnaliikmete importimine jaotamismeetodiga, mis nõuab tundide tulemit ebaselges tõrketeates, kui määratud tunnid on null.
- Kasutajatele kuvatakse vale tõrge, kui projekti tööülesande väljale **Kirjeldus** on sisestatud maksimaalne arv märke.
- Leht **Microsoft Dynamics 365 Project Service Automationi lisandmooduli allalaadimine** suunab inglisekeelsele allalaadimise lehele, kus kasutaja keelesätted on määratud jaapani keelele.
- Kui ilmneb serveri tõrge, jääb mõnikord sünkroonimise silt vahekaardil **Ajakava** rakenduse **Projektid** vormides alles.
- Liigsed tööülesannete värskendused saadetakse serverisse tööülesande muutmisel.

**Sales**

Lahendatud on järgmised probleemid.

- Vormil **Leping** loob käsu **Loo arve** kaks arvet ühe tegeliku kirje kohta.
- Rakenduses Internet Explorer 11 ei saa kasutajad kulukirjeid luua.
- Kulu tagasipööramine ja arveldamata müügi tegelike näitajate tühistamine pole lingitud.
- Nupp **Värskenda tegelikud näitajad** **Projekti** vormil ei värskenda väärtust **Tööülesande tegelikud tunnid**.
- **PreValidateProjectTeamMemberCreate** lisandmoodul saab dubleerida üldkasutatavaid ressursse juhul, kui atribuudi **msdyn_isgenericresourceprojectscoped** väärtuseks on seatud **väär**.
- Käsk **Arvuta** tühistab tootepõhise hinnapakkumise rea üksikasjade ja lepingurea üksikasjadega seotud tasustatavad kulud.
- Teatud juhtudel kuvab lisandmoodul **PostEstimateLineUpdate** nullviite erandi tõrke.
- Ajaetapi kestus **Kasumlikkuse analüüsi diagrammil** ei vasta fikseeritud hinnaga hinnapakkumise rea üksikasjade kulude kestusele.
- Üksuste ja üksuste rühma kulukategooriate väärtused ei ole vaikimisi õigedvormidel **Lepingurea üksikasjad** ja **Hinnapakkumise rea üksikasjad**.
- **Organisatsiooni ühiku omahinna** loendid lubavad efektiivse kuupäeva kattumist.
- Kasutajad ei tohi muuta **OrgUnit** it juhul, kui tellimuse tüüp ei ole tööpõhine, kuna selle tulemuseks on nullviite erandi tõrge.
- Kui proovite navigeerida vormilt **Hinnapakkumise rea üksikasjad** tagasi vahekaardile **Hinnapakkumine**, siis vorm värskendab ja kuvab vahekaardi **Kokkuvõte**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]