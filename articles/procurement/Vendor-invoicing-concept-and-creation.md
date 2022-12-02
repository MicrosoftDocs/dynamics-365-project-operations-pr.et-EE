---
title: Hankija arvete koostamine
description: See artikkel kirjeldab hankija arvete kontseptsiooni ja selgitatakse, kuidas neid rakenduses Microsoft Dynamics 365 Project Operations luua.
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
# <a name="create-vendor-invoices"></a>Hankija arvete koostamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles artiklis kirjeldatud funktsioonide kasutamiseks peate lubama funktsiooni **Ressursipõhiste stsenaariumide jaoks allhankelepingute tegelike näitajate töötlemise lubamine rakenduses Project Operations** tööruumis **Funktsioonihaldus**.

Hankija arveldust rakenduses Microsoft Dynamics 365 Project Operations saab kasutada hankijate poolt lõpule viidud projekti teenuste ja/või materjalide tarnimise kulude registreerimiseks.

Kui teenuste ja/või materjalide allhankelepingud sõlmitakse hankijaga, kujutab allhankeleping selle hankijaga sõlmitud lepingut. Kui hankija osutab teenuseid või kui materjale võetakse vastu ja kasutatakse projektiülesannete täitmisel, kirjendatakse kulud projektis. Seejärel saadab hankija perioodiliselt arveid. Need arved kontrollitakse ja viiakse vastavusse projektis kajastatud kuludega. Pärast kontrolliprotsessi lõppu kinnitatakse hankija arve ja see vabastatakse tasumiseks.

## <a name="scenarios-for-use"></a>Kasutamise stsenaariumid

Rakenduse Project Operations hankija arveid saab kasutada kahe erineva stsenaariumi toetamiseks.

- Kliendid kasutavad kõiki allhankekogemusi.
- Kliendid ei kasuta kõiki allhankekogemusi, kuid soovivad rakenduse Project Operations projektide kuludest ühtset ülevaadet.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Kliendid kasutavad kõiki allhankekogemusi

Hankija arvekogemused võimaldavad kontrollida ajakirjeid, materjalikasutuse- ja kulukirjeid, mis viitavad allhankelepingute sõlmitud komponentidele ja viiakse hankija arve ridadega vastavusse. Seda protsessi saab kasutada hankija arve ridade täpsuse kontrollimiseks. Pärast kinnitamisprotsessi lõpetamist ja hankija arve kinnitamist pöörab süsteem kinnitatud aja-, kulu- ja materjalikasutuse logides registreeritud tegelikud näitajad ümber ning seejärel loob hankija arve ridade abil uued kulude tegelikud näitajad.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Kliendid ei kasuta kõiki allhankekogemusi, kuid soovivad rakenduse Project Operations projektide kuludest ühtset ülevaadet

Kui jälgite allhankeprotsessi kolmanda osapoole süsteemis, saate registreerida selle kolmanda osapoole süsteemi kulud rakendusele Project Operations, luues hankija arveid, mis ei viita allhankelepingutele. Nii saavad teie projektijuhid omada ühte ja ühtset ülevaadet antud projekti kõigist kuludest.

## <a name="create-vendor-invoices-in-project-operations"></a>Hankija arvete loomine rakenduses Project Operations

Hankija arved luuakse rakenduses Dynamics 365 Finance, kasutades moodulit **Ostureskontro**. Te ei saa hankija arveid otse teenuses Dataverse luua.

### <a name="set-up-vendor-invoice-verification"></a>Hankija arve kinnitamise seadistamine

Kui hankija arve on ette nähtud allhankelepingu jaoks teenuses Dataverse, peate lubama parameetri **Käsitsi kinnitamine on nõutav**. Valiku seadistus määrab, kas hankija arve tuleb teenuses Dataverse automaatselt kinnitada või nõuab see käsitsi kinnitamist. Iga projekti hankija arve päis sisaldab samanimelist valikut. Vaikimisi on kõigi projekti hankija arvete päises olev suvand seatud väärtusele, mille siin määrate. Siiski saate väärtust vastavalt vajadusele värskendada üksikute hankijaarvete päises.

Kui suvand on seatud väärtusele **Jah**, on teenuses Rahandus loodud ja teenusega Dataverse sünkroonitud hankija arvel olek **Mustand**. Seejärel peab projektijuht arve valideerima ja kontrollima ning kinnitama, enne kui see töödeldakse ja postitatakse konkreetsetele projekti- ja pearaamatu kontodele Rahanduses.

Kui valikuks on seatud **Ei**, kinnitatakse müüja arve automaatselt. Edasist tegevust pole vaja.

Hankija arvete kinnitamise seadistamiseks järgige järgmisi samme.

1. Rahanduses minge jaotisesse **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Projektihaldus ja raamatupidamisparameetrid**.
1. Kui ettevõtte poliitika nõuab alltöövõtja hankija arvete kinnitamist, määrake vahekaardil **Finants** suvandi **Käsitsi kinnitamine projektijuhi poolt on nõutav** väärtuseks **Jah**. Kui projektijuhi kinnitus pole teenuses Dataverse, jätke valikuks **Ei**. Vaikimisi kasutatakse seadet lehel **Ootel hankija arve**.

> [!NOTE]
> Allhankelepingute jaoks teenuses Dataverse loodud hankija arveid saab õigesti töödelda ainult siis, kui suvand **Projektijuhi käsitsi kinnitamine on nõutav** on seatud väärtusele **Jah**. Alltöövõtjja koostatud aja-, materjali- ja kulukulude tegelikke näitajaid saab projektijuht hankija arve ridadega käsitsi sobitada ainult siis, kui selle valiku väärtuseks on määratud **Jah**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Hankija arvete jaoks hangete integreerimise konto seadistamine

Kui hankija arve postitatakse rakenduse Project Operations rahandusse – integreeritud keskkonda (mittelaopõhine), postitatakse finantsandmed hankeintegratsiooni kontole. Süsteem genereerib sisestatud arve tegelikud näitajad teenuses Dataverse. Need tegelikud näitajad postitatakse Rahandusse projekti integreerimise töölehe abil. Projekti integreerimise töölehele postitamine postitab kulu tegeliku näitaja ja tühistab hanke integreerimise konto.

Hankija arvete hankeintegratsiooni konto seadistamiseks järgige neid samme.

1. Rahanduses minge jaotisesse **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Projektihaldus ja raamatupidamisparameetrid**.
1. Valige vahekaardil **Project operations rakenduses Dynamics 365 customer engagement**, valige **Materjalid** \> **Hangete integratsioonikonto**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Alltöövõtja hankija arvete loomine ja postitamine

Kui võlgnevuste ametnik saab ostureskontrolt arve, koostatakse rahanduses uus arve.

1. Rahanduses minge jaotisesse **Ostureskontrod** \> **Arved** \> **Ootel hankija arved**.
1. Hankija arve loomiseks valige **Toimingupaanil** **Uus**.
1. Arve päises valige väljal **Arvekonto** **Alltöövõtja**.
1. Valige arve kuupäev.
1. Vahekaardil **Päis** määrake suvandi **Projektijuhi käsitsi kinnitamine on nõutav** väärtuseks **Jah**. Selle valiku vaikesäte pärineb lehelt **Projektihaldus ja raamatupidamisparameetrid**. Seda saab aga muuta hankija arve tasemel.
1. Valige kiirkaardil **Arve rida** hankija arve rea loomiseks **Lisa rida**.
1. Valige allhankeridade jaoks loodud hankekategooria ja sisestage ühiku hind, mõõtühik ja kogus.
1. Valige jaotises hankija arve read vahekaardil **Projekt** projekt, mille suhtes alltöövõtja allhankearvet jagab.
1. Valige projekti kategooria. See võib olla mis tahes tüüpi **Üksus**, **Kaup**, **Materjalid** või **Tunnid**.
1. Valige roll ainult siis, kui valitud projektikategooria on tüübiga **Tund**.
1. Hankija arve postitamiseks valige **Postita**.

Teise võimalusena saate hankija arve koostada, minnes jaotisesse **Ostureskontro** \> **Arved** \> **Avatud hankija arved** ja valides **Uus**.

Kui hankija arve on postitatud, muutub see teenuses Dataverse kättesaadavaks projektijuhi kinnitamiseks ja töötlemiseks.

## <a name="vendor-invoice-processing-in-dataverse"></a>Hankija arvete töötlemine teenuses Dataverse

Teenuses Dataverse loodud hankija arvel pärinevad mõned välja väärtused Rahanduses salvestatud hankija arvelt. Muud väärtused on allhankelepingust tulenevad vaikeväärtused.

Järgmised väljad ja seotud kirjed kopeeritakse allhankelepingust hankija arve päisesse.

- Valuuta
- Lepingut sõlmiv üksus
- Maksetingimused

Hankija arve ridadel kasutab rakendus Project Operations allhankelepingu ja allhankelepingurea vaikeviite sisestamiseks järgmisi väljaväärtusi.

- Kande klass
- Roll
- Kande kategooria
- Tooteväljad
- Project
- Toiming

> [!NOTE]
> Fikseeritud hinnaga allhankelepinguid ei toetata rakenduses Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
