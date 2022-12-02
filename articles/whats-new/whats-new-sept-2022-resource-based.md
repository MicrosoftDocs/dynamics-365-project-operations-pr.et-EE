---
title: Mis on uut septembris 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: See artikkel annab teavet kvaliteedivärskenduste kohta, mis on saadaval rakenduse Microsoft Dynamics 365 Project Operations 2022. aasta septembri väljalaskes ressursi-/mittelaopõhiste stsenaariumide jaoks.
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

See artikkel kehtib rakenduse Microsoft Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Rakenduse Project Operations Dataverse keskkonna versioonis 4.46.0.60
- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.29

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

| Funktsiooni ala | Funktsiooni nimi | Lisateave |
| --- | --- | --- |
| Müügivõimaluse haldus | **Hinnapakkumiste läbivaatamine ja aktiveerimine**<br>Project Operations pakub müügiprotsessile täielikku tuge. Projekti hinnapakkumisi saab aktiveerida, et esindada olekut, kus hinnapakkumine on kirjutuskaitstud ja seda vaadatakse üle. Aktiveeritud hinnapakkumisi saab üle vaadata, et luua uusi hinnapakkumisi, millel on suurendatud revisjoni number. Aktiveeritud projekti hinnapakkumised või hinnapakkumise versioonid saab sulgeda võidetud või kaotatud kujul. | [Projekti hinnapakkumise aktiveerimine ja kontrollimine](/dynamics365/project-operations/sales/activation-and-revision) |
| Arveldamine ja hinnakujundus | **Ajavööndi agnostiline hind ei tööta**<br>Project Operations on võtnud kasutusele ajavööndi agnostilise kuupäeva kontseptsiooni kõigi projekti tegelike näitajate puhul. Uus väli **Tehingu kuupäev** on nüüd saadaval töölehele kandmistel ja tegelikel näitajatel ning seda kasutatakse tehingu toimumise kuupäeva salvestamiseks, kuid ilma seda kuupäeva koordineeritud universaalajaks teisendamata. Seda kuupäeva kasutatakse järgnevate protsesside jaoks, nagu hinna rikkumine ja arvete koostamine. | <p>[Määrake projektipõhiste prognooside ja tegelike näitajate kulumäärad](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Projektipõhiste prognooside ja tegelike näitajate müügihinna määratlemine](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Arveldamine ja hinnakujundus | **Kuupäeva kehtivad hinnad alistatakse rakenduses Project Operations**<br>Kuupäeva kehtiva hinna tühistamised pakuvad võimalust hinnakirjas konkreetseid hindu tühistada või muuta. | [Kuupäeva kehtiva hinna tühistamised](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Allhankeleping | **Alltöövõtt ja hankija arvete vastavus**<br>See funktsioon võimaldab klientidel sõlmida allhankelepinguid ressursiaja, kulukategooriate ja materjalide ostmiseks, mida projektitööks kasutatakse. Samuti võimaldab see klientidel salvestada finants- ja äritoiminguste rakenduses hankijate arveid, mis on teenuses Dataverse projektijuhtidele kontrollimiseks kättesaadavad. | <p>[Allhankelepingu haldus](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Hankija arvete koostamine](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Aeg ja kulu | **Globaalne kinnitaja**<br>See funktsioon võimaldab sõltumatut tarkvara hankijat (ISV) ja tsentraliseeritud kinnitust, olenemata projekti või meeskonnaliikme staatusest projektis. | [Turve ja kinnitused](/dynamics365/project-operations/approvals/approvals-security) |
| Kuluhaldus | **Võimalus postitada kulukohustust hankija valuutas**<br>See funktsioon võimaldab kuluaruandeid postitada sularahamakseviisi hankija valuutas. | [Võimalus postitada kulukohustust hankija valuutas](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projekti hanked | **Makske hankija maksete tasumisel**<br>See funktsioon võimaldab funktsiooni makske maksete tasumise korral (PWP) kasutada rakenduse Project Operations mittelaopõhistes keskkondades. See võimaldab hankija makseid säilitustingimuste alusel blokeerida/säilitada kuni kliendilt makse laekumiseni. | [Makske hankija maksete tasumisel](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projekti hanked | **Projekti ostutaotlused**<br>See funktsioon võimaldab kasutajatel luua projektiga seotud ostutellimusi juriidilistes isikutes, kus rakendus Project Operations on Dynamics 365 Customer Engagementi integratsioon on lubatud. Projekti ostutellimusi saab hankeosakonna isik kasutada mittelaopõhiste materjalihanke kajastamiseks projekti suhtes. Projekti ostutellimusi ei sünkroonita teenusega Dataverse. Siiski saate projektijuhi teabe saamiseks kasutada virtuaalset olemit teenuses Dataverse projekti ostutellimuste ridade kuvamiseks. Projektiga seotud hankija arve maksumus on teenuses Dataverse integreeritud projekti tegelike näitajate olemiga. Projekti maksumus kirjendatakse projekti alammoodulisse, kasutades rakenduse Project Operations integratsiooni töölehte. | |
|Projekti plaanimine ja jälgimine|**Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks** </br> </br>Ressursi määramise kontuuride redigeerimise API võimaldab arendajatel programmiliselt määrata ülesande määraja jõupingutusi mis tahes toetatud kuupäevavahemikus, et ajaliselt etapiviisilisemalt planeerida.|[Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Järgmises tabelis on esitatud topeltkirjutuskaardid, mida on muudetud või lisatud rakendusele Project Operations 2022. aasta septembri väljaandes.

| Olemikaart | Värskendatud versioon | Kommentaarid |
| -------------- | ------------------- | ------------|
| Project Operationsi integreerimise tegelikud näitajad (msdyn_actuals) | 1.0.0.15 | See kaart toetab ressursipõhiste stsenaariumide jaoks alltöövõtu tegelike näitajate töötlemist rakendusega Project Operations. |
| Project Operationsi integreerimise projekti tarnija arve ekspordist (msdyn_projectvendorinvoices) | 1.0.0.2 | See kaart toetab ressursipõhiste stsenaariumide jaoks alltöövõtu tegelike näitajate töötlemist rakendusega Project Operations. |
| Project Operationsi integratsioon projekti tarnija arve rea ekspordist (msdyn_projectvendorinvoices) | 1.0.0.5 | See kaart toetab ressursipõhiste stsenaariumide jaoks alltöövõtu tegelike näitajate töötlemist rakendusega Project Operations. |

Käitage oma keskkonnas alati kaardi uusimat versiooni ja lubage kõik seotud tabelikaardid oma Project Operationsi lahenduse Dataverse ja Finance versiooni värskendamisel. Kui kaardi uusim versioon pole aktiveeritud, ei pruugi mõned funktsioonid ja võimalused õigesti töötada. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastivälise tabelikaardi, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib probleeme kaardi käivitamisel, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises [Probleem kaardilt puuduvate tabeli veergudega](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2754422 | Materjali- ja kuluprognoosid ei voola rahanduse rakendusse, kui projekte kopeeritakse rakendusse Dataverse. |
| Aeg ja kulu | 2787409 | Mittekehtiv kinnitaja võib kinnitada projektivälise ajakirje. |
| Müügivõimaluse haldus | 2788907 | Värskendatud tõrketeate lippe sisaldavate tellimuseridade unikaalsuse kinnitamise kohta. |
| Aeg ja kulu | 2842253 | Null-erandiga töötlemine aja kinnitamiseks. |
| Arveldamine ja hinnakujundus | 2844181 | Korrelatsiooni ID hankimise ebaõnnestumine blokeerib arve loomise. |
| Arveldamine ja hinnakujundus | 2876628 | QLD, CLD – prognoositava hinnakirja lahendus peaks kasutama hinnakirja pärandkuupäevavahemiku välju. |
| Allhankeleping | 2893222 | Kui allhankelepingurea jaoks pole rolli määratud, peaks olema võimalik seda rida meeskonnaliikmel iga rolli jaoks valida. |

### <a name="project-management-and-accounting-in-finance"></a>Projektihaldus ja raamatupidamine rahanduses

Lisateabe saamiseks tõrkeparanduste kohta, mis sisalduvad selles värskenduses, logige sisse teenusesse Microsoft Dynamics Lifecycle Services ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funktsioonid on tulevase versioonis vaikimisi sisse lülitatud

Järgmises tabelis on loetletud funktsioonid, mis on versioonis 10.0.30 vaikimisi sisse lülitatud. Enamiku automaatselt sisse lülitatud funktsioone saab sisse lülitada jaotises [Funktsioonihaldus](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Tulevikus võidakse mõned automaatselt sisse lülitatud funktsioonid funktsioonihaldusest eemaldada ja muutuda kohustuslikuks. See muudatus tagab, et kliendid kasutavad praegust funktsionaalsust, nii et täiustused saaksid nende lisamisel olemasolevatele funktsioonidele tugineda. Funktsioone ei lubata kunagi automaatselt vähem kui aasta pärast, välja arvatud juhul, kui need on hädavajalikud.

| Funktsiooni nimi | Lubamise kuupäev | Funktsioon lisatud | Funktsiooni olek | Moodul |
| --- | --- | --- |--- |--- |
| Lubage asünkroonimistoimingud, kui kasutajal on vaja sünkroonimise ja asünkroonimise vahe lümber lülituda | 21. oktoober 2022 | 9. aprill 2021 | Vaikimisi sees | Kuluhaldus |
| Vajalik on kviitungite kulupoliitika hindamine | 21. oktoober 2022 | 20. detsember 2021 | Vaikimisi sees | Kuluhaldus |
| Töötajate delegeerimisel loodud kuluaruannete loendivaade | 21. oktoober 2022 | 19. veebruar 2020 | Vaikimisi sees | Kuluhaldus |
| Läbisõidu kogusumma arvutamine finantsaasta järgi | 21. oktoober 2022 | 10. mai 2022 | Vaikimisi sees | Kuluhaldus |
