---
title: Tarnija arve integreerimine
description: See artikkel annab teavet Project Operationsi hankija arvete integreerimise kohta.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d1e41638b6fe827e9e577860a78a84a9948053e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912051"
---
# <a name="vendor-invoice-integration"></a>Tarnija arve integreerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Projektiga seotud hankeid rakenduses Dynamics 365 Project Operations saab salvestada, kui lähete jaotisse **Ostureskontro** > **Arved** > **Ootel hankijate arved** ja kasutate ootel hankija arvedokumenti. Lisateavet leiate teemast [Logimata materjalide ostmine ootel oleva hankija arvega](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Enne selles artiklis kirjeldatud funktsioonide kasutamist vaadake üle ja rakendage nõutavad konfiguratsioonid. Lisateavet leiate teemast [Logimata materjalide ja ootel hankijate arvete lubamine](../procurement/configure-materials-nonstocked.md).

Project Operationsis sisestatakse projektiga seotud hankija arved spetsiaalsete sisestusreeglite abil.

- Projektiga seotud kulu (sh tagastamatu maks) ei sisestata kohe pearaamatusse projekti kulukontole. Selle asemel sisestatakse kulu **Hanke integreerimise kontole**. See konto on konfigureeritud jaotises **Projektihaldus ja raamatupidamine** > **Seadistus** > **Projektihalduse ja raamatupidamise parameetrid** vahekaardil **Project Operations on Dynamics 365 Customer engagement**.
- Topeltkirjutamine sünkroonib hankija arve üksikasjad rakendusse Microsoft Dataverse järgmiste tabelikaartide abil.

     - **Project Operationsi integreerimise projekti hankija arve ekspordi olem (msdyn_projectvendorinvoices)**: see tabelikaart sünkroonib hankija arve päise teabe. Sünkroonitakse ainult vähemalt ühe projekti ID-ga reaga hankija Dataverse’i arved.
     - **Project Operationsi integreerimise projekti hankija arve rea ekspordi olem (msdyn_projectvendorinvoices)**: see tabelikaart sünkroonib hankija arve rea teabe. Dataverse’i sünkroonitakse ainult need read, mis sisaldavad projekti ID-d.

     > [!NOTE]
     > Hankija arve üksikasju Dataverse’is ei saa redigeerida.

Maksu alammoodul, hankija alammoodul ja muud finantspostitused kirjendatakse hankija arve postitamisel vajaduse järgi rakenduses Dynamics 365 Finance, kui hankija arve on sisestatud.

![Hankija arve integratsioon.](media/DW7VendorInvoice.png)

Kui kirjed kirjutatakse olemis **Hankija arve** rakenduses Dataverse, algab kirjete automaatne kinnitamisprotsess. Vajaduse korral saab automaatse kinnitamise protsessi oleku üle vaadata, kui avate Dataverse’i jaotise **Täpsemad sätted** > **Süsteem** > **Süsteemitööd**. Pärast kinnitamise lõpetamist loob süsteem olemis **Tegelikud andmed** kandeklassi kirjed.

Materjaliga seotud tegelikud andmed töödeldakse seejärel topeltkirjutamise tabelikaardi abil, **Project Operationsi integreerimise tegelikud andmed (msdyn_actuals)**. Lisateavet leiate teemast [Projekti prognoosid ja tegelikud andmed](resource-dual-write-estimates-actuals.md).

Perioodiline protsess **Import koondandmetest** loob hankija arvega seotud Project Operationsi integreerimise töölehe read. Vastaskonto vaikeväärtus on hangete integreerimise konto. Kui integreerimise tööleht on sisestatud, tühjendatakse hankija arvekande kontosaldo ja rea summa teisaldatakse projekti kulukontole. Projekti alampearaamatu kanded luuakse ka järelarveldamiseks ja tulude kajastamiseks.
