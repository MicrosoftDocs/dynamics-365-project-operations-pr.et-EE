---
title: Fikseeritud hinnaga tulukalkulatsiooniga projektid
description: Selles teemas antakse teavet projektide fikseeritud hinnaga prognoosi kohta.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531408"
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

