---
title: Projekti ressursside ajastamine
description: Projekti ressursside ajastamine Project Service'is
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 7beb1f86795a909a1266b2a2c97421e1f04ef3c4cf2f9b49413cd1382b0f2011
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998141"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Projekti ressursside ajastamine (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Saate kontrollida ressursi kättesaadavust, et näha ülevaadet oma ressursside reserveeritusest, või filtreerida vaadet oskuste, meeskonna, asukoha ja muude valikute järgi.  
  
Ajakavapaneelil kuvatakse ressursside loend ja nende saadavus. Valige saadavust ajavahemikus **Tunnid**, **Päev**, **Nädal** või **Kuu** kuvav vaaterežiim.  
  
Enne ajakavapaneeli kasutamist peate selle seadistama. Lisainfo saamiseks, vt jaotist [Ajakavapaneeli konfigureerimine (Field Service või Project Service Automation)](/dynamics365/field-service/configure-schedule-board).
  
Kui kasutate vanemat versiooni, uurige ressursside saadavaloleku kohta teabe saamiseks artiklit [Ressursi saadavuse vaatamine](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Kui soovite kasutada ajakavapaneeli broneerimise funktsioone, geokodeerimist ja asukohateenuseid, peate sisse lülitama kaartide kasutamise.  
> 
> 1. Valige põhimenüüs suvandid **Ressursiplaanimine** > **Haldus**.  
> 2. Klõpsake valikut **Ajastamise parameetrid**.  
> 3. Avage kirje ja kerige jaotiseni **Resource Scheduling Optimization**.  
> 4. Väljal **Ühenda kaartidega** valige **Jah**.  
> 5. Nõustuge tingimustega ja salvestage kirje.  
> 6. Valige peamenüüst **Project Service** > **Ajakavapaneel**. Broneeringunõude käsitsi ajastamiseks on siin mitu võimalust. Valige meetod, mis teile sobib.
  
## <a name="find-available-resources"></a>Saadaolevate ressursside leidmine

1.  Loendis **Broneerimise nõuded** paremklõpsake plaanimata broneeringut ja valige üks järgmistest valikutest.  
  
- Ajakavapaneelil olevast loendist saadaoleva ressursi leidmiseks valige **Otsi kättesaadavust – praegused ressursid**.  
- Süsteemis olevatest ressurssidest saadaoleva ressursi leidmiseks valige **Otsi kättesaadavust – kõik ressursid**.  
   > [!NOTE]
   >  Kui toimite eelkirjeldatud viisil, kuvavad filtrid valitud broneeringunõude kohta valikuid.  
  
2. Kui näete vaba vahemikku, paremklõpsake plaanimistahvlil ajavahemikku ja valige nupp **Broneeri siin**. Võite ka broneeringunõude vabale ajavahemikule lohistada.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Ressursi broneerimine päevavaate abil ja vaatamine, kes on alabroneeritud
  
1.  Ajakavapaneelil valige **Vaaterežiim** ja valige **Päevad**.  
  
    Kuvatakse tabel, millest on näha, mitu tundi päevas on ressurss broneeritud ja millistel päevadel on see vaba.  
  
2.  Ressursi broneerimiseks klõpsake ressursi nime ja seejärel valige **Broneeri**.  
  
3.  Valige dialoogiboksist **Ressursi broneerimine (loo)** lisaks projektile, mille jaoks soovite ressurssi broneerida, ka broneerimismeetod ja algus- ja lõppkellaajad.  
  
4.  Kui olete lõpetanud, valige suvand **Broneeri**.  
  
## <a name="view-to-the-schedule-board"></a>Ajakavapaneeli vaade
  
1.  Valige ajastamata broneeringunõue allpool asuvast loendist.  
  
2.  Lohistage broneeringunõue ajakavapaneelil saadaoleva ressursi/aja lahtrisse.  
  
3.  Kui olete lõpetanud, valige suvand **Broneeri**.  
  
### <a name="additional-resources"></a>Lisaressursid  
 [Ressursihalduri juhend](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]