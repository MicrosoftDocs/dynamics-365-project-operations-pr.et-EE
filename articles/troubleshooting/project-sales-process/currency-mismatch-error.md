---
title: Valuuta mittevastavuse tõrge
description: Selles teemas on tõrkeotsinguteave valuuta mittevastavuse tõrke kohta, mis ilmneb kindlate kirjetüüpide salvestamisel.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903652"
---
# <a name="currency-mismatch-error"></a>Valuuta mittevastavuse tõrge 

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Projekti, lepingu, pakkumise või broneeritava ressursi salvestamisel võite saada tõrke, **ettevõtte valuuta omamine ei vasta lepinguühiku valuutale. Jätkamiseks valige erinev omamisettevõte või lepinguüksus**. Seda seetõttu, et kirje lepinguühiku valuuta ja omava ettevõtte valuuta vahel on valuuta mittevastavus.


## <a name="resolution"></a>Lahendus

Selle probleemi lahendamiseks tehke järgmist.
- Kontrollige selle kirje lepinguüksuse valuutat. Valuutat saate vaadata, avades organisatsiooniüksuse kirje ja kontrollides väärtust **välja** Valuuta vahekaardil **Üldine**.
- Kontrollige omava ettevõtte valuutat. Valuutat saate vaadata, minnes **ettevõtte kirjesse Seotud** > **pearaamatud**. Topeltklõpsake ettevõttega seotud pearaamatukirjet ja kontrollige väärtust **väljal** Arvestusvaluuta vahekaardil **Üldine**.

Kui lepinguüksuses ja pearaamatukirjes määratud valuuta ei ühti, reguleerige kirje salvestamisel konfiguratsiooni või valige erinevad väärtused. Süsteem nõuab nende kirjete sobitamist, et tagada korrektsed kontsernisisesed arveldusvood. Kontsernisiseste konfiguratsioonide kohta leiate lisateavet teemast [Kontsernisiseste kannete loomine](../../project-accounting/create-intercompany-transactions.md).

Kui ettevõttekirjel pole seostatud pearaamatukirjet, näitab see, et keskkonna seadistamisel puudub konfiguratsioon. Süsteemiadministraator peab konfiguratsiooni parandama. Süsteemiadministraator peab minema **kahe kirjaga konfiguratsioonidele** ning peatama ja taaskäivitama **pearaamatute topeltkirjutamise kaardi** selle kaardi algse sünkroonimisega ja selle eeltingimustega. Lisateavet leiate teemast [Rakenduse Project Operations topeltkirjutamise vastenduse versioonid](../../environment/resource-dual-write-maps.md).
