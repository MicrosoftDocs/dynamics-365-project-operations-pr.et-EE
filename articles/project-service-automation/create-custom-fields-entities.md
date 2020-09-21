---
title: Kohandatud väljade ja olemite loomine
description: Selles teemas kirjeldatakse, kuidas luua suvandikomplekte ja olemeid oma platvormi Power Apps lahenduses.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751030"
---
# <a name="create-custom-fields-and-entities"></a>Kohandatud väljade ja olemite loomine 

Läbige järgmised etapid iga kord, kui soovite luua kohandatud suvandikomplekt või olemi platvormil Power Apps.  
Selles teemas kirjeldatud protseduurid tuleb lõpule viia, kasutades rakenduse Project Service Automation (PSA) veebiliidest.

> [!IMPORTANT]
> Soovitame teil teha kõik kohandatud hinnakujunduse dimensiooni muudatused eraldi lahenduses. See oluline hea tava annab tulevikus paindlikkuse muudatuste värskendamiseks või eemaldamiseks vastavalt vajadusele, aitab teie tööd uuesti kasutada ja muudab nende muudatuste teisaldamise teistele eksemplaridele hõlpsamaks. Kui olete kõik vajalikud muudatused teinud, eksportige see lahendus kui **Hallatud lahendus** ja importige see muudesse eksemplaridesse, et saaksite oma hinnakujunduse seadistust uuesti kasutada.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Kohandatud lahenduse loomine hinnakujunduse dimensioonide jaoks
1. Klõpsake rakenduses PSA nuppu **Sätted** > **Lahendused**, ja seejärel uue lahenduse loomiseks nuppu **Uus**. 
2. Sisestage lahenduse nimi, **\<teie organisatsiooni nimi > hinnakujunduse dimensioonid**, sisestage ülejäänud nõutav teave ja klõpsake siis nuppu **Salvesta**.

> ![Kohandatud lahenduse loomine hinnakujunduse dimensioonide jaoks](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Kohandatud väljade ja suvandikomplekti loomine hinnakujunduse dimensiooni lahenduses

Hinnakujunduse dimensioon võib olla suvandikomplekt või olem. Mõlemad tuleb luua hinnakujunduse lahenduses. Selle protseduuri etapid selgitavad, kuidas luua olemil ja suvandikomplektil põhinevaid dimensioone.

### <a name="entity-based-dimensions"></a>Olemil põhinevad dimensioonid

1. Klõpsake PSA-s valikuid **Sätted** > **Lahendused** ja seejärel topeltklõpsake **\<oma organisatsiooni nime > hinnakujunduse dimensioone**.
2. Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Olemid**.
3. Klõpsake nuppu **Uus**, et luua uus olem nimega **Standardne pealkiri**. Sisestage ülejäänud nõutav teave ja seejärel klõpsake nuppu **Salvesta**.

> ![Standardse pealkirja olemi kirjeldus](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Suvandikomplektil põhinevad dimensioonid 
Saate luua kaks suvandikomplektil põhinevat dimensiooni. Kasutage suvandit **Ressursi töö asukoht**, et jälgida asukoha **Kodu** ja **Kohapeal** töö hinda ning kasutada suvandit **Ressursi töö aega** väärtustega **Regulaarne** ja **Ületunnitöö**, et rakendada rakendamiseks töö lõpetamisel märgistus.


1. Klõpsake rakenduses PSA nuppu **Sätted** > **Lahendused**, ja seejärel topeltklõpsake **\<teie organisatsiooni nimi > hinnakujunduse dimensioonid**. 
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

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Lisage kõik nõutavad PSA olemid ja seotud komponendid hinnakujunduse dimensiooni lahendusse
Hinnakujunduse lahendusele tuleb lisada järgmised Project Service’i olemid. Kasutage selle protseduuri etappe, et muuta hinnakujunduse lahenduses teatud olulisi skeeme, et olemid oleksid uutest hinnakujunduse dimensioonidest teadlikud.

1. Klõpsake PSA-s valikuid **Sätted** > **Lahendused** ja seejärel topeltklõpsake **\<oma organisatsiooni nime > hinnakujunduse dimensioone**. 
2. Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvandid **Lisa olemasolev** > **Olemid**.
3. Valige dialoogiboksis **Lahenduse komponendid** järgmised olemid.

- Tegelik
- Broneeritav ressurss
- Prognoosi rida
- Arve rea üksikasjad
- Töölehe rida
- Projekti lepingurea üksikasjad
- Projektimeeskonna liige
- Hinnapakkumise rea üksikasi
- Rolli hinna hinnalisand
- Rolli hind 
- Ajakirje 

> ![Olemasolevate olemite lisamine hinnakujunduse dimensioonide lahendusse](media/Existing-entities-to-PD-solution.png)

> ![Lahenduse komponentide valimine](media/Dimension-Components.png)

> [!NOTE]
> Veenduge, et kõigi valitud olemite jaoks kaasatakse kõik vormid ja vaated.

4. Kui teil palutakse kaasata eespool valitud olemite jaoks kõik sõltuvaid olemeid, klõpsake nuppu **Ei**.

> ![Ära kaasa kõiki seotud komponente](media/Do-not-include-required.png)


