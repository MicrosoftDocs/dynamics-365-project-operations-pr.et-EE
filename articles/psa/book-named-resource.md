---
title: Broneeri nimega ressursid ressursinõuetest
description: Selles teemas antakse teavet üldise ressursi nõudega seotud nimega ressursside broneerimise kohta.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: e929a5fb4c307d3b64d0f7f70203fe20bc6dd4f99e89e039fae0ce8276c69c52
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000481"
---
# <a name="book-named-resources-from-resource-requirements"></a>Broneeri nimega ressursid ressursinõuetest

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nimega ressursi saate broneerida ressursi nõutava üldressursi asendamiseks.

1. Klõpsake rakenduses Project Service Automation (PSA) lehel **Projektid** vahekaarti **Meeskond**.
2. Valige loendist ressursinõudega üldine ressurss ja klõpsake seejärel suvandit **Broneeri**. Või avage ressursinõue ja seejärel klõpsake suvandit **Broneeri**.


![Üldise meeskonnaliikme broneerimine.](media/RM-how-to-14.png)


3. Valige lehel **Ajastamise abimees** nimega ressurss, mille soovite oma projekti meeskonnale broneerida, seejärel klõpsake suvandit **Broneeri**.

![Üldise meeskonnaliikme broneerimine ajakavaabilise abil.](media/RM-how-to-15.png)

Kui broneering on valmis ja täidetud nimega ressursi poolt, asendatakse üldine ressurss nimega ressurss.

![Üldise meeskonnaliikme asendamine nimega meeskonnaliikmega.](media/RM-how-to-16.png)

Ajakavas olevad määrangud värskendatakse ka nimega ressursiga.

![Projekti tööülesannetele määratud nimega meeskonnaliige.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Üldise ressursi täitmine mitme nimega ressurssidega
Mitme nimega ressurssi sisaldava üldressursi nõude täitmine on sarnane ühe nimega ressursi määramisega. Näiteks on tööülesanne kestusega viis päeva ja 120 tundi pingutust. Seda tööülesannet ei saa lõpule viia üks ressurss, mis töötab viis päeva nädalas tüüpilise 8-tunnise päevaga. 

![Toiming, mis vajab 5 päeva jooksul 120 tundi pingutust.](media/RM-how-to-21.png)

Nõue on 120 tundi robootika inseneri üle viie päeva, mis on 24 tundi päevas.

![Päevane nõue.](media/RM-how-to-22.png)

See on näide sellest, kui üldiste ressursside taotluse täitmiseks on vaja mitut nimega ressurssi. Nõude täitmiseks on vaja broneerida mitu ressurssi.

![Mitme ressursi broneerimine nõude täitmiseks.](media/RM-how-to-23.png)

Peamine erinevus selle stsenaariumi puhul seisneb selles, et üldine ressurss jääb tööülesandele määratud meeskonnale ja broneeritud nimega ressursi meeskonnaliikmeid ei määrata positsiooni osana. Projektijuht saab määrata tööd vastavalt vajadusele nimega ressurssidele. Vaade **Sobitamine** võib aidata projektijuhti broneeringute jaotamisel üle mitmete ressursside vahel määrangute tegemisel. Seda ei tehta automaatselt, kuna mis tahes stsenaariumi korral, mis on keerulisem kui ülaltoodud lihtne näide, näiteks juhul, kui teil on nõude komplekt ülesandeid, peab süsteem eeldama, kuidas projektijuht soovib seda määrata. Kuna süsteem ei saa kavatsusest aru, on võimalik, et eeldused on teistsugused kui ette nähtud ja juhtub vale või ettearvamatu tulemus. Prognoositav tulemus on, et üldine ressurss jääb alles, kuni projektijuht tahtlikult vaate **Sobitamine** abil määrangu loob.




[!INCLUDE[footer-include](../includes/footer-banner.md)]