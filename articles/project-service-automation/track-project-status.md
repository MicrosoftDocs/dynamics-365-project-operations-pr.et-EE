---
title: Projekti oleku jälgimine
description: Projekti oleku jälgimine Project Service’is
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7610aecb-318c-422b-b626-9106b0736b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e4d53b6235c3b941bce525dca09ee3d647c3d242
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751036"
---
# <a name="track-a-projects-status-project-service"></a>Projekti oleku jälgimine (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Kasutage funktsiooni [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] kliendi projekti edenemise jälgimiseks.  

Tegevuste edenedes värskendatakse projekti etappe, kajastades tegevuste etappi.  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Uus**    | Projekti loomisel määratakse etapiks **Uus**. Kui lõite projekti mallist, võib projektil olla selles staadiumis ajakava hinnanguid ja meeskonnaandmeid. Vastasel korral on tegemist projekti struktuuriga ja ülejäänud projekti komponendid tuleb käsitsi sisestada. |
|  **Hinnapakkumine**   |      Kui seostate projekti hinnapakkumisega või loote selle hinnapakkumise põhjal, määratakse projekti etapiks **Hinnapakkumine** ning värskendatakse ka eeldatavaid algus- ja lõppkuupäevi. Kui projekt on hinnapakkumise staadiumis, kuvatakse hinnapakkumise üksikasjad vahekaardil **Müük** lehel **Projekt**.      |
|   **Plaan**   |                                     Kui võidate projektiga seotud hinnapakkumise ja tegevused jõuavad lepingu etappi, määratakse projekti etapiks **Plaan**. Lepingu üksikasjad kuvatakse vahekaardil **Müük** lehel **Projekt**.                                      |
| **Lõpule viidud** |                    Kui projekti töö on lõpetatud, saate määrata etapiks **Valmis**. Kui projekti etapiks on määratud Valmis, siis tähendab see, et töö on 100% valmis, kuid projekt hoitakse avatuna pooleliolevate aja- või kulukirjete registreerimiseks.                     |
|  **Sule**   |           Kui kõik projekti toimingud on registreeritud ja neid pole enam vaja logida, võite märkida etapiks käsitsi **Sule**. Kui projekti olekuks on määratud **Sule**, ei saa logida projekti rohkem kandeid ja projekt on kirjutuskaitstud.           |

## <a name="to-track-a-projects-status"></a>Projekti oleku jälgimine  

1.  Minge jaotisse **Project Service > Projektid**.  

2.  Klõpsake projekti, millega soovite töötada.  

3.  Valige kuva ülaosas asuvalt ribalt projekti nime kõrval olev allanool ja seejärel klõpsake suvandit **Projekti jälgimine**.  

4.  Valige ülesannete loendi kohal olevast rippmenüüst **Panuse jälgimine** või **Kulude jälgimine**.  

5.  Topeltklõpsake tööülesandel selle redigeerimiseks. Saate ka Gantti diagrammil tulpasid teisaldada või nende suurust muuta, et muuta ülesande aega ja edenemist.  

### <a name="see-also"></a>Vt ka  
 [Projektijuhi juhend](../project-service/project-manager-guide.md)
