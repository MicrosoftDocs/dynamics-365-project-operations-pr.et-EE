---
title: Hankija arvete loomine
description: Selles artiklis kirjeldatakse hankija arvete mõistet ja selgitatakse, kuidas neid Microsoftis luua Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475460"
---
# <a name="create-vendor-invoices"></a>Hankija arvete loomine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles artiklis kirjeldatud funktsioonide kasutamiseks peate tööruumis Funktsioonihaldus lubama **funktsiooni** Alltöövõtu tegeliku töötlemise lubamine ressursipõhiste stsenaariumide **project operationsiga.**

Microsofti hankija arveldust Dynamics 365 Project Operations saab kasutada hankijate poolt lõpule viidud projekti teenuste ja/või materjalide tarnete kulude registreerimiseks.

Kui teenused ja/või materjalid tellitakse allhanke korras hankijalt, tähistab alltöövõtt selle hankijaga sõlmitud lepingut. Kui hankija osutab teenuseid või kui materjalid võetakse vastu ja neid kasutatakse projekti ülesannetes, kajastatakse kulud projektis. Seejärel saadab hankija perioodiliselt arveid. Need arved kontrollitakse ja sobitatakse projektis kajastatud kuludega. Kui kinnitusprotsess on lõpule viidud, kinnitatakse hankija arve ja väljastatakse maksmiseks.

## <a name="scenarios-for-use"></a>Kasutatavad stsenaariumid

Hankija arveid projektitoimingutes saab kasutada kahe erineva stsenaariumi toetamiseks.

- Kliendid kasutavad kõiki allhankekogemusi.
- Kliendid ei kasuta täielikku alltöövõtukogemust, kuid soovivad saada ühtset vaadet project operationsi projektide kulude kohta.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Kliendid kasutavad kõiki allhankekogemusi

Hankija arve kasutuskogemused võimaldavad kontrollida ajakandeid, materjalikasutust ja kulukandeid, mis viitavad allhanke komponentidele, ning sobitada need hankija arve ridadega. Seda protsessi saab kasutada hankija arve ridade täpsuse kontrollimiseks. Kui kinnitusprotsess on lõpule viidud ja hankija arve kinnitatud, tühistab süsteem kinnitatud aja-, kulu- ja materjalikasutuse logidega salvestatud tegelikud kulud ning loob seejärel hankija arve ridade abil uued tegelikud kuluartiklid.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Kliendid ei kasuta täielikke allhankekogemusi, kuid soovivad saada ühtset vaadet project operationsi projektide kulude kohta

Kui jälgite allhankeprotsessi kolmanda osapoole süsteemis, saate salvestada kulud sellest kolmanda osapoole süsteemist Project Operationsisse, luues hankija arved, mis ei viita allhankele. Sel viisil saab teie projektijuhtidel olla ühtne ülevaade kõigi konkreetse projekti kulude kohta.

## <a name="create-vendor-invoices-in-project-operations"></a>Hankija arvete loomine rakenduses Project Operations

Hankija arved luuakse Dynamics 365 Finance moodulis **Ostureskontro**. Hankija arveid ei saa luua otse rakenduses Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Hankija arve kinnitamise seadistamine

Kui hankija arve on mõeldud allhanke jaoks rakenduses Dataverse, peate lubama **parameetri Pm käsitsi kontrollimine on nõutav**. Valiku seadistus määrab, kas hankija arve tuleks automaatselt kinnitada Dataverse või nõuab see käsitsi kinnitamist. Iga projekti hankija arve päis sisaldab samanimelist valikut. Vaikimisi on kõigi projekti hankija arvete päises olev valik määratud väärtusele, mille määrasite siin. Siiski saate väärtust värskendada vastavalt vajadusele üksikute hankija arvete päises.

Kui suvandi väärtuseks **on seatud Jah**, on rakenduses Finance loodud ja sünkroonitud Dataverse **hankija arve olek Mustand**. Seejärel peab projektijuht arve kinnitama ja kinnitama ning kinnitama, enne kui seda töödeldakse ja sisestatakse finance’is konkreetsetele projekti- ja pearaamatukontodele.

Kui suvandi väärtuseks **on määratud Ei**, kinnitatakse hankija arve automaatselt. Täiendavaid meetmeid ei ole vaja võtta.

Hankija arve kinnitamise seadistamiseks toimige järgmiselt.

1. Avage jaotises Rahandus **jaotis Projektihalduse ja raamatupidamise** \> **seadistamine** \> **Projektijuhtimine ja raamatupidamise parameetrid.**
1. **Määrake vahekaardil Finants suvand** Käsitsi kinnitamine PM-i järgi on nõutav **valikule** Jah **,** kui ettevõtte poliitika nõuab alltöövõtja hankija arvete kontrollimist. Kui projektijuhi kinnitust pole vaja Dataverse, jätke suvandikomplekt väärtusele **Ei**. Vaikimisi kasutatakse sätet lehel Hankija arve **ootel**.

> [!NOTE]
> Hankija arveid, mis on loodud alltöövõtulepingute jaoks, Dataverse saab õigesti töödelda ainult siis, kui **suvandi PM käsitsi kontrollimise kohustus** on seatud väärtusele **Jah**. Alltöövõtjate loodud tegelikud aja-, materjali- ja kulukulud saab projektijuht käsitsi hankija arve ridadega vastendada ainult siis, kui selle suvandi väärtuseks **on seatud Jah**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Hankija arvete jaoks hangete integratsioonikonto seadistamine

Kui hankija arve sisestatakse rakendusse Finance for Project Operations – integreeritud keskkond (mitte laos), sisestatakse finantsid hanke integratsioonikontole. Süsteem genereerib sisestatud arve tegelikud Dataverse väärtused. Need tegelikud andmed sisestatakse rakendusse Finance, kasutades projekti integreerimise töölehte. Projekti integreerimise töölehe sisestamine sisestab tegeliku kulu ja tühistab hanke integratsioonikonto.

Hankija arvete jaoks hanke integratsioonikonto seadistamiseks toimige järgmiselt.

1. Avage jaotises Rahandus **jaotis Projektihalduse ja raamatupidamise** \> **seadistamine** \> **Projektijuhtimine ja raamatupidamise parameetrid.**
1. **Vahekaardil Projektitoimingud Dynamics 365 customer engagement-is** valige **Materjalide** \> **hanke integratsioonikonto.**

### <a name="create-and-post-subcontract-vendor-invoices"></a>Allhanke hankija arvete loomine ja sisestamine

Kui ostureskontro ametnik saab alltöövõtjalt arve, luuakse rakenduses Finance uus arve.

1. Avage jaotises Rahandus **võlgnevused Arved** \> **·** \> **hankija ootel**.
1. **Valige toimingupaanil** **Hankija arve loomiseks Uus**.
1. Valige arve päises väljal **Arvekonto** suvand **Alltöövõtja**.
1. Valige arve kuupäev.
1. **Määrake vahekaardil Päis** suvandiKs **Pm-i käsitsi kontrollimine on nõutav** suvandiga **Jah**. Selle suvandi vaikesäte pärineb lehelt **Projektihalduse ja raamatupidamise parameetrid**. Kuid seda saab muuta hankija arve tasemel.
1. Valige kiirkaardil **Arve rida**, **et** luua hankija arve rida.
1. Valige allhankeridade jaoks loodud hankekategooria ja sisestage ühiku hind, mõõtühik ja kogus.
1. Valige jaotises **Hankija arve read vahekaardil Projekt** projekt, mille suhtes alltöövõtja alltöövõtuarvet jagab.
1. Valige projekti kategooria. See võib olla mis tahes tüüpi **kaupadest**, **kuludest**, **materjalidest** või **tundidest**.
1. Valige roll ainult siis, kui valitud projektikategooria on **tüüpi Tund**.
1. Hankija arve sisestamiseks valige **Postita**.

Teise võimalusena saate luua hankija arve, minnes valikule **Ostureskontro** \> **arved** \> **Ava hankija arved** ja valides **Uus.**

Kui hankija arve on sisestatud, muutub see projektijuhi kinnitamiseks ja töötlemiseks kättesaadavaks Dataverse.

## <a name="vendor-invoice-processing-in-dataverse"></a>Hankija arve töötlemine Dataverse

Rakenduses loodud hankijaarves Dataverse pärinevad mõned väljaväärtused hankija arvelt, mis on rakenduses Finance registreeritud. Muud väärtused on alltöövõtust tulenevad vaikeväärtused.

Järgmised väljad ja seotud kirjed kopeeritakse allhankelepingust hankija arve päisesse.

- Valuuta
- Lepingut sõlmiv üksus
- Maksetingimused

Hankija arve ridadel kasutab Project Operations järgmisi väljaväärtusi alltöövõtu ja allhanke rea vaikeviite sisestamiseks.

- Kande klass
- Roll
- Kande kategooria
- Toote väljad
- Project
- Toiming

> [!NOTE]
> Fikseeritud hinnaga allhankeridu project operationsis ei toetata.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
