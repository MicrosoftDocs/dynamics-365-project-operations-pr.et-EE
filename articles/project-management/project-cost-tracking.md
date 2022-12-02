---
title: Projektikulu jälgimine
description: See artikkel annab teavet selle kohta, kuidas rakendus Project Operations jälgib projekti edenemist seoses tööjõukulu ja kulutustega.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c069a28c6dc546e5e632c4dff29686dc7965f23e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923735"
---
# <a name="labor-cost-tracking-on-projects"></a>Projektide tööjõukulu jälgimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations jälgib tööjõu prognoose ja kulutusi projektiplaani väikseimal nõutaval väärtusel. Tööjõukulu finantsprognoosimine põhineb plaanitud väärtusel ja üldistel või nimelistel ressurssidel, mis määratakse projektiplaani igale lehe ülesandele. Kui projekt algab ja inimesed hakkavad erinevate projektiülesannete kohta aega märkima, summeeritakse tööjõu tegelik kulu, mis käivitab projekti osade arvutuse.

## <a name="labor-cost-tracking-view"></a>Tööjõukulu jälgimise vaade

Lehel **Projektid** vahekaardil **Jälgimine** saate valida **Jälgimine** > **Kulu**, et avada vaade **Kulujälgimine** ja vaadata tööjõu kulutuse edenemist projektiplaani iga ülesande jaoks. Selles vaates võrreldakse ka tööülesandele kulutatud tegelikku tööjõukulu tööülesande plaanitud tööjõukuluga. Project Operations kasutab tööjõu kulumõõdikute arvutamiseks järgmisi valemeid.

- **Plaanitud kulu**: iga lehe ülesande kõikide ressursi määramiste eeldatav kulu
- **Tegelik kulu**: kõigi kulude tegelike väärtuste summa tööülesandele registreeritud aja jaoks
- **Kulu tarbimise protsent**: tegelik kulu ÷ kuluprognoos lõpetamisel
- **Allesjäänud kulu**: kuluprognoos lõpetamisel – tegelik kulu
- **Kulu lõpetamisel**: järelejäänud kulu – tegelik kulu
- **Kulu hälve**: planeeritud kulu – kuluprognoos lõpetamisel

Iga ülesanne näitab ülesande kuluhälbe projektsiooni. Kui kuluprognoos lõpule viimisel on plaanitud kulust suurem, siis kavandatakse ülesande eelarve ületamine. Kui kuluprognoos lõpule viimisel on plaanitud kulust väiksem, siis kavandatakse ülesande lõpetamine eelarve ülejäägiga.

>[!NOTE]
> Project Operations kuvab tööjõukulud ainult lehel **Projekt** vahekaardil **Jälgimine**. Kuigi materjale ja kulusid saab prognoosida ja jälgida tarbimise jaoks, ei kaasata neid kulusid vahekaardil **Jälgimine** kuvatavate kulude hulka. See vahekaart on loodud toimima ainult tööjõukulude ümber kavandamiseks panuse ümber kavandamisega.
Kõik näidatavad kulusummad teisendatakse projekti kuluvaluutasse projekti omahinna valuutast, mida kasutatakse kulumäära määratlemiseks. Projekti kuluvaluuta on projekti lepinguüksuse valuuta. Aja prognoositava kulu väärtused, mis on näidatud vahekaardi **Projekt** vahekaardil **Prognoosid**, ei pruugita vahekaardi **Jälgimine** plaanitud kulule lisada. Selle vastuolu põhjus on erinevused selles, kuidas summeeritakse ruudustikus **Prognoosid** prognoositud kulusid ja kuidas arvutatakse plaanitud kulusid ruudustikus **Jälgimine**. 
>
> - **Vahekaardil Prognoosid** arvutatakse prognoositav kulu, kasutades hinnakirjas sama kulumäära valuutat. Seejärel teisendatakse prognoositav kulu hinnakirja valuutas prognoositavaks kuluks projekti kuluvaluutas. Prognoositav kulu projektivaluutas näidatakse kahe kümnendkohani ümardatuna. Selle teisendamise ajal pole kordagi valuuta täpsust rakendatud. 
> - Vahekaardil **Jälgimine** järgib plaanitud kulu arvutamine veidi erinevat arvutusjärjestust, mis hõlmab valuuta täpsuse rakendamist kahes etapis. 
   ><ol>
   ><li>Hinnakirja valuutas prognoositav kulusumma teisendatakse põhivaluutasse (1. teisendamine).</li>
   ><li>Põhivaluutas prognoositav kulusumma teisendatakse projekti kulu valuutasse (2. teisendamine). </li>
   ></ol>
   >Valuuta täpsust rakendatakse mõlemas etapis, et saada plaanitud kulu (vahekaardil **Jälgimine**), mis erineb veidi prognoositavast kulust (vahekaardi **Prognoosid** vaates **Ajafaasid**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Lehe ülesannete kulude ümber kavandamine

Lehe ülesande tööjõukulusid ei saa otse vahekaardil **Jälgimine** lehel **Projekt** uuesti prognoosida. Samas saate kasutada vaadet **Panuse jälgimine**, et prognoosida ülesande järelejäänud panus uuesti. See põhjustab ülesande ülejäänud kulu ümberarvutamist. Selle toimimise kirjeldus on järgmine.

1. Projektijuht saab ülesannete panuse uuesti projekteerida, värskendades välja **Järelejäänud panus** vaikeväärtust ülesande järelejäänud panuse uue prognoosiga. Uuesti projekteerimine põhjustab ülesande panuse prognoosi lõpetamisel, edenemisprotsendi ja ülesande projekteeritud panuse hälbe uuesti arvutamist. Lisaks arvutatakse ümber ka kokkuvõtlike ülesannete EAC, lõpetamise prognoos (ETC) ja edenemisprotsent, mis annavad panuse hälbe uue prognoosi.
2. Sõltuvalt ülesande järelejäänud panuse uuest väärtusest arvutab süsteem järelejäänud kulu vaates **Kulu jälgimine**. Järelejäänud kulu järelejäänud panuse põhjal arvutamiseks arvutab süsteem esmalt ülesande jaoks plaanitud kuluks või plaanitud panuseks keskmise ühe tunni panuse kuluks. Plaanitud kulu on ülesande kõigi ressursimäärangute kulu summa. Tunni keskmist kulu kasutatakse vastloodud projekteeritud ülesande ülejäänud panuse allesjäänud kulu arvutamiseks.
3. Kulu lõpetamisel ja kulu kasutamise protsent arvutatakse lehe sõlme ülesandel uuesti.
4. Kokkuvõtlike ülesannete lõpetamise kulu väärtus arvutatakse ümber juursõlme tasemeni.

## <a name="reprojecting-costs-on-summary-tasks"></a>Kokkuvõtte ülesannete kulude ümber kavandamine

Saate tööjõukulu kokkuvõtteülesannete või konteinerülesannete jaoks uuesti projekteerida. Samas te ei saa tööjõukulusid otseselt uuesti projekteerida kokkuvõtte projektiülesannetes vahekaardi **Jälgimine** lehel **Projekt**. Sarnaselt lehe ülesannetele saab kokkuvõtte ja konteineri ülesannete uuesti projekteerimist teha kasutades vaadet **Panuse jälgimine**. Selles vaates saate kokkuvõtteülesande allesjäänud panuse uuesti projekteerida, põhjustades kokkuvõtteülesande järelejäänud kulu uuesti arvutamise. Selle toimimise kirjeldus on järgmine.

1. Projektijuht saab kokkuvõtte ülesannete panuse uuesti projekteerida, värskendades vaikimisi järelejäänud panuse väärtust ülesande uue prognoosiga. See uuendus põhjustab kokkuvõtte ülesande prognoosi lõpetamisel (EAC), edenemisprotsendi ja ülesande projekteeritud panuse hälbe uuesti arvutamist. Lisaks arvutatakse ümber ka kokkuvõtlike ülesannete EAC, ETC ja edenemisprotsent, mis annavad panuse hälbe uue prognoosi.
2. Sõltuvalt kokkuvõtte ülesande järelejäänud panuse uuest väärtusest arvutab süsteem järelejäänud kulu vaates **Kulu jälgimine**. Järelejäänud kulu järelejäänud panuse põhjal arvutamiseks arvutab süsteem esmalt kokkuvõtte ülesande jaoks plaanitud kuluks või plaanitud panuseks keskmise ühe tunni panuse kuluks. Tunni keskmist kulu kasutatakse vastloodud projekteeritud kokkuvõtte ülesande ülejäänud panuse kulu arvutamiseks.
3. Kulu lõpetamisel ja kulu kasutamise protsent arvutatakse kokkuvõtte ülesandel uuesti.
4. Lõpetamise uus kulu jaotatakse alamülesannete vahel sama proportsiooniga, mis ülesande algne plaanitud kulu väärtus.
5. Iga individuaalse ülesande puhul arvutatakse uus kulu lõpetamise väärtusel kuni lehe ülesannete tasemeni. Selle väärtuse põhjal arvutatakse mõjutatud alamülesannetel kuni leheni järelejäänud kulu ja kulu protsent, mis arvutatakse ümber lõpetamise kulu põhjal. Selle väärtuse tulemuseks on ülesande kulu hälbe uus prognoos. 


Välja **Kulu jõudlus** saab määrata jälgimisandmetest. Kui juursõlme kuluhälve on vaates **Kulu jälgimine** negatiivne, saate selle välja määrata valikule **Eelarve ülejääk**. Kui juursõlme kuluhälve on positiivne, saate väärtuseks seada **Ületab eelarvet**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
