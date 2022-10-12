---
title: Mis on uut septembris 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: Sellest artiklist leiate teavet kvaliteedivärskenduste kohta, mis on saadaval Microsofti Dynamics 365 Project Operations 2022. aasta septembri väljaandes ressursipõhiste/varumata stsenaariumide jaoks.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621320"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut septembris 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kehtib microsofti järgmiste komponentide ja versioonide kohta Dynamics 365 Project Operations:

- Projektitoimingud keskkonnaversioonis Dataverse 4.46.0.60
- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnas versioon 10.0.29

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

| Funktsiooni ala | Funktsiooni nimi | Lisateave |
| --- | --- | --- |
| Müügivõimaluse haldus | **Tsitaatide läbivaatamine ja aktiveerimine**<br>Project Operations toob müügiprotsessi täieliku toe. Projekti hinnapakkumisi saab aktiveerida, et esindada olekut, kus hinnapakkumine on kirjutuskaitstud ja seda vaadatakse üle. Aktiveeritud hinnapakkumisi saab muuta, et luua uusi hinnapakkumisi, millel on astmeline parandusnumber. Aktiveeritud projekti hinnapakkumisi või hinnapakkumisi saab sulgeda kui võidetud või kaotatud. | [Projekti hinnapakkumise aktiveerimine ja kontrollimine](/dynamics365/project-operations/sales/activation-and-revision) |
| Arveldamine ja hinnakujundus | **Ajavööndi agnostiline hind on vaikimisi**<br>Project Operations on võtnud kasutusele ajavööndi agnostilise kuupäeva kontseptsiooni kõigil projekti tegelikel osadel. Uus väli **Kande kuupäev** on nüüd saadaval töölehe ridadel ja tegelikel andmetel ning seda kasutatakse kande toimumise kuupäeva salvestamiseks, kuid ilma seda kuupäeva koordineeritud maailmaajaks teisendamata. Seda kuupäeva kasutatakse järgmise etapi protsesside jaoks, nagu hinna vaikeväärtuse määramine ja arve loomine. | <p>[Projektipõhiste prognooside ja tegelike kulude määra määramine](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Projektipõhiste prognooside ja tegelike hindade müügihindade määramine](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Arveldamine ja hinnakujundus | **Jõustumiskuupäeva hinna alistamised Project Operationsis**<br>Jõustumiskuupäevaga hinna alistamised võimaldavad hinnakirjas konkreetseid hindu alistada või muuta. | [Jõustumiskuupäevaga hinna alistamised](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Allhanked | **Alltöövõtt ja hankija arve vastavusse viimine**<br>See funktsioon võimaldab klientidel luua alltöövõtulepinguid, et osta ressursi aega, kulukategooriaid ja materjale, mida kasutatakse projektitöös. Samuti võimaldab see klientidel finants- ja toimingurakendustes salvestada hankija arveid, mis on projektijuhtidele Dataverse kinnitamiseks saadaval. | <p>[Alltöövõtu haldamine](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Hankija arvete koostamine](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Aeg ja kulu | **Globaalne kinnitaja**<br>See funktsioon võimaldab sõltumatut tarkvaratarnijat (ISV) ja tsentraliseeritud kinnitamist, olenemata projekti või meeskonnaliikme staatusest projektis. | [Turve ja kinnitused](/dynamics365/project-operations/approvals/approvals-security) |
| Kuluhaldus | **Võimalus sisestada kulukohustus hankija valuutas**<br>See funktsioon võimaldab kuluaruandeid sisestada sularaha makseviisi hankija valuutas. | [Võimalus sisestada kulukohustus hankija valuutas](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projekti hanked | **Maksa, kui maksad hankija maksed**<br>See funktsioon võimaldab funktsiooni Maksa maksmisel (PWP) kasutada Project Operationsi mittelaos asuvate keskkondadega. See võimaldab hankija makseid blokeerida/säilitada säilitamistingimuste alusel kuni makse laekumiseni kliendilt. | [Maksa, kui maksad hankija maksed](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projekti hanked | **Projekti ostutaotlused**<br>See funktsioon võimaldab kasutajatel luua projektiga seotud ostutellimusi juriidilistes isikutes, kus project operations on Dynamics 365 Customer Engagement integratsioon on lubatud. Projekti ostutellimusi saab kasutada ladustamata materjalihangete kirjendamiseks projekti suhtes hankeosakonna persona poolt. Projekti ostutellimusi ei sünkroonita Dataverse. Siiski saate kasutada virtuaalset olemit projekti ostutellimuse ridade Dataverse kuvamiseks projektihalduri teabe jaoks. Projektiga seotud hankija arve kulu on integreeritud olemiga Projekti tegelikud kulud.Dataverse Projekti kulu salvestatakse alammoodulis Projekt, kasutades töölehte Project Operations Integration. | |

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Järgmises tabelis on kujutatud topeltkirjutusega kaardid, mida on muudetud või lisatud Project Operationsi 2022. aasta septembri väljaandes.

| Olemikaart | Värskendatud versioon | Kommentaarid |
| -------------- | ------------------- | ------------|
| Project Operationsi integreerimise tegelikud näitajad (msdyn_actuals) | 1.0.0.15 | See kaart toetab ressursipõhiste stsenaariumide puhul alltöövõtu tegelike hankijate töötlemist koos project operationsiga. |
| Project Operationsi integreerimise projekti tarnija arve ekspordist (msdyn_projectvendorinvoices) | 1.0.0.2 | See kaart toetab ressursipõhiste stsenaariumide puhul alltöövõtu tegelike hankijate töötlemist koos project operationsiga. |
| Project Operationsi integratsioon projekti tarnija arve rea ekspordist (msdyn_projectvendorinvoices) | 1.0.0.5 | See kaart toetab ressursipõhiste stsenaariumide puhul alltöövõtu tegelike hankijate töötlemist koos project operationsiga. |

Käivitage oma keskkonnas alati kaardi uusim versioon ja lubage project operationsi Dataverse lahenduse ja finance lahenduse versiooni värskendamisel kõik seotud tabelikaardid. Mõned funktsioonid ja võimalused ei pruugi õigesti töötada, kui kaardi uusim versioon pole aktiveeritud. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud valmis tabelikaarti, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib kaardi käivitamisel probleem, järgige juhiseid, mis on toodud [tõrkeotsingu juhendi Jaotises Puuduvad tabeli veerud kaardil](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2754422 | Materjali- ja kuluprognoosid ei liigu finantsidesse, kui projektid kopeeritakse.Dataverse |
| Aeg ja kulu | 2787409 | Mittekehtiv kinnitaja saab kinnitada projektivälise ajakirje. |
| Müügivõimaluse haldus | 2788907 | Värskendatud tõrketeade kordumatuse valideerimise kohta tellimusridade puhul, mis sisaldavad lippe. |
| Aeg ja kulu | 2842253 | Null erandi käsitlemine aja kinnitamiseks. |
| Arveldamine ja hinnakujundus | 2844181 | Korrelatsiooni ID mittesaamine blokeerib arve loomise. |
| Arveldamine ja hinnakujundus | 2876628 | QLD, CLD – hinnanguline hinnakirja lahendus peaks kasutama hinnakirja varasema kuupäevavahemiku välju. |
| Allhanked | 2893222 | Kui allhankeliinile ei ole rolli määratud, peaks olema võimalik valida see rida meeskonnaliikmel mis tahes rolli jaoks. |

### <a name="project-management-and-accounting-in-finance"></a>Projektijuhtimine ja raamatupidamine rahanduses

Selles värskenduses sisalduvate veaparanduste kohta teabe saamiseks logige sisse teenusesse Microsoft Dynamics Lifecycle Services ja vaadake [teabebaasi artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funktsioonid, mis on eelseisvas väljalaskes vaikimisi sisse lülitatud

Järgmises tabelis on loetletud funktsioonid, mis on versioonis 10.0.30 vaikimisi sisse lülitatud. Enamikku automaatselt sisse lülitatud funktsioone saab funktsioonihalduses [välja](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) lülitada. Tulevikus võidakse mõned automaatselt sisse lülitatud funktsioonid funktsioonihaldusest eemaldada ja muutuda kohustuslikuks. See muudatus tagab, et kliendid kasutavad praeguseid funktsioone, nii et täiustused saavad nende lisamisel tugineda praegusele funktsioonile. Funktsioone ei lubata automaatselt vähem kui ühe aasta jooksul, välja arvatud juhul, kui on kindlaks tehtud, et need on hädavajalikud.

| Funktsiooni nimi | Luba kuupäev | Funktsioon on lisatud | Funktsiooni olek | Moodul |
| --- | --- | --- |--- |--- |
| Asünkroonimistoimingu lubamine, kui kasutaja peab vaheldumisi aktiveerima sünkroonimis- ja asünkroonimistoiminguid | 21. oktoober 2022 | 9. aprill 2021 | Vaikimisi sees | Kuluhaldus |
| Vajalike laekumiste kulupoliitika hindamine | 21. oktoober 2022 | 20. detsember 2021 | Vaikimisi sees | Kuluhaldus |
| Töötajate delegeerimisel loodud kuluaruannete loendivaade | 21. oktoober 2022 | 19. veebruar 2020 | Vaikimisi sees | Kuluhaldus |
| Läbisõidu summaarne arvutamine finantsaasta järgi | 21. oktoober 2022 | 10. mai 2022 | Vaikimisi sees | Kuluhaldus |
