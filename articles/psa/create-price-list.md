---
title: Hinnakirja loomine
description: Hinnakirja loomine Project Service'is
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bf75286fd1837e27a9b6053ccb21b60771ee197d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074992"
---
# <a name="create-a-price-list-project-service"></a>Hinnakirja loomine (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Hinnakirjad annavad malli, mille abil saavad teie kontohaldurid luua hinnapakkumisi ja projekte ning teha kindlaks projekti kulusid. Need pakuvad reaüksuse rollide ja kulude loendi ning igaühe hinna. Saate luua mitu hinnakirja, et hallata erinevate müügipiirkondade või müügikanalite puhul eraldi hinnastruktuure. Arukas on luua vähemalt üks hinnakiri iga valuuta kohta, milles kavatsete oma klientidele arveid esitada.  
  
Edastatava töö finantsprognooside loomiseks veenduge, et igal projektil oleks aluseks olev kulu- ja müügihinnakiri. Seadistage kulu ja müügi vaikehinnakiri, mis kehtib kõigi teie organisatsioonis loodud projektide puhul.  
  
Hinnakirjad tuginevad rollidele ja kulukategooriatele, seega enne hinnakirja loomist veenduge, et oleksite konfigureerinud rollid ja kulukategooriad, mida soovite hinnakirja loomise kasutada.  
  
1.  Minge jaotisse **Project Service > Hinnakirjad**.  
  
2.  Klõpsake nuppu **Uus**.  
  
3.  Valige jaotises **Kontekst** , kas hinnakirja tüüp on **Kulu** , **Ost** või **Müük**.  
  
4.  Sisestage väljale **Nimi** hinnakirja nimi.  
  
5.  Valige väljal **Valuuta** arveldamiseks või omahinna arvutamiseks kasutatav valuuta.  
  
6.  Määrake väljal **Ajaühik** hinna kehtimise ajaperiood, nagu päev või tund.  
  
7.  Vajaduse korral täitke väljad **Alguskuupäev** , **Lõppkuupäev** ja **Kirjeldus**.  
  
8.  Klõpsake kirje loomiseks käsku **Salvesta** , seejärel saate selle redigeerimist jätkata.  
  
9. Hinnakirjale rollihinna lisamiseks klõpsake jaotises **Rollihinnad** nuppu **+**.  
  
10. Sisestage üksikasjad paanil **Rolli hind** ja seejärel klõpsake käsku **Salvesta**. Jätkake rollihindade lisamisega vajadust mööda. Kui olete lõpetanud, klõpsake kuva paremas alanurgas käsku **Salvesta**.  
  
11. Hinnakirjale kulukategooria lisamiseks klõpsake jaotises **Kategooriahinnad** nuppu **+**.  
  
12. Sisestage üksikasjad paanil **Tehingukategooria hind** ja seejärel klõpsake käsku **Salvesta**. Jätkake kategooriahindade lisamisega vajadust mööda. Kui olete lõpetanud, klõpsake kuva paremas alanurgas käsku **Salvesta**.  
  
13. Hinnakirjale hinnakirjaüksuste lisamiseks klõpsake jaotises **Hinnakirjaüksused** nuppu **+**.  
  
14. Sisestage üksikasjad paanil **Hinnakirjaüksus** ja seejärel klõpsake käsku **Salvesta**. Jätkake hinnakirjaüksuste lisamisega vajadust mööda. Kui olete lõpetanud, klõpsake kuva paremas alanurgas käsku **Salvesta**.  
  
15. Hinnakirjale piirkonnaseoste lisamiseks klõpsake jaotises **Piirkonnaseosed** nuppu **+**.  
  
16. Sisestage üksikasjad aknas **Uus ühendus** ja seejärel klõpsake käsku **Salvesta**. Jätkake piirkonnaseoste lisamisega vajadust mööda. Kui olete lõpetanud, klõpsake kuva paremas alanurgas käsku **Salvesta**.  
  
### <a name="see-also"></a>Vt ka  
 [Project Service Automation konfigureerimine](../psa/configure.md)