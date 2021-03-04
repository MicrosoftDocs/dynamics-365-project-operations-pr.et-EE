---
title: Projektipõhiste lepinguridadega töötamine – liht
description: See teema sisaldab teavet projektipõhiste lepinguridadega töötamise kohta.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7ec8973df1def3f707603019cdd45147423c1ae3
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180637"
---
# <a name="work-with-projectbased-contract-lines---lite"></a>Projektipõhiste lepinguridadega töötamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakenduse Dynamics 365 Project Operations projektipõhised lepinguread on loodud sisaldama suhtluse projekti töö konkreetsete komponentide prognoose ja arvelduse kokkuleppeid. Projektipõhise lepingurea struktuur on laiendatud projekti prognooside ja arveldamise stsenaariumide jaoks järgmiste kontseptsioonidega.

- Arveldusmeetod
- Projekti ja ülesannete vastendamine
- Kaasatud tehingu klassid
- Mitteületatav limiit
- Arveldatavuse seadistus
- Lepingurea üksikasju kasutavad prognoosid
- Lepingurea kliendid

Järgmises tabelis on toodud projektopõhiste lepinguridade vahekaardi **Üldine** väljad, mis aitavad häälestada projektipõhise töö üksikasjaliku algusest lõpuni prognoosi ja arvelduse korraldusi.

| Väli | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- |
| **Nimi** | Lepingure nimi. See määratleb prognoositava lepingu diskreetse komponendi. Hinnapakkumise põhjal loodud projektilepingu puhul kopeeritakse see väärtus projektipõhise hinnapakkumise rea vastavast väärtusest. | Projekti arvereale kopeeritav nimi, mis luuakse arve loomise ajal lepingureast. |
| **Arveldusmeetod** | Hinnapakkumise põhjal loodud projektilepingu puhul kopeeritakse see väärtus projektipõhise hinnapakkumise rea vastavalt väljalt. See on suvandikomplekt, mis tähistab rakenduse Project Operations kahte peamist toetatavat lepingumudelit.</br>- **Fikseeritud hind**</br>- **Aeg ja materjal** | Vastavalt viidatud lepingurea arveldusmeetodile käsitletakse tegelikku kannet. Kui tegeliku näitaja poolt viidatud lepungureal on aja ja materjali arveldusmeetod, luuakse kulu ja arveldamata müügi tegelike näitajate kirjed. Kui tegeliku näitaja viidatud lepingureal on fikseeritud arveldusmeetod, luuakse ainult tegelik kulu. |
| **Project** | Selle välja abil saate tuvastada projekti, mida kasutatakse selle tegevusega seotud tööde pakkumiseks. | Seda väärtust kasutatakse koos suvanditega **Kaasatud ülesanded** ja **Kaasatud tehinguklassid**, et lahendada lepingurea viidet tegelikule või prognoositavale rea kirjele. |
| **Kaasatud ülesanded** | Näitab, kas see lepingurida sisaldab valitud projekti kõiki projekti ülesandeid või ainult ülesannete alamhulka. See on suvandikomplekt, millel on järgmised võimalikud väärtused.</br>- **Kõik projekti ülesanded**</br>- **Ainult valitud projekti ülesanded**. Selle välja tühi väärtus võrdub suvandi **Kõik projekti ülesanded** valimisega. | Kui valitud on suvand **Aiult valitud ülesanded**, saate valida konkreetsed ülesanded ja seostada need vahekaardil **Ülesande arvelduse seadistus** lehel **Projekt** selle lepingureaga. Väärtust kasutatakse koos klassidega **Projekt** ja **Kaasatud tehingud**, et lahendada lepingurea viidet tegelikule või prognoositavale rea kirjele. |
| **Kaasa aeg** | Lipp näitab, kas valitud projektiga seotud ajakanded või tööjõukulud kaasatakse sellele lepingureale. Väärtus **Ei** näitab, et ajakandeid ega tööjõukulusid ei kaasata sellele lepingureale. Väärtus **Jah** näitab, et kaasatakse. | Seda väärtust kasutatakse koos projektiga, et lahendada lepingurea viidet tegelikule või prognoositava rea kirjele. |
| **Kaasa kulu** | Lipp näitab, kas valitud projekti kulude maksumused kaasatakse sellele lepingureale. Väärtus **Ei** näitab, et kulude maksumust ei kaasata sellele lepingureale. Väärtus **Jah** näitab, et kaasatakse. | Seda väärtust kasutatakse koos projektiga, et lahendada lepingurea viidet tegelikule või prognoositava rea kirjele. |
| **Kaasa tasu** | Lipp näitab, kas valitud projekti tasud kaasatakse sellele lepingureale. Väärtus **Ei** näitab, et tasusid ei kaasata sellele lepingureale. Väärtus **Jah** näitab, et kaasatakse. | Seda väärtust kasutatakse koos projektiga, et lahendada lepingurea viidet tegelikule või prognoositava rea kirjele. |
| **Lepingu summa** | Fikseeritud hinnaga lepingurea puhul on see summa kokkulepitud väärtus, mille eest saadetakse kliendile arve kõikide selle lepingureaga seostatud töökomponentide eest. Aja ja materjali lepingurea puhul on see summa prognoositav väärtus, mille eest saadetakse kliendile arve kõikide selle lepingureaga seostatud töökomponentide eest. Hinnapakkumisest loodud loodud projektilepingu puhul kopeeritakse see väärtus projektipõhise hinnapakkumise rea vastavalt väljalt. Kui projektipõhisel lepingureal on rea üksikasjad, lukustatakse see väli redigeerimiseks ja see summeeritakse lepingurea üksikasjade summa põhjal. | Kui lepingureal on rea üksikasjad olemas, saab seda väärtust muuta, muutes rea üksikasjade summasid. Fikseeritud hinnaga lepingurea korral kasutatakse seda väärtust perioodilise arvelduse vahe-eesmärkide maksueelse summa loomiseks. |
| **Hinnanguline maks** | Kasutaja saab seda välja redigeerida, et sisestada lepingurea eeldatav maksusumma. Kui projektipõhisel lepingureal on rea üksikasjad, lukustatakse see väli redigeerimiseks ja see summeeritakse lepingurea üksikasjade maksusumma põhjal. | Kui lepingureal on rea üksikasjad olemas, saab seda väärtust muuta, muutes rea üksikasjade maksusummasid. Fikseeritud hinnaga lepingurea korral kasutatakse seda väärtust perioodilise arvelduse vahe-eesmärkide maksusumma loomiseks. |
| **Lepingu summa pärast maksu mahaarvamist** | Lepingu summa pärast maksu mahaarvamist. See väli on kirjutuskaitstud ja arvutatakse järgnevalt: **lepingu summa + maks**. | Fikseeritud hinnaga lepingurea korral kasutatakse seda väärtust perioodilise arvelduse vahe-eesmärkide loomiseks. |
| **Mitteületatav limiit** | Kasutaja saab seda välja redigeerida ja see on saadaval ainult projektipõhistel lepinguridadel, millel on määratud aja ja materjali põhjal arvete esitamise meetod. | Kasutaja saab seda välja redigeerida. Kui aja- ja materjalikulu tegelikud näitajad viitavad selle lepingurea ajale ja materjalile, hinnatakse tegeliku näitaja summa lepingurea mitte ületatava limiidiga võrreldes. See hindamine lõpetatakse pärast juba kulutatud ja kinnitatud summade arvestamist. |
| **Kliendi eelarve** | See väli on redigeeritav ja kopeeritakse hinnapakkumise rea vastavalt väljalt, kui lepingu loodi hinnapakkumisest. | Seda välja kasutatakse ainult teavitamiseks ja sellel pole allavoolu tähtsust. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Projektipõhiste lepinguridade vahekaardi Üldine valikute valideerimisreeglid

1. reegel: kui väli **Kaasatud ülesanded** on tühi või määratud väärtusele **Kõik projekti ülesanded**, kaasatakse lepingureale kõik projekti ülesanded.

2. reegel: kui väli **Kaasatud ülesanded** on tühi või otse määratud valikule **Kõik projekti ülesanded**, saab projekti ja teatud tehinguklassid kaasata ainult ühele lepingu projektipõhisele lepingureale.

3. reegel: kui väli **Kaasatud ülesanded** on määratud valikule **Ainult valitud projekti ülesanded**, saab projekti ja teatud tehinguklassid kaasata mitmele lepingu projektipõhisele lepingureale.

| Leping | Lepingurida | Project | Kaasatud ülesanded      | Kaasa aeg | Kaasa kulu | Kaasa tasu | Kehtiv/kehtetu | Põhjus                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------|---------------|---------|---------------------|--------------|-----------------|-------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Tühi               | Ja          | Ja             | Ja         | Kehtetu       | Reegli nr 2 rikkumine. Projekti P1 aeg, kulu ja tasud kaasatakse nii lepinguridadele CL1 kui ka CL2.                                                                                                                                                                                                                                                                                                              |
| C1       | CL2           | P1      | Tühi               | Ja          | Ja             | Ja         | Kehtetu       | Reegli nr 2 rikkumine. Projekti P1 aeg, kulu ja tasud kaasatakse nii lepinguridadele CL1 kui ka CL2.                                                                                                                                                                                                                                                                                                              |
| C1       | CL1           | P1      | Tühi               | Ja          | No              | Ja         | Kehtetu       | Reegli nr 2 rikkumine. Projekti P1 aeg ja tasud kaasatakse nii lepinguridadele CL1 kui ka CL2.                                                                                                                                                                                                                                                                                                                          |
| C1       | CL2           | P1      | Tühi               | Ja          | Ja             | Ja         | Kehtetu       | Reegli nr 2 rikkumine. Projekti P1 aeg ja tasud kaasatakse nii lepinguridadele CL1 kui ka CL2.                                                                                                                                                                                                                                                                                                                          |
| C1       | CL1           | P1      | Tühi               | Ja          | No              | Ja         | Kehtib           | Projekti P1 aeg ja tasud kaasatakse CL1-s. Projekti P1 kulu on kaasatud reale CL2. </br>   Igale lepingureale kaasatava puhul ei esine ülekatteid ja seega need kehtivad.                                                                                                                                                                                                                         |
| C1       | CL2           | P1      | Tühi               | No           | Ja             | No          | Kehtib           | Projekti P1 aeg ja tasud kaasatakse CL1-s. Projekti P1 kulu on kaasatud reale CL2. </br>   Igale lepingureale kaasatava puhul ei esine ülekatteid ja seega need kehtivad.                                                                                                                                                                                                                         |
| C1       | CL1           | P1      | Ainult valitud ülesanded | Ja          | Ja             | Ja         | Kehtetu       | Reegli nr 2 rikkumine.   </br>- C1 sisaldab projekti P1 ülesannete andmehulga aega, kulusid ja tasusid. </br>- CL2 hõlmab kogu projektiga P1 seotud aega, kulu ja tasusid ning seega kattub see sellega, mis on kaasatud C1-te.                                                                                                                                                                                          |
| C1       | CL2           | P1      | Tühi               | Ja          | Ja             | Ja         | Kehtetu       | Reegli nr 2 rikkumine.   </br>- C1 sisaldab projekti P1 ülesannete andmehulga aega, kulusid ja tasusid. </br>- CL2 hõlmab kogu projektiga P1 seotud aega, kulu ja tasusid ning seega kattub see sellega, mis on kaasatud C1-te.                                                                                                                                                                                          |
| C1       | CL1           | P1      | Ainult valitud ülesanded | Ja          | Ja             | Ja         | Kehtib           | Reegli nr 3 kohta</br>- C1 sisaldab projekti P1 ülesannete andmehulka aeg, kulud ja tasud. </br> - CL2 sisaldab projekti P1 ülesannete andmehulka aeg, kulud ja tasud. </br> Ainus täiendav valideerimine on CL1 tööülesannete andmekomplekt, mis erineb CL2 tööülesannete andmekomplektist, et vältida kattumist. Selle valideerimise teeb süsteem, kui ülesanded on seostatud. |
| C1       | CL2           | P1      | Ainult valitud ülesanded | Ja          | Ja             | Ja         | Kehtib           | Reegli nr 3 kohta</br>- C1 sisaldab projekti P1 ülesannete andmehulka aeg, kulud ja tasud. </br> - CL2 sisaldab projekti P1 ülesannete andmehulka aeg, kulud ja tasud. </br> Ainus täiendav valideerimine on CL1 tööülesannete andmekomplekt, mis erineb CL2 tööülesannete andmekomplektist, et vältida kattumist. Selle valideerimise teeb süsteem, kui ülesanded on seostatud. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]