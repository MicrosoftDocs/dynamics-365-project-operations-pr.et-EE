---
title: Lahenduse loomine kohandatud hinnakujunduse dimensioonide jaoks
description: Selles teemas kirjeldatakse, kuidas luua kohandatud hinnakujunduse jaoks lahendusi.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 82593d3d00b008c1922d70c508bc77624aeb46b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601105"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Lahenduse loomine kohandatud hinnakujunduse dimensioonide jaoks

 _**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_ 

>[!IMPORTANT]
>Kõik kohandatud hinnakujunduse dimensiooni muudatused peaksid olema eraldi lahenduses. See oluline hea tava võimaldab paindlikkust värskendada või eemaldada vastavalt vajadusele muudatusi, aitab teid oma töö uuesti kasutamisel ja muudab lihtsamaks teisedada need muudatused teistesse eksemplaridesse. Pärast vajalike muudatuste tegemist eksportige see lahendus kui **Hallatud** lahendus ja importige seejärel muudesse eksemplaridesse, et uuesti kasutada.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Lahenduse loomine kohandatud hinnakujunduse dimensioonide jaoks

1.  Valige **Sätted** > **Lahendused** ja valige seejärel **Uus**.
2.  Sisestage lahenduse nimi, organisatsiooni *\<your organization name\> hinnakujunduse dimensioonid*.
3. Sisestage ülejäänud nõutav teave ja calige seejärel **Salvesta**.

  ![Kohandatud hinnakujunduse dimensiooni lahenduse loomine.](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Lisage kõik nõutavad olemid ja seotud komponendid hinnakujunduse dimensiooni lahendusse

Lisage oma hinnakujunduse lahendusele järgmised teenuse Project Service olemid, et teha oma hinnakujunduse lahenduses olulised skeemi muudatused. Pärast selle toimingu lõpetamist tuvastavad olemid uue hinnakujunduse dimensiooni.

1.  Valige **Sätted** > **Lahendused** ja topeltklõpsake seejärel valikut **organisatsiooni <*teie organisatsiooni nimi*> hinnakujunduse dimendioonid**.
2.  Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvandid **Lisa olemasolev** > **Olemid**.
3.  Valige dialoogiboksis **Lahenduse komponendid** järgmised olemid.
 
   - **Tegelik**
   - **Broneeritav ressurss**
   - **Prognoosi rida**
   - **Projekti ülesanne**
   - **Arve rea üksikasjad**
   - **Töölehe rida**
   - **Projekti lepingurea üksikasi**
   - **Projektimeeskonna liige**
   - **Hinnapakkumise rea üksikasi**
   - **Rolli hinna hinnalisand**
   - **Rolli hind**
   - **Ajakirje**
 
   ![Olemasolevate olemite kohandatud hinnakujunduse dimensiooni lahenduse lisamine.](./media/Existing-entities-to-PD-solution.png)
 
 4. Vaadake iga olemi kohta lisatavaid komponente ja iga olemi kohta olemi varade lõplikku loendit. 

   >[!NOTE]
   > Kaasake iga valitud olemite jaoks kõik vormid ja vaated.

  ![Lisatud olemid.](./media/solution-component-selection.png)


5.  Kui teil palutakse lisada valitud olemite jaoks mis tahes sõltuvaid olemeid, valige suvand **Ei, ära kaasa nõutavaid komponente.**

    ![Kaasab sõltuvad olemid.](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]