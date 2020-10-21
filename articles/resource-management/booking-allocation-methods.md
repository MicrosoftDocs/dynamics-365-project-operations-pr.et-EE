---
title: Broneeringu eraldusmeetodid
description: Selles teemas antakse teavet selle kohta, kuidas broneeringu eraldusmeetorid Project Operationsis töötavad.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 74f8889022e42a7bbd37879df870401c0e103446
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897671"
---
# <a name="booking-allocation-methods"></a>Broneeringu eraldusmeetodid

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Olenemata sellest, kas lisate meeskonnaliikme projektile otse vahekaardilt **Meeskond** või broneerite ressursi projektile või nõudele ajakavapaneelilt, on paar broneeringu jaotamismeetodit, mida saate kasutada. Selles artiklis selgitatakse, kuidas iga meetod töötab, ja millised meetodid võivad põhjustada ressursside ülebroneerimist.

## <a name="booking-allocation-methods"></a>Broneeringu eraldusmeetodid

Te saate kasutada kuut broneeringu eraldusmeetodit.

- [Täisvõimsus](#full)
- [Järelejäänud võimsus](#remaining)
- [Protsendimaht](#percentage)
- [Jaota tunnid ühtlaselt](#evenly)
- [Eesmise koormuse tunnid](#front)
- [Pole](#none)

### <a name="full-capacity"></a><a name="full"></a>Täisvõimsus 
Täisvõimsuse meetod broneerib määratud kuupäevadeks ressursi täieliku võimsuse. Näiteks kui ressursi kalendris on määratud tööaeg 8 tundi päevas ja 5 päeva nädalas ning algus- ja lõppkuupäevad hõlmavad 5 tööpäeva, siis broneeritakse ressurss 40 tunniks. Reserveeringu tegemisel ei võeta arvesse ressursi allesjäänud tööaega. Kui ressurss on sellel ajavahemikul juba teiste projektide jaoks broneeritud, siis broneeritakse 40 tundi lisatundidena, mis võib põhjustada ülebroneerimist.

### <a name="remaining-capacity"></a><a name="remaining"></a>Järelejäänud võimsus
Järelejäänud võimsuse meetod on saadaval ainult juhul, kui broneerite ajakavapaneeliga otse projekti. See meetod reserveerib ressursi saadavaloleva võimsuse määratud ajavahemikus. Näiteks kui ressursi võimsus on nädalas 40 tundi ja ta on juba broneeritud 10 tunniks nädalas, siis samal nädalal järelejäänud võimsuse meetodiga broneerimise tulemusena broneeritakse selle nädala ülejäänud 30 tundi.

### <a name="percentage-capacity"></a><a name="percentage"></a>Protsendimaht
Osakoormus broneerib määratud kuupäevadeks teatud protsendi ressursi võimsusest. Näiteks kui ressursi kalendris on määratud tööaeg 8 tundi päevas ja 5 päeva nädalas ning algus- ja lõppkuupäevad hõlmavad 5 tööpäeva, broneerib 50% võimsus ressursi 20 tunniks. Iga päeva individuaalsed broneeringud jaotatakse määratud ajavahemikule võrdselt; selle näite puhul oleks see 4 tundi päevas. Reserveeringu tegemisel ei võeta arvesse ressursi allesjäänud tööaega. Kui ressurss on sellel perioodil juba teiste projektide jaoks reserveeritud, siis broneeritakse 20 tundi lisatundidena, mis võib põhjustada ülebroneerimist.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Jaota tunnid ühtlaselt
Jaga ühtlaselt tundide järgi meetod broneerib ressursi määratud arvu tundideks, jagades aega määratud kuupäevadel ühtlaselt igale päevale. Näiteks kui broneerite ressurssi 5 päeva jooksul 20 tunniks, siis jaotab see meetod 20 tundi ühtlaselt 4 tunniks päeva kohta. Reserveeringu tegemisel ei võeta arvesse ressursi allesjäänud tööaega. Kui ressurss on sellel perioodil juba teiste projektide jaoks reserveeritud, siis broneeritakse 20 tundi lisatundidena, mis võib põhjustada ülebroneerimist.

### <a name="front-load-hours"></a><a name="front"></a>Eesmise koormuse tunnid
Jaga eesmine koormus tundide järgi meetod broneerib ressursi määratud arvu tundideks, jagades aega määratud kuupäevadel nii, et suurem koormus jääks algusesse. Eesmise koormuse jagamine täidab ressursi kogu saadavaloleva võimsuse algusest alates. Näiteks kui ressursi töö ajakava on 8 tundi päevas ja 5 päeva nädalas ning tal pole olemasolevaid broneeringuid, siis ressurssi 20 tunniks reserveerimine 5 päeva jooksul tekitab järgmise mustri. 

|                           |    1. päev    |    2. päev    |    3. päev    |    4. päev    |    5. päev    |    Kokku    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Olemasolevad reserveeringud**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Uus reserveering**          |    8        |    8        |    4        |    0        |    0        |    20       |

Eesmise koormuse meetod võtab arvesse olemasolevaid reserveeringuid ja saadavaolevat võimsust. Näiteks kui samal ressursil on töönädalas juba olemas 20 tundi reserveeringuid, siis hõivavad uued reserveeringud allesjäänud võimsuse järgmiselt.

|                     | 1. päev | 2. päev | 3. päev | 4. päev | 5. päev | Kokku |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Olemasolevad reserveeringud** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Uus reserveering**       | 0     | 0     | 4     | 8     | 8     | 20    |

Kuna arvesse võetakse saadavalolevat võimsust, siis võite saada tõrketeate, kui ressursil pole üle jäänud võimsust, mida reserveering hõivata saaks. Selle meetodiga ei saa ülereserveerida.

### <a name="none"></a><a name="none"></a>Pole
Pole meetod on saadaval ainult juhul, kui broneerite projektis vahekaardilt **Meeskond**. See meetod lisab ressursi projektile meeskonnaliikmena, kuid ei loo reserveeringuid, mis hõivaks ressursi võimsuse. Seda meetodit kasutatakse, kui projekti loomisel lisatakse projektijuhi vaikerolliga meeskonnaliige. Projektile lisatakse vaikimisi projekti loonud projektijuhist kasutaja, nii et projekti olemi kirjel oleks omanik ja projektil oleks üks kinnitaja. Kuna sellel kasutajal pole broneeringuid, siis peate ressursi broneerimiseks ressursi kas kustutama ja teise eraldamismeetodiga uuesti lisama, või lisama ressursi ülesannetele ning seejärel kasutama vahekaardil **Sobitamine** käsku **Pikenda broneeringuid**, et ressursile broneeringuid luua.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Eraldamismeetodid, mis põhjustavad ülereserveerimist
Kokkuvõttes – järgmised eraldamismeetodid põhjustavad ülereserveerimist, kui ressurss on juba teistele projektidele määratud (või muudele töökäskudele või ajastatavatele olemitele).

- Täisvõimsus
- Protsendimaht
- Jaga ühtlaselt tundide järgi

Nende kolme eraldamismeetodi kasutamisel ei teavitata teid, kui ressurss on ülereserveeritud. Ülebroneerimise parandamiseks peate kasutama ajakavapaneeli.
