---
title: Integreerimise tööleht rakenduses Project Operations
description: See teema sisaldab teavet integreerimise töölehega töötamise kohta rakenduses Project Operations.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5e1a455d055fe562a1946cc3b90c8274ef1a4b12
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582429"
---
# <a name="integration-journal-in-project-operations"></a>Integreerimise tööleht rakenduses Project Operations

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Aja- ja kulukirjed loovad **tegelikud** tehingud, mis esindavad projektiga seoses lõpule viidud töö toiminguvaadet. Dynamics 365 Project Operations pakub raamatupidajatele tööriista, et vaadata tehinguid ja muuta vastavalt vajadusele raamatupidamise atribuute. Pärast läbivaatamise ja korrigeerimise lõpetamist sisestatakse kanded projekti alammoodulisse ja pearaamatusse. Raamatupidaja saab neid toiminguid teha projektitoimingute integreerimise töölehel(Dynamics 365 Finance Projektihaldus- ja raamatupidamisžurnaalid **Projektioperatsioonide** integreerimine **.** > **·** > **·** > **·**

![Integreerimise töölehe voog.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Kirjete loomine Project Operationsi integreerimise töölehel

Project Operationsi integreerimise töölehe kirjed luuakse kasutades perioodilist protsessi **Koondtabelist importimine**. Seda protsessi saate käivitada **, minnes Dynamics 365 Finance** > **Projektihaldus ja raamatupidamine** > **Perioodiliste** > **projektitoimingute integreerimise** > **import lavastustabelist**. Saate vastavalt vajadusele käivitada toimingu interaktiivselt või konfigureerida protsessi töötama taustal.

Kui perioodiline protsess töötab, leitakse kõik tegelikud näitajad, mis ei ole veel Project Operationsi integreerimise töölehele lisatud. Luuakse iga tegeiku tehingu töölehe rida.
Süsteem rühmitab žurnaaliread eraldi töölehtedeks, lähtudes väljal Projektitoimingute integreerimise tööleht väljal Perioodi üksus valitud **väärtusest (** Finantsprojekti **haldus ja raamatupidamine** > **Setup** > **Project management and accounting parameters** > **,** Project Operations on Dynamics 365 Customer Engagement **).** Selle välja võimalikud väärtused on hõlmavad.

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
    - Kui **kategooria** Kanne pole projekti tegelikus komplektis määratud, kasutab süsteem lehe Projektihaldus- ja raamatupidamisparameetrite **vahekaardi** Projektitoimingud **Dynamics 365 Customer Engagement** välja **Projekti kategooria vaikesätted olevat väärtust**.
  - Väli **Ressurss** näitab selle tehinguga seotud projekti ressurssi. Ressurssi kasutatakse kliendile tehtavates projekti arve ettepanekutes viitena.
  - Valuutakursi **·** **väli on vaikimisi Dynamics 365 Finance. aastal määratud valuutakursilt**. Kui vahetuskursi seadistus puudub, ei lisa **koondtabelist importimise** perioodiline protsess töölehele kirjet ja töö täitmise logisse lisatakse tõrketeade.
  - Väli **Rea atribuut** tähistab projekti tegelike näitajate arve tüüpi. Rea atribuut ja arveldustüübi vastendamine on määratletud **lehe Projektihaldus- ja raamatupidamisparameetrite vahekaardil** Projektitoimingud **Dynamics 365 Customer Engagement**.

Rakenduse Project Operations integreerimise töölehe ridadel saab värskendada ainult järgmisi raamatupidamise atribuute:

- **Arveldue käibemaksu rühm** ja **Arveldamise üksuse käibemaksu rühm**
- **Finantsilised dimensioonid** (toimingu **Hajuta summasid** kasutamine)

Integreerimise töölehe ridasid saab kustutada, kuid kõik konteerimata read lisatakse pärast perioodilisse protsessi **Koondtabelist importimine** naasmist uuesti töölehele.

Integreerimise töölehe postitamisel luuakse projekti alammooduli ja pearaamatu tehingud. Neid kasutatakse allavooli kliendi arveldamises, tulu kajastamises ja finantsaruandluses.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
