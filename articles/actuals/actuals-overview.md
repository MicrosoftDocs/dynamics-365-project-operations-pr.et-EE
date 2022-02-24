---
title: Tegelikud näitajad
description: Selles teemas antakse teavet tegelike andmetega töötamise kohta Microsofti Dynamics 365 Project Operationsis.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852539"
---
# <a name="actuals"></a>Tegelikud näitajad 

_**Rakendub:** Project Operationsi ressursipõhiste/mittelaopõhiste stsenaariumide korral, lihtjuurutamine – tehing näidisarveldusele_

Tegelikud andmed esindavad projekti läbivaadatud ja kinnitatud finantsilist ning ajakava edenemist. Need luuakse aja, kulu, materjali kasutuskirjete, töölehe kannete ja arvete kinnitamise tulemusena.

## <a name="journal-lines-and-time-submission"></a>Töölehe read ja aja esitamine

Lisateavet ajakirje kohta vaadake teemast [Ajakirje ülevaade](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Aeg ja materjalid

Kui esitatud ajakirje on seotud projektiga, mis on vastendatud mõne aja ja materjali lepingureaga, loob süsteem kaks töölehe rida – ühe kulu ja ühe arveldamata müügi jaoks.

### <a name="fixed-price"></a>Fikseeritud hind

Kui esitatav ajakirje seotakse projektiga, mis on vastendatud fikseeritud hinnaga lepingureaga, loob süsteem ühe töölehe rea kulu jaoks.

### <a name="default-pricing"></a>Vaikimisi hinnakujundus

Vaikehindade looise loogika asub töölehe real. Ajakirje välja väärtused kopeeritakse töölehe reale. Need väärtused hõlmavad tehingu kuupäeva, lepingurida, millega projekt on vastendatud, ja vastava hinnakirja valuutat.

Vaikimisi hinnakujundust mõjutavaod välju (nt **roll** ja **ressursiüksus**) kasutatakse töölehe rea sobiva hinna kindlakstegemiseks. Saate lisada ajakirjele kohandatud välja. Kui soovite kanda välja väärtuse tegelikele väärtustele, looge väli tabelites **Tegelikud** ja **Töölehe kanne**. Kasutage kohandatud koodi, et edastada valitud välja väärtuse töölehe rea kaudu ajakirjest tegelikele näitajatele, kasutades kande päritolu. Lisateavet kannete päritolu ja ühenduste kohta vaadake teemast [Tegelike näitajate seostamine algsete kirjetega](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Töölehe read ja põhikulu esitamine

Lisateavet kulukirje kohta vaadake teemast [Kulu ülevaade](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Aeg ja materjalid

Kui esitatud põhikulu kirje on seotud projektiga, mis on vastendatud mõne aja ja materjali lepingureaga, loob süsteem kaks töölehe rida – ühe kulu ja ühe arveldamata müügi jaoks.

### <a name="fixed-price"></a>Fikseeritud hind

Kui esitatud põhikulu kirje on ühendatud projektiga, mis on vastendatud fikseeritud hinnaga lepingureaga, loob süsteem ühe töölehe rea ainult kulu jaoks.

### <a name="default-pricing"></a>Vaikimisi hinnakujundus

Kulude vaikehindade sisestamise loogika põhineb kulukategoorial. Sobiva hinnakirja määratlemiseks kasutatakse tehingu kuupäeva, lepingurida, millega projekt on vastendatud, ja valuutat. Vaikimisi hinnakujundust mõjutavaod välju (nt **tehingukategooria** ja **ressursiüksus**) kasutatakse töölehe rea sobiva hinna kindlakstegemiseks. Samas toimib see ainult juhul, kui hinnakirjas on hinnakujundusmeetodiks **Ühiku hind**. Kui hinnakujundusmeetodiks on **Kulu** või **Hinnalisand kulule**, kasutatakse kulukirje loomisel sisestatud hinda kulude jaoks ja müügiesindaja rea hind arvutatakse hinnakujundusmeetodi põhjal. 

Saate lisata kulukirjele kohandatud välja. Kui soovite kanda välja väärtuse tegelikele väärtustele, looge väli tabelites **Tegelikud** ja **Töölehe kanne**. Kasutage kohandatud koodi, et edastada valitud välja väärtuse töölehe rea kaudu ajakirjest tegelikele näitajatele, kasutades kande päritolu. Lisateavet kannete päritolu ja ühenduste kohta vaadake teemast [Tegelike näitajate seostamine algsete kirjetega](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Töölehe kanded ja materjali kasutuslogi esitamine

Lisateavet kulukirje kohta vaadake teemast [Materjalide kasutuslogi](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Aeg ja materjalid

Kui edastatud materjalide kasutuslogi kirje on seotud aja ja materjalide lepingureaga vastendatud projektiga, loob süsteem kaks tekstirida – ühe kulu ja ühe tasustamata müügi jaoks.

### <a name="fixed-price"></a>Fikseeritud hind

Kui esitatud materjali kasutuslogi kirje on ühendatud projektiga, mis on vastendatud fikseeritud hinnaga lepingureaga, loob süsteem ühe töölehe rea ainult kulu jaoks.

### <a name="default-pricing"></a>Vaikimisi hinnakujundus

Materjali vaikehindade sisestamise loogika põhineb tootel ja ühikukombinatsioonil. Sobiva hinnakirja määratlemiseks kasutatakse tehingu kuupäeva, lepingurida, millega projekt on vastendatud, ja valuutat. Vaikimisi hinnakujundust mõjutavaod välju (nt **toote ID** ja **ressursiüksus**) kasutatakse töölehe rea sobiva hinna kindlakstegemiseks. Kuid see toimib ainult kataloogitoodete puhul. Sisestatavate toodete puhul kasutatakse materjalide kasutuslogi kirje loomisel sisestatud hinda töölehe ridade kulu- ja müügihinnana. 

Saate lisata kirjele **Materjali kasutuslogi** kohandatud välja. Kui soovite kanda välja väärtuse tegelikele väärtustele, looge väli tabelites **Tegelikud** ja **Töölehe kanne**. Kasutage kohandatud koodi, et edastada valitud välja väärtuse töölehe rea kaudu ajakirjest tegelikele näitajatele, kasutades kande päritolu. Lisateavet kannete päritolu ja ühenduste kohta vaadake teemast [Tegelike näitajate seostamine algsete kirjetega](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Kirjete töölehtede kasutamine kulude kirjendamiseks

Saate kasutada töölehti kulu või tulu kirjendamiseks materjali-, tasu-, aja-, kulu- või maksukannete järgi. Töölehti saab kasutada järgmistel eesmärkidel.

- Viige tehingu tegelikud andmed teisest süsteemist Microsoft Dynamics 365 Project Operationsse üle.
- Muus süsteemis aset leidnud kulude kirjendamiseks. Need kulud võivad hõlmata hanke- või alltöövõtu kulusid.

> [!IMPORTANT]
> Rakendus ei kinnita töölege rea tüüpi ega töölehe reale sisestatud seotud hinnakirja. Seega peaksid tegelike näitajate loomiseks kasutama kirjete töölehti ainult kasutaja, kes on täielikult teadlik raamatupidamuslikust mõjust, mis tegelikel näitajatel projektile on. Selle töölehe tüübi mõju tõttu peaksite hoolikalt valima, kellel on kirjete töölehtede loomisele juurdepääs.

## <a name="record-actuals-based-on-project-events"></a>Projektisündmuste põhjal tegelike andmete kirjendamine

Project Operations salvestab projekti jooksul toimuvad finantstehingud. Need kanded kirjendatakse tegelike andmetena. Järgmistes tabelites on esitatud mitmesugused tegelike andmete tüübid, mis olenevad sellest, kas projekt on aja- ja materjalikulu või fikseeritud hinnaga projekt, mis on eelmüügi etapis, või on see sisemine projekt.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Ressurss kuulub projekti tellijaga samasse organisatsiooniüksusse

<table>
<thead>
<tr>
<th rowspan="3">Sündmus</th>
<th colspan="4">Arveldatav või müüdud projekt</th>
<th rowspan="3">Eelmüügi etapis projekt</th>
<th rowspan="3">Sisemine projekt</th>
</tr>
<tr>
<th colspan="2">Aeg ja materjalid</th>
<th colspan="2">Fikseeritud hind</th>
</tr>
<tr>
<th>Tegelikud</th>
<th>Tehingu valuuta</th>
<th>Fikseeritud hind</th>
<th>Tehingu valuuta</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ajakirje on loodud.</td>
<td colspan="6">Tegelike andmete olemites puudub tegevus</td>
</tr>
<tr>
<td>Ajakirje on esitatud.</td>
<td colspan="6">Tegelike andmete olemites puudub tegevus</td>
</tr>
<tr>
<td rowspan="2">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</td>
<td>Tegelik kulu</td>
<td>Lepingut sõlmiva üksuse valuuta</td>
<td rowspan="2">Tegelik kulu</td>
<td rowspan="2">Lepingut sõlmiva üksuse valuuta
<td rowspan="2">Tegelik kulu</td>
<td rowspan="2">Tegelik kulu</td>
</tr>
<tr>
<td>Arveldamata tegelik müük – arveldatav</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td rowspan="3">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</td>
<td>Tegelik kulu</td>
<td>Lepingut sõlmiva üksuse valuuta</td>
<td rowspan="3">Tegelik kulu</td>
<td rowspan="3">Lepingut sõlmiva üksuse valuuta</td>
<td rowspan="3">Tegelik kulu</td>
<td rowspan="3">Tegelik kulu</td>
</tr>
<tr>
<td>Arveldamata tegelik müük – uue koguse arveldus</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td>Arveldamata tegelik müük – mitte-arveldatav erinevus</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td rowspan="2">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</td>
<td>Arveldamata müügi tagasipööramine</td>
<td>Projektilepingu valuuta</td>
<td rowspan="2">Arveldatud müük vahekokkuvõtte jaoks</td>
<td rowspan="2">Projektilepingu valuuta</td>
<td rowspan="2">Pole rakendatav</td>
<td rowspan="2">Pole rakendatav</td>
</tr>
<tr>
<td>Arveldatud müük</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td rowspan="3">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</td>
<td>Arveldamata müügi tagasipööramine</td>
<td>Projektilepingu valuuta</td>
<td rowspan="3">Pole rakendatav</td>
<td rowspan="3">Pole rakendatav</td>
<td rowspan="3">Pole rakendatav</td>
<td rowspan="3">Pole rakendatav</td>
</tr>
<tr>
<td>Arveldatud müük – uue koguse arveldus</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td>Arveldatud müük – mitte-arveldatav erinevus</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td rowspan="2">Arvet parandatakse, et suurendada tasustatava kogust.</td>
<td>Arveldatud müük – tagasipööramine</td>
<td>Projektilepingu valuuta</td>
<td rowspan="5">
<ul>
<li>Arveldatud müük vahekokkuvõtete jaoks</li>
<li>Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></li>
</ul>
</td>
<td rowspan="5">Projektilepingu valuuta</td>
<td rowspan="5">Pole rakendatav</td>
<td rowspan="5">Pole rakendatav</td>
</tr>
<tr>
<td>Arveldatud müük</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td rowspan="3">Arvet parandatakse, et vähendada tasustatava kogust.</td>
<td>Arveldatud müük – tagasipööramine</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td>Arveldatud müük uue koguse jaoks</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td>Arveldatud müük – mitte-arveldatav erinevus</td>
<td>Projektilepingu valuuta</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Ressurss kuulub organisatsiooniüksusse, mis ei ole sama kui projekti tellija organisatsiooniüksus

<table>
<thead>
<tr>
<th rowspan="3">Sündmus</th>
<th colspan="4">Arveldatav või müüdud projekt</th>
<th rowspan="3">Eelmüügi etapis projekt</th>
<th rowspan="3">Sisemine projekt</th>
</tr>
<tr>
<th colspan="2">Aeg ja materjalid</th>
<th colspan="2">Fikseeritud hind</th>
</tr>
<tr>
<th>Tegelikud</th>
<th>Tehingu valuuta</th>
<th>Fikseeritud hind</th>
<th>Tehingu valuuta</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ajakirje on loodud.</td>
<td colspan="6">Tegelike andmete olemites puudub tegevus</td>
</tr>
<tr>
<td>Ajakirje on esitatud.</td>
<td colspan="6">Tegelike andmete olemites puudub tegevus</td>
</tr>
<tr>
<td rowspan="4">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</td>
<td>Tegelik kulu</td>
<td>Lepingut sõlmiva üksuse valuuta</td>
<td rowspan="4">Tegelik kulu</td>
<td rowspan="4">Lepingut sõlmiva üksuse valuuta</td>
<td rowspan="4">Tegelik kulu</td>
<td rowspan="4">Tegelik kulu</td>
</tr>
<tr>
<td>Arveldamata tegelik müük – arveldatav</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td>Ressursiühiku maksumus</td>
<td>Ressursiühiku valuuta</td>
</tr>
<tr>
<td>Organisatsiooniüksuste vaheline müük</td>
<td>Lepingut sõlmiva üksuse valuuta</td>
</tr>
<tr>
<td rowspan="5">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</td>
<td>Tegelik kulu</td>
<td>Lepingut sõlmiva üksuse valuuta</td>
<td rowspan="5">Tegelik kulu</td>
<td rowspan="5">Lepingut sõlmiva üksuse valuuta</td>
<td rowspan="5">Tegelik kulu</td>
<td rowspan="5">Tegelik kulu</td>
</tr>
<tr>
<td>Ressursiühiku maksumus</td>
<td>Ressursiühiku valuuta</td>
</tr>
<tr>
<td>Organisatsiooniüksuste vaheline müük</td>
<td>Lepingut sõlmiva üksuse valuuta</td>
</tr>
<tr>
<td>Arveldamata tegelik müük – uue koguse arveldus</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td>Arveldamata tegelik müük – mitte-arveldatav erinevus</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td rowspan="2">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</td>
<td>Arveldamata müügi tagasipööramine</td>
<td>Projektilepingu valuuta</td>
<td rowspan="2">Arveldatud müük vahekokkuvõtte jaoks</td>
<td rowspan="2">Projektilepingu valuuta</td>
<td rowspan="2">Pole rakendatav</td>
<td rowspan="2">Pole rakendatav</td>
</tr>
<tr>
<td>Arveldatud müük</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td rowspan="3">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</td>
<td>Arveldamata müügi tagasipööramine</td>
<td>Projektilepingu valuuta</td>
<td rowspan="3">Pole rakendatav</td>
<td rowspan="3">Pole rakendatav</td>
<td rowspan="3">Pole rakendatav</td>
<td rowspan="3">Pole rakendatav</td>
</tr>
<tr>
<td>Arveldatud müük – uue koguse arveldus</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td>Arveldatud müük – mitte-arveldatav erinevus</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td rowspan="2">Arvet parandatakse, et suurendada tasustatava kogust.</td>
<td>Arveldatud müük – tagasipööramine</td>
<td>Projektilepingu valuuta</td>
<td rowspan="5">
<ul>
<li>Arveldatud müük vahekokkuvõtete jaoks</li>
<li>Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></li>
</ul>
</td>
<td rowspan="5">Projektilepingu valuuta</td>
<td rowspan="5">Pole rakendatav</td>
<td rowspan="5">Pole rakendatav</td>
</tr>
<tr>
<td>Arveldatud müük</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td rowspan="3">Arvet parandatakse, et vähendada tasustatava kogust.</td>
<td>Arveldatud müük – tagasipööramine</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td>Arveldatud müük uue koguse jaoks</td>
<td>Projektilepingu valuuta</td>
</tr>
<tr>
<td>Arveldatud müük – mitte-arveldatav erinevus</td>
<td>Projektilepingu valuuta</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
