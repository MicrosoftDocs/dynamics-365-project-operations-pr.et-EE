---
title: Hinnakujunduse ja kuluarvestuse dimensioonide avaleht
description: Selles teemas antakse ülevaade hindade dimensioonidest.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750946"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Hinnakujunduse ja kuluarvestuse dimensioonide avaleht

Dimensioonid, mida kasutatakse inimressurssides hinnakujunduse ja kulude seadistamiseks, kuuluvad kahte kategooriasse.

- Inimesed
- Plaanitud töö

Seetõttu on olemas kahte tüüpi hinnakujunduse dimensiooniväärtusi, mis on saadaval rakenduses Project Service Automation (PSA). 

- **Suvandikomplektid** – dimensioonid, mis on väärtuste kogumi jaoks fikseeritud loendites.
- **Olemil põhinevad väärtused** – dimensioonid, mis võivad olla vaheldusrikkad väärtuste kogumid.

## <a name="pricing-dimensions"></a>Hinnadimensioonid

PSA tarnitakse vaikimisi seatud hinnakujunduse dimensioonidega. Neid saate vaadata, kui avate **Project Service** > **Parameetrid**. Veenduge, et parameetri kirjel on vahekaardil **Summal põhinevad hinnakujunduse dimensioonid**, et selle rollide **msdyn_resourcecategory** ja ressursi organisatsiooniüksus **msdyn_organizationalunit** väljad **Kehtib müügi kohta** ja **Kehtib kulu kohta** oleks seatud väärtusele **Jah**. See võimaldab teil seadistada iga rolli ja organisatsiooniüksuse kombinatsiooni hinna ja maksumuse.

![Esiletõstetud projektiteenuse parameetrite kuvatõmmis, millel on esile tõstetud „Kehtib müügi kohta”](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Kui olete kasutanud valmiskujul rolli välju ja organisatsiooniüksust hinnakujunduse mõõtmetena enne PSA versiooni 3, ei ole mingeid jälgitavaid muudatusi. Saate jätkuvalt kasutada Project Service nagu tavaliselt. 

Kui teil on vaja ressursside hinda või kulu, kasutades täiendavaid atribuute, saate luua kohandatud välju, olemeid ja dimensioone. Lisateavet leiate järgmistest teemadest, kuid pange tähele, et protseduurid tuleb lõpule viia allpool toodud järjekorras.

- [Kohandatud väljade ja olemite loomine](create-custom-fields-entities.md)
- [Kohandatud väljade lisamine hinna seadistusele ja ülekande olemitele](field-references.md)
- [Kohandatud väljade seadistamine hinnakujunduse dimensioonidena](set-up-pricing-dimensions.md)
- [Lisandmooduli atribuutide värskendamine uute hinnakujunduse dimensioonide lisamiseks](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Inimressursside aja hinnakujundus
Organisatsiooni hindade arvestamine inimressursside aja järgi on sageli oluline strateegiline kaalutlus, mis mõjutab otseselt organisatsiooni tasuvust. Kui teie organisatsioon on valmis tuvastama, kuidas ta soovib arve ja kulumäära inimressursside aja järgi seadistada, saate tööd rahastada meeskondade ja tavadega.

Muud kaalutlused hinna osas hõlmavad seda, kas uuesti kasutada välju või olemeid, mis pole praegu hinnakujunduse dimensioonid, kuid mida kohaldatakse teie organisatsiooni hinnakujunduse dimensioonina. Väljad, nagu **Tehingu kategooria** (**msdyn_transactioncategory**) ja **broneeritav ressurss**(**bookableresource**), on näited kandidaadi dimensioonidest. 

Samuti peaksite kaaluma, kas teie hinnakujunduse dimensioon peaks olema tabel või suvandikomplekt. Kui teil on ette nähtud sellise dimensiooni väärtuste muudatused, mis ületavad 10 või 12 ja vajate nende väärtuste jaoks lisaatribuute, võite luua suvandikomplekti asemel olemi. Suvandikomplekti haldamine, näiteks väärtuste lisamine või eemaldamine, nõuab administraatorilt või arendajalt, et enamikul kasutajatel oleks võimalik tabelisse uusi ridu lisada.

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
