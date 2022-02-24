---
title: Arveldatava ressursikasutuse vaatamine
description: Selles teemas antakse teavet ressursi kasutamise vaate kohta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e1c123854209b3cb5c310e3bbcb242c9219279a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992829"
---
# <a name="view-chargeable-utilization-for-resources"></a>Arveldatava ressursikasutuse vaatamine

[!include [banner](../includes/psa-now-project-operations.md)]
 
Vaates **Kasutamise vaade** lehel **Project Service ressursi kasutamine** kuvatakse tasustatav kasutamine iga broneeritava ressursi kohta. Vaade põhineb ajakavapaneelil, nii et leiate sellelt mitmeid sarnaseid funktsioone.

> ![Kasutusvaate kuvatõmmis](media/FAQ-utilization-1.png)
 

Arveldatava kasutuse arvutamine toimib järgmiselt.

   Arveldatav kasutus = (arveldatavad tegelikud tunnid) / (ressursi koormus)

Lahtrites on toodud vaate valitud perioodi (päevade, nädalate või kuude) arvutatud arveldatav kasutus.

Iga lahtri värvid näitavad ressursi arveldatavat kasutust võrreldes nende arveldatava kasutuse eesmärgiga. 

Kasutuse eesmärgi saab seada kas ressursi vaikerollis või üksikressursis. Arvutamisel vaadatakse kõigepealt üksikressurssi ja seejärel alles ressursi vaikerolli.

## <a name="set-target-on-a-resource"></a>Ressursi sihi seadmine

1. Avage **Ressursid** \> **Ressursid**. 
2. Seejärel valige kirje avamiseks ressurss. 
3. Vahekaardil **Project Service** saate seada ressursi kasutamise eesmärgi.

> ![Kuvatõmmis kasutuse eesmärgi seadmisest vahekaardil Project Service](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Kasutamise eesmärgi seadmine rollile

1. Avage **Ressursid** \> **Ressursirollid**. 
2. Valige roll ja avage kirje. 
3. Seadke rollile kasutuse eesmärk.

> ![Kuvatõmmis kasutuse eesmärgi seadmisest ressursirollides](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Arveldatava ressursikasutuse arvutamine

Selleks et arvutada ressursi arveldatavat kasutust, peate täitma mõne eeltingimuse. 

### <a name="set-default-role-for-individual-resource"></a>Üksikute ressursside vaikerolli seadmine

Esiteks, tuleb üksikressursis või ressursirollides määrata kasutuse eesmärk. Kui kasutate eesmärkide seadmiseks ressursirolle, peab igal üksikressursil olema vaikeroll. 

1. Selle määramiseks avage **Ressursid** \> **Ressursid**. 
2. Valige ressurss, avage kirje ja seejärel valige vahekaart **Project Service**. 
3. Veenduge, et **ressursi rolli** ruudustikus on ressursi jaoks üks roll ja **Vaikimisi** seatakse suvandi väärtuseks **Jah**.
 
### <a name="change-billing-type-for-resource-role"></a>Ressursirolli arveldustüübi vahetamine

Ressursirollidele peab olema määratud arveldustüübiks **Arveldatav**. 

1. Avage **Ressursid** \> **Ressursirollid**. 
2. Avage kirje, mida soovite värskendada ja määrake seejärel vaikearveldustüübiks **Arveldatav**.

### <a name="set-working-hours-for-resource-role"></a>Ressursirollile töötundide määramine
 
Koormuse arvutamiseks peavad ressursil olema määratud töötunnid. 

1. Avage **Ressursid** \> **Ressursid**. 
2. Valige kirje avamiseks ressurss ja seejärel valige **Kuva töötunnid**. 
3. Saate ressursside loendit hulgivärskendada, kui rakendate vaatest **Ressursiloend** vaatest **töötundide malli**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Tasustatava tegeliku tööaja tõrkeotsing

Tegelikud arveldatavad tunnid pärinevad olemist **Tegelikud näitajad**. Arvutusse kaasatakse tegelikult näitajad arveldustüübiga **Arveldatav** ja seepärast peavad teie projektide tegelikud näitajad olema arveldatavad.

Kui te ei näe arveldatavat kasutust, kontrollige järgmist.

- Ressursi koormuse jaoks on töötunnid määratud.
- Ressursil on kas üksikult määratud kasutuse eesmärk või talle on määratud vaikeroll. Rollile on määratud kasutuse eesmärk.
- Tegelike näitajate arveldustüübiks on kasutusarvutuse tegemise ajavahemikul määratud **Arveldatav**. Kui näete tegelikke näitajaid, millel on mõni muu arveldustüüp kui arveldatav, siis kontrollige järgmist.

  - Tegelikus näitajas kasutatud rollil on vaikearveldustüübiks seatud muu tüüp kui arveldatav.
  - Projekti varundav projekti lepingurea roll on määratud mittearveldatavaks.
  - Projektil pole seostatud lepingurida.



[!INCLUDE[footer-include](../includes/footer-banner.md)]