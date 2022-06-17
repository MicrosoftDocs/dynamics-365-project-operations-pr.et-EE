---
title: Kande päritolu – tegelike seoste linkimine nende allikaga
description: Selles artiklis selgitatakse, kuidas kande päritolu mõistet kasutatakse tegelike seoste sidumiseks algsete lähtekirjetega (nt ajasisestus, kulukanne või materjali kasutuslogid).
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921297"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Kande päritolu – tegelike seoste linkimine nende allikaga

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Kande päritolukirjed luuakse, et linkida tegelikud andmed nende allikaga, näiteks ajakannete, kulukannete, materjali kasutuslogide ja projektiarvetega.

Järgmises näites on toodud ajakannete tüüpiline töötlemine Project Operationsi projekti töötsüklis.

> ![Töötlemisaeg tervikuna Project Operationsis.](media/basic-guide-17.png)
 
1. Ajakande esitamisel luuakse kaks žurnaalirida: üks kulu ja teine sisestamata müügi jaoks.
2. Ajakande lõplik kinnitamine põhjustab kahe tegeliku loomise: üks kulu ja teine sisestamata müügi jaoks.
3. Kui kasutaja loob projekti arve, luuakse arverea tehing, kasutades arveldamata müügi tegelikke andmeid.
4. Pärast arve kinnitamist luuakse kaks uut tegelikku versiooni: arveldamata müügi tühistamine ja arveldatud müügi tegelik.

Iga selle töötlemistöövoo sündmus käivitab olemis Transaction origin kirjete loomise, et aidata luua jälgi nende kirjete vahelistest seostest, mis on loodud ajakande, žurnaalirea, tegelike ja arverea üksikasjade vahel.

Järgmises tabelis on kuvatud eelmise töövoo tehingute päritolu olemi kirjed.

| Sündmus                        | Päritolu                   | Päritolu tüüp                       | Tehing                       | Tehingu tüüp         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Edasta ajakirje        | Ajakirje kirje GUID   | Ajakirje                        | Töölehe rea kirje GUID (kulu)   | Töölehe rida             |
| Ajakirje kirje GUID       | Ajakirje               | Töölehe rea kirje GUID (müük)  | Töölehe rida                      |                          |
| Kinnitatud aeg                | Töölehe rea kirje GUID (kulu) | Töölehe rida                      | Arveldamata müügi kirje GUID        | Tegelik                   |
| Ajakirje kirje GUID       | Ajakirje               | Arveldamata müügi kirje GUID        | Tegelik                            |                          |
| Töölehe rea kirje GUID (kulu)     | Töölehe rida             | Tegelike kulude kirje GUID           | Tegelik                            |                          |
| Ajakirje kirje GUID       | Ajakirje               | Tegelike kulude kirje GUID           | Tegelik                            |                          |
| Arve loomine             | Ajakirje kirje GUID   | Ajakirje                        | Arve rea tehingu GUID     | Arve rea tehing |
| Töölehe rea kirje GUID (kulu)     | Töölehe rida             | Arve rea tehingu GUID     | Arve rea tehing          |                          |
| Arve kinnitamine         | Arve rea GUID        | Arve rida                      | Arveldatud müügi kirje GUID          | Tegelik                   |
| Arve GUID                 | Arve                  | Arveldatud müügi kirje GUID          | Tegelik                            |                          |
| Arve rea üksikasjade GUID     | Arve rea üksikasjad      | Arveldatud müügi kirje GUID          | Tegelik                            |                          |
| Ajakirje kirje GUID       | Ajakirje               | Arveldatud müügi kirje GUID          | Tegelik                            |                          |
| Töölehe rea kirje GUID (kulu)     | Töölehe rida             | Arveldatud müügi kirje GUID          | Tegelik                            |                          |
| Ajakirje kirje GUID       | Ajakirje               | Arveldamata müügi tagasipöörde GUID      | Tegelik                            |                          |
| Töölehe rea kirje GUID (kulu)     | Töölehe rida             | Arveldamata müügi tagasipöörde GUID      | Tegelik                            |                          |
| Arve paranduse mustand     | Vana arve rea üksikasja GUID             | Arve rea tehing          | Paranduse arve rea üksikasja GUID               | Arve rea tehing |
| Vana arve rea GUID                  | Arve rida             | Paranduse arve rea üksikasja GUID               | Arve rea tehing          |                          |
| Vana arve GUID             | Arve                  | Paranduse arve rea üksikasja GUID               | Arve rea tehing          |                          |
| Ajakirje kirje GUID       | Ajakirje               | Paranduse arve rea üksikasja GUID               | Arve rea tehing          |                          |
| Töölehe rea kirje GUID (kulu)     | Töölehe rida             | Paranduse arve rea üksikasja GUID               | Arve rea tehing          |                          |
| Kinnitatud arve parandus | Vana arve rea üksikasja GUID             | Arve rea tehing          | Tagasipööratud arveldatud müügi tegelik GUID | Tegelik                   |
| Vana arve rea GUID                  | Arve rida             | Tagasipööratud arveldatud müügi tegelik GUID | Tegelik                            |                          |
| Vana arve GUID             | Arve                  | Tagasipööratud arveldatud müügi tegelik GUID | Tegelik                            |                          |
| Ajakirje kirje GUID       | Ajakirje               | Tagasipööratud arveldatud müügi tegelik GUID | Tegelik                            |                          |
| Töölehe rea kirje GUID (kulu)     | Töölehe rida             | Tagasipööratud arveldatud müügi tegelik GUID | Tegelik                            |                          |
| Vana arve rea üksikasja GUID                 | Arve rea tehing | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |
| Vana arve rea GUID                  | Arve rida             | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |
| Vana arve GUID             | Arve                  | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |
| Ajakirje kirje GUID       | Ajakirje               | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |
| Töölehe rea kirje GUID (kulu)     | Töölehe rida             | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |
| Paranduse arve rea üksikasja GUID          | Arve rea tehing | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |
| Paranduse arve rea GUID           | Arve rida             | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |
| Parandatud arve GUID      | Arve                  | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |


Järgmisel joonisel on näidatud lingid, mis luuakse tegelike ja nende allikate vahel erinevatel sündmustel, kasutades projektitoimingute ajakirjete näidet.

> ![Kuidas on tegelikud andmed projektitoimingutes lähtekirjetega lingitud?](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
