---
title: Projekti arve integreerimine
description: Selles teemas antakse teavet Project Operationsi topeltkirjutamisega integreerimise kohta kliendi arvelduses.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996561"
---
# <a name="project-invoice-integration"></a>Projekti arve integreerimine

Selles teemas antakse teavet Project Operationsi topeltkirjutamisega integreerimise kohta kliendi arvelduses.

Project Operationsis haldab projekti haldur projekti arvelduse mahajäämust ja loob kliendile pro forma arve rakenduses Microsoft Dataverse. Selle pro forma arve põhjal loob müügireskontro ametnik või projekti raamatupidaja kliendile suunatud arve. Topeltkirjutamise integreerimine tagab pro forma arve üksikasjade sünkroonimise rakendustega Finance and Operations. Pärast kliendile suunatud arve sisestamist värskendab süsteem asjakohased projekti tegelikud andmed rakenduses Dataverse raamatupidamise üksikasjadega. Järgmine joonis annab sellest integreerimisest kõrgetasemelise kontseptuaalse ülevaate.

   ![Projekti arve integreerimine](./media/DW5Invoicing.png)

Pärast seda, kui projektijuht kinnitab pro forma arve rakenduses Dataverse, sünkroonitakse pro forma arve päise teave rakendustega Finance and Operations, kasutades topeltkirjutamise kaarti **Projekti arvesoovitus V2 (arved)**. See on üks võimalus, kuidas integreerida Dataverse rakendustesse Finance and Operations. Projekti arve loomist või kustutamist otse rakenduses Finance and Operations ei toetata.

Arve kinnitus Dataverse’is käivitab äriloogika ka arvega seotud kirjete loomiseks olemis **Tegelikud andmed**. Need kirjed sünkroonitakse rakendusega Finance and Operations, kasutades topeltkirjutamise tabelikaarti, **Project Operationsi integreerimise tegelikud andmed (msdyn \_actuals).** Lisateavet leiate teemast [Projekti prognoosid ja tegelikud andmed](resource-dual-write-estimates-actuals.md). 

Projekti arve arveldamise read luuakse perioodilise protsessiga **Import koondandmetest**. See protsess põhineb arveldatud müügi tegelikel andmetel tabelis **Tegelike andmete koondamine**. Lisateavet leiate teemast [Projektiarve soovituste haldamine](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
