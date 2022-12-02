---
title: Projekti mehitamine lepinguliste töötajatega ja allhankelepinguga ressursiruumiga
description: See artikkel selgitab, kuidas projektinõudeid saab teenindada, kasutades rakenduse Microsoft Dynamics 365 Project Operations lepingulisi töötajaid või allhanget.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522430"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Projekti mehitamine lepinguliste töötajatega ja allhankelepinguga ressursiruumiga

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Üldine projektimeeskond võib koosneda töötajatest või lepingulistest töötajatest. Töötajate värbamisel lepinguliste töötajatega saate piirata oma värbamisvõimalusi konkreetsete lepinguliste töötajatega, kes on määratud allhankelepingu reale. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Otsige töötajate ressursivajadusi lepinguliste töötajatega, kes kuuluvad konkreetsele allhankelepingu reale

Konkreetsele allhankelepingu reale kuuluvate lepinguliste töötajate otsimiseks ja töötajate ressursinõuete otsimiseks toimige järgmiselt.

1. Looge üldine projektimeeskonna liige, kes viitab allhankele ja allhankelepingu reale.
2. Looge selle üldise projektimeeskonna liikme jaoks ressursinõue, kasutades projektimeeskonna liikmete alamruudustiku nuppu **Nõude loomine**.
3. Valige meeskonnaliikme rida ja seejärel alamruudustikul nupp **Broneeri**. 
4. See avab nõuete kontekstiga ajakavatahvli. Koos muude atribuutidega, nagu kuupäevad, roll ja organisatsiooniüksuse väljad, täidetakse ajakavatabeli filtrid automaatselt ka ressursinõude hankija, allhankelepingu ja allhankelepingu rea väljadega.
5. Süsteem otsib filtrikriteeriumitele vastavaid ressursse ja loetleb need. 
6. Valige üks filtreeritud ressurssidest ja broneerige ressurss nõude jaoks. 
7. Projektimeeskonna liige luuakse ja värskendatakse allhanke- ja allhankelepingurea viidetega. Minge jaotisesse **Projektiprognoosid** ja valige **Hindade värskendamine**, et näha ressursi määramise värskendatud maksumust. 

> [!NOTE]
> Projektimeeskonna liikme värskendamine allhanke ja allhankelepingurea viitega ei pruugi broneerimise ajal olla alati võimalik, kui ressurss on määratud mitmele alltöövõtuliinile. Kui süsteem ei saa projektimeeskonna liiget allhanke ja allhankelepingureaga värskendada, avage projektimeeskonna liikme kirje ja värskendage neid välju käsitsi nii, et finantskulu prognoos kajastaks täpselt allhanke kulu.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Otsige iga lepingulise töötajaga ja personaliressursside nõudeid

Mis tahes lepingulise töötaja otsimiseks ja personalivajaduste otsimiseks toimige järgmiselt.

1. Projekti üldise meeskonnaliikme loomine.
2. Looge selle üldise projektimeeskonna liikme jaoks ressursinõue, kasutades projektimeeskonna liikmete alamruudustiku nuppu **Nõude loomine**.
3. Valige meeskonnaliikme rida ja seejärel alamruudustikul nupp **Broneeri**. 
4. See avab nõuete kontekstiga ajakavatahvli. Koos muude atribuutidega, nagu kuupäevad, roll ja organisatsiooniüksuse väljad, täidetakse ajakavatabeli filtrid automaatselt ka ressursinõude hankija, allhankelepingu ja allhankelepingu rea väljadega. Kuna nõudes ei olnud täidetud ühtegi allhankelepingut ega allhankelepingurea väärtust, on need atribuudid filtripaanil tühjad.
5. Süsteem otsib filtrikriteeriumitele vastavaid ressursse ja loetleb need.
6. Värskendage filtripaanil välja **Töötaja tüüp** väärtuseks **Lepinguline töötaja**, et piirata otsingut lepinguliste töötajatega. Värskendage filtripaanil valikut **Hankija**, et valida hankija, et piirata otsingut nii, et kuvatakse ainult lepingulised töötajad, kes kuuluvad konkreetsele hankijaettevõttele.
7. Valige loendist lepinguline töötaja ja broneerige nõude jaoks ressurss.
8. Projekti meeskonnaliikme loomine. Kuid projektimeeskonna liiget ei värskendata ühegi allhankelepingu või allhankelepingureaga ja seetõttu ei arvestata ressursi määramist allhankehinna alusel. Värskendage projektimeeskonna liiget käsitsi allhankelepingureaga ja minge jaotisesse **Projekti prognoosid** ja valige **Hindade värskendamine**, et näha ressursi määramise värskendatud maksumust.

> [!NOTE]
> Projektimeeskonna liikmed, kellel on **Töötaja tüüp** kui **Lepinguline töötaja**, kuid kellel ei ole allhankelepingut, on märgitud kui **Kehtetu** ruudustikus **Projektimeeskonna liikmed**. Kui projektimeeskonnal on selles olekus mõni projektimeeskonna liige, avage projektimeeskonna liikme kirje ja värskendage käsitsi alltöövõtu ja alltöövõtu rea välju, nii et finantskulude prognoos kajastaks täpselt alltöövõtja kulusid vahekaardil **Prognoosid**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
