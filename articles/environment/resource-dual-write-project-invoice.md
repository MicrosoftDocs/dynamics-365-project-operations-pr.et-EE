---
title: Projekti arve integreerimine
description: Selles teemas antakse teavet Project Operationsi topeltkirjutamisega integreerimise kohta kliendi arvelduses.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581233"
---
# <a name="project-invoice-integration"></a>Projekti arve integreerimine

Selles teemas antakse teavet Project Operationsi topeltkirjutamisega integreerimise kohta kliendi arvelduses.

Project Operationsis haldab projekti haldur projekti arvelduse mahajäämust ja loob kliendile pro forma arve rakenduses Microsoft Dataverse. Selle pro forma arve põhjal loob müügireskontro ametnik või projekti raamatupidaja kliendile suunatud arve. Kahe kirjutamise integreerimine tagab, et proforma arve üksikasjad sünkroonitakse rakendustega Finance and Operations. Pärast kliendile suunatud arve sisestamist värskendab süsteem asjakohased projekti tegelikud andmed rakenduses Dataverse raamatupidamise üksikasjadega. Järgmine joonis annab sellest integreerimisest kõrgetasemelise kontseptuaalse ülevaate.

   ![Projekti arve integreerimine.](./media/DW5Invoicing.png)

Pärast seda, kui projektijuht kinnitab proforma arve rakenduses Dataverse, sünkroonitakse proforma arve päise teave finance and Operations rakendustega, kasutades kahe kirjutamisega tabelikaarti, **Projekti arve ettepanekut V2 (arved)**. See on ühesuunaline integratsioon Dataverse finance and operationsi rakendustest. Projektiarvete ettepanekute loomist või kustutamist otse Finance and Operationsi rakendustes ei toetata.

Arve kinnitus Dataverse’is käivitab äriloogika ka arvega seotud kirjete loomiseks olemis **Tegelikud andmed**. Need kirjed sünkroonitakse rakendusega Finance and Operations, kasutades kahe kirjutamisega tabelikaarti Project **Operations integration actuals (msdyn\_ actuals).** Lisateavet leiate teemast [Projekti prognoosid ja tegelikud andmed](resource-dual-write-estimates-actuals.md). 

Projekti arve arveldamise read luuakse perioodilise protsessiga **Import koondandmetest**. See protsess põhineb arveldatud müügi tegelikel andmetel tabelis **Tegelike andmete koondamine**. Lisateavet leiate teemast [Projektiarve soovituste haldamine](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
