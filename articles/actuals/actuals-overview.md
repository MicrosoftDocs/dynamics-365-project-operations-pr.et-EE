---
title: Tegelikud näitajad
description: See teema sisaldab teavet selle kohta, kuidas töötada rakenduses Microsoft Dynamics 365 Project Operations tegelike näitajatega.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074946"
---
# <a name="actuals"></a>Tegelikud näitajad 

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Tegelikud andmed on projektiga lõpule viidud tööd. Need luuakse aja- ja kulukirjete ja ning töölehe kannete ja arvete tulemusena.

## <a name="journal-lines-and-time-submission"></a>Töölehe read ja aja esitamine

Lisateavet ajakirje kohta vaadake teemast [Ajakirje ülevaade](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Aeg ja materjalid

Kui esitatud ajakirje on seotud projektiga, mis on vastendatud mõne aja ja materjali lepingureaga, loob süsteem kaks töölehe rida – ühe kulu ja ühe arveldamata müügi jaoks.

### <a name="fixed-price"></a>Fikseeritud hind

Kui esitatav ajakirje seotakse projektiga, mis on vastendatud fikseeritud hinnaga lepingureaga, loob süsteem ühe töölehe rea kulu jaoks.

### <a name="default-pricing"></a>Vaikimisi hinnakujundus

Vaikehindade looise loogika asub töölehe real. Ajakirje välja väärtused kopeeritakse töölehe reale. Need väärtused hõlmavad tehingu kuupäeva, lepingurida, millega projekt on vastendatud, ja vastava hinnakirja valuutat.

Vaikimisi hinnakujundust mõjutavaid välju (nt **Roll** ja **Organisatsiooniüksus** ) kasutatakse töölehe rea vastava hinna määratlemiseks. Saate lisada ajakirjele kohandatud välja. Kui soovite, et väljale oleks kantud tegelikud väärtused, looge tegelikes olemites väli ja kasutage välja vastendusi, et kopeerida väli ajakirjest tegelikule.

## <a name="journal-lines-and-basic-expense-submission"></a>Töölehe read ja põhikulu esitamine

Lisateavet kulukirje kohta vaadake teemast [Kulu ülevaade](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Aeg ja materjalid

Kui esitatud põhikulu kirje on seotud projektiga, mis on vastendatud mõne aja ja materjali lepingureaga, loob süsteem kaks töölehe rida – ühe kulu ja ühe arveldamata müügi jaoks.

### <a name="fixed-price"></a>Fikseeritud hind

Kui esitatav põhikulu kirje seotakse projektiga, mis on vastendatud fikseeritud hinnaga lepingureaga, loob süsteem ühe töölehe rea kulu jaoks.

### <a name="default-pricing"></a>Vaikimisi hinnakujundus

Kulude vaikehindade sisestamise loogika põhineb kulukategoorial. Sobiva hinnakirja määratlemiseks kasutatakse tehingu kuupäeva, lepingurida, millega projekt on vastendatud ja valuutat. Samas vaikimisi määratakse hinna enda jaoks sisestatav summa otse kulu ja müügiga seotud kulu töölehe ridadel.

Kategoorial põhinev ühiku vaikehinna kanne pole saadaval.

## <a name="use-entry-journals-to-record-costs"></a>Kirjete töölehtede kasutamine kulude kirjendamiseks

Saate kasutada töölehti kulu või tulu kirjendamiseks materjali-, tasu-, aja-, kulu- või maksukannete järgi. Töölehti saab kasutada järgmistel eesmärkidel.

- Projektiga seotud tegeliku materjalikulu ja müügi kirjendamiseks.
- Tehingu tegelike andmete teistest süsteemist rakendusse Microsoft Dynamics 365 Project Operations üle viimiseks.
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
