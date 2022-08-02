---
title: Integreerimise tööleht rakenduses Project Operations
description: Sellest artiklist leiate teavet Project Operationsi integratsiooni töölehega töötamise kohta.
author: sigitac
ms.date: 06/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d6f1709c4bf44cfd45516d9ac74b30d4817bb653
ms.sourcegitcommit: a5a1d81d2fe0a6f684e79859fcddf45e913d76bc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9106270"
---
# <a name="integration-journal-in-project-operations"></a>Integreerimise tööleht rakenduses Project Operations

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Aja-, kulu-, tasu- ja materjalikirjed loovad **tegelikud** kanded, mis esindavad projekti suhtes tehtud töö operatiivvaadet. Dynamics 365 Project Operations pakub raamatupidajatele tööriista, et vaadata tehinguid ja muuta vastavalt vajadusele raamatupidamise atribuute. Pärast läbivaatamise ja korrigeerimise lõpetamist sisestatakse kanded projekti alammoodulisse ja pearaamatusse. Raamatupidaja saab neid toiminguid teha, kasutades **projektioperatsioonide integreerimise** töölehte (**Dynamics 365 Finance** > **Projektihalduse ja raamatupidamise** > **töölehed** > **Projektitoimingute integreerimine** tööleht.

![Integreerimise töölehe voog.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Kirjete loomine Project Operationsi integreerimise töölehel

Project Operationsi integreerimise töölehe kirjed luuakse kasutades perioodilist protsessi **Koondtabelist importimine**. Selle protsessi **käivitamiseks avage jaotis Dynamics 365 Finance** > **Projektihaldus ja raamatupidamine** > **Perioodiliste** > **projektitoimingute integreerimine** > **Import koondamistabelist**. Saate vastavalt vajadusele käivitada toimingu interaktiivselt või konfigureerida protsessi töötama taustal.

Kui perioodiline protsess töötab, leitakse kõik tegelikud näitajad, mis ei ole veel Project Operationsi integreerimise töölehele lisatud. Luuakse iga tegeiku tehingu töölehe rida.
Süsteem rühmitab töölehe read eraldi töölehtedeks, lähtudes väärtusest, mis on valitud **väljal Perioodiüksus väljal Project Operations Integration** (**Projektihalduse** > **ja raamatupidamise** > **finantseerimine** > **Seadistamine Projektihaldus ja raamatupidamise parameetrid**, **vahekaardil Project Operations on Dynamics 365 Customer Engagement**). Selle välja võimalikud väärtused on hõlmavad.

  - **Päevad**: tegelikud näitajad rühmitatakse tehingu kuupäeva järgi. Iga päeva jaoks luuakse eraldi tööleht.
  - **Kuud**: tegelikud näitajad on rühmitatud kalendrikuu järgi. Iga kuu jaoks luuakse eraldi tööleht.
  - **Aastad**: tegelikud näitajad on rühmitatud kalendriaasta järgi. Iga aasta jaoks luuakse eraldi tööleht.
  - **Kõik**: kõik tegelikud tehingud lisatakse samale integreerimise töölehele. Kui tööleht ei ole perioodilise protsessi töötamise ajal saadaval, näiteks kui tööleht on tehingute postitamise protsessis, luuakse uus tööleht.

Tööleh read luuakse vastavalt projekti tegelikele näitajatele. Järgnev loend sisaldab osasid olulisemaid vaike -ja teisendusreegleid.

  - Iga projekti tegelikul tehingul on Project Operationsi integratsiooni töölehel rida. Aja- ja materjali arveldustüübi kulu ja arveldamata müügitehingud on näidatud eraldi ridadel.
  - Väli **Kuupäev** tähistab tehingu kuupäeva. Väli **Raamatupidamise kuupäev** tähistab kuupäeva, mil kanne pearaamatusse kantakse. Kui raamatupidamise kuupäev on [suletud eelarveperioodil](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) ja parameeter **Määra raamatupidamise kuupäev automaatselt avatud eelarveperioodile** on määratud vahekaardil **Finantsteenused** lehel **Projektihalduse ja raamatupidamise parameetrid**, määrab süsteem tehingu raamatupidamise kuupäeva järgmise avatud eelarveperioodi esimesele kuupäevale.
  - Väli **Kanne** näitab iga tegeliku tehingu kande numbrit. Kande numbri järjestuse määratleb vahekaart **Numbriseeriad** lehel **Projektihalduse ja raamatupidamise parameetrid**. Igale reale määratakse uus number. Pärast kande sisestamist saate vaadata, kuidas kulu- ja arveldamata müügitehingud on seotud, valided lehel **Kande tehingud** suvandi **Seotud kanded**.
  - Väli **Kategooria** näitab seotud projekti tegelike näitajate tehingu kategooriate põhjal projekti tehingut ja vaikeväärtusi.
    - Kui **Tehingu kategooria** on projekti tegelikes näitajates määratud ja seotud **Projekti kategooria** on kindlas juriidilises olemis olemas, on kategooria vaikeväärtuseks see projekti kategooria.
    - Kui **kandekategooria** pole tegelikus projektis määratud, kasutab süsteem väärtust väljal **Projektikategooria vaikeväärtused** **vahekaardil** Projektitoimingud Dynamics 365 Customer Engagement **lehel Projektihalduse ja raamatupidamise parameetrid**.
  - Väli **Ressurss** näitab selle tehinguga seotud projekti ressurssi. Ressurssi kasutatakse kliendile tehtavates projekti arve ettepanekutes viitena.
  - Väli **Vahetuskurss** vaikeväärtuseks **on Dynamics 365 Finance määratud valuutakurss**. Kui vahetuskursi seadistus puudub, ei lisa **koondtabelist importimise** perioodiline protsess töölehele kirjet ja töö täitmise logisse lisatakse tõrketeade.
  - Väli **Rea atribuut** tähistab projekti tegelike näitajate arve tüüpi. Reaatribuudi ja arveldustüübi vastendamine on määratletud **vahekaardil** Projektitoimingud Dynamics 365 Customer Engagement **lehel Projektihaldus ja raamatupidamise parameetrid**.

Rakenduse Project Operations integreerimise töölehe ridadel saab värskendada ainult järgmisi raamatupidamise atribuute:

- **Arveldue käibemaksu rühm** ja **Arveldamise üksuse käibemaksu rühm**
- **Finantsilised dimensioonid** (toimingu **Hajuta summasid** kasutamine)

Integratsiooni töölehe ridu saab kustutada. Kuid kõik sisestamata read sisestatakse töölehele uuesti pärast perioodilise protsessi Impordi koondamisest **uuesti käivitamist**.

### <a name="post-the-project-operations-integration-journal"></a>Project Operationsi integratsiooni töölehe sisestamine

Integreerimise töölehe postitamisel luuakse projekti alammooduli ja pearaamatu tehingud. Neid kasutatakse allavooli kliendi arveldamises, tulu kajastamises ja finantsaruandluses.

Valitud Project Operationsi integratsioonitöölehe saab sisestada, kasutades **lehte Postita** Project Operationsi integratsioonitöölehel. Kõiki töölehti saab automaatselt sisestada, käivitades protsessi periodics **Project Operations integration** > **Post Project Operations integratsiooni töölehel** > **·**.

Postitamist saab teha interaktiivselt või partiina. Pange tähele, et kõik töölehed, millel on rohkem kui 100 rida, sisestatakse automaatselt partiisse. Parema jõudluse tagamiseks, kui töölehed, millel on palju ridu, sisestatakse paketti, lubage **tööruumis** Funktsioonihaldus mitme pakett-ülesande **funktsiooni abil integreerimistööleht Projektitoimingute postitamine**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Kõigi sisestusvigadega ridade ülekandmine uude töölehele

> [!NOTE]
> Selle võimaluse kasutamiseks lubage **tööruumis** Funktsioonihaldus **funktsioon Edasta kõik sisestusvigadega read uude Project Operationsi integratsioonitöölehele**.

Project Operationsi integratsioonitöölehele sisestamise ajal valideerib süsteem töölehe iga rea. Süsteem sisestab kõik read, millel pole tõrkeid, ja loob uue töölehe kõigile ridadele, millel on sisestusvigu. Sisestamise tõrkeridadega töölehtede ülevaatamiseks **avage Project management and accounting** > **Journals** > **Project Operations integratsioonitööleht** ja filtreerige töölehed välja Algne tööleht **abil**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
