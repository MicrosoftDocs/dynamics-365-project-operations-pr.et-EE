---
title: Integreerimise tööleht rakenduses Project Operations
description: See teema sisaldab teavet integreerimise töölehega töötamise kohta rakenduses Project Operations.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c5cc3254c52750b35be2c66137b6c57bbd9acbfbc89dedc6559059a89c8e2393
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987926"
---
# <a name="integration-journal-in-project-operations"></a>Integreerimise tööleht rakenduses Project Operations

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Aja- ja kulukirjed loovad **tegelikud** tehingud, mis esindavad projektiga seoses lõpule viidud töö toiminguvaadet. Dynamics 365 Project Operations pakub raamatupidajatele tööriista, et vaadata tehinguid ja muuta vastavalt vajadusele raamatupidamise atribuute. Pärast läbivaatamise ja korrigeerimise lõpetamist sisestatakse kanded projekti alammoodulisse ja pearaamatusse. Raamatupidaja saab teha need toimingud kasutades töölehte **Project Operationsi integreerimine** suvandis **Dynamics 365 Finance** > **Projektihaldus ja raamatupidamine** > **Töölehed** >  tööleht **Project Operationsi integreerimine**.

![Integreerimise töölehe voog.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Kirjete loomine Project Operationsi integreerimise töölehel

Project Operationsi integreerimise töölehe kirjed luuakse kasutades perioodilist protsessi **Koondtabelist importimine**. Saate selle protsessi käivitada, kui avate **Dynamics 365 Finance** > **Projektihaldus ja raamatupidamine** > **Perioodiline** > **Project Operationsi integreerimine** > **Koondtabelist importimine**. Saate vastavalt vajadusele käivitada toimingu interaktiivselt või konfigureerida protsessi töötama taustal.

Kui perioodiline protsess töötab, leitakse kõik tegelikud näitajad, mis ei ole veel Project Operationsi integreerimise töölehele lisatud. Luuakse iga tegeiku tehingu töölehe rida.
Süsteem rühmitab töölehe read eraldi töölehtedeks vastavalt väljal **Project Operationsi integreerimise töölehe perioodi ühik** valitud väärtusele (**Finance** > **Projektihaldus ja raamatupidamine** > **Seadistus** > **Projektihalduse ja raamatupidamise parameetrid**, vahekaart **Project Operations teenuses Dynamics 365 Customer Engagement**). Selle välja võimalikud väärtused on hõlmavad.

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
    - Kui **Kande kategooria** pole projekti tegelikes näitajates määratud, kasutab süsteem välja **Projekti kategooria vaikeväärtused** väärtust vahekaardil **Project Operations teenuses Dynamics 365 Customer Engagement** lehel **Projektihalduse ja raamatupidamise parameetrid**.
  - Väli **Ressurss** näitab selle tehinguga seotud projekti ressurssi. Ressurssi kasutatakse kliendile tehtavates projekti arve ettepanekutes viitena.
  - Välja **Vahetuskurss** vaikeväärtus pärineb suvandist **Valuuta vahetuskurss**, mis on määratud rakenduses Dynamics 365 Finance. Kui vahetuskursi seadistus puudub, ei lisa **koondtabelist importimise** perioodiline protsess töölehele kirjet ja töö täitmise logisse lisatakse tõrketeade.
  - Väli **Rea atribuut** tähistab projekti tegelike näitajate arve tüüpi. Rea atribuudi ja arve tüübi vastendamine on määratletud vahekaardil **Project Operations teenuses Dynamics 365 Customer Engagement** lehel **Projektihaldus ja raamatupidamise parameetrid**.

Rakenduse Project Operations integreerimise töölehe ridadel saab värskendada ainult järgmisi raamatupidamise atribuute:

- **Arveldue käibemaksu rühm** ja **Arveldamise üksuse käibemaksu rühm**
- **Finantsilised dimensioonid** (toimingu **Hajuta summasid** kasutamine)

Integreerimise töölehe ridasid saab kustutada, kuid kõik konteerimata read lisatakse pärast perioodilisse protsessi **Koondtabelist importimine** naasmist uuesti töölehele.

Integreerimise töölehe postitamisel luuakse projekti alammooduli ja pearaamatu tehingud. Neid kasutatakse allavooli kliendi arveldamises, tulu kajastamises ja finantsaruandluses.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
