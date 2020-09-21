---
title: Broneeringu jaotamise meetodid
description: Selles teemas antakse teavet erinevate võimaluste kohta, kuidas broneeringuid jaotada.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
ms.assetid: 5bb0fdbc-88fe-43eb-8abf-4af9c2352a57
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 030d4fc3bb64fcc67b4a5e51016a8b3a028f3ca8
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750914"
---
# <a name="booking-allocation-methods"></a>Broneeringu jaotamise meetodid

Olenemata sellest, kas lisate meeskonnaliikme projektile otse vahekaardilt **Meeskond** või broneerite ressursi projektile või nõudele ajakavapaneelilt, on paar broneeringu jaotamismeetodit, mida saate kasutada. Selles artiklis selgitatakse, kuidas iga meetod töötab, ja millised meetodid võivad põhjustada ressursside ülebroneerimist.

## <a name="booking-allocation-methods"></a>Broneeringu jaotamise meetodid

### <a name="full-capacity"></a>Täiskoormus 
Täisvõimsuse meetod broneerib määratud kuupäevadeks ressursi täieliku võimsuse. Näiteks kui ressursi kalendris on määratud tööaeg 8 tundi päevas ja 5 päeva nädalas ning algus- ja lõppkuupäevad hõlmavad 5 tööpäeva, siis broneeritakse ressurss 40 tunniks. Reserveeringu tegemisel ei võeta arvesse ressursi allesjäänud tööaega. Kui ressurss on sellel ajavahemikul juba teiste projektide jaoks broneeritud, siis broneeritakse 40 tundi lisatundidena, mis võib põhjustada ülebroneerimist.

### <a name="remaining-capacity"></a>Järelejäänud võimsus
Järelejäänud võimsuse meetod on saadaval ainult juhul, kui broneerite ajakavapaneeliga otse projekti. See meetod reserveerib ressursi saadavaloleva võimsuse määratud ajavahemikus. Näiteks kui ressursi võimsus on nädalas 40 tundi ja ta on juba broneeritud 10 tunniks nädalas, siis samal nädalal järelejäänud võimsuse meetodiga broneerimise tulemusena broneeritakse selle nädala ülejäänud 30 tundi.

### <a name="percentage-capacity"></a>Protsendimaht
Osakoormus broneerib määratud kuupäevadeks teatud protsendi ressursi võimsusest. Näiteks kui ressursi kalendris on määratud tööaeg 8 tundi päevas ja 5 päeva nädalas ning algus- ja lõppkuupäevad hõlmavad 5 tööpäeva, broneerib 50% võimsus ressursi 20 tunniks. Iga päeva individuaalsed broneeringud jaotatakse määratud ajavahemikule võrdselt; selle näite puhul oleks see 4 tundi päevas. Reserveeringu tegemisel ei võeta arvesse ressursi allesjäänud tööaega. Kui ressurss on sellel perioodil juba teiste projektide jaoks reserveeritud, siis broneeritakse 20 tundi lisatundidena, mis võib põhjustada ülebroneerimist.

### <a name="evenly-distribute-hours"></a>Jaga ühtlaselt tundide järgi
Jaga ühtlaselt tundide järgi meetod broneerib ressursi määratud arvu tundideks, jagades aega määratud kuupäevadel ühtlaselt igale päevale. Näiteks kui broneerite ressurssi 5 päeva jooksul 20 tunniks, siis jaotab see meetod 20 tundi ühtlaselt 4 tunniks päeva kohta. Reserveeringu tegemisel ei võeta arvesse ressursi allesjäänud tööaega. Kui ressurss on sellel perioodil juba teiste projektide jaoks reserveeritud, siis broneeritakse 20 tundi lisatundidena, mis võib põhjustada ülebroneerimist.

### <a name="front-load-hours"></a>Jaga eesmine koormus tundide järgi
Jaga eesmine koormus tundide järgi meetod broneerib ressursi määratud arvu tundideks, jagades aega määratud kuupäevadel nii, et suurem koormus jääks algusesse. Eesmise koormuse jagamine täidab ressursi kogu saadavaloleva võimsuse algusest alates. Näiteks kui ressursi töö ajakava on 8 tundi päevas ja 5 päeva nädalas ning tal pole olemasolevaid broneeringuid, siis ressurssi 20 tunniks reserveerimine 5 päeva jooksul tekitab järgmise mustri. 

|                           |    1. päev    |    2. päev    |    3. päev    |    4. päev    |    5. päev    |    Kokku    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Olemasolevad reserveeringud    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Uus reserveering          |    8        |    8        |    4        |    0        |    0        |    20       |

Eesmise koormuse meetod võtab arvesse olemasolevaid reserveeringuid ja saadavaolevat võimsust. Näiteks kui samal ressursil on töönädalas juba olemas 20 tundi reserveeringuid, siis hõivavad uued reserveeringud allesjäänud võimsuse järgmiselt.

|                     | 1. päev | 2. päev | 3. päev | 4. päev | 5. päev | Kokku |
|---------------------|-------|-------|-------|-------|-------|-------|
| Olemasolevad reserveeringud | 8     | 8     | 4     | 0     | 0     | 20    |
| Uus reserveering       | 0     | 0     | 4     | 8     | 8     | 20    |

Kuna arvesse võetakse saadavalolevat võimsust, siis võite saada tõrketeate, kui ressursil pole üle jäänud võimsust, mida reserveering hõivata saaks. Selle meetodiga ei saa ülereserveerida.

### <a name="none"></a>Pole
Pole meetod on saadaval ainult juhul, kui broneerite projektis vahekaardilt **Meeskond**. See meetod lisab ressursi projektile meeskonnaliikmena, kuid ei loo reserveeringuid, mis hõivaks ressursi võimsuse. Seda meetodit kasutatakse, kui projekti loomisel lisatakse projektijuhi vaikerolliga meeskonnaliige. Projektile lisatakse vaikimisi projekti loonud projektijuhist kasutaja, nii et projekti olemi kirjel oleks omanik ja projektil oleks üks kinnitaja. Kuna sellel kasutajal pole broneeringuid, siis peate ressursi broneerimiseks ressursi kas kustutama ja teise eraldamismeetodiga uuesti lisama, või lisama ressursi ülesannetele ning seejärel kasutama vahekaardil **Sobitamine** käsku **Pikenda broneeringuid**, et ressursile broneeringuid luua.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Eraldamismeetodid, mis põhjustavad ülereserveerimist
Kokkuvõttes – järgmised eraldamismeetodid põhjustavad ülereserveerimist, kui ressurss on juba teistele projektidele määratud (või muudele töökäskudele või ajastatavatele olemitele).

- Täisvõimsus
- Protsendimaht
- Jaga ühtlaselt tundide järgi

Nende kolme eraldamismeetodi kasutamisel ei teavitata teid, kui ressurss on ülereserveeritud. Ülebroneerimise parandamiseks peate kasutama ajakavapaneeli.
