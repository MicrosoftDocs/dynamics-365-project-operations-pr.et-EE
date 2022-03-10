---
title: Kohandatud lahenduste loomine hinnakujunduse dimensioonide jaoks
description: Selles teemas selgitatakse, kuidas luua kohandatud hinnakujunduse dimensioonide loomise ajal kohandatud lahendus.
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
ms.openlocfilehash: 4dea80d8e4645675d3e89e846532ca7c0f292faa328c45938941c50dc15486fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995261"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Kohandatud lahenduste loomine hinnakujunduse dimensioonide jaoks

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Kõik kohandatud hinnakujunduse dimensiooni muudatused peaksid olema eraldi lahenduses. See oluline hea tava annab tulevikus paindlikkuse muudatuste värskendamiseks või eemaldamiseks vastavalt vajadusele, aitab teie tööd uuesti kasutada ja muudab nende muudatuste teisaldamise teistele eksemplaridele hõlpsamaks. Kui teete vajalikke muudatusi, eksportige see lahendus kui **Hallatud lahendus** ja importige see muudesse eksemplaridesse, et saaksite oma hinnakujunduse seadistust uuesti kasutada.

1. Valige **Sätted** > **Lahendused** ja valige seejärel **Uus**. 
2. Pange lahendusele nimi **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**, sisestage ülejäänud nõutav teave ja valige seejärel **Salvesta**.

> ![Kohandatud lahenduse loomine hinnakujunduse dimensioonide jaoks.](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Lisage kõik nõutavad olemid ja seotud komponendid hinnakujunduse dimensiooni lahendusse
Hinnakujunduse lahendusele tuleb lisada järgmised Project Service’i olemid. Läbige selle protseduuri etapid, et muuta hinnakujunduse lahenduses teatud olulisi skeeme, et olemid oleksid uutest hinnakujunduse dimensioonidest teadlikud.

1. Valige **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**. 
2. Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvandid **Lisa olemasolev** > **Olemid**.
3. Valige dialoogiboksis **Lahenduse komponendid** järgmised olemid.

- Tegelik
- Broneeritav ressurss
- Prognoosi rida
- Projekti ülesanne
- Arve rea üksikasjad
- Töölehe rida
- Projekti lepingurea üksikasi
- Projektimeeskonna liige
- Hinnapakkumise rea üksikasi
- Rolli hinna hinnalisand
- Rolli hind 
- Ajakirje 

> ![Olemasolevate olemite lisamine hinnakujunduse dimensioonide lahendusse.](media/Existing-entities-to-PD-solution.png)

> ![Lahenduse komponentide valimine.](media/Dimension-Components.png)

> [!NOTE]
> Veenduge, et kõigi valitud olemite jaoks kaasatakse kõik vormid ja vaated.

4. Kui teil palutakse kaasata valitud olemite jaoks kõik sõltuvad olemid, valige **Ei**.

> ![Ära kaasa kõiki seotud komponente.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]