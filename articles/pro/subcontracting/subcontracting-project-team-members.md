---
title: Allhankelepinguga projektimeeskonna liikmed
description: Selles artiklis selgitatakse, kuidas teha Microsoftis projektimeeskonna liikmetele alltöövõttu Dynamics 365 Project Operations.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522790"
---
# <a name="subcontracting-project-team-members"></a>Allhankelepinguga projektimeeskonna liikmed

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Microsoftis Dynamics 365 Project Operations saate valida personalita või personalita projektimeeskonna liikmete alltöövõtulepingu.

- Personalita projektimeeskonna liikmetele on määratud üldine ressurss.
- Töötajatega meeskonnaliikmetele on määratud nimega ressurss.

Kui lingite projektimeeskonna liikme allhankereaga, taastatakse kõik meeskonnaliikme ülesannete ülesanded allhankelepingule lisatud ostuhinnaloendi alusel.  **Valige lehe Projekti üksikasjad vahekaardil** Prognoosid **nupp** Värskenda hindu **,** et näha allhanke otsusest tulenevat värskendatud hinnakujundust ja/või kuluarvestust. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Personalita projektimeeskonna liikme alltöövõtt
Meeskonnaliikme **üksikasjade** lehel on alltöövõtu ja allhanke reaväljad, mis võimaldavad projektijuhil väljendada, kuidas ta soovib allhankelepingust nõutavat võimsust kasutada. Projektimeeskonna liikmele üldise ressursina allhankelepingu sõlmimiseks toimige järgmiselt.

1.  Valige alltöövõtt lehel Meeskonnaliikme **üksikasjad**.

2.  Saate valida ainult mustandi **või** kinnitatud olekuga **alltöövõtulepinguid**. **Suletud** või **tühistatud** alltöövõtulepinguid ei saa valida. 

3.  Väli **Allhanke rida** muutub nähtavaks pärast allhanke valimist.

4.  Väljal **Allhanke rida** saate valida ainult need allhanke read, mis on mõeldud aja jaoks. Kulu või materjali jaoks ei saa valida allhanke ridu.

5.  Projektimeeskonna liikme kirje roll peab vastama allhanke real olevale rollile. See tagab, et projektis hinnatava rolli jaoks kuluv aeg on sama roll, mis ostetakse allhankeliinilt. 

Kui üldine meeskonnaliige on seostatud allhanke ja allhanke reaga, **värskendatakse üldise meeskonnaliikme rea välja Töötaja tüüp** väärtuseks **Lepinguline töötaja** ja **Allhanke kehtivus** väärtuseks **Kehtiv**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Personaliga projektimeeskonna liikme alltöövõtt
Nagu üldised või personalita meeskonnaliikmed, saab ka projektis nõutavat meeskonnaliikmete arvu alltöövõtuga siduda. Nimega projektimeeskonna liikme alltöövõtulepingu sõlmimiseks toimige järgmiselt.

1.  Veenduge, et nimetatud ressurss oleks seadistatud lepingulise töötaja tüüpi broneeritava ressursina. Samuti veenduge, et **broneeritava ressursi väli Hankija** vastaks teie valitud allhanke hankijale. 

2.  Alltöövõtulepinguid saate valida ainult olekus **Mustand** või **Kinnitatud**. **Suletud** või **tühistatud** alltöövõtulepinguid ei saa valida. 

3.  Väli **Allhanke rida** muutub nähtavaks pärast allhanke valimist.

4.  Väljal **Allhanke rida** saate valida ainult need allhanke read, mis on mõeldud aja jaoks. Kulu või materjali jaoks ei saa valida allhanke ridu.

5.  Projektimeeskonna liikme kirje roll peab vastama allhanke real olevale rollile. See tagab, et projektis hinnatava rolli jaoks kuluv aeg on sama roll, mis ostetakse allhankeliinilt. 

Nimega projektimeeskonna liikmed, kes on seadistatud lepingulise töötaja tüüpi **broneeritava ressursina**, kuvatakse allhankelepingu kehtivuse olekuga **Pole kehtiv,** kui nad pole allhankelepinguga seotud. Kui nimega projektimeeskonna liige on seostatud allhanke ja allhanke reaga, **värskendatakse meeskonnaliikme rea välja Töötaja tüüp** väärtuseks **Lepinguline töötaja** ja **allhanke kehtivus** väärtuseks **määratakse Kehtiv**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
