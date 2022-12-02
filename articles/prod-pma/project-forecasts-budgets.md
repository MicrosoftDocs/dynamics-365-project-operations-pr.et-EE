---
title: Projekti prognoosid ja eelarved
description: Rakendus Microsoft Dynamics 365 Finance pakub projekti prognoose ja eelarveid teie projektide haldamiseks ja juhtimiseks.
author: Yowelle
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15731010877b5d62329867e878f624149e74f761
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684545"
---
# <a name="project-forecasts-and-budgets"></a>Projekti prognoosid ja eelarved

[!include [banner](../includes/banner.md)]

Projektide haldamiseks ja juhtimiseks on kaks viisi: prognoosid ja eelarved. 

Kasutage projekti prognoosimist, kui teie organisatsioon lähtub toimimise seisukahas ja kui see keskendub konkreetsest kandest pärinevatele tuludele ja kuludele. Kasutage projekti eelarve kavandamist, kui teie organisatsioon keskendub rohkem rahalistele summadele. 

Nii projekti prognoosid kui ka projekti eelarved kasutavad projitseeritud kandesummade jaoks prognoosi mudeleid. 

Igal meetodil on omad eelised. Enne oma organisatsiooni jaoks meetodi valimist peaksite kaaluma järgmisi aspekte.

|   Eraldamismeetod       |           Projekti prognoosimine            |        Projekti eelarve koostamine                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Perioodi jaotumine**     | Te ei saa kandeid tehinguid otse fiskaalperioodi ajale. Selle asemel põhinevad prognoos ja prognoosi juhtimine projekti elueal. Kuna prognoosid põhinevad kindlal kuupäeval, peate tuletama perioodi alates teatud kuupäevast. | Te saate määrata kandeid terve projekti või fiskaalperioodi üleselt. Kui jaotate perioodi üleselt, saate kasutamata summad viia üle järgmisele fiskaalperioodile. |
| **Kannete vaatamine**  | Saate vaadata kandeid prognoosi vormides, kus näete kogu ettevõtte ja kõigi projektide prognoose, olenemata hierarhiast. Kindlale projektile keskendumiseks peate andmeid filtreerima.                                       | Saate vaadata ühe projekti hierarhia eelarvelisi kandeid. Seega saate vaadata peamise projekti või selle allprojektide kandeid.                 |
| **Kande muutujad** | Prognoosi kannete sisestamisel saate kasutada iga atribuuti, mis tegeliku kande jaoks eksisteerivad. See muudab prognoosi veelgi üksikasjalikumaks. Näiteks saate sisestada koguse, töötajate, üksuste või rea atribuutide üksikasjad.         | Eelarve üksikasjade sisestamisel saate kasutada ainult summasid, kategooriaid ja tegevusi.                    |
| **Turvalisus**              | Prognoosimine põhineb kannetel, mille prognoosi vormidele sisestasite ja see ei hõlma protsessi kontrollimise mehhanismi. Kõik töötajad, kellel on prognoosi vormi õigused, saavad teavet ilma kinnitamata läbi vaadata.                                        | Eelarve koostamine kasutab töövoo süsteemi, mis lubab muuta haldust ja võimaldab teil hoida läbivaatuste ajalugu.         |
| **Sisestuse tüübid**           | Prognoosi kande kirjed põhinevad mitmetel üksustel ning kulu- ja müügihindadel.  | Eelarve üksikasjad põhinevad summadel, mis on jaotatud kulude ja tulude vahel.                                          |
| **Prognoosi mudelid**       | Kuna iga prognoos tuleb seostada mudeliga, saate luua mitu prognoosimudelit ja seadistada ka allmudeleid.           | Projekti eelarve koostamine piirab prognoosimudeleid, mida eelarve koostamiseks kasutatakse. Väiksem prognoosimudelite hulk võib aidata suurendada prognooside järjepidevust.                           |
| **Kulude ületamised**         | Saate ainult lubada või keelata kannete olemi, mis põhjustab kulu ületamise.   | Projekti eelarve koostamine pakub kasutajatele täiendavaid juhtimisvõimalusi. Saate hoiatused ja ületamised lubada.                    |
| **Juhtelement**               | Prognoosi juhtimine tehakse prognoosi vähendamist kasutades. Tegelikud summad lahutatakse prognoosi tehingu saldodest ilma ühegi auditeerimise jäljeta. See võib muuta tegelike kannete esinemise jälgimise veelgi keerulisemaks .                   | Projekti eelarve kontrollimisel lahutatakse tegelikud summad järelejäänud eelarve summadest. See võimaldab selgemat auditeerimise jälge..                                   |

## <a name="project-forecasts"></a>Projekti prognoosid
Projekti prognoosimise kasutamisel saate sisestada prognoosi kanded prognoosi vormidel iga kandetüübi jaoks. Kõiki atribuute, mis on tegeliku kande jaoks saadaval, saab kasutada prognoosi kandeks (nt rea tasuvus, rea atribuudid, töötajad või kirjeldused). Samuti saate määrata, kui kaua pärast kulu esinemist te kliendile arve esitate. 

Projekti prognoosimise kanded põhinevad ühikutel ja summadel. 

Peate seostama iga projekti prognoosi prognoosimudeliga. Prognoosi tehingu sisestamisel soovitatakse prognoosimudel automaatselt. Prognoosimudel toimib prognoosi kannete puhul ümbrisena. 

Saate määrata mudeli puhul prognoosimudelid alammudelitena. Nii saate prognoosida regiooni, ajavahemiku või osakonna järgi. Saate uue mudeli loomiseks kopeerida prognoosi kanded mudelisse ja saate ka edastada kanded pearaamatusse. Kuna prognoosi ja mudeli vahel puudub üks-ühele seos, siis igal prognoosimismudel moodustab projekti jaoks eraldi eelarve. 

Prognoosimudelid saavad projektide kontrollmehhanismina kasutada prognoosi vähendamist. Prognoosi vähendamisel vähendavad tegelikud kanded prognoosi kande saldot. Samas kuna prognoosi vähendamist rakendatakse hierarhias kõrgeimale projektile, pakub see prognoosis muudatuste piiratud vaadet. Näiteks kui töötaja on seostatud allprojektiga, sisestatakse töötaja tegelikud kanded peamisesse projekti. See võib muuta muudatuste jälgimise keeruliseks, kuna te ei saa hõlpsasti määratleda, milline tehing millises alamprojektis põhjustas prognoositud summa vähendamise. Seetõttu on hea mõte prognoosi vähendamise poolt kasutamiseks luua prognoosimudeli koopia. Seejärel saate kasutada aruannet, et näha, mis prognoositi algselt. 

Saate projekti prognoose vaadata läbi, kopeerida, kustutada või edastada pearaamatu eelarvele. Samas protsessi ei saa kontrollida. Kõik töötajad, kellel on prognoosi vormi õigus, saavad teha muudatusi ilma läbi vaatamata.

-   **Muutmine** – saate muuta prognoosikannet samadel vormidel, kus algsed kanded tehti.
-   **Kopeerimine või kustutamine** – prognoosi kannete kopeerimisel kopeerite ühe prognoosimudeli kannete read teisse prognoosimudelisse. Kui te prognoosi kustutate, siis te kustutate prognoosi kanded prognoosimudelist. Kopeeritud või kustutatud prognoosi kannete piiramiseks valige konkreetsed kandetüübid ja kuupäevad. See võimaldab teil kopeerida või kustutada ainult prognoosi konkreetsed osad.
-   **Edastamine** – kui edastate projekti prognoosi pearaamatu eelarvesse, siis edastate prognoosimudeli prognoosi kanded pearaamatu eelarvesse. Saate kirjutada pearaamatu eelarves üle kõik eelnevalt edastatud kanded, kuhu oma projekti prognoosid edastate.

## <a name="project-budgets"></a>Projekti eelarved
Projekti eelarve koostamine on prognoosimisest lihtsam meetod, kuigi see integreerib prognoosimudelitega. See kasutab algsete eelarve üksikasjade ja läbivaatamiste jaoks ühe kirje vormi ja võimaldab projitseerimisi, mis põhinevad ainult summal, kategoorial või tegevusel. 

Projekti eelarve koostamisel tuleb kõik algsed eelarved ja läbivaatused saata heakskiitmiseks projekti töövoogu. Töövood annavad teile protsessi üle suurema kontrolli ja loovad muudatuste ajaloo kirje. 

Projekti eelarve koostamine sarnaneb pearaamatu eelarve koostamisele, kuid see on kiirem ja seda on hõlpsam seadistada. Paljusid pearaamatu eelarve koostamise valikuid (nt numbri järjestused või valuuta) ei ole vaja projektide jaoks eraldi häälestada.

Projekti eelarved seostatakse automaatselt kahe prognoosimudeliga, ühe algse eelarve ja ühe järelejäänud eelarvega. Seega saavad prognoosimudelitel põhinevad aruanded kasutada eelarve teavet. Kui projekti eelarve on kindlaks määratud, loob süsteem seotud mudelite põhjal prognoosi kanded, mida kasutatakse aruandluse ja kontrolli eesmärkidel.

## <a name="forecast-models"></a>Prognoosimudelid
Prognoosimudelitel on ühe kihiga hierarhia. See tähendab, et üks projekti prognoos tuleb seostada ühe prognoosimudeliga.

Kui kasutate projekti prognoosimist, saate määratleda mudelid allmudelitena. Seejärel saate luua prognoosid osakonna, ajavahemiku või regiooni põhjal. Näiteks saate luua aastaks prognoosimudeli ja seejärel luua allmudeleid kirde-, kagu-, loode- ja edela-piirkonna prognooside jaoks, mille esitavad piirkondlikud juhid. Kui valite saadaolevates aruannetes erinevad suvandid, saate vaadata teavet kogu prognoosi või allmudeli järgi.





[!INCLUDE[footer-include](../includes/footer-banner.md)]