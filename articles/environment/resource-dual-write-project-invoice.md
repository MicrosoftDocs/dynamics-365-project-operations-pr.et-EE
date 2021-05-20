---
title: Projekti arve integreerimine
description: Selles teemas antakse teavet Project Operationsi topeltkirjutamisega integreerimise kohta kliendi arvelduses.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955735"
---
# <a name="project-invoice-integration"></a>Projekti arve integreerimine

Selles teemas antakse teavet Project Operationsi topeltkirjutamisega integreerimise kohta kliendi arvelduses.

Project Operationsis haldab projekti haldur projekti arvelduse mahajäämust ja loob kliendile pro forma arve rakenduses Microsoft Dataverse. Selle pro forma arve põhjal loob müügireskontro ametnik või projekti raamatupidaja kliendile suunatud arve. Topeltkirjutamise integreerimine tagab pro forma arve üksikasjade sünkroonimise rakendustega Finance and Operations. Pärast kliendile suunatud arve sisestamist värskendab süsteem asjakohased projekti tegelikud andmed rakenduses Dataverse raamatupidamise üksikasjadega. Järgmine joonis annab sellest integreerimisest kõrgetasemelise kontseptuaalse ülevaate.

   ![Projekti arve integreerimine](./media/DW5Invoicing.png)

Pärast seda, kui projektijuht kinnitab pro forma arve rakenduses Dataverse, sünkroonitakse pro forma arve päise teave rakendustega Finance and Operations, kasutades topeltkirjutamise kaarti **Projekti arvesoovitus V2 (arved)**. See on üks võimalus, kuidas integreerida Dataverse rakendustesse Finance and Operations. Projekti arve loomist või kustutamist otse rakenduses Finance and Operations ei toetata.

Arve kinnitus Dataverse’is käivitab äriloogika ka arvega seotud kirjete loomiseks olemis **Tegelikud andmed**. Need kirjed sünkroonitakse rakendusega Finance and Operations, kasutades topeltkirjutamise tabelikaarti, **Project Operationsi integreerimise tegelikud andmed (msdyn \_actuals).** Lisateavet leiate teemast [Projekti prognoosid ja tegelikud andmed](resource-dual-write-estimates-actuals.md). 

Projekti arve arveldamise read luuakse perioodilise protsessiga **Import koondandmetest**. See protsess põhineb arveldatud müügi tegelikel andmetel tabelis **Tegelike andmete koondamine**. Lisateavet leiate teemast [Projektiarve soovituste haldamine](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
