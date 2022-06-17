---
title: Mis on uut märtsis 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: Selles artiklis antakse teavet kvaliteedivärskenduste kohta, mis on saadaval 2021. aasta märtsi väljaandes Project Operations ressursi-/ladustamata stsenaariumide jaoks.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fbdcb01117c39f879f80319b01d278c91a56e8f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932935"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut märtsis 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kehtib järgmiste Dynamics 365 Project Operations komponentide ja versioonide kohta.

- Project Operations Dataverse’i keskkonna versioonis 4.8.0.91 
- Projektijuhtimine ja Dynamics 365 Finance keskkonnaversiooni arvestus 10.0.16 

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse


| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2133873 | Parandatud on **Ühiku müügihinna** valuuta sümbol ruudustikus **Kuluprognoosid**. |
| Arveldamine ja hinnakujundus | 2174616 | Kui hinnapakkumine võidetakse, viidatakse lepingu kohandatud hinnakirjale lepingurea üksikasjades, mis kopeeritakse hinnapakkumisest. |
| Müügivõimaluse haldus | 2167475 | Parandatud on maksusumma parandusarves, mis pärines arveldamata tegelikust kirjest. |
| Müügivõimaluse haldus | 2176285 | Maksusummat ei tohi kopeerida müügilepingu/hinnapakkumise rea üksikasjadest kululepingu/hinnapakkumise rea üksikasjadesse. |
| Müügivõimaluse haldus | 2188079 | Jagatud arveldamise reeglit ei tohi luua lepingute jaoks, mis ei põhine tööl. |
| Plaanimine ja jälgimine | 2125274 | Atribuut **Projekti topeltkirjutuse vastendus** atribuudile **Projekti alguskuupäeva vastendus** värskendati väärtuselt **msdyn\_taskearlieststart** väärtusele **msdyn\_actualstart**. |
| Plaanimine ja jälgimine | 2138853 | Projekti kopeerimise funktsioon värskendati, et tagada tööülesandele viitavate kuluprognoosi ridade kopeerimine sihtprojekti. |
| Plaanimine ja jälgimine | 2154306 | Parandatud on probleemid kuluprognooside kustutamisega Project Operationsis ressursipõhiste stsenaariumide puhul. |
| Plaanimine ja jälgimine | 2173259 | Projekti kopeerimisfunktsioon on värskendatud, et tagada, et see ei kuvaks teatud stsenaariumite korral tõrketeadet **WBS-i kopeerimine**. |
| Aeg ja kulu | 2148910 | Lahendatud on kuvamisprobleem lehel **Kirje redigeerimine** ruudustikus **Ajakirje**. |
| Aeg ja kulu | 2159798 | Süvendati kontrolli tagamaks, et kinnitatud kulukirjeid ei saaks redigeerida. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektijuhtimine ja raamatupidamine Dynamics 365 Finance

Lisateavet vaadake jaotisest [Mis on uut jaanuaris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Regulatiivsed uuendused

Finance and Operationsi rakenduste regulatiivsete värskenduste kohta leiate teavet teemast [Regulatiivsed värskendused](/dynamics365/finance/localizations/regulatory-updates). Veel üks võimalus regulatiivsete värskenduste kohta teada saada on logida teenusesse LCS ja vaadata plaanitud regulatiivseid värskendusi, kasutades probleemide otsingu tööriista. Probleemi otsing võimaldab teil otsida riigi, funktsiooni tüübi ja väljalaske põhjal.


[!INCLUDE[footer-include](../includes/footer-banner.md)]