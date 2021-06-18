---
title: Esialgse broneerimise nõuded
description: Selles teemas kirjeldatakse esialgse broneerimise nõudeid.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bc58c805bfe1a3087600b8d4a6be2d1bcdd18188
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997911"
---
# <a name="soft-book-requirements"></a>Esialgse broneerimise nõuded

[!include [banner](../includes/psa-now-project-operations.md)]

Ressursinõuet saab fikseeritult broneerida. Fikseeritud broneering loob pakkumise, mis kasutab ressursi võimsust. Seejärel saadetakse pakkumine kinnitamiseks tagasi taotlejale. Esialgne broneering lisab ressursi ebalevalt projektimeeskonda ja sellel on ajakavapaneelil teistsugune olek, kuid see ei tarbi ressursi võimsust. Ressursi esialgseks broneerimiseks ajakavapaneelilt määrake väli **Broneerimise olek** väärtusele **Esialgne**.

![Broneeringu olekuks on määratud Esialgne](media/Resource-Management-image77.png)

Kui vahekaart **Meeskond** on vaates **Nimega meeskonnaliikmed**, kuvatakse ressurss seal. Esialgselt broneeritud tunnid esitatakse veerus **Esialgselt broneeritud tunnid**.

![Esialgselt broneeritud tunnid nimega meeskonnaliikmete vaates](media/Resource-Management-image78.png)

Esialgselt broneeritud meeskonnaliikmeid saab määrata ülesannetele.

![Ülesandele määratud esialgselt broneeritud meeskonnaliige](media/Resource-Management-image79.png)

Vahekaardil **Vastavusseviimine** ei kuvata esialgselt broneeritud ressursile ühtegi broneeringut, kuna vahekaart **Vastavusseviimine** arvestab ainult fikseeritud broneeringutega.

![Broneeringuteta esialgselt broneeritud ressurss vahekaardil Vastavusseviimine](media/Resource-Management-image80.png)

> [!NOTE]
> Te ei saa ressurssi esialgselt broneerida nõudest, mis loodi üldisest meeskonnaliikmest.

Ressursi esialgse broneerimise jaoks kasutatakse ajakavapaneelil erinevat värvi.

![Esialgsed broneeringud ajakavapaneelil](media/Resource-Management-image81.png)

Esialgse broneeringu teisendamiseks fikseeritud broneeringuks paremklõpsake ajakavapaneelil esialgset broneeringut ja seejärel tehke valikud **Muuda olekut** \> **Fikseeritud broneering** \> **Fikseeritud**.

![Broneeringu oleku muutmine fikseerituks](media/Resource-Management-image82.png)

Broneeringut muudetakse ja olekut muudetakse ajakavapaneelil. Kuna broneeringu olekuks on nüüd **Fikseeritud**, kuvatakse ressurss broneerituna ja selle võimsust ning saadavust reguleeritakse.

Sama meetodit saate kasutada ka fikseeritud või esialgse broneeringu ajakavapaneelilt tühistamiseks.

Esialgselt broneeritud ressursi teisendamiseks fikseeritud broneeringuks projekti vahekaardil **Meeskond**, valige ressurss ja seejärel tehke valik **Kinnita**.

![Käsk Kinnita](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]