---
title: Allhankelepingu valikud projektimeeskonna liikmete jaoks
description: See artikkel selgitab projektimeeskonna liikmete allhankevalikuid rakenduses Microsoft Dynamics 365 Project Operations.
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

Rakenduses Microsoft Dynamics 365 Project Operations saate hinnata ühe või mitme projektimeeskonna liikme jaoks saadaolevaid allhankevalikuid. Saadaolevad allhankevõimalused võimaldavad teil:

- Luua valitud projektimeeskonna liikmete jaoks uus allhankeleping ja/või looge olemasolevale allhankelepingule uued read. 
- Reserveerida juba olemasoleva allhankelepingu ja allhankelepingurea alusel. 

Valida saadaolevate allhankevõimaluste hulgast üldiste projektimeeskonna liikmete jaoks või valida projektimeeskonna liikmete hulgast, kes on töötanud nimelise ressursiga, mis on lepinguline töötaja. 

Allhankevõimalused ei ole saadaval järgmistel juhtudel:

- Projekti meeskonnaliikmed, kes on töötajatega komplekteeritud. 
- Projektimeeskonna liikmed, kes on juba seotud allhanke ja allhankelepingureaga. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Personalita projektimeeskonna liikme allhange

Üldise või personalita projektimeeskonna liikme saadaolevate allhankevalikute ülevaatamiseks ja nende hulgast valimiseks toimige järgmiselt.

1. Valige üks või mitu projektimeeskonna liikme kirjet, kus ressurss on üldine ressurss.
2. Veenduge, et ükski valitud projektimeeskonna liikme kirjetest ei oleks juba allhankelepingu alusel sõlmitud. 
3. Valige projektimeeskonna liikmete alamruudustikus **Allhanke valikud**. Avaneb dialoog **Allhanke valikud**. 
4. Kui valisite 1. etapis ainult ühe projektimeeskonna liikme kirje, on saadaval järgmised valikud.
    - Looge uus allhankelepingu rida. 
    - Reserveerige olemasoleva allhankelepingu alusel, kui valisite 1. etapis mitu projektimeeskonna liikme kirjet, on ainus saadaolev võimalus luua uued allhankelepinguread.
5. Olemasoleva allhankelepingu rea alusel reserveerimise võimalus võimaldab teil valida allhankelepingu ja allhankelepingu rea, mille jaoks soovite reserveerida. Tootmisvõimsuse reserveerimiseks allhankelepingurea valimisel peaksite tagama, et valitud allhankelepingu rida on ajaline ja, et projektimeeskonna liikmel nõutav roll ühtib allhankelepingu realt ostetud rolliga.
6. Kui valite projektimeeskonna liikmete jaoks uute allhankelepinguridade loomise, võimaldab süsteem teil valida allhankelepingu, mille alusel soovite need read luua. Allhankeleping, mille valite uute ridade loomiseks, peaks olema olekus **Mustand**. Selle valikuga luua valitud projektimeeskonna liikmetele uued allhankelepinguread, loob süsteem iga projektimeeskonna liikme jaoks aja jaoks ühe allhankelepingurea. Roll, tunnid ja kuupäevad kopeeritakse projektimeeskonna liikmelt igale loodavale allhankelepingureale. 
7. Kui üldine meeskonnaliige on seotud allhankelepingu ja allhankelepingureaga, värskendatakse üldise meeskonnaliikme rea välja **Töötaja tüüp** väärtuseks **Lepinguline töötaja** ja väärtus **Allhanke kehtivus** seatakse väärtusele **Kehtiv**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Projekti meeskonnaliikme allhange personaliga

Sarnaselt üldistele või personalita meeskonnaliikmetele saate vaadata ka projekti meeskonnaliikme allhanke võimalusi, kui meeskonnaliige on lepinguline töötaja. Selleks, et vaadata ja valida allhanke võimaluste hulgast personaliga või nimelise projektimeeskonna liikme jaoks, järgige järgmisi samme.

1. Valige üks või mitu projektimeeskonna liikme kirjet, kus ressurss on lepinguline töötaja.
2. Veenduge, et ükski valitud projektimeeskonna liikme kirjetest ei oleks juba allhankelepingu alusel sõlmitud. 
3. Valige projektimeeskonna liikmete alamruudustikus **Allhanke valikud**. Avaneb dialoog **Allhanke valikud**. 
4. Kui valisite 1. etapis ainult ühe projektimeeskonna liikme kirje, on saadaval järgmised valikud.
      - Looge uus allhankelepingu rida.
      - Reserveerige olemasoleva allhankelepingu vastu.
  Kui valisite 1. etapid mitu projektimeeskonna liikme kirjet, on ainus saadaolev võimalus luua uued allhankelepinguread.
5. Olemasoleva allhankelepingu rea alusel reserveerimise võimalus võimaldab teil valida allhankelepingu ja allhankelepingu rea, mille jaoks soovite reserveerida. Kui valite allhankelepingurea võimsuse reserveerimiseks, peaksite tagama järgmise.
      - Valitud allhankelepingu rida on ajaline. 
      - Projektimeeskonna liikmelt nõutav roll vastab rollile, mis osteti allhankelepingurealt. 
      - Hankija, kellega lepinguline töötaja on seotud, on sama, mis allhankelepingus sõlmitud hankija.
6. Kui valite projektimeeskonna liikmete jaoks uute allhankelepinguridade loomise, võimaldab süsteem teil valida allhankelepingu, mille alusel soovite need read luua. Selle valiku puhul peaksite tagama, et hankija, kellele lepinguline töötaja kuulub, on sama, mis allhankelepingu sõlminud hankija. 
7. Allhankeleping, mille valite uute ridade loomiseks, peaks olema olekus **Mustand**. Selle valikuga luua valitud projektimeeskonna liikmetele uued allhankelepinguread, loob süsteem iga projektimeeskonna liikme jaoks aja jaoks ühe allhankelepingurea. Roll, tunnid ja kuupäevad kopeeritakse projektimeeskonna liikmelt igale loodavale allhankelepingureale.  
8. Kui nimeline meeskonnaliige on seotud allhankelepingu ja allhankelepingureaga, värskendatakse nimelise meeskonnaliikme rea välja **Töötaja tüüp** väärtuseks **Lepinguline töötaja** ja väärtus **Allhanke kehtivus** seatakse väärtusele **Kehtiv**.

## <a name="re-costing-subcontractor-assignments"></a>Allhanke ülesannete kulude ümbermääramine

Kui projektimeeskonna liige (üldine või nimeline) on seotud allhankelepingu ridadega, kasutades dialoogi **Allhanke valikud**, siis kõik meeskonnaliikme ülesannetele määratud ülesanded kalkuleeritakse ümber allhankepingule lisatud ostuhinnakirja alusel. Valige vahekaardi **Prognoosid** lehel **Projekti üksikasjad** nuppu **Hindade värskendamine**, et näha allhankeotsusest tulenevat värskendatud hinnakujundust ja/või kulukalkulatsiooni.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
