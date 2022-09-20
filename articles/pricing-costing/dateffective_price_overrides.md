---
title: Jõustumiskuupäevaga hinna alistamised
description: Selles artiklis selgitatakse, kuidas seadistada hinnakirjas konkreetsete hindade alistamised.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445999"
---
# <a name="date-effective-price-overrides"></a>Jõustumiskuupäevaga hinna alistamised 

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

*Jõustumiskuupäevaga hinna alistamised* võimaldavad hinnakirjas konkreetseid hindu alistada või muuta. Näiteks on teil standardhinnakiri, mis kehtib 1. jaanuarist 2022 kuni 31. detsembrini 2022. Selles hinnakirjas on hinnad paljudele rollidele. Võrgutehniku **rolli jaoks** seadistatud hind on 100 USA dollarit (USD) tunnis. Kui võrgutehnik logib aega ajavahemikus 1. jaanuar 2022 kuni 31. detsember 2022, on selle aja hinnaks 100 USD. 1. oktoobril 2022 peate kohandama hinda *ainult* võrgutehniku **rolli jaoks**, alates 100 USD tunnis kuni 110 USD tunnis. Funktsioon Jõustumiskuupäev **alistab** selle muudatuse selle konkreetse rollihinna rea alistamisena. Seetõttu ei pea te kopeerima kogu hinnakirja ja muutma ainult selle ühe rea hinda.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Tööjõu hinnakujunduse jõustumistähtajaga hinna alistamised

Projekti tööaja kuupäeva-efektiivsete hinnaületuste seadistamise protsess koosneb kahest põhietapist.

1. Luba **jõustumiskuupäeva hinna alistamise** funktsioon.
1. Seadistage jõustumisjärgse hinna alistamine.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Hinna alistamise kuupäeva funktsiooni lubamine

> [!NOTE]
> Pärast seda, **kui funktsioon Jõustumiskuupäev** on lubatud, ei saa seda keelata.

Jõustumiskuupäeva **hinna alistamise** funktsiooni lubamiseks toimige järgmiselt.

1. Avage **Seaded** \> **Parameetrid.**
1. **Avage kirje Parameetrid**.
1. Valige toimingupaani vahekaardil **Funktsioonijuhtimine** käsk **Luba kehtiva hinna alistamise** kuupäev.
1. Valige kinnitusdialoogis **OK**.
1. Mõne hetke pärast värskendage brauserit. Kuupäevaga kehtiva hinna alistamise võimalused peaksid nüüd saadaval olema. Te teate, et need võimalused on lubatud, kui **toimingupaanil ei kuvata enam lubamiskuupäeva kehtivaid hinna alistamist**.

### <a name="set-up-a-date-effective-price-override"></a>Kuupäevaga kehtiva hinna alistamise seadistamine

Jõustumiskuupäevaga hinna alistamised saab seadistada hinnakirjades **Kulu**, **Müük** või **Ost**.

> [!NOTE]
>Hinna alistamise **kuupäeva** käitumisel on praegu järgmised piirangud.
>
> - Ainult rollide hinnad ja rolli hinna juurdehindlused toetavad Project Operationsi **funktsiooni Jõustumishinna alistamise** kuupäev.
> - Kui kopeerite hinnakirja, kasutades **toimingut** Kopeeri **lehel Hinnakirja üksikasjad**, ja kui loote lepingu loomise ajal standardsest või kohandatud hinnakirjast projekti hinnakirja, ei **kopeerita kuupäevaga kehtivaid hinnaalustusi** lähtehinnaloendist.

Rolli hinna või rolli hinna juurdehindluse kuupäevapõhise hinna alistamise seadistamiseks toimige järgmiselt.

1. Avage selle hinnakirja leht, mille jaoks soovite seadistada jõustumiskuupäevaga hinna alistamise.
1. Valige **vahekaart Rollide hinnad** . Sellel vahekaardil on **loetletud kõik hinnakirjas olevad rolli hinnakirjed**.
1. **Valige rolli hinnakirje**, mille jaoks soovite seadistada uue kuupäevaga kehtiva alistamise hinna, ja seejärel topeltpuudutage (või topeltklõpsake) **rolli hinda**, et avada **leht Rolli hinna üksikasjad**.
1. **Valige vahekaart Jõustumiskuupäev alistamised**. Selle vahekaardi ruudustikus on loetletud kõik valitud **rolli hinnakirje** kuupäevapõhise hinna alistamised.
1. Tehke ruudustiku kohal oleval tööriistaribal valik **Uus rollihinna alistamine**. Avaneb **liugur Uus rollihinna alistamine**.
1. Määrake alistatud hinna jõustumiskuupäeva, ühiku ja uue hinna. Seejärel valige **Salvesta** ja sulgege vorm.

> [!NOTE]
> - Rolli hinna või rolli hinna juurdehindluse kuupäevaga kehtiva hinna alistamine rakendatakse samale hinnadimensiooni väärtuste kombinatsioonile, mis on olemas emarolli **hinna** või **rolli hinna juurdehindluse** real.
> - Väljal **Kehtiv** alates valitud kuupäev peaks jääma emahinnakirja jõustumiskuupäevade piiresse. Hinna alistamine jõustub väljal Jõustumine **alates valitud** kuupäeval ja kehtib kuni põhihinnakirja lõppkuupäeva lõpuni. Kui seadistate sama rolli hinna jaoks uue kuupäevaga kehtiva hinna alistamise, jõustub esimene hinna alistamine väljal Kehtiv **alates valitud** kuupäeval ja kehtib kuni teise alistamise alguseni.

## <a name="examples"></a>Näited

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Näide 1: kuupäevaefektiivsuse määramine rolli hinnale, millel on rolli hinna alistamised

Järgmine näide näitab, kuidas kuupäevaefektsus määratakse konkreetse rolli hinna jaoks, mille jaoks rolli hinna alistamised on seadistatud.

**Hinnakiri A: 1. jaanuar kuni 30. juuni**

*Rolli hind*

| Rolli hind | Üksus | Hind | Mõju sissetulevate tehingute hinnakujundusele |
|---|---|---|---|
| Võrgutehnik | tund | 100 | Seda hinda kasutatakse kõigi tehingute puhul, mille tehingu kuupäev on vahemikus 1. jaanuar kuni 14. märts. |

*Rolli hinna alistamine*

| Efektiivne alates | Üksus | Hind | Mõju sissetulevate tehingute hinnakujundusele |
|---|---|---|---|
| 15. märts | tund | 110 | Seda hinda kasutatakse kõigi tehingute puhul, mille tehingu kuupäev on vahemikus 15. märts kuni 30. märts. |
| Aprill 1 | tund | 120 | Seda hinda kasutatakse kõigi tehingute puhul, mille tehingu kuupäev on vahemikus 1. aprill kuni 30. juuni. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Näide 2: kuupäevaefektsuse määramine rolli hinnalisandi puhul, millel on rolli hinna juurdehindluse alistamine

Järgmine näide näitab, kuidas kuupäevaefektsus määratakse konkreetsele rolli hinnalisandile, mille jaoks rolli hinnalisand alistamised on seadistatud.

**Hinnakiri A: 1. jaanuar kuni 30. juuni**

*Rolli hind*

| Rolli hind | Tööaeg | Üksus | Hind | Mõju sissetulevate tehingute hinnakujundusele |
|---|---|---|---|---|
| Võrgutehnik | Regulaarne | tund | 100 | Seda hinda kasutatakse kõigi tehingute puhul, mille tehingu kuupäev on vahemikus 1. jaanuar kuni 14. märts. |

*Rolli hinna juurdehindlus*

| Organisatsiooni üksus | Tööaeg | Üleshindlus % |
|---|---|---|
| Jõgi US | Ületunnitöö | 10% |

*Rolli hinna juurdehindluse alistamine*

| Efektiivne alates | Hind | Mõju sissetulevate tehingute hinnakujundusele |
|---|---|---|
| 15. märts | 20% | Seda juurdehindluse protsenti kasutatakse kõigi tehingute puhul, mille tehingu kuupäev on vahemikus 15. märts kuni 30. märts. |
| Aprill 1 | 25% | Seda märgistust kasutatakse kõigi tehingute puhul, mille tehingu kuupäev on vahemikus 1. aprill kuni 30. juuni. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
