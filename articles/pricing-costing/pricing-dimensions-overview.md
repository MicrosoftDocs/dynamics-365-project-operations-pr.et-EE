---
title: Hinnakujunduse dimensioonide ülevaade
description: See teema sisaldab teavet hinnakujunduse dimensioonide kohta rakenduses Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 33f55976eafedd046fba952ab6381c297ab4e271
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650182"
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

Rakenduses Dynamics 365 Project Operations tarnitakse vaikimisi seatud hinnakujunduse dimensioonidega. Neid hinnakujunduse dimensioone saate vaadata, kui avate **Project Operations** > **Parameetrid**. Veenduge, et parameetri kirjel on vahekaardil **Summal põhinevad hinnakujunduse dimensioonid**, et selle rollide **msdyn_resourcecategory** ja ressursi organisatsiooniüksus **msdyn_organizationalunit** väljad **Kehtib müügi kohta** ja **Kehtib kulu kohta** oleks seatud väärtusele **Jah**. Kui need väljad on lubatud, saate seadistada iga rolli ja organisatsiooniüksuse kombinatsiooni hinna ja maksumuse.

![Esiletõstetud projektiteenuse parameetrite kuvatõmmis, millel on esile tõstetud „Kehtib müügi kohta”](media/PS-OOB-parameters.png)

Kui teil on vaja ressursside hinda või kulu, kasutades täiendavaid atribuute, saate luua kohandatud välju, olemeid ja dimensioone. Lisateabe saamiseks vaadake järgmisi teemasid. 
  
  > [!NOTE]
  > Toimingud tuleb teha loendamise järjekorras.

1. [Lahenduse loomine kohandatud hinnakujunduse dimensioonide jaoks](../sales/create-solution-custompd.md)
2. [Kohandatud väljade ja olemite loomine](create-custom-fields-entities-pricing-dimensions.md)
3. [Kohandatud väljade lisamine hinna seadistusele ja ülekande olemitele ](add-custom-fields-price-setup-transactional-entities.md)
4. [Kohandatud väljade seadistamine hinnakujunduse dimensioonidena ](set-up-custom-fields-pricing-dimensions.md)
5. [Lisandmooduli atribuutide värskendamine uute hinnakujunduse dimensioonide lisamiseks](update-plugin-attributes-pd.md)


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


[!INCLUDE[footer-include](../includes/footer-banner.md)]