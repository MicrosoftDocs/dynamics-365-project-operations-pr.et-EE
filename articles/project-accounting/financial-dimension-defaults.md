---
title: Finantsdimensiooni vaikeväärtused
description: Selles teemas antakse teavet, kuidas häälestada finantsdimensiooni vaikeväärtused.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9f43fed57a1411a55dcd7929f34e87aed136a6b5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579485"
---
# <a name="financial-dimension-defaults"></a>Finantsdimensiooni vaikeväärtused

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_



Dynamics 365 Project Operations [kasutab Dynamics 365 Finance finantsdimensioonide](/dynamics365/finance/general-ledger/financial-dimensions) raamistikku, et anda täiendavaid ülevaateid projekti alammoodulite ja pearaamatukannete kohta.

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
