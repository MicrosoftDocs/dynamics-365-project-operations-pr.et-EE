---
title: Projekti ajatabelite mobiilirakendus
description: See artikkel annab teavet mobiilirakenduse Microsoft Dynamics 365 Project Timesheet kohta. Mobiilirakendus Project Timesheet lubab kasutajatel oma mobiilsideseadmes esitada ja kinnitada projektide ajatabeleid.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110970"
---
# <a name="project-timesheet-mobile-application"></a>Projekti ajatabelite mobiilirakendus

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Ülevaade

Mobiilirakendus Microsoft Dynamics 365 Project Timesheet laseb kasutajatel oma mobiilsideseadmes esitada ja kinnitada projektide ajatabeleid (iPhone või Android). See mobiilirakendus toob esile ajatabeli funktsioonid, mis asuvad rakenduse Dynamics 365 Finance projektihalduse ja raamatupidamise alal. See aitab parandada kasutajate tootlikkust ja tõhusust ning võimaldab ka õigeaegselt sisestada ja kinnitada projekti ajatabelid.

## <a name="download-and-install-the-mobile-app"></a>Mobiilirakenduse allalaadimine ja installimine

Laadige oma seadme poest alla ja installige mobiilirakendus Microsoft Dynamics 365 Project Timesheet Androidile või iPhone’ile.

## <a name="enable-the-app"></a>Rakenduse lubamine 

Finance’is peab mobiilirakendus Project Timesheet olema lubatud. Funktsiooni lubamiseks avage **Projektihalduse ja raamatupidamise näitajad \> Ajatabelid** ja valige parameeter **Luba Microsoft Dynamics 365 Project Timesheet**.

### <a name="resolve-sign-in-issues"></a>Sisselogimisprobleemide lahendamine

**Issue:** Projekti ajatabeli mobiilirakendusse sisselogimisel saavad kasutajad tõrketeate, mis ütleb, et nad „ei pääse selle rentniku rakendusele '2bc50526-cdc3-4e36-a970-c284c34cbd6e' juurde“.

**Probleem:** Projekti ajatabeli mobiilirakendusse sisselogimisel kuvatakse tõrketeade, mis sarnaneb ühega järgmistest näidetest.

- „AADSTS50020: identiteedipakkuja 'https://sts.windows.net/[rakenduse ID]' kasutajakontot '[kasutajanimi]' ei eksisteeri rentnikus '[rentniku ID]' ja see ei pääse juurde rakendusele '[rakenduse ID]' selles rentnikus“.
- „Valitud kasutajakontot ei eksisteeri rentnikus [rentniku ID] ja see ei pääse selle rentniku rakendusele [rakenduse ID] juurde“.

**Selgitus:** Need probleemid on põhjustatud muudatusest, mis tehti Azure Active Directory (Azure AD) mais 2022 ja mis on seotud väliste kasutajatega. Kuna seda muudatust ei tehtud finants- ja äritoimingute rakendustes, võib see mõjutada kliente platvormi või rakenduse mis tahes versioonis.

**Parandus:** Kõik väliskasutajad tuleb Azure AD kaudu rentniku juurde kutsuda. Lisateabe saamiseks vaadake jaotist [Kasutajate kutsumine Azure Active Directory B2B koostööga](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Rakendusse sisse logimine

1.  Käivitage oma mobiilsideseadmes rakendus.

2.  Sisestage oma Finance’i URL.

3.  Esmakordsel sisselogimisel küsitakse teilt kasutajanime ja parooli. Sisestage oma identimisteave.

4. Teid logitakse sisse vaikeettevõttesse.

## <a name="submit-a-project-timesheet"></a>Projekti ajatabeli esitamine

Saate projekti ajatabeli luua ja esitada rakenduses. Saate uue ajatabeli luua varasema ajatabeli, salvestatud ridade ja projekti ülesannete teabe põhjal. Kui olete määratud delegaadiks, saate sisestada ka mõne teise töötaja ajatabeli. Delegaadina ajatabeli loomiseks valige nupp **Menüü** ja seejärel ressursi nimi.

Ajatabeli leht loob praeguse kuupäeva põhjal ajatabeli perioodi jaoks uue ajatabeli. Kuvatakse töönädal. Kui ajatabeli periood hõlmab mitut nädalat, saate valida vahekaardilt töönädal mõne muu töönädala.
Kui eksisteerib ajatabel praeguse kuupäeva jaoks, siis see kuvatakse. Kui peate looma erineval ajatabeli perioodil uue ajatabeli, valige nupp **Menüü** ja valige seejärel suvand **Uus ajatabel**.

Saate sisestada projekti teabe klõpsates tegevust **Lisa aega** või tegevust **Kopeeri aeg kohast**. Tegevus **Kopeeri aeg kohast** kopeerib projektirea teabe, kuid mitte tunnid. Menüü **Kopeeri aeg kohast** sisaldab järgmisi suvandeid.

- **Kopeeri olemasolevast ajatabelist** – kopeerige ajatabeli read olemasolevast ajatabelist.

- **Kopeeri lemmikutest** – looge uued ajatabeli read, kasutades lemmikutena valitud ajatabeli sätteid.

- **Kopeeri ülesandest** – looge uued ajatabeli read määratud projektidest.

Kuvatav projekti teave sõltub lehel **Projektihalduse ja raamatupidamise näitajad** määratletud mobiilsideseadmete näitajatest.

Valige väljal **Juriidiline üksus** juriidiline üksus, mille jaoks te projekti töö tegite. Väli **Juriidiline üksus** on saadaval ainult juhul, kui teie juriidilise üksuse jaoks on kontsernisisene ajatabeli tugi lubatud.

Valige klient, kes on ajatabeli projektiga seostatud. Androidi esmase versiooni puhul ei toetata kliendi sisestamist, kuna peate esmalt valima projekti. Kui valisite esmalt projekti, täidetakse väli **Klient** automaatselt.

Väljal **Projekt** valige projekt, mille kohta aega sisestate. Väli **Klient** täidetakse automaatselt.

Kliendi ja projekti otsingud võimaldavad otsida nii klientide kui ka projektide üleselt.

Valige vastavalt vajadusele teave väljadel **Kategooria**, **Tegevus**, **Rea atribuut**, **Käibemaksu rühm** ja **Eseme käibemaksu rühm**. Neid välju saab alistada.

Väli **Rea atribuut** seatakse projektihalduse ja raamatupidamise näitajate põhjal vaikeväärtusele. Kui parameetrid projekt/kategooria ja kategooria/ressurss on lubatud, seadistatakse väärtus **Rea atribuut** vaikeväärtusele, mille oolete selle valideerimise jaoks määratlenud. Kui parameetrid projekt/kategooria ja kategooria/ressurss parameetrid pole lubatud, läheb väärtus **Rea atribuut** vaikeväärtusele vastavalt väljale **Luba vaikerea atribuut** lehel **Projektihalduse ja raamatupidamise parameetrid**. Väärtu **Rea atribuut** on võimalik alistada.

Valige kellaaja lisamiseks päev. Sisestage iga päev töötatud tundide arv.

Sisestatud tundide kohta kommentaaride lisamiseks klõpsake nuppu **Lisa kommentaarid** ja seejärel sisestage sisemine publik, kliendi publik või mõlemad.
Projektihaldurid saavad sisemisi kommentaare vaadata. Klientide märkused lisatakse arvetele.

Rea lemmikuna salvestamiseks valige märkeruut ja klõpsake seejärel valikut **Salvesta lemmikuks**.

Mobiilirakenduses ei pakuta rahalist dimensioone ega manuste tuge.

Jätkake projektiridade vastavalt vajadusele lisamist, et ajatabeli lõpule viia.

Ajatabeli kinnitamise töövoogu saatmiseks klõpsake nuppu **Esita**.

## <a name="review-timesheets"></a>Ajatabelite läbivaatamine

Läbivaatamist vajavate ajatabelite loend on saadaval menüüs. See suvand on saadaval ainult juhul, kui olete määratud töövoo kinnitajaks. Toetatud on nii päise kui ka rea kinnitamine. Rea tasemel kinnitamine võimaldab märkida kinnitamiseks ühe või mitu. Pärast ajatabeli teabe läbivaatamist töövoo jätkamiseks klõpsake käsku **Kinnita**, **Delegeeri** või **Naase**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
