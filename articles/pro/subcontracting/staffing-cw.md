---
title: Projekti komplekteerimine lepinguliste töötajate ja alltöövõtuvõimsusega
description: Selles teemas selgitatakse, kuidas projektinõudeid saab microsofti lepinguliste töötajate või alltöövõtuvõimsuse abil komplekteerida Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903651"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Projekti komplekteerimine lepinguliste töötajate ja alltöövõtuvõimsusega

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Üldise projekti meeskonna liikmeid saab komplekteerida töötajate või lepinguliste töötajatega. Lepinguliste töötajatega projekti personali määramisel saate piirata oma personalivalikuid konkreetsete lepinguliste töötajatega, kes on määratud allhankeliinile. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Konkreetsele alltöövõtuliinile kuuluvate lepinguliste töötajate personaliressursside nõuete otsimine

Konkreetsele alltöövõtuliinile kuuluvate lepinguliste töötajate otsimiseks ja personaliressursside nõuete otsimiseks tehke järgmist.

1. Looge üldine projektimeeskonna liige, mis viitab alltöövõtu- ja alltöövõtureale.
2. Selle üldise projektimeeskonna liikme ressursivajaduse loomine, kasutades **projektimeeskonna** liikmete alamruudustiku nuppu Loo nõue.
3. Valige meeskonnaliikme rida ja seejärel **valige** alamruudustikus nupp Raamat. 
4. See avab ajakava juhatuse nõude kontekstiga. Koos teiste atribuutidega(nt kuupäevad, roll ja organisatsiooniüksuse väljad) asustatakse plaanigraafiku filtrid automaatselt ka ressursivajaduse hankija, allhanke ja alltöövõtu rea väljadega.
5. Süsteem otsib ressursse, mis vastavad filtrikriteeriumidele, ja loetleb need. 
6. Valige üks filtreeritud ressurssidest ja broneerige nõude ressurss. 
7. Projektimeeskonna liige luuakse ja uuendatakse allhanke- ja alltöövõturea viidetega. Ressursi **määramise** värskendatud maksumuse kuvamiseks avage projekti hinnangud ja valige **Värskenda** hindu. 

> [!NOTE]
> Projektimeeskonna liikme värskendamine allhanke ja alltöövõtuliini viitega ei pruugi broneeringu ajal alati võimalik olla, kui ressurss on määratud mitmele alltöövõtureale. Kui süsteem ei saa projektimeeskonna liiget allhanke- ja alltöövõtureaga värskendada, avage projektimeeskonna liikme kirje ja värskendage neid välju käsitsi nii, et finantskulude hinnang kajastaks täpselt alltöövõtja kulu.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Otsi ja personali ressursi nõuded mis tahes lepingulise töötajaga

Lepingulise töötaja otsimiseks ja personaliressursside nõuete otsimiseks tehke järgmist.

1. Looge üldine projektimeeskonna liige.
2. Selle üldise projektimeeskonna liikme ressursivajaduse loomine, kasutades **projektimeeskonna** liikmete alamruudustiku nuppu Loo nõue.
3. Valige meeskonnaliikme rida ja seejärel **valige** alamruudustikus nupp Raamat. 
4. See avab ajakava juhatuse nõude kontekstiga. Koos teiste atribuutidega(nt kuupäevad, roll ja organisatsiooniüksuse väljad) asustatakse plaanigraafiku filtrid automaatselt ka ressursivajaduse hankija, allhanke ja alltöövõtu rea väljadega. Kuna nõudel ei olnud alltöövõtu- või alltöövõturea väärtusi täidetud, on need atribuudid filtripaanil tühjad.
5. Süsteem otsib ressursse, mis vastavad filtrikriteeriumidele, ja loetleb need.
6. Värskendage **filtripaani välja Töötaja tüüp** **lepingulisele** töötajale, et piirata otsingut lepinguliste töötajatega. Värskendage **filtripaanil** hankijat, et piirata otsingut ainult kindlasse hankijaettevõttesse kuuluvate lepinguliste töötajate kuvamiseks.
7. Valige loendist lepinguline töötaja ja broneerige nõude jaoks ressurss.
8. Luuakse projektimeeskonna liige. Projektimeeskonna liiget ei uuendata siiski ühegi alltöövõtu- või alltöövõtuliiniga ning seetõttu ei lähe ressursi määramine alltöövõtuhinna abil kalliks maksma. Värskendage projektimeeskonna liiget käsitsi alltöövõtureaga ja minge **projecti hinnangutele** ja valige Ressursi määramise **värskendatud maksumuse kuvamiseks suvand Uuenda** hindu.

> [!NOTE]
> Projektimeeskonna liikmed, mille töötaja tüüp **on** **lepinguline** töötaja, kuid kellel pole alltöövõtu viidet, märgitakse **projekti** **meeskonnaliikmete** ruudustikus kehtetuks. Kui selle olekuga projektimeeskonna liikmeid on, avage projektimeeskonna liikmekirje ning värskendage alltöövõtu- ja alltöövõturea välju käsitsi nii, et finantskulude hinnang kajastaks täpselt allhankija kulu **vahekaardil** Hinnangud. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
