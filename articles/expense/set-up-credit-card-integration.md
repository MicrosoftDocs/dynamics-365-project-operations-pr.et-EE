---
title: Krediitkaardi integratsiooni seadistamine
description: Selles teemas kirjeldatakse kuluga seotud krediitkaarditehingute importimist ja haldamist.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276163"
---
# <a name="set-up-credit-card-integration"></a>Krediitkaardi integratsiooni seadistamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Kuluga seotud krediitkaarditehinguid saab seadistada nii, et need imporditakse automaatselt korduvas ajakava põhjal. Teise võimalusena saab kandeid käsitsi vajadusel importida. Krediitkaarditehinguid imporditakse krediitkaarditehingute andmete olemi kaudu.

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