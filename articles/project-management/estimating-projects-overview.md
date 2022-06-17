---
title: Finantsprognoosi mõisted
description: Selles artiklis antakse teavet projektitoimingute projektide finantsprognooside kohta.
author: rumant
ms.date: 03/22/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f8a4c3dd31cf5612c352331891178ac0ab852921
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931003"
---
# <a name="financial-estimation-concepts"></a>Finantsprognoosi mõisted

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Rakenduses Dynamics 365 Project Operations saate luua oma projektide finantsprognoosid kahes etapis. 
1. Müügieelses etapis enne tehingu võitmist. 
2. Täitmisetapis pärast projektilepingu loomist. 

Finantsprognoosi saate luua projektipõhise töö jaoks, kasutades mis tahes lehte järgmise kolme seas.
- Leht **Hinnapakkumine**, kasutades hinnapakkumise rea üksikasju.  
- Leht **Projekti lepingurida**, kasutades lepingurea üksikasju. 
- Leht **Projekt**, kasutades vahekaardi lehti **Ülesanded** või **Kuluprognoosid**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Prognoosi loomiseks projekti hinnapakkumise kasutamine
Projektil põhineva hinnapakkumise puhul saate projekti elluviimiseks nõutava töö prognoosimiseks kasutada olemit **Hinnapakkumise rea üksikasjad**. Seejärel saate seda hinnangut kliendiga jagada.

Projektipõhistel hinnapakkumise ridadel võib olla null kuni palju hinnapakkumise rea üksikasju. Hinnapakkumise rea üksikasju kasutatakse aja, kulude või tasude hindamiseks. Microsoft Dynamics 365 Project Operations ei luba hinnapakkumise rea üksikasjade jaoks olulisi hinnanguid. Neid nimetatakse tehingu klassideks. Hinnangulise maksusumma saab sisestada ka tehingu klassi.

Lisaks tehingu klassidele on hinnapakkumise rea üksikasjades tehingu tüüp. Hinnapakkumise rea üksikasjade joaks toetatakse kahte tüüpi tehinguid: **Kulud** ja **Projekti leping**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Prognoosi loomiseks projektilepingu kasutamine

Kui kasutasite projektil põhineva lepingu loomiseks hinnapakkumist, kopeeritakse projekti lepingusse hinnapakkumise iga hinnapakkumise rea kohta esitatud hinnang. Projekti lepingu ülesehitus on nagu projekti hinnapakkumise ülesehitus, millel on read, rea üksikasjad ja arve ajakavad.

Hinnanguid saab teha otse projekti lepingus, nagu ka projekti hinnapakkumises. Projekti hinnapakkumise puhul tehakse hinnang lepingu ridade ja lepingurea üksikasjade abil. Lepingu rea üksikasju saab luua ka projekti plaanist, mis on loodud alt-üles lähenemise abil.

Lepingu rea üksikasju kasutatakse aja, kulude või tasude hindamiseks. Eeldatava maksusumma saab sisestada ka tehingu klassi.

Materjali prognoosid ei ole lepingurea üksikasjade seas lubatud.

## <a name="use-a-project-to-create-an-estimate"></a>Prognoosi loomiseks projekti kasutamine 

Saate hinnata projektidega seotud aega ja kulusid. Project Operations ei toeta projektidele materjalide ega tasude prognoose.

Aja hinnangud luuakse, kui loote tööülesande ja tuvastate toimingu sooritamiseks vajaliku üldise ressursi atribuudid. Aja hinnangud luuakse ajastamise toimingutest. Aja hinnanguid ei looda, kui loote üldised meeskonnaliikmed väljaspool ajakava konteksti.

Kulude hinnangud lehe **Kuluprognoosid** ruudustikus.

Projekti prognoosi loomist peetakse parimaks tavaks, kuna saate koostada iga projektiplaani ülesande kohta tööjõu või aja ja kulude alt üles üksikasjalikud hinnangud. Seejärel saate kasutada seda üksikasjalikku hinnangut, et luua prognoose iga hinnapakkumise rea kohta ja koostada kliendi jaoks palju tõepärasema hinnapakkumise. Kui impordite või loote projektiplaani abil hinnapakkumise rea jaoks üksikasjaliku hinnangu, impordib Project Operations nende hinnangute müügiväärtused ja kuluväärtused. Pärast importimist saate vaadata projekti hinnapakkumise kasumlikkust, marginaale ja teostatavuse mõõdikuid.

## <a name="understanding-estimates"></a>Prognooside mõistine

Kasutage allolevat tabelit äriloogika mõistmiseks prognoosimise faasis.

| Stsenaarium                                                                                                                                                                                                                                                                                                                                          | Olemikirje                                                                                                                                                                                                       | Kandetüüp | Kande liik | Lisateave                                                            |
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
