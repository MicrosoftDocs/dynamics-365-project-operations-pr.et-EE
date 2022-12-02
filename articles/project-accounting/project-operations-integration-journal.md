---
title: Integreerimise tööleht rakenduses Project Operations
description: See artikkel annab teavet integreerimise töölehega töötamise kohta rakenduses Project Operations.
author: sigitac
ms.date: 09/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e947fe895a1caa9c9ea092597957a859cd8d61c9
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541072"
---
# <a name="integration-journal-in-project-operations"></a>Integreerimise tööleht rakenduses Project Operations

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Aja-, kulu-, tasu- ja materjalikirjed loovad **Tegeliku näitaja** tehingud, mis esindavad projektiga seoses lõpule viidud töö toiminguvaadet. Dynamics 365 Project Operations pakub raamatupidajatele tööriista, et vaadata tehinguid ja muuta vastavalt vajadusele raamatupidamise atribuute. Pärast läbivaatamise ja korrigeerimise lõpetamist sisestatakse kanded projekti alammoodulisse ja pearaamatusse. Raamatupidaja saab teha need toimingud kasutades töölehte **Project Operationsi integreerimine** suvandis (**Dynamics 365 Finance** > **Projektihaldus ja raamatupidamine** > **Töölehed** > **Project Operationsi integreerimine**.

![Integreerimise töölehe voog.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Kirjete loomine Project Operationsi integreerimise töölehel

Project Operationsi integreerimise töölehe kirjed luuakse kasutades perioodilist protsessi **Koondtabelist importimine**. Saate selle protsessi käivitada, kui avate **Dynamics 365 Finance** > **Projektihaldus ja raamatupidamine** > **Perioodiline** > **Project Operationsi integreerimine** > **Koondtabelist importimine**. Saate vastavalt vajadusele käivitada toimingu interaktiivselt või konfigureerida protsessi töötama taustal.

Kui perioodiline protsess töötab, leitakse kõik tegelikud näitajad, mis ei ole veel Project Operationsi integreerimise töölehele lisatud. Luuakse iga tegeiku tehingu töölehe rida.
Süsteem rühmitab töölehe read eraldi töölehtedeks vastavalt väljal **Project Operationsi integreerimise töölehe perioodi ühik** valitud väärtusele (**Finance** > **Projektihaldus ja raamatupidamine** > **Seadistus** > **Projektihalduse ja raamatupidamise parameetrid**, vahekaart **Project Operations rakenduses Dynamics 365 Customer Engagement**). Selle välja võimalikud väärtused on hõlmavad.

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
    - Kui **Kande kategooria** pole projekti tegelikes näitajates määratud, kasutab süsteem välja **Projekti kategooria vaikeväärtused** väärtust vahekaardil **Project Operations rakenduses Dynamics 365 Customer Engagement** lehel **Projektihalduse ja raamatupidamisparameetrid**.
  - Väli **Ressurss** näitab selle tehinguga seotud projekti ressurssi. Ressurssi kasutatakse kliendile tehtavates projekti arve ettepanekutes viitena.
  - Välja **Vahetuskurss** vaikeväärtus pärineb suvandist **Valuuta vahetuskurss**, mis on määratud rakenduses Dynamics 365 Finance. Kui vahetuskursi seadistus puudub, ei lisa **koondtabelist importimise** perioodiline protsess töölehele kirjet ja töö täitmise logisse lisatakse tõrketeade.
  - Väli **Rea atribuut** tähistab projekti tegelike näitajate arve tüüpi. Rea atribuutide ja arveldustüübi vastendamine on määratletud **Project Operations rakenduses Dynamics 365 Customer Engagement** leheküljel **Projektihaldus ja raamatupidamisparameetrid**.

Rakenduse Project Operations integreerimise töölehe ridadel saab värskendada ainult järgmisi raamatupidamise atribuute:

- **Arveldue käibemaksu rühm** ja **Arveldamise üksuse käibemaksu rühm**
- **Finantsilised dimensioonid** (toimingu **Hajuta summasid** kasutamine)

Integratsiooni töölehele kandmiseid saab kustutada. Kuid kõik postitamata read lisatakse pärast perioodilisse protsessi **Koondtabelist importimine** naasmist uuesti töölehele.

### <a name="post-the-project-operations-integration-journal"></a>Rakenduse Project Operations integreerimise töölehe postitamine

Integreerimise töölehe postitamisel luuakse projekti alammooduli ja pearaamatu tehingud. Neid kasutatakse allavooli kliendi arveldamises, tulu kajastamises ja finantsaruandluses.

Valitud rakenduse Project Operations integratsioonitöölehte saab postitada, kasutades rakenduse Project Operations integratsioonitöölehel käsku **Postita**. Kõiki töölehti saab automaatselt postitada, käivitades protsessi aadressil **Perioodilisus** > **Project Operationsi integreerimine** > **Project Operationsi integreerimise tööleht**.

Postitamine võib toimuda interaktiivselt või partiidena. Pange tähele, et kõik töölehed, millel on rohkem kui 100 rida, postitatakse automaatselt partiidena. Parema jõudluse saavutamiseks, kui palju ridu sisaldavaid töölehti postitatakse partiina, aktiveerige funktsioon **Project Operationsi integratsioonitöölehe postitamine mitme partiiülesande abil** tööruumis **Funktsioonihaldus**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Teisaldage kõik postitamise vigadega read uude töölehte

> [!NOTE]
> Selle võimaluse kasutamiseks aktiveerige **Kõikide postitamise vigadega ridade teisaldamine rakenduse Project Operations integratsioonitöölehele** funktsioon **Funktsioonihalduse** tööruumis.

See funktsioon aitab parandada Project Operationsi integratsioonitöölehe kasutuskogemust. Kui see on lubatud, ei takista topeltkirjutuse ajastusprobleemid ja häälestusprobleemid enam kehtivate ajakirjete postitamist. Project Operationsi integratsioonitöölehele postitamise ajal valideerib süsteem iga töölehe rea. See postitab kõik read, millel ei ole vigu, ja loob uue töölehe kõigi ridade jaoks, millel on postitamisvigu.

Postitamisvigade ridu sisaldavate töölehtede vaatamiseks minge **Projektihaldus ja raamatupidamine** \> **Töölehed** \> **Project Operationsi integratsioonitööleht** ja filtreerige töölehtede loendit, kasutades välja **Algne tööleht**. Järgneval joonisel on näide, kus lehel **Project Operationsi integratsioonitööleht** olevad töölehed on sel viisil filtreeritud.

![Algne tööleht, mis on näidatud Project Operationsi integratsioonitöölehe lehel.](./media/transferLines-originalJournal.png)

Kui integratsioonitöölehe postitamiseks on konfigureeritud perioodiline partiitöö, üritatakse postitamist uuesti ja töölehed postitatakse, kui ajastusprobleem on kõrvaldatud. Kõiki ülejäänud töölehti tuleks käsitsi uurida, vaadates läbi logid ja võttes vajalikud meetmed.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
