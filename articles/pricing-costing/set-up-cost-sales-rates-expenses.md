---
title: Kulutuste kulumäärade ja müügihindade seadistamine
description: Selles teemas kirjeldatakse kulumäärade ja müügihindade seadistamist tehingute ja kulutuste kategooriates.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e5a2402a2c1059ff11dbe1a331a028da77958235
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074875"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Kulutuste kulumäärade ja müügihindade seadistamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operationsis saate tehingute kategooriate jaoks seadistada kulumäärad ja müügihinnad. Kuna kulumäärad ja müügihinnad on välja töötatud kulutuste jaoks, tuleb iga sellist kannet sisaldavat kategooriat ka kulukategooriana seadistada. See seadistus tagab allavoolu funktsionaalsuse täpsuse. Tehingute kategooriate kulumäärasid ja müügihindu saab loetleda ainult ühes valuutas, milleks peab olema hinnakirja päise valuuta.

Tehingukategooriate jaoks kulumäärade ja müügihindade seadistamiseks toimige järgmiselt. 

1. Looge hinnakirja päise põhjal hinnakiri. 
2. Valige jaotise **Kategooria hinnad** andmeruudustiku menüüst **+ Uus kategooria hind**. 
3. Sisestage lehel **Kiirloomine** tehingukategooria ja üksus, mille jaoks uue hinna loote.

Järgmises tabelis on kategooria hinna rea vahekaardi **Üldine** väljad ja paan **Kiirloomine** , mida peate müügi või omahinnakirjale kategooria hindade loomisel meeles pidama.

| Väli | Asukoht | Asjakohasus, eesmärk ja juhised | Allavoolu mõjud |
| --- | --- | --- | --- |
| Kande kategooria | Vahekaart **Üldine** ja lehed **Kiirloomine** | Valige tehingukategooria, mille jaoks müügi- või omahinda loote. | Kulutuse sissetuleva prognoosi või tegeliku näitaja tehingukategooria vastendatakse selle reaga tehingukategooria kulumäära või müügihinna vaikeväärtuse saamiseks. |
| Üksuse ajakava | Vahekaart **Üldine** ja lehed **Kiirloomine** | Üksuse ajakava vaikeväärtuseks on tehingukategooria üksuse ajakava. | Sellest väljast puudub allavoolu mõju. |
| Üksus | Vahekaart **Üldine** ja lehed **Kiirloomine** | Valige üksus, mille jaoks hindu seadistatakse. | Sissetuleva prognoosi või tegelike näitajate üksus vastendatakse selle rea üksusega, et saada kuluprognoosi või tegeliku näitaja vaikehind. |
| Hinnakujundusmeetod | Vahekaart **Üldine** ja lehed **Kiirloomine** | Välja **Hinnakujundusmeetod** võimalikud väärtused on **Ühiku hind** , **Omahind** ja **Juurdehindlus üle omahinna**. | Valides hinna seadistamise aja **Ühiku hinna** , siis kategooria hinna rea väli **Protsent** lukustub. Kui valitud on **Ühiku hind** , lukustatakse müügi hinnakirja väljad **Hind** ja **Protsent**. Väärtuse **Juurdehindlus üle omahinna** lukustab müügi hinnakirja välja **Hind**. Kulu sissetuleval tegeliku näitaja real viib hinnakujundusmeetod **Omahind** või **Juurdehindlus üle omahinna** vastavale arveldamata müügi reale sellise hinna määramiseni, mis on võrdne kulu tegeliku näitajaga või mida arvestatakse juurdehindlusena üle omahinna. |
| Hind | Vahekaart **Üldine** ja lehed **Kiirloomine** | Ühiku hinna seadistamine tehingukategooria ja ühiku kombinatsioonile. Näiteks on läbisõidu määr 10 USD miili kohta ja 8 USD kilomeetri kohta. | Läbisõidu määr on määr, mille vaikeväärtuseks on sissetuleva prognoosi või kulu tehinguklassi tegeliku näitaja rea ühiku hind või kulu.|
| Protsent | Vahekaart **Üldine** ja lehed **Kiirloomine** | Tehingu kategooria ja ühiku kombinatsioonile juurdehindluse protsendi seadistamine. Näiteks tuleks lennupileti müügihinnale lisada juurdehindlus 10 protsenti üle lennupileti kulutuse omahinna. | Juurdehindlust rakendatakse müügi hinnakirjas ainult siis, kui hinnakujundusmeetodiks on valitud **Juurdehindlus üle omahinna**. |
| Valuuta | Vahekaart **Üldine** ja lehed **Kiirloomine** | Vaikimisi tuleb see väärtus hinnakirja päise valuutast. Tehingukategooria hinna määramiseks ei saa valuutat alistada. | See valuuta on vaikimisi valuuta, mille vaikeväärtuseks on kulude ja müügi sissetuleva kulutehingu klassi tegeliku rea hind. |

## <a name="pricing-methods-for-expenses"></a>Kulutuste hinnakujundus

Kui seadistate kategooria hindu, mis on asjakohased ainult kulutuste hinnakujunduse kontekstis, saate kasutada ühte järgmise kolme hinnakujundusmeetodi hulgast.

- **Ühiku hind**
- **Omahinnaga**
- **Juurdehindlus üle omahinna**

### <a name="price-per-unit"></a>Ühiku hind
Kui müügi hinnakirjaga seotud kategooria hinna real on valitud see hinnakujundusmeetod, on vaikehinnaks kategooria ja uhiku kombinatsioon nii prognoosis kui tegelikus näitajas. Prognoos viitab projekti prognoositavatele kulutuste ridadele, hinnapakkumise rea üksikasjadele ja kulutuste lepingurea üksikasjadele.

### <a name="at-cost"></a>Omahinnaga
Kui müügi hinnakirjaga seotud kategooria hinna real on valitud see hinnakujundusmeetod, on vaikehinnaks kategooria ja uhiku kombinatsioon ainult kulutuse tegeliku näitaja korral. Näiteks arveldamata müügi tegelikud näitajad kulutuse tehinguklassile. Ühiku hind määratakse arveldamata müügi tegelikule näitajale selle kulutuse tegeliku kulu ühiku hinna järgi. Kulul põhinevat hinna vaikeväärtuse määramist ei tehta kulutuste projekti prognoosis või kulutuste hinnapakkumise rea ja lepingu rea üksikasjades.

### <a name="markup-over-cost"></a>Juurdehindlus üle omahinna
Kui müügi hinnakirjaga seotud kategooria hinna real on valitud see hinnakujundusmeetod, on vaikehinnaks kategooria ja uhiku kombinatsioon ainult kulutuse tegeliku näitaja korral. Näiteks arveldamata müügi tegelikud näitajad kulutuse tehinguklassile. See ühikuhind määratakse tegelikule arveldamata müügile arvutatud väärtusele ühikuhinnast selle kulu tegelikule maksumusele pärast määratletud juurdehindlusprotsendi rakendamist. Kulul põhinevat hinna vaikeväärtuse määramist ei tehta kulutuste projekti prognoosis või kulutuste hinnapakkumise rea ja lepingu rea üksikasjades.
