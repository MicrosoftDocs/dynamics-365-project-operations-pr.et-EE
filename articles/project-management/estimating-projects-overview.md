---
title: Prognoosi projektide ülevaade
description: Selles teemas antakse teavet prognooside kohta rakenduses Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8e7ee4888a907b9d8c3ce06c1597f6b05be84477
ms.sourcegitcommit: 6eb26bab511ec09201ab70c3e2808dece3f74c4c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/07/2020
ms.locfileid: "3968038"
---
# <a name="estimate-projects-overview"></a>Prognoosi projektide ülevaade

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Projektil põhineva hinnapakkumise puhul saate projekti elluviimiseks nõutava töö prognoosimiseks kasutada olemit **Hinnapakkumise rea üksikasjad**. Seejärel saate seda hinnangut kliendiga jagada.

Projektipõhistel hinnapakkumise ridadel võib olla null kuni palju hinnapakkumise rea üksikasju. Hinnapakkumise rea üksikasju kasutatakse aja, kulude või tasude hindamiseks. Microsoft Dynamics 365 Project Operations ei luba hinnapakkumise rea üksikasjade jaoks olulisi hinnanguid. Neid nimetatakse tehingu klassideks. Hinnangulise maksusumma saab sisestada ka tehingu klassi.

Lisaks tehingu klassidele on hinnapakkumise rea üksikasjades tehingu tüüp. Hinnapakkumise rea üksikasjade joaks toetatakse kahte tüüpi tehinguid: **Kulud** ja **Projekti leping**.

## <a name="estimate-by-using-a-contract"></a>Hindamine lepingu abil

Kui kasutasite projektil põhineva lepingu loomiseks hinnapakkumist, kopeeritakse projekti lepingusse hinnapakkumise iga hinnapakkumise rea kohta esitatud hinnang. Projekti lepingu ülesehitus on nagu projekti hinnapakkumise ülesehitus, millel on read, rea üksikasjad ja arve ajakavad.

Hinnanguid saab teha otse projekti lepingus, nagu ka projekti hinnapakkumises. Projekti hinnapakkumise puhul tehakse hinnang lepingu ridade ja lepingurea üksikasjade abil. Lepingu rea üksikasju saab luua ka projekti plaanist, mis on loodud alt-üles lähenemise abil.

Lepingu rea üksikasju kasutatakse aja, kulude või tasude hindamiseks. Eeldatava maksusumma saab sisestada ka tehingu klassi.

Materjali prognoosid ei ole lepingurea üksikasjade seas lubatud.

Projekti lepinguga toetatavad protsessid on arvete loomine ja kinnitamine. Arve loomine loob projektil põhineva arve projekti, mis sisaldab kõiki arveldamata müügi tegelikke näitajaid kuni tänase kuupäevani.

Kinnitamine teeb lepingu kirjutuskaitstuks ja muudab selle olekust **Mustand** olekuks **Kinnitatud**. Pärast selle toimingu tegemist ei saa te seda tagasi võtta. Kuna see tegevus on püsiv, on parim tava lepingu olekus **Mustand** hoidmine.

Lepingute mustandite ja kinnitatud lepingute eelnõude ainus erinevus on nende olek ja asjaolu, et lepingute mustandeid saab muuta, kuid kinnitatud lepingud ei saa. Arvete loomise ja tegelike jälgimise saab teha nii lepingutes kui ka kinnitatud lepingute eelnõudes.

Projecti toimingud ei toeta lepingute või projektide tellimuste muutmist.

## <a name="estimating-projects"></a>Projektide hindamine

Saate hinnata projektidega seotud aega ja kulusid. Projecti toimingud ei luba projektides kasutatavate materjalide või tasude hindamist.

Aja hinnangud luuakse, kui loote tööülesande ja tuvastate toimingu sooritamiseks vajaliku üldise ressursi atribuudid. Aja hinnangud luuakse ajastamise toimingutest. Aja hinnanguid ei looda, kui loote üldised meeskonnaliikmed väljaspool ajakava konteksti.

Kulude hinnangud lehe **Hinnangud** ruudustikus.

## <a name="understanding-estimation"></a>Hinnangu ülevaade

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

Kui lisasite hinnapakkumise rea üksikasjadesse kohandatud välja ja soovite, et süsteem sisestaks välja väärtuse vaikeväärtuseks selle loodud seostuva kulurea vaikeväärtusena, kasutage lisandmooduli registreerimise vahendeid **PreOperationContractLineDetailUpdate** ja **PreOperationQuoteLineDetailUpdate**. Need lisandmoodulid tuleb pärast hinnapakkumise rea üksikasjade või lepingu rea üksikasjade muutmist uuesti registreerida. Protsessi läbimiseks toimige järgmiselt.

1. Avage PluginRegistrationTool ja looge ühendus võrgueksemplariga.
2. Valige **Otsi** ja otsige lisandmoodulit, mida soovite värskendada.
3. Valige lisandmoodul ja klõpsake seejärel avalehel suvandit **Vali**.
4. Valige värskendamiseks lisandmooduli etapp, paremklõpsake nuppu ja seejärel valige **Värskenda**.
5. Valige dialoogiboksis **Värskenda olemasolevat etappi** väljal **Filtreerimise atribuudid** kolmikpunkt (**...**).
6. Valige dialoogiboksis **Vali atribuudid** märkeruudud kohandatud atribuutide jaoks.
7. Valige dialoogiboksi sulgemiseks nupp **OK**, seejärel valige **Värskenda etappi**.
8. Korrake etappe 1–7 teise lisandmooduli jaoks.
9. Sulgege **PluginRegistrationTool**.
