---
title: Projektikategooriate konfigureerimine
description: Selles teemas antakse teavet projektikategooriate seadistamise kohta.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cea43422469adf12f336f7686814a8199717090c18804d3d0a7509452349566e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997106"
---
# <a name="configure-project-categories"></a>Projektikategooriate konfigureerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Project Operations pakub projektide tulude ja kulude kategooriatesse jaotamiseks töökindlad funktsioone. Kategooriad pakuvad võimalust teatada ja analüüsida projekti kandeid ning vedada pearaamatusse märkimist.

Järgmisel diagrammil on toodud kannete kategooriate, ühiskasutuses kategooriate ja projekti kategooriate vaheline korrelatsioon. 

Kannete kategooriad on projekti kannete peamine rühmitamine. Selles rühmas on ühiskasutuses kategooriate komplekt, mida saab rakenduste ja moodulite üleselt ühiselt kasutada. Täpsustades seda veelgi, siis projekti kategooriad on kategooriate kõige granuleeritum tase. Projekti kategooriad on omased juriidilistele olemitele, moodulitele ja rakendusele.

![Kandekategooriate, ühiskategooriate ja projektikategooriate vaheline korrelatsioon.](media/project-categories.png)

## <a name="transaction-categories"></a>Kandekategooriad

Kannete kategooriad esindavad projekti kannete põhirühmitust ja ei ole ettevõttele ega kande tüübile spetsiifilised. Näiteks Contoso Robotics kasutab projektitehingute rühmitamiseks kategooriaid kujundus, sõit, paigaldamine ja hooldustehingud.

Kannete kategooriad on määratletud rakenduse Project Operations moodulis. 
1. Vormi avamiseks avage **Sätted** \> **Tehingu kategooriad**. 
2. Looge uus kande kategooria valides kas suvandi **Uus** või valides **Impordi Excelist**.

## <a name="shared-categories"></a>Ühiskasutuses kategooriad

Dynamics 365 kasutab ühiskasutuses kategooriate mõistet kulude kategoriseerimiseks erinevates rakendustes, näiteks rakendustes Dynamics 365 Finance, Dynamics 365 Supply Chain ja Dynamics 365 Project Operations. Iga loodud kande kategooria jaoks loob Project Operations automaatselt neli seotud üiskasutuses kategooriat: tunnid, kulu, tasud ja kaup. Saate ühiskasutuses kategooriaid läbi vaadata, kui avate **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Kategooriad** \> **Ühiskasutuses kategooriad**.

## <a name="project-categories"></a>Projektikategooriad

Projekti kategooriad esindavad kategooriate konfigureerimise kõige granuleeritumat taset ja peavad olema projekti raamatupidaja poolt konfigureeritud eraldi ja iga ettevõtte jaoks.

1. Avage **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Kategooriad** \> **Projekti kategooriad**.
2. Tehke valik **Uus**.
3. Vaige ühiskasutuses kategooria jaoks **kategooria ID**, mille eelmises jaotises lõite. Project Operations võimaldab ainult nende ühiskasutuses kategooriate kasutamist, mis on tehingu kategooriatega seotud.
4. Valige kategooria rühm.

## <a name="category-groups"></a>Kategooria rühmad

Kategooria rühmasid kasutatakse atribuutide ühiskasutuseks, peamiselt profiilide postitamiseks seotud projekti kategooriate vahel. Igal tehingu tüübil peab olema vähemalt üks kategooria rühm ja igale projekti kategooriale peab olema määratud rühm.

Rakenduses Project Operations on postitamise tehnilised andmed määratletud projekti kulu- ja tuluprofiili reeglite, projekti kategooriate ja kategooriate rühmade poolt. Kategooria rühmad saate häälestada avades **Projektihaldus ja raamatupidamine** \> **Seadistamine** \> **Kategooriad** \> **Kategooria rühmad**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]