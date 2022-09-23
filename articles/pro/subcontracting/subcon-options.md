---
title: Allhankelepingu valikud projektimeeskonna liikmete jaoks
description: Selles artiklis selgitatakse Microsofti projektimeeskonna liikmete allhankevõimalusi Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522273"
---
# <a name="subcontracting-options-for-project-team-members"></a>Allhankelepingu valikud projektimeeskonna liikmete jaoks

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Microsoftis Dynamics 365 Project Operations saate hinnata allhanke võimalusi, mis on saadaval ühe või mitme projektimeeskonna liikme jaoks. Saadaolevad alltöövõtusuvandid võimaldavad teil teha järgmist.

- Looge valitud projektimeeskonna liikmetele uus alltöövõtt ja/või olemasolevale allhankele uued read. 
- Reserv juba olemasoleva alltöövõtu ja alltöövõtuliini eest. 

Saate valida üldiste projektimeeskonna liikmete jaoks saadaolevate allhankevalikute hulgast või valida projektimeeskonna liikmete hulgast, kelle personaliks on nimega ressurss, mis on lepinguline töötaja. 

Alltöövõtuvõimalusi pole saadaval järgmistel juhtudel.

- Projektimeeskonna liikmed, kellel on töötaja. 
- Projektimeeskonna liikmed, kes on juba seostatud allhanke ja allhankeliiniga. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Personalita projektimeeskonna liikme alltöövõtt

Üldise või personalita projektimeeskonna liikme jaoks saadaolevate alltöövõtusuvandite ülevaatamiseks ja valimiseks tehke järgmist.

1. Valige üks või mitu projektimeeskonna liikme kirjet, kus ressurss on üldine ressurss.
2. Veenduge, et ükski valitud projektimeeskonna liikme kirje pole juba allhankelepinguga sõlmitud. 
3. Valige **projektimeeskonna liikmete alamruudustikus Allhankesuvandid**. Avaneb **dialoog Allhankesuvandid**. 
4. Kui valisite 1. etapis ainult ühe projektimeeskonna liikme kirje, on saadaval järgmised valikud.
    - Looge uusi allhankeliine. 
    - Olemasoleva allhankelepingu alusel reserveerimine Kui valisite 1. etapis mitu projektimeeskonna liikme kirjet, on ainus võimalus luua uued allhankeread.
5. Võimalus reserveerida olemasoleva alltöövõturea eest võimaldab teil valida allhanke ja allhankerea, mille jaoks soovite varuda. Võimsuse reserveerimiseks allhankerea valimisel peaksite tagama, et valitud allhankerida on ajaline ja et projektimeeskonna liikmelt nõutav roll vastab allhankeliinilt ostetud rollile.
6. Kui otsustate luua projektimeeskonna liikmetele uusi allhankeridu, võimaldab süsteem teil valida allhanke, mille soovite need read luua. Alltöövõtt, mille valite uute ridade loomiseks, peaks olema olekus **Mustand**. Selle suvandiga luua valitud projektimeeskonna liikmetele uusi allhankeridu loob süsteem iga projektimeeskonna liikme jaoks aja jooksul ühe allhankerea. Roll, tunnid ja kuupäevad kopeeritakse projektimeeskonna liikmelt igale loodud allhankereale. 
7. Kui üldine meeskonnaliige on seostatud allhanke ja allhanke reaga, **värskendatakse üldise meeskonnaliikme rea välja Töötaja tüüp** väärtuseks **Lepinguline töötaja** ja **väärtuse Allhanke kehtivus** väärtuseks **Määratakse Kehtiv**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Personaliga projektimeeskonna liikme alltöövõtt

Sarnaselt üldistele või personalita meeskonnaliikmetele saate vaadata ka personaliga projektimeeskonna liikme allhankevõimalusi, kui töötaja on lepinguline töötaja. Personaliga või nimega projektimeeskonna liikme jaoks saadaolevate alltöövõtusuvandite ülevaatamiseks ja nende hulgast valimiseks tehke järgmist.

1. Valige üks või mitu projektimeeskonna liikme kirjet, kus ressurss on nimega lepinguline töötaja.
2. Veenduge, et ükski valitud projektimeeskonna liikme kirjetest pole juba allhankeleping. 
3. Valige **projektimeeskonna liikmete alamruudustikus Allhankesuvandid**. Avaneb **dialoog Allhankesuvandid**. 
4. Kui valisite 1. etapis ainult ühe projektimeeskonna liikme kirje, on saadaval järgmised valikud.
      - Looge uusi allhankeliine.
      - Reserveerige olemasoleva alltöövõtulepingu eest.
  Kui valisite juhises 1 mitu projektimeeskonna liikme kirjet, on ainus saadaolev võimalus luua uued allhankeread.
5. Võimalus reserveerida olemasoleva alltöövõturea eest võimaldab teil valida allhanke ja allhankerea, mille jaoks soovite varuda. Võimsuse reserveerimiseks alltöövõtuliini valimisel peaksite tagama järgmise:
      - Valitud allhanke rida on aja jaoks. 
      - Projektimeeskonna liikmelt nõutav roll ühtib allhankereal ostetud rolliga. 
      - Hankija, kellega lepinguline töötaja on seostatud, on sama, mis alltöövõtu hankija.
6. Kui otsustate luua projektimeeskonna liikmetele uusi allhankeridu, võimaldab süsteem teil valida allhanke, mille soovite need read luua. Selle valikuga peaksite tagama, et hankija, kuhu lepinguline töötaja kuulub, on sama, mis allhanke hankija. 
7. Alltöövõtt, mille valite uute ridade loomiseks, peaks olema olekus **Mustand**. Selle suvandiga luua valitud projektimeeskonna liikmetele uusi allhankeridu loob süsteem iga projektimeeskonna liikme jaoks aja jooksul ühe allhankerea. Roll, tunnid ja kuupäevad kopeeritakse projektimeeskonna liikmelt igale loodud allhankereale.  
8. Kui nimeline meeskonnaliige on seostatud allhanke ja allhanke reaga, **värskendatakse nimega meeskonnaliikme rea välja Töötaja tüüp** väärtuseks **Contract Worker** ja **väärtuse Allhanke kehtivus** väärtuseks **Saab.**

## <a name="re-costing-subcontractor-assignments"></a>Alltöövõtjate tööülesannete ümberhindamine

Kui projektimeeskonna liige (üldine või nimeline) on dialoogi Allhankesuvandid **abil** lingitud allhanke ridadega, hinnatakse kõik meeskonnaliikme ülesannetele määratud määrangud ümber allhankelepingule lisatud ostuhinnaloendi alusel. **Valige lehe Projekti üksikasjad vahekaardil** Prognoosid **nupp** Värskenda hindu **,** et näha allhanke otsusest tulenevat värskendatud hinnakujundust ja/või kuluarvestust.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
