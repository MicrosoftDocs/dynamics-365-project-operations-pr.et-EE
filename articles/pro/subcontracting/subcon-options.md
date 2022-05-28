---
title: Allhankelepingu valikud projektimeeskonna liikmete jaoks
description: Selles teemas selgitatakse Microsofti projektimeeskonna liikmete alltöövõtusuvandeid Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aacd2f97d3120a854c78fe87e512fad1c43b9651
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600185"
---
# <a name="subcontracting-options-for-project-team-members"></a>Allhankelepingu valikud projektimeeskonna liikmete jaoks

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsoftis Dynamics 365 Project Operations saate hinnata ühe või mitme projektimeeskonna liikme jaoks saadaolevaid alltöövõtusuvandeid. Saadaolevad alltöövõtuvõimalused võimaldavad teil teha järgmist.

- Looge uus alltöövõtt ja/või looge valitud projektimeeskonna liikmetele olemasolevale alltöövõtule uued read. 
- Reserveerige juba olemasoleva alltöövõtu- ja alltöövõtuliini suhtes. 

Saate valida üldiste projektimeeskonna liikmete saadaolevate alltöövõtuvõimaluste hulgast või valida projektimeeskonna liikmete hulgast, kellel on lepinguline töötaja nimega ressurss. 

Alltöövõtu võimalusi pole saadaval järgmiste jaoks.

- Projektimeeskonna liikmed, kes on töötanud töötajaga. 
- Projektimeeskonna liikmed, kes on juba seotud alltöövõtu- ja alltöövõtureaga. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Alltöövõtt personalita projektimeeskonna liikmelt

Üldise või personalita projektimeeskonna liikme saadaolevate alltöövõtusuvandite ülevaatamiseks ja nende hulgast valimiseks tehke järgmist.

1. Valige üks või mitu projektimeeskonna liikme kirjet, kus ressurss on üldine ressurss.
2. Veenduge, et ükski valitud projektimeeskonna liikmekirjetest pole juba allhanke korras. 
3. Valige **projektimeeskonna liikmete alamruudustikus alltöövõtu suvandid**. Avaneb **dialoog Alltöövõtusuvandid**. 
4. Kui valisite 1. etapis ainult ühe projektimeeskonna liikme kirje, on saadaval järgmised suvandid.
    - Looge uusi alltöövõtu ridu. 
    - Reserveeri olemasoleva allhanke vastu Kui valisite 1. etapis mitu projektimeeskonna liikme kirjet, on ainus saadaolev võimalus luua uued alltöövõturead.
5. Olemasoleva allhankerea reserveerimise võimalus võimaldab teil valida allhanke- ja alltöövõturea, mille vastu soovite reserveerida. Kui valite võimsuse reserveerimiseks allhankerea, peaksite tagama, et valitud allhankerida on ajakohane ja et projektimeeskonna liikmel nõutav roll vastab alltöövõtureal ostetud rollile.
6. Kui otsustate projektimeeskonna liikmetele luua uusi alltöövõturidu, võimaldab süsteem valida allhankelepingu, mille soovite need read luua. Alltöövõtt, mille valite uute ridade loomiseks, peaks olema olekus **Mustand**. Selle suvandiga valitud projektimeeskonna liikmetele uute alltöövõturidade loomiseks loob süsteem iga projektimeeskonna liikme jaoks ühe alltöövõturea. Roll, tunnid ja kuupäevad kopeeritakse projektimeeskonna liikmelt igale loodavale allhankereale. 
7. Kui üldine meeskonnaliige on seostatud alltöövõtu- ja alltöövõtureaga, **uuendatakse üldise meeskonnaliikme rea väli Töötaja tüüp** lepingutöötajaks **ja** **väärtuseks allhanke kehtivus** väärtuseks **määratakse Kehtiv**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Personaliseeritud projektimeeskonna liikme alltöövõtt

Nagu üldised või personalita meeskonnaliikmed, saate vaadata ka personaliga projektimeeskonna liikme alltöövõtu võimalusi, kui töötaja on lepinguline töötaja. Töötaja või nimega projektimeeskonna liikme saadaolevate alltöövõtuvõimaluste ülevaatamiseks ja nende hulgast valimiseks tehke järgmist.

1. Valige üks või mitu projektimeeskonna liikme kirjet, kus ressurss on nimega lepingutöötaja.
2. Veenduge, et ükski valitud projektimeeskonna liikme kirje pole juba allhanke korras allhanke korras. 
3. Valige **projektimeeskonna liikmete alamruudustikus alltöövõtu suvandid**. Avaneb **dialoog Alltöövõtusuvandid**. 
4. Kui valisite 1. etapis ainult ühe projektimeeskonna liikme kirje, on saadaval järgmised suvandid.
      - Looge uusi alltöövõtu ridu.
      - Reserveerige olemasoleva allhanke vastu.
  Kui valisite 1. etapis mitu projektimeeskonna liikme kirjet, on ainus võimalus luua uued alltöövõturead.
5. Olemasoleva allhankerea reserveerimise võimalus võimaldab teil valida allhanke- ja alltöövõturea, mille vastu soovite reserveerida. Kui valite võimsuse reserveerimiseks alltöövõturea, peaksite tagama järgmise.
      - Valitud alltöövõturida on ajastatud. 
      - Projektimeeskonna liikmel nõutav roll vastab allhanke realt ostetud rollile. 
      - Hankija, kellega lepingutöötaja on seotud, on sama, mis allhanke hankijal.
6. Kui otsustate projektimeeskonna liikmetele luua uusi alltöövõturidu, võimaldab süsteem valida allhankelepingu, mille soovite need read luua. Selle suvandiga peaksite tagama, et hankija, kellele lepingutöötaja kuulub, on sama, mis allhanke hankija. 
7. Alltöövõtt, mille valite uute ridade loomiseks, peaks olema olekus **Mustand**. Selle suvandiga valitud projektimeeskonna liikmetele uute alltöövõturidade loomiseks loob süsteem iga projektimeeskonna liikme jaoks ühe alltöövõturea. Roll, tunnid ja kuupäevad kopeeritakse projektimeeskonna liikmelt igale loodavale allhankereale.  
8. Kui nimega meeskonnaliige on seotud alltöövõtu- ja alltöövõtureaga, **uuendatakse nimega meeskonnaliikmete rea väli Töötaja tüüp** väärtuseks **Lepingutöötaja** ja **väärtuseks allhanke kehtivus** väärtuseks **määratakse Kehtiv**.

## <a name="re-costing-subcontractor-assignments"></a>Alltöövõtjate määramiste ümbermaksmine

Kui projektimeeskonna liige (üldine või nimega) on dialoogiboksi Alltöövõtusuvandite **abil** lingitud alltöövõtu ridadega, võetakse kõik meeskonnaliikme ülesannete määramised allhankega seotud ostuhinnakirja alusel ümber. **Valige lehe Projekti üksikasjad** vahekaardil **Hinnangud** nupp Uuenda hindu **,** et näha alltöövõtuotsusest tulenevat värskendatud hinnakujundust ja/või kuluarvestust.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
