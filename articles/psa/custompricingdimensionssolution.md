---
title: Kohandatud lahenduste loomine hinnakujunduse dimensioonide jaoks
description: Selles artiklis selgitatakse, kuidas kohandatud hinnakujundusdimensioonide loomisel luua kohandatud lahendus.
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
ms.openlocfilehash: 0df6728634b169c8a1a128aba1555d79fee5719f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929025"
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
