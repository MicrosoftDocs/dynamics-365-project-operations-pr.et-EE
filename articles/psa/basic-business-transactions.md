---
title: Äritehingud
description: Selles teemas antakse teavet äritehingute kohta.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 68506142c5cd046806bc085f297ac928b0c94440
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291209"
---
# <a name="business-transactions"></a>Äritehingud

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Rakenduses Dynamics 365 Project Service Automation on *äritehing* abstraktne mõiste, mida ei esinda ükski olem. Mõned olemite levinumad väljad ja protsessid on aga mõeldud äritehingute mõiste kasutamiseks. Järgmised olemid kasutavad seda ülevaadet.

- Hinnapakkumise rea üksikasjad
- Lepingurea üksikasjad
- Hinnangu read
- Töölehe read
- Tegelikud

Nende olemite, hinnapakkumise rea üksikasjade, lepingurea üksikasjade ja hinnangu read vastendatakse projekti töötsükli prognoosi etapiga. Töölehe read ja tegelikud olemid vastendatakse projekti töötsükli täitmise etapiga.

PSA kohtleb kirjeid neid viies olemis äritehingutena. Ainus erinevus on see, et olemite kirjeid, mis on vastendatud hindamise etapiga, loetakse finantsprognoosideks, kuid olemite kirjeid, mis on vastendatud täitmise etappidega, loetakse juba toimunud finantsfaktideks.

Lisateavet leiate teemast [Hinnangud](estimates.md) ja [Tegelikud](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Ärikannetele kordumatud mõisted
Järgmised mõisted on äritehingute mõiste jaoks kordumatud.

- Tehingu tüüp
- Tehingu klass
- Tehingu päritolu
- Tehingu seos

### <a name="transaction-type"></a>Tehingu tüüp

Tehingu tüüp tähistab projekti finantsmõju ajastust ja konteksti. Seda tähistab suvandikomplekt, millel on PSA-s järgmised toetatud väärtused.
- Kulu
- Projektileping
- Arveldamata müük
- Arveldatud müük
- Organisatsioonidevaheline müük
- Ressursiühiku maksumus

### <a name="transaction-class"></a>Tehingu klass

Tehingu klass tähistab erinevat tüüpi kulusid, mis on seotud projektidega. Seda tähistab suvandikomplekt, millel on PSA-s järgmised toetatud väärtused.

- Time
- Kulu
- Materjal
- Tasu
- Vahe-eesmärk
- Maks

Väärtust **Vahekokkuvõte** kasutab äriloogika tavaliselt PSA-s fikseeritud hinnaga arvete puhul.

### <a name="transaction-origin"></a>Tehingu päritolu

Kande päritolu on olem, mis talletab iga äritehingu päritolu. Kui toimub projekti käivitamine, toob iga äritehing kaasa teis äritehingu, mis omakorda loob järgmise ja nii edasi. Tehingu päritolu olem on välja töötatud salvestama andmeid iga tehingu päritolu kohta, et aidata kaasa aruandlusele ja jälgitavusele. 

### <a name="transaction-connection"></a>Tehingu seos

Tehingu seos on olem, mis talletab kahe sarnase äritehingu (nt kulu ja seotud müügi tegelikud näitajad) vahelisi seoseid või tehingu tagasipöördumist, mis käivitatakse arveldamise tegevuste (nt arve kinnituse või arve korrektsiooni) alusel.

Koos saate tehingute päritolu ja tehingute seose olemite kaudu jälgida äritehingute ning toimingute vahelisi seoseid, mis põhjustavad kindla äritehingu loomist.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Näide: kuidas tehingu päritolu töötab koos tehingu seosega

Järgmises näites on toodud ajakannete tüüpiline töötlemine PSA projekti töötsüklis.

> ![Töötlemise ajakirjed Project Service’i teenusetsüklis](media/basic-guide-17.png)
 
1. Ajakirje esitamise põhjuseks on kahe töölehe rea loomine: üks kulu ja teine arveldamata müügi jaoks.
2. Ajakirje lõplik kinnitamine põhjustab kahe tegeliku versiooni loomise: üks kulu ja teine arveldamata müügi jaoks.
3. Kui kasutaja loob projekti arve, luuakse arverea tehing, kasutades arveldamata müügi tegelikke andmeid. 
4. Pärast arve kinnitamist luuakse kaks uut tegelikku versiooni: arveldamata müügi tühistamine ja arveldatud müügi tegelik.

Kõik need sündmused käivitavad tehingute päritolu ja tehingute seose olemite kirjete loomise, mis aitavad luua jälgi seostest nende kirjete vahel, mis on loodud üle ajakirje, töölehe rea, tegelike ning arve rea üksikasjadega.

Järgmises tabelis on kuvatud eelmise töövoo tehingute päritolu olemi kirjed.

| Sündmus                        | Päritolu                   | Päritolu tüüp                       | Tehing                       | Tehingu tüüp         |
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

Järgmises tabelis on kuvatud eelmise töövoo tehingute seose olemi kirjed.

| Sündmus                          | Tehing 1                 | Tehingu 1 roll | Tehingu 1 tüüp           | Kanne 2                | Tehingu 2 roll | Tehingu 2 tüüp |
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