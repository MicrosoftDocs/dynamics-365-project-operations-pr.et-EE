---
title: Hinnangud
description: Selles teemas antakse teavet hinnangute kohta rakenduses Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 8edb1689-2059-4776-8522-11cf0bb19b7a
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: a17ca814a71b05b0864d3da8f1cdbebe03e65f74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750895"
---
# <a name="estimates"></a>Hinnangud

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektil põhineva hinnapakkumise puhul saate projekti elluviimiseks nõutava töö hindamiseks kasutada hinnapakkumise rea üksikasjade olemit. Seejärel saate seda hinnangut kliendiga jagada.

Projektil põhinevad hinnapakkumise read ei pea sisaldama hinnapakkumise rea üksikasju. See eest võib neil olla palju hinnapakkumise rea üksikasju. Hinnapakkumise rea üksikasju kasutatakse aja, kulude või tasude hindamiseks. PSA ei luba hinnapakkumise rea üksikasjade jaoks olulisi hinnanguid. Neid nimetatakse tehingu klassideks. Hinnangulise maksusumma saab sisestada ka tehingu klassi.

Lisaks tehingu klassidele on hinnapakkumise rea üksikasjades tehingu tüüp. PSA toetab kahte tüüpi tehingu tüübi hinnapakkumise rea üksikasju: **Kulud** ja **Projekti leping**.

## <a name="estimate-by-using-a-contract"></a>Hindamine lepingu abil

Kui kasutasite projektil põhineva lepingu loomiseks PSA hinnapakkumist, kopeeritakse projekti lepingusse hinnapakkumise iga hinnapakkumise rea kohta esitatud hinnang. Projekti lepingu ülesehitus on nagu projekti hinnapakkumise ülesehitus, millel on read, rea üksikasjad ja arve ajakavad.

Hinnanguid saab teha otse projekti lepingus, nagu ka projekti hinnapakkumises. Projekti hinnapakkumise puhul tehakse hinnang lepingu ridade ja lepingurea üksikasjade abil. Lepingu rea üksikasju saab luua ka projekti plaanist, mis on loodud alt-üles lähenemise abil.

Lepingu rea üksikasju kasutatakse aja, kulude või tasude hindamiseks. Eeldatava maksusumma saab sisestada ka tehingu klassi.

PSA ei luba lepingu rea üksikasjade jaoks olulisi hinnanguid.

Projekti lepinguga toetatavad protsessid on arvete loomine ja kinnitamine. Arve loomine loob projektil põhineva arve projekti, mis sisaldab kõiki arveldamata müügi tegelikke näitajaid kuni tänase kuupäevani.

Kinnitamine teeb lepingu kirjutuskaitstuks ja muudab selle olekust **Mustand** olekuks **Kinnitatud**. Pärast selle toimingu tegemist ei saa te seda tagasi võtta. Kuna see tegevus on püsiv, on parim tava lepingu olekus **Mustand** hoidmine.

Lepingute mustandite ja kinnitatud lepingute eelnõude ainus erinevus on nende olek ja asjaolu, et lepingute mustandeid saab muuta, kuid kinnitatud lepingud ei saa. Arvete loomise ja tegelike jälgimise saab teha nii lepingutes kui ka kinnitatud lepingute eelnõudes.

PSA ei toeta lepingute või projektide tellimuste muutmist.

## <a name="estimating-projects"></a>Projektide hindamine

Saate hinnata projektidega seotud aega ja kulusid. PSA ei luba projektides kasutatavate materjalide või tasude hindamist.

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
| Kui kasutaja kirjeldab projekti tööülesande ressurssi                                                                                                                                                                                                                                                                                            | Hinnanguline reakirje ülesande müügiväärtuse näitamiseks luuakse, kui ülesanne on loodud kõigi nõutavate hinnakujunduse dimensioonidega. Rolli- ja organisatsiooniüksused on OOB Project Service’i hinnakujunduse dimensioonid | Projektileping | Time        |                                                                                   |
|     | Hinnanguline reakirje ülesande kuluväärtuse näitamiseks luuakse, kui ülesanne on loodud kõigi nõutavate hinnakujunduse dimensioonidega. Süsteem kopeerib kõik mitterahalised väljad müügihinnangute realt kuluhinnangute reale. Rolli- ja organisatsiooniüksused on OOB PSA hinnakujunduse dimensioonid nii kulumäära kui ka arve määra jaoks.                                                                                                                                                                                                                | Kulu             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Hinnapakkumise rea üksikasjade ja lepingu rea üksikasjade olemite kohandamine

Kui lisasite hinnapakkumise rea üksikasjadesse kohandatud välja ja soovite, et süsteem sisestaks välja väärtuse vaikeväärtuseks selle loodud seostuva kulurea vaikeväärtusena, kasutage lisandmooduli registreerimise vahendeid PreOperationContractLineDetailUpdate ja PreOperationQuoteLineDetailUpdate. Need lisandmoodulid tuleb pärast hinnapakkumise rea üksikasjade või lepingu rea üksikasjade muutmist uuesti registreerida. Protsessi läbimiseks toimige järgmiselt.

1. Avage PluginRegistrationTool ja looge ühendus võrgueksemplariga.
2. Valige **Otsi** ja otsige lisandmoodulit, mida soovite värskendada.

    ![Otsingupuu dialoogiboks](media/basic-guide-19.png)

3. Valige lisandmoodul ja seejärel valige avalehel suvand **Vali**.
4. Valige värskendamiseks lisandmooduli etapp, paremklõpsake nuppu ja seejärel valige **Värskenda**.

    ![Etapi valimine lisandmoodulis](media/basic-guide-20.png)

5. Valige dialoogiboksis **Värskenda olemasolevat etappi** väljal **Filtreerimise atribuudid** kolmikpunkt (**...**).
 
    ![Olemasoleva etapi värskendamise dialoogiboks](media/basic-guide-21.png)

6. Valige dialoogiboksis **Vali atribuudid** märkeruudud kohandatud atribuutide jaoks.

    ![Atribuutide valimise dialoogiboks](media/basic-guide-22.png)

7. Valige dialoogiboksi sulgemiseks nupp **OK**, seejärel valige **Värskenda etappi**.
 
    ![Etapi värskendamise nupp](media/basic-guide-23.png)

8. Korrake etappe 1–7 teise lisandmooduli jaoks.
9. Sulgege PluginRegistrationTool.
