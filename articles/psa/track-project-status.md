---
title: Projekti oleku jälgimine
description: Projekti oleku jälgimine Project Service’is
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 58274886a9f9ce6ae49c64c1d7ac491e29c7d06c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593377"
---
# <a name="track-a-projects-status-project-service"></a>Projekti oleku jälgimine (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Kasutage funktsiooni [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] kliendi projekti edenemise jälgimiseks.  

Tegevuste edenedes värskendatakse projekti etappe, kajastades tegevuste etappi.  

| Toiming | Kirjeldus | 
|------------|----------|
| **New** | Projekti loomisel määratakse etapiks **Uus**. Kui lõite projekti mallist, võib projektil olla selles staadiumis ajakava hinnanguid ja meeskonnaandmeid. Vastasel korral on tegemist projekti struktuuriga ja ülejäänud projekti komponendid tuleb käsitsi sisestada. |
| **Hinnapakkumine** |  Kui seostate projekti hinnapakkumisega või loote selle hinnapakkumisest, seatakse projektietapiks **Hinnapakkumine** ning värskendatakse ka hinnangulisi algus- ja lõppkuupäevi. Kui projekt on hinnapakkumise staadiumis, kuvatakse hinnapakkumise üksikasjad vahekaardil **Müük** lehel **Projekt**. |
| **Plaan** |  Kui võidate projektiga seotud hinnapakkumise ja tegevused jõuavad lepingu etappi, määratakse projekti etapiks **Plaan**. Lepingu üksikasjad kuvatakse vahekaardil **Müük** lehel **Projekt**. |
| **Lõpule viidud** | Kui projekti töö on lõpetatud, saate määrata etapiks **Valmis**. Kui projekti etapiks on määratud Valmis, siis tähendab see, et töö on 100% valmis, kuid projekt hoitakse avatuna pooleliolevate aja- või kulukirjete registreerimiseks. |
| **Sule** | Kui kõik projekti toimingud on registreeritud ja neid pole enam vaja logida, võite märkida etapiks käsitsi **Sule**. Kui projekti olekuks on määratud **Sule**, ei saa logida projekti rohkem kandeid ja projekt on kirjutuskaitstud. |

## <a name="to-track-a-projects-status"></a>Projekti oleku jälgimine  

1.  Minge jaotisse **Project Service > Projektid**.  

2.  Klõpsake projekti, millega soovite töötada.  

3.  Valige kuva ülaosas asuvalt ribalt projekti nime kõrval olev allanool ja seejärel klõpsake suvandit **Projekti jälgimine**.  

4.  Valige ülesannete loendi kohal olevast rippmenüüst **Panuse jälgimine** või **Kulude jälgimine**.  

5.  Topeltklõpsake tööülesandel selle redigeerimiseks. Saate ka Gantti diagrammil tulpasid teisaldada või nende suurust muuta, et muuta ülesande aega ja edenemist.  

### <a name="see-also"></a>Vt ka  
 [Projektijuhi juhend](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
