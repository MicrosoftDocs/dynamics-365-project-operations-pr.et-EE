---
title: Mis on uut juulis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: Sellest artiklist leiate teavet kvaliteedivärskenduste kohta, mis on saadaval Microsofti Dynamics 365 Project Operations 2022. aasta juuli väljaandes ressursipõhiste/varudeta stsenaariumide jaoks.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183888"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut juulis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kehtib microsofti järgmiste komponentide ja versioonide kohta Dynamics 365 Project Operations:

- Projektitoimingud keskkonnaversioonis Dataverse 4.44.0.22
- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnas versioon 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Selles väljaandes ei ole Project Operationsi topeltkirjutuse kaartide jaoks värskendusi. Project Operationsi topeltkijrutusega kaartide praeguse loendi ja versioonide jaoks vaadake teemat [Project Operationsi topeltkirjutamise kaardi versioonid](../environment/resource-dual-write-maps.md).

Käivitage oma keskkonnas alati kaardi uusim versioon ja lubage project operationsi Dataverse lahenduse ja finance lahenduse versiooni värskendamisel kõik seotud tabelikaardid. Mõned funktsioonid ja võimalused ei pruugi õigesti töötada, kui kaardi uusim versioon pole aktiveeritud. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud valmis tabelikaarti, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib kaardi käivitamisel probleem, järgige juhiseid, mis on toodud [tõrkeotsingu juhendi Jaotises Puuduvad tabeli veerud kaardil](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Juurutamine ja konfiguratsioon | 2761472 | Käsitletakse rakenduse Project Operations installitõrget. |
| Arveldamine ja hinnakujundus | 2746940 | Allhankerea nime maksimaalne pikkus peaks olema 100 tähemärki. |
| Arveldamine ja hinnakujundus | 2739162 | Kliendid peavad nägema lindinuppe tegeliku ruudustiku vaates. |
| Projekti plaanimine ja jälgimine | 2730318 | Värskendatud on projekti teema toetamata märkide valideerimist. |
| Arveldamine ja hinnakujundus | 2705361 | Verstapostiga arveldatud müügi tegelikud näitajad tuleb kaasata projekti jälgimisväljadele. |
| Arveldamine ja hinnakujundus | 2675880 | Vältige projekti linkimist lepingureaga, mis pole tööpõhine. |
| Arveldamine ja hinnakujundus | 2664396 | Kui hinnapakkumise hinnakiri salvestatakse ilma hinnapakkumiseta, peab olema viga, mis ütleb, et hinnapakkumine ei saa olla tühi. |
| Arveldamine ja hinnakujundus | 2184019 | Vahekaarti **Ülesandepõhine arveldamine** ei tohiks kuvada projektide puhul, millel pole tugilepingut ega hinnapakkumist. |

### <a name="project-management-and-accounting-in-finance"></a>Projektijuhtimine ja raamatupidamine rahanduses

Selles värskenduses sisalduvate veaparanduste kohta teabe saamiseks logige sisse teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja vaadake [teabebaasi artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funktsioonid, mis on eelseisvas väljalaskes vaikimisi sisse lülitatud

Järgmises tabelis on loetletud funktsioonid, mis on versioonis 10.0.29 vaikimisi sisse lülitatud. Enamikku automaatselt sisse lülitatud funktsioone saab funktsioonihalduses [välja lülitada](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Tulevikus võidakse mõned automaatselt sisse lülitatud funktsioonid funktsioonihaldusest eemaldada ja muutuda kohustuslikuks. See muudatus tagab, et kliendid kasutavad praeguseid funktsioone, nii et täiustused saavad nende lisamisel tugineda praegusele funktsioonile. Funktsioone ei lubata automaatselt vähem kui ühe aasta jooksul, välja arvatud juhul, kui on kindlaks tehtud, et need on hädavajalikud.

| Funktsiooni nimi | Luba kuupäev | Funktsioon on lisatud | Funktsiooni olek | Moodul |
| --- | --- | --- |--- |--- |
| Tunnikande korrigeerimise lubamine rahastamisreegli eraldamise muudatuse alusel | 16. september 2022 | 7. oktoober 2020 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Projekti ostutellimuse ettemaksuarve ümberpööramise funktsioon | 16. september 2022 | 6. oktoober 2021 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Arvesoovituse ridade kustutamine, kui kasutate projektitoiminguid ressursipõhiste/ ladustamata stsenaariumide jaoks | 16. september 2022 | 6. oktoober 2021 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Sisestatud projektikande raamatupidamise korrigeerimine | 16. september 2022 | 10. mai 2020 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Luba projekti raamatupidamise vaikehäälestus | 16. september 2022 | 19. veebruar 2020 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Mitme lepingurea lubamine projekti jaoks | 16. september 2022 | 29. juuni 2020 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Project Houri töölehtede kirjutuskaitstuks muutmine, kui praegune kinnitamise olek ei luba redigeerimist | 16. september 2022 | 6. oktoober 2021 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Müügiridade sünkroonimise lubamine osturidadelt, kui osturidu värskendatakse ja ostutellimuse muutmise haldusparameeter on sisse lülitatud | 16. september 2022 | 7. oktoober 2020 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Project Operationsi lubamine Dynamics 365 Customer Engagement | 16. september 2022 | 29. juuni 2020 | Vaikimisi sees | Projektihaldus ja raamatupidamine |
| Projektikande ümberpööramise parandamise funktsioon | 16. september 2022 | 13. juuli 2020 | Vaikimisi sees | Projektihaldus ja raamatupidamine |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funktsioonid, mis muutuvad eelseisvas väljalaskes kohustuslikuks

Järgmises tabelis on loetletud funktsioonid, mis on kohustuslikud alates versioonist 10.0.29.

| Funktsiooni nimi | Luba kuupäev | Funktsioon on lisatud | Funktsiooni olek | Moodul |
| --- | --- | --- | --- | --- |
| Määratud väärtuse arvutamine rahastamisallika kohta ilma vahetuskurssi ümardamata | 16. september 2022 | 14. juuni 2020 | Kohustuslik | Projektihaldus ja raamatupidamine |
| Projekti korrigeerimise sisestamise lubamine sama pearaamatukontoga nagu algne kanne | 16. september 2022 | 14. juuni 2020 | Kohustuslik | Projektihaldus ja raamatupidamine |
| Projektilepinguga seotud summa üksikasjad | 16. september 2022 | 31. august 2019 | Kohustuslik | Projektihaldus ja raamatupidamine |
| Ressursi järgi sortimise lubamine projekti arvesoovituse loomise ajal | 16. september 2022 | 31. august 2019 | Kohustuslik | Projektihaldus ja raamatupidamine |
