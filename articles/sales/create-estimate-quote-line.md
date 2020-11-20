---
title: Prognooside loomine hinnapakkumise real
description: See teema sisaldab teavet, kuidas luua projekti hinnapakkumise real prognoosi.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 97030689eddb88576ffcf9dd848f8a0776512192
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122923"
---
# <a name="create-estimates-on-a-quote-line"></a>Prognooside loomine hinnapakkumise real

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Projektil põhineva hinnapakkumise puhul saate projekti elluviimiseks nõutava töö hindamiseks kasutada hinnapakkumise rea üksikasjade olemit. Seejärel saate seda hinnangut kliendiga jagada.

Projektil põhinevad hinnapakkumise read ei pea sisaldama hinnapakkumise rea üksikasju. See eest võib neil olla palju hinnapakkumise rea üksikasju. Hinnapakkumise rea üksikasju kasutatakse aja, kulude või tasude hindamiseks. Dynamics 365 Project Operations ei luba hinnapakkumise rea üksikasjade jaoks olulisi hinnanguid. Neid nimetatakse tehingu klassideks. Hinnangulise maksusumma saab sisestada ka tehingu klassi.

Lisaks tehingu klassidele on hinnapakkumise rea üksikasjades tehingu tüüp. Hinnapakkumise rea üksikasjade jaoks on kahte tüüpi tehinguid: **Kulud** ja **Projekti leping**.

## <a name="estimate-by-using-a-contract"></a>Hindamine lepingu abil

Kui kasutasite projektiööl põhineva lepingu loomiseks Project Operationsi hinnapakkumist, kopeeritakse projekti lepingusse hinnapakkumise iga hinnapakkumise rea kohta esitatud hinnang. Projekti lepingu ülesehitus on nagu projekti hinnapakkumise ülesehitus, millel on read, rea üksikasjad ja arve ajakavad.

Hinnanguid saab teha otse projekti lepingus, nagu ka projekti hinnapakkumises. Projekti hinnapakkumise puhul tehakse hinnang lepingu ridade ja lepingurea üksikasjade abil. Lepingu rea üksikasju saab luua ka projekti plaanist, mis on loodud alt-üles lähenemise abil.

Lepingu rea üksikasju kasutatakse aja, kulude või tasude hindamiseks. Eeldatava maksusumma saab sisestada ka tehingu klassi.

Materjali prognoosid ei ole lepingurea üksikasjade seas lubatud.

Projekti lepinguga toetatavad protsessid on arvete loomine ja kinnitamine. Arve loomine loob projektil põhineva arve projekti, mis sisaldab kõiki arveldamata müügi tegelikke näitajaid kuni tänase kuupäevani.

Kinnitamine teeb lepingu kirjutuskaitstuks ja muudab selle olekust **Mustand** olekuks **Kinnitatud**. Pärast selle toimingu tegemist ei saa te seda tagasi võtta. Kuna see tegevus on püsiv, on parim tava lepingu olekus **Mustand** hoidmine.

Lepingute mustandite ja kinnitatud lepingute eelnõude ainus erinevus on nende olek ja asjaolu, et lepingute mustandeid saab muuta, kuid kinnitatud lepingud ei saa. Arvete loomise ja tegelike jälgimise saab teha nii lepingutes kui ka kinnitatud lepingute eelnõudes.

Tellimuste muutmine ei ole lepingute ega projektide puhul toetatud.

## <a name="estimating-projects"></a>Projektide hindamine

Saate prognoosida projektile kuluvat aega ja kulutusi, kuid mitte materjale ega tasusid.

Aja hinnangud luuakse, kui loote tööülesande ja tuvastate toimingu sooritamiseks vajaliku üldise ressursi atribuudid. Aja hinnangud luuakse ajastamise toimingutest. Aja hinnanguid ei looda, kui loote üldised meeskonnaliikmed väljaspool ajakava konteksti.

Kulude hinnangud lehe **Hinnangud** ruudustikus.

## <a name="understand-estimation"></a>Prognoosi mõistmine

Kasutage allolevat tabelit äriloogika mõistmiseks hindamise faasis.

| Stsenaarium                                                                                                                                                                                                                                                                                                                                          | Olemikirje                                                                                                                                                                                                       | Kandetüüp | Tehingu klass | Lisateave                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Kui teil on vaja hinnata hinnapakkumise aja müügiväärtust                                                                                                                                                                                                                                                                                    | Hinnapakkumise rea üksikasjade (QLD) kirje on loodud                                                                                                                                                                               | Projektileping | Time        | Tehingu päritolu väli müügi poolel QLD real viitab kulu poole QLD-le |
|                                                                                                                                                                                                                                                                                     | Süsteem loob teise QLD kirje, kus talletatakse vastavad omahinna väärtused. Süsteem kopeerib kõik mitte-raha väljad müügi QLD-st kulu QLD-sse.                                                                                                                                                                               | Kulu | Time        | Tehingu päritolu väli müügi poolel hinnapakkumise rea üksikasjade (QLD) real viitab kulu poole QLD-le |
| Kui teil on vaja hinnata lepingu aja müügiväärtust                                                                                                                                                                                                                                                                                 | Projekti lepingu rea üksikasjade (CLD) kirje on loodud                                                                                                                                                                    | Projektileping | Time        | Tehingu päritolu väli müügi poolel CLD real viitab kulude CLD-le      |
|                                                                                                                                                                                                                                                                                  | Süsteem loob teise CLD kirje, kus talletatakse vastavad omahinna väärtused. Süsteem kopeerib kõik mitte-raha väljad müügi CLD-st kulu CLD-sse.                                                                                                                                                                    | Kulu | Time        | Tehingu päritolu väli müügi poolel CLD real viitab kulude CLD-le      |
| Kui kasutaja kirjeldab projekti tööülesande ressurssi                                                                                                                                                                                                                                                                                            | Hinnanguline reakirje ülesande müügiväärtuse näitamiseks luuakse, kui ülesanne on loodud kõigi nõutavate hinnakujunduse dimensioonidega. Rolli- ja organisatsiooniüksused on hinnakujunduse dimensioonid | Projekti leping | Aeg        |                                                                                   |
|     | Hinnanguline reakirje ülesande kuluväärtuse näitamiseks luuakse, kui ülesanne on loodud kõigi nõutavate hinnakujunduse dimensioonidega. Süsteem kopeerib kõik mitterahalised väljad müügihinnangute realt kuluhinnangute reale. Rolli- ja organisatsiooniüksused on hinnakujunduse dimensioonid nii kulumäära kui ka arve määra jaoks.                                                                                                                                                                                                                | Kulu             | Aeg           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Hinnapakkumise rea üksikasjade ja lepingu rea üksikasjade olemite kohandamine

Kui lisasite hinnapakkumise rea üksikasjadesse kohandatud välja ja soovite, et süsteem sisestaks välja väärtuse vaikeväärtuseks selle loodud seostuva kulurea vaikeväärtusena, kasutage lisandmooduli registreerimise vahendeid PreOperationContractLineDetailUpdate ja PreOperationQuoteLineDetailUpdate. Need lisandmoodulid tuleb pärast hinnapakkumise rea üksikasjade või lepingu rea üksikasjade muutmist uuesti registreerida. Protsessi läbimiseks toimige järgmiselt.

1. Avage PluginRegistrationTool ja looge ühendus võrgueksemplariga.
2. Valige **Otsi** ja otsige lisandmoodulit, mida soovite värskendada.
3. Valige lisandmoodul ja seejärel valige avalehel suvand **Vali**.
4. Valige värskendamiseks lisandmooduli etapp, paremklõpsake nuppu ja seejärel valige **Värskenda**.
5. Valige dialoogiboksis **Värskenda olemasolevat etappi** väljal **Filtreerimise atribuudid** kolmikpunkt (**...**).
6. Valige dialoogiboksis **Vali atribuudid** märkeruudud kohandatud atribuutide jaoks.
7. Valige dialoogiboksi sulgemiseks nupp **OK**, seejärel valige **Värskenda etappi**.
8. Korrake etappe 1–7 teise lisandmooduli jaoks.
9. Sulgege PluginRegistrationTool.
