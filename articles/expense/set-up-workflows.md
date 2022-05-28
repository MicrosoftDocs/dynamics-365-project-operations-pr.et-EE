---
title: Töövoogude seadistamine kuluhalduseks
description: Saate seadistada töövoo protsessi, mida kasutatakse reisi-ja kuludokumentide ülevaatamiseks ja kinnitamiseks.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: da015904aebfb4cfe046407bbf7bc7fe5a0a0faa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581187"
---
# <a name="set-up-workflows-for-expense-management"></a>Töövoogude seadistamine kuluhalduseks

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Saate seadistada töövoo protsessi reisi-ja kuludokumentide ülevaatamiseks ja kinnitamiseks. Saate määratleda kuluaruannete, reisidetellimuste ja ettemaksetaotluste töövood.

Töövoog esindab äriprotsessi ja määratleb, kuidas dokument süsteemist läbi liigub. Töövoog näitab ka, kes peab tööülesande lõpetama või dokumendi kinnitama. Teie ettevõttes on töövoo süsteemi kasutamisel mitu eelist.

- **Järjepidevad protsessid**: saate määratleda konkreetsete dokumentide (nt ostutellimuste ja kuluaruannete) kinnitamise protsessi. Töövoogude süsteemi kasutamine aitab tagada, et dokumente töödeldakse ja kinnitatakse järjekindlalt ja tõhusalt.
- **Protsessi nähtavus**: saate jälgida kindla töövoo eksemplari olekut, ajalugu ja jõudluse mõõdikuid. See aitab teil kindlaks teha, kas töövoogu tuleb muuta tõhusamaks.
- **Tsentraliseeritud tööloend**: kasutajad saavad vaadata tsentraliseeritud tööloendit, et kuvada neile määratud töövoo tööülesandeid ja kinnitusi. 

## <a name="workflow-types"></a>Töövoo tüübid

Järgmises tabelis on loetletud töövoogude tüübid, mida saate **Kuluhalduses** luua.


|              <strong>Tüüp</strong>              |                   <strong>Kasutage seda tüüpi järgnevaks</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Kuluaruande automaatne kinnitamine</strong> |            Kuluaruannete jaoks kinnitamise töövoogude loomine.             |
|  <strong>Kuluaruande automaatne sisestamine</strong>   |        Kuluaruannete jaoks automaatse sisestamise töövoogude loomine.        |
|       <strong>Kulu reaüksus</strong>        |     Kuluaruannete reaüksuste jaoks kinnitamise töövoogude loomine.      |
| <strong>Kulu reaüksuse automaatne sisestamine</strong> | Kuluaruannete reaüksuste jaoks automaatse sisestamise töövoogude loomine. |
|       <strong>Reisitellimus</strong>       |          Reisitellimuste jaoks kinnitamise töövoogude loomine.           |
|      <strong>Ettemakse taotlus</strong>      |         Ettemakse taotluste jaoks kinnitamise töövoogude loomine.          |
|        <strong>Käibemaksu sissenõudmine</strong>        | Käibemaksu (VAT) sissenõudmise kinnitamise töövoogude loomine.  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]