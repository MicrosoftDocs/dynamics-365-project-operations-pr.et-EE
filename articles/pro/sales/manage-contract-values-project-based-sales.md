---
title: Projektipõhiste lepinguridade ülevaade
description: See teema sisaldab teavet projektipõhiste lepinguridadega töötamise kohta.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8af32b0475650db9c5862ea23d185588a631ade6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003131"
---
# <a name="project-based-contract-lines-overview"></a>Projektipõhiste lepinguridade ülevaade

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

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
| **Project** | Selle välja abil saate tuvastada projekti, mida kasutatakse selle tegevusega seotud tööde pakkumiseks. | Seda väärtust kasutatakse koos suvanditega **Kaasatud tööülesanded** ja **Kaasatud tehinguklassid**, et lahendada tegelikul või prognoositud reakirjel lepingurea viide. |
| **Kaasatud ülesanded** | Näitab, kas see lepingurida sisaldab valitud projekti kõiki projekti ülesandeid või ainult ülesannete alamhulka. See on suvandikomplekt, millel on järgmised võimalikud väärtused.</br>- **Kõik projekti ülesanded**</br>- **Ainult valitud projekti ülesanded**. Selle välja tühi väärtus võrdub suvandi **Kõik projekti ülesanded** valimisega. | Kui valitud on suvand **Aiult valitud ülesanded**, saate valida konkreetsed ülesanded ja seostada need vahekaardil **Ülesande arvelduse seadistus** lehel **Projekt** selle lepingureaga. Väärtust kasutatakse koos klassidega **Projekt** ja **Kaasatud tehingud**, et lahendada lepingurea viidet tegelikule või prognoositavale rea kirjele. |
| **Kaasa aeg** | Väärtus **Jah**/**Ei** näitab, kas valitud projekti tehingu või tööjõu maksumused lisatakse sellele lepingureale. Väärtus **Ei** näitab, et ajakandeid ega tööjõukulusid ei kaasata sellele lepingureale. Väärtus **Jah** näitab, et kaasatakse. | Seda väärtust kasutatakse seoses projektiga, et lahendada lepingurea kirje tegelikul või prognoositud rea kirjel. |
| **Kaasa kulu** | Väärtus **Jah**/**Ei** näitab, kas valitud projekti kulu maksumused lisatakse sellele lepingureale. Väärtus **Ei** näitab, et kulude maksumust ei kaasata sellele lepingureale. Väärtus **Jah** näitab, et kaasatakse. | Seda väärtust kasutatakse seoses projektiga, et lahendada lepingurea kirje tegelikul või prognoositud rea kirjel. |
| **Kaasa materjalid** | Väärtus **Jah**/**Ei** näitab, kas valitud projekti materjali maksumused lisatakse sellele lepingureale. Väärtus **Ei** näitab, et materjali maksumust ei lisata sellele lepingureale. Väärtus **Jah** näitab, et kaasatakse. | Seda väärtust kasutatakse seoses projektiga, et lahendada lepingurea kirje tegelikul või prognoositud rea kirjel. |
| **Kaasa tasu** | Väärtus **Jah**/**Ei** näitab, kas valitud projekti tasud lisatakse sellele lepingureale. Väärtus **Ei** näitab, et tasusid ei kaasata sellele lepingureale. Väärtus **Jah** näitab, et kaasatakse. | Seda väärtust kasutatakse seoses projektiga, et lahendada lepingurea kirje tegelikul või prognoositud rea kirjel. |
| **Lepingu summa** | Fikseeritud hinnaga lepingurea puhul on see summa kokkulepitud väärtus, mille eest saadetakse kliendile arve kõikide selle lepingureaga seostatud töökomponentide eest. Aja ja materjali lepingurea puhul on see summa prognoositav väärtus, mille eest saadetakse kliendile arve kõikide selle lepingureaga seostatud töökomponentide eest. Hinnapakkumisest loodud loodud projektilepingu puhul kopeeritakse see väärtus projektipõhise hinnapakkumise rea vastavalt väljalt. Kui projektipõhisel lepingureal on rea üksikasjad, lukustatakse see väli redigeerimiseks ja see summeeritakse lepingurea üksikasjade summa põhjal. | Kui lepingureal on rea üksikasjad olemas, saab seda väärtust muuta, muutes rea üksikasjade summasid. Fikseeritud hinnaga lepingurea korral kasutatakse seda väärtust perioodilise arvelduse vahe-eesmärkide maksueelse summa loomiseks. |
| **Hinnanguline maks** | Kasutaja saab seda välja redigeerida, et sisestada lepingurea eeldatav maksusumma. Kui projektipõhisel lepingureal on rea üksikasjad, lukustatakse see väli redigeerimiseks ja see summeeritakse lepingurea üksikasjade maksusumma põhjal. | Kui lepingureal on rea üksikasjad olemas, saab seda väärtust muuta, muutes rea üksikasjade maksusummasid. Fikseeritud hinnaga lepingurea korral kasutatakse seda väärtust perioodilise arvelduse vahe-eesmärkide maksusumma loomiseks. |
| **Lepingu summa pärast maksu mahaarvamist** | Lepingu summa pärast maksu mahaarvamist. See väli on kirjutuskaitstud ja arvutatakse järgnevalt: **lepingu summa + maks**. | Fikseeritud hinnaga lepingurea korral kasutatakse seda väärtust perioodilise arvelduse vahe-eesmärkide loomiseks. |
| **Mitteületatav limiit** | Kasutaja saab seda välja redigeerida ja see on saadaval ainult projektipõhistel lepinguridadel, millel on määratud aja ja materjali põhjal arvete esitamise meetod. | Kasutaja saab seda välja redigeerida. Kui aja- ja materjalikulu tegelikud näitajad viitavad selle lepingurea ajale ja materjalile, hinnatakse tegeliku näitaja summa lepingurea mitte ületatava limiidiga võrreldes. See hindamine lõpetatakse pärast juba kulutatud ja kinnitatud summade arvestamist. |
| **Kliendi eelarve** | See väli on redigeeritav ja kopeeritakse hinnapakkumise rea vastavalt väljalt, kui lepingu loodi hinnapakkumisest. | Seda välja kasutatakse ainult teavitamiseks ja sellel pole allavoolu tähtsust. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Projektipõhiste lepinguridade vahekaardi Üldine valikute valideerimisreeglid

1. reegel: kui väli **Kaasatud ülesanded** on tühi või määratud väärtusele **Kõik projekti ülesanded**, kaasatakse lepingureale kõik projekti ülesanded.

2. reegel: kui väli **Kaasatud ülesanded** on tühi või otse määratud valikule **Kõik projekti ülesanded**, saab projekti ja teatud tehinguklassid kaasata ainult ühele lepingu projektipõhisele lepingureale.

3. reegel: kui väli **Kaasatud ülesanded** on määratud valikule **Ainult valitud projekti ülesanded**, saab projekti ja teatud tehinguklassid kaasata mitmele lepingu projektipõhisele lepingureale.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Leping</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Lepingurida</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Kaasatud ülesanded</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Kaasa aeg</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Kaasa kulu</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Kaasa materjalid</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Kaasamine</strong>
                </p>
                <p>
                    <strong>Tasu</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Kehtiv/kehtetu</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Põhjus</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tühi </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Kehtetu </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Reegli nr 2 rikkumine. P1-projekti aeg, kulu, materjalid ja tasud on kaasatud nii lepingureale CL1 kui ka CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tühi </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tühi </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Kehtetu </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Reegli nr 2 rikkumine. P1-projekti aeg, materjalid ja tasud on kaasatud nii lepingureale CL1 kui ka CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tühi </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tühi </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Sobiv </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
P1-projekti aeg, materjale ja tasud on kaasatud reale CL1.
                </p>
                <ul>
                    <li>
P1-projekti kulu on kaasatud reale CL2.
                    </li>
                </ul>
                <p>
Igal lepingureal sisalduv ei kattu ja on seetõttu kehtiv.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tühi </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Ainult valitud ülesanded </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Kehtetu </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Reegli nr 2 rikkumine </p>
                <p>
C1 sisaldab aega, materjale, kulusid ja tasusid P1-projekti ülesannete alamhulgas.
                </p>
                <p>
CL2 hõlmab kogu projektiga P1 seotud aega, materjale, kulutusi ja tasusid ning seega kattub see sellega, mis on kaasatud C1-te.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tühi </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Ainult valitud ülesanded </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Sobiv </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Reegli nr 3 kohta </p>
                <p>
C1 sisaldab aega, kulusid, materjale ja tasusid P1-projekti ülesannete alamhulgas.
                </p>
                <p>
CL2 sisaldab aega, kulusid, materjale ja tasusid P1-projekti ülesannete alamhulgas.
                </p>
                <p>
Ainus täiendav valideerimine on CL1 toimingute alamhulga ümber, mis erineb CL2 tööülesannete alamhulgast, tagamaks, et seal poleks kattumisi. Seda teeb süsteem ülesannete sidumisel.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Ainult valitud ülesanded </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
