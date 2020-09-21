---
title: Projekti edenemine ja tarbitud kulud
description: Selles teemas kirjeldatakse, kuidas jälgida projekti edenemist ja tarbitud kulusid.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751023"
---
# <a name="project-progress-and-cost-consumption"></a>Projekti edenemine ja tarbitud kulud

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Vajadus edenemise jälgimiseks ajakava suhtes sõltub majandusharust. Mõned majandusharud jälgivad minimaalsel tasandil, samas kui teised jälgivad kõrgemal tasemel. Selles teemas kirjeldatakse, kuidas kasutada ajakava oma organisatsiooni vajadustele vastavalt.

## <a name="effort-tracking-view"></a>Panuse jälgimise vaade

Vaade **Panuse jälgimine** jälgib ajakavas ülesannete edenemist. See võrdleb ülesandele tegelikult kulutatud panusetunde ülesandele plaanitud panusetundidega. Rakendus PSA kasutab jälgimismõõdikute arvutamiseks järgmisi valemeid.

- Edenemisprotsent = tegelik panus senini ÷ ülesandele plaanitud panus 
- Lõpetamise prognoos (ETC) = plaanitud panus – seni tehtud tegelik panus 
- Hinnang lõpetamisel (EAC) = ülejäänud panus + seni tehtud tegelik panus 
- Eeldatav panuse hälve = plaanitud panus – EAC

Rakendus PSA näitab ülesande eeldatavat panuse hälvet. Kui EAC on plaanitud panusest suurem, siis eeldatakse, et ülesanne võtab algselt plaanitust rohkem aega. Seega on see graafikust maas. Kui EAC on plaanitud panusest väiksem, siis eeldatakse, et ülesanne võtab algselt plaanitust vähem aega. Seega on see graafikust ees.

## <a name="re-projecting-effort"></a>Panuse ümberkavandamine

On tavaline, et projektijuht vaatab ülesande esialgsed prognoosid üle. Projekti ümberkavandamine hõlmab projektijuhi ettekujutust prognoosidest, võttes arvesse projekti praegust olekut. Kuid me ei soovita projektijuhtidel muuta alusnumbreid, kuna projekti alus kujutab endast projekti graafiku ja kuluprognoosi kindlaks määratud dokumenti, millega kõik projekti huvirühmad on nõustunud.

Projektijuht saab ülesannete panust ümber kavandada kahel viisil.

- Alistada vaikimisi ETC ülesande tegeliku järelejäänud panuse uue prognoosiga. 
- Alistada vaikimisi edenemisprotsent ülesande tegeliku edenemise uue prognoosiga.

Kõik need lähenemised põhjustavad ülesande ETC, EAC ja edenemisprotsendi ning ülesande eeldatava panuse hälbe ümberarvutamist. Lisaks arvutatakse ümber ka kokkuvõtlike ülesannete EAC, ETC ja edenemisprotsent, mis annavad panuse hälbe uue prognoosi.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Kokkuvõtlike ülesannete panuse ümberkavandamine

Kokkuvõtvate või konteinerülesannete panust saab ümber kavandada. Sõltumata sellest, kas kasutaja kavandab ümber järelejäänud panust või kokkuvõtlike ülesannete edenemisprotsenti kasutades, algab järgmine arvutuste kogum.

- Arvutatakse ülesande EAC, ETC ja edenemisprotsent.
- Uus EAC jaotatakse alamülesannete vahel samas proportsioonis kui oli ülesande esialgne EAC.
- Iga individuaalse ülesande puhul arvutatakse uus EAC kuni lehesõlme ülesannete tasemeni. 
- Mõjutatud alamülesannete jaoks (kuni lehesõlme tasemeni) arvutatakse EAC väärtuse põhjal ümber nende ETC ja edenemisprotsent. Selle tulemuseks on ülesande panuse hälbe uus prognoos. 
- Kokkuvõtlike ülesannete EAC-d arvutatakse ümber juursõlme tasemeni.

### <a name="cost-tracking-view"></a>Kulude jälgimise vaade 

Vaates **Kulude jälgimine** võrreldakse ülesandele kulutatud tegelikku kulu ülesandele plaanitud kuluga. 

> [!NOTE]
> See vaade kuvab ainult tööjõukulud ja ei sisalda kuluhinnangute kulusid. 

Rakendus PSA kasutab jälgimismõõdikute arvutamiseks järgmisi valemeid.

- Tarbitud kulu protsent = senini kulutatud tegelik kulu ÷ ülesandele plaanitud kulu
- Lõpetamise kulu (CTC) = plaanitud kulu – seni kulutatud tegelik kulu
- EAC = CTC + seni kulutatud tegelik kulu
- Eeldatav kuluhälve = plaanitud kulu – EAC

Ülesandes on kuvatud kuluhälbe projektsioon. Kui EAC on plaanitud kulust suurem, siis eeldatakse, et ülesanne on algselt plaanitust kulukam. Seega on suundumuseks eelarve ületamine. Kui EAC on plaanitud kulust väiksem, siis eeldatakse, et ülesanne on algselt plaanitust odavam. Seega on suundumuseks eelarve ülejääk.

## <a name="project-managers-re-projection-of-cost"></a>Projektijuhi tehtud kulude ümberkavandamine

Kui panus kavandatakse ümber, arvutatakse CTC, EAC, tarbitud kulu protsent ja eeldatav kuluhälve kõik vaates **Kulude jälgimine** ümber.

## <a name="project-status-summary"></a>Projekti oleku kokkuvõte

Andmete jälitamine vaadetes **Panuse jälgimine** ja **Kulude jälgimine** kuvab edenemise ja tarbitud kulud projekti juursõlme, kokkuvõtlike ülesannete ja lehesõlme tasemetel. Lehe **Projektiolem** jaotises **Olek** kuvatakse projektitaseme oleku kokkuvõte.

## <a name="status-summary-fields"></a>Oleku kokkuvõtte väljad

Väli **Üldine projekti olek** on redigeeritav väli, mis kuvab projekti üldise oleku. See kasutab kasvavale ohule viitamiseks värvkodeerimist (nt roheline, kollane ja punane). Väli **Kommentaarid** võimaldab projektijuhil sisestada oleku kohta konkreetseid märkuseid. Väli **Olekut värskendatud** pole redigeeritav ja väärtus on ajatempel, mis näitab, millal olekut viimati värskendati.

Väljad **Ajakava täitmine** ja **Kulude täitmine** määratakse jälgimise kuupäevast. Kui vaates **Panuse jälgimine** on juursõlme ajakava ja kuluhälve positiivsed, saate need väljad määrata väärtusele **Ees**. Kui juursõlme ajakava ja kuluhälve on negatiivsed, saate need määrata väärtusele **Taga**.
