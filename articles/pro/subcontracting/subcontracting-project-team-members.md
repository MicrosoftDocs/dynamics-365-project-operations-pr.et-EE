---
title: Allhankelepinguga projektimeeskonna liikmed
description: Selles artiklis selgitatakse, kuidas microsofti projektimeeskonna liikmeid allhanke korras allhanke korras tellida Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 649687cb9ac66e684069434a353b63155103aefb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916881"
---
# <a name="subcontracting-project-team-members"></a>Allhankelepinguga projektimeeskonna liikmed

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsoftis Dynamics 365 Project Operations saate valida allhanke korras töötajate või töötajatega projektimeeskonna liikmete allhanke korras.

- Palgata projektimeeskonna liikmetele on määratud üldine ressurss.
- Personaliga meeskonnaliikmetele on määratud nimega ressurss.

Kui seote projektimeeskonna liikme alltöövõtureaga, võetakse kõik meeskonnaliikme ülesannetega seotud ülesanded allhankega seotud ostuhinnakirja alusel tagasi.  **Valige lehe Projekti üksikasjad** vahekaardil **Hinnangud** nupp Uuenda hindu **,** et näha alltöövõtuotsusest tulenevat värskendatud hinnakujundust ja/või kuluarvestust. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Alltöövõtt personalita projektimeeskonna liikmelt
Meeskonnaliikme **üksikasjade** lehel on alltöövõtu- ja alltöövõturea väljad, mis võimaldavad projektijuhil väljendada, kuidas ta soovib allhanke korras nõutavat võimsust kasutada. Projektimeeskonna liikme alltöövõtuks üldise ressursina tehke järgmist.

1.  Valige alltöövõtt **meeskonnaliikme üksikasjade** lehelt.

2.  Saate valida ainult allhankeid, mille **olek on Mustand** või **Kinnitatud**. **Suletud** või **tühistatud** allhankeid ei saa valida. 

3.  Väli **Alltöövõturida** muutub nähtavaks pärast alltöövõtu valimist.

4.  Väljal **Alltöövõturida** saate valida ainult aja jooksul saadaolevaid alltöövõturidu. Kulu või materjali jaoks ei saa alltöövõturidu valida.

5.  Projektimeeskonna liikme kirje roll peab vastama alltöövõtureal olevale rollile. See tagab, et projektis hinnatava rolli aeg on sama roll, mis ostetakse allhankeliinilt. 

Kui üldine meeskonnaliige on seostatud alltöövõtu- ja alltöövõtureaga, **uuendatakse üldise meeskonnaliikme rea väli Töötaja tüüp** lepingutöötajaks **ja** **alltöövõtu kehtivus** väärtuseks **määratakse Kehtiv**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Personaliseeritud projektimeeskonna liikme alltöövõtt
Nagu üldised või personalita meeskonnaliikmed, saab ka projekti jaoks vajalikku töötajate arvu siduda alltöövõtuga. Nimega projektimeeskonna liikme allhanke allhankeks tehke järgmist.

1.  Veenduge, et nimega ressurss oleks seadistatud lepingutöötaja broneeritava ressursi tüübina. Samuti veenduge, et **broneeritava ressursi väli Hankija** vastaks teie valitud allhankelepingu hankijale. 

2.  Allhankeid saate valida ainult olekus **Mustand** või **Kinnitatud**. **Suletud** või **tühistatud** allhankeid ei saa valida. 

3.  Väli **Alltöövõturida** muutub nähtavaks pärast alltöövõtu valimist.

4.  Väljal **Alltöövõturida** saate valida ainult aja jooksul saadaolevaid alltöövõturidu. Kulu või materjali jaoks ei saa alltöövõturidu valida.

5.  Projektimeeskonna liikme kirje roll peab vastama alltöövõtureal olevale rollile. See tagab, et projektis hinnatava rolli aeg on sama roll, mis ostetakse allhankeliinilt. 

Nimega projektimeeskonna liikmed, kes on seadistatud lepingulise töötaja tüübina **Broneeritav ressurss**, kuvatakse allhanke kehtivusolekuga **Ei kehti,** kui nad pole allhankelepinguga seotud. Kui nimeline projektimeeskonna liige on seostatud alltöövõtu- ja alltöövõtureaga, **uuendatakse meeskonnaliikmete rea väli Töötaja tüüp** lepingutöötajaks **ja** **alltöövõtu kehtivus** väärtuseks **on seatud Kehtiv**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
