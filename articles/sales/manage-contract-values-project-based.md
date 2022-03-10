---
title: Projektipõhiste lepinguridadega töötamine
description: See teema sisaldab teavet projektipõhiste lepinguridade kohta.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c1c935a998cba8bd42ba2f11c8310d41e72de94adac7c2cb83f4c7224127b10b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990041"
---
# <a name="work-with-projectbased-contract-lines"></a>Projektipõhiste lepinguridadega töötamine

Rakenduse Dynamics 365 Project Operations projektipõhised lepinguread on loodud sisaldama suhtluse projekti töö konkreetsete komponentide prognoose ja arvelduse kokkuleppeid. Projektipõhise lepingurea struktuur on laiendatud projekti prognooside ja arveldamise stsenaariumide jaoks järgmiste kontseptsioonidega.

- Arveldusmeetod
- Projekti ja ülesannete vastendamine
- Kaasatud tehingu klassid
- Mitteületatav limiit
- Arveldatavuse seadistus
- Lepingurea üksikasju kasutavad prognoosid
- Lepingurea kliendid

Projektipõhiste lepinguridade vahekaardil **Üldine** on kaasatud järgmised väljad. Need väljad aitavad luua projektipõhise töö jaoks aluseid üksikasjalikuks, alt üles prognoosideks ja arvelduse korraldamiseks.

| Väli | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- |
| **Nimi** | Lepingurea nimi, mis määratleb prognoositava lepingu diskreetse komponendi. Hinnapakkumise põhjal loodud projektilepingu puhul kopeeritakse see väärtus projektipõhise hinnapakkumise rea vastavast väärtusest. | Sele välja väärtus kopeeritakse projekti arvereale, mis luuakse arve loomise ajal lepingureast. |
| **Arveldusmeetod** | Hinnapakkumise põhjal loodud projektilepingu puhul kopeeritakse see väärtus projektipõhise hinnapakkumise rea vastavalt väljalt. See on suvandikomplekt, mis tähistab rakenduse Project Operations kahte peamist toetatavat lepingumudelit.</br>- **Fikseeritud hind**</br>- **Aeg ja materjal** | Vastavalt viidatud lepingurea arveldusmeetodile käsitletakse tegelikku kannet. Kui tegeliku näitaja poolt viidatud lepungureal on aja ja materjali arveldusmeetod, luuakse kulu ja arveldamata müügi tegeliku näitaja kirje. Kui tegeliku näitaja viidatud lepingureal on fikseeritud arveldusmeetod, luuakse ainult tegelik kulu. |
| **Project** | Selle välja abil saate tuvastada projekti, mida kasutatakse selle tegevusega seotud tööde pakkumiseks. | Selle välja väärtust kasutatakse koos väljadega **Kaasatud ülesanded** ja **Kaasatud tehinguklassid**, et lahendada lepingurea viidet tegelikule või prognoositava rea kirjele. |
| **Kaasa aeg** | Lipp näitab, kas valitud projektiga seotud ajakanded või tööjõukulud on kaasatud sellele lepingureale. Väärtus **Ei** näitab, et ajakandeid ega tööjõukulusid ei kaasata sellele lepingureale. Väärtus **Jah** näitab, et kaasatakse. | Selle välja väärtust kasutatakse koos projektiga, et lahendada lepingurea viidet tegelikule või prognoosi rea kirjele. |
| **Kaasa kulu** | Lipp näitab, kas valitud projekti kulude maksumused kaasatakse sellele lepingureale. Väärtus **Ei** näitab, et kulude maksumust ei kaasata sellele lepingureale. Väärtus **Jah** näitab, et kaasatakse. | Selle välja väärtust kasutatakse koos projektiga, et lahendada lepingurea viidet tegelikule või prognoosi rea kirjele. |
| **Kaasa tasu** | Lipp näitab, kas valitud projekti tasud kaasatakse sellele lepingureale. Väärtus **Ei** näitab, et tasusid ei kaasata sellele lepingureale. Väärtus **Jah** näitab, et kaasatakse. | Selle välja väärtust kasutatakse koos projektiga, et lahendada lepingurea viidet tegelikule või prognoosi rea kirjele. |
| **Lepingu summa** | Fikseeritud hinnaga lepingurea puhul on see kokkulepitud väärtus, mille eest saadetakse kliendile arve kõikide selle lepingureaga seostatud töökomponentide eest. Aja ja materjali lepingurea puhul on see summa prognoositav väärtus, mille eest saadetakse kliendile arve kõikide selle lepingureaga seostatud töökomponentide eest. Hinnapakkumisest loodud loodud projektilepingu puhul kopeeritakse see väärtus projektipõhise hinnapakkumise rea vastavalt väljalt. Kui projektipõhisel lepingureal on rea üksikasjad, lukustatakse see väli redigeerimiseks ja see summeeritakse lepingurea üksikasjade summa põhjal. | Kui lepingureal on rea üksikasjad olemas, saab seda väärtust muuta, muutes rea üksikasjade summasid. Fikseeritud hinnaga lepingurea korral kasutatakse seda väärtust perioodilise arvelduse vahe-eesmärkide maksueelse summa loomiseks. |
| **Hinnanguline maks** | Kasutaja saab seda välja redigeerida, et sisestada lepingurea eeldatav maksusumma. Kui projektipõhisel lepingureal on rea üksikasjad, lukustatakse see väli redigeerimiseks ja see summeeritakse lepingurea üksikasjade maksusumma põhjal. | Kui lepingureal on rea üksikasjad olemas, saab seda väärtust muuta, muutes rea üksikasjade maksusummasid. Fikseeritud hinnaga lepingurea korral kasutatakse seda väärtust perioodilise arvelduse vahe-eesmärkide maksusumma loomiseks. |
| **Lepingu summa pärast maksu mahaarvamist** | Lepingu summa pärast maksu mahaarvamist. See väli on kirjutuskaitstud ja arvutatakse järgnevalt: **lepingu summa + maks**. | Fikseeritud hinnaga lepingurea korral kasutatakse seda väärtust perioodilise arvelduse vahe-eesmärkide loomiseks. |
| **Mitteületatav limiit** | Kasutaja saab seda välja redigeerida ja see on saadaval ainult projektipõhistel lepinguridadel, millel on aja ja materjali põhjal arvete esitamise meetod. | Kasutaja saab seda välja redigeerida. Kui aja- ja kulu tegelikud näitajad viitavad selle lepingurea ajale ja materjalile, hinnatakse tegeliku näitaja summa selle lepingurea mitte ületatava limiidiga võrreldes, pärast juba kulutatud ja kinnitatud summade arvestamist. |
| **Kliendi eelarve** | See väli on redigeeritav ja kopeeritakse hinnapakkumise rea vastavalt väljalt, kui leping loodi hinnapakkumisest. | Seda välja kasutatakse ainult teavitamiseks ja sellel pole allavoolu tähtsust. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Projektipõhiste lepinguridade vahekaardi Üldine valikute valideerimisreegel

Reegel: projekti ja teatud tehinguklassi saab kaasata ainult ühele lepingu projektipõhisele lepingureale.

| Leping | Lepingurida | Project | Kaasa aeg | Kaasa kulu | Kaasa tasu | Kehtiv/kehtetu | Põhjus                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Ja          | Ja             | Ja         | Kehtetu       | Rikub reeglit. Projekti P1 aeg, kulu ja tasud kaasatakse nii lepinguridadele CL1 kui ka CL2.                                                                                       |
| C1       | CL2           | P1      | Ja          | Ja             | Ja         | Kehtetu       | Rikub reeglit. Projekti P1 aeg, kulu ja tasud kaasatakse nii lepinguridadele CL1 kui ka CL2.                                                                                       |
| C1       | CL1           | P1      | Ja          | No              | Ja         | Kehtetu       | Rikub reeglit. Projekti P1 aeg ja tasud kaasatakse nii lepinguridadele CL1 kui ka CL2.                                                                                                   |
| C1       | CL2           | P1      | Ja          | Ja             | Ja         | Kehtetu       | Rikub reeglit. Projekti P1 aeg ja tasud kaasatakse nii lepinguridadele CL1 kui ka CL2.                                                                                                   |
| C1       | CL1           | P1      | Ja          | No              | Ja         | Kehtib           | Projekti P1 aeg ja tasud kaasatakse CL1-s. Projekti P1 kulu on kaasatud reale CL2. </br>   Igale lepingureale kaasatava puhul ei esine ülekatteid ja seega need kehtivad.  |
| C1       | CL2           | P1      | No           | Ja             | No          | Kehtib           | Projekti P1 aeg ja tasud kaasatakse CL1-s. Projekti P1 kulu on kaasatud reale CL2. </br>   Igale lepingureale kaasatava puhul ei esine ülekatteid ja seega need kehtivad.  |
| C1       | CL1           | P1      | Ja          | Ja             | Ja         | Kehtetu       | Rikub reeglit. Projekti P1 aeg, kulu ja tasud kaasatakse kahe lepingu ridadel.                                                                                               |
| CL2      | CL2           | P1      | Ja          | Ja             | Ja         | Kehtetu       | Rikub reeglit. Projekti P1 aeg, kulu ja tasud kaasatakse kahe lepingu ridadel.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]