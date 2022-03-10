---
title: Krediitkaarditehingute importimine ja säilitamine
description: Selles teemas kirjeldatakse kuluga seotud krediitkaarditehingute importimist ja haldamist. Neid tehinguid saab seadistada nii, et need imporditakse automaatselt regulaarselt teatud aja tagant, või neid saab vajaduse kohaselt käsitsi importida.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c3a53d2ae4eae411364aaf68ac806b55335c75d4870a24715954ccae327f4358
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995846"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Krediitkaarditehingute importimine ja säilitamine

Kuluga seotud krediitkaarditehinguid saab seadistada nii, et need imporditakse automaatselt korduvas ajakava põhjal. Teise võimalusena saab kandeid käsitsi vajadusel importida. Krediitkaarditehinguid imporditakse krediitkaarditehingute andmete olemi kaudu.

Lisateavet andmeolemite kohta leiate teemast [Andmeolemid ](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Krediitkaarditehingute importimine

1. Valige lehel **Krediitkaarditehingud** suvand **impordi tehingud**. Kui avate andmehaldust esimest korda, peab süsteem enne jätkamist värskendama andmete olemite loendit.
2. Sisestage väljale **Nimi** imporditoimingule kordumatu kirjeldus.
3. Valige väljal **Allika andmete vorming** imporditavaid krediitkaarditehinguid sisaldava faili vorming.
4. Valige **Laadi üles** ja seejärel otsige ja valige imporditav fail.
5. Pärast seda, kui fail on üles laaditud, valideerige krediitkaarditehingute faili vastendamine krediitkaarditehingute andmete olemi veergudega, valides paanil lingi **Vaata kaarti**. Kui vastendamisel esineb vigu või kui peate vastendust muutma, muutke vastendust kas vahekaardilt **Vastenduse visualiseerimine** või vahekaardilt **Vastendamise üksikasjad**.
6. Krediitkaarditehingute automatiseerimiseks valige **Loo korduvate andmete töö**. Seejärel saate määrata korduvuse, mis määratleb, kui tihti tuleb krediitkaarditehinguid importida. Kui olete lõpetanud, valige **OK**.
7. Valitud faili kohe importimiseks valige **Impordi**.
8. Kui importimisel ilmneb tõrkeid, saate vaadata täitmislogi või koondamise andmeid, et näha, milliseid vigu tuleb parandada, et aidata tagada edukat importimist.

> [!NOTE]
> Kui peate importima rohkem kui ühe failivormingu, peate looma eraldi importimistööd iga vormingu tüübi jaoks.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Lahkunud töötajate krediitkaarditehingute mujale määramine

Pärast seda, kui töötaja kirje on lõpetatud, on töötaja Active Directory Domain Services'i (AD DS) konto keelatud. Siiski võib esineda aktiivseid krediitkaarditehinguid, mida peab veel kuludesse kandma ja tagasi maksma. Lehelt **Krediitkaarditehingud** saate töötaja ümber määrata mistahes krediitkaarditehingu korral, kus seotud töötaja on töölt lahkunud.

Valige üks või mitu krediitkaarditehingut ja seejärel valige **Kannete ümbermääramine**. Seejärel saate valida mõne muu töötaja, kellele soovite krediitkaarditehingud määrata. Pärast seda, kui krediitkaarditehingud on ümber määratud, saab neid valida kuluaruande jaoks ja tagasi maksta kuluaruande tavalise protsessi kaudu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]