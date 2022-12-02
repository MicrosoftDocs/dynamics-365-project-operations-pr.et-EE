---
title: Kuupäeva kehtiva hinna tühistamised
description: See artikkel kirjeldab, kuidas hinnakirjas teatud hindade puhul hindasid tühistada.
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
# <a name="date-effective-price-overrides"></a>Kuupäeva kehtiva hinna tühistamised 

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

*Kuupäeva kehtiva hinna tühistamised* pakuvad võimalust hinnakirjas konkreetseid hindu tühistada või muuta. Näiteks on teil tavahinnakiri, mis kehtib 1. jaanuarist 2022 kuni 31. detsembrini 2022. Selles hinnakirjas on hinnad paljudele rollidele. **Võrgutehniku** rolli jaoks seadistatud hind on 100 USA dollarit (USD) tunnis. Kui võrgutehnik logib aega ajavahemikus 1. jaanuar 2022 kuni 31. detsember 2022, on aja hind 100 USD. 1. oktoobril 2022 peate kohandama *ainult* **Võrgutehniku** rolli hinda 100 USD-lt tunnis 110 USD-le tunnis. Funktsioon **Kuupäeva kehtiva hinna tühistamised** võimaldab teil seadistada selle muudatuse selle konkreetse rollihinna rea alistamiseks. Seetõttu ei pea te kogu hinnakirja kopeerima ja muutma ainult selle ühe rea hinda.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Kuupäeva kehtiva hinna tühistamised tööjõu hinnakujunduse jaoks

Projekti tööaja kuupäeva kehtiva hinna tühistamiste seadistamise protsess koosneb kahest põhietapist.

1. Lubage funktsioon **Kuupäeva kehtiva hinna tühistamised**.
1. Seadistage kuupäeva kehtiva hinna tühistamine.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Lubage funktsioon kuupäeva kehtiva hinna tühistamine.

> [!NOTE]
> Kui funktsioon **Kuupäeva kehtiva hinna tühistamine** on lubatud, ei saa seda keelata.

Funktsiooni **Kuupäeva kehtiva hinna tühistamine** lubamiseks järgige neid samme.

1. Minge jaotisse **Sätted** \> **Parameetrid**.
1. Avage kirje **Parameetrid**.
1. Valige toimingupaani vahekaardil **Funktsiooni juhtimine** käsk **Luba kuupäeva kehtiva hinna tühistamine**.
1. Valige kinnitusdialoogis **OK**.
1. Mõne hetke pärast värskendage oma brauserit. Kuupäeva kehtiva hinna tühistamise võimalused peaksid nüüd olema saadaval. Teate, et need võimalused on lubatud, kui tegevuspaanil ei kuvata enam valikut **Luba kuupäeva kehtiva hinna tühistamine**.

### <a name="set-up-a-date-effective-price-override"></a>Seadistage kuupäeva kehtiva hinna tühistamine

Hinnakirjade **Kulu**, **Müük** või **Ost** hinnakirjades saab seadistada kuupäeva kehtiva hinna tühistamist.

> [!NOTE]
>Funktsiooni **Kuupäeva kehtiva hinna tühistamine** käitumisel on praegu järgmised piirangud.
>
> - Ainult rollihinnad ja rollihindade hinnalisandid toetavad rakenduse Project Operations funktsiooni **Kuupäeva kehtiva hinna tühistamine**.
> - Kui kopeerite hinnakirja, kasutades toimingut **Kopeeri** lehel **Hinnakirja üksikasjad** ja kui loote lepingu loomise ajal projekti hinnakirja standard- või kohandatud hinnakirjast, jõustub kuupäeva kehtiva hinna tühistamine **mitte** kopeeritud lähtehinnakirjast.

Rollihinna või rolli hinnalisandi kuupäeva kehtiva hinna tühistamise seadistamiseks järgige neid samme.

1. Avage selle hinnakirja leht, mille jaoks soovite kuupäeva kehtiva hinna tühistamise seadistada.
1. Valige vahekaart **Rollihinnad**. Sellel vahekaardil on loetletud kõik hinnakirja **Rollihinna** kirjed.
1. Valige kirje **Rollihind** millele soovite seadistada uue kuupäeva kehtiva hinna tühistamise, ja seejärel topeltpuudutage (või topeltklõpsake) **Rollihind**, et avada leht **Rolli hinna üksikasjad**.
1. Valige vahekaart **kuupäeva kehtiva hinna tühistamine**. Sellel vahekaardil olev ruudustik loetleb kõik valitud kirje **Rollihind** kuupäevast kehtiva hinna tühistamised.
1. Tehke ruudustiku kohal oleval tööriistaribal valik **Uue rolli hinna tühistamine**. Avaneb **Uue rolli hinna tühistamise** liugur.
1. Määrake hinna tühistamise kehtivusaeg, ühik ja uus hind. Seejärel valige **Salvesta** ja sulgege vorm.

> [!NOTE]
> - Rollihinna või rollihinna hinnalisandi tühistamine kuupäeva järgi on rakendatav samale hinnadimensiooni väärtuste kombinatsioonile, mis on olemas põhireal **Rollihind** või **Rollihinna hinnalisand**.
> - Väljal **Jõustub alates** valitud kuupäev peab jääma põhihinnakirja jõustumiskuupäevadesse. Hinna tühistamine jõustub väljal **Jõustub alates** valitud kuupäeval ja kehtib kuni põhihinnakirja lõppkuupäeva lõpuni. Kui seadistate samale rollihinnale teise kuupäeva kehtiva hinna tühistamise, jõustub esimene hinna tühistamine kuupäeval, mis on valitud väljal **Jõustub alates**, ja see kehtib kuni teise tühistamise alguseni.

## <a name="examples"></a>Näited

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Näide 1: kuupäeva kehtivuse määramine rollihinna jaoks, millel on rollihinna tühistamised

Järgmine näide näitab, kuidas määratakse kuupäeva kehtivus konkreetse rollihinna jaoks, mille jaoks on seadistatud rollihinna tühistamised.

**Hinnakiri A: 1. jaanuar kuni 30. juuni**

*Rollihind*

| Rollihind | Üksus | Hind | Mõju sissetulevate tehingute hinnakujundusele |
|---|---|---|---|
| Võrgutehnik | tund | 100 | Seda hinda kasutatakse kõigi tehingute puhul, mille tehingukuupäev on vahemikus 1. jaanuar kuni 14. märts. |

*Rollihinna tühistamine*

| Jõustub alates | Üksus | Hind | Mõju sissetulevate tehingute hinnakujundusele |
|---|---|---|---|
| 15. märts | tund | 110 | Seda hinda kasutatakse kõigi tehingute puhul, mille tehingukuupäev on vahemikus 15. märts kuni 30. märts. |
| Aprill 1 | tund | 120 | Seda hinda kasutatakse kõigi tehingute puhul, mille tehingukuupäev on vahemikus 1. aprill kuni 30. juuni. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Näide 2: kuupäeva kehtivuse määramine rollihinna hinnalisandi jaoks, millel on rollihinna hinnalisandi tühistamine

Järgmine näide näitab, kuidas määratakse kuupäeva kehtivus konkreetse rollihinna hinnalisandi jaoks, mille jaoks on seadistatud rollihinna hinnalisandi tühistamised.

**Hinnakiri A: 1. jaanuar kuni 30. juuni**

*Rollihind*

| Rollihind | Tööaeg | Üksus | Hind | Mõju sissetulevate tehingute hinnakujundusele |
|---|---|---|---|---|
| Võrgutehnik | Tavaline | tund | 100 | Seda hinda kasutatakse kõigi tehingute puhul, mille tehingukuupäev on vahemikus 1. jaanuar kuni 14. märts. |

*Rolli hinna hinnalisand*

| Organisatsiooniühik | Tööaeg | Hinnalisandi % |
|---|---|---|
| Jõgi US | Ületunnitöö | 10% |

*Rollihinna hinnalisandi tühistamine*

| Jõustub alates | Hind | Mõju sissetulevate tehingute hinnakujundusele |
|---|---|---|
| 15. märts | 20% | Seda hinnalisandi protsenti kasutatakse kõigi tehingute puhul, mille tehingukuupäev on vahemikus 15. märts kuni 30. märts. |
| Aprill 1 | 25% | Seda hinnalisandit kasutatakse kõigi tehingute puhul, mille tehingukuupäev on vahemikus 1. aprill kuni 30. juuni. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
