---
title: Projekti ajakava API jõudlus
description: See artikkel annab teavet projekti ajakava API-de jõudluse võrdlustestide kohta ja tuuakse välja head tavad optimaalseks kasutamiseks.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911177"
---
# <a name="project-schedule-api-performance"></a>Projekti ajakava API jõudlus

_**Kehtiv järgnevale:** Project Operations ressursi-/mitteressursipõhised stsenaariumid, lihtjuurutus – tehing näidisarveldusele, Project for the web_

See artikkel annab teavet projekti ajakava rakenduse programmeerimisliideste (API-de) jõudluse võrdlustestide kohta ja tuuakse välja head tavad kasutamise optimeerimiseks.

## <a name="project-scheduling-service"></a>Projekti kavandamise teenus
Projekti kavandamise teenus on mitme rentnikuga teenus, mis töötab teenuses Microsoft Azure. See on mõeldud suhtluse parandamiseks, pakkudes kasutajatele projektidega töötades kiiret ja sujuvat kogemust. See täiustus saavutatakse muutmise taotluste kinnitamise, nende töötlemise ja tulemuse kohese tagastamise kaudu. Teenus püsib asünkroonselt rakenduses Dataverse ja ei takista kasutajatel muid toiminguid tegemast.

Projekti ajakava API-d sõltuvad projekti kavandamise teenusest taotluste käitamisel, mida on täpsemalt kirjeldatud selle artikli hilisemates jaotistes.

Projekti ajakava API-d on välja töötatud nii, et need töötaksid järgmiste tööjaotuse struktuuri (WBS) olemitega.

  - Project
  - Projekti ülesanne
  - Projekti ülesande sõltuvus
  - Projektimeeskonna liige
  - Ressursi määramine
  
Toetatakse nii valmisvälju kui ka kohandatud välju. Kui pole teisiti märgitud, toetatakse kõiki levinud toiminguid (nt loomine, värskendamine ja kustutamine). Lisateavet leiate teemast [Projekti ajakava API-de kasutamine toimingute tegemiseks ja olemite kavandamiseks](schedule-api-preview.md).

Projekti ajakava API-de osana on lisatud tööüksuse muster. Muster on tuntud kui OperationSet ja seda saab kasutada, kui ühes tehingus tuleb töödelda mitut taotlust.

Järgmisel joonisel on kujutatud voog, mida partner selle funktsiooni kasutamisel kogeb.

![Dataverse’i ja projekti kavandamise teenuse voog.](./media/dataverse-project-scheduling-service-flow.png)

**1. etapp**: klient teeb API kutse avatud andmete protokolli (OData) lõpp-punktile rakenduses Dataverse, et luua OperationSet.

**2. etapp**: pärast uue OperationSeti loomist tagastatakse väärtus **OperationSetId**.

**3. etapp**: klient kasutab väärtust **OperationSetId** uue projekti ajakava API taotluse tegemiseks. Tulemuseks on ajastatavas olemis loomise, värskendamise või kustutamise taotlus. Taotluse tegemisel tehakse metaandmete valideerimine. Valideerimise nurjumisel taotlus lõpetatakse ja tagastatakse tõrge.

**Etapid 4a–4c**: need etapid tähistavad NÕUSTUMISE faasi. Klient kutsub API **ExecuteOperationSetV1**, mis saadab kõik projekti kavandamise teenusele tehtud muudatused ühe partiina. Projekti kavandamise teenus käivitab partiis taotluste jaoks enda valideerimised. Mis tahes valideerimistõrked tühistavad partii ja tagastavad helistajale erandi. Kui projekti kavandamise teenus partii kinnitab, värskendatakse OperationSeti olekut, et see kajastaks asjaolu, et projekti kavandamise teenus töötleb OperationSeti.

**5. etapp**: see etapp tähistab PÜSIMISE faasi. Projekti kavandamise teenus kirjutab partii tehingu kaudu asünkroonselt rakendusse Dataverse. Kui kirjutustoiming õnnestub, märgitakse OperationSeti olekuks **Lõpule viidud**. Mis tahes tõrked pööravad tehingu ja partii tagasi ning OperationSeti olekuks märgitakse **Nurjunud**.

## <a name="performance-methodology"></a>Jõudluse metoodika
Täitmisaeg on määratletud kui aeg alates API **ExecuteOperationSetV1** kutsest kuni projekti kavandamise teenus lõpetab kirjutamise rakendusse Dataverse. Kõiki toiminguid käitatakse kombineeritult 2200 korda ja esitatakse P99 täitmisaja mõõtmised. Mõõdetakse ühe kirje ja hulgitoiminguid.

Ühe kirje toimingu puhul sisaldab OperationSet ühte taotlust. Hulgitoimingute korral sisaldab see 20, 50 või 100 taotlust. Iga hulgitoimingu maht esitatakse eraldi.

Neid toimingud käitatakse Põhja-Ameerikas juurutusel UR 15 Project Operations Lite.

## <a name="results"></a>Tulemid
### <a name="create-operations"></a>Toimingute loomine
#### <a name="single-record-create-operations"></a>Toimingute loomine ühe kirje kaupa
Järgmises tabelis on toodud ühe kirje loomise täitmisajad. Ajad on toodud sekundites.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Kirje&nbsp;&nbsp;&nbsp;tüüp</th>
    <th class="tg-0lax" colspan="2">Aeg</th>
  </tr>
  <tr>
    <th class="tg-0lax">Kohustuslikud väljad</th>
    <th class="tg-0lax">Kõik toetatud väljad</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Toiming</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Määramine</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Meeskonnaliige</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Sõltuvus</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Toimingute loomine hulgi
Järgmises tabelis on toodud mitme kirje loomise täitmisajad. Täpsemalt mõõtis Microsoft 20, 50 ja 100 kirje loomise täitmisaegu ühes OperationSetis. Ajad on toodud sekundites.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Kirje&nbsp;&nbsp;&nbsp;tüüp</th>
    <th class="tg-0lax" colspan="6">Aeg</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 kirjet</th>
    <th class="tg-0lax" colspan="2">50 kirjet</th>
    <th class="tg-0lax" colspan="2">100 kirjet</th>
  </tr>
  <tr>
    <th class="tg-0lax">Kohustuslikud väljad</th>
    <th class="tg-0lax">Kõik toetatud väljad</th>
    <th class="tg-0lax">Kohustuslikud väljad</th>
    <th class="tg-0lax">Kõik toetatud väljad</th>
    <th class="tg-0lax">Kohustuslikud väljad</th>
    <th class="tg-0lax">Kõik toetatud väljad</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Toiming</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Määramine</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Sõltuvus</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Sellesse tabelisse pole kaasatud olemite **Projekt** ja **Meeskonnaliige** toimingute hulgiloomist, kuna nende toimingute käitusaeg sarnaneb sellele käitusajale, kui ühe kirje loomise API-t kutsutakse mitu korda. Need API-d käivitatakse kohe rakenduses Dataverse.

Järgmisel joonisel on esitatud olemite **Ülesanne**, **Määramine** ja **Sõltuvus** täitmisaegade plaan, kui luuakse 20, 50 ja 100 kirjet ning kasutatakse kõiki toetatud välju.

![Kirje loomise täitmise ajagraafik.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Toimingute värskendamine
#### <a name="single-record-update-operations"></a>Toimingute värskendamine ühe kirje kaupa
Järgmises tabelis on toodud ühe kirje värskendamise täitmisajad. Ajad on toodud sekundites.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Kirje&nbsp;&nbsp;&nbsp;tüüp</th>
    <th class="tg-0lax" colspan="2">Aeg</th>
  </tr>
  <tr>
    <th class="tg-0lax">Kohustuslikud väljad </th>
    <th class="tg-0lax">Kõik toetatud väljad</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Toiming</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Meeskonnaliige</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Värskendamistoimingud olemites **Ressursimääramised** ja **Projekti ülesande sõltuvus** pole toetatud.

#### <a name="bulk-update-operations"></a>Toimingute värskendamine hulgi
Järgmises tabelis on toodud mitme kirje värskendamise täitmisajad. Täpsemalt mõõtis Microsoft 20, 50 ja 100 kirje värskendamise täitmisaegu ühes OperationSetis. Ajad on toodud sekundites.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Kirje&nbsp;&nbsp;&nbsp;tüüp</th>
    <th class="tg-0lax" colspan="6">Aeg</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 kirjet</th>
    <th class="tg-0lax" colspan="2">50 kirjet</th>
    <th class="tg-0lax" colspan="2">100 kirjet</th>
  </tr>
  <tr>
    <th class="tg-0lax">Kohustuslikud väljad</th>
    <th class="tg-0lax">Kõik toetatud väljad</th>
    <th class="tg-0lax">Kohustuslikud väljad</th>
    <th class="tg-0lax">Kõik toetatud väljad</th>
    <th class="tg-0lax">Kohustuslikud väljad</th>
    <th class="tg-0lax">Kõik toetatud väljad</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Toiming</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Meeskonnaliige</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Värskendamistoimingud olemites **Ressursimääramised** ja **Projekti ülesande sõltuvus** pole toetatud.

Järgmisel joonisel on esitatud olemite Ülesanne ja Meeskonnaliige täitmisaegade plaan, kui värskendatakse 20, 50 ja 100 kirjet ning kasutatakse kõiki toetatud välju.

![Kirje värskendamise täitmise ajagraafik.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Toimingute kustutamine
#### <a name="single-record-delete-operations"></a>Toimingute kustutamine ühe kirje kaupa
Järgmises tabelis on toodud ühe kirje kustutamise täitmisajad. Ajad on toodud sekundites.

| Kirje tüüp | Aeg  |
|-------------|-------|
| Toiming        | 20.12 |
| Määramine  | 10.86 |
| Meeskonnaliige | 12.52 |
| Sõltuvus  | 20.89 |

> [!NOTE]
> Olemi **Projekt** kustutamistoimingud pole toetatud.

#### <a name="bulk-delete-operations"></a>Toimingute hulgi kustutamine
Järgmises tabelis on toodud mitme kirje kustutamise täitmisajad. Täpsemalt mõõtis Microsoft 20, 50 ja 100 kirje kustutamise täitmisaegu ühes OperationSetis. Ajad on toodud sekundites.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Kirje&nbsp;&nbsp;&nbsp;tüüp</th>
    <th class="tg-0lax" colspan="3">Aeg</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 kirjet</th>
    <th class="tg-0lax">50 kirjet</th>
    <th class="tg-0lax">100 kirjet</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Toiming</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Määramine</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Meeskonnaliige</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Sõltuvus</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Olemi **Projekt** kustutamistoimingud pole toetatud.

Järgmisel joonisel on esitatud olemite **Ülesanne**, **Määramine**, **Meeskonnaliige** ja **Sõltuvus** täitmisaegade plaan, kui kustutatakse 20, 50 ja 100 kirjet.

![Kirje kustutamise täitmise ajagraafik.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Tähelepanekud
Iga kirje toimingu puhul kulub API-l **ExecuteOperationSet** umbes 800 millisekundit taotluse saatmiseks projekti kavandamise teenusele. Seejärel kulub projekti kavandamise teenusel lasti töötlemiseks ja Dataverse’i kutsumiseks ligikaudu viis sekundit. Ülejäänud täitmisaeg kulub äriloogika käitamisele ja andmete kirjutamisele andmebaasi rakenduses Dataverse.

Kui luuakse, värskendatakse või kustutatakse 100 kirjet, kulub API-l **ExecuteOperationSet** aega umbes kolm sekundit, et saata taotlus projekti kavandamise teenusele. Seejärel kulub projekti kavandamise teenusel taotluste töötlemiseks ja Dataverse’i kutsumiseks ligikaudu viis sekundit. Hulgitoimingud peavad tasuma **projekti kavandamise teenuse maksu** üks kord kõigi OperationSetis olevate kirjete eest. Seetõttu on hulgitoimingute keskmine täitmisaeg oluliselt väiksem kui ühe kirjega toimingutel.

## <a name="scenarios"></a>Stsenaariumid
Järgmises tabelis on toodud täitmisajad, kui projekti ajakava API-sid kasutatakse teatud stsenaariumite saavutamiseks. Ajad on toodud sekundites.

| Stsenaarium                                                                   | Aeg  |
|----------------------------------------------------------------------------|-------|
| Looge 40 ülesandega projekt.                                      | 36.01 |
| Looge 40 ülesande ja 20 sõltuvusega projekt.                  | 38.11 |
| Looge 40 ülesande ja 30 määramisega projekt.                   | 60.17 |
| Looge 40 ülesande, 20 sõltuvuse ja 30 määramisega projekt. | 60.27 |

## <a name="best-practices"></a>Head tavad
Eelnevate stsenaariumite tulemuste põhjal toimivad API-d paremini järgmistes tingimustes.

  - Rühmitage nii palju toiminguid kui võimalik. Hulgitoimingute keskmine käitusaeg on parem, kui ühe kirjega toimingute keskmine käitusaeg. Mida väiksem on kasutusel olevate OperationSetide arv, seda kiirem on keskmine täitmisaeg.
  - Määrake stsenaariumi saavutamiseks ainult vajalikud miinimumatribuudid. Olge valiv, milliseid mittenõutud väljade tüüpe OperationSeti taotlusse kaasate. Väljad, mis sisaldavad võõrvõtmeid või ümberarvestusvälju, mõjutavad jõudlust negatiivselt.
