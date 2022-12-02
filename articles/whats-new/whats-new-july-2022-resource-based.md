---
title: Mis on uut juulis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: See artikkel annab teavet rakenduse Microsoft Dynamics 365 Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks 2022. a juuli väljalaskes saadaolevate kvaliteedivärskenduste kohta.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403946"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut juulis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kehtib rakenduse Microsoft Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Rakenduse Project Operations Dataverse keskkonna versioonis 4.44.0.22
- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Selles väljaandes ei ole Project Operationsi topeltkirjutuse kaartide jaoks värskendusi. Project Operationsi topeltkijrutusega kaartide praeguse loendi ja versioonide jaoks vaadake teemat [Project Operationsi topeltkirjutamise kaardi versioonid](../environment/resource-dual-write-maps.md).

Käitage oma keskkonnas alati kaardi uusimat versiooni ja lubage kõik seotud tabelikaardid oma Project Operationsi lahenduse Dataverse ja Finance versiooni värskendamisel. Kui kaardi uusim versioon pole aktiveeritud, ei pruugi mõned funktsioonid ja võimalused õigesti töötada. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastivälise tabelikaardi, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib probleeme kaardi käivitamisel, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises [Probleem kaardilt puuduvate tabeli veergudega](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Juurutamine ja konfiguratsioon | 2761472 | Rakenduse Project Operations installimistõrkega tegeletakse. |
| Arveldamine ja hinnakujundus | 2746940 | Allhankelepingu rea nimi peab olema maksimaalselt 100 tähemärki pikk. |
| Arveldamine ja hinnakujundus | 2739162 | Kliendid peavad nägema lindi nuppe tegelike näitajate ruudustiku vaates. |
| Projekti plaanimine ja jälgimine | 2730318 | Värskendatud valideerimine projekti teemas toetamata tähemärkide jaoks. |
| Arveldamine ja hinnakujundus | 2705361 | Vahekokkuvõttega arveldatud müügi tegelikud näitajad peavad sisalduma projekti jälgimise väljadele. |
| Arveldamine ja hinnakujundus | 2675880 | Vältige projekti sidumist lepingureaga, mis ei ole tööpõhine. |
| Arveldamine ja hinnakujundus | 2664396 | Kui hinnapakkumise hinnakiri salvestatakse ilma hinnapakkumiseta, peab seal olema tõrge, mis ütleb, et pakkumine ei saa olla tühi. |
| Arveldamine ja hinnakujundus | 2184019 | Vahekaarti **Ülesandepõhine arveldamine** ei tohiks kuvada projektide puhul, millel puudub toetusleping või hinnapakkumine. |
| Aeg ja kulu | 2754459 | Kui korduv ajastamise pilvevoog on passiivne, kuvage bänner ja minge asünkroonimistöötlusest mööda. |
| Arveldamine ja hinnakujundus | 2724391 | Vale erand tehakse siis, kui projektilepingu jaotatud arveldusreeglil puudub kliendi väärtus. |
| Arveldamine ja hinnakujundus | 2708638 | Kirjet ei leitud, kui otsiti ruudustikuotsinguga jaotises Materjalikasutused ja Materjalikasutuse kinnitamised.|
| Arveldamine ja hinnakujundus | 2686977 | Takistage arve rea valideerimine arve loomise ajal. |
| Arveldamine ja hinnakujundus | 2683032 | Tasuliste rollide ja kategooriate kopeerimine ei ulatu üle 5000 kirje.|
| Arveldamine ja hinnakujundus | 2673363 | Projekti kulu % on rikutud, kui projekti jaoks on olemas nii pingutuse kui ka kulude prognoosid ja tegelikud näitajad. |

### <a name="project-management-and-accounting-in-finance"></a>Projektihaldus ja raamatupidamine rahanduses

Lisateabe saamiseks tõrkeparanduste kohta, mis sisalduvad selles värskenduses, logige sisse teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funktsioonid on tulevase versioonis vaikimisi sisse lülitatud

Järgmises tabelis on loetletud funktsioonid, mis on versioonis 10.0.29 vaikimisi sisse lülitatud. Enamiku automaatselt sisse lülitatud funktsioone saab sisse lülitada jaotises [Funktsioonihaldus](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Tulevikus võidakse mõned automaatselt sisse lülitatud funktsioonid funktsioonihaldusest eemaldada ja muutuda kohustuslikuks. See muudatus tagab, et kliendid kasutavad praegust funktsionaalsust, nii et täiustused saaksid nende lisamisel olemasolevatele funktsioonidele tugineda. Funktsioone ei lubata kunagi automaatselt vähem kui aasta pärast, välja arvatud juhul, kui need on hädavajalikud.

| Funktsiooni nimi | Lubamise kuupäev | Funktsioon lisatud | Funktsiooni olek | Moodul |
| --- | --- | --- |--- |--- |
| Tunnitehingu korrigeerimise lubamine rahastamisreegli jaotuse muutuse alusel | 16. september 2022 | 7. oktoober 2020 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Projekti ostutellimuse ettemaksuarve tühistamise funktsioon | 16. september 2022 | 6. oktoober 2021 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Kustutage arve ettepaneku read, kui kasutate rakenduse Project Operations ressursi-/mittelaopõhiste stsenaariumide jaoks | 16. september 2022 | 6. oktoober 2021 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Kohandage kirjendatud projektitehingu arvestust | 16. september 2022 | 10. mai 2020 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Raamatupidamise vaikeseade lubamine projekti jaoks | 16. september 2022 | 19. veebruar 2020 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Mitme lepingurea lubamine projekti jaoks | 16. september 2022 | 29. juuni 2020 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Muutke projektitunni ajakirjed kirjutuskaitstuks, kui praegune kinnitusolek ei võimalda redigeerimist | 16. september 2022 | 6. oktoober 2021 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Lubage müügiridade sünkroonimine osturidadest, kui osturidu värskendatakse ja ostutellimuse muudatuste haldusparameeter on sisse lülitatud | 16. september 2022 | 7. oktoober 2020 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Rakenduse Project Operations lubamine rakenduses Dynamics 365 Customer Engagement | 16. september 2022 | 29. juuni 2020 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Projekti tehingu tagasipööramise korrigeerimise funktsioon | 16. september 2022 | 13. juuli 2020 | Vaikimisi sees | Projektihaldus ja raamatupidamine |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funktsioonid, mis muutuvad tulevases versioonis kohustuslikuks

Järgmises tabelis on loetletud funktsioonid, mis on kohustuslikud alates versioonist 10.0.29.

| Funktsiooni nimi | Lubamise kuupäev | Funktsioon lisatud | Funktsiooni olek | Moodul |
| --- | --- | --- | --- | --- |
| Arvutage rahastamisallika kulutatud väärtus ilma vahetuskurssi ümardamata | 16. september 2022 | 14. juuni 2020 | Kohustuslik | Projektihaldus ja raamatupidamine |
| Pprojekti korrigeerimise kirjendamine lubamine algse tehinguga sama pearaamatukontoga | 16. september 2022 | 14. juuni 2020 | Kohustuslik | Projektihaldus ja raamatupidamine |
| Projekti lepingu kohustuse summa üksikasi | 16. september 2022 | 31. august 2019 | Kohustuslik | Projektihaldus ja raamatupidamine |
| Lubage projektiarve ettepaneku loomise ajal ressursi järgi sortimine | 16. september 2022 | 31. august 2019 | Kohustuslik | Projektihaldus ja raamatupidamine |
