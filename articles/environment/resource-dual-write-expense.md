---
title: Kuluhalduse integreerimine
description: Selles teemas antakse teavet kuluaruande integreerimise kohta Project Operationsiga, kasutades topeltkirjutamist.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b41be519dbfa89668712bc28ccb1888cd08c38a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585787"
---
# <a name="expense-management-integration"></a>Kuluhalduse integreerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles teemas antakse teavet kuluaruannete integreerimise kohta Project Operationsis [täielik kulujuurutus](../expense/expense-overview.md), kasutades topeltkirjutamist.

## <a name="expense-categories"></a>Kulukategooriad

Täieliku kulujuurutuse korral luuakse ja hallatakse kulukategooriaid finance and Operationsi rakendustes. Uue kulukategooria loomiseks tehke järgmist.

1. Looge Microsoft Dataverse’is kategooria **Kanne**. Kahe kirjutamisega integratsioon sünkroonib selle kandekategooria rakendustega Finance and Operations. Lisateavet leiate teemadest [Projektikategooriate konfigureerimine](/dynamics365/project-operations/project-accounting/configure-project-categories) ja [Project Operationsi seadistamise ja konfigureerimise andmeintegreerimine](resource-dual-write-setup-integration.md). Selle integratsiooni tulemusena loob süsteem rakenduses Finance and Operations neli jagatud kategooria kirjet.
2. Minge valikusse **Kulude haldus** > **Seadistamine** > **Jagatud kategooriad** ja valige jagatud kategooria **kulutehingu** klassiga. Määrake parameetri **Kulus kasutatav** väärtuseks **Tõene** ja määrake kasutatava kulu tüüp.
3. Looge selle jagatud kategooria kirje abil uus kulukategooria, valides suvandid **Kuluhaldus** > **Seadistus** > **Kulukategooriad** ja uue **Uus**. Kirje salvestamisel kasutab topeltkirjutamine tabelikaarti **Project Operationsi integreerimine projekti kulukategooriate ekspordi olem (msdyn\_expensecategories)**, et sünkroonida see kirje Dataverse’i.

  ![Kulukategooriate integreerimine.](./media/DW6ExpenseCategories.png)

Finance and Operationsi rakenduste kulukategooriad on ettevõtte- või juriidilise isikupõhised. Dataverse’is on eraldi vastavad juriidilise isiku kirjed. Kui projektijuht prognoosib kulusid, ei saa ta valida projekti jaoks loodud kulukategooriaid, mille omanikuks on mõni muu ettevõte kui see, mille projektiga nad töötavad. 

## <a name="expense-reports"></a>Kuluaruanded

Kuluaruanded luuakse ja kinnitatakse finance and Operationsi rakendustes. Lisateavet leiate teemast [Kuluaruannete loomine ja töötlemine rakenduses Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Pärast seda, kui projektijuht on kuluaruande kinnitanud, sisestatakse see pearaamatusse. Project Operationsis sisestatakse projektiga seotud kuluaruande read spetsiaalsete sisestusreeglite abil.

  - Projektiga seotud kulusid (sealhulgas tagastamatut maksu) ei kirjendata kohe pearaamatu projekti kulukontole, vaid need kantakse kulude integreerimise kontole. See konto on konfigureeritud jaotises **Projektihaldus ja raamatupidamine** > **Seadistus** > **Projektihaldus ja raamatupidamisparameetrid**, vahekaardil **Project Operations rakenduses Dynamics 365 Customer Engagement**.
  - Topeltkirjutamine sünkroonitakse Dataverse’is, kasutades **Project Operationsi integreerimise projektikulude ekspordi olemi (msdyn\_expenses)** tabelikaarti.
  - Maksude allkirjastaja, hankija allkirjastaja ja muud finantssisestused kirjendatakse kuludeklaratsiooni postitamise hetke järgi.

  ![Kuluaruannete integreerimine.](./media/DW6ExpenseReports.png)

Kui kirje kirjutatakse üksuses **Kulu**, käivitab süsteem kirje automaatse kinnitamise Dataverse’i protsessi. Vajaduse korral saab automaatse kinnitamise protsessi oleku üle vaadata, kui avate Dataverse’i jaotise **Täpsemad sätted** > **Süsteem** > **Süsteemitööd**. Pärast kinnitamise lõpetamist luuakse olemis **Tegelikud andmed** kulukande klassi kirjed.

Kuluga seotud tegelikke andmeid töödeldakse seejärel, kasutades topeltkirjutamise tabelikaarti **Project Operationsi integreerimise tegelike andmetega (msdyn\_actuals)**. Lisateavet leiate teemast [Projekti prognoosid ja tegelikud andmed](resource-dual-write-estimates-actuals.md).

Perioodiline protsess **Import koondatud andmetest** loob kuluaruandega seotud töölehe read Project Operationsi integreerimise protsessis. Vastaskonto vaikeväärtuseks on kulude integreerimise konto. Konteerimise integreerimise tööleht tühjendab kulukande kontosaldo ja teisaldab kulusumma projekti kulukontole. Süsteem loob ka projekti alamandmikukanded järelarveldamiseks ja tulude kajastamiseks.
