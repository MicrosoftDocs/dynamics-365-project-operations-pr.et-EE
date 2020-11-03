---
title: Kohandatud väljade ja olemite loomine hinnakujunduse dimensioonidena
description: Selles teemas antakse teavet, kuidas luua kohandatud suvandikomplekte või olemeid.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074994"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Kohandatud väljade ja olemite loomine hinnakujunduse dimensioonidena

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Läbige järgmised etapid iga kord, kui soovite luua kohandatud suvandikomplekt või olemi.

> [!IMPORTANT]
> Soovitame teil teha kõik kohandatud hinnakujunduse dimensiooni muudatused eraldi lahenduses. See oluline hea tava annab tulevikus paindlikkuse muudatuste värskendamiseks või eemaldamiseks vastavalt vajadusele, aitab teie tööd uuesti kasutada ja muudab nende muudatuste teisaldamise teistele eksemplaridele hõlpsamaks. Kui olete kõik vajalikud muudatused teinud, eksportige see lahendus kui **Hallatud lahendus** ja importige see muudesse eksemplaridesse, et saaksite oma hinnakujunduse seadistust uuesti kasutada.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Kohandatud lahenduse loomine hinnakujunduse dimensioonide jaoks
1. Avage **Sätted** > **Lahendused** ja seejärel uue lahenduse loomiseks valige **Uus**. 
2. Pange lahendusele nimi **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid** , sisestage ülejäänud nõutav teave ja valige seejärel **Salvesta**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Kohandatud väljade ja suvandikomplekti loomine hinnakujunduse dimensiooni lahenduses

Hinnakujunduse dimensioon võib olla suvandikomplekt või olem. Mõlemad tuleb luua hinnakujunduse lahenduses. Selle protseduuri etapid selgitavad, kuidas luua olemil ja suvandikomplektil põhinevaid dimensioone.

### <a name="entity-based-dimensions"></a>Olemil põhinevad dimensioonid

1. Avage **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**.
2. Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Olemid**.
3. Valige **Uus** , et luua uus olem nimega **Standardne pealkiri**. 
4. Sisestage ülejäänud nõutav teave ja calige seejärel **Salvesta**.


### <a name="option-set-based-dimensions"></a>Suvandikomplektil põhinevad dimensioonid 
Saate luua kaks suvandikomplektil põhinevat dimensiooni. Kasutage suvandit **Ressursi töö asukoht** , et jälgida asukoha **Kodu** ja **Kohapeal** töö hinda ning kasutada suvandit **Ressursi töö aega** väärtustega **Regulaarne** ja **Ületunnitöö** , et rakendada rakendamiseks töö lõpetamisel märgistus.


1. Avage **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**. 
2. Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Suvandikomplektid**. 
3. Uue suvandikomplekti loomiseks valige **Uus** , sisestage ülejäänud nõutav teave ja valige seejärel **Salvesta**.

## <a name="create-data-for-entity-based-dimensions"></a>Olemil põhinevate dimensioonide andmete loomine

Olemil põhinevate dimensioonide andmeid saate luua ka käsitsi, või kasutada rakenduse Microsoft Excel importimise või hoolduskõnede funktsiooni. Selle protseduuri etappide abil saate luua kaks standardset pealkirja, **Süsteemide insener** ja **Süsteemide vaneminsener** olemil põhinevast dimensioonist, **Standardne pealkiri**. Kui andmed, mida soovite luua, on väikesed, nagu järgmises näites, saate kasutada standardset vormi.

1. Valige **Täpsem otsing** , valige olem **Standardpealkiri** ja valige seejärel **Tulemid**. Kuvatakse kõik olemi **Standardne pealkiri** read.
2. Valige **Uus** ja väljale **Nmi** sisestafe Süsteemi insener ja valige seejärel **Salvesta**.
3. Sulgege vorm. 
4. Korrake etappe 1–3, et luua teine standardne suvandile Süsteemi vaneminsener.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Lisage kõik nõutavad olemid ja seotud komponendid hinnakujunduse dimensiooni lahendusse
Hinnakujunduse lahendusele tuleb lisada järgmised olemid. Kasutage selle protseduuri etappe, et muuta hinnakujunduse lahenduses teatud olulisi skeeme, et olemid oleksid uutest hinnakujunduse dimensioonidest teadlikud.

1. Valige **Sätted** > **Lahendused** ja topeltklõpsake suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**. 
2. Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvandid **Lisa olemasolev** > **Olemid**.
3. Valige dialoogiboksis **Lahenduse komponendid** järgmised olemid.

  - Tegelik
  - Broneeritav ressurss
  - Prognoosi rida
  - Arve rea üksikasjad
  - Töölehe rida
  - Projekti lepingurea üksikasjad
  - Projektimeeskonna liige
  - Hinnapakkumisrea üksikasi
  - Rolli hinna hinnalisand
  - Rolli hind 
  - Ajakirje 


> [!NOTE]
> Veenduge, et kõigi valitud olemite jaoks kaasatakse kõik vormid ja vaated.

4. Kui teil palutakse kaasata eespool valitud olemite jaoks kõik sõltuvaid olemeid, valige **Ei**.

