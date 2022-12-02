---
title: Kannete ühendused – erinevate kandetüüpide tegelike andmete linkimine
description: See artikkel selgitab, kuidas kasutatakse tehinguühendust eri tüüpi tegelike näitajate linkimiseks, et aidata jälgida kasumlikkust, tööjärjearveid ja arveldatud ja arveldamata tulude arvutamist.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926081"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Kannete ühendused – erinevate kandetüüpide tegelike andmete linkimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Tehinguühenduse kirjed luuakse eri tüüpi tegelike näitajate linkimiseks, kui aeg, kulu või materjalikasutus liigub oma elutsüklis pakkumisest või müügieelsest etapist lepingufaasi, kinnitamise ja/või tagasikutsumise, arvete esitamise ja potentsiaalselt krediidi- või parandusarvete esitamise etapini.

Järgmises näites on toodud ajakannete tüüpiline töötlemine Project Operationsi projekti töötsüklis.

> ![Aja sissekannete töötlemine rakenduses Project Operations.](media/basic-guide-17.png)

Aja sissekannete töötlemine Project Operationsi projekti elutsüklis toimub järgmiselt: 

1. Ajakirje esitamise põhjuseks on kahele töölehele kandmise loomine: üks kulu ja teine arveldamata müügi jaoks. 
2. Ajakirje lõplik kinnitamine põhjustab kahe tegeliku näitaja loomise: ühe kulu ja teise arveldamata müügi kohta. Need 2 tegelikku näitajad on seotud tehinguühenduste abil.
3. Kui kasutaja loob projekti arve, luuakse arverea tehing, kasutades arveldamata müügi tegelikke andmeid.
4. Kui arve kinnitatakse, loob see kaks uut tegelikku näitajat: arveldamata müügi tühistamine ja arveldatud müügi tegelik näitaja. Arveldamata müügi tühistamine ja esialgse arveldamata müügi tegelik näitaja ühendatakse omavahel, kasutades pöördtehingute ühendusi. Arveldatud müügid ja esialgse arveldamata müügi tegelikud näitajad on samuti ühendatud, et näidata seoseid selle vahel, mis oli kunagi tööjärje või poolelioleva töö (WIP) tulu ja mis on nüüd arveldatud tulu.   

Iga töötlemise töövoo sündmus käivitab kirjete loomise tabelis **Tehingu ühendus**. See aitab luua jälgi aja sissekande, töölehele kandmise rea, tegeliku näitaja ja arve rea üksikasjade vahel loodud kirjete vahelistest seostest.

Järgmises tabelis on kuvatud eelmise töövoo **Tehingute seose** olemi kirjed.

|Sündmus                   |Tehing 1                 |Tehingu 1 roll |Tehingu 1 tüüp       |Kanne 2          |Tehingu 2 roll |Tehingu 2 tüüp |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Edasta ajakirje   |Töölehe rea (müük) GUID     |Arveldamata müük |msdyn_journalline            |Töölehe rea (kulu) GUID     |Kulu            |msdyn_journalline  |
|Kinnitatud aeg           |Arveldamata tegelik (müük) GUID  |Arveldamata müük |msdyn_actual                 |Tegelike kulu (kulu) GUID       |Kulu            |msdyn_actual       |
|Arve loomine        |Arve rea üksikasjade GUID      |Arveldatud müük   |msdyn_invoicelinetransaction |Arveldamata müügi tegelik GUID   |Arveldamata müük  |msdyn_actual       |
|Arve kinnitamine    |Tegeliku GUID tagasipööramine         |Tagasipööramine      |msdyn_actual                 |Originaalne arveldamata müügi GUID |Algne        |msdyn_actual       |
|                        |Arveldatud müügi GUID             |Arveldatud müük   |msdyn_actual                 |Arveldamata müügi tegelik GUID   |Arveldamata müük  |msdyn_actual       |
|Arve paranduse mustand |Arve rea tehingu GUID|Asendamine      |msdyn_invoicelinetransaction |Arveldatud müügi GUID            |Algne        |msdyn_actual       |
|Arve parandamise kinnitamine|Arveldatud müügi tagasipööramise GUID  |Tagasipööramine      |msdyn_actual                 |Arveldatud müügi GUID            |Algne        |msdyn_actual       |
|                        |Uue arveldamata müügi GUID |Asendamine            |msdyn_actual                 |Arveldatud müügi GUID            |Algne        |msdyn_actual       |


Järgmine joonis näitab linke, mis luuakse erinevate sündmuste eri tüüpi tegelike näitajate vahel, kasutades aja sissekannete näidet rakenduses Project Operations.

> ![Kuidas eri tüüpi tegelikud näitajad on rakenduses Project Operations omavahel seotud.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
