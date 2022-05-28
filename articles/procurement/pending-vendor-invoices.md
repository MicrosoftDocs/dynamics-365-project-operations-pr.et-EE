---
title: Ladustamata materjalide või hankekategooriate ostmine ootel hankija arve abil
description: Selles teemas kirjeldatakse, kuidas kirjendada ootel hankija arveid.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612652"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Ladustamata materjalide või hankekategooriate ostmine ootel hankija arve abil

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Kuna ettevõte hangib projekti jaoks ladustamata materjale või hankekategooriaid, saab kulud kohe projekti suhtes kirjendada. 

Näiteks töötab ettevõte Contoso Robotics US vahendite uuendamise projekti kallal ja vajab tarkvaralitsentse. Need litsentsid on pärit kolmandalt osapoolelt.  Kasutades Dynamics 365 Finance, salvestab ostureskontro sekretär ootel hankija arve dokumendi ja omistab litsentsikulud otse seadmete uuendamise projekti vastu. 

> [!IMPORTANT]
> Enne selles teemas kirjeldatud funktsioonide kasutamist vaadake üle ja rakendage nõutavad konfiguratsioonid. Lisateavet leiate teemadest [Ladustamata materjalide ja ootel hankijaarvete](configure-materials-nonstocked.md) lubamine ning [Hankekategooriate kasutamine projekti ostutellimuste ja ootel hankija arvetega](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Projektiga seotud ootel hankija arve postitamine 

Ootel hankija arved saab registreerida lehel **Ootel tarnija arved** (**Ostureskontro** > **Arved** > **Ootel hankijate arved**). Projektiga seotud ootel hankija arve postitamiseks tehke järgmist.

1. **Avage ostureskontro** > **arved** ja valige **Uus**. 
1. Valige väljale **Arve konto** hankija ja seejärel sisestage väljale **Number** hankija arve ID.
1. Lisage hankija arvele rida ja seejärel valige väljal **Kauba number** hankijalt ostetud ladustamata kaup. Teise võimalusena valige väljal **Hankekategooria** hankijalt ostetud hankekategooria.   
1. Lisage ostetud kogus. Süsteem täidab ühiku hinna, mis põhineb ladustamata kauba hinnakonfiguratsioonil. 
1. Kontrollige real kogusummat ja muid nõutud üksikasju.
1. Valige rea üksikasjade vahekaardil **Projekt** selle projekti ID, kuhu see üksus salvestatakse.
1. Valikuline: valige tegevuse number ja värskendage projektikategooriat ja reaatribuuti.
1. Sisestage ootel hankija arve. Arve konteerimisel salvestab süsteem järgmise teabe.
    
    - Hankija saldosumma.
    - Käibemaksu summa.
    - Projektiga seotud kulud kirjendatakse hanke integreerimise kontole.
    - Projekti tegeliku kulu tehing teenuses Dataverse.  Seda tehingut töödeldakse edasi, kasutades [Project Operationsi integreerimise töölehte](../project-accounting/project-operations-integration-journal.md). Selle töölehe sisestamine teisaldab summa hanke integreerimise kontolt projekti kulu kontole. 
    - Ostud, mille eest arved esitatakse projekti kliendile aja- ja materjalide arveldusmeetodit kasutades. Lisaks luuakse teenuses Dataverse ostude jaoks arveldamata müügitehingud. Teenuse Dataverse toodete hinnakirja kasutatakse arveldamata müügitehingute müügihindade ja summade jaoks.
