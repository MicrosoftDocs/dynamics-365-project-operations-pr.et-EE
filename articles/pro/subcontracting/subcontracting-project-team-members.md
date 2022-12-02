---
title: Allhankelepinguga projektimeeskonna liikmed
description: See artikkel selgitab, kuidas sõlmida projektimeeskonna liikmetega allhankelepinguid rakenduses Microsoft Dynamics 365 Project Operations.
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

Rakenduses Microsoft Dynamics 365 Project Operations saate valida, kas sõlmida allhankelepingud töötajateta või töötajatega projektimeeskonna liikmetega.

- Töötajateta projektimeeskonna liikmetele on määratud üldine ressurss.
- Meeskonnaliikmetele on määratud nimeline ressurss.

Kui seote projektimeeskonna liikme allhankelepingureaga, arvestatakse kõik meeskonnaliikmel olevate ülesannete määramised ümber allhankelepingule lisatud ostuhinnakirja alusel.  Valige vahekaardi **Prognoosid** lehel **Projekti üksikasjad** nuppu **Hindade värskendamine**, et näha allhankeotsusest tulenevat värskendatud hinnakujundust ja/või kulukalkulatsiooni. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Personalita projektimeeskonna liikme allhange
Lehel **Meeskonnaliikme üksikasjad** on allhankelepingu ja allhankelepingurea väljad, mis võimaldavad projektijuhil väljendada, kuidas nad soovivad allhankelepingust nõutavat võimsust ammutada. Projektimeeskonna liikme allhankelepingu sõlmimiseks üldise ressursina toimige järgmiselt.

1.  Valige lehel **Meeskonnaliikme üksikasjad** allhange.

2.  Saate valida ainult allhankelepinguid, mille olek on **Mustand** või **Kinnitatud**. **Suletud** või **Tühistatud** allhankelepinguid ei saa valida. 

3.  Väli **Allhankelepingu rida** muutub nähtavaks pärast allhankelepingu valimist.

4.  Väljal **Allhankelepingu rida** saate valida ainult ajalised allhankelepinguread. Kulude või materjalide jaoks ei saa valida allhankelepinguridu.

5.  Projektimeeskonna liikme kirje roll peab ühtima rolliga allhankelepingureal. See tagab, et projektis prognoositava rolli täitmise aeg on sama roll, mis ostetakse allhankelepingurealt. 

Kui üldine meeskonnaliige on seotud allhankelepingu ja allhankelepingureaga, värskendatakse üldise meeskonnaliikme rea välja **Töötaja tüüp** väärtuseks **Lepinguline töötaja** ja **Allhankelepingu kehtivus** seatud väärtusele **Kehtiv**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Projekti meeskonnaliikme allhange personaliga
Sarnaselt üldistele või personalita meeskonnaliikmetele võib ka projektis nõutava meeskonnaliikme suutlikkuse siduda allhankelepinguga. Nimelise projektimeeskonna liikme allhankelepingus järgige järgmisi etappe.

1.  Veenduge, et nimetatud ressurss oleks seadistatud broneeritava ressursi lepingulise töötaja tüübina. Samuti veenduge, et broneeritava ressursi väli **Hankija** ühtiks teie valitud allhankelepingu hankijaga. 

2.  Allhankelepinguid saate valida ainult olekuga **Mustand** ja **Kinnitatud**. **Suletud** või **Tühistatud** allhankelepinguid ei saa valida. 

3.  Väli **Allhankelepingu rida** muutub nähtavaks pärast allhankelepingu valimist.

4.  Väljal **Allhankelepingu rida** saate valida ainult ajalised allhankelepinguread. Kulude või materjalide jaoks ei saa valida allhankelepinguridu.

5.  Projektimeeskonna liikme kirje roll peab ühtima rolliga allhankelepingureal. See tagab, et projektis prognoositava rolli täitmise aeg on sama roll, mis ostetakse allhankelepingurealt. 

Nimetatud projektimeeskonna liikmed, kes on seadistatud **Broneeritav ressurss** lepingulise töötajana, kuvatakse allhankelepingu kehtivuse olekuga **Ei kehti**, kui nad ei ole allhankelepinguga seotud. Kui nimetatud projektimeeskonna liige on seotud allhankelepingu ja allhankelepingureaga, värskendatakse meeskonnaliikme rea välja **Töötaja tüüp** väärtuseks **Lepinguline töötaja** ja **Allhankelepingu kehtivus** on seatud olekule **Kehtiv**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
