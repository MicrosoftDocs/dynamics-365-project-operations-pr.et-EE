---
title: Projekti ressursside ajastamine
description: Projekti ressursside ajastamine Project Service'is
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4935567d-9318-4f7c-9c02-c584a78b7841
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9767e324b3caec4b5f9723347537dbe97ea34fb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751038"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Projekti ressursside ajastamine (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Saate kontrollida ressursi kättesaadavust, et näha ülevaadet oma ressursside reserveeritusest, või filtreerida vaadet oskuste, meeskonna, asukoha ja muude valikute järgi.  
  
Ajakavapaneelil kuvatakse ressursside loend ja nende saadavus. Valige saadavust ajavahemikus **Tunnid**, **Päev**, **Nädal** või **Kuu** kuvav vaaterežiim.  
  
Enne ajakavapaneeli kasutamist peate selle seadistama. Lisainfo saamiseks, vt jaotist [Ajakavapaneeli konfigureerimine (Field Service või Project Service Automation)](../field-service/configure-schedule-board.md).
  
Kui kasutate vanemat versiooni, uurige ressursside saadavaloleku kohta teabe saamiseks artiklit [Ressursi saadavuse vaatamine](../project-service/view-resource-availability.md).  

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
 [Ressursihalduri juhend](../project-service/resource-manager-guide.md)
