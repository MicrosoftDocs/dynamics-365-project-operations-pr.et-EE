---
title: Üldine ressursinõude täitmine
description: Selles teemas antakse teavet üldise ressursi nõudega seotud nimega ressursside broneerimise kohta.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6bb7c185656ff87bb3ca24209594c07d25862d70
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074901"
---
# <a name="generic-resource-requirement-fulfillment"></a>Üldine ressursinõude täitmine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Nimega ressursi saate broneerida ressursi nõutava üldressursi asendamiseks.

1. Lehel **Projektid** valige vahekaart **Meeskond**.
2. Valige loendist pärineva ressursinõudega üldine ressurss ja valige seejärel **Broneeri**. Või avage ressursinõue ja valige seejärel **Broneeri**.
3. Valige lehel **Ajakava abimees** nimega ressurss, mille soovite oma projekti meeskonnale broneerida, seejärel klõpsake suvandit **Broneeri**.

Kui broneering on valmis ja täidetud nimega ressursi poolt, asendatakse üldine ressurss nimega ressurss.

Ajakavas olevad määrangud värskendatakse ka nimega ressursiga.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Üldise ressursi täitmine mitme nimega ressurssidega
Mitme nimega ressurssi sisaldava üldressursi nõude täitmine on sarnane ühe nimega ressursi määramisega. Näiteks on tööülesanne kestusega viis päeva ja 120 tundi pingutust. Seda tööülesannet ei saa lõpule viia üks ressurss, mis töötab viis päeva nädalas ja tavaliselt kaheksa tundi päevas. 

Nõue on 120 tundi robootika inseneri üle viie päeva, mis on 24 tundi päevas.

See on näide sellest, kui üldiste ressursside taotluse täitmiseks on vaja mitut nimega ressurssi. Nõude täitmiseks on vaja broneerida mitu ressurssi.

Peamine erinevus selle stsenaariumi puhul seisneb selles, et üldine ressurss jääb tööülesandele määratud meeskonnale ja broneeritud nimega ressursi meeskonnaliikmeid ei määrata positsiooni osana. Projektijuht saab määrata tööd vastavalt vajadusele nimega ressurssidele. Vaade **Sobitamine** võib aidata projektijuhti broneeringute jaotamisel üle mitmete ressursside vahel määrangute tegemisel. Seda ei tehta automaatselt, kuna mis tahes stsenaariumi korral, mis on keerulisem kui ülaltoodud lihtne näide, näiteks juhul, kui teil on nõude komplekt ülesandeid või peab süsteem eeldama, kuidas projektijuht soovib seda määrata. Kuna aga süsteem ei saa kavatsusest aru, siis need eeldused suure tõenäosusega erinevad sellest, mida tegelikult teha sooviti, ning seetõttu kuvatakse vale ja ettearvamatu tulemus. Prognoositav tulemus on, et üldine ressurss jääb alles, kuni projektijuht tahtlikult vaate **Sobitamine** abil määrangu loob.


