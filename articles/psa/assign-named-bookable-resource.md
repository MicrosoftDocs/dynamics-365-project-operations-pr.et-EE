---
title: Broneerige projekti meeskonnale nimega broneeritavad ressursid ja määrake ülesandeid
description: See teema pakub teavet projekti meeskondadele nimega ressursside broneerimise ja nende ülesannetele määramise kohta.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 0300c494a3294b26e2de6bbfa1dd50a76bb72651
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130168"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Broneerige projekti meeskonnale nimega broneeritavad ressursid ja määrake ülesandeid 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Saate lisada nimega ressursi oma projekti meeskonnale, kui broneerite neid otse meeskonnale. Selle tegemiseks tehke järgmist.

1. Avage rakenduses Project Service Automation suvand **Projektid**, ja valige selle projekti avamine, mille jaoks broneerite.
2. Klõpsake lehel **Projekt** vahekaardil **Meeskond** nuppu **Uus**. 

![Meeskonnaliikme lisamine meeskonna vahekaardi kaudu](media/RM-how-to-1.png)

3. Valige dialoogiboksis **Kiirloomine: projekti meeskonnaliige** broneeritav ressurss. Välja **Roll** täidetakse ressursi vaikerolliga, kui neil on selline määratud. Vajaduse korral saate rolli muuta. 
4. Valige ressursside vajalike kuupäevade algus- ja lõppkuupäevad ning valige ressursi võimsuse jaotamise meetod. 
5. Kui soovite, et meeskonnaliige oleks projekti kinnitaja, valige väljal **Projekti kinnitaja** suvand **Jah**. See tähendab, et meeskonnaliige saab kinnitada selle projekti jaoks esitatud aja- ja kulukirjeid. 
6. Klõpsake nuppu **Salvesta**.

![Meeskonnaliikme lisamine kiirloomise vormile](media/RM-how-to-2.png)


Nüüd saate projekti tööülesannetele määrata broneeritud ressursi. Klõpsake lehel **Projekt** vahekaarti **Ajakava**, et määrata tööülesanded uuele ressursile. Ressursivalijat, mis käivitatakse ülesande ruudustikus väljal **Ressursid**, kuvab meeskonnaliikmed, keda saate valida.

![Meeskonnaliikme määramine tööülesandele ajakava vahekaardil](media/RM-how-to-3.png)

Rakenduse Project Service Automation (PSA) versioonis 3 pole ressursi broneerimised ja määrangud tihedalt ühendatud. See tähendab, et kui kasutate ressursivalijat ajakavas, saate meeskonnaliikmetele määrata rohkem tööülesanded kui nende broneeringud projektis katavad.
Meeskonnaliikmete broneerimiste ja määrangute vahelisi erinevusi saate vaadata vahekaardilt **Meeskond** või vahekaardilt **Ressursi sobitamine**. Samuti saate sobitada erinevused ressursside broneeringute ja määrangute vahel üksikasjalikumal tasemel.

![Ressursi sobitamise vahekaart](media/RM-how-to-4.png)

Vahekaardil **Ajakava** saate kasutada ka ressursivalijat, et otsida ja valida broneeritavaid ressursse, mis pole juba projekti meeskonna osa. Need kuvatakse ressursivalijas suvandina **Muud ressursid**.

![Meeskonnavälise liikme ressursi määramine ülesandele](media/RM-how-to-5.png)

Kui te seda teete, lisatakse ressurss projekti meeskonda ja määratakse tööülesandele, kuid broneeringuid ei looda.

![Meeskonnaliige määrangute ja broneeringutega](media/RM-how-to-6.png)

Ressursi võimsuse broneerimiseks projektile saate kasutada vahekaardi **Sobitamine** pikendatud broneerimise võimalust või vahekaarti **Ajakava**.

![Meeskonnaliikme broneeringu pikendamine ressursi sobitamise vahekaardil](media/RM-how-to-7.png)

Pärast seda, kui meeskonnaliige on teie projektile broneeritud, saate broneeringuid säilitada või kasutada graafikut otse, et hallata oma broneeringuid.
