---
title: Mitme valuutaga stsenaariumid (versioon 3.x)
description: Selles teemas antakse teavet mitme valuutaga stsenaariumi kohta.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 2925d431258a150d5830238fb5ff365499b1b440
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590157"
---
# <a name="multiple-currency-scenarios"></a>Mitme valuutaga stsenaariumid

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Rakenduses Microsoft Dynamics 365 on kaks valuutakontseptsiooni.

- **Tehingu valuuta** – valuuta, milles tehing toimub. 
- **Põhivaluuta** – Dynamics 365 eksemplari valuuta. See valuuta seadistatakse juhul, kui Dynamics 365 eksemplar on ette valmistatud. Seda ei saa muuta.

Näiteks, Jõgi USA müüs 100 T-särki Suurbritannia kliendile hinnaga 15 naelsterlingit (GBP) tükk. Järgmine tabel näitab, kuidas see kanne salvestatakse tootetellimuste üksusesse.

| Toode | Kogus | Ühiku hind | Valuuta | Summa | Vahetuskurss | Hind ühiku kohta (alus)| Summa (alus)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| T-särk | 100      | 15             | GBP      | 1500   | 0.94          | 17.25               | 1725       |

Veerus **Valuuta** kuvatakse tehingu valuuta. Selleks on valuuta, milles müük toimus. Veerus **Vahetuskurss** kuvatakse tehingu valuuta ja põhivaluuta vahetuskurss. Põhivaluuta on USA dollar (USD). Põhivaluuta seadistatakse juhul, kui Dynamics 365 eksemplar on ette valmistatud.
Nagu tabelist näha, kirjendatakse kõik kanded nii tehingu valuutas kui ka põhivaluutas. Dynamics 365 kasutab valuuta vahetuskurssi põhivaluuta summade arvutamiseks.

## <a name="project-service-automation-extensions"></a>Project Service Automation laiendused

Dynamics 365 Project Service Automation mõjutab tehingu valuutat, kuna äritehingutel on tavaliselt kaks aspekti: kulu ja müük.

Äritehinguteks loetakse järgmisi üksusi.

- Hinnapakkumise rea üksikasi
- Projekti lepingurea üksikasjad
- Prognoosi rida
- Töölehe rida
- Arve rea üksikasjad
- Tegelik

Kõigis neis üksustes on kirje, mis tähistab kulu summat või müügisummat. Mis tahes Dynamics 365 üksuse puhul, millel on väli **Summa**, sisaldab iga kirje summasid nii tehingu valuutas kui ka põhivaluutas. 

PSA laiendab tehingu valuuta kontseptsiooni kulude ja müügi jaoks järgmistel viisidel.

- Ajakannete tehingu valuuta põhineb alati selle organisatsiooniüksuse valuutal, mis on projekti omanik või haldab seda. Seda organisatsiooniüksuse nimetatakse tellijaks.
- Aja- ja kuluarvestuse müügitehingute valuuta põhineb alati projektilepingu valuutal.
- Kulude kulutehingute valuuta põhineb valuutal, milles kulusisestus loodi.

## <a name="multiple-currency-scenario"></a>Mitme valuutaga stsenaarium

Selles jaotises on näide projektist, milles Jõgi UK saadab tooteid Fabrikami-nimelisele kliendile Jaapanis. Siin näete, kuidas selle stsenaarium üles on ehitatud.

1. GBP ja Jaapani jeen (JPY) seadistatakse jaotises **Sätted** \> **Ettevõtte haldus** \> **Valuutad**. 
2. Seadistatakse kliendikonto nimega **Fabrikami – Jaapan** ja ettevõtte konto valuutaks valitakse JPY.
3. Seadistatakse organisatsiooniüksus nimega **Jõgi UK** ja selle valuutaks valitakse GBP.
4. Luuakse projekti leping, milles **Jõgi UK** on määratletud kui tellija ja **Fabrikami – Jaapan** on määratud kliendiks.
5. Projekti lepinguread luuakse, võttes aluseks projekti erinevate tehingute klasside arvete esitamise korra, näiteks arvete esitamise aja või kulude järgi.
6. Luuakse projekt, kus **Jõgi UK** on määratletud hankija. Luuakse projekt ja vastendatakse see projekti lepinguridadega.


Hinnapakkumise rea üksikasju, projekti lepingurea üksikasju või ajakava kalkulatsiooni rida kasutava prognoosi jooksul luuakse olemis alati kaks kirjet. Üks kirje on kulu ja teine müügi jaoks.

- Vaikimisi seatakse kulukirje tehingu valuutaks projekti tellija riigi valuuta. Selles näites on valuutaks GBP.
- Vaikimisi seatakse müügikirje tehingu valuutaks projekti lepingu valuuta. Selles näites on valuutaks JPY.

Kui tegelikud andmed on loodud aja jaoks, kasutades ajakirjet või töölehe rida, ilmneb järgmine käitumine.

- Vaikimisi seatakse kulukirje tehingu valuutaks projekti tellija riigi valuuta.
- Vaikimisi seatakse müügikirje tehingu valuutaks projekti lepingu valuuta.

Kui tegelikud andmed on loodud kulude jaoks, kasutades kulukirjet või töölehe rida, ilmneb järgmine käitumine.

- Kulu summa saate kirjendada mis tahes valuutas. Valige valuuta, kasutades lehel **Kulukirje** või **Töölehe rida** olevat valuutavalijat. Vaikimisi seatakse kulukirje tehinguvaluutaks kulukirje valuuta. 
- Vaikimisi on müügikirje tehinguvaluutaks projekti lepingu valuuta. Selle valuuta seadmiseks teisendab süsteem kõigepealt tehingu summa valuutas, mille kasutaja on sisestanud põhivaluutasse. Seejärel teisendatakse summa projekti lepingu valuutaks. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Ümberarvestused, kui projekti tegelikud andmed salvestatakse mitmes tehinguvaluutasse

Dynamics 365 tegeleb automaatselt summade ümberarvestusega erinevates valuutades. Vaatame näidet.

| Kande klass | Kandetüüp| Date   | Ressurss | Kande kategooria | Kogus | Ühiku hind | Summa      | Vahetuskurss | Alussumma |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Arveldamata müük   | 14. juuni | Marko  |                      | 8 h    | 20 000 JPY    | 160 000 JPY | 123           | 1300.81 USD    |
| Time              | Arveldamata müük   | 15. juuni | Marko  |                      | 8 h    | 20 000 JPY    | 160 000 JPY | 123           | 1300.81 USD    |
| Kulu           | Arveldamata müük   | 16. juuni | Marko  | Hotell                | 1 EA     | 250 EUR      | 250 EUR     | 0.94          | 265.95 USD     |
| Kulu           | Arveldamata müük   | 17. juuni | Marko  | Autorent           | 1 EA     | 150 EUR      | 150 EUR     | 0.94          | 159.57 USD     |

Kui soovite arvutada projekti arveldamata müügi kogusummat, saate kõigi seostuvate arvestatud müügi tegelike väärtuste väljale **Summa** luua ümberarvestuse välja. Ümberarvestuse väli on Dynamics 365 konstruktsioon, mis võimaldab seostuvate kirjete jaoks kiiresti valemeid luua.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
