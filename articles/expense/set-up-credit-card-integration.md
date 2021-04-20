---
title: Krediitkaardi integratsiooni seadistamine
description: Selles teemas selgitatakse, kuidas töötada kuludega seotud krediitkaarditehingutega.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
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
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866678"
---
# <a name="set-up-credit-card-integration"></a>Krediitkaardi integratsiooni seadistamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Kuluga seotud krediitkaarditehinguid saab seadistada nii, et need imporditakse automaatselt korduvas ajakava põhjal. Teise võimalusena saab kandeid käsitsi vajadusel importida. Krediitkaarditehinguid imporditakse krediitkaarditehingute andmete olemi kaudu.

## <a name="import-credit-card-transactions"></a>Krediitkaarditehingute importimine

Krediitkaarditehingute importimiseks toimige järgmiselt.

1. Valige lehel **Krediitkaarditehingud** suvand **impordi tehingud**. Kui avate andmehaldust esimest korda, peab süsteem enne jätkamist värskendama andmete olemite loendit.
2. Sisestage väljale **Nimi** imporditöö kordumatu kirjeldus.
3. Valige väljal **Allika andmete vorming** imporditavaid krediitkaarditehinguid sisaldava faili vorming.
4. Valige **Laadi üles** ja seejärel otsige ja valige imporditav fail.
5. Pärast seda, kui fail on üles laaditud, valideerige krediitkaarditehingute faili vastendamine krediitkaarditehingute andmete olemi veergudega, valides paanil lingi **Vaata kaarti**. Kui vastendamisel esineb vigu või kui peate vastendust muutma, muutke vastendust kas vahekaardilt **Vastenduse visualiseerimine** või vahekaardilt **Vastendamise üksikasjad**.
6. Krediitkaarditehingute automatiseerimiseks valige **Loo korduvate andmete töö**. Seejärel saate määrata korduvuse, mis määratleb, kui tihti tuleb krediitkaarditehinguid importida. Kui olete lõpetanud, valige **OK**.
7. Valitud faili kohe importimiseks valige **Impordi**.
8. Kui importimise ajal tekib tõrkeid, saate vaadata käivituslogi või seadistusandmeid, et näha tõrkeid, mis tuleb eduka importimise tagamiseks parandada.

> [!NOTE]
> Kui peate importima mitu failivormingut, peate looma iga vormingutüübi jaoks eraldi imporditööd.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Lahkunud töötajate krediitkaarditehingute mujale määramine

Pärast seda, kui töötaja kirje on lõpetatud, on töötaja Active Directory Domain Services'i (AD DS) konto keelatud. Siiski võib esineda aktiivseid krediitkaarditehinguid, mida peab veel kuludesse kandma ja tagasi maksma. Lehel **Krediitkaarditehingud** saate määrata töötaja ümber mis tahes krediitkaarditehingu jaoks, kus seostatud töötaja on eemaldatud.

Valige üks või mitu krediitkaarditehingut ja seejärel valige **Kannete ümbermääramine**. Seejärel saate valida mõne muu töötaja, kellele soovite krediitkaarditehingud määrata. Pärast seda, kui krediitkaarditehingud on ümber määratud, saab neid valida kuluaruande jaoks ja tagasi maksta kuluaruande tavalise protsessi kaudu.

## <a name="delete-credit-card-transactions"></a>Krediitkaarditehingute kustutamine 

Mõnikord võib pärast krediitkaarditehingute importimist olla vaja teatud tehingud kustutada. Selle põhjuseks võib olla, et tehingud on duplikaadid või kuna andmed ei pruugi olla täpsed. Administraatorid saavad kasutada funktsiooni **Kustuta krediitkaartide tehingud**, et valida ja kustutada krediidikaarditehingud, mis pole kuluaruandele **lisatud**. 

1. Avage **Perioodilised ülesanded** > **Krediitkaarditehingute kustutamine**.
2. Valige **Filter** ja sisestage kaasatavate kirjete tuvastamiseks teave.
3. Kirjete kustutamiseks valige **OK**. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
