---
title: Projektipõhiste hinnapakkumiste ridade ülevaade
description: See artikkel annab teavet projektitööks projektipõhiste hinnapakkumise ridade kasutamise kohta.
author: rumant
ms.date: 03/30/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 90c5affa25b113476e43f0bbbadd5c9615f9c05c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934453"
---
# <a name="project-based-quote-lines-overview"></a>Projektipõhiste hinnapakkumiste ridade ülevaade 

_**Kehtib järgmistele:** lihtjuurutamine – tehing näidisarveldusele, Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks_

Projektipõhised hinnapakkumise read on loodud selleks, et aidata hinnata kohustuse projektitööd. Projektipõhise hinnapakkumise rea struktuuri pikendatakse projekti prognooside alusel järgmiste kontseptsioonide järgi.

- Arveldusmeetod
- Projekti ja ülesannete vastendamine
- Kaasatud tehingute klassid
- Mitteületatav limiit
- Arveldatavuse seadistus
- Prognoos hinnapakkumise rea üksikasjade abil
- Hinnapakkumisrea kliendid

Järgmine tabel annab teavet projektipõhise hinnapakkumise rea vahekaardi **Üldine** väljade kohta. Need väljad aitavad seadistada projektitöö üksikasjaliku, ligikaudse prognoosi aluse.

| **Väli** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- |
| Nimetus | Hinnapakkumise rea nimi, mis aitab teil teha kindlaks prognoositava hinnapakkumise diskreetse komponendi. | Kopeeritud projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Arveldusmeetod | Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väärtus vastavalt müügivõimaluse rea väljalt. See väli sisaldab kahte peamist lepingumudelit, mida rakendus Dynamics 365 Project Operations toetab.</br>- Fikseeritud hind</br>- Aeg ja materjal.| See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud. |
| Project | Kasutage seda valikulist välja, et tuvastada projekt, mida kasutatakse selle kohustusega seotud töö teostamiseks. Kui projekt on vastendatud hinnapakkumise reaga, aitab see teil seadistada tasustatavad tööülesanded ja esitada hinnapakkumise reale hinnapakkumise rea üksikasjadena projektipõhise prognoosi. Kui projekti ei vastendata projektipõhise hinnapakkumise reaga, tuleks prognoos luua käsitsi, luues kõigi hinnapakkumise ridade üksikasjad. | See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud.|
| Kaasatud ülesanded | Näitab, kas seda hinnapakkumise rida kasutatakse valitud projekti kõigi või mõnede projekti toimingute jaoks. Sellel väljal on järgmised võimalikud väärtused.</br>- Kõik projekti ülesanded</br>- Ainult valitud projekti ülesanded</br>Tühi väärtus sellel väljal võrdub valikuga **Kõik projekti ülesanded**. | Kui projekti lehel on valitud **Ainult valitud projekti ülesanded**, saate vahekaardil **Ülesande arvelduse seadistus** valida konkreetsed tööülesanded, et seostada need selle hinnapakkumise reaga. See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud. |
| Kaasa aeg | Väärtus **Jah**/**Ei** näitab, kas valitud projekti tehingu või tööjõu maksumused lisatakse selle hinnapakkumise rea prognoosile. Lipp **Ei** näitab, et valitud projekti ajakandeid või tööjõukulusid ei kaasata selle hinnapakkumise rea prognoosi. Lipp **Jah** näitab, et valitud projekti ajakanded või tööjõukulud kaasatakse selle hinnapakkumise rea prognoosi. | See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud. |
| Kaasa kulu | Väärtus **Jah**/**Ei** näitab, kas valitud projekti kulu maksumused lisatakse selle hinnapakkumise rea prognoosile. Lipp **Ei** näitab, et valitud projekti kulusid ei kaasata selle hinnapakkumise rea prognoosi. Lipp **Jah** näitab, et valitud projekti kulud kaasatakse selle hinnapakkumise rea prognoosi. | See väärtus kopeeritakse üle projekti lepingurea, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud. |
| Kaasa materjal | Väärtus **Jah**/**Ei** näitab, kas valitud projekti materjali maksumused lisatakse selle hinnapakkumise rea prognoosile. Väärtus **Ei** näitab, et materjali maksumust ei lisata selle hinnapakkumise rea prognoosile. Väärtus **Jah** näitab, et materjali maksumus lisatakse selle hinnapakkumise rea prognoosile. | See väärtus kopeeritakse üle projekti lepingurea, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud. |
| Kaasa tasu | Väärtus **Jah**/**Ei** näitab, kas valitud projekti tasud lisatakse selle hinnapakkumise rea prognoosile. Väärtus **Ei** näitab, et valitud projekti tasusid ei lisata selle hinnapakkumise rea prognoosile. Väärtus **Jah** näitab, et valitud projekti tasud lisatakse selle hinnapakkumise rea prognoosile. | See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud. |
| Hinnapakkumise summa | See on summa, mis esitatakse kliendile hinnapakkumisena selle projektipõhise hinnapakkumise rea kogu prognoositud töö kohta. Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väärtus müügivõimaluse rea väljalt **Kliendi eelarve**. Kui projektil põhineva hinnapakkumise real on rea üksikasjad, lukustatakse see väli redigeerimiseks ja summeeritakse hinnapakkumise rea üksikasjade summast. | See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud. |
| Hinnanguline maks | See on redigeeritav väli, et kasutaja saaks lisada hinnapakkumise reale eeldatava maksude summa. Kui projektil põhineva hinnapakkumise real on rea üksikasjad, lukustatakse see väli redigeerimiseks ja summeeritakse hinnapakkumise rea maksu summast. | See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud. |
| Hinnapakkumise summa pärast maksude mahaarvamist | See väli on hinnapakkumise rea summa pärast maksude mahaarvamist ja on kirjutuskaitstud. Sellel väljal olev summa arvutatakse kui *Hinnapakkumisega summa + käibemaks*. | See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud. |
| Mitteületatav limiit | Seda välja saab redigeerida ja see on saadaval ainult projektipõhiste hinnapakkumiste ridadel, millel on arveldamise meetodiks **Aeg ja materjal**. | See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud. |
| Kliendi eelarve | See väli on redigeeritav ja see kopeeritakse vastavalt müügivõimaluse rea väljalt, kui hinnapakkumine on loodud müügivõimaluse põhjal. | See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Projektipõhiste hinnapakkumiste ridade vahekaardi Üldine väljade valideerimise reeglid

**1. reegel**: kui väli **Kaasatud ülesanded** on tühi või seadistatud väärtusele **Kõik projekti ülesanded**, kaasatakse projekt hinnapakkumise reale.

**2. reegel**: kui väli **Kaasatud ülesanded** on tühi või kui selle sätte väärtuseks on seatud **kõik projekti tööülesanded**, saab projekti ja teatud kandeklassi kaasata ainult hinnapakkumise ühele projektipõhisele hinnapakkumise reale.

**3. reegel**: kui väli **Kaasatud ülesanded** on seadistatud väärtusele **Ainult valitud projekti ülesanded**, saab projekti ja teatud kandeklassi kaasata hinnapakkumise mitmele projektipõhisele hinnapakkumise reale.

**4. reegel**: kui müügivõimalusel on mitu hinnapakkumist, võivad erinevate hinnapakkumiste hinnapakkumise read viidata samale projektile ja sisaldada sama kandeklassi.

**5. reegel**: kui hinnapakkumised ei kuulu sama müügivõimaluse juurde, ei saa nad sisaldada sama projekti ja kandeklassi.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Müügivõimalus</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Hinnapakkumine</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Hinnapakkumise rida</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Kaasatud ülesanded</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Kaasa aeg</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Kaasa kulu</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Kaasa materjal</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Kaasamine</strong>
                </p>
                <p>
                    <strong>Tasu</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Kehtiv/kehtetu</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Põhjus</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tühi </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Kehtetu </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Reegli nr 2 rikkumine. P1-projekti aeg, kulud ja tasud on kaasatud hinnapakkumise ridadele QL1 ja QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tühi </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tühi </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Kehtetu </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Reegli nr 2 rikkumine. P1-projekti aeg, materjal ja tasud on kaasatud hinnapakkumise ridadele QL1 ja QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tühi </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tühi </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Sobiv </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
P1-projekti aeg, materjal ja tasud on kaasatud reale QL1 <br>
P1-projekti kulu on kaasatud reale QL2 <br>
Igal hinnapakkumise real olev ei kattu ja on seetõttu kehtiv.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tühi </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Ainult valitud ülesanded </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Kehtetu </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Reegli nr 2 rikkumine </p>
                <p>
Q1 sisaldab aega, materjale, kulusid ja tasusid P1-projekti ülesannete alamhulgas </p>
                <p>
QL2 hõlmab kogu projektiga P1 seotud aega, kulutusi ja tasusid ning seega kattub see sellega, mis on kaasatud Q1-te.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tühi </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Ainult valitud ülesanded </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Sobiv </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Reegli nr 3 järgi </p>
                <p>
Q1 sisaldab aega, materjale, kulusid ja tasusid P1-projekti ülesannete alamhulgas.
                </p>
                <p>
QL2 sisaldab aega, materjale, kulusid ja tasusid P1-projekti ülesannete alamhulgas.
                </p>
                <p>
Ainus täiendav valideerimine on QL1 toimingute alamhulga ümber, mis erineb QL2 tööülesannete alamhulgast, tagamaks, et poleks kattumist. Seda teeb süsteem ülesannete sidumisel.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Ainult valitud ülesanded </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kõik projekti ülesanded või tühi </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Sobiv </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Reegli nr 5 järgi on Q1 ja Q2 kaks sama müügivõimaluse hinnapakkumist, seega saavad mõlemad hinnata projekti samu komponente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Kv2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kõik projekti ülesanded või tühi </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kõik projekti ülesanded või tühi </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Kehtetu </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Reegli nr 4 järgi on Q1 ja Q2 kaks erineva müügivõimaluse hinnapakkumist, seega ei saa need mõlemad hinnata sama projekti samu komponente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kõik projekti ülesanded või tühi </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
