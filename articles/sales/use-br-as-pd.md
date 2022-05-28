---
title: Broneeritava ressursi kasutamine hinnakujunduse dimensioonina
description: Selles teemas antakse teavet selle kohta, kuidas kasutada broneeritavat ressursi hinnakujunduse dimensioonina.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dcd01d80236f0218bc6fa3a1fe1389f8314f3c9b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598622"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Broneeritava ressursi kasutamine hinnakujunduse dimensioonina

 _**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_ 

Selles teemas antakse teavet selle kohta, kuidas kasutada broneeritavat ressursi hinnakujunduse dimensioonina. Kui teie hinnakujunduse strateegia on häälestatud nii, et igal broneeritaval ressursil peab olema kindel hinna või kulumäär, kasutage broneeritavat ressurssi hinnakujunduse dimensioonina.

## <a name="prerequisites"></a>Eeltingimused
Enne selles teemas toodud toimingu lõpetamist peab teil olema oma organisatsiooni jaoks uus hinnakujunduse lahendus. Kui te pole seda veel loonud, lugege teemat [Kohandatud väljade ja olemite loomine](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Välja Broneeritav ressurss lisamine vormidele ja vaadetele
Hinnakujunduse dimensiooni lahenduses välja **Broneeritav ressurss** nähtavaks muutmiseks peate lisama välja kõikidele vormiedele ja vaadetele olemina.

Järgmises tabelis on toodud olemite kaupa kõik valmiskujul vormid ja vaated. Lisaks peate lisama uue välja oma kohandatud olemite mis tahes täiendavatele vormidele või vaadetele.

|   Entity        | Vormid   |Vaatamised        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rolli hind| Teave | - Aktiivse ressursikategooria hinnad<br> - Seostatud ressursikategooria hinnad |
|  Rolli hinna hinnalisand| Teave| - Aktiivse rolli hinna hinnalisand<br>- Seostatud rolli hinna hinnalisand |
|  Hinnapakkumise rea üksikasjad| - Projekti teave<br>- Projekti kiirloomine| - Aktiivse hinnapakkumise rea üksikasjad<br>- Kombineeritud hinnapakkumise rea üksikasjad<br>- Hinnapakkumise rea üksikasjade seostatud vaade |
|  Projekti lepingurea üksikasjad| - Projekti teave<br>- Projekti kiirloomine| - Kombineeritud lepingurea üksikasjad<br>- Aktiivse lepingurea üksikasjad<br>- Seostatud lepingurea üksikasjad |
|  Projekti ülesanne| - Teave<br>- Uus vorm| &nbsp; |
|  Projektimeeskonna liige| - Teave<br>- Uus vorm| - Aktiivsed projektimeeskonna liikmed<br>- Projektimeeskonna liikmed<br>- Seostatud projektimeeskonna liikmed |
|  Ajakirje| - Teave<br>- Loo ajakirje| - Minu ajakirjed kuupäeva järgi<br>- Minu selle nädala ajakirjed<br>- Kellaajakirjed kinnitamiseks|
|  Töölehe rida| - Teave<br>- Kiirloomine| - Aktiivse töölehe read<br>- Seostatud töölehe rida |
|  Arve rea üksikasjad| - Teave<br>- Kiirloomine| - Aktiivse arve rea üksikasjad<br>- Arveldatavad arvekanded<br>- Tasuta arvekanded<br>- Seostatud arve rea üksikasjad <br>- Mittearveldatavad arvekanded|
|  Tegelik| - Teave<br>- Aktiivsed tegelikud näitajad| Seostatud tegelik näitaja |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Broneeritava ressursi hinnakujunduse dimensioonina seadistamine
Broneeritava ressursi hinnakujunduse dimensioonina seadistamiseks tehke järgmist.

1. Minge jaotisse **Sätted** > **Parameetrid**. 
2. Kontrollige, kas lehe **Parameeter** vahekaardil **Summapõhised hinnakujunduse dimensioonid** näitab vahekaardil olev ruudustik olemi **Hinnakujunduse dimensioonid** kirjeid. 
2. Lisage suvand **Broneeritav ressurss** hinnakujunduse dimensioonide loendisse kui **msdyn_bookableresource**. 
3. Valige väljadel **Rakendatakse kuludele** ja **Rakendatakse müügile** väärtus.
4. Valige väljal **Dimensiooni tüüp** suvand **Summal põhinev**. 
5. Valige broneeritava ressursi jaoks kulu ja müügi prioriteet. Tavaliselt on broneeritaval ressursis hinnakujunduse dimensiooni kaasatuna suurim prioriteet. Määrake prioriteediks **1** (või **0**, olenevalt sellest, kuidas te prioriteeti loendate), et tagada selline käitumine.

## <a name="set-up-pricing-dimension-field-names"></a>Seadistage hinnakujundamise dimensioonide välja nimed

Kui hinnakujunduse dimensiooni välja nimi on tabelis **Rolli hind** erinev selle välja nimest mõnes muus olemis, kus kasutatakse vaikehinda, tuleb hinnakujunduse dimensiooni kirjet erinevatest nimedest teavitada.  

Broneeritud ressursi puhul on olemil **Projektimeeskonna liikmed** veidi teistsugune väljanimi kui olemil **Rolli hind**. 

 - Olem **Projektimeeskonna liikmed** = **msdyn_bookableresourceid**
 - Olem **Rolli hind** = **msdyn_bookableresource**

Suvandi **msydn_bookableresource** hinnakujunduse dimensiooni kirjet tuleb sellest erinevusest teavitada.

1. Topeltklõpsake ruudustikus **Hinnakujunduse dimensioonid** rida, et avada suvandi **msdyn_bookableresource** dimensioonide leht.
2. Valige dimensioonide lehel vahekaardil **Seotud** suvand **Hinnakujunduse dimensioonide väljanimed**.

  ![Hinnadimensioonide väljanimede vahekaart.](media/PD-fieldname.png)

3. Valige avanevas seosete vaates suvand **Lisa uus hinnakujunduse dimensiooni väljanimi**.

  ![Lisa uus hinnakujunduse dimensiooni väljanimi.](media/Add-NewPD-fieldname.png)

  Avaneb leht **Uus hinnakujunduse dimensiooni väljanimi** suvandi **msdyn_bookableresource** jaoks. 

4. Lisage lehel **Uus hinnakujunduse dimensiooni väljanimi** lisandmoodul **msdyn_projectteam** suvandile **Olemi loogiline nimi**.
5. Lisage lisandmoodul **msdyn_bookableresourceid** suvandile **Väljanimi**.

 ![Uus hinnakujunduse dimensiooni väljanime vorm.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]