---
title: Ressursi broneeringud ja kuidas need on seotud ülesande määramistega
description: Selles teemas antakse teavet selle kohta, kuidas hallata nimega ressursse, ressursside broneerimist ja ülesande määramist ning seda, kuidas need üksteisega seotud on.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 03285d324e855ecf933b155559e5a4826420ab25
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075143"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Ressursi broneeringud ja kuidas need on seotud ülesande määramistega


Nimelisi ressursse saab broneerida projekti meeskonnale ja määrata projekti ülesannetele kahel järgmisel viisil.

- Ressursi saab otse projektile reserveerida ja seejärel määrata projekti ülesannetele.
- Ülesandeid saab määrata üldisele ressursile, mida kasutatakse seejärel päris nimelise ressursi otsimiseks ja asendamiseks. 

Mõlemal juhul reserveerib ressursi reserveerimise toiming ressursi võimsuse.

Projekti kavandav projektijuht omab projektiplaani ja ajakava. Sellega, et üldist ressurssi kasutatakse määramiseks ja seejärel luuakse sellest ressursinõue, saab projektijuht projektile ressursse reserveerida projektiplaanis määratud kontuuridega. Nad saavad reserveerida ressursse projektile ja seejärel neid ülesannetele määrata, kuid reserveeringute kontuure ei saa kooskõlastada ülesannete kontuuridega. Broneeringud ei mõjuta projekti ajakava.

Kujutame ette keerukat mitme kattuva ülesandega projekti, kus mitu sama tüüpi ressurssi peavad samal ajal töötama. Kui ressursile antakse kontuur, mis erineb ülesannete koondkontuurist, siis on raske muuta neid ülesandeid nii, et sobitada reserveeringute kontuure nende eri ülesannete ja originaalsete kontuuridega.

Allolevas näites on nelja ülesandega samal ressursil kogupanust kokku 62 tundi kahe nädala jooksul ja olemas on konkreetne kontuur. Kui ressurss Taavi reserveeritakse nende kahe nädala jaoks 62 tunniks teistsuguse kontuuriga, siis on nõue ja reserveeringud kooskõlas.

| **Ülesannete kontuurid**    | **Tunde kokku** | E 04.06 | T 05.06 | K 06.06 | N 07.06 | R 08.06 | L 09.06 | P 10.06 | E 11.06 | T 12.06 | K 13.06 | N 14.06 | R 15.06 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Ülesanne 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Ülesanne 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Ülesanne 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Ülesanne 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Kogusummad**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Taavi saadavus
| **Ressursi reserveering** | **Tunde kokku** | E 04.06 | T 05.06 | K 06.06 | N 07.06 | R 08.06 | L 09.06 | P 10.06 | E 11.06 | T 12.06 | K 13.06 | N 14.06 | R 15.06 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Taavi                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Siiski pole süsteemset viisi, kuidas määrata reserveeritud tundide kontuuri ülesannetele päevade kaupa. Kui projektijuht on nõus muutma projekti ajakava, et see sobiks ressursi saadavusega, siis peavad nad määrangu eemaldama ja muutma kõiki ülesandeid, et need sobiks reserveeringute kontuuridega.

Juhul, kui organisatsioon on andnud projekti plaanimise ülesande nii projektijuhile kui ka ressursihaldurile, määrab projektijuht ajakava, mis hõlmab nõutud töö kontuurid. Ressursihaldur ei tohiks olla võimeline ajakava ilma projektijuhi teadmiseta muutma (muutma pärisressursside reserveerimisel panusekontuure). Kui ressursihaldur täidab midagi, mida projektijuht pole nõudnud, peavad nad jõudma üksmeelele selles, mida projekti ajakavas muuta vaja on.

Kuna reserveeringud ja määrangud pole tihedalt seotud, siis on võimalik reserveerida kontuure, mis erinevad ülesannete kontuuridest, või muuta määranguid nii, et reserveeringud ja määrangud pole kooskõlas.

Vaade **Vastavusse viimine** võimaldab projektijuhil näha iga projekti meeskonnaliikme reserveeringuid ja määranguid. See vaade kasutab värve ja varjutusi, et näidata kohti, kus meeskonnaliikmete reserveeringutes ja määrangutes on ebakõlad. Selle teabe põhjal saab projektijuht teha parandusi ja kas pikendada ressursi reserveeringuid juhtudel, kus pole määranguid ega reserveeringuid, või tühistada reserveeringud, kus ressursid on reserveeritud ilma määranguta.

> [!NOTE]
> Kui liigutate ülesannet, millele olete ise kontuuri seadistanud, siis neid kontuure ei hoita alles. Need kontuurid luuakse uuesti projekti kalendri järgi, et võtta arvesse muutusi töötundides ja puhkepäevades. See on taotluslik, kuna süsteem ei tea esialgse kontuuri eesmärki ja ei saa otsustada, kas kontuuri säilitamine uues ajavahemikus oleks sobiv. Kuna reserveeringud ja määrangud pole ühendatud, siis säilitavad reserveeringud esialgsed reserveeringu kontuurid. Sel juhul peate tühistama ja uue ülesande kontuurile uuesti reserveerima.

