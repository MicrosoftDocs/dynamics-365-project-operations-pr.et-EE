---
title: Kuluhalduse integreerimine
description: Selles teemas antakse teavet kuluaruande integreerimise kohta Project Operationsiga, kasutades topeltkirjutamist.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c347f14f3a479eb4aec951cfe4094c5581bce32
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955737"
---
# <a name="expense-management-integration"></a>Kuluhalduse integreerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles teemas antakse teavet kuluaruannete integreerimise kohta Project Operationsis [täielik kulujuurutus](../expense/expense-overview.md), kasutades topeltkirjutamist.

## <a name="expense-categories"></a>Kulukategooriad

Täieliku kulujuurutuse puhul luuakse ja hallatakse kulukategooriaid rakenduses Finance and Operations. Uue kulukategooria loomiseks tehke järgmist.

1. Looge Microsoft Dataverse’is kategooria **Kanne**. Topeltkirjutamise integreerimine sünkroonib selle kannete kategooria rakendustega Finance and Operations. Lisateavet leiate teemadest [Projektikategooriate konfigureerimine](/dynamics365/project-operations/project-accounting/configure-project-categories) ja [Project Operationsi seadistamise ja konfigureerimise andmeintegreerimine](resource-dual-write-setup-integration.md). Selle integreerimise tulemusena loob süsteem rakendustes Finance and Operations neli ühiskategooria kirjet.
2. Minge valikusse **Kulude haldus** > **Seadistamine** > **Jagatud kategooriad** ja valige jagatud kategooria **kulutehingu** klassiga. Määrake parameetri **Kulus kasutatav** väärtuseks **Tõene** ja määrake kasutatava kulu tüüp.
3. Looge selle jagatud kategooria kirje abil uus kulukategooria, valides suvandid **Kuluhaldus** > **Seadistus** > **Kulukategooriad** ja uue **Uus**. Kirje salvestamisel kasutab topeltkirjutamine tabelikaarti **Project Operationsi integreerimine projekti kulukategooriate ekspordi olem (msdyn\_expensecategories)**, et sünkroonida see kirje Dataverse’i.

  ![Kulukategooriate integreerimine](./media/DW6ExpenseCategories.png)

Rakenduste Finance and Operations kulukategooriad on ettevõtte või juriidilise olemi põhised. Dataverse’is on eraldi vastavad juriidilise isiku kirjed. Kui projektijuht prognoosib kulusid, ei saa ta valida projekti jaoks loodud kulukategooriaid, mille omanikuks on mõni muu ettevõte kui see, mille projektiga nad töötavad. 

## <a name="expense-reports"></a>Kuluaruanded

Kuluaruanded luuakse ja kinnitatakse rakendustes Finance and Operations. Lisateavet leiate teemast [Kuluaruannete loomine ja töötlemine rakenduses Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Pärast seda, kui projektijuht on kuluaruande kinnitanud, sisestatakse see pearaamatusse. Project Operationsis sisestatakse projektiga seotud kuluaruande read spetsiaalsete sisestusreeglite abil.

  - Projektiga seotud kulusid (sealhulgas tagastamatut maksu) ei kirjendata kohe pearaamatu projekti kulukontole, vaid need kantakse kulude integreerimise kontole. See konto on konfigureeritud jaotises **Projektihaldus ja raamatupidamine** > **Seadistus** > **Projektihaldus ja raamatupidamisparameetrid**, vahekaardil **Project Operations rakenduses Dynamics 365 Customer Engagement**.
  - Topeltkirjutamine sünkroonitakse Dataverse’is, kasutades **Project Operationsi integreerimise projektikulude ekspordi olemi (msdyn\_expenses)** tabelikaarti.
  - Maksude allkirjastaja, hankija allkirjastaja ja muud finantssisestused kirjendatakse kuludeklaratsiooni postitamise hetke järgi.

  ![Kuluaruannete integreerimine](./media/DW6ExpenseReports.png)

Kui kirje kirjutatakse üksuses **Kulu**, käivitab süsteem kirje automaatse kinnitamise Dataverse’i protsessi. Vajaduse korral saab automaatse kinnitamise protsessi oleku üle vaadata, kui avate Dataverse’i jaotise **Täpsemad sätted** > **Süsteem** > **Süsteemitööd**. Pärast kinnitamise lõpetamist luuakse olemis **Tegelikud andmed** kulukande klassi kirjed.

Kuluga seotud tegelikke andmeid töödeldakse seejärel, kasutades topeltkirjutamise tabelikaarti **Project Operationsi integreerimise tegelike andmetega (msdyn\_actuals)**. Lisateavet leiate teemast [Projekti prognoosid ja tegelikud andmed](resource-dual-write-estimates-actuals.md).

Perioodiline protsess **Import koondatud andmetest** loob kuluaruandega seotud töölehe read Project Operationsi integreerimise protsessis. Vastaskonto vaikeväärtuseks on kulude integreerimise konto. Konteerimise integreerimise tööleht tühjendab kulukande kontosaldo ja teisaldab kulusumma projekti kulukontole. Süsteem loob ka projekti alamandmikukanded järelarveldamiseks ja tulude kajastamiseks.
