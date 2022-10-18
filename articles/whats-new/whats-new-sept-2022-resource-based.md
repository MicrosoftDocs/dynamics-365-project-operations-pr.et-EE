---
title: Mis on uut septembris 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: Sellest artiklist leiate teavet kvaliteedivärskenduste kohta, mis on saadaval Microsofti Dynamics 365 Project Operations 2022. aasta septembri väljaandes ressursipõhiste / varudeta stsenaariumide jaoks.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634800"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut septembris 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kehtib järgmiste Microsofti Dynamics 365 Project Operations komponentide ja versioonide kohta.

- Projekti toimingud keskkonnaversioonis Dataverse 4.46.0.60
- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonna versioonis 10.0.29

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

| Funktsiooni ala | Funktsiooni nimi | Lisateave |
| --- | --- | --- |
| Müügivõimaluse haldus | **Hinnapakkumiste läbivaatamine ja aktiveerimine**<br>Project Operations pakub müügiprotsessile täielikku tuge. Projekti hinnapakkumisi saab aktiveerida, et need esindaksid olekut, kus hinnapakkumine on kirjutuskaitstud ja seda vaadatakse üle. Aktiveeritud hinnapakkumisi saab muuta, et luua uusi hinnapakkumisi, millel on suurendatud paranduste arv. Aktiveeritud projekti hinnapakkumisi või hinnapakkumiste parandusi saab sulgeda võidetuna või kaotatuna. | [Projekti hinnapakkumise aktiveerimine ja kontrollimine](/dynamics365/project-operations/sales/activation-and-revision) |
| Arveldamine ja hinnakujundus | **Ajavööndi agnostiline hinna vaikimisi jätmine**<br>Project Operations on kasutusele võtnud ajavööndi agnostilise kuupäeva kontseptsiooni kõigil projekti tegelikel andmetel. Uus väli Kande **kuupäev** on nüüd saadaval töölehe ridadel ja tegelikes väärtustes ning seda kasutatakse kande toimumise kuupäeva salvestamiseks, kuid ilma seda kuupäeva kooskõlastatud maailmaajaks teisendamata. Seda kuupäeva kasutatakse järgmiste protsesside jaoks, nagu hinna vaikimisi jätmine ja arve loomine. | <p>[Projektipõhiste hinnangute ja tegelike kulude määrade määramine](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Projektipõhiste hinnangute ja tegelike näitajate müügihindade määramine](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Arveldamine ja hinnakujundus | **Kuupäevaga kehtivad hinnaalistamised Project Operationsis**<br>Kuupäeval kehtivad hinna alistamised annavad võimaluse hinnakirjas teatud hindu alistada või muuta. | [Kuupäeval kehtivad hinna alistamised](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Allhanked | **Allhange ja hankija arvete vastavusseviimine**<br>See funktsioon võimaldab klientidel luua allhankeid ressursi aja, kulukategooriate ja projektitööks kasutatavate materjalide ostmiseks. Samuti võimaldab see klientidel finance and operationsi rakendustes salvestada hankija arveid, mis on projektijuhtidele Dataverse kinnitamiseks saadaval. | <p>[Alltöövõtu haldamine](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Hankija arvete koostamine](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Aeg ja kulu | **Globaalne kinnitaja**<br>See funktsioon võimaldab sõltumatut tarkvaratarnijat (ISV) ja tsentraliseeritud kinnitust, olenemata projekti või meeskonnaliikme olekust projektis. | [Turve ja kinnitused](/dynamics365/project-operations/approvals/approvals-security) |
| Kuluhaldus | **Võimalus sisestada kulukohustis hankija valuutas**<br>See funktsioon võimaldab sisestada kuluaruandeid sularahamakse meetodi hankija valuutas. | [Võimalus sisestada kulukohustis hankija valuutas](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projekti hanked | **Maksa hankijamaksete tasumisel**<br>See funktsioon võimaldab funktsiooni Maksa siis, kui olete tasuline (PWP) kasutada Project Operationsi mitte-laokeskkondades. See võimaldab hankija makseid blokeerida/säilitada säilitustingimuste alusel seni, kuni makse on kliendilt laekunud. | [Maksa hankijamaksete tasumisel](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projekti hanked | **Projekti ostutaotlused**<br>See funktsioon võimaldab kasutajatel luua projektiga seotud ostutellimusi juriidilistes isikutes, kus on lubatud Project Operations Dynamics 365 Customer Engagement integreerimisel. Projekti ostutellimusi saab kasutada ladustamata materjalihangete kirjendamiseks projekti suhtes hankeosakonna persona järgi. Projekti ostutellimusi ei sünkroonita rakendusega Dataverse. Siiski saate kasutada virtuaalset olemit projekti ostutellimuse ridade Dataverse kuvamiseks projektijuhi teabe jaoks. Projektiga seotud hankija arve kulu integreeritakse olemiga Project Actuals in Dataverse. Projekti kulu salvestatakse projekti alammoodulisse, kasutades töölehte Project Operations Integratsioon. | |
|Projekti plaanimine ja jälgimine|**Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks** </br> </br>Ressursi määramise kontuuri redigeerimise API võimaldab arendajatel programmiliselt määrata ülesande määraja panuse mis tahes toetatud kuupäevavahemikus, et tagada üksikasjalikum ajaline jõupingutuste plaanimine.|[Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Järgmine tabel näitab kahe kirjutusega kaarte, mida on Project Operationsi 2022. aasta septembri väljaandes muudetud või lisatud.

| Olemikaart | Värskendatud versioon | Kommentaarid |
| -------------- | ------------------- | ------------|
| Project Operationsi integreerimise tegelikud näitajad (msdyn_actuals) | 1.0.0.15 | See vaste toetab ressursipõhiste stsenaariumide puhul alltöövõtu tegelike kulude töötlemist Project Operationsiga. |
| Project Operationsi integreerimise projekti tarnija arve ekspordist (msdyn_projectvendorinvoices) | 1.0.0.2 | See vaste toetab ressursipõhiste stsenaariumide puhul alltöövõtu tegelike kulude töötlemist Project Operationsiga. |
| Project Operationsi integratsioon projekti tarnija arve rea ekspordist (msdyn_projectvendorinvoices) | 1.0.0.5 | See vaste toetab ressursipõhiste stsenaariumide puhul alltöövõtu tegelike kulude töötlemist Project Operationsiga. |

Käivitage oma keskkonnas alati kaardi uusim versioon ja lubage Project Operationsi Dataverse lahenduse ja finantslahenduse versiooni värskendamisel kõik seotud tabelikaardid. Mõned funktsioonid ja võimalused ei pruugi õigesti töötada, kui kaardi uusim versioon pole aktiveeritud. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud valmistabeli kaarti, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib kaardi käivitamisel probleem, järgige juhiseid [, mis on toodud topeltkirjutamise tõrkeotsingu juhendi jaotises Puuduvad tabeliveerud probleemid kaartidel](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2754422 | Materjali- ja kuluprognoosid ei liigu rakendusse Finance, kui projektid kopeeritakse .Dataverse |
| Aeg ja kulu | 2787409 | Mittekehtiv kinnitaja saab kinnitada mitteprojekti ajakirje. |
| Müügivõimaluse haldus | 2788907 | Värskendatud on tõrketeade lippe sisaldavate tellimuseridade kordumatuse valideerimise kohta. |
| Aeg ja kulu | 2842253 | Nullerandi käsitlemine aja kinnitamiseks. |
| Arveldamine ja hinnakujundus | 2844181 | Korrelatsiooni ID mittesaamine blokeerib arve loomise. |
| Arveldamine ja hinnakujundus | 2876628 | QLD, CLD - hinnanguline hinnakirja eraldusvõime peaks kasutama hinnakirja pärandkuupäevavahemiku välju. |
| Allhanked | 2893222 | Kui allhankereale ei ole rolli määratud, peaks olema võimalik valida see rida meeskonnaliikmel mis tahes rolli jaoks. |

### <a name="project-management-and-accounting-in-finance"></a>Projektijuhtimine ja raamatupidamine rahanduses

Selles värskenduses sisalduvate veaparanduste kohta teabe saamiseks logige sisse teenusesse Microsoft Dynamics Lifecycle Services ja vaadake [teabebaasi artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funktsioonid on tulevases väljaandes vaikimisi sisse lülitatud

Järgmises tabelis on loetletud funktsioonid, mis on versioonis 10.0.30 vaikimisi sisse lülitatud. Enamikku automaatselt sisse lülitatud funktsioone saab funktsioonihalduses [välja lülitada](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Tulevikus võidakse mõned automaatselt sisse lülitatud funktsioonid funktsioonihaldusest eemaldada ja muutuda kohustuslikuks. See muudatus tagab, et kliendid kasutavad praegust funktsionaalsust, nii et täiustused saavad nende lisamisel tugineda praegusele funktsionaalsusele. Funktsioone ei lubata kunagi automaatselt vähem kui ühe aasta jooksul, välja arvatud juhul, kui leitakse, et need on hädavajalikud.

| Funktsiooni nimi | Luba kuupäev | Lisatud funktsioon | Funktsiooni olek | Moodul |
| --- | --- | --- |--- |--- |
| Asünkroonimistoimingu lubamine, kui kasutaja peab sünkroonimis- ja asünkroonimistoiminguid vaheldumisi aktiveerima | 21. oktoober 2022 | 9. aprill 2021 | Vaikimisi sisse lülitatud | Kuluhaldus |
| Vajalike laekumiste kulupoliitika hindamine | 21. oktoober 2022 | 20. detsember 2021 | Vaikimisi sisse lülitatud | Kuluhaldus |
| Töötajate delegeerimisel loodud kuluaruannete loendivaade | 21. oktoober 2022 | 19. veebruar 2020 | Vaikimisi sisse lülitatud | Kuluhaldus |
| Läbisõidu kogusumma arvutamine finantsaasta järgi | 21. oktoober 2022 | 10. mai 2022 | Vaikimisi sisse lülitatud | Kuluhaldus |
