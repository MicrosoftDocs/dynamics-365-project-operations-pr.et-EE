---
title: Projektipõhiste hinnapakkumiste ridade ülevaade – liht
description: Selles teemas antakse teavet projektitööks projektipõhiste hinnapakkumise ridade kasutamise kohta. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4865c06691fba09eacf5fe6449adfaf542444520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272968"
---
# <a name="project-based-quote-lines-overview---lite"></a>Projektipõhiste hinnapakkumiste ridade ülevaade – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

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
| Nimetus | Hinnapakkumise rea nimi, mis peaks aitama teil tuvastada prognoositava hinnapakkumise diskreetse komponendi. | Kopeeritud projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Arveldusmeetod | Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väärtus vastavalt müügivõimaluse rea väljalt. See väli sisaldab kahte peamist lepingumudelit, mida rakendus Dynamics 365 Project Operations toetab.</br>- Fikseeritud hind</br>- Aeg ja materjal.| Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Project | Kasutage seda valikulist välja, et tuvastada projekt, mida kasutatakse selle kohustusega seotud töö teostamiseks. Kui projekt on vastendatud hinnapakkumise reaga, aitab see teil seadistada tasustatavad tööülesanded ja esitada hinnapakkumise reale hinnapakkumise rea üksikasjadena projektipõhise prognoosi. Kui projekti ei vastendata projektipõhise hinnapakkumise reaga, tuleks prognoos luua käsitsi, luues kõigi hinnapakkumise ridade üksikasjad. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.|
| Kaasatud ülesanded | Näitab, kas seda hinnapakkumise rida kasutatakse valitud projekti kõigi või mõnede projekti toimingute jaoks. Sellel väljal on järgmised võimalikud väärtused.</br>- Kõik projekti ülesanded</br>- Ainult valitud projekti ülesanded</br>Tühi väärtus sellel väljal võrdub valikuga **Kõik projekti ülesanded**. | Kui projekti lehel on valitud **Ainult valitud projekti ülesanded**, võimaldab vahekaart **Ülesande arvelduse seadistus** teil valida konkreetsed ülesanded selle hinnapakkumise reaga sidumiseks. Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Kaasa aeg | Lipp **Jah**/**Ei** näitab, kas valitud projekti ajakanded või tööjõukulud kaasatakse selle hinnapakkumise rea prognoosi. Lipp **Ei** näitab, et valitud projekti ajakandeid või tööjõukulusid ei kaasata selle hinnapakkumise rea prognoosi. Lipp **Jah** näitab, et valitud projekti ajakanded või tööjõukulud kaasatakse selle hinnapakkumise rea prognoosi. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Kaasa kulu | Lipp **Jah**/**Ei** näitab, kas valitud projekti kulud kaasatakse selle hinnapakkumise rea prognoosi. Lipp **Ei** näitab, et valitud projekti kulusid ei kaasata selle hinnapakkumise rea prognoosi. Lipp **Jah** näitab, et valitud projekti kulud kaasatakse selle hinnapakkumise rea prognoosi. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Kaasa tasu | Lipp **Jah**/**Ei** näitab, kas valitud projekti tasud kaasatakse selle hinnapakkumise rea prognoosi. Lipp **Ei** näitab, et valitud projekti tasusid ei kaasata selle hinnapakkumise rea prognoosi. Lipp **Jah** näitab, et valitud projekti tasud kaasatakse selle hinnapakkumise rea prognoosi. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Hinnapakkumise summa | See on hinnapakkumise summa, mis esitatakse kliendile kõigi selle projektipõhise hinnapakkumise rea prognoositavate tööde kohta. Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väärtus müügivõimaluse rea väljalt **Kliendi eelarve**. Kui projektil põhineva hinnapakkumise real on rea üksikasjad, lukustatakse see väli redigeerimiseks ja summeeritakse hinnapakkumise rea üksikasjade summast. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Hinnanguline maks | See on redigeeritav väli, et kasutaja saaks lisada hinnapakkumise reale eeldatava maksude summa. Kui projektil põhineva hinnapakkumise real on rea üksikasjad, lukustatakse see väli redigeerimiseks ja summeeritakse hinnapakkumise rea maksu summast. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Hinnapakkumise summa pärast maksude mahaarvamist | See väli on hinnapakkumise rea summa pärast maksude mahaarvamist ja on kirjutuskaitstud. Sellel väljal olev summa arvutatakse kui *Hinnapakkumisega summa + käibemaks*. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Mitteületatav limiit | Seda välja saab redigeerida ja see on saadaval ainult projektipõhiste hinnapakkumiste ridadel, millel on arveldamise meetodiks **Aeg ja materjal**. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Kliendi eelarve | See väli on redigeeritav ja see kopeeritakse vastavalt müügivõimaluse rea väljalt, kui hinnapakkumine on loodud müügivõimaluse põhjal. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Projektipõhiste hinnapakkumiste ridade vahekaardi Üldine väljade valideerimise reeglid

**1. reegel**: kui väli **Kaasatud ülesanded** on tühi või seadistatud väärtusele **Kõik projekti ülesanded**, kaasatakse projekt hinnapakkumise reale.

**2. reegel**: kui väli **Kaasatud ülesanded** on tühi või kui selle sätte väärtuseks on seatud **kõik projekti tööülesanded**, saab projekti ja teatud kandeklassi kaasata ainult hinnapakkumise ühele projektipõhisele hinnapakkumise reale.

**3. reegel**: kui väli **Kaasatud ülesanded** on seadistatud väärtusele **Ainult valitud projekti ülesanded**, saab projekti ja teatud kandeklassi kaasata hinnapakkumise mitmele projektipõhisele hinnapakkumise reale.

**4. reegel**: kui müügivõimalusel on mitu hinnapakkumist, võivad erinevate hinnapakkumiste hinnapakkumise read viidata samale projektile ja sisaldada sama kandeklassi.

**5. reegel**: kui hinnapakkumised ei kuulu sama müügivõimaluse juurde, ei saa nad sisaldada sama projekti ja kandeklassi.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Müügivõimalus</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Hinnapakkumine</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Hinnapakkumise rida</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="90" valign="top">
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
                    <strong>Kaasa</strong>
                </p>
                <p>
                    <strong>Tasu</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Kehtiv/kehtetu</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Põhjus</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Kehtetu </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Reegli nr 2 rikkumine. P1-projekti aeg, kulud ja tasud on kaasatud hinnapakkumise ridadele QL1 ja QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Kehtetu </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Reegli nr 2 rikkumine. P1-projekti aeg ja tasud on kaasatud hinnapakkumise ridadele QL1 ja QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Kehtib </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
P1-projekti tasud on kaasatud reale QL1.
P1-projekti kulu on kaasatud reale QL2.
See, mis on igale hinnapakkumise reale kaasatud, ei kattu ja on see kehtiv.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Kehtetu </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Eeltoodud reegli nr 2 rikkumine </p>
                <p>
Q1 sisaldab projekti P1 ülesannete alamhulga aega, kulusid ja tasusid.
                </p>
                <p>
QL2 sisaldab kogu projekti P1 aega, kulu ja tasu ning kattub sellega, mis on kaasatud reale Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Kehtib </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Vastavalt eeltoodud reeglile nr 3, </p>
                <p>
Q1 sisaldab projekti P1 ülesannete alamhulga aega, kulusid ja tasusid.
                </p>
                <p>
QL2 sisaldab projekti P1 ülesannete alamhulga aega, kulusid ja tasusid.
                </p>
                <p>
Ainus täiendav valideerimine toimub QL1 tööülesannete alamhulga ümber, mis erineb QL2 tööülesannete alamhulgast. See tagab, et kattumist ei esineks. Seda teeb süsteem ülesannete sidumisel.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Kõik projekti ülesanded või tühi </p>
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
            <td width="54" valign="top">
                <p>
Kehtib </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Vastavalt reeglile nr 5 on Q1 ja Q2 kaks sama müügivõimalusega hinnapakkumist, nii et nad saavad mõlemad prognoosida projekti samu komponente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kv2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Kõik projekti ülesanded või tühi </p>
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
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Kõik projekti ülesanded või tühi </p>
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
            <td width="54" valign="top">
                <p>
Kehtib </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Vastavalt reeglile nr 4 on Q1 ja Q2 kaks erineva müügivõimaluse hinnapakkumist, nii et nad ei saa mõlemad prognoosida sama projekti komponente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kv1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Kõik projekti ülesanded või tühi </p>
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
            <td width="54" valign="top">
                <p>
Kehtetu </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]