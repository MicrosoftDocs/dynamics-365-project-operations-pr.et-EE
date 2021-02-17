---
title: Lisandmooduli atribuutide värskendamine uute hinnakujunduse dimensioonidega
description: Selles teemas kirjeldatakse, kuidas värskendada hinnakujunduse dimensioonide jaoks lisandmooduli atribuute.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643213"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Lisandmooduli atribuutide värskendamine uute hinnakujunduse dimensioonidega

Selles teemas kirjeldatakse, kuidas värskendada hinnakujunduse dimensioonide jaoks lisandmooduli atribuute.

> [!NOTE]
> See teema kehtib ainult rakenduse Dynamics 365 Project Operations hinnapakkumise ja lepingu funktsioonide kohta.

## <a name="prerequisites"></a>Eeltingimused
Enne selles teemas toodud juhiste täitmist peate viima lõpule toimingud järgmistes teemades.

  - [Kohandatud väljade ja olemite loomine](create-custom-fields-entities-pricing-dimensions.md) 
  - [Kohandatud väljade lisamine hinna seadistusele ja ülekande olemitele ](add-custom-fields-price-setup-transactional-entities.md)
  - [Kohandatud väljade seadistamine hinnakujunduse dimensioonidena](set-up-custom-fields-pricing-dimensions.md). 
  
Kui te pole neid toiminguid lõpetanud, viige need lõpuni ja seejärel tulge selle teema juurde tagasi.

## <a name="register-a-plug-in"></a>Lisandmooduli registreerimine
Kui projekti hinnapakkumise rea jaoks luuakse lehel **Hinnapakkumise rida** hinnapakkumise rea üksikasi, loob süsteem kaks hinnangu rida. Üks rida on hinnangu kulupoole jaoks ja teine rida on müügipoole jaoks. Sama kehtib ka projekti lepinguridade kohta.

Kui muudate kulupoole kogust või välja, tehase see muudatus ka müügipoolel. See on võimalik, kuna atribuudi Quotelinedetail lisnadmoodulid PreOperation ja lepingurea üksikasja olemis ühendavad kulupoole kindlad atribuudid tehingu müügipoolega. Kui soovite, et müügipoole hinnakujunduse dimensiooni väärtustele tehtavad muudatused tehtaks ka kulupoolel, tuleb pärast hinnakujunduse dimensioonile muudatuste tegemist registreerida uuesti järgmised lisandmoodulid.

Järgmised lisandmoodulid tuleb värskendada ja uuesti registreerida.

- PreOperationContractLineDetailUpdate – **värskendab üksuse msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **värskendab üksuse msdyn_quotelinetransaction**

Lisandmoodulite värskendamiseks ja uuesti registreerimiseks peate tegema järgmist.

1. Avage **PluginRegistrationTool** ja ühendage oma Project Operationsi teenuse Dataverse keskkond.
2. Valige **Otsing** ja sisendage värskendatava lisandmooduli esimesed tähed.
3. Pärast lisandmooduli leidmist valige see ja valige seejärel suvand **Vali Põhivormil**.
4. Valige etapp **Üksuse msdyn_orderlinetransaction värskendamine**, tehke paremklõps ja valige seejärel **Värskenda**.
5. Dialoogilehel **Värskendus** valige filtreerimise atribuutides kolmikpunkt (**...**).
6. Avaneb filtreerimise atribuutide aken ja kuvab loendi kõikidest olemi atribuutidest ja hinnakujunduse dimensioonidest. Märkige hinnakujunduse dimensiooni atribuutide märkeruudud.
7. Lehe sulgemiseks valige **OK** ja valige seejärel käsk **Värskenda etappi**.
8. Korrake etappe 2–7 teise lisandmooduli **PreOperationQuoteLineDetail** jaoks. Selle lisandmooduli jaoks peate värskendama etappi **Üksuse msdyn_quotelinetransaction värskendamine**.
9. Sulgege tööriist **PluginRegistrationTool**.