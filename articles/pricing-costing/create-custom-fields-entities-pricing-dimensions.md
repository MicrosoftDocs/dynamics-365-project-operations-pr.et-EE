---
title: Kohandatud väljade ja olemite loomine hinnakujunduse dimensioonidena
description: Selles teemas antakse teavet, kuidas luua kohandatud suvandikomplekte või olemeid.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4912087d7a19f5f342beff94723acd6131ce2dd8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580681"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Kohandatud väljade ja olemite loomine hinnakujunduse dimensioonidena

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Läbige järgmised etapid, kui soovite luua kohandatud suvandikomplekti või olemit, et kasutada seda hinnakujunduse dimensioonina. Lisateabe saamiseks vt [Hinnakujunduse dimensioonide ülevaade](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Soovitame teil teha kõik kohandatud hinnakujunduse dimensiooni muudatused eraldi lahenduses. See oluline hea tava annab tulevikus paindlikkuse, et vajaduse korral saaks teha uuendusi või eemaldada muudatusi. See aitab teie tööd ka uuesti kasutada ja muudab pärast kõigi nõutavate muudatuste tegemist lihtsamaks nende muudatuste portimise teise eksemplari, eksportige see lahendus kui **Hallatav lahendus** ja importige see muudesse eksemplaridesse, et saaksite oma hinnakujunduse seadistust uuesti kasutada.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Kohandatud väljade ja suvandikomplekti loomine hinnakujunduse dimensiooni lahenduses

Hinnakujunduse dimensioon võib olla suvandikomplekt või olem. Mõlemad tuleb luua hinnakujunduse lahenduses. Selle protseduuri etapid selgitavad, kuidas luua olemil ja suvandikomplektil põhinevaid dimensioone.

### <a name="entity-based-dimensions"></a>Olemil põhinevad dimensioonid
Olemil põhinevate dimensioonide loomiseks toimige järgmiselt.

1. Avage **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**.
2. Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Olemid**.
3. Valige **Uus**, et luua uus olem nimega **Standardne pealkiri**. 
4. Sisestage ülejäänud nõutav teave ja calige seejärel **Salvesta**.

> ![Olemi Standardne pealkiri määratlus.](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Suvandikomplektil põhinevad dimensioonid 
Saate luua kaks suvandikomplektil põhinevat dimensiooni. 

- Kasutage **Ressursi töö asukohta**, et jälgida asukohaga **Kodu** töö ja asukohaga **Kohapealne** töö hinda. 
- Kasutage suvandit **Ressursi tööaeg** koos väärtustega **Regulaarne** ja **Ületunnitöö**, et rakendada töö lõpetamisel hinnalisandit.

Järgmine graafiline vaade sisaldab dimensiooni **Ressursi tööasukoht**. 

> ![Suvandikomplektil põhinev hinnakujunduse dimensioon nimega Ressursi tööasukoht.](media/Option-set-PD-called-Resource-Work-Location.png)

Järgmine graafiline vaade sisaldab dimensiooni **Ressursi töötunnid**. 

> ![Suvandikomplektil põhinev hinnakujunduse dimensioon nimega Ressursi töötunnid.](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Avage **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**. 
2. Valige rakenduses Solution Explorer vasakul navigeerimispaanil **Suvandikomplektid**. 
3. Uue suvandikomplekti loomiseks valige **Uus**, sisestage ülejäänud nõutav teave ja valige seejärel **Salvesta**.

## <a name="create-data-for-entity-based-dimensions"></a>Olemil põhinevate dimensioonide andmete loomine

Olemil põhinevate dimensioonide andmeid saate luua ka käsitsi, või kasutada rakenduse Microsoft Excel importimise või hoolduskõnede funktsiooni. Selle protseduuri etappide abil saate luua kaks standardset pealkirja, **Süsteemide insener** ja **Süsteemide vaneminsener** olemil põhinevast dimensioonist, **Standardne pealkiri**. Kui andmed, mida soovite luua, on väikesed, nagu järgmises näites, saate kasutada standardset vormi.

1. Valige **Täpsem otsing**.
2. Valige olem **Standardne pealkiri** ja seejärel **Tulemused**. Kuvatakse kõik olemi **Standardne pealkiri** read.
3. Valige **Uus** ja väljale **Nmi** sisestafe Süsteemi insener ja valige seejärel **Salvesta**.
4. Sulgege leht. 
5. Korrake etappe 1–3, et luua teine standardne suvandile Süsteemi vaneminsener.

> ![Näidisandmed olemi Standardne pealkiri jaoks.](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]