---
title: Kohandatud olemite uute vormide lisamine (Project Service Automation 2.x)
description: Selles teemas kirjeldatakse, kuidas rakenduses Dynamics 365 Project Service Automation 2.x müügivõimalustele, hinnapakkumistele, tellimustele või arvetele kohandatud olemi vorme lisada.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 31986efed81892cc5722cb8f5e292cde14d8843d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144588"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Kohandatud olemite uute vormide lisamine (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Välja tüüp 

Dynamics 365 Project Service Automation põhineb väljal **Tüüp** (**msdyn\_ordertype**) üksustes Müügivõimalus, Hinnapakkumine, Tellimus ja Arveldamine, et eristada nende olemite **tööpõhiseid** versioone **üksusepõhistest** ja **teenusepõhistest**. Nende olemite tööpõhiseid versioone käsitletakse PSA-s. Suur osa kliendi- ja serveripoolse lahenduse äriloogikast oleneb välja **Tüüp** väärtusest. Seetõttu on oluline, et väli lähtestatakse olemite loomisel õigete väärtusega. Vale väärtus võib põhjustada valet käitumist ja mõni äriloogika ei pruugi õigesti töötada.

## <a name="automatic-form-switching"></a>Automaatne vormi vahetamine

Üksuse kirjete valest lähtestamisest ja muutmisest põhjustatud võimaliku andmete rikkumise ja ootamatu käitumise vältimiseks on PSA kasutusvalmise vormides nüüd ka automaatseks vormiks ümberlülitamise loogika. See loogika viib kasutajad õigele vormile, et töötada tööpõhise versiooniga või mis tahes muud tüüpi müügivõimaluse, hinnapakkumise, tellimuse või arve üksusega. Kui kasutaja avab müügivõimaluse, hinnapakkumise, tellimuse või arve üksuse tööpõhise versiooni, lülitutakse vormile **Projekti teave**.

Automaatne vormilülituse loogika oleneb välja **formId** ja **msdyn\_ordertype** väärtuste vastendamisest. Kõik kasutusvalmis vormid on lisatud sellesse vastendamisse. Kohandatud vorme tuleb siiski käsitsi lisada, et näidata, millist olemi versiooni need käsitlema peaks. See põhineb väljal **msdyn\_ordertype**. Kui vormi ümberlülitamisel vastendust ei teki, lülitub loogika kasutusvalmis vormile, mis põhineb olemi **msdyn\_ordertype** väljal salvestatud väärtusel.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Kohandatud vormide lisamine ja vormilülituse loogika sisselülitamine

Järgmises näites kirjeldatakse, kuidas lisada kohandatud vormi ja vormi **Projekti teave**, nii et see töötaks tööpõhiste võimalustega. Sama protsessi kasutatakse kohandatud vormide lisamisel, nii et need töötavaks hinnapakkumiste, tellimuste ja arvetega.

Vormi **Projekti teave** kohandatud versiooni loomiseks toimige järgmiselt.

1. Avage müügivõimaluse üksuses vormi **Projekti teave** ja salvestage koopia nimega **Minu projekti teave**.
2. Avage uus vorm ja veenduge seejärel atribuutides, et vormil **Projekti teave** oleks olemas vormi käivitamise skriptid. 

    > [!IMPORTANT]
    > Ärge eemaldage skripte. Muidu võidakse teatud andmed valesti lähtestada.

3. Veenduge, et vormil oleks väli **Tüüp** (**msdyn\_ordertype**). 

    > [!IMPORTANT]
    > Ärge eemaldage seda välja. Muidu ei hakka lähtestamise skriptid tööle.

4. Leidke uue vormi väärtus **formId**. Nende sammude läbimiseks on kaks võimalust.

    - Eksportige vorm **Minu projekti teave** mittehallatava lahenduse osana ja leidke seejärel kohandatud XML-failist eksporditud lahenduse väärtus **formId**.
    - Avage redigeerija vormilt vorm **Minu projekti teave** ja leidke URL-i parameetri **fromId** kõrvalt globaalne kordumatu identifikaator (GUID), nagu on näidatud järgmisel illustratsioonil.

    ![Uue vormi formId-väärtuse otsimine URL-ilt](media/how-to-add-custom-forms-in-v2.0.png)

5. Looge vastendus **msdyn\_ordertype** väärtuse **formId** jaoks, redigeerides veebiressursse msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Eemaldage ressursist kood ja asendage see järgmise koodiga.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Salvestage kohandus ja seejärel avaldage see.
