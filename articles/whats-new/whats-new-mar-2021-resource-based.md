---
title: Mis on uut märtsis 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: See artikkel sisaldab teavet ressursi-/mittelaopõhiste stsenaariumite jaoks mõeldud rakenduse Project Operations 2021. aasta märtsi väljalaskes saadaolevate kvaliteedivärskenduste kohta.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e93b4eaad98267f163bad4aff3e4fdcc661e2ab0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028183"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut märtsis 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kehtib rakenduse Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Project Operations Dataverse’i keskkonna versioonis 4.8.0.91 
- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.16 

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

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektihaldus ja raamatupidamine rakenduses Dynamics 365 Finance

Lisateavet vaadake jaotisest [Mis on uut jaanuaris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Regulatiivsed uuendused

Lisateavet finants- ja äritoimingute rakenduste regulatiivsete värskenduste kohta, vt [Regulatiivsed värskendused](/dynamics365/finance/localizations/regulatory-updates). Veel üks võimalus regulatiivsete värskenduste kohta teada saada on logida teenusesse LCS ja vaadata plaanitud regulatiivseid värskendusi, kasutades probleemide otsingu tööriista. Probleemi otsing võimaldab teil otsida riigi, funktsiooni tüübi ja väljalaske põhjal.


[!INCLUDE[footer-include](../includes/footer-banner.md)]