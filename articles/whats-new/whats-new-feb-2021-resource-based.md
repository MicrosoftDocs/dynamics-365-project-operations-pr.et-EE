---
title: Mis on uut veebruaris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: See teema sisaldab teavet ressursi-/mittelaopõhiste stsenaariumite jaoks mõeldud rakenduse Project Operations 2021. aasta veebruari väljalaskes saadaolevate kvaliteedi värskenduste kohta.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cb6ab1337652d18a30fba56560ffe50f78dd4eb4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589007"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut veebruaris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.

- Project Operations Dataverse'i keskkonnas 4.7.0.95
- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnaversioonis 10.0.16 

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

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektijuhtimine ja raamatupidamine Dynamics 365 Finance 

Lisateavet projektijuhtimise ja raamatupidamise kohta Dynamics 365 Finance. aastal leiate teemast [Mis on uut jaanuar 2021 – Projektitoimingud ressursi-/ladustamata stsenaariumide puhul](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Regulatiivsed uuendused

Finance and Operationsi rakenduste regulatiivsete värskenduste kohta leiate teavet teemast [Regulatiivsed värskendused](/dynamics365/finance/localizations/regulatory-updates). Veel üks võimalus regulatiivsete värskenduste kohta teada saada on logida teenusesse Lifecycle Services (LCS) ja vaadata plaanitud regulatiivseid värskendusi, kasutades probleemide otsingu tööriista. Probleemi otsing võimaldab teil otsida riigi, funktsiooni tüübi ja väljalaske põhjal.


[!INCLUDE[footer-include](../includes/footer-banner.md)]