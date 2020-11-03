---
title: Miks lähtestub aja kande klassiga tegelike müüginäitajate hind väärtusele 0?
description: Tõrkeotsing, miks aja kande klassiga müüginäitajate hind lähtestub väärtusele 0.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: c886c4a53b4ba47e381b891fe22a565ad8fd1ac6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075080"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Miks lähtestub aja kande klassiga tegelike müüginäitajate hind väärtusele 0?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

See KKK kehtib selliste tegelike näitajate puhul, mille kande klassiks on määratud Aeg ja kande tüübiks Arveldamata müük. Alltoodud kolm kontrolli aitavad leida lahenduse, miks aja kande klassiga tegelike müüginäitajate hind lähtestub väärtusele 0.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>1. kontroll: projekti müügihinnakirja tuvastamine

Leidke projekt tegeliku näitaja projektiväljalt ja minge projekti lehele. Seejärel minge vahekaardile Müük ja klõpsake projekti lepinguridade ruudustikus linki väljal Projekti leping. Avaneb leht Projekti leping. Minge lehel Projekti leping vahekaardile Projekti hinnakirjad. Kontrollige, kas sellele on lisatud vähemalt üks hinnakiri. Kui projekti lepingu projekti hinnakirjade ruudustikus pole manustatud ühtki hinnakirja, siis olete probleemi leidnud. Manustage hinnakiri projekti hinnakirjade ruudustikku. Hinnakirjadel, mida lubatakse siia manustada, peab kontekstiväljaks olema määratud Müük ja hinnakirja valuutaväli peab kattuma projekti lepingus toodud valuutaväljaga. Kui olete vajalikud parandused teinud, looge ajakirje uuesti, kinnitage see ja veenduge, et tegelikus arveldamata müügisummas kuvataks kehtiv hind. 

Kui teil on projekti hinnakirjade ruudustikku manustatud rohkem kui üks projekti lepingu hinnakiri, jätkake lugemist artikli järgmisest kontrollist.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>2. kontroll: kas mõni ülalpool tuvastatud hinnakirjadest kehtib aja kande klassiga tegeliku müüginäitaja kindlal kuupäeval?

Selleks et Project Service'is arvestataks hinnakiri hinna vaikeväärtuseks, peab see hinnakiri rakenduma aja kande klassiga tegeliku müüginäitaja kuupäeval. Kongtrollige järgmist, et näha, kas ülalpool tuvastatud hinnakiri(hinnakirjad) rakenduvad.
- Kontrollige, kas lisatud hinnakirjade üldisel vahekaardil olev algus- ja lõppkuupäev on täidetud. Kui ülalpool tuvastatud hinnakirjade algus- ja lõppkuupäevad on tühjad, on probleem lahendatud. 
- Jätke meelde aja kande klassiga tegeliku müüginäitaja alguskuupäev ja kontrollige, kas mõni tuvastatud hinnakirjadest rakendub sellel päeval. Näiteks peaks aja kande klassiga tegeliku müüginäitaja kuupäev jääma hinnakirja algus- ja lõppkuupäeva vahele. 
    - Kui ükski hinnakiri ei kata seda aja kande klassiga tegeliku müüginäitaja kuupäeva, olete probleemi leidnud. Muutke hinnakirja algus- ja lõppkuupäeva tagamaks, et hinnakiri kataks aja kande klassiga tegeliku müüginäitaja kuupäeva. 
    - Kui rohkem kui üks hinnakiri katab seda aja kande klassiga tegeliku müüginäitaja kuupäeva, olete probleemi leidnud. Saate selle parandada, kui redigeerite hinnakirja(de) algus- ja lõppkuupäevi selliselt, et alles jääb ainult üks hinnakiri, mis katab aja kande klassiga tegeliku müüginäitaja kuupäeva. 
    - Kui alles on ainult üks hinnakiri, mis katab aja kande lassiga tegeliku müüginäitaja kuupäeva, liikuge edasi 3. kontrolli juurde.
Kui olete vajalikud parandused teinud, looge ajakirje uuesti, kinnitage see ja veenduge, et aja kande klassiga tegelikus müüginäitajas kuvataks kehtiv hind.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>3. kontroll: kas hinnakirjas on aja kande klassiga tegeliku müüginäitaja hinnadimensioonidel hind?

Kui olete edukalt lõpetanud 1. ja 2. kontrolli, peaks teil nüüd alles olema ainult üks projekti hinnakiri, mis rakendub aja kande klassiga tegeliku müüginäitaja kuupäeval. Avage see hinnakiri ja minge vahekaardile Rolli hinnad. Veenduge, et aja kande klassiga tegeliku müüginäitaja hinnadimensioonidel oleks ruudustikus rida.

Kui rolli hinna ruudustikus pole aja kande klassiga tegeliku müüginäitaja hinnadimensioonide jaoks ühtki rida, olete probleemi leidnud. Looge rolli hindade ruudustikus rida aja kande klassiga tegeliku müüginäitaja hinnadimensioonide jaoks. Kui see on tehtud, looge ajakirje uuesti, kinnitage see ja veenduge, et aja kande klassiga tegelikule müüginäitajale kuvataks kehtiv hind.

Kui te pärast ülaltoodud kolme kontrolli ei näe aja kande klassiga tegelike müüginäitajate maksumuse kehtivat hinda, esitage tugiteenusepilet. 

