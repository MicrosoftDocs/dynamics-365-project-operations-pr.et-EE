---
title: Ostke mittelaopõhiseid materjale või hankekategooriaid ooteloleva hankija arve abil
description: See artikkel kirjeldab, kuidas kirjendada ootel hankija arveid.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921987"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Ostke mittelaopõhiseid materjale või hankekategooriaid ooteloleva hankija arve abil

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Kuna ettevõttes kasutatakse projekti jaoks mittelaopõhiseid materjale või hankekategooriaid, saab kulud kohe projekti kohta kirjendada. 

Näiteks töötab ettevõte Contoso Robotics US vahendite uuendamise projekti kallal ja vajab tarkvaralitsentse. Need litsentsid on pärit kolmandalt osapoolelt.  Rakenduse Dynamics 365 Finance kasutamisel fikseerib Ostureskontro ametnik ootel oleva hankija arve dokumendi ja omistab litsentsikulud otse seadmete uuendamise projektile. 

> [!IMPORTANT]
> Enne selles artiklis kirjeldatud funktsioonide kasutamist vaadake üle ja rakendage nõutavad konfiguratsioonid. Lisateabe saamiseks vaadake jaotisi [Varustamata materjalide ja ootel hankijaarvete lubamine](configure-materials-nonstocked.md) ja [Hankekategooriate kasutamine projekti ostutellimuste ja ootel hankija arvetega](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Projektiga seotud ootel hankija arve postitamine 

Ootel hankija arved saab registreerida lehel **Ootel tarnija arved** (**Ostureskontro** > **Arved** > **Ootel hankijate arved**). Projektiga seotud ootel hankija arve postitamiseks tehke järgmist.

1. Minge jaotisesse **Ostureskontro** > **Arved** ja valige **Uus**. 
1. Valige väljal **Arve konto** soovitud tarnija ja seejärel sisestage väljal **Number** hankija arve ID.
1. Lisage rida hankija arvele ja seejärel valige väljal **Üksuse number** hankijalt ostetud mittelaopõhine üksus. Teise võimalusena valige väljal **Hankekategooria** hankijalt ostetud hankekategooria.   
1. Lisage ostetud kogus. Süsteem täidab ühikuhinna, lähtudes mittelaopõhise kauba hinna konfiguratsioonist. 
1. Kontrollige real kogusummat ja muid nõutud üksikasju.
1. Valige rea üksikasjade vahekaardis **Projekt** selle projekti ID, kus see üksus registreeritakse.
1. Valikuline: valige tegevuse number ning värskendage projekti kategooriat ja rea atribuuti.
1. Postitage ootel hankija arve. Kui arve on postitatud, salvestab süsteem järgmise teabe.
    
    - Hankija saldosumma.
    - Käibemaksu summa.
    - Projektiga seotud kulud kirjendatakse hanke integreerimise kontole.
    - Projekti tegeliku kulu tehing teenuses Dataverse.  Seda tehingut töödeldakse edasi, kasutades [Project Operationsi integreerimise töölehte](../project-accounting/project-operations-integration-journal.md). Selle töölehe sisestamine teisaldab summa hanke integreerimise kontolt projekti kulu kontole. 
    - Ostud, mille eest arved esitatakse projekti kliendile aja- ja materjalide arveldusmeetodit kasutades. Lisaks luuakse teenuses Dataverse ostude jaoks arveldamata müügitehingud. Teenuse Dataverse toodete hinnakirja kasutatakse arveldamata müügitehingute müügihindade ja summade jaoks.
