---
title: Kontsernisisesed arved
description: See artikkel pakub teavet ja näiteid ettevõtete kontsernisiseste arvete kohta.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0385c796ca1ac02d6b8f66c04dad21bafe15ef8
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750909"
---
# <a name="intercompany-invoicing"></a>Kontsernisisesed arved

[!include [banner](../includes/banner.md)]

See artikkel pakub teavet ja näiteid ettevõtete kontsernisiseste arvete kohta.

Teie organisatsioonis võib olla mitu allüksust, tütarettevõtet ja muud juriidilist isikut, kes edastavad üksteisele tooteid ja teenuseid projektidele. Juriidilist isikut, mis pakub teenust või toodet, nimetatakse *laenuandjaks juriidiliseks isikuks* ja juriidilise isikut, kes saab teenuse või toote, nimetatakse *laenusaavaks juriidiliseks isikuks*. 

Järgmisel joonisel on kujutatud tüüpiline stsenaarium, kus kaks juriidilist isikut, SI FR (laenav juriidiline isik) ja SI USA (laenuandev juriidiline isik) jagavad ressursse, et pakkuda projekti kliendile A. Selle stsenaariumi jaoks on SI FR sõlminud lepingu, et pakkuda tööd kliendile A. 

[![Kontsernisisese arve näide](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Eesmärgiks on muuta kontsernisisese projekti kulude kontroll, tulude kajastamine, maksud ja edastamise hind paindlikumaks ja tõhusamaks. Lisaks on saadaval järgmised võimalused.

-   Kliendi arvete loomine laenu saava juriidilise isiku projekti kohta, kasutades kontsernisiseseid ajatabeleid, kulusid ja tarnijaarveid laenuandvad juriidilises üksuses.
-   Tugiteenuste maksuarvutused ja kaudsed kulud.
-   Tulu kajastamise viivitamine laenuandvas juriidilises üksuses ja kui laenusaav juriidiline üksus peaks ära tundma kulu.
-   Kogunenud töö (WIP) tulu laenuandvas juriidilises üksuses.
-   Määrake edastuse hinnad, mis võivad põhineda erinevatel hinnakujunduse mudelitel. Järgmiselt on toodud mõned näited.
    -   **Kogus** – summa, mille sisestate väljale **Hind**, on tegelik kulu koguse või ühiku kohta.
    -   **Maksude summa** – hind/kulu tehingu kohta ja tasude summa, mille sisestate väljale **Hind**.
    -   **Maksude protsent** – ülekandehind on hind/kulu tehingu kohta, mis on korrutatud tasu protsendiga, mille sisestate väljale **Hind**.
    -   **Müügihinna protsent** – müügihinna protsent, mis kantakse üle laenuandvale juriidilisele üksusele.
    -   **Summa, mis on madalam kui müügihind** – summa, mille laenusaav juriidiline üksus on müügihinnast tagasi võtnud enne seda, kui see on ülekantud laenuandvale juriidilisele üksusele.
    -   **Tulumäär** – väljale **Hind** sisestatav arv on tulumäär, mis on väljendatud müügihinna protsendina.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Näide 1: kontsernisiseste arvete parameetrite seadistamine
Selles näites on USSI laenuandev juriidiline üksus ja selle ressursid kajastavad aega laenusaava juriidilise isiku FRSI suhtes, kes omab lepingut lõppkliendiga. Tunde ja kulusid, mida USSI töötajad raporteerivad, saab kaasata FRSI loodud projekti arvesse. Lisaks on olemas kolmas tehingute allikas, mis võib pärineda laenuandvast juriidilisest üksusest (USSI selles näites), kui see pakub tütarettevõtetele (näiteks FRSI) jagatud tarnijate teenuseid, ja seejärel edastab need kulud neile tütarettevõtjatele kuuluvatele projektidele. Kõik vastavad arvedokumendid ja maksukalkulatsioonid täidetakse rakenduses Finance. 

Selles näites peab FRSI olema USSI juriidilise isiku klient ja USSI peab olema FRSI juriidilise isiku tarnija. Seejärel saate seadistada kahe juriidilise üksuse vahel kontsernisisese seose. Järgmises toimingus kirjeldatakse, kuidas seadistada parameetreid nii, et mõlemad juriidilised üksused saavad osaleda kontsernisisestes arvetes.

1. Seadistage FRSI kliendina USSI juriidilises isikus ja seadistage USSI tarnijana FRSI juriidilises isikus. Selle ülesande jaoks vajalike sammude jaoks on kolm sisenemispunkti.

   | Etapp |                                                       Sisenemispunkt                                                        |                                                                                                                                                                                               Kirjeldus                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | USSI-s klõpsake <strong>Müügireskontro</strong> &gt; <strong>Kliendid</strong> &gt; <strong>Kõik kliendid</strong>. |                                                                                                                                                                  Looge FRSI jaoks uus kliendi kirje ja valige soovitud kliendirühm.                                                                                                                                                                  |
   |  P   |    Klõpsake FRSI-s <strong>Ostureskontro</strong> &gt; <strong>Tarnijad</strong> &gt; <strong>Kõik tarnijad</strong>.     |                                                                                                                                                                    Looge USSI jaoks uus tarnijakirje ja valige soovitud tarnijarühm.                                                                                                                                                                    |
   |  C   |                                  Avage FRSI-s äsja loodud tarnijakirje.                                  | Klõpsake toimingupaanil vahekaardil <strong>Üldine</strong> rühmas <strong>Seadistus</strong> <strong>Kontsernisisesed</strong>. Lehel <strong>Kontsernisisesed</strong>, vahekaardil <strong>Kaubandussuhted</strong> seadke liugur <strong>Aktiivsed</strong> asendisse <strong>Jah</strong>. Väljal <strong>Kliendi ettevõte</strong> valige kliendikirje, mille lõite sammus A. |


2. Klõpsake **Projekti haldamine ja raamatupidamine** &gt; **Seadistamine** &gt; **Projekti haldamise raamatupidamisparameetrid** ja seejärel klõpsake vahekaarti **Kontsernisisesed**. Parameetrite seadistamise viis sõltub sellest, kas olete laenuvõttev juriidiline isik või laenuandev juriidiline isik.
   -   Kui olete laenuvõttev juriidiline isik, valige hankekategooria, mida tuleks kasutada tarnija arvete vastendamiseks, mis luuakse automaatselt.
   -   Kui olete laenuandev juriidiline isik, valige iga laenuvõtja üksuse jaoks iga kandetüübi jaoks vaikimisi kasutatav projekti kategooria. Projekti kategooriaid kasutatakse maksude konfigureerimiseks juhul, kui kontsernisiseste tehingute kategooria on olemas ainult laenvõtval juriidilisel isikul. Saate valida, kas koguda tulu kontsernisiseste kannete jaoks. See kogumine tehakse kannete sisestamisel ja seejärel tühistatakse kontsernisisese arve sisestamisel.

3. Klõpsake **Projektijuhtimine ja raamatupidamine** &gt; **Seadistamine** &gt; **Hinnad** &gt; **Ülekandehind**.
4. Valige valuuta, tehingutüüp ja ülekandehinna mudel. Arvel kasutatav valuuta on valuuta, mis on kliendi kirjes seadistatud laenuvõtva juriidilise isiku jaoks laenuandvale juriidilisele iskule. Valuutat kasutatakse kirjete vastendamiseks ülekannete maksumuse tabelis.
5. Klõpsake **Pearaamat** &gt; **Sisestuse seadistus** &gt; **Kontsernisisene raamatupidamine** ja seadke suheUSSI ja FRSI jaoks.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Näide 2: kontsernisisese ajatabeli loomine ja sisestamine
USSI, laenuandev juriidiline isik, peab looma ja sisestama projekti ajatabeli FRSI, laenavõtva juriidilise isiku jaoks. Selle ülesande jaoks vajalike sammude jaoks on kaks sisenemispunkti.

| Etapp | Sisenemispunkt                                                                       | Kirjeldus                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektijuhtimine ja raamatupidamise** &gt; **Ajatabelid** &gt; **Kõik ajatabelid** | Uue komponendi loomine. Ajatabeli real, väljal **Juriidiline üksus** valige **FRSI**. Väljal **Projekti ID** valige projekt FRSI-s. Sisestage iga nädalapäeva tunnid. |
| P    | **Ajatabeli** leht                                                                | Pärast töövoo käitamist sisestage ajatabel ja märkige kande number.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Näide 3: kontsernisisese tarnijaarve loomine ja sisestamine
USSI, laenuandev juriidiline isik, peab looma ja sisestama projekti kontsernisisese tarnijaarve FRSI, laenavõtva juriidilise isiku jaoks. See tarnijaarve näitab allhanke korras tehtud tööd ja kulu, mis on teostatud USSI poolt tasutud tarnijatelt. Selle ülesande jaoks vajalike sammude jaoks on kaks sisenemispunkti.

| Etapp | Sisenemispunkt                                                                                      | Kirjeldus                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Ostureskontro** &gt; **Arved** &gt; **Avatud tarnijaarved** &gt; **Uus tarnijaarve** | Looge uus tarnijaarve ja sisestage teenused, mis on hangitud FRSI nimel.                                                                                                                                                                                  |
| P    | Leht **Tarnija arve**                                                                      | Saate sisestada read, mis esindavad alhankena pakutavaid teenuseid FRSI nimel. Kiirkaardil **Rea üksikasjad** vahekaardil **Projekt** arve rea jaoks väljal **Projekti ettevõte** sisestage **FRSI**. Sisestage projekt ja vastav teave. Seejärel sisestage tarnija arve. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Näide 4: kontsernisisese tarnijaarve loomine ja sisestamine
USSI, laenuandev juriidiline isik peab looma ja sisestama kontsernisisese arve. Selle ülesande jaoks vajalike sammude jaoks on kaks sisenemispunkti.

| Etapp | Sisenemispunkt                                                                                             | Kirjeldus                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projekti haldus ja raamatupidamine** &gt; **Projekti arved** &gt; **Kontsernisisese kliendi arve**  | Klõpsake nuppu **Uus**, et avada leht **Kontsernisisese arve loomine**.                                                                                  |
| P    | **Projektihaldus ja raamatupidamine** &gt; **Projekti arved** &gt; **Kontsernisisese kliendi arved** | Lehel **Kontsernisisene** arve, sisestage juriidiline isik, määrake hõlmatav tehing ja klõpsake **Otsi**. |
| C    | **Projektihaldus ja raamatupidamine** &gt; **Projekti arved** &gt; **Kontsernisisese kliendi arved** | Valige arveldatavad kanded või klõpsake **Vali kõik**, et teha arve loendi kõigi tehingute kohta ja seejärel klõpsake nuppu **OK**.                  |
| D    | Leht **Kontsernisisene arve**                                                                       | Kuvatakse kontsernisisese kliendi arve soovitus.                                                                                             |
| E    | Leht **Kontsernisisene arve**                                                                       | Klõpsake **Sisesta**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Näide 5: sisestage tarnija arve ja saatke kliendile
Kui laenuandev juriidiline isik USSI sisestab kontsernisisese kliendiarve, luuakse ootel tarnijaarve laenuvõtvasse juriidilisse isikusse, FRSI-sse. Pärast selle tarnijaarve sisestamist arveldab FRSI ka projekti kliendiga USSI sisestatud tundide eest. Selle ülesande jaoks vajalike sammude jaoks on kolm sisenemispunkti.

| Etapp | Sisenemispunkt                                                                                        | Kirjeldus                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Ostureskontro** &gt; **Arved** &gt; **Ootel tarnija arved**                            | Vaadake arve üle veendumaks, et ajatabeli väärtused on kaasatud, ja seejärel sisestage tarnija arve.                  |
| P    | **Projektihaldus ja raamatupidamine** &gt; **Projekti arved** &gt; **Projekti arvete ettepanekud** | Looge projekti jaoks uus projektiarve ja kontrollige, kas sisestatud tundide kanded kuvatakse.            |
| C    | Leht **Projektiarve**                                                                       | Valige projektiarve ja seejärel klõpsake nuppu **Kuva üksikasjad**, et vaadata kulu- ja müügisummat. Seejärel sisestage arve. |


Lisateavet vt teemast [Kontsernisiseste projektide arvete konfigureerimine](tasks/configure-intercompany-project-invoicing.md).


