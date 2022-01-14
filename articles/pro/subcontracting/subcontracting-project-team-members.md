---
title: Alltöövõtu projektimeeskonna liikmed
description: Selles teemas selgitatakse, kuidas microsoftis projektimeeskonna liikmeid allhanke korras allhanke korras teha Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: b98fc356d7de77fa7f05667acaa5569a7053e4d1
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903643"
---
# <a name="subcontracting-project-team-members"></a>Alltöövõtu projektimeeskonna liikmed

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsoftis Dynamics 365 Project Operations saate valida allhanketööta või personalita projektimeeskonna liikmed.

- Personalita projektimeeskonna liikmetel on määratud üldine ressurss.
- Töötajatega meeskonnaliikmetele on määratud nimega ressurss.

Kui seote projektimeeskonna liikme alltöövõtureaga, kodeeritakse kõik meeskonnaliikme ülesannetega seotud ülesanded ümber allhankega seotud ostuhinnakirja alusel.  Valige **lehel** Projekti üksikasjad vahekaardil **Hinnangud nupp Hindade** **värskendamine**, et näha alltöövõtuotsusest tulenevat värskendatud hinnakujundust ja/või kuluarvestust. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Alltöövõtuta projektimeeskonna liige
**Lehel Meeskonnaliikme üksikasjad on** allhanke- ja alltöövõturea väljad, mis võimaldavad projektijuhil väljendada, kuidas ta soovib allhankelt nõutavat võimsust kasutada. Projektimeeskonna liikme alltöövõtuks üldressursina tehke järgmist.

1.  Valige allhanke **leht Meeskonna** liige.

2.  Saate valida ainult allhankeid **olekuga Mustand** või **Kinnitatud**. **Suletud** või **Tühistatud** allhankeid ei saa valida. 

3.  **Väli Alltöövõtu rida** muutub nähtavaks pärast alltöövõtu valimist.

4.  **Väljal Alltöövõturida** saate valida ainult aja jaoks mõeldud allhankeread. Kulude või materjali jaoks ei saa allhankeridu valida.

5.  Projektimeeskonna liikmekirje roll peab vastama alltöövõturea rollile. See tagab, et projektis hinnatav rolli aeg on sama roll, mis ostetakse allhankeliinilt. 

Kui üldine meeskonnaliige on seotud alltöövõtu- ja alltöövõtureaga, **uuendatakse üldise meeskonnaliikme rea väli Töötaja tüüp** **lepingulisele töötajale** ja **alltöövõtu** kehtivuseks **määratakse Kehtiv**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Töötajaga projektimeeskonna liikme alltöövõtt
Sarnaselt üldistele või personalita meeskonnaliikmetele võib projektis nõutavat personalitöötaja suutlikkust seostada ka alltöövõtuga. Nimetatud projektimeeskonna liikme alltöövõtuks tehke järgmist.

1.  Veenduge, et nimetatud ressurss on seadistatud broneeritava ressursi lepingulise töötaja tüübina. Samuti veenduge, et **broneeritava** ressursi väli Hankija vastab teie valitud allhanke hankijale. 

2.  Allhankeid saate valida ainult **olekus Mustand** või **Kinnitatud**. **Suletud** või **Tühistatud** allhankeid ei saa valida. 

3.  **Väli Alltöövõtu rida** muutub nähtavaks pärast alltöövõtu valimist.

4.  **Väljal Alltöövõturida** saate valida ainult aja jaoks mõeldud allhankeread. Kulude või materjali jaoks ei saa allhankeridu valida.

5.  Projektimeeskonna liikmekirje roll peab vastama alltöövõturea rollile. See tagab, et projektis hinnatav rolli aeg on sama roll, mis ostetakse allhankeliinilt. 

Nimega projektimeeskonna liikmed, mis on seadistatud lepingulise töötaja tüüpi **broneeritava** ressursina, kuvatakse alltöövõtu kehtivusolekuga **Ei kehti,** kui need pole alltöövõtuga seotud. Kui nimega projektimeeskonna liige on seotud alltöövõtu- ja alltöövõtureaga, **uuendatakse meeskonna liikme rea väli Töötaja liik** **lepingulisele töötajale** ja **alltöövõtu** kehtivuseks **määratakse Kehtiv**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
