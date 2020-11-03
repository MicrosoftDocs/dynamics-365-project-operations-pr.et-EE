---
title: Müügiprognoosid ja projektid
description: See teema pakub teavet selle kohta, kuidas müügiprotsessis ajakava ja prognoose ära kasutada.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: eafe60362003198a223026526f56261de414bb4a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074974"
---
# <a name="sales-estimates-and-projects"></a>Müügiprognoosid ja projektid

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Müügiprotsessi käigus saate luua müügiprognoose, kui seostate projekti müügipakkumisega. Sel viisil saab müügiprotsessi ajal toimuda kindel prognoos, et saaksite ära kasutada projekti ajastamise ja prognoosimise võimalusi. Kui müük toimub, saab müügiprognoosi eesmärkidel kasutatud ajakava kasutada projektiplaani edasiseks täiustamiseks.

## <a name="linking-a-project-to-a-quote-line"></a>Projekti linkimine hinnapakkumise reaga

Projektipõhise hinnapakkumise rea loomisel saate luua uue projekti või seostada olemasoleva projekti lehel **Hinnapakkumise rida**. 

> ![Hinnapakkumise rea vorm](media/project-8.png)
 
Kui loote hinnapakkumise rea üksikasjadest uue projekti, võite ära kasutada projekti malle. Projektimallid on mudelprojektid, mis esindavad standardseid projektiplaane ja organisatsioonile tüüpilisi finantskalkulatsioone. Need võivad esindada ka projektiplaanide koopiaid ja varasemate projektide prognoose.

> ![Hinnapakkumise rea üksikasjad](media/project-9.png)
  
Kui loote hinnapakkumisest projekti, seostatakse projekt automaatselt hinnapakkumise reaga.

## <a name="components-of-estimates-in-a-project"></a>Projekti prognooside komponendid

Ajakava abil saate töö jaotada ülesanneteks, hallata ülesannete hierarhiat, otsustada, milliseid ressursse on ülesande lõpule viimiseks vaja ja määrata ülesande lõpule viimiseks vajaliku panuse prognoosi.

Saate määrata töökoormuse ja ajastada prognoose, kui kasutate lehe **Projekt** vahekaardil **Ajakava** olevaid välju. Kuna hinnakiri on projektiga seotud, arvutatakse finantskalkulatsioonid hinnakirjas määratletud omahindade ja müügihindade alusel.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Prognooside importimine projektist hinnapakkumisse

Pärast projekti prognooside määramist saate need importida hinnapakkumise reale. Projekti prognooside summeerimiseks kande tüübi, rolli või ülesande taseme järgi tehke lehe **Hinnapakkumise rea üksikasjad** ribal valik **Impordi prognoosidest**.