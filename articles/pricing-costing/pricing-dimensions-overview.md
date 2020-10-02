---
title: Hinnakujunduse dimensioonide ülevaade
description: Selles teemas antakse teavet Dynamics 365 Project Operationsi hinnakujunduse dimensioonide kohta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898211"
---
# <a name="pricing-dimensions-overview"></a>Hinnakujunduse dimensioonide ülevaade

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dimensioonid, mida kasutatakse inimressurssides hinnakujunduse ja kulude seadistamiseks, kuuluvad kahte kategooriasse.

- Inimesed
- Plaanitud töö

Seetõttu on olemas kahte tüüpi hinnakujunduse dimensiooniväärtusi.

- **Suvandikomplektid**: dimensioonid, mis on väärtuste kogumi jaoks fikseeritud loendites.
- **Olemil põhinevad väärtused**: dimensioonid, mis võivad olla vaheldusrikkad väärtuste kogumid.

## <a name="pricing-dimensions"></a>Hinnakujunduse dimensioonid

Dynamics 365 Project Operations tuleb vaikimisi seatud hinnakujunduse dimensioonidega. Neid hinnakujunduse dimensioone saate vaadata, kui avate **Project Operations** > **Parameetrid**. Veenduge, et parameetri kirjel on vahekaardil **Summal põhinevad hinnakujunduse dimensioonid**, et selle rollide **msdyn_resourcecategory** ja ressursi organisatsiooniüksus **msdyn_organizationalunit** väljad **Kehtib müügi kohta** ja **Kehtib kulu kohta** oleks seatud väärtusele **Jah**. Kui need väljad on lubatud, saate seadistada iga rolli ja organisatsiooniüksuse kombinatsiooni hinna ja maksumuse.

Kui teil on vaja ressursside hinda või kulu, kasutades täiendavaid atribuute, saate luua kohandatud välju, olemeid ja dimensioone.

## <a name="pricing-human-resource-time"></a>Inimressursside aja hinnakujundus
Organisatsiooni hindade arvestamine inimressursside aja järgi on sageli oluline strateegiline kaalutlus, mis mõjutab otseselt organisatsiooni tasuvust. Kui teie organisatsioon on valmis tuvastama, kuidas ta soovib arve ja kulumäära inimressursside aja järgi seadistada, saate tööd rahastada meeskondade ja tavadega.

Muud kaalutlused hinna osas hõlmavad seda, kas uuesti kasutada välju või olemeid, mis pole praegu hinnakujunduse dimensioonid, kuid mida kohaldatakse teie organisatsiooni hinnakujunduse dimensioonina. Väljad, nagu **Tehingu kategooria** (**msdyn_transactioncategory**) ja **broneeritav ressurss**(**bookableresource**), on näited kandidaadi dimensioonidest. 

Kaaluge, kas teie hinnakujunduse dimensioon peaks olema tabel või suvandikomplekt. Kui teil on ette nähtud sellise dimensiooni väärtuste muudatused, mis ületavad 10 või 12 ja vajate nende väärtuste jaoks lisaatribuute, võite luua suvandikomplekti asemel olemi. Suvandikomplekti haldamine, näiteks väärtuste lisamine või eemaldamine, nõuab administraatorilt või arendajalt, et enamikul kasutajatel oleks võimalik tabelisse uusi ridu lisada.

Järgmises näites on toodud arve määrad, mis on seadistatud vastavalt rollile ja selle ressursside eralduse organisatsiooni üksusele, kuhu ressurss kuulub. Kulumäära aluseks on tavaliselt töötaja ja organisatsiooni ühik, kuhu nad kuuluvad. Selles näites näevad arve intressimäära ja kulumäära tabelid välja nagu järgmised.

**Näidishinnad**

| Roll        | Organisatsiooniüksus    |Ühik      |Hind      |Valuuta  |
| ------------|-------------|----------|----------:|----------|
| Arendaja   | Jõgi US  |Hour | 200|USD     |
| Arendaja   | Jõgi India |Hour|   112|USD     |


**Kulumäära näidis**

| Palgavahemik     | Organisatsiooniüksus    |Ühik      |Hind      |Valuuta  |
| ----------------|-------------|----------|----------:|----------|
| Minu company_Band1 | Jõgi US  |Hour | 145|USD     |
| Minu company_Band2 | Jõgi India |Hour|   67|USD     |
