---
title: Projektipõhiste lepingute kopeerimine
description: See artikkel annab teavet projektilepingute kopeerimise kohta rakenduses Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410363"
---
# <a name="copy-project-based-contracts"></a>Projektipõhiste lepingute kopeerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Saate hõlpsasti luua uusi projektilepinguid, kopeerides olemasolevad lepingud kahel viisil.

- Valige loendilehel **Projektilepingud** projektileping ja seejärel valige **Kopeeri**.
- Valige üksikasjade lehel **Projekti lepingu** suvand **Kopeeri**.

Mõlemal juhul ilmub dialoogiboks, kus saab määrata kopeeritava lepingu parameetrid. Dialoogiboks sisaldab järgmisi välju. Sõltuvalt teie valitud väärtustest võib kopeerimisprotsess muutuda.

| Väli | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- |
| Teema | Sisestage eesmärklepingu teema. Dialoogiboksi avamisel määrab süsteem väljale lähtelepingu nimetuse, kuid sellele lisatakse sõna „koopia“. | Sellel väljal puudub allavoolu mõju. |
| klient | Viide kliendi ettevõttele või konto kirjele. Dialoogiboksi avamisel määrab süsteem välja lähtelepingus oleva konto. | See väli on lepingu peamine klient. |
| Omanikust ettevõte | Ettevõte, mis vastutab selle tehinguga seotud projektide tarnimise eest. Dialoogiboksi avamisel määrab süsteem välja lähtelepingu omava ettevõtte. | Omanikettevõte on juriidiline olem, mis hakkab pärast tehingu sõlmimist projekti ellu viima. Omanikettevõtte valuuta peab ühtima lepingut sõlmiva üksuse valuutaga. |
| Lepingut sõlmiv üksus | Organisatsiooniüksus, mis vastutab selle tehinguga seotud projektide elluviimise eest. Kui dialoogiboks avatakse, seab süsteem väljale lähtelepingu lepingulise ühiku. | Lepingut sõlmiv üksus on ettevõtte see allüksus, kes pärast tehingu sulgemist projektid teostab. Igal lepinguüksusel on valuuta. Seda valuutat kasutatakse projekti käigus tekkinud hinnanguliste ja tegelike kulude kajastamiseks. |
| Valuuta | Valuuta, milles tehing edastatakse. Dialoogiakna avamisel määrab süsteem väljale lähtelepingu valuuta. Valuutat saab muuta. Kui see on nii, määratakse väljale **Koopia hinnakujundus** alati **Ei**, kuna lähtelepingu hinnakirjad pole enam asjakohased. | Seda valuutat kasutatakse vaikehinnakirjade jaoks, lepingu finantsprognooside koostamiseks ja tehingu võitmise korral kliendile arve esitamiseks. |
| Soovitud tarnekuupäev | Tarnekuupäev, mida klient soovib. | Seda kuupäeva kasutatakse lõpukuupäevana, kui loote arvelduskuupäevi teatud sagedusega. |
| Hinnakujunduse kopeerimine | Väärtus, mis näitab, kas lepingu hinnakujundus peaks olema kopeeritud lähtelepingust. | Kui välja väärtuseks on seatud **Jah**, kopeeritakse projekti- ja toote hinnakirja viiteid lähtelepingust sihtlepingusse. Kui väärtuseks on seatud **Ei**, kasutatakse vaikimisi hinnakirju, mis põhinevad konto või projekti parameetrite viimasel hinnakirjal. |

Kui valite dialoogiboksis **OK**, loob süsteem lepingu koopia, mis põhineb teie poolt määratud parameetrite väärtustel. Seejärel avaneb uus leping.

Järgmist teavet **ei** kopeerita lähtelepingust sihtlepingusse, kuna see on iga lepingu puhul spetsiifiline.

- Arve ajakavad
- Lepingu ja lepingurea kliendid
- Projektiviide projektipõhistel lepinguridadel
- Kliendi eelarve teave

Kopeeritakse projektide ja toodete lepinguread, lepingurea üksikasjades olevad hinnangud ja mitteületatavad väärtused lepingu tasemel. Vaikimisi hindade ja kulumäärade sisestamine sõltub dialoogiboksi väljal **Hinnakujunduse kopeerimine** dialoogiboksis **Parameetrite kopeerimine** tehtud valikust.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
