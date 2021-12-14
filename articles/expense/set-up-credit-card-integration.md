---
title: Krediitkaardi integratsiooni seadistamine
description: Selles teemas selgitatakse, kuidas töötada kuludega seotud krediitkaarditehingutega.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 49c8f2369a8be41fbc04c74bdb6b565b4f4b7b79
ms.sourcegitcommit: 9f26cf8bb640af1eb9f7f0872805965d7ffcb9d3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/19/2021
ms.locfileid: "7826251"
---
# <a name="set-up-credit-card-integration"></a>Krediitkaardi integratsiooni seadistamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Kuluga seotud krediitkaarditehinguid saab seadistada nii, et need imporditakse automaatselt korduvas ajakava põhjal. Teise võimalusena saab kandeid käsitsi vajadusel importida. Krediitkaarditehinguid imporditakse krediitkaarditehingute andmete olemi kaudu.

## <a name="import-credit-card-transactions"></a>Krediitkaarditehingute importimine

Krediitkaarditehingute importimiseks toimige järgmiselt.

1. Valige lehel **Krediitkaarditehingud** suvand **impordi tehingud**. Kui avate andmehaldust esimest korda, peab süsteem enne jätkamist värskendama andmeolemite loendit.
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

Pärast töötajakirje lõpetamist on töötaja Active Directory domeeniteenuste (AD DS) konto keelatud. Siiski võib esineda aktiivseid krediitkaarditehinguid, mida peab veel kuludesse kandma ja tagasi maksma. Lehel **Krediitkaarditehingud** saate määrata töötaja ümber mis tahes krediitkaarditehingu jaoks, kus seostatud töötaja on eemaldatud.

Valige üks või mitu krediitkaarditehingut ja seejärel valige **Kannete ümbermääramine**. Seejärel saate valida mõne muu töötaja, kellele soovite krediitkaarditehingud määrata. Pärast seda, kui krediitkaarditehingud on ümber määratud, saab neid valida kuluaruande jaoks ja tagasi maksta kuluaruande tavalise protsessi kaudu.

## <a name="delete-credit-card-transactions"></a>Krediitkaarditehingute kustutamine 

Mõnikord võib pärast krediitkaarditehingute importimist olla vaja teatud tehingud kustutada. Selle põhjuseks võib olla asjaolu, et kanded on duplikaadid või kuna andmed pole täpsed. Administraatorid saavad kasutada funktsiooni **Kustuta krediitkaartide tehingud**, et valida ja kustutada krediidikaarditehingud, mis pole kuluaruandele **lisatud**. 

1. Avage **Perioodilised ülesanded** > **Krediitkaarditehingute kustutamine**.
2. Valige **Filter** ja sisestage kaasatavate kirjete tuvastamiseks teave.
3. Kirjete kustutamiseks valige **OK**. 

## <a name="storing-credit-card-numbers"></a>Krediitkaardinumbrite salvestamine

Krediitkaardinumbrite hoidmiseks on saadaval kolm võimalust. Krediitkaardi numbrid salvestatakse **kuluhalduse parameetrite** lehele.

- **Takista kaardi numbri sisestamist** – krediitkaardinumbreid ei salvestata.
- **Räsikaardi numbrid (pood viimased neli numbrit)** – krediitkaardinumbrite viimased neli numbrit salvestatakse krüpteeritud vormingus.
- **Poekaardi numbrid** – krediitkaardi numbrid salvestatakse krüpteerimata vormingus. See suvand ei vasta maksekaarditööstuse (PCI) andmeturbe standardile (DSS). Seetõttu peaksid organisatsiooni administraatorid pci DSS-i eeskirjadega vastavusse hoidmiseks valima, kas mitte salvestada krediitkaardinumbreid või salvestada räsikaardi numbreid.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
