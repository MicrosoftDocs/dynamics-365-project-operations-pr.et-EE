---
title: Tegelike näitajate ülevaade
description: Selles teemas antakse teavet projektiga seotud tegelike andmete kohta.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cbb3e5c7f74cdf37ae4d259687bf7a98102a8131
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368156"
---
# <a name="actuals-overview"></a>Tegelike näitajate ülevaade

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tegelikud andmed on projektiga lõpule viidud tööd. Projekti tegelikke andmeid saab tuvastada nende alusdokumendi kaudu. Alusdokumendid sisaldavad aja-, kulu- ja töölehe kandeid, aga ka arveid.

![Kuidas projekti tegelikud andmed alusdokumentidega ühendatakse?](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Ajakirje esitamisel

Kui ajakirje esitatakse projekti jaoks, mis on vastendatud aja- ja materjalide töölehe reaga, luuakse rakenduses PSA kaks töölehe rida. Üks rida on kulu ja teine rida müükide jaoks, mille kohta pole veel arvet. Kui ajakirje esitatakse projekti jaoks, mis on vastendatud fikseeritud hinnaga lepingureaga, luuakse töölehe rida ainult kulu jaoks. 

Vaikehindade sisestamise loogika asub töölehe real. Kõik ajakirje välja väärtused kopeeritakse töölehe reale. Need väljad hõlmavad tehingu kuupäeva, lepingurida, millega projekt on vastendatud, ja vastava hinnakirja valuutat. 

Vaikehindu mõjutavate väljade (nt **roll** ja **organisatsiooniüksus**) töölehe reale sisestatakse sobivad hinnad vaikimisi. Kui lisate ajakirjele kohandatud välja ning soovite, et väljale oleks kantud tegelikud väärtused, looge tegelikes olemites väli ja kasutage välja vastendusi, et kopeerida väli ajakirjest tegelikule.

## <a name="submitting-an-expense-entry"></a>Kulukirje esitamine

Kui kulukirje esitatakse projekti jaoks, mis on vastendatud aja- ja materjali lepingureaga, luuakse rakenduses PSA kaks töölehe rida. Üks rida on kulu ja teine rida müükide jaoks, mille kohta pole veel arvet. Kui fikseeritud hinnaga sisestus esitatakse projektile, mis on vastendatud fikseeritud hinnaga lepingureaga, luuakse töölehe rida ainult kulu jaoks.

Kulude vaikehindade sisestamise loogika põhineb kulukategoorial, mis on lehe jaotises **Kulukirje**. Sobiva hinnakirja määratlemiseks kasutatakse tehingu kuupäeva, lepingurida, millega projekt on vastendatud ja valuutat. Hinna enda jaoks on kasutaja sisestatud suurus kulude ja müügi jaoks vaikimisi määratud otse seotud kulukirje töölehe ridadel.

PSA praeguses versioonis ei ole kategoorial põhinev ühiku vaikehinna kanne saadaval.

## <a name="using-entry-journals-to-record-costs"></a>Kulude kirjendamiseks kirjete töölehtede kasutamine

PSA-s võimaldavad kirje töölehed teil kirjendada kulu või tulu materjali-, tasu-, aja-, kulu- või maksukannete järgi. Töölehel on päis, read ja toiming **Kinnita**. Toome mõned näited, kus võiksite töölehte kasutada.

- Peate kirjendma projektiga seotud tegelikku materjalikulu ja müüki.
- Peate tehingu tegelikud andmed teistest süsteemist PSA-sse üle viima.
- Peate kirjendama mõnes muus süsteemis aset leidnud kulusid (nt hanke- või alltöövõtu kulud).

> [!IMPORTANT]
> Tegelike näitajate loomiseks kirje töölehtede kasutamine peaks olema tehtav ainult kasutajate poolt, kes on täielikult teadlikud projektis tegelike näitajate mõjust raamatupidamisele. Selle põhjuseks on, et rakendus ei kontrolli töölehe rea tüüpi ega seotud hinda, mis on töölehe reale sisestatud. Selle töölehe tüübi mõju tõttu olge hästi ettevaatlik, et kellele kirje töölehtede loomisele juurdepääs antakse.     


## <a name="recording-actuals-based-on-project-events"></a>Projektisündmustel põhinevate tegelike andmete kirjendamine

PSA salvestab projekti jooksul toimuvad finantstehingud. Need kanded kirjendatakse **tegelike andmetena**. Järgmistes tabelites on esitatud mitmesugused tegelike andmete tüübid, mis olenevad sellest, kas projekt on aja- ja materjalikulu või fikseeritud hinnaga projekt, mis on eelmüügi etapis, või on see sisemine projekt.

**Ressurss kuulub projekti tellijaga samasse organisatsiooniüksusse**

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

**Ressurss kuulub organisatsiooniüksusse, mis ei ole sama kui projekti tellija organisatsiooniüksus**

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