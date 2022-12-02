---
title: Projekti arve integreerimine
description: See artikkel annab teavet rakenduse Project Operations topeltkirjutusega integreerimise kohta kliendi arvelduses.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029019"
---
# <a name="project-invoice-integration"></a>Projekti arve integreerimine

See artikkel annab teavet rakenduse Project Operations topeltkirjutusega integreerimise kohta kliendi arvelduses.

Project Operationsis haldab projekti haldur projekti arvelduse mahajäämust ja loob kliendile pro forma arve rakenduses Microsoft Dataverse. Selle pro forma arve põhjal loob müügireskontro ametnik või projekti raamatupidaja kliendile suunatud arve. Topeltkirjutuse integreerimine tagab näidisarve üksikasjade sünkroonimise finants- ja äritoimingute rakendustega. Pärast kliendile suunatud arve sisestamist värskendab süsteem asjakohased projekti tegelikud andmed rakenduses Dataverse raamatupidamise üksikasjadega. Järgmine joonis annab sellest integreerimisest kõrgetasemelise kontseptuaalse ülevaate.

   ![Projekti arve integreerimine.](./media/DW5Invoicing.png)

Pärast seda, kui projektijuht kinnitab näidisarve rakenduses Dataverse, sünkroonitakse näidisarve päise teave finants- ja äritoimingute rakendustega, kasutades topeltkirjutuse tabelikaarti **Projekti arve ettepanek V2 (arved)**. See on üks võimalus, kuidas integreerida rakendus Dataverse finants- ja äritoimingute rakendustesse. Projekti arve loomist või kustutamist otse finants- ja äritoimingute rakenduses ei toetata.

Arve kinnitus Dataverse’is käivitab äriloogika ka arvega seotud kirjete loomiseks olemis **Tegelikud andmed**. Need kirjed sünkroonitakse finants- ja äritoimingute rakendusega, kasutades topeltkirjutusega tabelikaarti, **Project Operationsi integreerimise tegelikud näitajad (msdyn\_actuals).** Lisateavet leiate teemast [Projekti prognoosid ja tegelikud andmed](resource-dual-write-estimates-actuals.md). 

Projekti arve arveldamise read luuakse perioodilise protsessiga **Import koondandmetest**. See protsess põhineb arveldatud müügi tegelikel andmetel tabelis **Tegelike andmete koondamine**. Lisateavet leiate teemast [Projektiarve soovituste haldamine](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
