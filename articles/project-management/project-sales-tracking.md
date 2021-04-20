---
title: Projektimüügi jälgimine
description: Selles teemas antakse teavet selle kohta, kuidas Project Operations jälgib projekti edenemist seoses tööjõutuluga.
author: rumant
manager: AnnBe
ms.date: 03/24/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 438c44dcfaf9677075eb07688c1e65c6e7053755
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711039"
---
# <a name="project-sales-tracking"></a>Projektimüügi jälgimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations jälgib tööjõu prognoose ja tulu projektiplaani väikseimal nõutaval väärtusel. Tööjõutulu prognoosimine põhineb plaanitud väärtusel ja üldistel või nimelistel ressurssidel, mis määratakse projektiplaani igale lehe ülesandele. Kui projekt algab ja inimesed hakkavad erinevate projektiülesannete kohta aega märkima, summeeritakse tööjõu tegelik tulu, mis käivitab projekti osade arvutuse.

## <a name="labor-revenue-tracking-view"></a>Tööjõutulu jälgimise vaade

Lehel **Projektid** vahekaardil **Jälgimine** saate valida suvandi **Jälgimine** > **Kulu**, et avada vaade **Kulu jälgimine**. Või saate valida suvandi **Kasutus** > **Arvemäär**, et avada vaate **Tulu jälgimine**, mis kuvab iga projektiplaani ülesande töötulu edenemise. Selles vaates võrreldakse ka tööülesandele kulutatud tegelikku tööjõutulu tööülesande plaanitud tööjõutuluga. Project Operations kasutab tööjõutulu mõõdikute arvutamiseks järgmisi valemeid.

- **Plaanitud tulu**: iga lehe ülesande kõikide ressursi määramiste eeldatavad müügiväärtused
- **Tegelik tulu**: kõigi arveldamata müügi tegelike väärtuste summa tööülesandele registreeritud aja jaoks
- **Arveldatava tulu protsent**: tegelik tulu ÷ tuluprognoos lõpetamisel
- **Järelejäänud tulu**: tuluprognoos lõpetamisel – tegelik tulu
- **Prognoositud tulu lõpetamisel**: järelejäänud tulu + tegelik tulu
- **Tulu erinevus**: plaanitud tulu – prognoositud tulu lõpetamisel


> [!NOTE]
> Project Operations kuvab tööjõutulu ainult lehel **Projekt** vahekaardil **Jälgimine**. Kuigi materjale ja kulusid saab prognoosida ja jälgida tarbimise jaoks, ei kaasata neid tulusid vahekaardil **Jälgimine** kuvatavate tulude hulka. See vahekaart on loodud toimima ainult tööjõutulude ümber kavandamiseks panuse ümber kavandamisega.  
> Kõik kuvatavad tulusummad teisendatakse projekti kuluvaluutasse. Projekti kuluvaluuta on projekti lepinguüksuse valuuta. Fikseeritud hinnaga projektide puhul ei ole vaates **Tööjõutulu jälgimine** tulunumbrid olulised, kuna tasustamata müügi tegelikke numbreid ei salvestata aja kinnitamisel.
> Projekti vahekaardil **Prognoos** kuvatavaid prognoositavaid ajalisi müügiväärtuseid ei pruugita lisada vahekaardi **Jälgimine** prognoositud tuluväärtusele. Selle vastuolu allikaks on kaks võimalikku põhjust.
><ol>
   ><li> Vahekaardil <b>Prognoosid</b> kuvatakse prognoositav tulu müügivaluutas, samas kui vahekaardil <b>Jälgimine</b> on plaanitud tulu teisendatud kuluvaluutasse. </li>
   ><li> Kui prognoositav müük teisendatakse lepinguvaluutasse, nagu on näidatud vahekaardil <b>Prognoosid</b>, projekti valuutasse, sisaldab teisendamine etappe, mille tulemuseks võib olla täpsuse teatav kadu. </li>
><ol>
><li> Lepinguvaluutas prognoositav müügisumma teisendatakse esmalt põhivaluutasse (1. teisendamine).</li>
><li> Põhivaluutas prognoositav müügisumma teisendatakse projekti kuluvaluutasse (2. teisendamine). </li>
></ol>
></ol>
> Valuuta täpsust rakendatakse mõlemas etapis, mille tulemusena plaanitud tulu projekti valuutas erineb plaanitud müügist lepinguvaluutas.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Lehe ülesannete tulude ümber kavandamine

Lehe ülesande tööjõutulusid ei saa otse vahekaardil **Jälgimine** lehel **Projekt** uuesti prognoosida. Samas saate kasutada vaadet **Panuse jälgimine**, et prognoosida ülesande järelejäänud panus uuesti. See põhjustab ülesande ülejäänud tulu ümberarvutamist. Selle toimimise kirjeldus on järgmine.

1. Projektijuht saab ülesannete panuse uuesti projekteerida, värskendades välja **Järelejäänud panus** vaikeväärtust ülesande järelejäänud panuse uue prognoosiga. Uuesti projekteerimine põhjustab ülesande panuse prognoosi lõpetamisel, edenemisprotsendi ja ülesande projekteeritud panuse hälbe uuesti arvutamist. Lisaks arvutatakse ümber ka kokkuvõtlike ülesannete EAC, lõpetamise prognoos (ETC) ja edenemisprotsent, mis annavad panuse hälbe uue prognoosi.
2. Sõltuvalt ülesande järelejäänud panuse uuest väärtusest arvutab süsteem järelejäänud tulu vaates **Tulu jälgimine**. Järelejäänud tulu järelejäänud panuse põhjal arvutamiseks arvutab süsteem esmalt ülesande jaoks plaanitud tuluks või plaanitud panuseks keskmise ühe tunni panuse kuluks. Plaanitud tulu on ülesande kõigi ressursimäärangute tulu summa. Tunni keskmist tulu kasutatakse vastloodud projekteeritud ülesande ülejäänud panuse allesjäänud tulu arvutamiseks.
3. Prognoositav tulu lõpetamisel ja tulu kasutamise protsent arvutatakse lehe ülesandel uuesti.
4. Kokkuvõtlike ülesannete lõpetamise tulu väärtus arvutatakse ümber juursõlme tasemeni.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Kokkuvõtte ülesannete tulude ümber kavandamine

Saate tööjõutulu kokkuvõtteülesannete või konteinerülesannete jaoks uuesti projekteerida. Samas te ei saa tööjõutulusid otseselt uuesti projekteerida kokkuvõtte projektiülesannetes vahekaardi **Jälgimine** lehel **Projekt**. Sarnaselt lehe ülesannetele saab kokkuvõtte ja konteineri ülesannete uuesti projekteerimist teha kasutades vaadet **Panuse jälgimine**. Selles vaates saate kokkuvõtteülesande allesjäänud panuse uuesti projekteerida, põhjustades kokkuvõtteülesande järelejäänud tulu uuesti arvutamise. Selle toimimise kirjeldus on järgmine.

1. Projektijuht saab ülesannete panuse uuesti projekteerida, värskendades välja **Järelejäänud panus** vaikeväärtust uue ülesande suvandi **Järelejäänud panus** prognoosiga. Uuesti projekteerimine põhjustab ülesande prognoosi lõpetamisel, edenemisprotsendi ja ülesande projekteeritud panuse hälbe uuesti arvutamist. Lisaks arvutatakse ümber ka kokkuvõtlike ülesannete EAC, ETC ja edenemisprotsent, mis annavad panuse hälbe uue prognoosi.
2. Sõltuvalt ülesande välja **Järelejäänud panus** uuest väärtusest arvutab süsteem järelejäänud tulu vaates **Tulu jälgimine**. Järelejäänud tulu järelejäänud panuse põhjal arvutamiseks arvutab süsteem esmalt ülesande jaoks plaanitud tuluks või plaanitud panuseks keskmise ühe tunni panuse kuluks. Plaanitud tulu on ülesande kõigi ressursimäärangute tulu summa. Seda tunni keskmist tulu kasutatakse seejärel vastloodud projekteeritud ülesande ülejäänud panuse tulu arvutamiseks.
3. Prognoositav tulu lõpetamisel ja tulu kasutamise protsent arvutatakse kokkuvõtte ülesandel uuesti.
4. Lõpetamisel prognoositava tulu uus väärtus jaotatakse alamülesannete vahel sama proportsiooniga, mis ülesande algne plaanitud tulu väärtus.
5. Iga individuaalse ülesande puhul arvutatakse uus prognoositav tulu lõpetamisel kuni lehe ülesannete tasemeni. Selle väärtuse põhjal arvutatakse mõjutatud alamülesannetel kuni leheni järelejäänud tulu ja tulu protsent, mis arvutatakse ümber lõpetamise tulu põhjal. Selle tulemuseks on ülesande tulu hälbe uus prognoos. 
6. Kokkuvõtlike ülesannete lõpetamise tulu väärtus arvutatakse ümber juursõlme tasemeni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

