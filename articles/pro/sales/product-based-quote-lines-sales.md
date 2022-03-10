---
title: Tootepõhiste hinnapakkumiste ridade ülevaade – liht
description: See teema sisaldab teavet tootepõhiste hinnapakkumise ridadega töötamise kohta.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 871597b38d72d2b670c375d2a1711a6022e3446ba3955a3d2a233a6486d85f5c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003316"
---
# <a name="product-based-quote-lines-overview---lite"></a>Tootepõhiste hinnapakkumiste ridade ülevaade – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Saate luua tootel põhinevaid hinnapakkumise ridu rakenduses Dynamics 365 Project Operations. Tootepõhiste hinnapakkumiste ridu saab lisada käsitsi või need võivad olla tootekataloogi objektid.

## <a name="product-catalog"></a>Tootekataloog

Igal tootekataloogi toodetel on vaikimisi ühik ja ühikurühm. Kui mitmes tootes on sama atribuutide kogum, saate luua tootepere, mis kasutavad neid atribuute ühiselt. 

Näiteks ettevõte müüb kordustellimuse litsentse erinevat tüüpi tarkvara jaoks. Kõikidel kordustellimuse tarkvaradel on järgmised kaks atribuuti.

- Kasutajate arv
- Kuudes mõõdetud tellimuse kestus

Seda tüüpi kataloogi säilitamiseks looge tootepere, mille nimi on **Kordustellimuse tarkvara** ja lisage kasutajate arv ja tellimuse keskus atribuutidena. Järgmisena saate lisada lisada tooteperesse **Kordustellimuse tarkvara** individuaalseid tooteid.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Tootekataloogi üksuste lisamine projekti hinnapakkumisse

Lehtedel **Projekti hinnapakkumine** ja **Projekti leping** on jaotised projektipõhiste ridade ja tootepõhiste ridade jaoks. Projektipõhiste ridade puhul sisaldab hinnapakumise rea või projekti lepingurea ripploend kõiki toote hinnakirja tooteid ja ühikuid. Saate lisada ka tooteid, mis ei kuulu toodete hinnakirja.

Lisaks saate valida tooted teistest hinnakirjadest või otse tootekataloogi kaudu. Kui valite tooted otse tootekataloogi kaudu, kasutatakse toote müügihinna saamiseks selle toote vaikimisi kasutatavat hinnakirja. Kui vaike-hinnakirja ei määrata, määratakse hinnaks null (0).

Kui hinnapakkumise rida põhineb tootekataloogil, saate müügihinna alistada otse hinnapakkumise real. Hinnapakkumise rida väljal **Hinnakujundus**, millel on kaks saadaolevat väärtust.

- **Hinnakirja tühistamine**
- **Kasuta vaikeväärtust**

Kui valite suvandi **Hinnakirja tühistamine**, siis vaikimisi hinda ei määrata. Selle asemel peate sisestama toote hinna hinnapakkumise real. Kui valite suvandi **Kasuta vaikeväärtust**, kasutatakse vaikimisi müügihinda ja see väli on redigeerimiseks lukus.

Vaikimisi müügihinnad sisestatakse hinnapakkumise tootepõhistele ridadele. Välja **Hinnakiri** väärtuseks seatakse **Hinnakirja tühistamine**, et saaksite hinnapakkumise ridadel redigeerida vaikimisi kasutatavat hinda. See on rakendusele Project Operations omane rakenduse Dynamics 365 Sales tootepõhiste ridade käitumise alistamiseks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]