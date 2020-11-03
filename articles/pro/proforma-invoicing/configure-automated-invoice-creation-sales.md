---
title: Näidisarve automaatse loomise konfigureerimine
description: Selles teemas antakse teavet näidisarvete automaatse loomise konfigureerimise kohta.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e146dd510b3795d52d164fc6acf8e5400ba11310
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074865"
---
# <a name="configure-automated-proforma-invoice-creation"></a>Näidisarve automaatse loomise konfigureerimine

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Saate rakenduses Dynamics 365 Project Operations automaatse arve loomise konfigureerida. Süsteem loob iga projekti lepingu ja lepingurea jaoks arve ajakaval põhineva näidisarve mustandi. Arve ajakavad konfigureeritakse lepingurea tasemel. Igal lepingureal võib olla eraldi arve ajakava või saab igale lepingureale kaasata sama arve ajakava.

Arve loomisel loob süsteem alati projekti lepingu kohta vähemalt ühe arve. Mõnel juhul luuakse mitu arvet.

Näiteks kui lepingul on mitu klienti, luuakse sama arv arveid kui on kliente, kellel on selle projekti lepingu kohta arveldatavaid tehingud.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Tehingute arvesse kaasamise mõistmine 

Mõnikord määratleb iga projektil põhinev lepingurida eraldi arve ajakava. Näiteks Adatum lepingu rakendamisel on järgmised lepinguread.

- Prototüüp, mis on fikseeritud hinnaga koos kahe käsitsi loodud vahe-eesmärgiga.
- Rakendamise töö, mis sisaldab aega ja arveldatakse kahe nädala tagant esmaspäeviti.
- Kulud, mille eest tuleb arved esitada iga kuu esimesel esmaspäeval.

Mõlemal kahel real määratletud arvete ajakavad näevad välja nagu järgmine tabel.

| Lepingurida | Arve tsükli kuupäev | Kande katkestamise kuupäev | Vahe-eesmärgi kuupäev | Vahe-eesmärgi summa |
| --- | --- | --- | --- | --- |
| Prototüüp | Esmaspäev, 5. oktoober | - | Esmaspäev, 5. oktoober | 5000 USD |
| - | Teisipäev, 3. november | - | Teisipäev, 3. november | 12,000 USD |
| Töö rakendamine | Esmaspäev, 5. oktoober | Pühapäev, 4. oktoober | - | - |
| - | Esmaspäev, 19. oktoober | Pühapäev, 18. oktoober | - | - |
| - | Esmaspäev, 2. november | Pühapäev, 1. november | - | - |
| - | Esmaspäev, 16. november | Pühapäev, 15. november | - | - |
| Tekkinud kulud | Esmaspäev, 5. oktoober | Pühapäev, 4. oktoober | - | - |
| - | Esmaspäev, 2. november | Pühapäev, 1. november | - | - |

Selles näites käivitub automaatne arveldamine järgmiselt.

- **4. oktoober või mis tahes päev enne seda** : selle lepingu jaoks ei looda arvet, kuna iga sellise lepingurea tabel **Arve ajakava** ei sea arve rakendamise kuupäevaks pühapäeva, 4. oktoobrit.
- **Esmaspäev, 5. oktoober** : üks arve luuakse järgmise jaoks.

    - Prototüüp, mis sisaldab vahe-eesmärki, kui see on märgitud kui **Arveldamiseks valmis**.
    - Rakendamise töö, mis hõlmab kõiki ajatehinguid, mis on loodud enne tehingu katkestamise kuupäeva pühapäeval, 4. oktoobril, mis on märgitud kui **Arveldamiseks valmis**.
    - Tekkinud kulud, mis hõlmavad kõiki kulutehinguid, mis on loodud enne tehingu katkestamise kuupäeva pühapäeval, 4. oktoobril, mis on märgitud kui **Arveldamiseks valmis**.
  
- **6. oktoober või mis tahes päev enne 19. oktoobrit** : selle lepingu jaoks ei looda arvet, kuna iga sellise lepingurea tabel **Arve ajakava** ei sea arve rakendamise kuupäevaks pühapäeva, 6. oktoobrit või mis tahes päeva enne 19. oktoobrit.
- **Esmaspäev, 19. oktoober** : luuakse üks arve rakendamise töö jaoks, mis hõlmab kõiki ajatehinguid, mis on loodud enne tehingu katkestamise kuupäeva pühapäeval, 18. oktoobril, mis on märgitud kui **Arveldamiseks valmis**.
- **Esmaspäev, 2. november** : üks arve luuakse järgmise jaoks.

    - Rakendamise töö, mis hõlmab kõiki ajatehinguid, mis on loodud enne tehingu katkestamise kuupäeva pühapäeval, 1. novembril, mis on märgitud kui **Arveldamiseks valmis**.
    - Tekkinud kulud, mis hõlmavad kõiki kulutehinguid, mis on loodud enne tehingu katkestamise kuupäeva pühapäeval, 1. novembril, mis on märgitud kui **Arveldamiseks valmis**.

- **Teisipäev, 3. november** : üks arve luuakse prototüübi jaoks, mille vahe-eesmärk sisaldab 12 000 USA dollarit, kui see on märgitud kui **Arveldamiseks valmis**.

## <a name="configure-automatic-invoicing"></a>Automaatse arveldamise konfigureerimine

Toimige järgmiselt, et konfigureerida automatiseeritud arve.

1. Avage rakendus **Project Operations** , minge jaotisesse **Sätted** > **Korduva arve seadistamine**.
2. Looge pakett-töö ja pange sellele nimeks **Project Operationsi arvete loomine**. Pakett-töö nimi peab sisaldama sõnu „arvete loomine”.
3. Valige väljal **Töö tüüp** väärtus **Puudub**. Vaikimisi on väljade **Sageduse päev** ja **On aktiivne** väärtuseks **Jah**.
4. Valige **Käivita töövoog**. Näete dialoogiboksis **Kirje otsimine** kolme töövoogu.

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Valige **ProcessRunCaller** ja seejärel **Lisa**.
6. Valige järgmises dialoogiboksis **OK**. **Unerežiimi** töövoole järgneb **protsessi** töövoog. 

> [!NOTE]
> Etapis 5 saate valida ka töövoo **ProcessRunner**. Seejärel, kui valite **OK** , järgneb **protsessi** töövoole **unerežiimi** töövoog.

Töövood **ProcessRunCaller** ja **ProcessRunner** loovad arveid. **ProcessRunCaller** kutsub töövoo **ProcessRunner**. **ProcessRunner** on töövoog, mis tegelikult loob arveid. Töövoog läbib kõik lepinguread, mille jaoks tuleb arved luua, ja see loob neile ridadele arveid. Selleks et määratleda lepingu read, mille jaoks arved tuleb luua, vaatab töö lepingurea arve käivitamise kuupäevi. Kui ühele lepingule kuuluvatel lepinguridadel on sama arve käivitamise päev, kombineeritakse tehingud ühe arvega, millel on kaks arve rida. Kui arvete loomiseks pole kandeid, jätab töö arve loomise vahele.

Kui **ProcessRunner** on töö lõpetanud, kutsub see töövoo **ProcessRunCaller** , annab lõppkellaaja ja sulgub. **ProcessRunCaller** käivitab seejärel taimeri, mis kestab määratud lõppkellaajast 24 tundi. Taimeri lõpus on **ProcessRunCaller** suletud.

Arvete loomiseks kasutatav pakktöötluse töö on korduv töö. Kui seda pakktöötlust käitatakse mitu korda, luuakse mitu tööeksemplari ja need põhjustavad tõrkeid. Seetõttu peaksite pakktöötluse käivitama ainult üks kord ja seejärel uuesti käivitama ainult siis, kui see lakkab töötamast.

> [!NOTE]
> Project Operationsis pakett-arveldamine töötab ainult projekti lepinguridade jaoks, mis on arvegraafikute poolt konfigureeritud. Fikseeritud hinnaga arveldusmeetodiga lepingureal peavad olema seadistatud vahe-eesmärgid. Aja- ja materjalikulu arveldusmeetodiga projekti lepingurea jaoks peab olema seadistatud kuupäevapõhine ajakava.