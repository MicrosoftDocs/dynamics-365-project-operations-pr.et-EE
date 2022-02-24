---
title: Projekti edenemine ja kulu tarbimine
description: Selles teemas kirjeldatakse projekti edenemise ja tarbitud kulude jälgimist.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 0b69cee49e028b98bbb32e4a7e7aedf5479527dc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148008"
---
# <a name="project-progress-and-cost-consumption"></a>Projekti edenemine ja kulu tarbimine

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Vajadus edenemise jälgimiseks ajakava suhtes sõltub majandusharust. Mõned majandusharud jälgivad minimaalsel tasandil, samas kui teised jälgivad kõrgemal tasemel. Selles teemas kirjeldatakse, kuidas kasutada ajakava oma organisatsiooni vajadustele vastavalt.

## <a name="effort-tracking-view"></a>Panuse jälgimise vaade

Vaade **Panuse jälgimine** jälgib ajakavas ülesannete edenemist. See võrdleb tegelikult ülesande peale kulutatud panusetunde ülesandele plaanitud kulutatud tundidega. Rakendus Project Service Automation kasutab jälgimismõõdikute arvutamiseks järgmisi valemeid.

Algselt ülesande loomisel: planeeritud kulu määrakse lõpetamisel prognoositud kulule. Kui ülesande jaoks salvestatakse tegelikud näitajad, arvutatakse koormuse jälrgimise vaade järgnevalt

- Edenemisprotsent = seni tehtud tegelik panus ÷ hinnang lõpetamisel (EAC) 
- Lõpetamise prognoos (ETC) = hinnang lõpetamisel (EAC) – seni tehtud tegelik panus 
- EAC = ülejäänud panus + seni tehtud tegelik panus 
- Eeldatav panuse hälve = plaanitud panus – EAC

Rakendus Project Service Automation näitab ülesande eeldatavat panuse hälvet. Kui EAC on plaanitud panusest suurem, siis eeldatakse, et ülesanne võtab algselt plaanitust rohkem aega. Seega on see graafikust maas. Kui EAC on plaanitud panusest väiksem, siis eeldatakse, et ülesanne võtab algselt plaanitust vähem aega. Seega on see graafikust ees.

## <a name="reprojecting-effort"></a>Panuse ümberkavandamine

On tavaline, et projektijuht vaatab ülesande esialgsed prognoosid üle. Projekti ümberkavandamine hõlmab projektijuhi ettekujutust prognoosidest, võttes arvesse projekti praegust olekut. Kuid me ei soovita projektijuhtidel muuta alusnumbreid, kuna projekti alus kujutab endast projekti graafiku ja kuluprognoosi kindlaks määratud dokumenti, millega kõik projekti huvirühmad on nõustunud.

Projektijuht saab ülesannete panust ümber kavandada kahel viisil.

- Alistada vaikimisi ETC ülesande tegeliku järelejäänud panuse uue prognoosiga. 
- Alistada vaikimisi edenemisprotsent ülesande tegeliku edenemise uue prognoosiga.

Kõik need lähenemised põhjustavad ülesande ETC, EAC ja edenemisprotsendi ning ülesande eeldatava panuse hälbe ümberarvutamist. Lisaks arvutatakse ümber ka kokkuvõtlike ülesannete EAC, ETC ja edenemisprotsent, mis annavad panuse hälbe uue prognoosi.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Kokkuvõtlike ülesannete panuse ümberkavandamine

Kokkuvõtvate või konteinerülesannete panust saab ümber kavandada. Sõltumata sellest, kas kasutaja kavandab ümber järelejäänud panust või kokkuvõtlike ülesannete edenemisprotsenti kasutades, algab järgmine arvutuste kogum.

- Arvutatakse ülesande EAC, ETC ja edenemisprotsent.
- Uus EAC jaotatakse alamülesannete vahel samas proportsioonis kui oli ülesande esialgne EAC.
- Iga individuaalse ülesande puhul arvutatakse uus EAC kuni lehesõlme ülesannete tasemeni. 
- Mõjutatud alamülesannete jaoks (kuni lehesõlme tasemeni) arvutatakse EAC väärtuse põhjal ümber nende ETC ja edenemisprotsent. Selle tulemuseks on ülesande panuse hälbe uus prognoos. 
- Kokkuvõtlike ülesannete EAC-d arvutatakse ümber juursõlme tasemeni.

### <a name="cost-tracking-view"></a>Kulude jälgimise vaade 

Vaates **Kulude jälgimine** võrreldakse ülesandele kulutatud tegelikku kulu plaanitud kuluga. 

> [!NOTE]
> See vaade kuvab ainult tööjõukulud ja ei sisalda kuluhinnangute kulusid. 

Rakendus Project Service Automation kasutab jälgimismõõdikute arvutamiseks järgmisi valemeid.

Ülesande loomisel on planeeritud kulu võrdne lõpetamisel prognoositud kuluga. Kui ülesande jaoks on tegelikud näitajad salvestatud, arvutatakse kulu jaoks vaates **Jälgimine** järgnev:

 - Tarbitud kulu protsent = senini kulutatud tegelik kulu ÷ ülesande lõpetamisel prognoositud kulu
 - Lõpetamise kulu (CTC) = lõpetamisel prognoositud kulu – seni kulutatud tegelik kulu
 - Lõpetamisel prognoositud kulu = CTC + seni kulutatud tegelik kulu
 - Eeldatav kuluhälve = plaanitud kulu – lõpetamisel prognoositud kulu

Ülesandes on kuvatud kuluhälbe projektsioon. Kui lõpetamisel prognoositud kulu on plaanitud kulust suurem, siis eeldatakse, et ülesanne on algselt plaanitust kulukam. Seega on suundumuseks eelarve ületamine. Kui lõpetamisel prognoositud kulu on plaanitud kulust väiksem, siis eeldatakse, et ülesanne on algselt plaanitust odavam ja suundumuseks on eelarve ülejääk.

## <a name="project-managers-reprojection-of-cost"></a>Projektijuhi kulude ümberkavandamine

Kui panus kavandatakse ümber, arvutatakse CTC, lõpetamisel prognoositud kulu, tarbitud kulu protsent ja eeldatav kuluhälve kõik vaates **Kulude jälgimine** ümber.

## <a name="project-status-summary"></a>Projekti oleku kokkuvõte

Andmete jälitamine vaadetes **Panuse jälgimine** ja **Kulude jälgimine** kuvab edenemise ja tarbitud kulud projekti juursõlme, kokkuvõtlike ülesannete ja lehesõlme tasemetel. Lehe **Projektiolem** jaotises **Olek** kuvatakse projektitaseme oleku kokkuvõte.

## <a name="status-summary-fields"></a>Oleku kokkuvõtte väljad

Väli **Üldine projekti olek** on redigeeritav väli, mis kuvab projekti üldise oleku. See kasutab kasvavale ohule viitamiseks värvkodeerimist (nt roheline, kollane ja punane). Väli **Kommentaarid** võimaldab projektijuhil sisestada oleku kohta konkreetseid märkuseid. Väli **Olekut värskendatud** pole redigeeritav ja väärtus on ajatempel, mis näitab, millal olekut viimati värskendati.

Väljad **Ajakava täitmine** ja **Kulude täitmine** määratakse jälgimise kuupäevast. Kui vaates **Panuse jälgimine** on juursõlme ajakava ja kuluhälve positiivsed, saate need väljad määrata väärtusele **Ees**. Kui juursõlme ajakava ja kuluhälve on negatiivsed, saate need määrata väärtusele **Taga**.
