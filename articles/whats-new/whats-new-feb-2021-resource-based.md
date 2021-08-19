---
title: Mis on uut veebruaris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: See teema sisaldab teavet ressursi-/mittelaopõhiste stsenaariumite jaoks mõeldud rakenduse Project Operations 2021. aasta veebruari väljalaskes saadaolevate kvaliteedi värskenduste kohta.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 41d7d7133652069ca3899db7f12e67e9ba531bcd3e36d67c3686a6b637b077d3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986801"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut veebruaris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.

- Project Operations Dataverse'i keskkonnas 4.7.0.95
- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.16 

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| **Arveldamine ja hinnakujundus** | 2053736 | Arverea üksikasjad on nüüd juurdepääsetav jaotises **Arve** > **Arvega seotud teave**. |
| **Arveldamine ja hinnakujundus** | 2122613 | Toimingud **Aktiveeri** ja **Deaktiveeri** eemaldati **Hinnakirja** seose olemitelt. |
| **Arveldamine ja hinnakujundus** | 2128606 | Lahendatud on probleem tõrkega **ullReferenceException** lisandmoodulis **GetEstimatesForProject**. |
| **Juurutamine ja konfiguratsioon** | 2139346 | Lahendatud on probleem mittehallatava lahenduse **Dynamics365ProjectOperationsDualWrite** importimisega. |
| **Juurutamine ja konfiguratsioon** | 2140569 | Projekti lahendus ei tohi olla installitud Dataverse'i meeskondade keskkondadesse. |
| **Juurutamine ja konfiguratsioon** | 2086991 | Veebiressursside piiratud kohandamise lokaliseerimine. |
| **Müügivõimaluse haldus** | 2136794 | Saate kuvada õige tõrketeate, kui protsessid **Arve kinnitamine** või **Arve tasutuks märkimine** nurjub. |
| **Müügivõimaluse haldus** | 2139330 | Projekti projektijuhi muutmine ei tohi lähtestada omanikuks olevat ettevõtet tagasi vaikeväärtusele. |
| **Müügivõimaluse haldus** | 2146376 | Arve kinnituselt luuakse parandatud maksusumma mittearveldatavad tegelikus näitajas. |
| **Projekti plaanimine ja jälgimine** | 2099879 | Dataverse'i keskkonna juurutamine peab looma tehingu vaikekategooria koos staatilise ID-ga ja mitte seda juhuslikult keskkonna kohta looma. |
| **Projekti plaanimine ja jälgimine** | 2128577 | Parandatud on Project Service'i kasutajaõigused tehingu kategooria värskendamiseks ressursi määramisel. |
| **Projekti plaanimine ja jälgimine** | 2164035 | Parandatud on probleemid funktsiooniga **Projekti kopeerimine**. |
| **Ajakirje** | 2129161 | Rakendatakse kitsamaid piiranguid tagamaks, et kasutajad ei saaks muuta või värskendada esitatud või kinnitatud ajakirjet. |
| **Ajakirje** | 2103572 | Projektiväliste ajakirjete aja kinnitamine ei pea nõudma projekti kinnitaja rolli. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektihaldus ja raamatupidamine rakenduses Dynamics 365 Finance 

Lisateavet projektijuhtimise ja raamatupidamise kohta rakenduses Dynamics 365 Finance vt jaotisest [Mida on uut jaanuaris 2021 - Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Regulatiivsed uuendused

Lisateavet teenuse Finance and Operations rakenduste regulatiivsete uuenduste kohta vaadake teemast [Regulatiivsed uuendused](/dynamics365/finance/localizations/regulatory-updates). Veel üks võimalus regulatiivsete värskenduste kohta teada saada on logida teenusesse Lifecycle Services (LCS) ja vaadata plaanitud regulatiivseid värskendusi, kasutades probleemide otsingu tööriista. Probleemi otsing võimaldab teil otsida riigi, funktsiooni tüübi ja väljalaske põhjal.


[!INCLUDE[footer-include](../includes/footer-banner.md)]