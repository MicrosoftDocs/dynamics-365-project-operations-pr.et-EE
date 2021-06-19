---
title: Kandekategooria kasutamine hinnakujunduse dimensioonina
description: Selles teemas antakse teavet selle kohta, kuidas kasutada välja Kandekategooria hinnakujunduse dimensioonina.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d956545e1ad38fb09660f107e085f38d099c2207
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004436"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Kandekategooria kasutamine hinnakujunduse dimensioonina


_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


Selles teemas selgitatakse, kuidas kasutada välja **Kandekategooria** hinnakujunduse dimensioonina. 

## <a name="prerequisites"></a>Eeltingimused
Enne selles teemas toodud toimingu lõpetamist peab teil olema oma organisatsiooni jaoks uus hinnakujunduse lahendus. Kui te pole seda veel loonud, lugege teemat [Kohandatud väljade ja olemite loomine hinnakujunduse dimensioonidena](create-custom-fields-entities-pricing-dimensions.md).

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