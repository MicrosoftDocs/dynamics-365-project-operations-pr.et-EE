---
title: Projekti mehitamine lepinguliste töötajatega ja allhankelepinguga ressursiruumiga
description: Selles artiklis selgitatakse, kuidas projektinõudeid saab microsoftis lepinguliste töötajate või alltöövõtu võimsuse abil komplekteerida Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 173e1c20d2d046ee2120ec178e51d4868b70847d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922079"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Projekti mehitamine lepinguliste töötajatega ja allhankelepinguga ressursiruumiga

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Üldistes projektimeeskonna liikmetes võivad olla töötajad või lepingulised töötajad. Kui kasutate projekti lepinguliste töötajatega, saate piirata oma personalivalikuid kindlate lepinguliste töötajatega, kes on määratud alltöövõtureale. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Personaliressursi nõuete otsimine lepinguliste töötajatega, kes kuuluvad kindlale alltöövõtureale

Konkreetsele alltöövõtureale kuuluvate lepinguliste töötajatega ressursivajaduste otsimiseks ja personali personalivajaduste otsimiseks ja personalitööks tehke järgmist.

1. Looge üldine projektimeeskonna liige, kes viitab alltöövõtu- ja alltöövõtureale.
2. Saate luua selle üldise projektimeeskonna liikme jaoks ressursivajaduse, kasutades **projektimeeskonna liikmete alamruudustiku nuppu Loo nõue**.
3. Valige meeskonnaliikme rida ja seejärel valige **alamruudustikus nupp Raamat**. 
4. See avab ajakava tahvli nõude kontekstiga. Koos teiste atribuutidega (nt kuupäevad, roll ja organisatsiooniüksuse väljad) täidetakse plaanimisnõukogu filtrid automaatselt ka hankija, alltöövõtu ja alltöövõtu rea väljadega ressursivajadusest.
5. Süsteem otsib filtrikriteeriumidele vastavaid ressursse ja loetleb need. 
6. Valige üks filtreeritud ressurssidest ja broneerige nõude ressurss. 
7. Projektimeeskonna liige luuakse ja seda värskendatakse alltöövõtu- ja alltöövõtu rea viidetega. **Ressursimääramise värskendatud maksumuse kuvamiseks avage projekti hinnangud** ja valige **Värskenda hindu**. 

> [!NOTE]
> Projektimeeskonna liikme uuendamine alltöövõtu ja alltöövõtu rea viitega ei pruugi broneeringu ajal alati olla võimalik, kui ressurss on määratud mitmele alltöövõtureale. Kui süsteem ei saa projektimeeskonna liiget alltöövõtu- ja alltöövõtureaga värskendada, avage projektimeeskonna liikmekirje ja värskendage neid välju käsitsi nii, et finantskulude hinnang kajastaks täpselt alltöövõtja kulusid.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Otsingu- ja personaliressursi nõuded mis tahes lepingulise töötajaga

Mis tahes lepingulise töötajaga ressursivajaduste otsimiseks ja personali ressursivajaduste otsimiseks ja personalivajadusteks tehke järgmist.

1. Looge üldine projektimeeskonna liige.
2. Saate luua selle üldise projektimeeskonna liikme jaoks ressursivajaduse, kasutades **projektimeeskonna liikmete alamruudustiku nuppu Loo nõue**.
3. Valige meeskonnaliikme rida ja seejärel valige **alamruudustikus nupp Raamat**. 
4. See avab ajakava tahvli nõude kontekstiga. Koos teiste atribuutidega (nt kuupäevad, roll ja organisatsiooniüksuse väljad) täidetakse plaanimisnõukogu filtrid automaatselt ka hankija, alltöövõtu ja alltöövõtu rea väljadega ressursivajadusest. Kuna nõudes ei olnud alltöövõtu- või alltöövõturea väärtusi täidetud, on need atribuudid filtripaanil tühjad.
5. Süsteem otsib filtrikriteeriumidele vastavaid ressursse ja loetleb need.
6. **Värskendage filtripaani väli Töötaja tüüp** lepingutöötajaks **·**, et piirata otsingut lepinguliste töötajatega. Värskendage **filtripaanil hankijat**, et valida hankija, kes piirab otsingut, et kuvada ainult lepingulised töötajad, kes kuuluvad kindlasse hankija ettevõttesse.
7. Valige loendist lepingutöötaja ja broneerige nõude ressurss.
8. Luuakse projektimeeskonna liige. Projektimeeskonna liiget ei uuendata siiski ühegi allhanke- või allhankereaga ning seetõttu ei kulu ressursi määramist alltöövõtu hinnakujunduse abil. Värskendage projektimeeskonna liiget käsitsi alltöövõtureaga ja minge jaotisse **Projekti hinnangud** ning valige Ressursimääramise värskendatud kulu kuvamiseks suvand **Uuenda hindu**.

> [!NOTE]
> Projektimeeskonna liikmed, kelle tüüp **töötaja on** lepinguline töötaja **, kuid kellel pole alltöövõtu viidet, märgitakse projecti meeskonnaliikmete** ruudustikus **sobimatuks** **.** Kui selle olekuga projektimeeskonna liikmeid on mõni, avage projektimeeskonna liikme kirje ja värskendage alltöövõtu- ja alltöövõturea välju käsitsi nii, et finantskulude hinnang kajastaks täpselt allhankija kulusid vahekaardil **Hinnangud**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
