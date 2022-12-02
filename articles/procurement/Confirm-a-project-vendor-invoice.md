---
title: Projekti hankija arvete kinnitamine
description: See artikkel selgitab, kuidas kinnitada projekti hankija arvet teenuses Microsoft Dynamics 365 Project Operations ja kirjeldatakse projekti hankija arve kinnitamise finantsmõju.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475463"
---
# <a name="confirm-project-vendor-invoices"></a>Projekti hankija arvete kinnitamine

_ **Rakendub:** Project Operations ressursipõhiste/mitteladustatavate stsenaariumite jaoks

Kui parameeter **Käsitsi kinnitus projektijuhi poolt on nõutav** on lubatud, on Microsoft Dataverse’is loodud hankija arvete olek **Mustand**. Sel viisil koostatud hankija arved tuleb üle vaadata ja käsitsi kinnitada. Kui parameeter **Käsitsi kinnitus projektijuhi poolt on nõutav** on keelatud, kinnitatakse Dataverse’is loodud hankija arved automaatselt. Edasist tegevust pole vaja. 

Kui olete teenuses Dynamics 365 Project Operations kinnitanud hankija arvel kõik read, valige hankija arve kinnitamiseks **Kinnita**.

Kui valite hankija arvel valiku **Kinnita**, ilmneb järgmine käitumine.

1. Hankija arve olekuks on **Kinnitatud**.
1. Kinnitatud hankija arve ja sellega seotud kirjed muutuvad kirjutuskaitstuks ning neid ei saa muuta ega kustutada.
1. Kui mis tahes kulu tegelikud näitajad viitavad võrdlusprotsessi osana hankija arve reale, pööratakse kõik viidatud hankija arve reaga seotud kulu tegelikud näitajad ümber.
1. Uued kulu tegelikud näitajad luuakse hankija arve real olevat teavet kasutades.
1. Te ei saa enam luua paranduspäevikuid, töödelda aja sissekannete tagasikutsumisi ega tühistada algselt tagasipööratud aja-, kulu- või materjali tegelike näitajate kinnitamist.
1. Teenuses Dynamics 365 Finance värskendatakse **Projekti kulu** väärtust projekti integreerimise päeviku abil ja hanke integreerimise konto *pööratakse* pärast projekti integreerimise päeviku postitamist.

> [!NOTE]
> Kui hankija arve mõnel real on kinnitusolek muu kui **Täielik**, ei saa hankija arvet kinnitada.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
