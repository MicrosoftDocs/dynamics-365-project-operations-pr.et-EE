---
title: Tegelike näitajate seostamine algsete kirjetega
description: Selles teemas kirjeldatakse, kuidas siduda tegelikud andmed algsete kirjetega (nt ajakirje, kulukirje või materjalide kasutuslogid).
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9fc49211f3c2c79e18f6dd18e9a687091793cad0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996741"
---
# <a name="link-actuals-to-original-records"></a>Tegelike näitajate seostamine algsete kirjetega

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


Rakenduses Dynamics 365 Project Operations on *äritehing* abstraktne mõiste, mida olem ei esinda. Mõned olemite levinumad väljad ja protsessid on aga mõeldud äritehingute mõiste kasutamiseks. Järgmised olemid kasutavad seda kontseptsiooni.

- Hinnapakkumise rea üksikasjad
- Lepingurea üksikasjad
- Hinnangu read
- Töölehe read
- Tegelikud

Nende olemite seas **hinnapakkumise rea üksikasjade**, **lepingurea üksikasjade** ja **hinnangu read** vastendatakse projekti töötsükli prognoosi etapiga. **Töölehe read** ja **Tegelikud olemid** vastendatakse projekti töötsükli täitmise etapiga.

Project Operations tuvastab kirjed nendes viies olemis äritehingutena. Ainus erinevus on see, et olemite kirjeid, mis on vastendatud prognoosi etapiga, loetakse finantsprognoosideks, kuid olemite kirjeid, mis on vastendatud täitmise etappidega, loetakse juba toimunud finantsfaktideks.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Ärikannetele kordumatud mõisted
Järgmised mõisted on äritehingute mõiste jaoks kordumatud.

- Tehingu tüüp
- Tehingu klass
- Tehingu päritolu
- Tehingu seos

### <a name="transaction-type"></a>Tehingu tüüp

Tehingu tüüp tähistab projekti finantsmõju ajastust ja konteksti. Seda tähistab suvandikomplekt, millel on Project Operationsis järgmised toetatud väärtused.

  - Kulu
  - Projekti leping
  - Arveldamata müük
  - Arveldatud müük
  - Organisatsioonidevaheline müük
  - Ressursiühiku maksumus

### <a name="transaction-class"></a>Tehingu klass

Tehingu klass tähistab erinevat tüüpi kulusid, mis on seotud projektidega. Seda tähistab suvandikomplekt, millel on Project Operationsis järgmised toetatud väärtused.

  - Aeg
  - Kulu
  - Materjal
  - Tasu
  - Vahe-eesmärk
  - Maks

Äriloogika kasutab suvandit **Vahekokkuvõte** tavaliselt Project Operationsis fikseeritud hinnaga arvete puhul.

### <a name="transaction-origin"></a>Kande päritolu

**Kande päritolu** on olem, mis talletab iga äritehingu päritolu. Kuna projekt algab, tekitab iga äritehing teise äritehingu, mis omakorda loob uue jne. Tehingu päritolu olem on välja töötatud selleks, et talletada andmeid iga tehingu päritolu kohta, et aidata aruandluse ja jälgimisega. 

### <a name="transaction-connection"></a>Tehingu seos

**Tehingu seos** on olem, mis talletab kahe sarnase äritehingu (nt kulu ja seotud müügi tegelikud näitajad) vahelisi seoseid või tehingu tagasipöördumist, mis käivitatakse arveldamise tegevuste (nt arve kinnituse või arve korrektsiooni) alusel.

Olemid **Tehingu päritolu** ja **Tehingu seos** aitavad koos jälgida äritehingute ning toimingute vahelisi seoseid, mis põhjustavad kindla äritehingu loomist.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Näide: kuidas tehingu päritolu töötab koos tehingu seosega

Järgmises näites on toodud ajakannete tüüpiline töötlemine Project Operationsi projekti töötsüklis.

> ![Töötlemise ajakirjed Project Service’i teenusetsüklis](media/basic-guide-17.png)
 
1. Ajakirje esitamine loob kaks töölehe rida: üks rida kulu ja üks rida arveldamata müügi jaoks.
2. Ajakirje lõplik kinnitamine loob kaks tegelikku versiooni: üks tegelik väärtus kulu ja teine tegelik väärtus arveldamata müügi jaoks.
3. Kui luuakse uus projekti arve, luuakse arverea tehing, kasutades arveldamata müügi tegelikke andmeid. 
4. Pärast arve kinnitamist luuakse kaks uut tegelikku versiooni: arveldamata müügi tühistamise tegelik ja arveldatud müügi tegelik.

Kõik need sündmused loovad kirje olemites **Tehingu päritolu** ja **Tehingu seos**. Need uued kirjed aitavad luua kirjete vaheliste seoste ajaloo, mis loodi ajakirje, töölehe rea, tegelike ja arverea üksikasjade üleselt.

Järgmises tabelis on toodud töövoo olemi **Tehingu päritolu** kirjed.

| Üritus                        | Päritolu                   | Päritolu tüüp                       | Kanne                       | Tehingu tüüp         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Edasta ajakirje        | Ajakirje kirje GUID   | Ajakirje                        | Töölehe rea kirje GUID (kulu)   | Töölehe rida             |
| Ajakirje kirje GUID       | Ajakirje               | Töölehe rea kirje GUID (müük)  | Töölehe rida                      |                          |
| Kinnitatud aeg                | Töölehe rea kirje GUID (kulu) | Töölehe rida                      | Arveldamata müügi kirje GUID        | Tegelik                   |
| Ajakirje kirje GUID       | Ajakirje               | Arveldamata müügi kirje GUID        | Tegelik                            |                          |
| Töölehe rea kirje GUID (kulu)     | Töölehe rida             | Tegelike kulude kirje GUID           | Tegelik                            |                          |
| Ajakirje kirje GUID       | Ajakirje               | Tegelike kulude kirje GUID           | Tegelik                            |                          |
| Arve loomine             | Ajakirje kirje GUID   | Ajakirje                        | Arve rea tehingu GUID     | Arve rea tehing |
| Töölehe rea kirje GUID (kulu)     | Töölehe rida             | Arve rea tehingu GUID     | Arve rea tehing          |                          |
| Arve kinnitamine         | Arve rea GUID        | Arve rida                      | Arveldatud müügi kirje GUID          | Tegelik                   |
| Arve GUID                 | Arve                  | Arveldatud müügi kirje GUID          | Tegelik                            |                          |
| Arve rea üksikasjade GUID     | Arve rea üksikasjad      | Arveldatud müügi kirje GUID          | Tegelik                            |                          |
| Ajakirje kirje GUID       | Ajakirje               | Arveldatud müügi kirje GUID          | Tegelik                            |                          |
| Töölehe rea kirje GUID (kulu)     | Töölehe rida             | Arveldatud müügi kirje GUID          | Tegelik                            |                          |
| Ajakirje kirje GUID       | Ajakirje               | Arveldamata müügi tagasipöörde GUID      | Tegelik                            |                          |
| Töölehe rea kirje GUID (kulu)     | Töölehe rida             | Arveldamata müügi tagasipöörde GUID      | Tegelik                            |                          |
| Arve paranduse mustand     | Vana arve rea üksikasja GUID             | Arve rea tehing          | Paranduse arve rea üksikasja GUID               | Arve rea tehing |
| Vana arve rea GUID                  | Arve rida             | Paranduse arve rea üksikasja GUID               | Arve rea tehing          |                          |
| Vana arve GUID             | Arve                  | Paranduse arve rea üksikasja GUID               | Arve rea tehing          |                          |
| Ajakirje kirje GUID       | Ajakirje               | Paranduse arve rea üksikasja GUID               | Arve rea tehing          |                          |
| Töölehe rea kirje GUID (kulu)     | Töölehe rida             | Paranduse arve rea üksikasja GUID               | Arve rea tehing          |                          |
| Kinnitatud arve parandus | Vana arve rea üksikasja GUID             | Arve rea tehing          | Tagasipööratud arveldatud müügi tegelik GUID | Tegelik                   |
| Vana arve rea GUID                  | Arve rida             | Tagasipööratud arveldatud müügi tegelik GUID | Tegelik                            |                          |
| Vana arve GUID             | Arve                  | Tagasipööratud arveldatud müügi tegelik GUID | Tegelik                            |                          |
| Ajakirje kirje GUID       | Ajakirje               | Tagasipööratud arveldatud müügi tegelik GUID | Tegelik                            |                          |
| Töölehe rea kirje GUID (kulu)     | Töölehe rida             | Tagasipööratud arveldatud müügi tegelik GUID | Tegelik                            |                          |
| Vana arve rea üksikasja GUID                 | Arve rea tehing | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |
| Vana arve rea GUID                  | Arve rida             | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |
| Vana arve GUID             | Arve                  | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |
| Ajakirje kirje GUID       | Ajakirje               | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |
| Töölehe rea kirje GUID (kulu)     | Töölehe rida             | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |
| Paranduse arve rea üksikasja GUID          | Arve rea tehing | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |
| Paranduse arve rea GUID           | Arve rida             | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |
| Parandatud arve GUID      | Arve                  | Uus arveldamata müügi tegelik GUID    | Tegelik                            |                          |

Järgmises tabelis on toodud töövoo olemi **Tehingu seos** kirjed.

| Üritus                          | Kanne 1                 | Tehingu 1 roll | Tehingu 1 tüüp           | Kanne 2                | Tehingu 2 roll | Tehingu 2 tüüp |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Edasta ajakirje          | Töölehe rea (müük) GUID     | Arveldamata müük     | msdyn_journalline            | Töölehe rea (kulu) GUID     | Kulu               | msdyn_journalline  |
| Kinnitatud aeg                  | Arveldamata tegelik (müük) GUID  | Arveldamata müük     | msdyn_actual                 | Tegelike kulu (kulu) GUID       | Kulu               | msdyn_actual       |
| Arve loomine               | Arve rea üksikasjade GUID      | Arveldatud müük       | msdyn_invoicelinetransaction | Arveldamata müügi tegelik GUID   | Arveldamata müük     | msdyn_actual       |
| Arve kinnitamine           | Tegeliku GUID tagasipööramine         | Tagasipööramine          | msdyn_actual                 | Originaalne arveldamata müügi GUID | Algne           | msdyn_actual       |
| Arveldatud müügi GUID              | Arveldatud müük                  | msdyn_actual       | Arveldamata müügi tegelik GUID   | Arveldamata müük               | msdyn_actual       |                    |
| Arve paranduse mustand       | Arve rea tehingu GUID | Asendamine          | msdyn_invoicelinetransaction | Arveldatud müügi GUID            | Algne           | msdyn_actual       |
| Arve parandamise kinnitamine     | Arveldatud müügi tagasipööramise GUID    | Tagasipööramine          | msdyn_actual                 | Arveldatud müügi GUID            | Algne           | msdyn_actual       |
| Uus arveldamata müügi tegelik GUID | Asendamine                     | msdyn_actual       | Arveldatud müügi GUID            | Algne                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
