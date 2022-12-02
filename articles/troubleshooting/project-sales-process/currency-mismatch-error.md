---
title: Valuuta mittevastavuse tõrge
description: See artikkel annab teavet tõrkeotsingu kohta seoses vääringu mittevastavuse tõrkega, mis ilmneb teatud kirjetüüpide salvestamisel.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914719"
---
# <a name="currency-mismatch-error"></a>Valuuta mittevastavuse tõrge 

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

'Kui salvestate projekti, lepingu, hinnapakkumise või broneeritava ressursi, võidakse kuvada tõrketeade **Ettevõtte omamise valuuta ei ühti lepinguühiku valuutaga. Jätkamiseks valige teine omanikfirma või lepinguline ühik**. Selle põhjuseks on asjaolu, et kirje lepingulise ühiku valuuta ja omava ettevõtte valuuta vahel on valuuta mittevastavus.


## <a name="resolution"></a>Lahendus

Selle probleemi lahendamiseks tehke järgmist.
- Kontrollige selle kirje lepingulise ühiku valuutat. Valuutat saate näha, avades organisatsiooniühiku kirje ja kontrollides väärtust vahekaardil **Üldine** väljal **Valuuta**.
- Kontrollige omanikettevõtte valuutat. Valuutat näete, minnes ettevõtte kirjes jaotisse **Seotud** > **Pearaamatud**. Topeltklõpsake ettevõttega seotud pearaamatu kirjet ja kontrollige väärtust vahekaardil **Üldine** väljal **Arvestusvaluuta**.

Kui lepinguühiku ja pearaamatu kirjes määratud valuuta ei ühti, kohandage kirje salvestamisel konfiguratsiooni või valige erinevad väärtused. Süsteem nõuab, et need kirjed ühtiksid, et tagada korrektsed kontsernivahelised arveldusvood. Lisateavet kontsernivaheliste konfiguratsioonide kohta leiate jaotisest [Kontsernivaheliste tehingute loomine](../../project-accounting/create-intercompany-transactions.md).

Kui ettevõtte kirjel pole seotud pearaamatu kirjet, näitab see, et keskkonna seadistamisel on puudu konfiguratsioon. Süsteemiadministraator peab konfiguratsiooni parandama. Süsteemiadministraator peab minema jaotisse **Topeltkirjutuse konfiguratsioonid** ning peatama ja taaskäivitama **Pearaamatu topeltkirjutuskaart** selle kaardi esialgse sünkroonimise ja selle eeltingimustega. Lisateavet leiate teemast [Rakenduse Project Operations topeltkirjutamise vastenduse versioonid](../../environment/resource-dual-write-maps.md).
