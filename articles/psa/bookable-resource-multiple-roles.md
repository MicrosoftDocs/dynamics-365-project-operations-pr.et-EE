---
title: Projekti müügi ja kulude prognoosimine juhul, kui broneeritav ressurss täidab projekti jaoks mitut rolli
description: Selles teemas antakse teavet selle kohta, kuidas hinnakujunduse dimensioone saab kasutada projekti mitut rolli täitva ressursi hinnakujunduse ja kulude toetuseks.
author: rumant
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
ms.openlocfilehash: be24bb3bdf2f3c8351fc396ae67457b5213e1cd800e9d2ad23d59d0d038f22b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987476"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Projekti müügi ja kulude prognoosimine juhul, kui broneeritav ressurss täidab projekti jaoks mitut rolli 

[!include [banner](../includes/psa-now-project-operations.md)]

Projektipõhistel ettevõtetel on sageli vaja, et üks ressurss täidaks projektis mitut rolli. Kõikide nende rollide hinna ja kulu saab määrata eraldi, mis tähendab, et iga rolli arveldus- ja kulumäärast olenevalt, võidakse samal ressursil projektile kulunud aega hinnata rahaliselt erinevalt. Rakendus Project Service Automation võimaldab meeskonnaliikme kirjel nimetatud ressursside väärtuste häälestamist ja võimaldab iga meeskonnaliikmele määratud ülesande puhul erinevaid alistamisi.

Järgmises näites on selgitatud, kuidas selle väärtuse lihtne alistamine võimaldab ressursil omada projektis mitut rolli koos erinevate kulu- ja arveldusmääraga.

## <a name="create-tasks"></a>Ülesannete loomine
Looge kaks projekti ülesannet (ülesanne A ja ülesanne B), kumbki 40 tundi. Valige ülesanne A ülesande B eelkäijaks.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Üldise projektimeeskonna liikme jaoks rolli ja organisatsiooni üksuse häälestamine

1. Valige lehel **Ajakava** ülesande A jaoks rida **Ülesanne**. 
2. Valige väljal **Ressursid** ripploendist suvand **Loo**.
3. Lejel **Meeskonnaliikme kiirloomine** määrake atribuudid üldisele meeskonnaliikmele, kes saab selle ülesande sooritada.
4. Valige sobiv roll ja organisatsiooniüksus, seejärel valige **Salvesta ja sule**. Luuakse üldine meeskonnaliige ja määratakse sellele ülesandele. 

Korrake neid samme ülesande B jaoks ja veenduge, et ülesande B jaoks loodud üldise meeskonnaliikme roll ja organisatsiooniüksus erineksid ülesande A omast. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Projekti ülesande jaoks rolli ja organisatsiooniüksuse häälestamine

1. Pärast ülesande A loomist valige ülesanne ja valige seejärel **Redigeeri ülesannet**.
2. Lehel **Ülesande üksikasjad** leidke väljad **Roll** ja **Organisastioooniüksus**, lisage väärtused, mis on nõutavad ressursilt, kes selle ülesande sooritab. 

  > [!NOTE]
  > Kui läbite selle stsenaariumi kasutades rakenduse Project Service Automation demoandmeid, valige rolliks **Konsulteeriv müügivihje** ja organisatsiooniüksuseks **Fabrikam US**.

3. Valige ülesanne B ja valige seejärel **Redigeeri ülesannet**.
4. Lehel **Ülesande üksikasjad** leidke väljad **Roll** ja **Organisastioooniüksus**, lisage väärtused, mis on nõutavad ressursilt, kes selle ülesande sooritab. Veenduge, et väärtused väljadel **Roll** ja **Organisatsiooniüksus** oleksid ülesande B puhul erinevad ülesande A väärtustest. 

  > [!NOTE]
  > Kui läbite selle stsenaariumi kasutades rakenduse Project Service Automation demoandmeid, valige rolliks **Võrgutehnik** ja organisatsiooniüksuseks **Fabrikam US**.

5. Salvestage ja sulgege leht **Ülesande üksikasjad**. 

## <a name="team-member-and-estimates-behavior"></a>Meeskonna liige ja prognoositav käitumine 

1. Lehel **Ülesande üksikasjad** suvandis **Meeskonnaliige** valige kaks üldist meeskonnaliiget ja valige seejärel **Loo nõuded**. 
2. Valige suvandi **Konsulteeriv müügivihje** jaoks meeskonnaliige ja valige seejärel **Broneeri**. Avaneb ajakavapaneel ja broneerib selle nõude jaoks ressursi.
3. Valige suvandi **Võrgutehnik** jaoks meeskonnaliige ja valige **Broneeri**. Avaneb ajakavapaneel ja broneerib selle nõude jaoks sama ressursi.

### <a name="team-member-grid"></a>Meeskonnaliikme ruudustik 
Pange tähele, et ruudustikus **Meeskonnaliige** on kaks üldist meeskonnaliikme kirjet kustutatud ja asendatud ühe ressursiga. Selle ressursi jaoks on üks väärtuste komplekt, mis kuvab väljade **Roll** ja **Organisatsiooniüksus** jaoks vaikimisi väärtuste komplekti.
Kui te selle meeskonnaliikme kirje rida laiendate, näete meeskonnaliikme kirjes mõlema selle ülesande jaoks eraldi määramist. Igal ülesandereal on väljade **Roll** ja **Organisatsiooniüksus** jaoks konkreetsed ülesande väärtused. 

### <a name="estimates-grid"></a>Prognooside ruudustik 
Kui te navigeerite ruudustikku **Prognoosid**, siis märkate, et sama ressursi mõlemad määramised on erineva hinnakirjaga.
Ülesande A ressursi määramise hind on tehtud kindlaks kasutades atribuudi **Roll** väärtust suvandist **Konsulteeriv müügivihje**. Ülesande B sama ressursi määramise hind on tehtud kindlaks kasutades atribuudi **Roll** väärtust suvandist **Võrgutehnik**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]