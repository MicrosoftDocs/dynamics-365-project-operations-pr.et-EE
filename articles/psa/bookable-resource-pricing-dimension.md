---
title: Kasutage broneeritavat ressurssi hinnakujunduse dimensioonina
description: Selles teemas antakse teavet broneeritava ressursi kasutamise kohta hinnakujunduse dimensioonina.
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
ms.openlocfilehash: d3f5ed7da5972cec5b22524bdcb3dc34a83eee28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290939"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Kasutage broneeritavat ressurssi hinnakujunduse dimensioonina

[!include [banner](../includes/psa-now-project-operations.md)]

Selles teemas antakse teavet broneeritava ressursi kasutamise kohta hinnakujunduse dimensioonina. Enne alustamist peate looma uue hinnakujunduse dimensiooni lahenduse, kui te seda juba teinud ei ole. Kui teil on hinnakujunduse dimensiooni lahendus juba olemas, saate selles lahenduses muudatusi teha. Kui te pole oma organisatsiooni jaoks uut hinnakujunduse dimensiooni lahendust loonud, viige lõpuni teema [Kohandatud väljade ja olemite loomine](create-custom-fields-entities.md) protseduurid.

## <a name="add-bookable-resource-to-forms-and-views"></a>Lisage vormidele ja vaadetele broneeritav ressurss
Selleks, et muuta väljad hinna dimensiooni lahenduses kasutajaliideses nähtavaks, tuleb teil läbida kõik Project Service’i põhiolemite vormid ja vaated ning lisada need väljad nende olemite vormidele ja vaadetele.
Järgmine tabel on terviklik loend valmis vormidest ja vaadetest, mis on loetletud olemite kaupa ja mida tuleb värskendada. Kui nende olemite kohandamistes on täiendavaid vaateid või vorme, lisage neile ka uued väljad.
Avage hinnakujunduse dimensiooni lahendus Solution Explorer ja klõpsake seejärel käsku **Avalda kõik kohandused**.


|   Olem        | Vormid   |Vaated        |
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

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Seadistage broneeritav ressurss hinnakujunduse dimensioonina

1. Avage veebiliideses **Project Service** > **Sätted** > **Parameetrid**. Pange tähele, et lehel **Parameeter**, vahekaardil **Summapõhisel hinnakujunduse dimensioonid** olev ruudustik kuvab olemi hinnakujunduse dimensioonides olevad kirjed. 
2. Lisage suvand **Broneeritav ressurss** hinnakujunduse dimensioonide loendisse kui **msdyn_bookableresource**. 
3. Määrake kontekst, milles broneeritav ressurss töötab hinnakujunduse dimensioonina, ning määrake suvandite **Rakendatakse kuludele** ja **Rakendatakse müügile** väärtused.
4. Valige väljal **Dimensiooni tüüp** suvand **Summal põhinev**. 
5. Valige broneeritava ressursi jaoks kulu ja müügi prioriteet. Tavaliselt, kui see on seotud hinnakujunduse dimensiooniga, on broneeritaval ressursil kõrgeim prioriteet, nii et selle seadmine väärtuseks **1** (või **0**, olenevalt sellest, kuidas prioriteeti loendate) tagab selle käitumise.

## <a name="set-up-pricing-dimension-field-names"></a>Seadistage hinnakujundamise dimensioonide välja nimed

Kui hinnakujunduse dimensiooni välja nimi on tabelis **Rolli hind** erinev selle välja nimest mõnes muus olemis, kus hindade vaikeväärtus peab töötama, tuleb hinnakujunduse dimensiooni kirjet erinevatest nimedest teavitada.    
Broneeritud ressursi puhul on olemil **Projekti meeskonnaliikmed** veidi teistsugune väljanimi (**msdyn_bookableresourceid**), kui olemil **Rolli hind** (**msdyn_bookableresource**). Suvandi **msydn_bookableresource** hinnakujunduse dimensiooni kirje tuleb sellest teadlikuks teha. 
1. Selleks topeltklõpsake ruudustikus **Hinnakujunduse dimensioonid** rida, et avada suvandi **msdyn_bookableresource** dimensioonide leht.
2. Dimensioonide lehel klõpsake vahekaardil **Seotud** nuppu **Hinnakujunduse dimensioonide väljanimed**.

 ![Hinnadimensioonide väljanimede vahekaart](media/PD-fieldname.png)

4. Klõpsake avanevas seosete vaates käsku **Lisa uus hinnakujunduse dimensiooni väljanimi.**

 ![Lisa uus hinnakujunduse dimensiooni väljanimi](media/Add-NewPD-fieldname.png)


Avaneb leht **Uus hinnakujunduse dimensiooni väljanimi** suvandi **msdyn_bookableresource** jaoks. 

5. Lisage suvand **msdyn_projectteam** väljale **Olemi loogiline nimi** ja suvand **msdyn_bookableresourceid** väljale **Välja nimi**. Kirje salvestamine

 ![Uus hinnakujunduse dimensioonide välja nimede vorm](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]