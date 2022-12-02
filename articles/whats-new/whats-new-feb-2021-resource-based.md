---
title: Mis on uut veebruaris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: See artikkel annab teavet ressursi-/mittelaopõhiste stsenaariumite jaoks mõeldud rakenduse Project Operations 2021. aasta veebruari väljalaskes saadaolevate kvaliteedi värskenduste kohta.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1fe1e59a0a3674752fe62525349a50f00e11089b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029610"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut veebruaris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kehtib rakenduse Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

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

Lisateavet projektijuhtimise ja raamatupidamise kohta rakenduses Dynamics 365 Finance, vt jaotisest [Mida uut on jaanuaris 2021 - Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Regulatiivsed uuendused

Lisateavet finants- ja äritoimingute rakenduste regulatiivsete värskenduste kohta, vt [Regulatiivsed värskendused](/dynamics365/finance/localizations/regulatory-updates). Veel üks võimalus regulatiivsete värskenduste kohta teada saada on logida teenusesse Lifecycle Services (LCS) ja vaadata plaanitud regulatiivseid värskendusi, kasutades probleemide otsingu tööriista. Probleemi otsing võimaldab teil otsida riigi, funktsiooni tüübi ja väljalaske põhjal.


[!INCLUDE[footer-include](../includes/footer-banner.md)]