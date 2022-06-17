---
title: Projekti plaanimise logid
description: Selles artiklis antakse teavet ja näidiseid, mis aitavad teil kasutada projekti plaanimise logisid projekti plaanimise teenuse ja projekti plaanimise API-dega seotud tõrgete jälgimiseks.
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

_**Kehtib:** Projektitoimingud ressursi/ladustamata põhistsenaariumide puhul, Lite juurutamine - arveldamine proforma arvetega_, _Project for the Web_

Microsoft Dynamics 365 Project Operations kasutab [Project for the Webi](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) oma peamise plaanimismootorina. Selle asemel, et kasutada standardseid Microsoft Dataverse veebirakenduste programmeerimisliideseid( API-sid), kasutab Project Operations uusi projekti plaanimise API-sid projektiülesannete, ressursimääramiste, ülesandesõltuvuste, projektiämbrite ja projektimeeskondade liikmete loomiseks, värskendamiseks ja kustutamiseks. Kui aga luuakse, värskendatakse või kustutatakse toiminguid programmiliselt tööjaotuse struktuuri (WBS) olemites, võivad ilmneda tõrked. Nende tõrgete ja toimingute ajaloo jälgimiseks on rakendatud kaks uut halduslogi: **operatsioonide komplekt** ja **projekti planeerimise teenus (PSS)**. Nendele logidele juurdepääsemiseks minge jaotisse **Seadete** \> **ajakava integreerimine.**

Järgmisel joonisel on näidatud projektiplaneerimise logide andmemudel.

![Projekti plaanimise logide andmemudel.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Toimingu määra logi

Logi Toiming Set jälgib toimingukomplekti täitmist, mida kasutatakse projektide, projektiülesannete, ressursimäärangute, ülesandesõltuvuste, projektiämbrite või projektimeeskonna liikmete partii toimingute käitamiseks. Väli **Toiming olekus** näitab toimingukomplekti üldist olekut. Toimingukomplekti kasuliku koormuse üksikasjad jäädvustatakse seotud toimingukomplekti üksikasjade kirjetesse.

### <a name="operation-set"></a>Toimingu komplekt

Järgmises tabelis kuvatakse väljad, mis on seotud **olemiga Toimingukomplekt**.

| SchemaName            | Kirjeldus                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Kuupäev/kellaaeg, millal toimingukomplekt lõpetati või nurjus.                                                | CompletedOn            |
| msdyn_correlationid   | Taotluse **väärtus correlationId**.                                                                  | CorrelationId          |
| msdyn_description     | Toimingukomplekti kirjeldus.                                                                        | Kirjeldus            |
| msdyn_executedon      | Kirje esitamise kuupäev/kellaaeg.                                                                       | Käivituskuupäev            |
| msdyn_operationsetId  | Olemi eksemplaride ainuidentifikaator.                                                                   | OperationSet           |
| msdyn_Project         | Operatsioonikomplektiga seotud projekt.                                                            | Project                |
| msdyn_projectid       | Taotluse **väärtus ProjectId**.                                                                      | ProjectId (aegunud) |
| msdyn_projectName     | Pole rakendatav.                                                                                              | Pole rakendatav         |
| msdyn_PSSErrorLog     | Toimingukomplektiga seostatud tõrkelogi Project Scheduling Service ainuidentifikaator. | PSS-i tõrkelogi          |
| msdyn_PSSErrorLogName | Pole rakendatav.                                                                                              | Pole rakendatav         |
| msdyn_status          | Operatsioonikomplekti olek.                                                                             | Olek                 |
| msdyn_statusName      | Pole rakendatav.                                                                                              | Pole rakendatav         |
| msdyn_useraadid       | Selle Azure Active Directory kasutaja (Azure AD) objekti ID, kellele taotlus kuulub.                     | UserAADID              |

### <a name="operation-set-detail"></a>Toimingu määra detail

Järgmises tabelis kuvatakse väljad, mis on seotud **olemiga Toimingukomplekti üksikasjad**.

| SchemaName                 | Kirjeldus                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Taotluse seeriaviisilised Dataverse väljad.                                            | CdsPayload            |
| msdyn_entityname           | Taotluse olemi nimi.                                                     | EntityName            |
| msdyn_httpverb             | Taotlusmeetod.                                                                         | HTTPVerb (iganenud) |
| msdyn_httpverbName         | Pole rakendatav.                                                                             | Pole rakendatav        |
| msdyn_operationset         | Selle toimingukomplekti ainuidentifikaator, kuhu kirje kuulub.                      | OperationSet          |
| msdyn_operationsetdetailId | Olemi eksemplaride ainuidentifikaator.                                                  | OperationSeti üksikasi   |
| msdyn_operationsetName     | Pole rakendatav.                                                                             | Pole rakendatav        |
| msdyn_operationtype        | Toimingukomplekti detaili toimingu tüüp.                                             | Toimingu tüüp         |
| msdyn_operationtypeName    | Pole rakendatav.                                                                             | Pole rakendatav        |
| msdyn_psspayload           | Taotluse väljad Projekti plaanimisteenus on järjestatud.                           | PssPayload            |
| msdyn_recordid             | Päringukirje ID.                                                       | Kirje ID             |
| msdyn_requestnumber        | Automaatselt genereeritud number, mis tuvastab tellimuse, milles taotlused vastu võeti. | Taotluse number        |

## <a name="project-scheduling-service-error-logs"></a>Projekti plaanimisteenuse tõrkelogid

Tõrkelogid Projekti plaanimisteenuse logid jäädvustavad tõrkeid, mis ilmnevad, kui projekti plaanimisteenus proovib toimingut **Salvesta** või **Ava**. Nende logide loomisel on kolm toetatud stsenaariumi.

- Kasutaja algatatud toimingud nurjuvad kriitiliselt (nt määramist ei saa puuduvate õiguste tõttu luua).
- Projekti plaanimisteenus ei saa olemil programmiliselt luua, värskendada, kustutada ega teha muid kaskaadtoiminguid.
- Kasutajal ilmneb tõrkeid, kui kirjet ei avata (nt kui projekt avatakse või meeskonnaliikme teavet värskendatakse).

### <a name="project-scheduling-service-log"></a>Projekti plaanimisteenuse logi

Järgmises tabelis kuvatakse väljad, mis on kaasatud logisse Projekti plaanimisteenus.

| SchemaName          | Kirjeldus                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Erandi kutsevirn.                                               | Kutsevirn     |
| msdyn_correlationid | Vea korrelatsiooni ID.                                               | CorrelationId  |
| msdyn_errorcode     | Väli, mida kasutatakse tõrketähise Dataverse või HTTP-tõrkekoodi talletamiseks. | Tõrkekood     |
| msdyn_HelpLink      | Link avalikule spikridokumentatsioonile.                                       | Spikri link      |
| msdyn_log           | Projekti planeerimise teenuse logi.                                   | Logi            |
| msdyn_project       | Tõrkelogiga seostatud projekt.                             | Project        |
| msdyn_projectName   | Projekti nimi, kui toimingukomplekti kandevõime säilib. | Pole rakendatav |
| msdyn_psserrorlogId | Olemi eksemplaride ainuidentifikaator.                                     | PSS-i tõrkelogi  |
| msdyn_SessionId     | Projekti seansi ID.                                                        | Seansi ID     |

## <a name="error-log-cleanup"></a>Tõrkelogi puhastamine

Vaikimisi saab iga 90 päeva järel puhastada nii Project Scheduling Service'i tõrkelogisid kui ka toimingukomplekti logi. Kõik kirjed, mis on vanemad kui 90 päeva, kustutatakse. Kuid muutes lehe Projekti parameetrid **välja** msdyn_StateOperationSetAge **väärtust**, saavad administraatorid puhastusvahemikku reguleerida nii, et see oleks vahemikus 1 kuni 120 päeva. Selle väärtuse muutmiseks on saadaval mitu meetodit.

- Olemi **Projektiparameeter** kohandamiseks looge kohandatud leht ja lisage **väli Aegunud toimingute määra vanus**.
- Kasutage kliendikoodi, mis kasutab [WebApi tarkvaraarenduskomplekti (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Kasutage teenuse SDK koodi, mis kasutab mudelipõhistes rakendustes Xrm SDK **updateRecord** meetodit (Kliendi API viide). Power Apps sisaldab meetodi updateRecord **kirjeldust** ja toetatud parameetreid.

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
