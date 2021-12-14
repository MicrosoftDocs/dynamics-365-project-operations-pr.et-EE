---
title: Projekti plaanimise logid
description: See teema pakub teavet ja näidiseid, mis aitavad teil kasutada projekti planeerimise logisid projekti plaanimisteenuse ja projekti planeerimise API-dega seotud tõrgete jälgimiseks.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1c5632a880fa30d1b863c326b22e3d930c9564dc
ms.sourcegitcommit: 844ec8eacd0fc10d1659b437cc5cbb4480ec9e1e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/01/2021
ms.locfileid: "7877508"
---
# <a name="project-scheduling-logs"></a>Projekti plaanimise logid

_**Kehtib:** Ressursi/ladustamata stsenaariumide projektitoimingud, Lite'i juurutamine – tehing proforma arvetega_, _Veebiprojekt_

Microsoft Dynamics 365 Project Operations kasutab [project for the](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) Webi peamise plaanimismootorina. Selle asemel, et kasutada standardseid Microsoft Dataverse veebirakenduste programmeerimisliidesed (API-d), kasutab Project Operations uusi projekti planeerimise API-sid projektiülesannete, ressursimääramiste, ülesannete sõltuvuste, projektiämbrite ja projektimeeskondade liikmete loomiseks, värskendamiseks ja kustutamiseks. Kui aga tööjaotusstruktuuri (WBS) olemite loomisel, värskendamisel või kustutamisel töötatakse programmiliselt, võib esineda tõrkeid. Nende tõrgete ja toimingute ajaloo jälgimiseks on rakendatud kaks uut halduslogi: **operatsioonikomplekt** ja projekti **plaanimisteenus (PSS).** Nendele logidele juurdepääsemiseks minge **jaotisse Sätete** \> **ajakava integreerimine**.

Järgmisel joonisel on näidatud projekti plaanimise logide andmemudel.

![Projekti plaanimise logide andmemudel.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Toimingukomplekti logi

Logi Toimingu seadmine jälgib operatsioonikomplekti käivitamist, mida kasutatakse ühe või mitme projektiprojekti projektimeeskonna liikmega seotud toimingute loomiseks, värskendamiseks või kustutamiseks partiis. **Väli Operatsioon olekus näitab** toimingukomplekti üldist olekut. Toimingukomplekti kandevõime üksikasjad on jäädvustatud seostuvates toimingukomplekti üksikasjade kirjetes.

### <a name="operation-set"></a>Toimingukomplekt

Järgmises tabelis kuvatakse väljad, mis on seotud **olemiGa** Toimingukomplekt.

| SchemaName            | Kirjeldus                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Kuupäev/kellaaeg, millal toimingukomplekt lõpetati või nurjus.                                                | CompletedOn            |
| msdyn_correlationid   | Taotluse **väärtus** correlationId.                                                                  | CorrelationId          |
| msdyn_description     | Operatsioonikomplekti kirjeldus.                                                                        | Kirjeldus            |
| msdyn_executedon      | Kirje käivitamise kuupäev/kellaaeg.                                                                       | Täideviimise kuupäev            |
| msdyn_operationsetId  | Olemi eksemplaride ainuidentifikaator.                                                                   | OperationSet           |
| msdyn_Project         | Projektiga seotud projekt.                                                            | Project                |
| msdyn_projectid       | Taotluse **projectId** väärtus.                                                                      | ProjectId (aegunud) |
| msdyn_projectName     | Pole rakendatav.                                                                                              | Pole rakendatav         |
| msdyn_PSSErrorLog     | Toimingukomplektiga seotud projekti plaanimisteenuse tõrkelogi ainuidentifikaator. | PSS-i tõrkelogi          |
| msdyn_PSSErrorLogName | Pole rakendatav.                                                                                              | Pole rakendatav         |
| msdyn_status          | Toimingukomplekti olek.                                                                             | Olek                 |
| msdyn_statusName      | Pole rakendatav.                                                                                              | Pole rakendatav         |
| msdyn_useraadid       | Selle kasutaja Azure Active Directory (Azure AD) objekti ID, kuhu taotlus kuulub.                     | UserAADID              |

### <a name="operation-set-detail"></a>Toimingukomplekti üksikasjad

Järgmises tabelis kuvatakse väljad, mis on seotud **olemiGa Toimingu seadmine** Üksikasjad.

| SchemaName                 | Kirjeldus                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Päringu seerianumbrid Dataverse väljad.                                            | CdsPayload            |
| msdyn_entityname           | Päringu olemi nimi.                                                     | EntityName            |
| msdyn_httpverb             | Taotluse meetod.                                                                         | HTTPVerb (iganenud) |
| msdyn_httpverbName         | Pole rakendatav.                                                                             | Pole rakendatav        |
| msdyn_operationset         | Kirjesse kuuluva toimingukomplekti ainuidentifikaator.                      | OperationSet          |
| msdyn_operationsetdetailId | Olemi eksemplaride ainuidentifikaator.                                                  | OperationSeti üksikasi   |
| msdyn_operationsetName     | Pole rakendatav.                                                                             | Pole rakendatav        |
| msdyn_operationtype        | Operatsioonikomplekti üksikasjad.                                             | Toimingu tüüp         |
| msdyn_operationtypeName    | Pole rakendatav.                                                                             | Pole rakendatav        |
| msdyn_psspayload           | Taotluse väljad järjestatud projektiplaneerimise hooldus.                           | PssPayload            |
| msdyn_recordid             | Päringukirje ID.                                                       | Kirje ID             |
| msdyn_requestnumber        | Automaatselt loodud number, mis tuvastab taotluste vastuvõtmise järjekorra. | Taotluse number        |

## <a name="project-scheduling-service-error-logs"></a>Projekti plaanimisteenuse tõrkelogid

Projekti plaanimisteenuse tõrge logib hõivamistõrked, mis ilmnevad siis, kui projekti plaanimisteenus proovib **toimingut Salvesta** või **Ava**. Nende logide loomise kohta on kolm toetatud stsenaariumi.

- Kasutaja algatatud toimingud nurjuvad kriitiliselt (näiteks määramist ei saa puuduvate õiguste tõttu luua).
- Projekti plaanimisteenus ei saa olemile programmiliselt luua, värskendada, kustutada ega teha muid kaskaadtoiminguid.
- Kasutajal esineb tõrkeid, kui kirje ei avane (nt projekti avamisel või meeskonnaliikme teabe värskendamisel).

### <a name="project-scheduling-service-log"></a>Projekti plaanimisteenuse logi

Järgmises tabelis kuvatakse väljad, mis sisalduvad projekti plaanimisteenuse logis.

| SchemaName          | Kirjeldus                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Erandi kutsevirn.                                               | Kutsevirn     |
| msdyn_correlationid | Vea korrelatsiooni ID.                                               | CorrelationId  |
| msdyn_errorcode     | Väli, mida kasutatakse Dataverse tõrkekoodi või HTTP tõrkekoodi talletamiseks. | Tõrkekood     |
| msdyn_HelpLink      | Link avaliku spikri dokumentatsioonile.                                       | Spikri link      |
| msdyn_log           | Projekti plaanimisteenuse logi.                                   | Logi            |
| msdyn_project       | Vealogiga seotud projekt.                             | Project        |
| msdyn_projectName   | Projekti nimi, kui toimingukomplekti kandevõime säilib. | Pole rakendatav |
| msdyn_psserrorlogId | Olemi eksemplaride ainuidentifikaator.                                     | PSS-i tõrkelogi  |
| msdyn_SessionId     | Projekti seansi ID.                                                        | Seansi ID     |

## <a name="error-log-cleanup"></a>Tõrkelogi puhastamine

Vaikimisi saab nii projektiplaneerimise teenuse tõrkelogisid kui ka operatsioonikomplekti logi puhastada iga 90 päeva järel. Kõik kirjed, mis on vanemad kui 90 päeva, kustutatakse. Kuid muutes **msdyn_StateOperationSetAge lehe Projekti** **parameetrid** väärtust, saavad administraatorid koristusvahemikku reguleerida nii, et see oleks 1 kuni 120 päeva. Selle väärtuse muutmiseks on saadaval mitu meetodit.

- Kohandage **olemit** Projektiparameeter, luues kohandatud lehe ja lisades välja **Aegunud toimingute määra** vanus.
- Kasutage kliendikoodi, mis kasutab [WebApi tarkvaraarenduskomplekti (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Kasutage teenuse SDK-koodi, mis kasutab **mudelipõhistes rakendustes Xrm SDK updateRecord** meetodit (kliendi API viide). Power Apps sisaldab värskendusrekordi meetodi kirjeldust ja toetatud **parameetreid**.

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
