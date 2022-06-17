---
title: Kandekategooria kasutamine hinnakujunduse dimensioonina
description: Selles artiklis antakse teavet kandekategooria kasutamise kohta hinnakujundusdimensioonina.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 1a1c2dc17c2092e5364d90e7efc1f13aee80703e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915731"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Kandekategooria kasutamine hinnakujunduse dimensioonina

[!include [banner](../includes/psa-now-project-operations.md)]

Selles artiklis kirjeldatakse, kuidas kasutada tehingukategooriat hinnakujundusdimensioonina. Enne alustamist peate looma uue hinnakujunduse dimensiooni lahenduse, kui te seda juba teinud ei ole. Kui teil on hinnakujunduse dimensiooni lahendus juba olemas, saate selles lahenduses muudatusi teha. Kui te pole oma organisatsiooni jaoks uut hinnakujundusdimensioonilahendust loonud, täitke toimingud [artiklis Kohandatud väljade ja olemite](create-custom-fields-entities.md) loomine.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
