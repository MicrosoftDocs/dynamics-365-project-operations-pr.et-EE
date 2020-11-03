---
title: Kandekategooria kasutamine hinnakujunduse dimensioonina
description: Selles teemas antakse teavet selle kohta, kuidas kasutada kandekategooriat hinnakujunduse dimensioonina.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0019571a1d37d3b6a503e7221db3c3b51365c236
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075040"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Kandekategooria kasutamine hinnakujunduse dimensioonina
Selles teemas kirjeldatakse, kuidas kasutada kandekategooriat hinnakujunduse dimensioonina. Enne alustamist peate looma uue hinnakujunduse dimensiooni lahenduse, kui te seda juba teinud ei ole. Kui teil on hinnakujunduse dimensiooni lahendus juba olemas, saate selles lahenduses muudatusi teha. Kui te pole oma organisatsiooni jaoks uut hinnakujunduse dimensiooni lahendust loonud, viige lõpuni teema [Kohandatud väljade ja olemite loomine](create-custom-fields-entities.md) protseduurid.

## <a name="add-transaction-category-to-forms-and-views"></a>Kandekategooria lisamine vormidele ja vaadetele
Kui soovite, et kandekategooria oleks hinnakujunduse dimensiooni lahenduse kasutajaliideses nähtav, peate üle vaatama kõik põhiolemite vormid ja vaated ning lisama need väljad nende olemite vormidele ja vaadetele.
Järgmises tabelis on esitatud terviklik loend valmisvormidest ja -vaadetest olemitelt, mida on vaja uute väljadega värskendada. Kui teil on nende olemite kohandustes täiendavaid vaateid või vorme, lisage uued väljad ka neile.

|  Olem        | Vormid     |Vaated        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rolli hind|• Teave |• Aktiivse ressursikategooria hinnad<br> • Ressursikategooria hinna seostatud vaade|
|  Rolli hinna hinnalisand|• Teave|• Aktiivse rolli hinna hinnalisand<br>• Rolli hinna hinnalisandi seostatud vaade|
|  Hinnapakkumise rea üksikasi|• Projekti teave<br>• Projekti kiirloomine|• Aktiivse hinnapakkumise rea üksikasjad<br>• Kombineeritud hinnapakkumise rea üksikasjad<br>• Hinnapakkumise rea üksikasjade seostatud vaade|
|  Projekti lepingurea üksikasjad|• Projekti teave<br>• Projekti kiirloomine|• Kombineeritud lepingurea üksikasjad<br>• Aktiivse lepingurea üksikasjad<br>• Lepingurea üksikasjade seostatud vaade|
|  Projekti ülesanne|• Teave<br>• Uus vorm||
|  Projektimeeskonna liige|• Teave<br>• Uus vorm|• Aktiivsed projekti meeskonnaliikmed<br>• Projekti meeskonnaliikmed<br>• Projekti meeskonnaliikmete seostatud vaade|
|  Ajakirje|• Teave<br>• Ajakirje loomine|• Minu ajakirjed kuupäeva järgi<br>• Minu selle nädala ajakirjed<br>• Ajakirjed kinnitamiseks|
|  Töölehe rida|• Teave<br>• Kiirloomine|• Aktiivse töölehe read<br>• Töölehe rea seostatud vaade|
|  Arve rea üksikasjad|• Teave<br>• Kiirloomine|• Aktiivse arve rea üksikasjad<br>• Arveldatavad arvekanded<br>• Tasuta arvekanded<br>• Arve rea üksikasjade seostatud vaade<br>• Mittearveldatavad arvekanded|
|  Tegelik|• Teave<br>• Aktiivsed tegelikud näitajad|• Tegelik seostatud vaade|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Kandekategooria seadistamine hinnakujunduse dimensioonina

1. Avage veebiliideses **Project Service** > **Sätted** > **Parameetrid**. 
2. Pange tähele, et lehe **Parameetrid** vahekaardil **Summapõhised hinnakujunduse dimensioonid** näitab vahekaardil olev ruudustik olemi **Hinnakujunduse dimensioonid** kirjeid.
3. Lisage sellesse loendisse **Kandekategooria** ja seadke väljade **Kehtib kulu kohta** ja **Kehtib müügi kohta** väärtusteks **Jah**.
4. Valige väljast **Dimensiooni tüüp** väärtus **Summapõhine** ja seejärel valige kulu ja müügiga seotud **Kandekategooria** jaoks prioriteet.
