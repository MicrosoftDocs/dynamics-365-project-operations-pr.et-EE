---
title: Hinnakujunduse ja kuluarvestuse dimensioonide avaleht
description: Selles teemas antakse ülevaade hindade dimensioonidest.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d17939777a6670bafc41b372adc922f8bdcc0411f3fdb399e7c9ab01eca87dd0
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998456"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Hinnakujunduse ja kuluarvestuse dimensioonide avaleht

[!include [banner](../includes/psa-now-project-operations.md)]

Projektipõhiseöt tegutsevates organisatsioonides tööjõu hinna ja kulude määramiseks kasutatavaid dimensioone mõjutavad järgmised atribuudid:

- Inimesed, kes teevad vastavalt nende kogemusele, rollile või geograafilisele asukohale tööd sarnaselt
- Töö, mis tuleb teha vastavalt selle keerulisusele ja ajale sarnaselt

Arvestades nende töö tüüpilisi atribuute ja töö tegemiseks vajalikke inimesi, on rakenduses Project Service Automation saadaval järgmised kaks hinnakujunduse dimensiooni väärtuse tüüpi. 

- **Suvandikomplektid** – atribuudid, mis on väärtuste kogumi jaoks fikseeritud loendites.
- **Olemil põhinevad väärtused** – atribuudid, mis võivad omada vaheldusrikkaid väärtuste kogumeid, mis on lõplikud, kuid võivad aja jooksul muutuda.

## <a name="pricing-dimensions"></a>Hinnakujunduse dimensioonid

PSA tarnitakse vaikimisi seatud hinnakujunduse dimensioonidega. Neid saate vaadata, kui avate **Project Service** > **Parameetrid**. Veenduge, et parameetri kirjel on vahekaardil **Summal põhinevad hinnakujunduse dimensioonid**, et selle rollide **msdyn_resourcecategory** ja ressursi organisatsiooniüksus **msdyn_organizationalunit** väljad **Kehtib müügi kohta** ja **Kehtib kulu kohta** oleks seatud väärtusele **Jah**. See võimaldab teil seadistada iga rolli ja organisatsiooniüksuse kombinatsiooni hinna ja maksumuse.

![Project Service’i parameetrite kuvatõmmis, millel on esile tõstetud „Kehtib müügi kohta”.](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Kui olete kasutanud valmiskujul rolli välju ja organisatsiooniüksust hinnakujunduse mõõtmetena enne PSA versiooni 3, ei ole mingeid jälgitavaid muudatusi. Saate jätkuvalt kasutada Project Service nagu tavaliselt. 

Kui teil on vaja ressursside hinda või kulu, kasutades täiendavaid atribuute, saate luua kohandatud välju, olemeid ja dimensioone. Lisateavet leiate järgmistest teemadest, kuid pange tähele, et protseduurid tuleb lõpule viia allpool toodud järjekorras.

- [Kohandatud väljade ja olemite loomine](create-custom-fields-entities.md)
- [Kohandatud väljade lisamine hinna seadistusele ja ülekande olemitele](field-references.md)
- [Kohandatud väljade seadistamine hinnakujunduse dimensioonidena ](set-up-pricing-dimensions.md)
- [Lisandmooduli atribuutide värskendamine uute hinnakujunduse dimensioonide lisamiseks](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Inimressursside aja hinnakujundus
Organisatsiooni hindade arvestamine inimressursside aja järgi on sageli oluline strateegiline kaalutlus, mis mõjutab otseselt organisatsiooni tasuvust. Kui teie organisatsioon on valmis tuvastama, kuidas ta soovib arve ja kulumäära inimressursside aja järgi seadistada, saate tööd rahastada meeskondade ja tavadega.

Muud kaalutlused hinna osas hõlmavad seda, kas uuesti kasutada välju või olemeid, mis pole praegu hinnakujunduse dimensioonid, kuid mida kohaldatakse teie organisatsiooni hinnakujunduse dimensioonina. Väljad, nagu **Tehingu kategooria** (**msdyn_transactioncategory**) ja **broneeritav ressurss**(**bookableresource**), on näited kandidaadi dimensioonidest. 

Kaaluge, kas teie hinnakujunduse dimensioon peaks olema tabel või suvandikomplekt. Kui teil on ette nähtud sellise dimensiooni väärtuste muudatused, mis ületavad 10 või 12 ja vajate nende väärtuste jaoks lisaatribuute, looge suvandikomplekti asemel olem. Suvandikomplekti haldamine, näiteks väärtuste lisamine või eemaldamine, nõuab administraatorilt või arendajalt, et enamikul ärikasutajatel oleks võimalik tabelisse uusi ridu lisada.

Järgmises näites on toodud arve määrad, mis on seadistatud vastavalt rollile ja selle ressursside eralduse organisatsiooni üksusele, kuhu ressurss kuulub. Kulumäära aluseks on tavaliselt töötaja ja organisatsiooni ühik, kuhu nad kuuluvad. Selles näites näevad arve intressimäära ja kulumäära tabelid välja nagu järgmised.

**Näidishinnad**

| Roll        | Organisatsiooniüksus    |Üksus      |Hind      |Valuuta  |
| ------------|-------------|----------|----------:|----------|
| Arendaja   | Contoso US  |tund | 200|USD     |
| Arendaja   | Contoso India |tund|   112|USD     |


**Kulumäära näidis**

| Palgavahemik     | Organisatsiooniüksus    |Üksus      |Hind      |Valuuta  |
| ----------------|-------------|----------|----------:|----------|
| Minu company_Band1 | Contoso US  |tund | 145|USD     |
| Minu company_Band2 | Contoso India |tund|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]