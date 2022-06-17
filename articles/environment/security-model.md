---
title: Turbemudel
description: Selles artiklis antakse teavet rakenduse turbemudeli kohta Dynamics 365 Project Operations.
author: stsporen
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2f4992b1ea0c2b93a83c6c2c9a146a7610afc5fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924494"
---
# <a name="security-model"></a>Turbemudel

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_



Microsoft Dynamics 365 Project Operations sisaldab ainulaadset turbemudelit, mis võimaldab rollipõhist ettevõtte turbemudelit, mis teeb koostööd Microsoft Office’i rühmadega. 


## <a name="security-roles"></a>Turberollid
Project Operationsi kasutajaliidese võimalused sisaldavad järgmisi rolle.

| Roll                          | Kirjeldus                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Praktikajuht              | Toetab projektiülest aruandlust.                                                                                                            | Äriüksus              |
| Projekti kinnitaja              | Kinnitab projekti aega ja kulusid.                                                                                                                              | Äriüksus |
| Projekti arveldushaldur | Loob arve ettepaneku.                                                                                                                                                 | Äriüksus |
| Projektijuht               | Loob projekti kava ja taotleb ressursse.                                                                                                                              | Äriüksus |
| Projekti ressurss              | Meeskonnaliikmed, keda saab broneerida ja kes saavad esitada aega.                                                                                                          | Äriüksus|
| Ressursihaldur              | Kõik ressursihalduse funktsioonid, näiteks ressursi taotluste ja broneeringute täitmine, eraldatud, et toetada hübriidkonfiguratsiooni Projektijuht + Ressursihaldur ja ühe ning tsentraliseeritud ressursihalduri rolli. | Äriüksus |


Microsoft Projecti veebilanedus sisaldab järgmisi rolle.

| Roll           | Kirjeldus                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Projekti kasutaja   | Projekti koostööpartner, kes saab luua oma projekte ja vaadata temaga ühiskasutusse antud projekte. | Kasutaja   |
| Projekti süsteem | Rakenduse kontekstis kasutatav roll. Kliendid ei tohiks seda süsteemi rolli kasutada.                                    | Globaalne |

## <a name="security-enforcement"></a>Turvalisuse tagamine
Projektitasemel teostatud toiminguid teostatakse sisselogitud kasutaja kontekstis. See tähendab, et projekti loomiseks, avamiseks või kustutamiseks peab kasutajal olema juurdepääs CDS-ile. Juurdepääs CDS-ile võidakse anda ühe platvormil oleva võimaliku mehhanismi kaudu. Näiteks võib projektile olla juurdepääs suurema ulatusega kasutajal või kui on teostatud konkreetne projekti ühiskasutusse andmise toiming, mis annab kasutajale juurdepääsu.

Oluline on seda Project Operationsis projektide loomisel arvestada.

## <a name="modern-group-collaboration-with-project-operations"></a>Kaasaegne rühma koostöö Project Operationsiga
Veebi Project ja Project Operations toetavad kaasaegseid koostöörühmi. Projektile rühma kaudu lisatud kasutajad saavad projekti kava redigeerida.

Veebi Project lisab kasutajad määramisel automaatselt rühma.

Rühmad võimaldavad projekti õigusi ja toetavaid koostöö artefakte üheskoos töötamiseks. Järgmisel diagrammil on kujutatud sündmused ja oleku muudatused, mis toimuvad rühma määramise protsessi käigus.

Project Operations ei loo rühma kaudse tegevuse kaudu ja teeb seda ainult pakiliste rühmade selgesõnalise tegevuse kaudu.

Rühma liikmete otsing dialoogis **Rühma haldus** on piiratud nendega, kes on määratud keskkonna turberühma osaks. Lisateavet vt jaotisest [Kasutajate keskkondadele juurdepääsu juhtimine: turberühmad ja litsentsid](/power-platform/admin/control-user-access).

![Rühmarežiim.](./media/groupsmode.png)

1. Projekti loob ja omab loov kasutaja.
2. Projekti omanikuks värskendatakse meeskond.
3. Omanikuks olev meeskond vastendatakse määratud või loodud Office'i rühmaga.
4. Projekti algne omanik lisatakse Office'i rühma.

## <a name="deployment-recommendation"></a>Juurutamise soovitus
Office'i rühma koostöömudeli arenedes lisatakse funktsionaalsus, et aja jooksul saaks pakkuda üksikasjalikumat kontrolli. Klientidel, kes juurutavad Project Operationsi täna, soovitatakse keskenduda traditsioonilisele Microsoft Dynamics 365 turbemudelile.

Lisateavet leiate jaotisest [Common Data Service'i turvalisus](/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Projektitoimingud ja Microsoft Dynamics 365 Finantsturvalisus
Project Operations sisaldab järgmisi rolle.

- Projektijuht
- Projekti raamatupidaja

Lisateavet lahenduse Finance turbe kohta leiate teemast [Rollipõhine turve](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).




[!INCLUDE[footer-include](../includes/footer-banner.md)]