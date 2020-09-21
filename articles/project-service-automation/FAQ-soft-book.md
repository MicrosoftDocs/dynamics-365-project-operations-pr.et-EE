---
title: Ressursi esialgne reserveerimine
description: Selles teemas kirjeldatakse, kuidas projekti meeskonna liikmeid ajastada või esialgselt reserveerida.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.prod: Applies to Project Service version 3.x
ms.technology: ''
ms.assetid: 04e02ff7-1024-4b65-a281-6f149921b63d
ms.author: ruhercul
audience: Admin
ms.openlocfilehash: 07e768d756732e31df82a9865b957dae09c60821
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750931"
---
# <a name="soft-book-a-resource"></a>Ressursi esialgne reserveerimine

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Saate ressurssi esialgselt projektimeeskonda reserveerida, andmaks teada, et planeerite ressursi projekti määrata. Esialgselt reserveerimised ei lisa ressursile koormust ja teil on võimalik esialgselt reserveeritud meeskonnaliikmeid projekti ülesandeid täitma määrata. Kuna esialgselt reserveerimine ei lisa ressursile koormust, saate ressursile endiselt samasse perioodi muid kindlaid ülesandeid määrata. Üldisi ressursse pole võimalik esialgselt reserveerida, samuti ei täida esialgselt reserveerimine üldise ressursi taotlust.

Esialgselt reserveeritud meeskonnaliikmed on loetletud lehel **Projekt** vahekaardil **Meeskond**, kus vaate **Nimega meeskonnaliikmed** veerus **Esialgselt reserveeritud tunnid** on näha nende esialgselt reserveeritud tunnid. Esialgselt reserveeritud meeskonnaliikmed on toodud ka ajakavapaneelil. Kuna nad on reserveeritud esialgselt, ei näidata ajakavapaneelil nende ressursside koormust. Esialgselt reserveeritud aega ei kuvata vahekaardil **Vastavusseviimine** ega ajakavapaneeli vahekaardi **Vastavusseviimine** väljal **Pikenda broneeringuid**. 

Meeskonnaliikme esialgseks reserveerimiseks on kaks võimalust: otse ajakavapaneelil või lisades meeskonnaliikmeid vahekaardil **Meeskond**. 

## <a name="soft-book-from-the-schedule-board"></a>Esialgselt reserveerimine ajakavapaneelil
Ressursi esialgseks reserveerimiseks ajakavapaneelil tehke järgmised etapid. 

1. Avage ajakavapaneel ja seejärel valige paneelil **Broneeringu nõuded** vahekaart **Projekt**.
2. Leidke projekt, millele soovite ressursi esialgselt reserveerida. Kui loendis on suur hulk projekte, valige veerupäis **Projekt** ja seejärel kasutage filtrit ühe või mitme projekti otsimiseks.
3. Klõpsake projekti ja lohistage see ressursi ajaruudustikku.
5. Kohandage paneelil **Ressursi reserveeringu loomine** algus- ja lõppkuupäeva, määrake **Broneeringu olek** **Esialgseks** ja seadke tunnid. 
6. Klõpsake valikut **Broneeri**. Ressurss kuvatakse nüüd vahekaardil **Meeskond** projekti ressursina. Esialgselt reserveeritud tunde saate vaadata vaate **Nimega meeskonnaliige** veerus **Esialgselt reserveeritud tunnid**.

> [!NOTE]
> Pange tähele, et saate nüüd esialgselt reserveeritud ressurssidele vahekaardil **Ajakava** ülesandeid määrata. Kuna vahekaardil **Vastavusseviimine** arvestatakse ainult fikseeritud **reserveerimisi**, kuvatakse seal ressursi ülesandega seotult broneeringu puudujääk. Saate ressursi määramiste fikseeritud reserveerimiste puudujäägi kõrvaldada, kui reserveerite ressurssi fikseeritult funktsiooniga **Pikenda broneeringut**. Peate ressursi esialgselt reserveerimise jaotises **Reserveeringute haldamine** käsitsi tühistama.

## <a name="soft-book-on-the-team-tab"></a>Esialgselt reserveerimine vahekaardil Meeskond

Saate vahekaardil **Meeskond** meeskonnaliikmeid otse lisada ja seejärel jaotises **Reserveeringute haldamine** nende reserveerimisolekut **Fikseeritult** **Esialgseks** muuta. Kui lisate meeskonnaliikme sel viisil, tehakse alati fikseeritud reserveerimine, ka siis kui valite eraldusmeetodiks **Puudub**.

Selle meetodiga reserveerimiseks tehke järgmist.

1. Klõpsake lehel **Projekt** vahekaardil **Meeskond** nuppu **Uus**.
2. Valige reserveeritav ressurss, roll, algus- ja lõppkuupäev.
3. Valige mis tahes eraldusmeetod peale valiku **Puudub**.
4. Valige **Salvesta**. Näete ressurssi ruudustikus ja tema tunde veerus **Fikseeritult reserveeritud tunnid**.
5. Valige ressursi reserveerimiste haldamiseks **Reserveeringute haldamine**.
6. Kui ajakavapaneel avatakse, laiendage ressurssi nende reserveerimiste vaatamiseks. Reserveerimine kuvatakse olekuga **Fikseeritud**.
7. Paremklõpsake reserveerimist ja valige jaotises **Oleku muutmine**, **Esialgselt reserveerimine** \> **Esialgne**. Nüüd on broneeringu olek **Esialgne**.
8. Pärast ajakavapaneeli sulgemist näete, et ressursile määratud tunnid on viidud veerust **Fikseeritult reserveeritud tunnid** veergu **Esialgselt reserveeritud tunnid** vahekaardi **Meeskond** ruudustikus, kui vaadata vaadet **Nimega meeskonnaliikmed**.

> [!NOTE]
> Kui kasutate valikut **Reserveeringute haldamine** oleku muutmiseks **Fikseeritult** **Esialgsele**, kui reserveerite ressursi fikseeritult meeskonda ja määrate talle ajakavas ülesandeid, jäetakse ressursile määratud ülesanded alles. Kuid vahekaardil **Vastavusseviimine** on ressursil broneeringu puudujääk, kuna broneeringute ja määramiste vastavusseviimisel arvestatakse ainult fikseeritud reserveerimisi. Saate ressursi määramiste fikseeritud reserveerimiste puudujäägi kõrvaldada, kui reserveerite ressursi fikseeritult vahekaardil **Vastavusseviimine** funktsiooniga **Pikenda broneeringut**. Peate ressursi esialgselt reserveerimise jaotises **Reserveeringute haldamine** tühistama.

Kui olete valmis esialgselt reserveeritud meeskonnaliikme ressursi kindlaks meeskonnaliikmeks määrama, tehke järgmist.

1. Laiendage ressursi broneeringute vaatamiseks ajakavapaneelil ressurssi. Reserveerimine kuvatakse olekuga **Esialgne**.
2. Paremklõpsake reserveerimist ja valige jaotises **Oleku muutmine**, valige **Fikseeritult reserveerimine** \> **Fikseeritud**. Nüüd on broneeringu olek **Fikseeritud**.
3. Kui vaatate vaadet **Nimega meeskonnaliikmed** pärast ajakavapaneeli sulgemist ja projekti naasmist ning vahekaardi **Meeskond** avamist, siis näete, et ressursile määratud tunnid on viidud veerust **Esialgselt reserveeritud tunnid** veergu **Fikseeritult reserveeritud tunnid** vahekaardil **Meeskond**. Kui ressursile määrati ülesandeid, ei kuvata enam broneeringu puudujääki vahekaardil **Vastavusseviimine**, kuna reserveerimised on nüüd fikseeritud.

