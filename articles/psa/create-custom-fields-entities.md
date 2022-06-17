---
title: Kohandatud väljade ja olemite loomine
description: Selles artiklis selgitatakse, kuidas luua platvormil oma lahenduses valikukomplekte ja olemeid Power Apps.
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
ms.openlocfilehash: 3b6f675d604f3b6a6f2465c413ceff3d16815e12
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926909"
---
# <a name="create-custom-fields-and-entities"></a>Kohandatud väljade ja olemite loomine 

[!include [banner](../includes/psa-now-project-operations.md)]

Läbige järgmised etapid iga kord, kui soovite luua kohandatud suvandikomplekt või olemi platvormil Power Apps.  
Selle artikli protseduurid tuleks lõpule viia project service automation (PSA) veebiliidese abil.

> [!IMPORTANT]
> Soovitame teil teha kõik kohandatud hinnakujunduse dimensiooni muudatused eraldi lahenduses. See oluline hea tava annab tulevikus paindlikkuse muudatuste värskendamiseks või eemaldamiseks vastavalt vajadusele, aitab teie tööd uuesti kasutada ja muudab nende muudatuste teisaldamise teistele eksemplaridele hõlpsamaks. Kui olete kõik vajalikud muudatused teinud, eksportige see lahendus kui **Hallatud lahendus** ja importige see muudesse eksemplaridesse, et saaksite oma hinnakujunduse seadistust uuesti kasutada.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Kohandatud väljade ja suvandikomplekti loomine hinnakujunduse dimensiooni lahenduses

Hinnakujunduse dimensioon võib olla suvandikomplekt või olem. Mõlemad tuleb luua hinnakujunduse lahenduses. Selle protseduuri etapid selgitavad, kuidas luua olemil ja suvandikomplektil põhinevaid dimensioone.

### <a name="entity-based-dimensions"></a>Olemil põhinevad dimensioonid

1. Klõpsake PSA-s **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**.
2. Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Olemid**.
3. Klõpsake nuppu **Uus**, et luua uus olem nimega **Standardne pealkiri**. Sisestage ülejäänud nõutav teave ja seejärel klõpsake nuppu **Salvesta**.

> ![Olemi Standardne pealkiri määratlus.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Suvandikomplektil põhinevad dimensioonid 
Saate luua kaks suvandikomplektil põhinevat dimensiooni. Kasutage suvandit **Ressursi töö asukoht**, et jälgida asukoha **Kodu** ja **Kohapeal** töö hinda ning kasutada suvandit **Ressursi töö aega** väärtustega **Regulaarne** ja **Ületunnitöö**, et rakendada rakendamiseks töö lõpetamisel märgistus.


1. Klõpsake PSA-s **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**. 
2. Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Suvandikomplektid**. 
3. Uue suvandikomplekti loomiseks klõpsake nuppu **Uus**, sisestage ülejäänud nõutav teave ja seejärel klõpsake nuppu **Salvesta**.

> ![Suvandikomplektil põhinev hinnakujunduse dimensioon nimega Ressursi tööasukoht.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Suvandikomplektil põhinev hinnakujunduse dimensioon nimega Ressursi töötunnid.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Olemil põhinevate dimensioonide andmete loomine

Olemil põhinevate dimensioonide andmeid saate luua ka käsitsi, või kasutada rakenduse Microsoft Excel importimise või hoolduskõnede funktsiooni. Selle protseduuri etappide abil saate luua kaks standardset pealkirja, **Süsteemide insener** ja **Süsteemide vaneminsener** olemil põhinevast dimensioonist, **Standardne pealkiri**. Kui andmed, mida soovite luua, on väikesed, nagu järgmises näites, saate kasutada standardset vormi.

1. Klõpsake rakenduses PSA suvandit **Täpsem otsing**. Valige olem **Standardne pealkiri** ja klõpsake suvandit **Tulemused**. Kuvatakse kõik olemi **Standardne pealkiri** read.
2. Klõpsake nuppu **Uus**. Sisestage väljale **Nimi** suvand Süsteemi insener, ja klõpsake seejärel nuppu **Salvesta**.
3. Sulgege vorm. 
4. Korrake etappe 1–3, et luua teine standardne suvandile Süsteemi vaneminsener.

> ![Näidisandmed olemi Standardne pealkiri jaoks.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
