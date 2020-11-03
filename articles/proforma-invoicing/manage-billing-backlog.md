---
title: Arvete võlgnevuste haldamine
description: Selles teemas antakse teavet, kuidas Project Operationsis arvete võlgnevusi vaadata ja nendega töötada.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec77f3911a460b96414a61bc44ea254f1b7da660
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087885"
---
# <a name="manage-the-billing-backlog"></a>Arvete võlgnevuste haldamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operationsis on kaks püsivat vaadet, mis aitavad teil arvete võlgnevustega töötada ja neid hallata. Need on **Fikseeritud hinna vahe-eesmärgid** ja **Ajakavast mahajäämus ja materjali arvete võlgnevused**. Vaate valimiseks Project Operationsi alal **Müük** valige vasakpoolsel navigeerimise lehel suvand **Arveldamine**. Arvete võlgnevuste lingid salvestatakse sinna.

## <a name="fixed-price-milestones"></a>Fikseeritud hinna vahe-eesmärgid

Selles vaates loetletakse süsteemi projekti lepinguridade kõik fikseeritud hinna vahe-eesmärgid. Ühe- või mitmekordseid vahe-eesmärke saab selles vaates märgistada kui **Arveldamiseks valmis** või **Pole arveldamiseks valmis**. Kui märgite vahe-eesmärgi väärtuseks **Arveldamiseks valmis** , siis on vahe-eesmärk arve mustandi jaoks saadaval.

Kui mitme kliendiga lepinguridadel on fikseeritud hinnaga arveldusmeetod, luuakse iga lepingurea kliendi jaoks üks vahe-eesmärk. Kasutaja loob vahe-eesmärgi ja see vahe-eesmärk jaotatakse klientide vahel = konkreetsed vahe-eesmärgi kirjed ettevõttesiseselt, vastavalt iga lepingurea kliendi jaoks määratletud arveldusprotsendile. Vaates **Fikseeritud hinna vahe-eesmärgid** kuvatakse erinevad kliendiga seotud vahe-eesmärgi kirjed. Kõik need vahe-eesmärgi kirjed saab märkida kui **Arveldamiseks valmis** , sellest vaatest eraldi. Kui üks või mitu seotud vahe-eesmärgi jaotust märgitakse kui **Arveldamiseks valmis** , muutub päise olek olekust **Pole alustatud** olekuks  **Pooleli**. Kui kõik vahe-eesmärgi jaotused on arveldatud, muutub päise vahe-eesmärgi olekuks **Lõpetatud**.

Selles vaates kuvatakse arve mustandi vahe-eesmärk, mille arvelduse olek on **Kliendi arve on loodud**. Kui arve mustand kinnitatakse, muutub selle kirje arveldamise olekuks **Arve sisestatud**. Selle oleku väärtuse värskendamist kohandatud koodi abil ei soovitata. Projekt Operations ei tööta õigesti, kui oleku väärtused on värskendatud kohandatud koodiga.

## <a name="time-and-material-billing-backlog"></a>Ajakavast mahajäämus ja materjali arvete võlgnevused

Selles vaates loetletakse kõik arveldamata müügi tegelikud näitajad, mida pole kõigis süsteemi projekti lepingutes arveldatud. Ühe- või mitmekordseid arveldamata müügi tegelikke näitajaid saab selles vaates märgistada kui **Arveldamiseks valmis** või **Pole arveldamiseks valmis**. Arveldamata müügi tegeliku näitaja märgistamine kui **Arveldamiseks valmis** muudab selle kättesaadavaks arve mustandina esitamiseks.

Arveldamata müügi tegelikud näitajad, mille oleku **Mitteületatav** väärtust **Ebaõnnestus** ei saa märkida kui **Arveldamiseks valmis**. Kui need tegelikud näitajad peavad olema tähistatud sellisena, lähtestage olekuks määratud lepingurea tegelikud näitajad ja seejärel hinnake olekud **Mitteületatav**.

Mitme kliendiga lepinguridade korral, millel on aja- ja materjalikulu arveldusmeetod, mil aeg ja kulud kinnitatakse, luuakse iga lepingurea jaoks iga kliendi kohta eraldi arveldatud müügi tegelik näitaja, mis on määratletud lepingurea iga kliendi jaoks määratletud arveldusprotsendi alusel. Vaates **Aja- ja materjalikulu arvete võlgnevused** näete üksikuid kliendipõhiseid arveldamata müügi tegelikke näitajaid. Kõik need arveldamata müügi tegelike näitajate kirjed saab märkida kui **Arveldamiseks valmis** , sellest vaatest eraldi.

Selles vaates kuvatakse arve mustandi arveldamata müügi tegelik näitaja, mille väli **Arvelduse olek** on **Kliendi arve on loodud**. Kui arve mustand kinnitatakse, muutub selle kirje arveldamise olekuks **Kliendi arve on sisestatud**. Selle oleku väärtuse värskendamist, kui see on selles olekus, kohandatud koodi abil ei soovitata. Projekt Operations ei tööta õigesti, kui oleku väärtused on värskendatud kohandatud koodiga.
