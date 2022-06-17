---
title: Projekti arve integreerimine
description: Selles artiklis antakse teavet Project Operationsi topeltkirjutamise integreerimise kohta kliendi arveldamiseks.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912097"
---
# <a name="project-invoice-integration"></a>Projekti arve integreerimine

Selles artiklis antakse teavet Project Operationsi topeltkirjutamise integreerimise kohta kliendi arveldamiseks.

Project Operationsis haldab projekti haldur projekti arvelduse mahajäämust ja loob kliendile pro forma arve rakenduses Microsoft Dataverse. Selle pro forma arve põhjal loob müügireskontro ametnik või projekti raamatupidaja kliendile suunatud arve. Kahe kirjutamise integreerimine tagab, et proforma arve üksikasjad sünkroonitakse rakendustega Finance and Operations. Pärast kliendile suunatud arve sisestamist värskendab süsteem asjakohased projekti tegelikud andmed rakenduses Dataverse raamatupidamise üksikasjadega. Järgmine joonis annab sellest integreerimisest kõrgetasemelise kontseptuaalse ülevaate.

   ![Projekti arve integreerimine.](./media/DW5Invoicing.png)

Pärast seda, kui projektijuht kinnitab proforma arve rakenduses Dataverse, sünkroonitakse proforma arve päise teave finance and Operations rakendustega, kasutades kahe kirjutamisega tabelikaarti, **Projekti arve ettepanekut V2 (arved)**. See on ühesuunaline integratsioon Dataverse finance and operationsi rakendustest. Projektiarvete ettepanekute loomist või kustutamist otse Finance and Operationsi rakendustes ei toetata.

Arve kinnitus Dataverse’is käivitab äriloogika ka arvega seotud kirjete loomiseks olemis **Tegelikud andmed**. Need kirjed sünkroonitakse rakendusega Finance and Operations, kasutades kahe kirjutamisega tabelikaarti Project **Operations integration actuals (msdyn\_ actuals).** Lisateavet leiate teemast [Projekti prognoosid ja tegelikud andmed](resource-dual-write-estimates-actuals.md). 

Projekti arve arveldamise read luuakse perioodilise protsessiga **Import koondandmetest**. See protsess põhineb arveldatud müügi tegelikel andmetel tabelis **Tegelike andmete koondamine**. Lisateavet leiate teemast [Projektiarve soovituste haldamine](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
