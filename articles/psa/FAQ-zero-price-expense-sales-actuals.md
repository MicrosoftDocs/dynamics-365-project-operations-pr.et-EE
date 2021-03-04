---
title: Miks on tegelike müüginäitajate maksumuse vaikeväärtus null?
description: Alltoodud kolm kontrolli aitavad leida lahenduse, miks on tegelike müüginäitajate maksumuse vaikeväärtus 0.
author: rumant
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: d4910d3727085a45036f3b438ecd69abc3e99836
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146298"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Miks on tegelike müüginäitajate maksumuse vaikeväärtus null?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

See KKK kehtib selliste tegelike maksumuste puhul, mille kande liigiks on määratud Kulu ja kande tüübiks Arveldamata müük. Alltoodud kolm kontrolli aitavad leida lahenduse, miks on tegelike müüginäitajate maksumuse (arveldusmäär) vaikeväärtus 0.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>1. kontroll: projekti müügihinnakirja tuvastamine

Leidke projekt tegeliku näitaja projektiväljalt ja minge projekti lehele. Seejärel minge vahekaardile Müük. Klõpsake projekti lepinguridade ruudustikus linki väljal Projekti leping. Avatakse leht Projekti leping. Minge lehel Projekti leping vahekaardile Projekti hinnakirjad. Kontrollige, kas sellele on lisatud vähemalt üks hinnakiri.

Kui projekti lepingu projekti hinnakirjade ruudustikus pole ühtki hinnakirja, tehke järgmist.

- Manustage hinnakiri projekti hinnakirjade ruudustikku. Hinnakirjadel, mida lubatakse siia manustada, peab kontekstiväljaks olema määratud Müük ja hinnakirja valuutaväli peab kattuma projekti lepingus toodud valuutaväljaga. Kui olete vajalikud parandused teinud, looge kulukirje uuesti, kinnitage see ja veenduge, et tegelikus arveldamata müügisummas kuvataks kehtiv hind.
- Kui teil on projekti hinnakirjade ruudustikku manustatud rohkem kui üks projekti lepingu hinnakiri, vaadake 2. kontrolli.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>2. kontroll: kas mõni ülalpool tuvastatud hinnakirjadest kehtib tegeliku kulu kindlal kuupäeval?

Selleks et Project Service arvestaks hinnakirja hinna vaikeväärtuseks, peab see hinnakiri rakenduma tegelike müüginäitajate maksumuse kuupäeval. Kongtrollige järgmist, et näha, kas ülalpool tuvastatud hinnakiri(hinnakirjad) rakenduvad.

- Kõigepealt kontrollige, kas manustatud hinnakirjade üldisel vahekaardil olevad algus- ja lõppkuupäevad on täidetud. Kui ülalpool tuvastatud hinnakirjade algus- ja lõppkuupäevad on tühjad, on probleem lahendatud. 
- Jätke meelde tegelike müüginäitajate maksumuse alguskuupäev ja kontrollige, kas mõni tuvastatud hinnakirjadest rakendub sellel päeval. Näiteks peaks tegeliku kulu kuupäev jääma hinnakirja algus- ja lõppkuupäeva vahele. 
    - Kui ükski hinnakiri ei kata tegelike müüginäitajate maksumusel seda kuupäeva, on probleem lahendatud. Muutke hinnakirja algus- ja lõppkuupäeva, tagamaks, et hinnakiri kataks tegeliku kulu kuupäeva. 
    - Kui rohkem kui üks hinnakiri katab tegelike müüginäitajate maksumusel seda kuupäeva, on probleem lahendatud. Redigeerige hinnakirja(de) algus- ja lõppkuupäevi selliselt, et alles jääb ainult üks hinnakiri, mis katab tegeliku kulu kuupäeva. 
    - Kui alles on ainult üks hinnakiri, mis katab tegeliku kulu kuupäeva, liikuge edasi 3. kontrolli juurde.
Kui olete vajalikud parandused teinud, looge kulukirje uuesti, kinnitage see ja veenduge, et tegelikus arveldamata müügisummas kuvataks kehtiv hind.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>3. kontroll: kas rakenduvas projekti hinnakirjas on kulu kategoorial kehtiv hind? 

Kui olete edukalt lõpetanud 1. ja 2. kontrolli, peaks teil nüüd alles olema ainult üks projekti hinnakiri, mis rakendub tegelike müüginäitajate maksumuse kuupäeval. Avage see projekti hinnakiri ja minge vahekaardile Kategooria hinnad. Veenduge, et tegelikul kulul oleks ruudustikus kindel kulukategooria rida.
 
- Kui ühtegi rida pole, on probleem lahendatud. Looge tegeliku kulu kategooriale rida kategooria hinna ruudustikus. Seejärel looge kulukirje uuesti, kinnitage see ja veenduge, et tegelikus arveldamata müügisummas kuvataks kehtiv hind. 
- Kui kulu kategooria jaoks on kategooria hindade ruudustikus rida, kontrollige, kas sellel on kehtiv hind.

Kehtiva hinna mõistmiseks kasutage järgmisi meetodeid.

- Kui kategooria hinna rea välja Hinnakujundusmeetod väärtuseks on seatud Omahinnaga, määratakse tegelike müüginäitajate maksumuse ühiku hinnaks vaikimisi kulukirjes olev väärtus.
- Kui kategooria hinna rea välja Hinnakujundusmeetod väärtuseks on seatud Hinnalisandi protsent, siis kontrollige, kas väljal Protsent on määratud kehtiv väärtus. Tegelike müüginäitajate maksumuse ühiku hind määratakse vaikimisi seda hinnalisandi protsenti kulukirjes toodud hinnale rakendades.
- Kui kategooria hinna rea välja Hinnakujundusmeetod väärtuseks on seatud Ühiku hind, siis kontrollige, kas väljal Hind on määratud kehtiv väärtus. Tegelike müüginäitajate maksumuse ühiku hinnaks määratakse vaikimisi väljal Hind määratud valuutasumma.

Kui kulukategooria hinnaseadistus pole kehtiv, on probleem lahendatud. Lahendus on redigeerida kategooria hinna rida kulukategooria kehtiva hinnaga kooskõlas ülaltoodud reeglitega. Kui see on tehtud, looge kulukirje uuesti, kinnitage see ja veenduge siis, et tegelikus arveldamata müügisummas kuvataks kehtiv hind.

Kui te pärast ülaltoodud kolme kontrolli ei näe tegelike müüginäitajate maksumuse kehtivat hinda, esitage tugiteenusepilet.




[!INCLUDE[footer-include](../includes/footer-banner.md)]