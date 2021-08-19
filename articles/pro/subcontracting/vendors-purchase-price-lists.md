---
title: Hankija ja ostuhinnakirja haldus rakenduses Project Operations
description: Selles teemas antakse teavet, mis aitab teil allhankelepingute jaoks luua ja hallata hankija andmeid ning ostuhinnakirju.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf62ef8eb87ac2bc138e63c7f92132e00451df6d7766291a8399a94a070799ab
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994136"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Hankija ja ostuhinnakirja haldus rakenduses Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

## <a name="vendors-in-project-operations"></a>Hankijad rakenduses Project Operations

Rakenduses Microsoft Dynamics 365 Project Operations on hankija kontol seosetüüp **Hankija** või **Tarnija**. Saate valida ainult kontokirje, millel on allhankelepingus hankijana toodud üks neist seosetüüpidest.

Hankijakirjega saate seostada ühe või mitu ostuhinnakirja. Kuid igal hankijakirjega seotud ostuhinnakirjal peab olema kindel kehtivuskuupäev. Project Operations ei toeta ostuhinnakirjade puhul kattuvaid kehtivuskuupäevi.

Vaikimisi kasutatakse hankijakirjes mis tahes hankija jaoks loodud allhankelepingu puhul järgmiseid välju ja mõisteid.

- Maksetingimused
- Maksja: kontakt
- Esmane kontakt

    > [!NOTE]
    > Vaikimisi kasutatakse hankija allhankelepingu kontohaldurina hankija esmast kontakti.

- Valuuta
- Praegused ostuhinnakirjad

## <a name="purchase-price-lists-in-project-operations"></a>Ostuhinnakirjad rakenduses Project Operations

Ostuhinnakirjaks loetakse hinnakirja, kus välja **Kontekst** väärtuseks on **Ost**. Ostuhinnakirju saab määratleda aja, kulude ja materjalide ostumäärade kataloogi tähistamiseks. Ostuhinnakirjad sarnanevad rakenduse Project Operations kulu- ja müügihinnakirjadega. Järgmiseid mõisteid saab rakendada ostuhinnakirjadele samamoodi, nagu need kehtivad kulu- ja müügihinnakirjadele.

- **Kehtivuskuupäev** – ostuhinnakirjadel on kehtivuskuupäev. Kehtivuskuupäeva tähistavad igas hinnakirjas olevad algus- ja lõppkuupäeva väljad. Algus- ja lõppkuupäeva vaheline aeg on kehtivuskuupäeva periood.
- **Valuuta** – hinnakirja päises olevat valuutat kasutatakse valuutana, milles ostuhindu kataloogi tööjõu, kulukategooriate ja toodete puhul väljendatakse.
- **Vaikeajaühik** – vaikeajaühik väljendab ostude tööjõuhindu. Hinnakirja ajaühiku välja kasutatakse ainult vaikeväärtuse andmiseks. Seda väärtust saab muuta üksikute rollide hinnaridadel.

Ostuhinnakirju saab lisada hankijakirjetele seostena, mida nimetatakse projekti hinnakirjadeks. Neid hinnakirju kasutatakse allhankelepingu ridadele vaikehindade sisestamiseks. Kui hankijakirjele on lisatud mitu ostuhinnakirja, kasutatakse hankija jaoks loodud allhankelepingute puhul vaikimisi kõige ajakohasemat hinnakirja. Hankijakirjetele saab manustada ainult neid hinnakirju, kus välja **Kontekst** väärtuseks on **Ost**.

### <a name="subcontract-specific-purchase-price-lists"></a>Konkreetsele allhankelepingule mõeldud hinnakirjad

Ostuhinnakirju saab lisada allhankelepingutele ka seostena, mida nimetatakse projekti hinnakirjadeks. Neid hinnakirju kasutatakse allhankelepingu ridadele vaikehindade sisestamiseks. Vaikimisi, kui allhankelepingule on lisatud mitu ostuhinnakirja, peab igal ühel neist olema erinev kehtivuskuupäev. Project Operations ei toeta ostuhinnakirju, millel on kattuvad kehtivuskuupäevad. Allhankelepingutele saab manustada ainult neid hinnakirju, kus välja **Kontekst** väärtuseks on **Ost**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
