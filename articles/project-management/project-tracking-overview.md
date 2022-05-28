---
title: Projekti panuse jälgimine
description: Selles teemas kirjeldatakse, kuidas jälgida projekti panust ja töö edenemist.
author: ruhercul
ms.date: 02/15/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 037118714cf01ba2fb91cdd94345495d12ccb645
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593791"
---
# <a name="project-effort-tracking"></a>Projekti panuse jälgimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Vajadus edenemise jälgimiseks ajakava suhtes sõltub majandusharust. Mõned majandusharud jälgivad minimaalsel tasandil, samas kui teised jälgivad kõrgemal tasemel. Selles teemas kirjeldatakse, kuidas kasutada ajakava oma organisatsiooni vajadustele vastavalt.

## <a name="effort-tracking-view"></a>Panuse jälgimise vaade

**Panuse jälgimise** vaates jälgitakse tööülesannete edenemist ajakavas, võrreldes ülesandele kulunud tegelike tööpanuse tunde planeeritud tööpanuse tundidega. Dynamics 365 Project Operations kasutab jälgimismõõdikute arvutamiseks järgmisi valemeid.

- **Edenemisprotsent**: seni tehtud tegelik panus ÷ hinnang lõpetamisel (EAC) 
- **Järelejäänud panus**: prognoositav panus lõpetamisel – tegelik seni tehtud panus 
- **EAC**: ülejäänud panus + seni tehtud tegelik panus 
- **Eeldatav panuse hälve**: plaanitud panus – EAC

Project Operations näitab ülesande eeldatavat panuse hälvet. Kui EAC on plaanitud panusest suurem, siis eeldatakse, et ülesanne võtab algselt plaanitust rohkem aega ja on graafikust maas. Kui EAC on plaanitud panusest väiksem, siis eeldatakse, et ülesanne võtab algselt plaanitust vähem aega ja on graafikust ees.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Lehe ülesannete panuse ümber kavandamine

Projektijuhid vaatavad muudavad tihti ülesande esialgseid prognoose. Projekti ümberkavandamine hõlmab projektijuhi ettekujutust prognoosidest, võttes arvesse projekti praegust olekut. Samas me ei soovita, et projektijuhid muudaksid plaanitud panuse numbreid. Seda seetõttu, et projekti kavandatav panus tähistab projekti ajakava ja kuluprognoosi jaoks juba loodud kaasamisallikat ning kõik projekti raames tehtud huvirühmad on sellega nõustunud.

Projektijuht saab ülesannete panuse uuesti projekteerida, värskendades vaikimisi suvandit **Järelejäänud panus** ülesande uue prognoosiga. See uuendus põhjustab ülesande prognoosi lõpetamisel, edenemisprotsendi ja ülesande projekteeritud panuse hälbe uuesti arvutamist. Lisaks arvutatakse ümber ka kokkuvõtlike ülesannete EAC, ETC ja edenemisprotsent, mis annavad panuse hälbe uue prognoosi.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Kokkuvõtlike ülesannete panuse ümberkavandamine

Kokkuvõtvate või konteinerülesannete panust saab ümber kavandada. Projektijuhid saavad kokkuvõtteülesannete puhul allesjäänud jõupingutusi värskendada. Allesjäänud pingutuse värskendamisel käivitatakse rakenduses järgmine arvutuskomplekt.

- Arvutatakse ülesande EAC ja edenemisprotsent.
- Uus EAC jaotatakse alamülesannete vahel samas proportsioonis kui oli ülesande esialgne EAC.
- Iga individuaalse ülesande puhul arvutatakse uus EAC kuni lehesõlme ülesannete tasemeni. 
- Mõjutatud alamülesannete jaoks (kuni lehe tasemeni) arvutatakse EAC väärtuse põhjal ümber nende järelejäänud panus ja edenemisprotsent. Selle tulemuseks on ülesande panuse hälbe uus prognoos. 
- Kokkuvõtlike ülesannete EAC-d arvutatakse ümber juursõlme tasemeni.
- Heakskiidetud jõupingutused kokkuvõtliku ülesande täitmiseks on kõigi tütarülesannete heakskiidetud jõupingutuste summa ja kokkuvõtteülesande heakskiidetud jõupingutused.
- Kokkuvõtteülesande ülejäänud jõupingutused on kõigi tütarülesannete järelejäänud jõupingutuste summa, millest on maha arvatud kokkuvõtteülesande heakskiidetud jõupingutused.

## <a name="project-status-summary"></a>Projekti oleku kokkuvõte

Andmete jälitamine vaadetes **Panuse jälgimine** ja **Kulude jälgimine** kuvab edenemise ja tarbitud kulud projekti juursõlme, kokkuvõtlike ülesannete ja lehesõlme tasemetel. Lehe **Projektiolem** jaotises **Olek** kuvatakse projektitaseme oleku kokkuvõte.

## <a name="status-summary-fields"></a>Oleku kokkuvõtte väljad

Väli **Üldine projekti olek** on redigeeritav väli, mis kuvab projekti üldise oleku. See kasutab kasvavale ohule viitamiseks värvkodeerimist (nt roheline, kollane ja punane). Väli **Kommentaarid** võimaldab projektijuhil sisestada oleku kohta konkreetseid märkuseid. Väli **Olekut värskendatud** pole redigeeritav ja väärtus on ajatempel, mis näitab, millal olekut viimati värskendati.

Väljad **Ajakava täitmine** ja **Kulude täitmine** määratakse jälgimise kuupäevast. Kui vaates **Panuse jälgimine** on juursõlme ajakava ja kuluhälve positiivsed, saate need väljad määrata väärtusele **Ees**. Kui juursõlme ajakava ja kuluhälve on negatiivsed, saate need määrata väärtusele **Taga**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
