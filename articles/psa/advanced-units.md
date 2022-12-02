---
title: Ühikurühmad ja ühikud
description: See artikkel annab teavet ühikurühmade ja ühikute kohta.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ed413cc927901308a111263dbad1a59af8fce620
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933395"
---
# <a name="unit-groups-and-units"></a>Ühikurühmad ja ühikud

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ühikurühmad ja ühikud on rakenduses Microsoft Dynamics 365 põhiolemid. Ühik on üks mõõtühik ja mitu ühikut saab rühmitada ühikute rühmadesse. Ühikurühma nimetatakse vahel ka rakenduse Dynamics 365 kasutajaliideses (UI) üksuse ajakavaks. 

Siin on mõned näited ühikutest ja ühikurühmadest.
 
- **Ühikurühm**: vahemaa 
    - **Ühikud**: miil, kilomeeter jne.
- **Ühikurühm**: aeg
    - **Ühikud**: tund, päev, nädal jne. 

Kui seadistate ühikurühmas mitu ühikut, peate seadistama ka nende vahel teisendusteguri, määrates esimese ühiku, mille olete seadistanud ühikurühma vaike-või põhiühikuna. 

Näiteks ühikurühmas **Aeg**, kui seadistate esimeseks ühikuks **Tund**, määrab süsteem ühiku **Tund** vaikeühikuks. Kui teie järgmine seadistatud ühik on **Päev**, peate määrama teisendusteguri ühikust **Päev** ühikuks **Tund**. Kui lisate kolmanda ühikuna **Nädal**, peate seadistama teisendusteguri ühikule **Nädal** ühikute **Päev** või **Tund** osas. 

Järgmisel pildil on toodud näiteks ühiku **Päev** seadistus, kus väljal **Kogus** kuvatakse tundide arv, mis on päevas, ja ühiku **Nädal** seadistus, kus väljal **Kogus** kuvatakse päevade arv, mis on nädalas.

> ![Ühikurühm: teabeleht.](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Ühikute ja ühikurühmade kasutamine

Rakendus Dynamics 365 Project Service Automation kasutab ühikuid ja ühikurühmasid, et töödelda nii kulu kui ka aja hinnanguid ja kirjeid. 

Kulude puhul on igal kulukategooria vaikimisi ühikurühm ja ühik. Need väärtused sisestatakse kulukategooriate hinnakirja kirjetesse vaikeväärtustena. 

Näiteks on teil kulukategooria, mis on nimega **Läbisõit**. Sel on ühikrühm, mis on nimega **Vahemaa** ja vaikimisi ühik, mis on nimega **Miil**. Kui seadistate ühikurühma **Vahemaa** nii, et sellel on kaks ühikut (**Miil** ja **Kilomeeter**), saate kategooria **Läbisõit** jaoks määrata ühes hinnakirjas kaks müügihinda: üks hind miili ja teine kilomeetri kohta.

| Kulukategooria  | Ühikurühm  | Ühik      | Hinnakujundusmeetod  | Ühiku hind  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Läbisõit           | Kaugus      | Miil      | Ühiku hind    | 10 USD            |
| Läbisõit           | Kaugus      | Kilomeeter | Ühiku hind    |  6 USD            |

Projektile kulu sisestamisel määratleb süsteem kategooria ja kulul oleva ühiku kombinatsiooni kaudu hinna. 

| Kulu kirjeldus        | Kulukategooria  | Ühik  | Kogus  | Ühiku hind   |
|----------------------------|---------------------|-------|-----------|----------------|
| Sõida kliendi asukohta | Läbisõit             | Miil  | 10        | 10 USD         |

Iga hinnakirja päises on aja jaoks väli **Vaikimisi ajaühik**. Väärtus seatakse hinnakirja päise loomisel. Seda üksust kasutatakse seejärel selle hinnakirja kõigi rollipõhiste hindade seadistamiseks.

Välja **Hinnapakkumise aeg** hinnapakkumise ridu saab väljendada mis tahes ajaühikus. Projektidele määratud projektide hinnangu read ja ajakirjed saavad kasutada ainult ajaühikut **Tund**. Kui ajakirjes või hinnangu real olev ühik ei vasta selle rolli hinnakirja real olevale ühikule, teisendab süsteem hinna ühikuteks, mis on määratletud projekti hinnangus või projekti tegelikus tehingus.

Järgmises näites kirjeldatakse, kuidas PSA kasutab ühikurühma, ühikuid ja teisendustegureid.
- Ühikud

   - **Ühikurühm**: aeg 
   - **Ühikud**: tund 
    
    - **Päev** – teisendustegur: 8 tundi       
    - **Nädal** – teisendustegur: 40 tundi  
        
- Hinnakirja seadistus projektile A.

    - **Nimi**: UK müügihinnad 2016 
    - **Vaikimisi ajaühik**: päev 
    - **Valuuta**: GBP

| Roll      | Ühikurühm | Ühik | Organisatsiooniüksus | Hind   |
|-----------|------------|------|---------------------|---------|
| Arendaja | Time       | Day  | Jõgi UK          | 800 GBP |

### <a name="time-entry"></a>Ajakirje

Järgmises tabelis on toodud tulemuseks saadud müügiga seotud tehing, mille PSA on loonud kolmetunnine projekti jaoks.


| Projekt   | Tööülesanne    | Roll      | Kogus | Ühik  | Ühiku hind | Arveldamata müügisumma |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projekt A | Kujundus  | Arendaja | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Ajaühiku KKK

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Kas PSA teisendab kulude puhul erinevateks ühikuteks?
Ei. Ühiku teisendus töötab ainult aja puhul. Kulude puhul, kui süsteem ei leia kulude kategooria ja ühiku kombinatsiooni hinda, on vaikimisi hinnaks seatud 0,00.

### <a name="why-does-psa-convert-time-units"></a>Miks PSA ajaühikuid teisendab?
Mõnes riigis või piirkonnas on juriidiline nõue, et arveldusmäärad oleksid seadistatud päevades. Hinnapakkumise tsükli ajal toimuvad hinna läbirääkimised ja allahindlused tehakse kasutades iga tasustatava rolli jaoks päeva hindasid. Ajakava hinnang ja aja sisestamine toimub tundides. Kui soovite seda erinevust ajaühikutes toetada, teisendab PSA ajaühikud.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Kas ajaühikuid saab projekti hinnangutes muuta?
Ei. Ajakava hinnang on praegu piiratud tundidega ja seda ei saa muuta.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Kas ühikuid ja ühikurühmi saab redigeerida, kustutada ja lisada?
Jah. Peale ühikurühma **Aeg** ja ühikut **Tund**, saab kõiki ühikuid kustutada või redigeerida ning uusi ühikuid saab lisada. PSA-s ei saa ühikurühma **Aeg** ja ühikut **Tund** kustutada. Neid saab siiski värskendada tõlgitud tekstiga väljale **Nimi**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
