---
title: Projektimeeskonna liikmete alltöövõtuvõimalused
description: Selles teemas selgitatakse Microsofti projektimeeskonna liikmete alltöövõtu võimalusi Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903013"
---
# <a name="subcontracting-options-for-project-team-members"></a>Projektimeeskonna liikmete alltöövõtuvõimalused

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsoftis Dynamics 365 Project Operations saate hinnata ühe või mitme projektimeeskonna liikme jaoks saadaolevaid alltöövõtusuvandeid. Saadaolevad alltöövõtuvõimalused võimaldavad teil teha järgmist.

- Looge valitud projektimeeskonna liikmetele uus alltöövõtt ja/või looge olemasolevale allhankele uued read. 
- Reserveerige juba olemasoleva allhanke- ja alltöövõtuliini vastu. 

Saate valida üldiste projektimeeskonna liikmete saadaolevate alltöövõtuvõimaluste hulgast või valida projektimeeskonna liikmete hulgast, kes on komplekteeritud nimega ressursiga, mis on lepinguline töötaja. 

Alltöövõtu võimalusi ei ole saadaval järgmisteks.

- Projektimeeskonna liikmed, kes on töötajaga komplekteeritud. 
- Projektimeeskonna liikmed, kes on juba seotud alltöövõtu- ja alltöövõtuliiniga. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Alltöövõtuta projektimeeskonna liige

Üldise või töötaja jaoks saadaolevate alltöövõtuvõimaluste ülevaatamiseks ja nende hulgast valimiseks tehke järgmist.

1. Valige üks või mitme projektimeeskonna liikme kirje, kus ressurss on üldine ressurss.
2. Veenduge, et ükski valitud projektimeeskonna liikme kirje pole juba alltöövõtulepinguga. 
3. Valige **projektimeeskonna** liikmete alamruudustikus alltöövõtusuvandid. Avaneb **dialoogiboks** Alltöövõtusuvandid. 
4. Kui valisite 1. etapis ainult ühe projektimeeskonna liikme kirje, on saadaval järgmised suvandid.
    - Looge uusi alltöövõturidu. 
    - Reserveerige olemasoleva allhankega Kui valisite 1. etapis mitu projektimeeskonna liikme kirjet, on ainus võimalik võimalus luua uus alltöövõturida.
5. Võimalus reserveerida olemasoleva allhankerea vastu võimaldab teil valida allhanke- ja alltöövõtuliini, mille vastu soovite reserveerida. Võimsuse reserveerimiseks allhankerea valimisel peaksite tagama, et valitud allhankerida on aja jooksul ja et projektimeeskonna liikmel nõutav roll vastab alltöövõtuliinil ostetud rollile.
6. Kui valite projektimeeskonna liikmetele uute alltöövõturidade loomise, võimaldab süsteem valida allhanke, mida soovite need read luua. Alltöövõtt, mille valite uute ridade loomiseks, peaks olema **olekus** Mustand. Selle suvandiga, et luua valitud projektimeeskonna liikmetele uued alltöövõturead, loob süsteem iga projektimeeskonna liikme jaoks ühe allhankerea aja kohta. Roll, tunnid ja kuupäevad kopeeritakse projektimeeskonna liikmelt igale loodud allhankereale. 
7. Kui üldine meeskonnaliige on seotud alltöövõtu- ja alltöövõtureaga, **uuendatakse üldise meeskonnaliikme rea väli Töötaja liik** **lepinguliseks töötajaks** ja **alltöövõtu** kehtivuse väärtuseks määratakse **Kehtiv**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Töötajaga projektimeeskonna liikme alltöövõtt

Sarnaselt üldistele või personalita meeskonnaliikmetele saate vaadata ka personaliga projektimeeskonna liikme alltöövõtuvõimalusi, kui töötaja on lepinguline töötaja. Personali või nimega projektimeeskonna liikme saadaolevate alltöövõtuvõimaluste ülevaatamiseks ja nende hulgast valimiseks tehke järgmist.

1. Valige üks või mitme projektimeeskonna liikme kirje, kus ressurss on nimega lepinguline töötaja.
2. Veenduge, et ükski valitud projektimeeskonna liikmekirje pole juba alltöövõtulepinguga. 
3. Valige **projektimeeskonna** liikmete alamruudustikus alltöövõtusuvandid. Avaneb **dialoogiboks** Alltöövõtusuvandid. 
4. Kui valisite 1. etapis ainult ühe projektimeeskonna liikme kirje, on saadaval järgmised suvandid.
      - Looge uusi alltöövõturidu.
      - Reserveerige olemasoleva allhanke vastu.
  Kui valisite 1. etapis mitu projektimeeskonna liikme kirjet, on ainus võimalik võimalus luua uus allhankeread.
5. Võimalus reserveerida olemasoleva allhankerea vastu võimaldab teil valida allhanke- ja alltöövõtuliini, mille vastu soovite reserveerida. Võimsuse reserveerimiseks allhankerea valimisel peaksite tagama järgmise.
      - Valitud allhankerida on aja jaoks. 
      - Projektimeeskonna liikmel nõutav roll vastab alltöövõtuliinil ostetud rollile. 
      - Hankija, millega lepinguline töötaja on seotud, on sama, mis alltöövõtul olev hankija.
6. Kui valite projektimeeskonna liikmetele uute alltöövõturidade loomise, võimaldab süsteem valida allhanke, mida soovite need read luua. Selle suvandiga peaksite tagama, et hankija, kuhu lepinguline töötaja kuulub, on sama, mis alltöövõtu hankija. 
7. Alltöövõtt, mille valite uute ridade loomiseks, peaks olema **olekus** Mustand. Selle suvandiga, et luua valitud projektimeeskonna liikmetele uued alltöövõturead, loob süsteem iga projektimeeskonna liikme jaoks ühe allhankerea aja kohta. Roll, tunnid ja kuupäevad kopeeritakse projektimeeskonna liikmelt igale loodud allhankereale.  
8. Kui nimetatud meeskonnaliige on seotud alltöövõtu- ja alltöövõtureaga, **uuendatakse nimega meeskonnaliikme rea väli Töötaja liik** **lepinguliseks töötajaks** ja **alltöövõtu kehtivuse** väärtuseks **määratakse Kehtiv**.

## <a name="re-costing-subcontractor-assignments"></a>Alltöövõtja määramise ümberminek

Kui projektimeeskonna liige (üldine või nimeline) on lingitud alltöövõturidadega, kasutades **dialoogi** alltöövõtusuvandid, lähevad meeskonnaliikme ülesannetele määratud ülesanded allhankega seotud ostuhinnakirja alusel ümber. Valige **lehel** Projekti üksikasjad vahekaardil **Hinnangud nupp Hindade** **värskendamine**, et näha alltöövõtuotsusest tulenevat värskendatud hinnakujundust ja/või kuluarvestust.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
