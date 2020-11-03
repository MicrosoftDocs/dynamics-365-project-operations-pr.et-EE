---
title: Projektipõhised hinnapakkumise read
description: Selles teemas antakse teavet projektitööks projektipõhiste hinnapakkumise ridade kasutamise kohta.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074823"
---
# <a name="project-based-quote-lines"></a>Projektipõhised hinnapakkumise read

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Projektipõhised hinnapakkumise read on loodud selleks, et aidata hinnata kohustuse projektitööd. Projektipõhise hinnapakkumise rea struktuuri pikendatakse projekti prognooside alusel järgmiste kontseptsioonide järgi.

- Arveldusmeetod
- Projekti vastendamine
- Kaasatud tehingute klassid
- Mitteületatav limiit
- Arveldatavuse seadistus
- Prognoos hinnapakkumise rea üksikasjade abil
- Hinnapakkumisrea kliendid

Järgmine tabel annab teavet projektipõhise hinnapakkumise rea vahekaardi **Üldine** väljade kohta. Need väljad aitavad seadistada projektitöö üksikasjaliku, ligikaudse prognoosi aluse.

| **Väli** | **Asjakohasus, eesmärk ja juhised** | **Allavoolu mõjud** |
| --- | --- | --- |
| Nimetus | Hinnapakkumise rea nimi, mis peaks aitama teil tuvastada prognoositava hinnapakkumise diskreetse komponendi. | Kopeeritud projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Arveldusmeetod | Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väärtus vastavalt müügivõimaluse rea väljalt. See väli sisaldab kahte põhilist lepingumudelit, mida Dynamics 365 Project Operations toetab.</br>- Fikseeritud hind</br>- Aeg ja materjal.| Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Project | Kasutage seda valikulist välja, et tuvastada projekt, mida kasutatakse selle kohustusega seotud töö teostamiseks. Kui projekt on vastendatud hinnapakkumise reaga, aitab see teil seadistada tasustatavad tööülesanded ja esitada hinnapakkumise reale hinnapakkumise rea üksikasjadena projektipõhise prognoosi. Kui projekti ei vastendata projektipõhise hinnapakkumise reaga, tuleks prognoos luua käsitsi, luues kõigi hinnapakkumise ridade üksikasjad. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Kaasa aeg | Lipp **Jah**/**Ei** näitab, kas valitud projekti ajakanded või tööjõukulud kaasatakse selle hinnapakkumise rea prognoosi. Lipp **Ei** näitab, et valitud projekti ajakandeid või tööjõukulusid ei kaasata selle hinnapakkumise rea prognoosi. Lipp **Jah** näitab, et valitud projekti ajakanded või tööjõukulud kaasatakse selle hinnapakkumise rea prognoosi. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Kaasa kulu | Lipp **Jah**/**Ei** näitab, kas valitud projekti kulud kaasatakse selle hinnapakkumise rea prognoosi. Lipp **Ei** näitab, et valitud projekti kulusid ei kaasata selle hinnapakkumise rea prognoosi. Lipp **Jah** näitab, et valitud projekti kulud kaasatakse selle hinnapakkumise rea prognoosi. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Kaasa tasu | Lipp **Jah**/**Ei** näitab, kas valitud projekti tasud kaasatakse selle hinnapakkumise rea prognoosi. Lipp **Ei** näitab, et valitud projekti tasusid ei kaasata selle hinnapakkumise rea prognoosi. Lipp **Jah** näitab, et valitud projekti tasud kaasatakse selle hinnapakkumise rea prognoosi. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Hinnapakkumise summa | See on hinnapakkumise summa, mis esitatakse kliendile kõigi selle projektipõhise hinnapakkumise rea prognoositavate tööde kohta. Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väärtus müügivõimaluse rea väljalt **Kliendi eelarve**. Kui projektil põhineva hinnapakkumise real on rea üksikasjad, lukustatakse see väli redigeerimiseks ja summeeritakse hinnapakkumise rea üksikasjade summast. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Hinnanguline maks | See on redigeeritav väli, et kasutaja saaks lisada hinnapakkumise reale eeldatava maksude summa. Kui projektil põhineva hinnapakkumise real on rea üksikasjad, lukustatakse see väli redigeerimiseks ja summeeritakse hinnapakkumise rea maksu summast. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Hinnapakkumise summa pärast maksude mahaarvamist | See väli on hinnapakkumise rea summa pärast maksude mahaarvamist ja on kirjutuskaitstud. Sellel väljal olev summa arvutatakse kui *Hinnapakkumisega summa + käibemaks*. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Mitteületatav limiit | Seda välja saab redigeerida ja see on saadaval ainult projektipõhiste hinnapakkumiste ridadel, millel on arveldamise meetodiks **Aeg ja materjal**. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |
| Kliendi eelarve | See väli on redigeeritav ja see kopeeritakse vastavalt müügivõimaluse rea väljalt, kui hinnapakkumine on loodud müügivõimaluse põhjal. | Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Projektipõhiste hinnapakkumiste ridade vahekaardi Üldine väljade valideerimise reeglid

**1. reegel** : valitud projekti teatud kandeklassi saab lisada ainult hinnapakkumise ühele projektipõhise hinnapakkumise reale.

**2. reegel** : kui müügivõimalusel on mitu hinnapakkumist, võivad erinevate hinnapakkumiste hinnapakkumise read viidata samale projektile ja sisaldada sama kandeklassi.

**3. reegel** : kui hinnapakkumised ei kuulu sama müügivõimaluse juurde, ei saa nad sisaldada sama projekti ja kandeklassi.

<table border="1" cellspacing="0" cellpadding="0">
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
                    <strong>tasu</strong>
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
Reegli nr 1 rikkumine. P1-projekti aeg, kulud ja tasud on kaasatud mõlemale hinnapakkumise reale, QL1 ja QL2.
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
Reegli nr 1 rikkumine. P1-projekti aeg ja tasud on kaasatud mõlemale hinnapakkumise reale, QL1 ja QL2.
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
P1-projekti aeg ja tasud on kaasatud reale QL1.
P1-projekti kulu on kaasatud reale QL2.
See, mis on igale hinnapakkumise reale kaasatud, ei kattu, seega on see kehtiv.
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
Eeltoodud reegli nr 1 rikkumine </p>
                <p>
Q1 sisaldab kogu projekti P1 aega, kulu ja tasu.
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
Vastavalt reeglile nr 2 on Q1 ja Q2 kaks sama müügivõimalusega hinnapakkumist, nii et nad saavad mõlemad prognoosida projekti samu komponente.
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
Q2 rida QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
Vastavalt reeglile nr 3 on Q1 ja Q2 kaks erineva müügivõimaluse hinnapakkumist, nii et nad ei saa mõlemad prognoosida sama projekti komponente.
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

