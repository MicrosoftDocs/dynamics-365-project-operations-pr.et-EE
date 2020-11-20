---
title: Hinnakirjade seadistamine
description: Selles teemas kirjeldatakse, kuidas seadistada kulude ja müügi hinnakirju.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 578f5641659a5d05785781afe7055fe4449cf799
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087886"
---
# <a name="set-up-price-lists"></a>Hinnakirjade seadistamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operationsi hinnakirjad esindavad hinnakatalooge. Hinnad väljendavad kulu-, müügi- ja arveldusmäärasid. Sõltuvalt sellest, kas hinnakiri väljendab kulumäära või müügi- ja arveldusmäära, on hinnakirja sisuks kas **Müük** või **Kulu**.

Järgmised laiendused on omased Project Operationsile ja neid rakendatakse Dynamics 365 Salesi hinnakirjadele.

- **Kontekst** : sellel väljal on toetatud väärtused **Kulu** ja **Müük**. Väärtust **Ost** ei toetata. Määrake kontekst väärtusele **Kulu** , et teha kulu hinnakirja või määrake müügi hinnakirja jaoks kontekst väärtusele **Müük**. Omahinnakirjad lahendavad prognoosi ja tegeliku kirje hinna. Müügi hinnakirjad lahendavad arveldamata ja arveldatud müügi tüüpide prognoositavate ja tegelike kirjete hinna.
- **Ajaühik** : see on vaikimisi ajaüksus, mille jaoks on hind selle hinnakirja tabelis **Rolli hind** seadistatud.
- **Hinnakiri olem** : see peidetud väli on Project Operationsis, et eristada hinnakirju, mis on hinnapakkumise- või lepingupõhised nendest, mis on standardsed ja globaalselt rakendatavad.

## <a name="price-list-header"></a>Hinnakirja päis

Järgmises tabelis on toodud need väljad hinnakirja vahekaardil **Üldine** , mis on ainulaadsed Project Operationsi jaoks või mille käitumine on võrreldes Salesi hinnakirjadega oluliselt muudetud.

| Väli | Asukoht | Asjakohasus, eesmärk ja juhised | Allavoolu mõjud |
| --- | --- | --- | --- |
| Nimetus | Vahekaart **Üldine** ja vormid **Kiirloomine** | Hinnakirja identiteet. | Hinnakirjal kuvatakse seda väärtust kõigil loendilehekülgedel ja rippmenüüvalikutel.|
| Kontekst | Vahekaart **Üldine** ja vormid **Kiirloomine** | Selle välja väärtuseks saab seada **Kulu** või **Müük**. | Hinnakirja, mis on seatud olekusse **Kulu** , kasutatakse kulude prognooside ja tegelike kulude hinna otsimiseks. Hinnakirja, mis on seatud olekusse **Müük** , kasutatakse müügi prognooside ja tegeliku müügi otsimiseks. Klientide hinnakirjadele, projekti hinnapakkumistele ja projekti lepingutele saab lisada ainult hinnakirju, mille kontekstiks on seadistatud **Müük**. |
| Alguskuupäev | Vahekaart **Üldine** ja vormid **Kiirloomine** | Hinnakirja kehtivuse alguskuupäev. | Koos väljaga **Lõppkuupäev** kasutatakse seda välja, määramaks, milline hinnakiri on teatud prognoosile või tegelikule reale kohaldatav. |
| Lõppkuupäev | Vahekaart **Üldine** ja vormid **Kiirloomine** | Hinnakirja kehtivuse lõppkuupäev. | Koos väljaga **Alguskuupäev** kasutatakse seda välja, määramaks, milline hinnakiri on teatud prognoosile või tegelikule reale kohaldatav. |
| Valuuta | Vahekaart **Üldine** ja vormid **Kiirloomine** | Seda välja kasutatakse selle hinnakirjaga seotud iga rolli, kategooria või hinnakirja üksuse rea valuuta vaikeväärtusena. | **Müügi** hinnakirjades ei saa rolle, kategooriaid ega hinnakirja üksuse ridu luua üheski teises valuutas peale selle valuuta. **Kulu** hinnakirjades saate luua rolli hinna rea mistahes valuutas. Siin määratletud valuutat kasutatakse vaikimisi. Kasutaja rolli hindadega seotud seadistus võib selle väärtuse alistada, et lubada tööjõu kulumäära seadistamise mistahes valuutas. Kategooria kulumäärasid ja hinnakirjaüksuse kulusid saab seadistada ainult siin määratletud valuutas. |
| Ajaühik | Vahekaart **Üldine** ja vormid **Kiirloomine** | Seda välja kasutatakse selle hinnakirjaga seotud iga rolli rea ajaühiku vaikeväärtuse saamiseks. | Seda välja väärtust kasutatakse ainult seotud rolli hinna seadistamisel. Hinnakirjades **Kulu** ja **Müük** saate luua rolli hinna rea mistahes ajaühikus. Siin määratletud ajaühikut kasutatakse vaikimisi. Kasutaja rolli hindadega seotud seadistus võib selle väärtuse alistada, et lubada tööjõu kulu ja arveldusmäära seadistamise mistahes ajaühikus. |
| Kirjeldus | Vahekaart **Üldine** ja vormid **Kiirloomine** | See tekstiväli võimaldab teil anda hinnakirja mitmerealise kirjelduse. | See väli kuvatakse hinnakirja vaates **Seostatud** erinevates üksustes, millel on seotud hinnakirjad. |