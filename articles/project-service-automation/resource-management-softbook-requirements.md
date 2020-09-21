---
title: Esialgse broneerimise nõuded
description: Selles teemas kirjeldatakse esialgse broneerimise nõudeid.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 97323b73-c6de-4a7f-b889-19d4c42cf17a
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 08a8b46ee03fb93b30d178756e38c3086880f774
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751042"
---
# <a name="soft-book-requirements"></a>Esialgse broneerimise nõuded

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
