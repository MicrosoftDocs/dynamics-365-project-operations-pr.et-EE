---
title: Projekti jälgimise ülevaade
description: Selles teemas kirjeldatakse, kuidas jälgida projekti edenemist ja tarbitud kulusid.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 14094d603be2834dc66abff2ff1faf5e940b1ffa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286603"
---
# <a name="project-tracking-overview"></a>Projekti jälgimise ülevaade

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Vajadus edenemise jälgimiseks ajakava suhtes sõltub majandusharust. Mõned majandusharud jälgivad minimaalsel tasandil, samas kui teised jälgivad kõrgemal tasemel. Selles teemas kirjeldatakse, kuidas kasutada ajakava oma organisatsiooni vajadustele vastavalt.

## <a name="effort-tracking-view"></a>Panuse jälgimise vaade

**Panuse jälgimise** vaates jälgitakse tööülesannete edenemist ajakavas, võrreldes ülesandele kulunud tegelike tööpanuse tunde planeeritud tööpanuse tundidega. Dynamics 365 Project Operations kasutab jälgimismõõdikute arvutamiseks järgmisi valemeid.

- **Edenemisprotsent**: seni tehtud tegelik panus ÷ hinnang lõpetamisel (EAC) 
- **Lõpetamise prognoos (ETC)**: plaanitud panus – seni tehtud tegelik panus 
- **EAC**: ülejäänud panus + seni tehtud tegelik panus 
- **Eeldatav panuse hälve**: plaanitud panus – EAC

Project Operations näitab ülesande eeldatavat panuse hälvet. Kui EAC on plaanitud panusest suurem, siis eeldatakse, et ülesanne võtab algselt plaanitust rohkem aega ja on graafikust maas. Kui EAC on plaanitud panusest väiksem, siis eeldatakse, et ülesanne võtab algselt plaanitust vähem aega ja on graafikust ees.

## <a name="reprojecting-effort"></a>Panuse ümberkavandamine

Projektijuhid vaatavad muudavad tihti ülesande esialgseid prognoose. Projekti ümberkavandamine hõlmab projektijuhi ettekujutust prognoosidest, võttes arvesse projekti praegust olekut. Kuid me ei soovita, et projektijuhid muudaksid algseid numbreid. Seda seetõttu, et projekti alus kujutab endast projekti graafiku ja kuluprognoosi kindlaks määratud dokumenti, millega kõik projekti huvirühmad on nõustunud.

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

Vaates **Kulude jälgimine** võrreldakse ülesandele kulutatud tegelikku kulu ülesandele plaanitud kuluga. 

> [!NOTE]
> See vaade kuvab ainult tööjõukulud ja ei sisalda kuluhinnangute kulusid. Project Operations kasutab jälgimismõõdikute arvutamiseks järgmisi valemeid.

- **Tarbitud kulu protsent**: senini kulutatud tegelik kulu ÷ lõpetamisel prognoositud kulu
- **Lõpetamise kulu (CTC)**: plaanitud kulu – seni kulutatud tegelik kulu
- **EAC**: järelejäänud kulu + seni kulutatud tegelik kulu
- **Eeldatav kuluhälve**: plaanitud kulu – EAC

Ülesandes on kuvatud kuluhälbe projektsioon. Kui EAC on plaanitud kulust suurem, siis eeldatakse, et ülesanne on algselt plaanitust kulukam. Seega on suundumuseks eelarve ületamine. Kui EAC on plaanitud kulust väiksem, siis eeldatakse, et ülesanne on algselt plaanitust odavam. Seega on suundumuseks eelarve ülejääk.

## <a name="project-managers-reprojection-of-cost"></a>Projektijuhi kulude ümberkavandamine

Kui panus kavandatakse ümber, arvutatakse CTC, EAC, tarbitud kuluprotsent ja eeldatav kuluhälve kõik vaates **Kulude jälgimine** ümber.

## <a name="project-status-summary"></a>Projekti oleku kokkuvõte

Andmete jälitamine vaadetes **Panuse jälgimine** ja **Kulude jälgimine** kuvab edenemise ja tarbitud kulud projekti juursõlme, kokkuvõtlike ülesannete ja lehesõlme tasemetel. Lehe **Projektiolem** jaotises **Olek** kuvatakse projektitaseme oleku kokkuvõte.

## <a name="status-summary-fields"></a>Oleku kokkuvõtte väljad

Väli **Üldine projekti olek** on redigeeritav väli, mis kuvab projekti üldise oleku. See kasutab kasvavale ohule viitamiseks värvkodeerimist (nt roheline, kollane ja punane). Väli **Kommentaarid** võimaldab projektijuhil sisestada oleku kohta konkreetseid märkuseid. Väli **Olekut värskendatud** pole redigeeritav ja väärtus on ajatempel, mis näitab, millal olekut viimati värskendati.

Väljad **Ajakava täitmine** ja **Kulude täitmine** määratakse jälgimise kuupäevast. Kui vaates **Panuse jälgimine** on juursõlme ajakava ja kuluhälve positiivsed, saate need väljad määrata väärtusele **Ees**. Kui juursõlme ajakava ja kuluhälve on negatiivsed, saate need määrata väärtusele **Taga**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]