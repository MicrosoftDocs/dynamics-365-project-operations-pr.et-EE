---
title: Tootepõhiste lepinguridade ülevaade – liht
description: Selles teemas antakse teavet tootepõhiste lepinguridade kohta.
author: rumant
ms.date: 10/07/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8006e90e0d4fdf02042f26b261775a92f87f47ca
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598207"
---
# <a name="product-based-contract-lines-overview---lite"></a>Tootepõhiste lepinguridade ülevaade – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Saate luua tootel põhinevaid lepinguridu rakenduses Dynamics 365 Project Operations. Tootepõhiseid lepinguread võivad olla käsitsi loodud read või need võivad olla tootekataloogi objektid.

## <a name="product-catalog"></a>Tootekataloog

Tootekataloogi toodetel on vaikimisi ühik ja ühikurühm. Kui mitmes tootes on sama atribuutide kogum, saate luua ka tootepere, millel on ka need atribuudid. Kõik ühe tootepere tooted pärivad sama hulga atribuute.

Näiteks ettevõte müüb kordustellimuse litsentse erinevat tüüpi tarkvara jaoks. Kõikidel kordustellimuse tarkvaradel on järgmised kaks atribuuti.

- Kasutajate arv
- Kordustellimuse kestus (kuudes)

Seda tüüpi kataloogi säilitamiseks looge tooteperekond nimega **Kordustellimuse tarkvara**. Lisage tooteperekonnale atribuudid **Kasutajate arv** ja **Kordustellimuse kestus**. Seejärel lisage tooteperekonda **Kordustellimuse tarkvara** üksikud tooted.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Tootekataloogi üksuste lisamine projekti lepingusse

Projekti lepingutel on jaotised kahte tüüpi ridade jaoks - projektipõhised ja tootepõhised. Tootepõhised read hõlmavad kõiki lepingu toote hinnakirja tooteid ja ühikuid. Lisada saab tooteid, mis ei ole lepingu toodete hinnakirja osaks.

Saate valida tooteid teistest hinnakirjadest või otse tootekataloogist. Kui valite tooted otse tootekataloogi kaudu, kasutatakse toote müügihinna saamiseks selle toote vaikimisi kasutatavat hinnakirja. Kui vaike-hinnakirja ei määrata, määratakse hinnaks 0 (null).

Kui lepingurida põhineb tootekataloogil, saate müügihinna alistada otse real. Lepingureal on kahe väärtusega väli **Hinnakujundus**.

- **Hinnakirja tühistamine**
- **Kasuta vaikeväärtust**

Kui määrate välja **Hinnakujundus** väärtuseks **Hinnakirja tühistamine**, ei määrata vaikehinda. Sisestage lepingureal tootele hind. Kui määrate välja olekuks **Kasuta vaikeväärtust**, kasutatakse vaikimisi müügihinda ja välja ei saa redigeerida.

Pärast seda, kui olete Project Operationsi installinud, sisestatakse vaikimisi müügihinnad lepingu tootepõhistele ridadele. Välja **Hinnakiri** väärtuseks seatakse **Hinnakirja tühistamine**, et saaksite lepinguridadel vaikimisi kasutatavat hinda redigeerida. See on Project Operationsile spetsiifiline tootepõhiste ridade tühistamine käitumine rakenduses Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]