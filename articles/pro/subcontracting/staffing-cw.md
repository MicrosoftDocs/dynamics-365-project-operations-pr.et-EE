---
title: Projekti mehitamine lepinguliste töötajatega ja allhankelepinguga ressursiruumiga
description: Selles artiklis selgitatakse, kuidas saab projekti nõudeid komplekteerida Microsofti lepinguliste töötajate või allhankevõimsuse abil Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8edb053467ef200ca3e051e2fd78106734318389
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261249"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Projekti mehitamine lepinguliste töötajatega ja allhankelepinguga ressursiruumiga

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Üldised projektimeeskonna liikmed võivad olla töötajad või lepingulised töötajad. Lepinguliste töötajatega projekti personalistamisel saate piirata oma personalivalikud konkreetsete lepinguliste töötajatega, kes on määratud allhankeliinile. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Kindlale allhankereale kuuluvate lepinguliste töötajatega personali ressursinõuete otsimine

Kindlale allhankeliinile kuuluvate lepinguliste töötajate otsimiseks ja personali ressursinõuete täitmiseks tehke järgmist.

1. Looge üldine projektimeeskonna liige, kes viitab allhankele ja allhankereale.
2. Looge selle üldise projektimeeskonna liikme jaoks ressursivajadus, **kasutades projektimeeskonna liikmete alamruudustiku nuppu Loo nõue**.
3. Valige meeskonnaliikme rida ja seejärel valige **alamruudustikus nupp Broneeri**. 
4. See avab ajakavatahvli nõude kontekstiga. Koos muude atribuutidega, nagu kuupäevad, roll ja organisatsiooniüksuse väljad, täidetakse ajakavapaneeli filtrid ressursinõudest automaatselt ka hankija, allhanke ja allhanke rea väljadega.
5. Süsteem otsib filtrikriteeriumidele vastavaid ressursse ja loetleb need. 
6. Valige üks filtreeritud ressurssidest ja broneerige nõude jaoks ressurss. 
7. Projektimeeskonna liige luuakse ja seda värskendatakse alltöövõtu ja allhanke reaviidetega. Minge jaotisse **Projekti prognoosid** ja valige **Värskenda hindu**, et näha ressursimäärangu värskendatud kulu. 

> [!NOTE]
> Projektimeeskonna liikme värskendamine allhanke ja allhanke rea viitega ei pruugi broneerimise ajal alati võimalik olla, kui ressurss on määratud mitmele allhankereale. Kui süsteem ei saa projektimeeskonna liiget alltöövõtu ja allhankereaga värskendada, siis avage projektimeeskonna liikme kirje ja värskendage neid välju käsitsi, et finantskulu prognoos kajastaks täpselt alltöövõtja kulu.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Otsing ja personali ressursinõuded mis tahes lepingulise töötajaga

Mis tahes lepingulise töötaja otsimiseks ja personali ressursinõuete täitmiseks toimige järgmiselt.

1. Looge üldine projektimeeskonna liige.
2. Looge selle üldise projektimeeskonna liikme jaoks ressursivajadus, **kasutades projektimeeskonna liikmete alamruudustiku nuppu Loo nõue**.
3. Valige meeskonnaliikme rida ja seejärel valige **alamruudustikus nupp Broneeri**. 
4. See avab ajakavatahvli nõude kontekstiga. Koos muude atribuutidega, nagu kuupäevad, roll ja organisatsiooniüksuse väljad, täidetakse ajakavapaneeli filtrid ressursinõudest automaatselt ka hankija, allhanke ja allhanke rea väljadega. Kuna nõudel ei olnud täidetud alltöövõtu või allhanke rea väärtusi, on need atribuudid filtripaanil tühjad.
5. Süsteem otsib filtrikriteeriumidele vastavaid ressursse ja loetleb need.
6. **Värskendage filtripaani välja Töötaja tüüp** väärtuseks **Lepinguline töötaja**, et piirata otsingut lepinguliste töötajatega. Värskendage **filtripaanil hankijat**, et valida hankija, kes piirab otsingut, et kuvada ainult konkreetsele hankijaettevõttele kuuluvad lepingulised töötajad.
7. Valige loendist lepinguline töötaja ja broneerige nõude jaoks ressurss.
8. Luuakse projektimeeskonna liige. Projektimeeskonna liiget ei värskendata aga ühegi allhanke- või allhankereaga ja seetõttu ei arvestata ressursimäärangut allhanke hinnakujunduse alusel. Värskendage projektimeeskonna liiget käsitsi allhankereaga ja minge jaotisse **Projekti prognoosid** ning valige **Ressursimäärangu värskendatud kulu kuvamiseks värskenda hinnad**.

> [!NOTE]
> Projektimeeskonna liikmed, kelle tüüp **Töötaja on** Lepinguline töötaja **, kuid kellel pole alltöövõtuviidet, märgistatakse projektimeeskonna liikmete** ruudustikus **sobimatuks** **.** Kui selle olekuga projektimeeskonna liikmeid on, avage projektimeeskonna liikme kirje ja värskendage käsitsi allhanke ja allhanke rea välju, et finantskulu prognoos kajastaks täpselt alltöövõtja kulusid **vahekaardil Prognoosid**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
