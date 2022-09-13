---
title: Projektipõhiste lepingute kopeerimine
description: Sellest artiklist leiate teavet projektilepingute kopeerimise kohta Microsoftis Dynamics 365 Project Operations.
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

Saate hõlpsalt luua uusi projektilepinguid, kopeerides olemasolevaid lepinguid ühel kahest viisist.

- Valige loendilehel **Projektilepingud** projektileping ja seejärel valige **Kopeeri**.
- Valige üksikasjade lehel **Projekti lepingu** suvand **Kopeeri**.

Mõlemal juhul ilmub dialoogiboks, kus saate määrata kopeeritud lepingu parameetrid. Dialoogiboks sisaldab järgmisi välju. Sõltuvalt valitud väärtustest võib kopeerimisprotsess muutuda.

| Väli | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- |
| Teema | Sisestage eesmärklepingu teema. Dialoogiboksi avamisel määrab süsteem välja lähtelepingu nimele, kuid sellele lisatakse sõna "koopia". | Sellel väljal puudub allavoolu mõju. |
| klient | Viide kliendi ettevõttele või konto kirjele. Dialoogiboksi avamisel määrab süsteem välja lähtelepingu kontole. | See väli on lepingu peamine klient. |
| Omanikust ettevõte | Ettevõte, kes vastutab selle tehinguga seotud projektide elluviimise eest. Dialoogiboksi avamisel määrab süsteem välja lähtelepingu omanikule. | Omav ettevõte on juriidiline isik, kes teostab projekti pärast tehingu sulgemist. Omava ettevõtte valuuta peab vastama lepinguüksuse valuutale. |
| Lepingut sõlmiv üksus | Organisatsiooniüksus, mis vastutab selle tehinguga seotud projektide elluviimise eest. Dialoogiboksi avamisel määrab süsteem välja lähtelepingu lepinguüksusele. | Lepingut sõlmiv üksus on ettevõtte see allüksus, kes pärast tehingu sulgemist projektid teostab. Igal lepinguüksusel on valuuta. Seda valuutat kasutatakse projekti käigus tekkinud hinnanguliste ja tegelike kulude kajastamiseks. |
| Valuuta | Valuuta, milles tehing edastatakse. Dialoogiboksi avamisel määrab süsteem välja lähtelepingu valuutaks. Valuutat saab muuta. Kui see on nii, **on välja Kopeeri hinnakujundus** väärtuseks **alati seatud Ei**, kuna lähtelepingu hinnakirjad ei ole enam asjakohased. | Seda valuutat kasutatakse vaikehinnaloendite jaoks, lepingu finantsprognooside loomiseks ja kliendile arve esitamiseks tehingu võitmisel. |
| Soovitud tarnekuupäev | Tarnekuupäev, mida klient soovib. | Seda kuupäeva kasutatakse lõppkuupäevana, kui loote arvelduskuupäevi kindla sagedusega. |
| Hinnakujunduse kopeerimine | Väärtus, mis näitab, kas lepingu hind tuleks lähtelepingust kopeerida. | Kui välja väärtuseks **on määratud Jah**, kopeeritakse projekti ja toote hinnakirja viited lähtelepingust sihtlepingusse. Kui selle väärtuseks **on seatud Ei**, kasutatakse vaikehinnakirju, mis põhinevad konto või projekti parameetrite uusimatel hinnakirjadel. |

Kui valite **dialoogiboksis OK**, loob süsteem teie määratud parameetriväärtuste põhjal lepingu koopia. Seejärel avatakse uus leping.

Järgmist teavet **ei** kopeerita lähtelepingust sihtlepingusse, kuna see on iga lepingu puhul asjakohane.

- Arve ajakavad
- Lepingu ja lepingurea kliendid
- Projektiviide projektipõhistel lepinguridadel
- Kliendi eelarve teave

Kopeeritakse projektide ja toodete lepinguread, hinnangud lepingurea üksikasjades ja mitteületavad väärtused lepingu tasandil. Vaikehindade ja kulumäärade sisestamine sõltub valikust väljal **Kopeeri** hinnakujundus **dialoogiboksis Kopeeri parameetrid**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
