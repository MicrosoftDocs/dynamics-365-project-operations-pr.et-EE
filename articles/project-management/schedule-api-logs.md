---
title: Projekti plaanimise logid
description: See artikkel annab teavet ja näidiseid, mis aitavad teil projekti ajastamise logisid kasutada projekti ajastamise teenuse ja projekti ajastamise API-dega seotud tõrgete jälgimiseks.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923690"
---
# <a name="project-scheduling-logs"></a>Projekti plaanimise logid

_**Kehtiv järgnevale:** Project Operations ressursi-/mitteressursipõhised stsenaariumid, lihtjuurutus – tehing näidisarveldusele_, _Project for the Web_

Microsoft Dynamics 365 Project Operations kasutab [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) esmase ajastamismootorina. Standardse Microsoft Dataverse veebirakenduse programmeerimisliideste (API-de) asemel kasutab Project Operations projektiülesannete, ressursimäärangute, ülesannete sõltuvuste, projektisalvede ja projektimeeskondade liikmete loomiseks, värskendamiseks ja kustutamiseks uusi Projekti ajastamise API-sid. Kui loomis-, värskendamis- või kustutamistoiminguid käivitatakse programmiliselt tööjaotuse struktuuri (WBS) üksustel, võivad ilmneda vead. Nende vigade ja toimingute ajaloo jälgimiseks on juurutatud kaks uut halduslogi: **Toimingukomplekt** ja **Projekti ajastamisteenus (PSS)**. Nendele logidele juurde pääsemiseks minge jaotisse **Sätted** \> **Ajakava integreerimine**.

Järgmisel joonisel on kujutatud projekti ajastamise logide andmemudel.

![Projekti ajastamise logide andmemudel.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Toimingukomplekti logi

Toimingukomplekti logi jälgib toimingukomplekti täitmist, mida kasutatakse ühe või mitme projekti, projektiülesannete, ressursside määramise, ülesannete sõltuvuste, projektisalvede või projektimeeskonna liikmete partii loomise, värskendamise või kustutamise toimingu käivitamiseks. Väli **Toiming olekus** näitab toimingukomplekti üldist olekut. Toimingukomplekti kasuliku koormuse üksikasjad on salvestatud seotud toimingukomplekti üksikasjade kirjetesse.

### <a name="operation-set"></a>Toimingukomplekt

Järgmises tabelis on näidatud väljad, mis on seotud olemiga **Toimingukomplekt**.

| Skeemi nimi            | Kirjeldus                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Kuupäev/kellaaeg, millal toimingukomplekt lõpetati või ebaõnnestus.                                                | CompletedOn            |
| msdyn_correlationid   | Taotluse **correlationId** väärtus.                                                                  | CorrelationId          |
| msdyn_description     | Toimingukomplekti kirjeldus.                                                                        | Kirjeldus            |
| msdyn_executedon      | Kirje käivitamise kuupäev/kellaaeg.                                                                       | Käivituskuupäev            |
| msdyn_operationsetId  | Olemi eksemplaride ainuidentifikaator.                                                                   | OperationSet           |
| msdyn_Project         | Toimingukomplektiga seotud projekt.                                                            | Project                |
| msdyn_projectid       | Päringu **projectId** väärtus.                                                                      | ProjectId (aegunud) |
| msdyn_projectName     | Pole rakendatav.                                                                                              | Pole rakendatav         |
| msdyn_PSSErrorLog     | Projekti ajastamisteenuse tõrkelogi ainuidentifikaator, mis on seotud toimingukomplektiga. | PSS-i tõrkelogi          |
| msdyn_PSSErrorLogName | Pole rakendatav.                                                                                              | Pole rakendatav         |
| msdyn_status          | Toimingukomplekti olek.                                                                             | Olek                 |
| msdyn_statusName      | Pole rakendatav.                                                                                              | Pole rakendatav         |
| msdyn_useraadid       | Azure Active Directory (Azure AD) objekti ID, kellele taotlus kuulub.                     | UserAADID              |

### <a name="operation-set-detail"></a>Toimingukomplekti üksikasi

Järgmises tabelis on näidatud väljad, mis on seotud olemiga **Toimingukomplekti üksikasi**.

| Skeemi nimi                 | Kirjeldus                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serialiseeritud Dataverse-i väljad taotluse jaoks.                                            | CdsPayload            |
| msdyn_entityname           | Olemi nimi selle taotluse jaoks.                                                     | EntityName            |
| msdyn_httpverb             | Taotluse meetod.                                                                         | HTTPVerb (iganenud) |
| msdyn_httpverbName         | Pole rakendatav.                                                                             | Pole rakendatav        |
| msdyn_operationset         | Selle toimingukomplekti ainuidentifikaator, kuhu see kirje kuulub.                      | OperationSet          |
| msdyn_operationsetdetailId | Olemi eksemplaride ainuidentifikaator.                                                  | OperationSeti üksikasi   |
| msdyn_operationsetName     | Pole rakendatav.                                                                             | Pole rakendatav        |
| msdyn_operationtype        | Toimingukomplekti üksikasja toimingu tüüp.                                             | Toimingu tüüp         |
| msdyn_operationtypeName    | Pole rakendatav.                                                                             | Pole rakendatav        |
| msdyn_psspayload           | Taotluse serialiseeritud projekti ajastamisteenuse väljad.                           | PssPayload            |
| msdyn_recordid             | Taotluse kirje identifikaator.                                                       | Kirje ID             |
| msdyn_requestnumber        | Automaatselt genereeritud number, mis tuvastab taotluste vastuvõtmise järjekorra. | Taotluse number        |

## <a name="project-scheduling-service-error-logs"></a>Projekti ajastamisteenuse tõrkelogid

Projekti ajastamisteenuse tõrkelogid salvestavad tõrked, mis ilmnevad siis, kui projekti ajastamisteenus proovib toimingut **Salvesta** või **Ava**. Nende logide loomisel on kolm toetatud stsenaariumi.

- Kasutaja algatatud toimingud ebaõnnestuvad kriitiliselt (näiteks ei saa puuduvate õiguste tõttu ülesannet luua).
- Projekti ajastamisteenus ei saa olemiga programmiliselt luua, värskendada, kustutada ega teha muid kaskaadtoiminguid.
- Kui kirje avamine ebaõnnestub (näiteks projekti avamisel või meeskonnaliikme teabe värskendamisel), kogeb kasutaja tõrkeid.

### <a name="project-scheduling-service-log"></a>Projekti ajastamisteenuse logi

Järgmises tabelis on näidatud väljad, mis sisalduvad projekti ajastamisteenuse logis.

| Skeemi nimi          | Kirjeldus                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Erandi kutsevirn.                                               | Kutsevirn     |
| msdyn_correlationid | Tõrke korrelatsiooni ID.                                               | CorrelationId  |
| msdyn_errorcode     | Väli, mida kasutatakse Dataverse’i tõrkekoodi või HTTP tõrkekoodi salvestamiseks. | Tõrkekood     |
| msdyn_HelpLink      | Link avalikule Spikri dokumentatsioonile.                                       | Spikri link      |
| msdyn_log           | Logi projekti ajastamisteenusest.                                   | Logi            |
| msdyn_project       | Projekt, mis on seotud tõrkelogiga.                             | Project        |
| msdyn_projectName   | Projekti nimi, kui toimingukomplekti kasulik koormus säilib. | Pole rakendatav |
| msdyn_psserrorlogId | Olemi eksemplaride ainuidentifikaator.                                     | PSS-i tõrkelogi  |
| msdyn_SessionId     | Projekti seansi ID.                                                        | Seansi ID     |

## <a name="error-log-cleanup"></a>Tõrkelogi puhastamine

Vaikimisi saab nii projekti ajastamisteenuse tõrkelogi kui ka toimingukomplekti logi puhastada iga 90 päeva järel. Kõik kirjed, mis on vanemad kui 90 päeva, kustutatakse. Kuid muutes välja **msdyn_StateOperationSetAge** lehel **Projekti parameetrid** väärtust, saavad administraatorid reguleerida puhastusvahemikku nii, et see jääb vahemikku 1–120 päeva. Selle väärtuse muutmiseks on saadaval mitu meetodit.

- Kohandage olemit **Projekti parameeter** luues kohandatud lehe ja lisades välja **Aegunud toimingukomplekti vanus**.
- Kasutage kliendikoodi, mis kasutab [WebApi tarkvaraarenduskomplekti (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Kasutage mudelipõhistes rakendustes teenuse SDK koodi, mis kasutab meetodit Xrm SDK **updateRecord** (kliendi API viide). Power Apps sisaldab meetodi **updateRecord** kirjeldust ja toetatud parameetreid.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
