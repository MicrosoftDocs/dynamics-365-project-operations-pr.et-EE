---
title: Kohandatud olemite uute vormide lisamine (Project Service Automation 2.x)
description: Selles teemas kirjeldatakse, kuidas rakenduses Dynamics 365 Project Service Automation 2.x müügivõimalustele, hinnapakkumistele, tellimustele või arvetele kohandatud olemi vorme lisada.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 400d817ee7cbae6f6da95db4286ad6c4d6ff349a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007991"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="a5143-103">Kohandatud olemite uute vormide lisamine (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="a5143-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="a5143-104">Välja tüüp</span><span class="sxs-lookup"><span data-stu-id="a5143-104">Type field</span></span> 

<span data-ttu-id="a5143-105">Dynamics 365 Project Service Automation põhineb väljal **Tüüp** (**msdyn\_ordertype**) üksustes Müügivõimalus, Hinnapakkumine, Tellimus ja Arveldamine, et eristada nende olemite **tööpõhiseid** versioone **üksusepõhistest** ja **teenusepõhistest**.</span><span class="sxs-lookup"><span data-stu-id="a5143-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="a5143-106">Nende olemite tööpõhiseid versioone käsitletakse PSA-s.</span><span class="sxs-lookup"><span data-stu-id="a5143-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="a5143-107">Suur osa kliendi- ja serveripoolse lahenduse äriloogikast oleneb välja **Tüüp** väärtusest.</span><span class="sxs-lookup"><span data-stu-id="a5143-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="a5143-108">Seetõttu on oluline, et väli lähtestatakse olemite loomisel õigete väärtusega.</span><span class="sxs-lookup"><span data-stu-id="a5143-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="a5143-109">Vale väärtus võib põhjustada valet käitumist ja mõni äriloogika ei pruugi õigesti töötada.</span><span class="sxs-lookup"><span data-stu-id="a5143-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="a5143-110">Automaatne vormi vahetamine</span><span class="sxs-lookup"><span data-stu-id="a5143-110">Automatic form switching</span></span>

<span data-ttu-id="a5143-111">Üksuse kirjete valest lähtestamisest ja muutmisest põhjustatud võimaliku andmete rikkumise ja ootamatu käitumise vältimiseks on PSA kasutusvalmise vormides nüüd ka automaatseks vormiks ümberlülitamise loogika.</span><span class="sxs-lookup"><span data-stu-id="a5143-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="a5143-112">See loogika viib kasutajad õigele vormile, et töötada tööpõhise versiooniga või mis tahes muud tüüpi müügivõimaluse, hinnapakkumise, tellimuse või arve üksusega.</span><span class="sxs-lookup"><span data-stu-id="a5143-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="a5143-113">Kui kasutaja avab müügivõimaluse, hinnapakkumise, tellimuse või arve üksuse tööpõhise versiooni, lülitutakse vormile **Projekti teave**.</span><span class="sxs-lookup"><span data-stu-id="a5143-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="a5143-114">Automaatne vormilülituse loogika oleneb välja **formId** ja **msdyn\_ordertype** väärtuste vastendamisest.</span><span class="sxs-lookup"><span data-stu-id="a5143-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="a5143-115">Kõik kasutusvalmis vormid on lisatud sellesse vastendamisse.</span><span class="sxs-lookup"><span data-stu-id="a5143-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="a5143-116">Kohandatud vorme tuleb siiski käsitsi lisada, et näidata, millist olemi versiooni need käsitlema peaks.</span><span class="sxs-lookup"><span data-stu-id="a5143-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="a5143-117">See põhineb väljal **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="a5143-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="a5143-118">Kui vormi ümberlülitamisel vastendust ei teki, lülitub loogika kasutusvalmis vormile, mis põhineb olemi **msdyn\_ordertype** väljal salvestatud väärtusel.</span><span class="sxs-lookup"><span data-stu-id="a5143-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="a5143-119">Kohandatud vormide lisamine ja vormilülituse loogika sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="a5143-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="a5143-120">Järgmises näites kirjeldatakse, kuidas lisada kohandatud vormi ja vormi **Projekti teave**, nii et see töötaks tööpõhiste võimalustega.</span><span class="sxs-lookup"><span data-stu-id="a5143-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="a5143-121">Sama protsessi kasutatakse kohandatud vormide lisamisel, nii et need töötavaks hinnapakkumiste, tellimuste ja arvetega.</span><span class="sxs-lookup"><span data-stu-id="a5143-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="a5143-122">Vormi **Projekti teave** kohandatud versiooni loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a5143-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="a5143-123">Avage müügivõimaluse üksuses vormi **Projekti teave** ja salvestage koopia nimega **Minu projekti teave**.</span><span class="sxs-lookup"><span data-stu-id="a5143-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="a5143-124">Avage uus vorm ja veenduge seejärel atribuutides, et vormil **Projekti teave** oleks olemas vormi käivitamise skriptid.</span><span class="sxs-lookup"><span data-stu-id="a5143-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="a5143-125">Ärge eemaldage skripte.</span><span class="sxs-lookup"><span data-stu-id="a5143-125">Don't remove the scripts.</span></span> <span data-ttu-id="a5143-126">Muidu võidakse teatud andmed valesti lähtestada.</span><span class="sxs-lookup"><span data-stu-id="a5143-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="a5143-127">Veenduge, et vormil oleks väli **Tüüp** (**msdyn\_ordertype**).</span><span class="sxs-lookup"><span data-stu-id="a5143-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="a5143-128">Ärge eemaldage seda välja.</span><span class="sxs-lookup"><span data-stu-id="a5143-128">Don't remove this field.</span></span> <span data-ttu-id="a5143-129">Muidu ei hakka lähtestamise skriptid tööle.</span><span class="sxs-lookup"><span data-stu-id="a5143-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="a5143-130">Leidke uue vormi väärtus **formId**.</span><span class="sxs-lookup"><span data-stu-id="a5143-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="a5143-131">Nende sammude läbimiseks on kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="a5143-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="a5143-132">Eksportige vorm **Minu projekti teave** mittehallatava lahenduse osana ja leidke seejärel kohandatud XML-failist eksporditud lahenduse väärtus **formId**.</span><span class="sxs-lookup"><span data-stu-id="a5143-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="a5143-133">Avage redigeerija vormilt vorm **Minu projekti teave** ja leidke URL-i parameetri **fromId** kõrvalt globaalne kordumatu identifikaator (GUID), nagu on näidatud järgmisel illustratsioonil.</span><span class="sxs-lookup"><span data-stu-id="a5143-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Uue vormi formId-väärtuse otsimine URL-ilt](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="a5143-135">Looge vastendus **msdyn\_ordertype** väärtuse **formId** jaoks, redigeerides veebiressursse msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="a5143-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="a5143-136">Eemaldage ressursist kood ja asendage see järgmise koodiga.</span><span class="sxs-lookup"><span data-stu-id="a5143-136">Remove the code from the resource, and replace it with the following code.</span></span>

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

6. <span data-ttu-id="a5143-137">Salvestage kohandus ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="a5143-137">Save and then publish the customizations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]