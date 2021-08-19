---
title: Logimata materjalide ostmine ootel oleva hankija arve abil
description: Selles teemas kirjeldatakse, kuidas kirjendada ootel hankija arveid.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ce9f244eaa549742aeb55024ca9ef4d82cde1bd4a5b9c7f8c762cf72e0da83f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009031"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Logimata materjalide ostmine ootel oleva hankija arve abil

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Kuna ettevõttes kasutatakse projekti jaoks logimata materjale, saab kulud kohe projekti kohta kirjendada. 

Näiteks teeb ettevõte Contoso Robotics US tarkvara uuendamise projekti ja vajab tarkvaralitsentse. Need litsentsid on pärit kolmandalt osapoolelt.  Funktsiooni Dynamics 365 Finance kasutamisel fikseerib ostureskontro ametnik ootel oleva hankija arve dokumendi ja omistab litsentsikulud otse seadmete uuendamise projektile. 

> [!IMPORTANT]
> Enne selles teemas kirjeldatud funktsioonide kasutamist vaadake üle ja rakendage nõutavad konfiguratsioonid. Lisateavet leiate teemast [Logimata materjalide ja ootel hankija arvete lubamine](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Projektiga seotud ootel hankija arve postitamine 

Ootel hankija arved saab registreerida lehel **Ootel tarnija arved** (**Ostureskontro** > **Arved** > **Ootel hankijate arved**). Projektiga seotud ootel hankija arve postitamiseks tehke järgmist.

1. Minge jaotisesse **Ostureskontro** > **Arved** ja valige **Uus**. 
2. Valige väljal **Arve konto** soovitud tarnija ja sisestage väljal **Number** hankija arve ID.
3. Lisage rida hankija arvele ja valige väljal **Üksuse number** tarnijalt ostetud logimata üksus. 

    > [!NOTE]
    > Hankija arve ridu, mis põhinevad hankekategoorial, ei saa projekti suhtes registreerida. 
    
5. Lisage ostetud kogus. Süsteem asustab ühikuhinna logimata üksuse hinna konfiguratsiooni kohaselt. 
6. Kontrollige real kogusummat ja muid nõutud üksikasju.
7. Valige rea üksikasjade vahekaardil **Projekt** selle projekti ID, kus see üksus registreeritakse.
8. Soovi korral valige tegevuse number ning värskendage projekti kategooriat ja rea atribuuti.
9. Sisestage ootel hankija arve. Arve sisestamisel salvestab süsteem järgmised andmed.
    
    - Hankija saldosumma.
    - Käibemaksu summa.
    - Projektiga seotud kulud kirjendatakse hanke integreerimise kontole.
    - Projekti tegelik kande väärtus Dataverse’is. Seda tehingut töödeldakse edasi, kasutades [Project Operationsi integreerimise töölehte](../project-accounting/project-operations-integration-journal.md). Selle töölehe sisestamine teisaldab summa hanke integreerimise kontolt projekti kulu kontole.
