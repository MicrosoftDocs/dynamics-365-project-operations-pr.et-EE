---
title: Valuuta mittevastavuse tõrge
description: Selles teemas leiate tõrkeotsinguteavet valuuta mittevastavuse tõrke kohta, mis ilmneb kindlate kirjetüüpide salvestamisel.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589743"
---
# <a name="currency-mismatch-error"></a>Valuuta mittevastavuse tõrge 

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Projekti, lepingu, hinnapakkumise või broneeritava ressursi salvestamisel võite saada tõrke, **ettevõtte valuuta omamine ei vasta lepinguühiku valuutale. Jätkamiseks valige mõni muu omamisettevõte või lepinguüksus**. Selle põhjuseks on asjaolu, et kirje lepinguühiku valuuta ja omava ettevõtte valuuta vahel on valuuta mittevastavus.


## <a name="resolution"></a>Lahendus

Selle probleemi lahendamiseks tehke järgmist.
- Kontrollige selle kirje lepinguüksuse valuutat. Valuuta kuvamiseks avage organisatsiooniüksuse kirje ja kontrollige väärtust välja Valuuta vahekaardil **Üldine** **.**
- Kontrollige omava ettevõtte valuutat. Valuutat saate vaadata, minnes ettevõttekirjes jaotisse **Seostuvad** > **pearaamatud**. Topeltklõpsake ettevõttega seostatud pearaamatukirjet ja kontrollige väärtust väljal Arvestusvaluuta vahekaardil **Üldine** **.**

Kui lepinguüksuses ja pearaamatukirjes seatud valuuta ei ühti, korrigeerige kirje salvestamisel konfiguratsiooni või valige erinevad väärtused. Süsteem nõuab, et need kirjed vastaksid, et tagada õiged kontsernisisesed arveldusvood. Kontsernisiseste konfiguratsioonide kohta leiate lisateavet teemast [Kontsernisiseste kannete](../../project-accounting/create-intercompany-transactions.md) loomine.

Kui ettevõttekirjel pole seostatud pearaamatukirjet, näitab see, et keskkonna seadistamisel puudub konfiguratsioon. Süsteemiadministraator peab konfiguratsiooni parandama. Süsteemiadministraator peab minema **dual-write konfiguratsioonidele** ning peatama ja taaskäivitama **Ledgersi topeltkirjutamise kaardi** selle kaardi algse sünkroonimise ja selle eeltingimustega. Lisateavet leiate teemast [Rakenduse Project Operations topeltkirjutamise vastenduse versioonid](../../environment/resource-dual-write-maps.md).
