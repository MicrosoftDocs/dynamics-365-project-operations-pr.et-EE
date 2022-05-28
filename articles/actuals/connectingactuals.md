---
title: Kandeühendused – erinevate kandetüüpide tegelike linkide linkimine
description: Selles teemas selgitatakse, kuidas tehinguühendust kasutatakse erinevat tüüpi tegelike seoste linkimiseks, et aidata jälgida kasumlikkust, arvelduse mahajäämust ja arveldatud versus sisestamata tuluarvutusi.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580773"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Kandeühendused – erinevate kandetüüpide tegelike linkide linkimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Tehinguühenduse kirjed luuakse selleks, et linkida eri tüüpi aktuaalsused, kuna aja-, kulu- või materjalikasutuse kasutamine liigub oma elutsükli elutsüklis hinnapakkumisest või müügieelsest etapist lepinguetappi, kinnituste ja/või tagasikutsumisteni, arvete esitamiseni ning potentsiaalselt krediidi- või parandusarvete esitamiseni.

Järgmises näites on toodud ajakannete tüüpiline töötlemine Project Operationsi projekti töötsüklis.

> ![Ajakannete töötlemine Project Operationsis.](media/basic-guide-17.png)

Projektitoimingute projekti elutsükli ajakirjete töötlemine on järgmine. 

1. Ajakande esitamisel luuakse kaks žurnaalirida: üks kulu ja teine sisestamata müügi jaoks. 
2. Ajakande lõplik kinnitamine põhjustab kahe tegeliku loomise: üks kulu ja teine sisestamata müügi jaoks. Need 2 tegelikkust on lingitud tehinguühenduste abil.
3. Kui kasutaja loob projekti arve, luuakse arverea tehing, kasutades arveldamata müügi tegelikke andmeid.
4. Kui arve kinnitatakse, loob see kaks uut tegelikkust: sisestamata müügi tühistamine ja arveldamata müük tegelik. Sisestamata müügi tühistamine ja tegelik algne sisestamata müük on ühendatud tagurdamiskandeühenduste abil. Arveldatud müük ja algsed sisestamata müügi tegelikud tegelikud andmed on samuti seotud, et näidata seoseid selle vahel, mis oli kunagi mahajäämus või pooleliolev töö (WIP) tulu, mis on nüüd arveldatud tulu.   

Iga töötlemistöövoo sündmus käivitab kirjete **loomise tabelis Kande ühendus**. See aitab luua jälje ajakande, žurnaalirea, tegelike ja arverea üksikasjade vahel loodud kirjete vahelistest seostest.

Järgmises **tabelis kuvatakse eelmise töövoo olemi Transaction connection** kirjed.

|Sündmus                   |Tehing 1                 |Tehingu 1 roll |Tehingu 1 tüüp       |Kanne 2          |Tehingu 2 roll |Tehingu 2 tüüp |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Edasta ajakirje   |Töölehe rea (müük) GUID     |Arveldamata müük |msdyn_journalline            |Töölehe rea (kulu) GUID     |Kulu            |msdyn_journalline  |
|Kinnitatud aeg           |Arveldamata tegelik (müük) GUID  |Arveldamata müük |msdyn_actual                 |Tegelike kulu (kulu) GUID       |Kulu            |msdyn_actual       |
|Arve loomine        |Arve rea üksikasjade GUID      |Arveldatud müük   |msdyn_invoicelinetransaction |Arveldamata müügi tegelik GUID   |Arveldamata müük  |msdyn_actual       |
|Arve kinnitamine    |Tegeliku GUID tagasipööramine         |Tagasipööramine      |msdyn_actual                 |Originaalne arveldamata müügi GUID |Algne        |msdyn_actual       |
|                        |Arveldatud müügi GUID             |Arveldatud müük   |msdyn_actual                 |Arveldamata müügi tegelik GUID   |Arveldamata müük  |msdyn_actual       |
|Arve paranduse mustand |Arve rea tehingu GUID|Asendamine      |msdyn_invoicelinetransaction |Arveldatud müügi GUID            |Algne        |msdyn_actual       |
|Arve parandamise kinnitamine|Arveldatud müügi tagasipööramise GUID  |Tagasipööramine      |msdyn_actual                 |Arveldatud müügi GUID            |Algne        |msdyn_actual       |
|                        |Uus sisestamata müügi GUID |Asendamine            |msdyn_actual                 |Arveldatud müügi GUID            |Algne        |msdyn_actual       |


Järgmisel joonisel on näidatud lingid, mis luuakse eri tüüpi tegelike vahel erinevatel sündmustel, kasutades projektitoimingute ajakirjete näidet.

> ![Kuidas eri tüüpi tegelikud andmed projektitoimingutes üksteisega lingitakse?](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
