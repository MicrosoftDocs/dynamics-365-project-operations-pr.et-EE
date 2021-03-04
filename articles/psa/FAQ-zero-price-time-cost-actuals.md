---
title: Miks on tegeliku ajakulu vaikeväärtus null?
description: Tõrkeotsing, miks on tegeliku ajakulu vaikeväärtus 0.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 635fe6dfb547e8b9f96ca1786912309a770e24c2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146253"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Miks on tegeliku ajakulu vaikeväärtus null?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

See KKK kehtib sellise tegeliku kulu maksumuse puhul, mille kande liigiks on määratud Aeg ja kande tüübiks Kulu. Alltoodud kolm kontrolli aitavad leida lahenduse, miks on tegeliku ajakulu vaikeväärtus 0.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>1. kontroll: projekti omahinnakirja tuvastamine

Leidke projekt tegeliku näitaja projektiväljalt ja minge siis projekti lehele. Klõpsake väljal lepingut sõlmiva üksuse linki. Kontrollige lehel Lepingut sõlmiv üksus, kas lepingut sõlmival üksusel on omahinnakirjade ruudustikus hinnakiri.

Kui seal on rohkem kui üks hinnakiri, on probleem lahendatud. Project Service'is on ühe organisatsiooniüksuse kohta toetatud ainult üks hinnakiri. Eemaldage sellest olemist kõik hinnakirjad, kuni organisatsiooniüksuse omahinnakirjade ruudustikku jääb alles ainult üks manustatud hinnakiri.

Kui organisatsiooniüksusele pole manustatud ühtki hinnakirja, jätke meelde organisatsiooniüksuse valuuta. Minge rakendusse Project Service, seejärel valige Parameetrid ja avage vahekaart Hinnakirjad. Kontrollige, kas mõne hinnakirja kontekstiväljaks on määratud Kulu ja kas valuuta kattub organisatsiooniüksuse valuutaga.
 
Kui ühtki sellisele kriteeriumile vastavat hinnakirja pole, on probleem lahendatud. Veenduge, et teil oleks vähemalt üks hinnakiri, mille kontekstiks on määratud Kulu, ja valuuta kattuks organisatsiooniüksuse valuutaga.

Kui sellisele kriteeriumile vastab rohkem kui üks hinnakiri, jätkake dokumendi lugemist ja tehke järgmised kontrollid.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>2. kontroll: kas mõni ülalpool tuvastatud hinnakirjadest kehtib tegeliku ajakulu kindlal kuupäeval?

Selleks et Project Service'is arvestataks hinnakiri hinna vaikeväärtuseks, peab see hinnakiri rakenduma tegeliku ajakulu kuupäeval. Kongtrollige järgmist, et näha, kas ülalpool tuvastatud hinnakiri(hinnakirjad) rakenduvad.

- Kontrollige, kas lisatud hinnakirjade üldisel vahekaardil olev algus- ja lõppkuupäev on täidetud. Kui ülalpool tuvastatud hinnakirjade algus- ja lõppkuupäevad on tühjad, on probleem lahendatud. 
- Jätke meelde tegeliku ajakulu alguskuupäev ja kontrollige, kas mõni tuvastatud hinnakirjadest rakendub sellel päeval. Näiteks peaks tegeliku ajakulu kuupäev jääma hinnakirja algus- ja lõppkuupäeva vahele. 
    - Kui ükski hinnakiri ei kata tegeliku ajakulu seda kuupäeva, on probleem lahendatud. Muutke hinnakirja algus- ja lõppkuupäeva tagamaks, et hinnakiri kataks tegeliku ajakulu kuupäeva. 
    - Kui rohkem kui üks hinnakiri katab tegeliku ajakulu seda kuupäeva, on probleem lahendatud. Saate selle parandada, kui redigeerite hinnakirja(de) algus- ja lõppkuupäevi selliselt, et alles jääb ainult üks hinnakiri, mis katab tegeliku ajakulu kuupäeva. 
    - Kui on ainult üks hinnakiri, mis katab tegeliku ajakulu kuupäeva, liikuge edasi järgmise dokumendis toodud kontrolli juurde.
Kui olete vajalikud parandused teinud, looge ajakirje uuesti, kinnitage see ja veenduge, et tegelikus ajakulus kuvataks kehtiv hind.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>3. kontroll: kas hinnakirjas on tegeliku ajakulu hinnadimensioonidel hind?

Kui olete edukalt lõpetanud 1. ja 2. kontrolli, peaks teil nüüd alles olema ainult üks projekti hinnakiri, mis rakendub tegeliku ajakulu kuupäeval. Avage see hinnakiri ja minge vahekaardile Rolli hinnad. Veenduge, et tegeliku ajakulu hinnadimensioonidel oleks ruudustikus rida.

Kui rolli hinna ruudustikus pole tegeliku ajakulu hinnadimensioonide jaoks ühtki rida, on probleem lahendatud. Looge tegeliku ajakulu hinnadimensioonidele rida rolli hindade ruudustikus. Kui see on tehtud, looge ajakirje uuesti, kinnitage see ja veenduge, et tegelikus ajakulus kuvataks kehtiv hind.
 
Kui te pärast ülaltoodud kolme kontrolli ei näe tegeliku ajakulu kehtivat hinda, esitage tugiteenusepilet.



