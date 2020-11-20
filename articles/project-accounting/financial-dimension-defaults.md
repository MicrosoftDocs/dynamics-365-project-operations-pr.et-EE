---
title: Finantsdimensiooni vaikeväärtused
description: Selles teemas antakse teavet, kuidas häälestada finantsdimensiooni vaikeväärtused.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131878"
---
# <a name="financial-dimension-defaults"></a>Finantsdimensiooni vaikeväärtused

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Dynamics 365 Project Operationskasutab [finantsdimensioonide](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) raamistikku rakenduses Dynamics 365 Finance, et pakkuda projekti alammooduli ja üldiste pearaamatu tehingute kohta täiendavad ülevaateid.

Vaikimisi finantsdimensioonid saab määrata kliendile, projekti finantseerimisallikale, vahe-eesmärgile, projekti leingureale või projektile.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Kliendi vaikimisi finantsdimensioonide määratlemine

Rakenduses Finance määratletud kliendi dimensiooni vaikesätted. Dimensiooni vaikeväärtuste määramiseks tehke järgmist.

1. Avage **Mügireskontro** > **Kliendid** > **Kõik kliendid**.
2. Lehe **Kliendid** vahekaardil **Finantsdimensioonid** määrake konkreetse kliendi finantsdimensiooni väärtused.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Projektilepingute vaikimisi finantsdimensioonide määratlemine

Projektilepinguid luuakse ja hallatakse teenuses Common Data Service (CDS). Projektilepingute raamatupidamise atribuudid määratakse rakenduse Finance moodulis **Projektihaldus ja raamatupidamine**.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Projekti finantseerimisallika finantsdimensioonide määramine

1. Avage **Projektijuhtimine ja raamatupidamine** > **Projektid** > **Projekti lepingud**.
2. Valige kirje, mida soovite värskendada, ja valige vahekaardil **Projektileping** suvand **Kuva vaikimisi raamatupidamine**.
3. Laiendage suvandit **Seotud teave** ja valige vahekaart **Rahastamisallikad**.
4. Määrake finantsdimensiooni vaikeväärtused. Pange tähele, et finantsdimensioonide vaikeväärtused pärinevad kliendi kontolt.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Projekti lepingurea finantsdimensioonide määramine

1. Avage **Projektijuhtimine ja raamatupidamine** > **Projektid** > **Projekti lepingud**.
2. Valige kirje, mida soovite värskendada, ja valige vahekaardil **Projektileping** suvand **Kuva vaikimisi raamatupidamine**.
3. Laiendage suvandit **Seotud teave** ja valige vahekaart **Lepinguread**.
4. Määrake finantsdimensiooni vaikeväärtused. Finantsdimensioonide vaikeväärtused kehtivad ja saab kasutada ainult fikseeritud hinnaga (vahe-eesmärgi) lepinguridadega.

Neid vaikeväärtusi kasutatakse seostuvates projektides kontoga seotud kannetes ja arveridadel.

## <a name="define-default-financial-dimensions-for-projects"></a>Projektide vaikimisi finantsdimensioonide määratlemine

Projekte luuakse ja hallatakse CDS-is. Projektide raamatupidamise atribuudid määratakse rakenduse Finance moodulis **Projektihaldus ja raamatupidamine**.

1. Minge jaotisse **Projektijuhtimine ja raamatupidamine** > **Projektid** > **Kõik projektid**.
2. Valige kirje, mida soovite värskendada, ja valige vahekaardil **Projekt** suvand **Kuva vaikimisi raamatupidamine**.
3. Laiendage suvandit **Seotud teave** ja valige vahekaart **Seadistus**.
4. Määrake finantsdimensiooni vaikeväärtused. Pange tähele, et finantsdimensioonide vaikeväärtused pärinevad kliendi kontolt. Kui projekt on seostatud mitme projektilepingu kliendiga lepingureaga, kasutatakse vaikimisi finatsdimensioonideks peamist klienti.

Projekti vaikimisi finantsdimensioone kasutatakse suvandis **Project Operationsi integreerimise tööleht** ja seotud projekti arvete ridade jaoks aja, kulu ja tasu kannete jaoks tööleherea vaikeväärtuste määramiseks.
