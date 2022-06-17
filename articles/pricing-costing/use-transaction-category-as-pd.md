---
title: Kandekategooria kasutamine hinnakujunduse dimensioonina
description: Selles artiklis antakse teavet selle kohta, kuidas kasutada välja Kandekategooria hinnakujundusdimensioonina.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 648933299616a683b19bbe2f1231caac779bd1f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911689"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Kandekategooria kasutamine hinnakujunduse dimensioonina


_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


Selles artiklis selgitatakse, kuidas kasutada **välja Kandekategooria** hinnakujundusdimensioonina. 

## <a name="prerequisites"></a>eeltingimused
Enne selle artikli protseduuride lõpuleviimist peab teil olema oma organisatsiooni jaoks uus hinnakujundusdimensiooni lahendus. Kui te pole seda veel loonud, lugege teemat [Kohandatud väljade ja olemite loomine hinnakujunduse dimensioonidena](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Välja Kandekategooria lisamine vormidele ja vaadetele
Hinnakujunduse dimensiooni lahenduses välja **Kandekategooria** nähtavaks muutmiseks peate lisama välja kõikidele vormiedele ja vaadetele olemina.

Järgmises tabelis on toodud olemite kaupa kõik valmiskujul vormid ja vaated. Lisaks peate lisama uue välja oma kohandatud olemite mis tahes täiendavatele vormidele või vaadetele.

|  Entity        | Vormid     |Vaatamised        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rolli hind| Teave |- Aktiivse ressursikategooria hinnad<br> - Seostatud ressursikategooria hinnad |
|  Rolli hinna hinnalisand| Teave|- Aktiivse rolli hinna hinnalisand<br>- Seostatud rolli hinna hinnalisand |
|  Hinnapakkumisrea üksikasi|- Projekti teave<br>- Projekti kiirloomine| - Aktiivse hinnapakkumise rea üksikasjad<br>- Kombineeritud hinnapakkumise rea üksikasjad<br>- Hinnapakkumise rea üksikasjade seostatud vaade |
|  Projekti lepingurea üksikasi|- Projekti teave<br>- Projekti kiirloomine|- Kombineeritud lepingurea üksikasjad<br>- Aktiivse lepingurea üksikasjad<br>- Seostatud lepingurea üksikasjad |
|  Projekti ülesanne|- Teave<br>- Uus vorm| &nbsp; |
|  Projektimeeskonna liige|- Teave<br>- Uus vorm|- Aktiivsed projektimeeskonna liikmed<br>- Projektimeeskonna liikmed<br>- Seostatud projektimeeskonna liikmed |
|  Ajakirje|- Teave<br>- Loo ajakirje|- Minu ajakirjed kuupäeva järgi<br>- Minu selle nädala ajakirjed<br>- Kellaajakirjed kinnitamiseks|
|  Töölehe rida|- Teave<br>- Kiirloomine|- Aktiivse töölehe read<br>- Seostatud töölehe rida|
|  Arve rea üksikasjad|- Teave<br>- Kiirloomine|- Aktiivse arve rea üksikasjad<br>- Arveldatavad arvekanded<br>- Tasuta arvekanded<br>- Seostatud arve rea üksikasjad <br>- Mittearveldatavad arvekanded|
|  Tegelik|- Teave<br>- Aktiivsed tegelikud näitajad| Seostatud tegelik näitaja |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Välja Kandekategooria seadistamine hinnakujunduse dimensioonina

1. Minge jaotisse **Sätted** > **Parameetrid**. 
2. Kontrollige, kas lehe **Parameetrid** vahekaardil **Summapõhised hinnakujunduse dimensioonid** näitab vahekaardil olev ruudustik olemi **Hinnakujunduse dimensioonid** kirjeid.
3. Lisage sellesse loendisse **Kandekategooria** ja seadke väljade **Kehtib kulu kohta** ja **Kehtib müügi kohta** väärtusteks **Jah**.
4. Valige väljast **Dimensiooni tüüp** väärtus **Summapõhine** ja seejärel valige suvandi **Kandekategooria** jaoks prioriteet, kui see on seotud kulu ja müügiga.


[!INCLUDE[footer-include](../includes/footer-banner.md)]