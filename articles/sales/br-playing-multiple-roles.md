---
title: Projekti müügi ja kulude hindamine, kui broneeritav ressurss täidab projekti jaoks mitu rolli
description: Selles teemas kirjeldatakse, kuidas kasutada hinnakujunduse dimensioone, et toetada hinna ja omahinna arvutamist, mis on seotud projektile mitme rolli täitva ressursiga.
author: rumant
manager: tfehr
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f01c9c6adfeedc11fcb04a7e8b8f5a55e5f8dc79
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278818"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Projekti müügi ja kulude hindamine, kui broneeritav ressurss täidab projekti jaoks mitu rolli 

_**Kehtib järgmiste puhul:** Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks, lihtjuurutus – tehing näidisarveldusele, Project Operations ressursi-/tootmispõhiste stsenaariumite jaoks_ 

Projektil põhinevad ettevõtted vajavad sageli ühte ressurssi, et täita projekti jaoks mitut rolli. Iga rolli saab hinnata ja maksta erinevalt. See tähendab, et sama ressursi aeg projektis võib anda erineva finantskalkulatsiooni olenevalt iga rolli arvest ja omahinna määradest. Nimetatud ressursi meeskonnaliikme kirjele saate seadistada väärtused, millel on erinevad alistused iga ülesande jaoks, millele meeskonnaliige on määratud.

Järgnevast näitest näete, kuidas väärtuse lihtne alistamine võimaldab ressursile mitut projektirolli, millel on erinevad kulud ja arve määrad.

## <a name="create-tasks"></a>Ülesannete loomine
Tööülesannete loomiseks tuleb lisada tööülesanded ja kokkuvõtvad tööülesanded ning pärast seda peate tööülesande määrama, et lisada sellele kestus. 

### <a name="add-tasks-and-summary-tasks"></a>Tööülesannete ja kokkuvõtte tööülesannete lisamine
Tööülesande lisamiseks tehke järgmist.

1. Minge jaotisse **Projektid** ja avage projekt, kuhu soovite tööülesanded lisada.
2. Valige **Lisa uus tööülesanne**. Nimetage tööülesanne ja vajutage seejärel sisestusklahvi **Enter**.
3. Sisestage veel üks tööülesanne ja vajutage seejärel sisestusklahvi **Enter**. Korrake seda toimingut seni, kuni teil on täielik tööülesannete loend.
3. Tööülesannete taandamiseks valige jaotises **Kokkuvõte** kolm vertikaalset punkti tööülesande nime juures ja seejärel käsk **Tee alamülesanne**. 

  > [!TIP]
  > Mitme tööülesande valimiseks valige tööülesanne, vajutage ja hoidke all klahvi **Ctrl** ning valige seejärel mõni muu tööülesanne.
  >
  > Soovi korral saate valida ka **Ülenda alamülesanne**, et tööülesanded jaotisest **Kokkuvõte** teisaldada.

### <a name="assign-tasks"></a>Määratud ülesanded

Ülesannete määramiseks tehke järgmist.

1. Valige tööülesande veerus **Määratud:** isiku ikoon.
2. Valige loendist meeskonnaliige või sisestage otsitav nimi.

### <a name="add-task-duration-and-columns"></a>Tööülesande kestuse ja veergude lisamine

Oma projekti loomisel on sageli kõige lihtsam alustada kestusest. Tööülesande kestuse lisamiseks tehke järgmist.

1. Tippige tööülesande veerus **Kestus** päevade arv, mis on teie arvates toimingu täitmiseks vaja. Kui soovite kasutada mõnda muud ajaühikut, sisestage number pluss sõna **tunnid**, **nädalad** või **kuud**.
2. Kui soovite, et teie tööülesanne kuvataks **ajajoone** vaates teemandikujuline verstapostina, sisestage veerus **kestus** väärtuseks **0 päeva**.
3. Vajutage sisestusklahvi **Enter**, et liikuda järgmise tööülesande väärtuse **Kestus** juurde ja jätkata kestuste sisestamist.

  > [!NOTE]
  > Kokkuvõtvate tööülesannete kestust ei saa sisestada.

Saate lisada oma projektile veerge, et esitada rohkem üksikasju. Selleks valige **Lisa veerg**. 

Lisateavet vt teemast [Projekti loomine](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Üldise projekti meeskonnaliikme rolli ja organisatsiooniüksuse seadistamine
Järgige allolevaid juhiseid, et luua üldmeeskonna liikme roll ja organisatsiooniüksus.

1. Valige lehel **Tööülesanded** rida **Tööülesanne** valiku **Ülesanne A** jaoks. 
2. Valige jaotises **Määratud:** **Lisa üldine ressurss**. See avab lehe **Meeskonnaliikmete kiirloomine**.
3. Lejel **Meeskonnaliikme kiirloomine** määrake atribuudid üldisele meeskonnaliikmele, kes saab selle ülesande sooritada.
4. Valige sobiv roll ja organisatsiooniüksus, seejärel valige **Salvesta ja sule**. Luuakse üldine meeskonnaliige ja määratakse sellele ülesandele. 
5. Korrake samme 1–4 **Tööülesande B** jaoks. **Tööülesanne B** peab aga olema erineva rolliga ja erinev organisatsiooniüksus kui üldmeeskonna liikmele määratud **Tööülesanne A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Projekti tööülesande rolli ja organisatsiooniüksuse seadistamine
Järgige allolevaid samme, et luua tööülesande jaoks roll ja organisatsiooniüksus.

1. Pärast **Tööülesande A** loomist valige tööülesanne ja seejärel ikoon **i**, et avada paan **Tööülesande üksikasjad**. 
2. Kerige paanil **Tööülesande üksikasjad** ja valige **Kuva üksikasjad**, et avada leht **Tööülesande üksikasjad**.
3. Lisage lehel **Tööülesande üksikasjad** väärtused **Roll** ja **Organisatsiooniüksus**, mis on vajalikud selle ressursi jaoks toimingu sooritamiseks. 

  > [!NOTE]
  > Kui täidate selle stsenaariumi Project Operationsi demoandmete abil, valige rolli jaoks väärtus **Konsulteeriv müügivihje** ja organisatsiooniüksuseks **Fabrikam US**.

4. Valige **Tööülesanne B** ja seejärel tööülesanne.
5. Valige ikoon **i** paani **Tööülesande üksikasjad** avamiseks. 
6. Kerige paanil **Tööülesande üksikasjad** ja valige **Kuva üksikasjad**, et avada leht **Tööülesande üksikasjad**.
7. Lisage lehel **Tööülesande üksikasjad** väärtused **Roll** ja **Organisatsiooniüksus**, mis on vajalikud toimingut sooritava ressursi jaoks. Väärtused **Roll** ja **Organisatsiooniüksus** ülesande **Tööülesanne B** jaoks peavad erinema nendest, mis on määratud **Tööülesandele A**. 

  > [!NOTE]
  > Kui täidate selle stsenaariumi Project Operationsi demoandmete abil, valige rolliks **Võrgutehnik** ja organisatsiooniüksuseks **Fabrikam US**.

8. Salvestage ja sulgege leht **Ülesande üksikasjad**. 

## <a name="team-member-and-estimates-behavior"></a>Meeskonna liige ja prognoositav käitumine 
Ruudustiku **Meeskonna liige** ja prognoositava käitumise mõistmiseks tehke järgmist.

1. Valige ruudustikus **Meeskonnaliige** kaks üldmeeskonna liiget ja seejärel **Loo nõuded**. See loob ressursinõuded. 
2. Valige suvandi **Konsulteeriv müügivihje** jaoks meeskonnaliikme rida ja valige seejärel **Broneeri**. Ajakava paneel avaneb koos ressursside loendiga. Valige ressurss ja seejärel **Broneeri**, et ressurssi sellele nõudele broneerida.
3. Valige suvandi **Võrgutehnik** jaoks meeskonnaliikme rida ja seejärel **Broneeri**. Ajakava paneel avaneb koos ressursside loendiga. Valige sama ressurss nagu ülal ja seejärel **Broneeri**, et ressurssi sellele nõudele broneerida.

### <a name="team-member-grid"></a>Meeskonnaliikme ruudustik 

Ruudustikus **Meeskonnaliikmed** kustutatakse kaks üldmeeskonnaliikme kirjet ja need asendatakse ainult ühe ressursiga. Selle ressursi jaoks on olemas üks väärtuste hulk, mis on seatud atribuutide **Roll** ja **Organisatsiooniüksus** vaikeväärtuste hulgaks.

Kui laiendate selle meeskonnaliikme kirje rida, näete mõlema tööülesande jaoks meeskonnaliikme kirjes erinevaid ülesandeid. Igal ülesandereal on väljade **Roll** ja **Organisatsiooniüksus** jaoks konkreetsed ülesande väärtused. 

### <a name="estimates-grid"></a>Prognooside ruudustik 

Ruudustikus **Prognoosid** hinnatakse sama ressursi määramist erinevalt. **Ülesande A** ressursi määramise hind on tehtud kindlaks, kasutades atribuudi **Roll** väärtust suvandist **Konsulteeriv müügivihje**. **Ülesande B** sama ressursi määramise hind on tehtud kindlaks, kasutades atribuudi **Roll** väärtust suvandist **Võrgutehnik**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]