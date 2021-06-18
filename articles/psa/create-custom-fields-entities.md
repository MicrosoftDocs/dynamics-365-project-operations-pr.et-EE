---
title: Kohandatud väljade ja olemite loomine
description: Selles teemas kirjeldatakse, kuidas luua suvandikomplekte ja olemeid oma platvormi Power Apps lahenduses.
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
ms.openlocfilehash: 3d838bde8a3d7cbc15e06fb3289924468c284a8a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998946"
---
# <a name="create-custom-fields-and-entities"></a>Kohandatud väljade ja olemite loomine 

[!include [banner](../includes/psa-now-project-operations.md)]

Läbige järgmised etapid iga kord, kui soovite luua kohandatud suvandikomplekt või olemi platvormil Power Apps.  
Selles teemas kirjeldatud protseduurid tuleb lõpule viia, kasutades rakenduse Project Service Automation (PSA) veebiliidest.

> [!IMPORTANT]
> Soovitame teil teha kõik kohandatud hinnakujunduse dimensiooni muudatused eraldi lahenduses. See oluline hea tava annab tulevikus paindlikkuse muudatuste värskendamiseks või eemaldamiseks vastavalt vajadusele, aitab teie tööd uuesti kasutada ja muudab nende muudatuste teisaldamise teistele eksemplaridele hõlpsamaks. Kui olete kõik vajalikud muudatused teinud, eksportige see lahendus kui **Hallatud lahendus** ja importige see muudesse eksemplaridesse, et saaksite oma hinnakujunduse seadistust uuesti kasutada.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Kohandatud väljade ja suvandikomplekti loomine hinnakujunduse dimensiooni lahenduses

Hinnakujunduse dimensioon võib olla suvandikomplekt või olem. Mõlemad tuleb luua hinnakujunduse lahenduses. Selle protseduuri etapid selgitavad, kuidas luua olemil ja suvandikomplektil põhinevaid dimensioone.

### <a name="entity-based-dimensions"></a>Olemil põhinevad dimensioonid

1. Klõpsake PSA-s **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**.
2. Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Olemid**.
3. Klõpsake nuppu **Uus**, et luua uus olem nimega **Standardne pealkiri**. Sisestage ülejäänud nõutav teave ja seejärel klõpsake nuppu **Salvesta**.

> ![Standardse pealkirja olemi kirjeldus](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Suvandikomplektil põhinevad dimensioonid 
Saate luua kaks suvandikomplektil põhinevat dimensiooni. Kasutage suvandit **Ressursi töö asukoht**, et jälgida asukoha **Kodu** ja **Kohapeal** töö hinda ning kasutada suvandit **Ressursi töö aega** väärtustega **Regulaarne** ja **Ületunnitöö**, et rakendada rakendamiseks töö lõpetamisel märgistus.


1. Klõpsake PSA-s **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**. 
2. Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Suvandikomplektid**. 
3. Uue suvandikomplekti loomiseks klõpsake nuppu **Uus**, sisestage ülejäänud nõutav teave ja seejärel klõpsake nuppu **Salvesta**.

> ![Suvandikomplektil põhinev hinnakujunduse dimensioon nimega ressursi töö asukoht ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Suvandikomplektil põhinev hinnakujunduse dimensioon nimega ressursi töö tunnid ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Olemil põhinevate dimensioonide andmete loomine

Olemil põhinevate dimensioonide andmeid saate luua ka käsitsi, või kasutada rakenduse Microsoft Excel importimise või hoolduskõnede funktsiooni. Selle protseduuri etappide abil saate luua kaks standardset pealkirja, **Süsteemide insener** ja **Süsteemide vaneminsener** olemil põhinevast dimensioonist, **Standardne pealkiri**. Kui andmed, mida soovite luua, on väikesed, nagu järgmises näites, saate kasutada standardset vormi.

1. Klõpsake rakenduses PSA suvandit **Täpsem otsing**. Valige olem **Standardne pealkiri** ja klõpsake suvandit **Tulemused**. Kuvatakse kõik olemi **Standardne pealkiri** read.
2. Klõpsake nuppu **Uus**. Sisestage väljale **Nimi** suvand Süsteemi insener, ja klõpsake seejärel nuppu **Salvesta**.
3. Sulgege vorm. 
4. Korrake etappe 1–3, et luua teine standardne suvandile Süsteemi vaneminsener.

> ![Standardse jaotise olemi andmete Näidisandmete ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]