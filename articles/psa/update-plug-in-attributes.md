---
title: Lisandmooduli atribuutide värskendamine uute hinnakujunduse dimensioonide lisamiseks
description: Selles teemas kirjeldatakse hinnakujunduse dimensioonide jaoks lisandmooduli atribuutide värskendamist.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d04561fb6bcbc64f6ad3ea922bff1912824be64c6bb2b18cddd95e9b1b5c7850
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988781"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Lisandmooduli atribuutide värskendamine uute hinnakujunduse dimensioonide lisamiseks

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Kui te ei kasuta Project Service Automation (PSA) hinnapakkumise tegemise ja lepingute sõlmimise funktsioone, võite selle teema vahele jätta.

See teema eeldab, et olete lõpetanud toimingud teemades [Kohandatud väljade ja olemite loomine](create-custom-fields-entities.md), [Kohandatud väljade lisamine hinna seadistamisele ja ülekande olemitele](field-references.md) ning [Kohandatud väljade seadistamine hinnakujunduse dimensioonidena](set-up-pricing-dimensions.md). Kui te pole neid toiminguid lõpetanud, minge tagasi, viige need lõpuni ja seejärel tulge selle teema juurde tagasi.

Kui projekti hinnapakkumise rea jaoks luuakse hinnapakkumise rea üksikasjad lehel **Hinnapakkumise rida**, loob süsteem taustal kaks prognoosirida: üks rida prognoosi kulu poolele ja teine müügi poolele. Sama kehtib ka projekti lepinguridade kohta.

Kui muudate kulupoole kogust või välja, kantakse see muudatus üle ka müügipoolele. See on võimalik tänu järgnevatele lisandmoodulitele, mida tuleb pärast hinnakujunduse dimensioonide muutmist uuesti registreerida.

- PreOperationContractLineDetailUpdate – värskendused **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate – värskendused **msdyn_quotelinetransaction**.

Järgmised etapid selgitavad teile lisandmoodulite registreerimise protsessi.

1. Avage **PluginRegistrationTool** ja looge ühendus oma võrguühendusega eksemplariga.
2. Klõpsake käsku **Otsi** ja otsige üles lisandmoodul, mida soovite värskendada.

 ![Otsingupuu kuvatõmmis.](media/PRT-1.png)

3. Pärast lisandmooduli leidmist valige see ja klõpsake valikut **Vali Põhivormil**.

4. Valige lisandmooduli etapp, mida soovite värskendada, paremklõpsake seda ja valige seejärel käsk **Värskenda**.

 ![Kuvatõmmis värskendatavast lisandmoodulist.](media/PRT-2.png)
 
5. Klõpsake värskendamise aknas filtreerimise atribuutides kolmikpunkti (**...**).

 ![Kuvatõmmis olemasoleva etapi värskendamise konfiguratsiooniteabest.](media/PRT-3.png)
 
6. Valige hinnakujunduse atribuudi märkeruudud.

 ![Kuvatõmmis, kus on näha hinnakujunduse atribuutide märkeruutude valikut.](media/PRT-4.png)

7. Lehe sulgemiseks klõpsake nuppu **OK** ja seejärel käsku **Värskenda etappi**.

 ![Kuvatõmmis, kus on näha nuppu „Värskenda etappi”.](media/PRT-5.png)
 
8. Korrake seda protsessi ka teise lisandmooduli puhul, **PreOperationQuoteLineDetail – msdyn_quotelinetransaction-i värskendamine**.

9. Sulgege lisandmooduli registreerimistööriist.



[!INCLUDE[footer-include](../includes/footer-banner.md)]