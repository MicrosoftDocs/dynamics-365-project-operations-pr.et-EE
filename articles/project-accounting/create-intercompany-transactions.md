---
title: Kontsernisiseste kannete loomine
description: See artikkel annab teavet selle kohta, kuidas luua kontsernisiseseid tehinguid.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: da6fd8e0e6bfe2e2543f5c4a453ed769e412f1e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919365"
---
# <a name="create-intercompany-transactions"></a>Kontsernisiseste kannete loomine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Kontsernisisesed tehingud on projekti lepingust pärinevad aja- ja kulutehingud, mis kuuluvad ühele ettevõtte- või organisatsiooniüksusele, samas kui projektilepingu ressursid on erineva ettevõtte- või organisatsiooniüksuse osad.

Kontsernisisese tehingu kinnitamisel luuakse järgmised tegelikud tehingud

| **Kande tüüp** | **Rakendatud hinnakiri** | **Tehingu valuuta** |
| --- | --- | --- |
| Kulu | Lepingut sõlmiva üksuse omahinnakiri | Hinnarea valuuta |
| Arveldamata müük. Need on loodud ainult tegelike näitajate jaoks, mis on seostatud arve tüübi, kellaaja ja materjaliga lepingureaga. | Lepingu projekti müügi hinnakiri | Lepingu valuuta |
| Ressursiühiku maksumus | Ressursiüksuse omahinnakiri | Hinnarea valuuta |
| Organisatsioonidevaheline üksuse müük | Lepingut sõlmiva üksuse omahinnakiri | Hinnarea valuuta |

Kulu, ressursiüksuse kulu ning organisatsioonidevahelise üksuse müügitehingu hinnakujundus ja valuuta määratakse **organisatsiooni üksuse** poolt. Seda on oluline meeles pidada, kui otsustate, kuidas ettevõtteid ja organisatsiooniüksusi oma juurutuses struktureerida.

Müügivõimaluse, hinnapakkumise, projektilepingu ja projekti kirjete loomisel kontrollib süsteem, kas lepingut sõlmiva üksuse valuuta ühtib lepingu sõlmiva ettevõtte arvestusvaluutaga. Kui need pole samad, saab luua järgmised kirjed. Organisatsiooniüksuse valuuta määratletakse rakenduses Dynamics 365 Project Operations, avades suvandi **Dataverse** > **Sätted** > **Organisatsiooniüksused**. Ettevõtte arvestusvaluuta määratakse Dynamics 365 Finance’is, minnes **Pearaamat** > **Pearaamatu seadistamine** > **Pearaamat**. Valuuta sünkroonitakse pearaamatute topeltkirjendamise kaarti kasutades teie Dataverse’i keskkonnaga.

Süsteem loob ressursiühiku kulu ja organisatsioonidevahelise üksuse müükide tegelikud näitajad järgmistes olukordades.

  - Kui ressursiüksus erineb lepingut sõlmivast üksusest
  - Kui ressursiettevõte erineb lepingut sõlmivast ettevõttest

Samas viiakse rakenduse Dynamics 365 Finance keskkonda täiendava raamatupidamise jaoks üle ainult tehingud, millel on lepingut sõlmivast ettevõttest erinev ressursiettevõtte.

Projekti tegelike näitajate raamatupidamine salvestatakse rakenduse Finance teenuse Project Operations integreerimise töölehele. Süsteem loob järgmised töölehe kanded.

| **Kande tüüp** | **Juriidiline isik** | **Loob kande jaoks projektitehingu** | **Finantsdimensioonide vaikevorm** | **Vaikimisi arvelduse käibemaksugrupp ja arveldusüksuse käibemaksugrupp** |
| --- | --- | --- | --- | --- |
| Kulu | Ei lisata integreerimise töölehele | Puudub | Puudub | Puudub |
| Arveldamata müük | Laenava juriidilise olemi integreerimise tööleht | Ja | Project | **Arveldamise käibemaksugrupp**: põhineb **lepingu kliendil** <br/> **Arveldusüksuse käibemaksugrupp**: töölehe kande praegusest juriidilise üksuse projektikategooriast |
| Ressursiühiku maksumus | Laenu andva juriidilise olemi integreerimise tööleht | No | Kontsernisisene klient | **Arveldamise käibemaksugrupp**: põhineb **kontsernisisesel kliendil** <br/> **Arveldusüksuse käibemaksugrupp**: töölehe kande praegusest juriidilise üksuse projektikategooriast |
| Organisatsioonidevaheline müük | Laenu andva juriidilise olemi integreerimise tööleht | No | Kontsernisisene klient | **Arveldamise käibemaksugrupp**: põhineb **kontsernisisesel kliendil** <br/> **Arveldusüksuse käibemaksugrupp**: töölehe kande praegusest juriidilise üksuse projektikategooriast |

### <a name="example-intercompany-transactions"></a>Näide: kontsernisisesed kanded

Helle Ives, GBPM-i palgal olev arendaja paneb kirja 10 töötundi ettevõtte USPM Seiklusmängud projekti jaoks, mis on projektijuhi poolt heaks kiidetud. Arendaja kulu ettevõttes GBPM on 88 eurot tunnis. GBPM esitab ettevõttele USPM arve, kus arendaja tunnihinne on 120 USA dollarit. USPM esitab kliendile Seiklusmängud arve 200 USA dollarit töö eest, mille tegi ettevõtte GBPM ressurss. Lisateavet vaadake juhendist [Kontsernisisese arveldamise konfigureerimine](configure-intercompany-invoicing.md).

1. Avage rakenduses Project Operations suvand **Ressursid** ja valige loendist **Helle Ilves**. Tehke vahekaardil **Kavandamine** väljal **Ettevõte** valik **GBPM**.
2. Minge jaotisse **Müük** > **Kliendid** ja valige suvand **Uus**, et luua kliendi Seiklusmängud jaoks uus kliendikirje.
    1. Määrake ettevõtte valikuks **USPM**.
    2. Määrake suvandi **Seose tüüp** väärtuseks **Klient**.
    3. Valige **Kliendirühm 10 – kodumaine**.
    4. Määrake valuuta väärtuseks **USD**.
    5. Kirje salvestamine
3. Avage jaotis **Müük** > **Projektilepingud** ja looge kliendi Seiklusmängud jaoks uus projektileping.
    1. Määrake omanikettevõtteks **USPM** ja lepingu sõlmivaks üksuseks **Jõgi Robootika US**.
    2. Valige kliendiks Seiklusmängud.
    3. Valige toote hinnakiri ja salvestage kirje.
    4. Vahekaardil **Lepinguread** looge uus lepingurida. Määrake mis tahes nimi ja valige arveldusviisiks **Aeg ja materjalid**.
    5. Looge uus projekt ja seostage see selle lepingureaga.
4. Logige sisse ressursina **Helle Ilves**. Minge jaotisse **Projektid** > **Ajakirjed** ja looge Seiklusmängude projekti jaoks ajakirje.
5. Logige sisse projektijuhina. Minge jaotisse **Projektid** > **Kinnitused** ja kinnitage ajakirjetehing, mille logis Helle Ilves.
6. Liikuge Seiklusmängude projekti ja valige suvand **Seotud** > **Tegelikud**. Luuakse järgmised tegelikud kanded.

| **Kande tüüp** | **Hind** | **Tehingu valuuta** | **Summa** |
| --- | --- | --- | --- |
| Kulu | 120 | USD | 1200 |
| Arveldamata müük | 200 | USD | 2000 |
| Ressursiühiku maksumus | 88 | GBP | 880 |
| Organisatsioonidevaheline üksuse müük | 120 | USD | 1200 |

7. Logige sisse USPM-i raamatupidajana. Avage rakenduse Project Operations eksemplar ja valige ettevõte **USPM**. 
8. Minge jaotisse **Projektihaldus ja raamatupidamine** > **Perioodiline** > **Project Operations rakenduses Customer Engagement** > **Koondtabelist importimine** ja valige perioodilise protsessi käivitamine. See perioodiline protsess täidab Project Operationsi integreerimise töölehe.
9. Minge jaotisse **Projektihaldus ja raamatupidamine** > **Töölehed** > **Project Operationsi integreerimise tööleht** ja vaadake töölehe read läbi. Süsteem loob järgmise töölehe rea.

    | **Kande tüüp** | **Hind** | **Tehingu valuuta** | **Summa** |
    | --- | --- | --- | --- |
    | Arveldamata müük | 200 | USD | 2000 |

    Kui süsteem on häälestatud võtma vastu selle projekti viitlaekumisi, kirjendatakse järgnev.

    - Deebet: projekt – WIP müügiväärtus 200 USD
    - Krediit: projekt – viitlaekumine 200 USD

    See arveldamata müük on nüüd arveldamiseks valmis. Kliendi Seiklusmängud arve saab vajaduse korral finantsiliselt kirjendada.

10. Logige sisse kui **GBPM**-i raamatupidaja. Avage rakenduse Project Operations eksemplar ja avage ettevõte **GBPM**. 
11. Minge jaotisse **Projektihaldus ja raamatupidamine** > **Perioodiline** > **Project Operationsi integreerimine** > **Import etapitabelist** ja käivitage perioodiline protsess, et täita Project Operationsi integreerimise tööleht.
12. Minge jaotisse **Projektihaldus ja raamatupidamine** > **Töölehed** > **Project Operationsi integreerimise tööleht** ja vaadake read läbi. Süsteem loob järgmised töölehe read.

    | **Kande tüüp** | **Hind** | **Tehingu valuuta** | **Summa** |
    | --- | --- | --- | --- |
    | Ressursiühiku maksumus | 88 | GBP | 880 |
    | Organisatsioonidevaheline üksuse müük | 120 | USD | 1200 |

    Nende kirjete kirjendamise tulemuseks on järgmised vautšeri tehingud.

    - Deebet: projektimaksumus 88 GBP
    - Krediit: palgaarvestuse jaotus 88 GBP

    Kui süsteem on häälestatud võtma vastu kontsernisiseseid viitlaekumisi, kirjendatakse järgnev.

    - Deebet: projekt – WIP müügiväärtus 120 USD
    - Krediit: projekt – viitlaekumine 120 USD

    Süsteem on nüüd valmis looma kontsernisisese kliendiarve.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
