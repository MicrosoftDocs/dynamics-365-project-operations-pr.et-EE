---
title: Fikseeritud hinnaga tulukalkulatsiooniga projektid
description: See artikkel annab teavet projektide fikseeritud hinnaga prognoosi kohta.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928381"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Fikseeritud hinnaga tulukalkulatsiooniga projektid 

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Kui te loote rakenduses Dynamics 365 Project Operations teenuses Microsoft Dataverse järgmiste atribuutidega projekti lepingurea, loob süsteem automaatselt fikseeritud hinnaga tulukalkulatsiooniga projekti. Selle projekti teave põhineb järgneval.

  - Fikseeritud hinnaga arveldusmeetod.
  - Seostatud projekt.
  - Vähemalt üks vahe-eesmärk, mis on määratletud vahekaardil **Arve ajakava** lehel **Projekti lepingurida**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Fikseeritud hinnaga tulukalkulatsioonidega projektide läbivaatamine
Fikseeritud hinnaga tulukalkulatsioonidega projektide läbivaatamiseks tehke järgmist.

1. Avage rakenduse Dynamics 365 Finance keskkonnas suvand **Projektihaldus ja raamatupidamine** > **Projektid** > **Fikseeritud hinnaga tulukalkulatsiooniga projektid**.
2. Valige projekt, mida soovite vaadata, ja topeltklõpsake suvandit **Hinnangu projekti ID**, et avada kirje ja vaadata läbi projekti üksikasjad.
3. Laiendage vahekaarti **Projekt**. Näete ruudustikus **Valitud projektid** ühte projekti. Süsteem kasutab seda vaikimisi projektina, kuna see on projekti lepingureaga seostatud projekt. 
4. Seose muutmiseks valige täiendavad projektid ja lisage need ruudustikku **Valitud projektid**. Kui selles ruudustikus on valitud mitu projekti, siis projekti lõpuleviimise protsent ja tulukalkulatsioonid arvutatakse kõikide valitud projektide jaoks koos.

  Projekti kulu, tuluprofiili, kulumalli ja perioodi koodi saab määrata käsitsi. Kui neid käsitsi ei määrata, lisatakse väärtuste vaikeväärtused projekti esimese hinnangu arvutamise ajal, mis kasutab projektikulu ja tuluprofiilide jaoks konfigureeritud reegleid.



[!INCLUDE[footer-include](../includes/footer-banner.md)]