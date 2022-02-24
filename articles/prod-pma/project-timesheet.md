---
title: Projekti ajatabelite mobiilirakendus
description: Selles teemas on toodud mobiilirakenduse Microsoft Dynamics 365 Project Timesheet teave. Mobiilirakendus Project Timesheet lubab kasutajatel oma mobiilsideseadmes esitada ja kinnitada projektide ajatabeleid.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b9cbd84ecb0d71a99982e158d7e0ea1e236fb369
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075129"
---
# <a name="project-timesheet-mobile-application"></a>Projekti ajatabelite mobiilirakendus

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Ülevaade

Mobiilirakendus Microsoft Dynamics 365 Project Timesheet lubab kasutajatel oma mobiilsideseadmes esitada ja kinnitada projektide ajatabeleid (iPhone või Android). See mobiilirakendus esitab ajatabeli funktsiooni, mis sisaldub rakenduse Dynamics 365 Finance alas Projektihaldus ja raamatupidamine, mis parandab kasutajate jõudlust ja tõhusust ning lubab ajamahukaid projekti ajatabelite õigeaegset sisestamist ja heakskiitu.

## <a name="download-and-install-the-mobile-app"></a>Mobiilirakenduse allalaadimine ja installimine

Laadige oma seadme poest alla ja installige mobiilirakendus Microsoft Dynamics 365 Project Timesheet Androidile või iPhone’ile.

## <a name="enable-the-app"></a>Rakenduse lubamine 

Finance’is peab mobiilirakendus Project Timesheet olema lubatud. Funktsiooni lubamiseks avage **Projektihalduse ja raamatupidamise näitajad \> Ajatabelid** ja valige parameeter **Luba Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Rakendusse sisse logimine

1.  Käivitage oma mobiilsideseadmes rakendus.

2.  Sisestage oma Finance’i URL.

3.  Esmakordsel sisselogimisel küsitakse teilt kasutajanime ja parooli. Sisestage oma identimisteave.

4.  Teid logitakse vaikimisi kasutatavasse ettevõttesse sisse.

## <a name="submit-a-project-timesheet"></a>Projekti ajatabeli esitamine

Saate projekti ajatabeli luua ja esitada rakenduses. Saate uue ajatabeli luua varasema ajatabeli, salvestatud ridade ja projekti ülesannete teabe põhjal. Kui olete määratud delegaadiks, saate sisestada ka mõne muu töötaja ajatabeli. Ajatabeli delegaadina loomiseks valige nupp **Menüü** ja valige seejärel ressursi nimi.

Ajatabeli leht loob praeguse kuupäeva põhjal ajatabeli perioodi jaoks uue ajatabeli. Kuvatakse töönädal. Kui ajatabeli periood hõlmab mitut nädalat, saate valida vahekaardilt töönädal mõne muu töönädala.
Kui eksisteerib ajatabel praeguse kuupäeva jaoks, siis see kuvatakse. Kui peate looma erineval ajatabeli perioodil uue ajatabeli, valige nupp **Menüü** ja valige seejärel suvand **Uus ajatabel**.

Saate sisestada projekti teabe klõpsates tegevust **Lisa aega** või tegevust **Kopeeri aeg kohast**. Tegevus **Kopeeri aeg kohast** kopeerib projektirea teabe, kuid mitte tunnid. Menüü **Kopeeri aeg kohast** sisaldab järgmisi suvandeid.

- **Kopeeri olemasolevast ajatabelist** – kopeerige ajatabeli read olemasolevast ajatabelist.

- **Kopeeri lemmikutest** – looge uued ajatabeli read, kasutades lemmikutena valitud ajatabeli sätteid.

- **Kopeeri ülesandest** – looge uued ajatabeli read määratud projektidest.

Kuvatav projekti teave sõltub lehel **Projektihalduse ja raamatupidamise näitajad** määratletud mobiilsideseadmete näitajatest.

Valige väljal **Juriidiline üksus** juriidiline üksus, mille jaoks te projekti töö tegite. Väli **Juriidiline üksus** on saadaval ainult juhul, kui teie juriidilise üksuse jaoks on kontsernisisene ajatabeli tugi lubatud.

Valige klient, kes on ajatabeli projektiga seostatud. Androidi algse väljaande jaoks ei ole kliendipoolne olem toetatud, kuna te peate kõigepealt valima projekti. Kui valisite esmalt projekti, täidetakse väli **Klient** automaatselt.

Väljal **Projekt** valige projekt, mille kohta aega sisestate. Väli **Klient** täidetakse automaatselt.

Kliendi ja projekti otsingud võimaldavad otsida nii klientide kui ka projektide üleselt.

Valige vastavalt vajadusele teave väljadel **Kategooria**, **Tegevus**, **Rea atribuut**, **Käibemaksu rühm** ja **Eseme käibemaksu rühm**. Neid välju saab alistada.

Väli **Rea atribuut** seatakse projektihalduse ja raamatupidamise näitajate põhjal vaikeväärtusele. Kui parameetrid projekt/kategooria ja kategooria/ressurss on lubatud, seadistatakse väärtus **Rea atribuut** vaikeväärtusele, mille oolete selle valideerimise jaoks määratlenud. Kui parameetrid projekt/kategooria ja kategooria/ressurss parameetrid pole lubatud, läheb väärtus **Rea atribuut** vaikeväärtusele vastavalt väljale **Luba rea vaikeatribuut** lehel **Projektihalduse ja raamatupidamise parameetrid**. Väärtu **Rea atribuut** on võimalik alistada.

Valige kellaaja lisamiseks päev. Sisestage iga päev töötatud tundide arv.

Sisestatud tundide kohta kommentaaride lisamiseks klõpsake nuppu **Lisa kommentaarid** ja seejärel sisestage sisemine publik, kliendi publik või mõlemad.
Projektihaldurid saavad sisemisi kommentaare vaadata. Klientide märkused lisatakse arvetele.

Rea lemmikuna salvestamiseks valige märkeruut ja klõpsake seejärel valikut **Salvesta lemmikuks**.

Finantsiline mõõde ja manuste tuge mobiilirakendustes ei pakuta.

Jätkake projektiridade vastavalt vajadusele lisamist, et ajatabeli lõpule viia.

Ajatabeli kinnitamise töövoogu saatmiseks klõpsake nuppu **Esita**.

## <a name="review-timesheets"></a>Ajatabelite läbivaatamine

Läbivaatamist vajavate ajatabelite loend on kättesaadav menüüs. See suvand on saadaval ainult juhul, kui olete määratud töövoo kinnitajaks. Toetatud on nii päise kui ka rea kinnitamine. Rea tasemel kinnitamine võimaldab märkida kinnitamiseks ühe või mitu. Pärast ajatabeli teabe läbivaatamist töövoo jätkamiseks klõpsake käsku **Kinnita**, **Delegeeri** või **Naase**.
