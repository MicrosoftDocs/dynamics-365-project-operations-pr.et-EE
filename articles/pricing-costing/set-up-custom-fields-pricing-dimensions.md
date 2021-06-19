---
title: Kohandatud väljade seadistamine hinnakujunduse dimensioonidena
description: Selles teemas kirjeldatakse, kuidas seadistada kohandatud väljade abil hinnakujunduse dimensioone.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d40a80f80bd766bfc19e831ea805a4043baf0030
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004706"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Kohandatud väljade seadistamine hinnakujunduse dimensioonidena

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Enne kui alustate, eeldame, et olete lõpetanud toimingud teemades [Kohandatud väljade ja olemite loomine](create-custom-fields-entities-pricing-dimensions.md) ning [Nõutavate kohandatud väljade lisamine hinna seadistamisele ja ülekande olemitele](add-custom-fields-price-setup-transactional-entities.md). Kui te pole neid toiminguid lõpetanud, minge tagasi, viige need lõpuni ja seejärel tulge selle teema juurde tagasi. 

Selles teemas kirjeldatakse, kuidas seadistada kohandatud hinnakujunduse dimensioone. Pange tähele, et lehe **Parameetrid** vahekaart **Summapõhised hinnakujunduse dimensioonid** näitab hinnakujunduse dimensioonide kirjeid. Vaikimisi on sellel vahekaardil ruudustikus kaks rida.

- **msdyn_resourcecategory** (roll)
- **msdyn_OrganizationalUnit** (organisatsiooniüksus)

> [!IMPORTANT]
> Ärge kustutage neid ridu. Kui te aga neid ei vaja, saate need sätestada selliselt, et nad konkreetses kontekstis ei rakenduks, seades väljade **Kehtib kulu kohta**, **Kehtib müügi kohta** ja **Kehtib ostu kohta** väärtuseks **Ei**. Kui seate need atribuudiväärtused sättele **Ei**, teeb see sama välja nagu teil puuduks väli hinnakujunduse dimensioonina.

Selleks et väli saaks muutuda hinnakujunduse dimensiooniks, peab see olema:

- Loodud väljana **Rolli hinna** ja **Rolli hinna hinnalisandi** olemites. Lisateavet selle kohta, kuidas seda teha, leiate jaotisest [Kohandatud väljade lisamine hinna seadistamisele ja ülekande olemitele](add-custom-fields-price-setup-transactional-entities.md).

- Luuakse reana tabelisse **Hinnakujunduse dimensioon**. Näiteks lisage hinnakujunduse dimensiooni read järgmisel pildil kuvatud kujul. 

![Summapõhised hinnakujunduse dimensiooni read](media/Amt-based-PD.png)

Ressursi töötunnid (**msdyn_resourceworkhours**) lisatakse hinnalisandipõhise dimensioonina ja see on lisatud vahekaardil **Hinnalisandipõhise hinnakujunduse dimensioon** olevasse ruudustikku.

![Hinnalisandipõhised hinnakujunduse dimensioonide read](media/Markup-based-PD.png)


> [!IMPORTANT]
> Mis tahes hinnakujunduse dimensiooni andmete muudatus siin tabelis, olemasolev või uus, lisatakse hinnakujunduse äriloogikasse alles pärast vahemälu värskendamist. Vahemälu värskendusaeg võib olla kuni 10 minutit. Oodake see aeg ära, et näha hinnakujunduse vaikeloogikas muutusi, mis peavad tulenema hinnakujunduse dimensiooni andmete muudatustest.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Hinnakujunduse dimensioonide tabeli atribuudid
Järgmistes jaotistes antakse teavet tabeli **Hinnakujunduse dimensioonid** erinevate atribuutide kohta.

### <a name="pricing-dimension-name"></a>Hinnakujunduse dimensiooni nimi
See väärtus peaks olema täpselt sama välja skeemi nimega, mis on lisatud kohandatud hinnakujunduse dimensioonide jaoks tabelisse **Rolli hind**. Lisateavet selle kohta, kuidas lisada välju tabelisse **Rolli hind**, leiate jaotisest [Kohandatud väljade lisamine hinna seadistamisele ja ülekande olemitele](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Dimensiooni tüüp
Hinnakujunduse dimensioone on kahte tüüpi.
  
  - **Summapõhised dimensioonid**: sisendi konteksti dimensiooniväärtused vastavad **Rolli hinna** real olevatele dimensiooniväärtustele ja hind/kulu võetakse vaikimisi otse tabelist **Roll hind**.
  - **Hinnalisandipõhised dimensioonid**: need on dimensioonid, kus hinna/kulu saamiseks kasutatakse kolmeetapilist protsessi
 
    1. Põhimäära saamiseks vastendataksesisendi konteksti mitte-hinnalisandipõhised dimensiooniväärtused Rolli hinna reale.
    2. Hinnalisandi protsendi saamiseks vastendatakse sisendi konteksti kõik dimensiooniväärtused **Rolli hinna** reale.
    3. Lõpliku hinna/kulu saamiseks rakendatakse teisest etapist saadud hinnalisandi protsendi tabelist **Rolli hind** pärit põhimäärale, mis saadi esimeses etapis.
   
   Järgmine tabel näitab hindade hinnalisanduste arvutamist.
  
| Roll        | Organisatsiooniüksus    |Töö asukoht      |Standardpealkiri      |Ressursi töötunnid      |  Tõsta hinda|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Kohapeal            |                    |Ületunnitöö                 |15     |
|             | Contoso India|Kohalikud             |                    |Ületunnitöö                 |10     |
|             | Contoso US   |Kohalikud             |                    |Ületunnitöö                 |20     |


Kui Contoso Indiast pärinev ressurss, mille põhimäär on 100 USA dollarit, töötab kohapeal ning nad logivad ajakirjes 8 tundi tavalist tööaega ja 2 tundi ületunnitööd, kasutab hinnakujunduse mootor 8 tunni salvestamiseks põhimäära väärtusega 100 (kokku 800 USA dollarit). 2 tunni ületunnitöö puhul rakendatakse põhimäärale 100 juurde 15%-hinnalisandit, saades ühiku hinnaks 115 USA dollarit ja salvestades kogukulu väärtuseks 230 USA dollarit.

### <a name="applicable-to-cost"></a>Kehtib kulu kohta 
Kui see on seadistatud sättele **Jah**, tähendab see seda, et kulu ja hinnalisandi määrade saamisel peab **Rolli hinnale** ja **Rolli hinna hinnalisandile** vastamiseks kasutama sisendi konteksti dimensiooniväärtust.

### <a name="applicable-to-sales"></a>Kehtib müügi kohta
Kui see on seadistatud sättele **Jah**, tähendab see seda, et arve ja hinnalisandi määrade saamisel peab **Rolli hinnale** ja **Rolli hinna hinnalisandile** vastamiseks kasutama sisendi konteksti dimensiooniväärtust.

### <a name="applicable-to-purchase"></a>Kehtib ostu kohta
Kui see on seadistatud sättele **Jah**, tähendab see seda, et ostuhinna saamisel peab **Rolli hinnale** ja **Rolli hinna hinnalisandile** vastamiseks kasutama sisendi konteksti dimensiooniväärtust. Allhankelepingute stsenaariumeid ei toetata, seega seda välja ei kasutata. 

### <a name="priority"></a>Prioriteet
Dimensiooni prioriteedi seadistamine aitab hinnakujundusel luua hinda isegi siis, kui ei leita sisendi dimensiooniväärtuste ja tabelitest **Rolli hind** või **Rolli hinna hinnalisand** pärit väärtuste vahel täpset vastet. Sellises stsenaariumis kasutatakse vasteta dimensiooniväärtuste jaoks nullväärtusi, mõõtes dimensioonid nende prioriteetide järgi.

- **Kuluprioriteet**: dimensiooni kuluprioriteedi väärtus näitab seadistatud kuluhindadega vastendamisel selle dimensiooni kaalu. **Kuluprioriteedi** väärtus peab olema kordumatu nende dimensioonide seas, mis **kehtivad kulu kohta**.
- **Müügiprioriteet**: dimensiooni müügiprioriteedi väärtus näitab seadistatud müügihindade või arveldusmääradega vastendamisel selle dimensiooni kaalu. **Müügiprioriteedi** väärtus peab olema kordumatu nende dimensioonide seas, mis **kehtivad müügi kohta**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]