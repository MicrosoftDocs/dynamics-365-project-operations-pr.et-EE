---
title: Projekti arve ettepanekute haldamine
description: Selles teemas antakse üksikasjalikku teavet kliendile suunatud arvete töötlemise kohta Project Operationsi abil ressursipõhiste/mittelaopõhiste stsenaariumide korral.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 61b43e05eb179e2b00189076290433dd72f89a6bc7ef72140fc1efd752149d43
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989906"
---
# <a name="manage-project-invoice-proposals"></a>Projekti arve ettepanekute haldamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Teie arveosakond saab projekti arve ettepanekuid töödelda, kui on täidetud järgmised kaks tingimust.

  - Projektijuht kinnitab proforma arve rakenduses Microsoft Dataverse.
  - Kõik arveldamata aja- ja materjali müügitehingud, mis on kaasatud proforma arvesse, sisestatakse Dynamics 365 **Project Operations integratsiooni** töölehe abil.

Projekti arve ettepaneku lõpetamiseks rakenduses Dynamics 365 Finance toimige järgmiselt.

1. Vaadake üle aja- ja materjali tehingute arveldusteave ja sisestage tööleht **Project Operationsi integratsioon**.
2. Vaadake üle fikseeritud hinnaga arveldamise vahe-eesmärkide arveldusandmed.
3. Vaadake üle ja vormindage projekti arve ettepanek.
4. Sisestage ja printige projekti arved.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Hallake arveldusteavet Project Operationsi integreerimise töölehel

Dataverse'is loodud projekti tegelikud näitajad vaatab üle ja sisestab Finance'i projekti raamatupidaja. Lisateavet integreerimise töölehega töötamise kohta vt jaotisest [Project Operationsi integreerimise tööleht](../project-accounting/project-operations-integration-journal.md).

Kulu tegelikud näitajad ja arveldamata müügi tegelikud näitajad lisatakse integreerimise töölehele eraldi ridadena.

  - Ühiku omahinna ja kulu summa tegelikus kulus tuleb vaikimisi projekti tegeliku kulu kandest Dataverse'is.
  - Arveldamata müügitehingu üksuse müügihinna ja müügisumma vaikeväärtuseks on projekti tegelik arveldamata müügitehing Dataverse'is.

### <a name="billing-sales-tax"></a>Arveldamise käibemaks

Arvelduse käibemaksuarvutuse määratleb väljade **Arvelduse käibemaksugrupp** ja **Arveldusüksuse käibemaksugrupp** kombinatsioon arveldamata müügikirjel töölehe real **Project Operationsi integreerimine**. Süsteem määrab nende väljade vaikeväärtused vahekaardi **Finantsasjad** sätete põhjal lehel **Projektihalduse ja raamatupidamise parameetrid**.

- **Käibemaksugrupi meetod** määratleb arvelduse käibemaksugrupi vaikeväärtuste loogika.
  
  - **Projekt**: arvelduse käibemaksugrupi vaikeväärtus saadakse alati projektist. Projekti arvelduse vaikimisi käibemaksugruppi saate üle vaadata või muuta, kui valite käsu **Kuva vaikimisi raamatupidamine** lehel **Kõik projektid**.
  - **Projekti leping**: arvelduse käibemaksugrupi vaikeväärtus saadakse alati projekti lepingust. Projekti lepingu vaikimisi käibemaksugruppi saate üle vaadata või muuta, kui valite käsu **Kuva vaikimisi raamatupidamine** lehel **Projekti lepingud**.
  - **Klient**: arvelduse käibemaksugrupi vaikeväärtus saadakse alati kliendist.
  - **Otsing**: otsib kõigist ülaltoodud olemitest ja valib esimese saadaoleva väärtuse. Otsing algab olemist **Projekt**, seejärel tuleb olem **Projekti leping** ja lõpuks olem **Klient**.

- **Üksuse käibemaksugrupi meetod** määratleb arvelduse üksuse käibemaksugrupi vaikeväärtuste loogika.
  
  - Aja, kulu ja tasu kannete tüüpide korral saadakse arveldusüksuse käibemaksugrupp alati vaikimisi olemist **Projekti kategooria**.
  - Materjali kannete tüüpide korral saadakse arveldusüksuse käibemaksugrupp vaikimisi sättest **Üksuse käibemaksugrupi meetod** jaotises **Projektihalduse ja raamatupidamise parameetrid**. Üksuse numbri vaikeväärtuseks on üksuse käibemaksugrupp olemist **Vabastatud toode**. Kategooria vaikeväärtuseks on üksuse käibemaksugrupp olemist **Projekti kategooria**.

### <a name="financial-dimensions"></a>Finantsdimensioonid

Arveldamata müügikirjete finantsdimensioonide vaikeväärtused töölehel **Project Operationsi integreerimine** saadakse olemist **Projekt**. Finantsdimensioone saab üle vaadata ja reguleerida, valides suvandi **Summade jaotamine**. Kui teil on vaja muuta arveldamata müügikirjete finantsdimensioone pärast integreerimise töölehe sisestamist aga enne Proforma arve kinnitamist, avage **Kõik projektid** > **Halda** > **Sisestatud tehingud**, valige tehing ja seejärel valige **Töötle** > **Kohanda raamatupidamist**.

### <a name="exchange-rates"></a>Vahetuskursid

Dataverse'is arveldamata tehingu valuutat kasutatakse Finance'i tehingu valuutana ja teisendatakse ettevõtte arvestusvaluutaks Finance'is määratud vahetuskursiga.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Arvelduse etappide finantsatribuutide haldamine 

Fikseeritud hinnaga arveldusmeetodit kasutavad projekti lepinguread arveldatakse [Fikseeritud hinnaga osamaksete](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line) kaudu. Projekti raamatupidaja saab arvelduse etapid Finance'is üle vaadata, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Halda** > **Kontoga seotud kanded**.

### <a name="billing-sales-tax"></a>Arveldamise käibemaks

**Käibemaksugrupi** ja **Üksuse käibemaksugrupi** vaikeväärtused saadakse sätetest, kui Dataverse'i luuakse uus arveldusetapp. Süsteem määrab nende väljade vaikeväärtused vahekaardi **Finantsasjad** sätete põhjal lehel **Projektihalduse ja raamatupidamise parameetrid**.

- **Käibemaksugrupi meetod** määratleb **Arvelduse käibemaksugrupi** vaikeväärtuse loogika.

    - **Projekti** arvelduse käibemaksugrupi vaikeväärtus saadakse alati projektist. Projekti vaikimisi käibemaksugruppi saate üle vaadata või muuta, kui valite käsu **Kuva vaikimisi raamatupidamine** lehel **Kõik projektid**.
    - **Projekti lepingu** arvelduse käibemaksugrupi vaikeväärtus saadakse alati projekti lepingust. Projekti lepingu vaikimisi käibemaksugruppi saate üle vaadata või muuta, kui valite käsu **Kuva vaikimisi raamatupidamine** lehel **Projekti lepingud**.
    - **Kliendi** arvelduse käibemaksugrupi vaikeväärtus saadakse alati kliendist.
    - **Otsing** otsib kõigist selle loendi olemitest ja valib esimese saadaoleva väärtuse. Otsing algab olemist **Projekt**, seejärel tuleb olem **Projekti leping** ja seejärel olem **Klient**.

- **Fikseeritud hinnaga eesmärgitoote müügimaksurühma** kasutatakse arvelduse vahekokkuvõtte **Kauba müügi maksurühm** vaikeväärtusena. Konto omanik saab selle väärtuse üle vaadata ja seda muuta lehel **Kontol tehtud tehingud**. Süsteem kasutab projekti arve arveldamise rea loomisel kontol oleva tehingu väärtust.
 

### <a name="financial-dimensions"></a>Finantsdimensioonid

Fikseeritud hinnaga arvelduse osamakse vaikimisi finantsdimensioonid seadistatakse projekti lepinguridadel. Avage **Projekti lepingud** > **Kuva vaikearvestust** ja valige vahekaardil **Lepinguread** rida **hinna lepingurida**, seejärel määratlege need finantsdimensioonide väärtused, mida soovite vaikimisi kasutada.

Projekti arvestaja saab redigeerida arve osamaksete käibemaksu- ja finantsdimensioonide andmeid kuni projekti arve ettepaneku loomiseni.


## <a name="create-project-invoice-proposals"></a>Projekti arve ettepanekute loomine

Projekti arve ettepanekuid saab üle vaadata moodulis **Projektihaldus ja raamatupidamine**, avades jaotise **Projekti arved** > **Projekti arve ettepanekud**.

Projekti arve ettepaneku päis luuakse Finance'is kui proforma arve Dataverse'is kinnitatakse. Lihtsamaks vastavusseviimiseks määrab süsteem projekti arve ettepaneku numbri Finance'is sama numbri peale, kui proforma arve ID on Dataverse'is. Kuna proforma arveid ei kinnitata tingimata samas järjekorras, nagu neid luuakse, peavad projekti arve ettepaneku numbrijadad Finance'is võimaldama väiksematele ja suurematele numbritele muutmist. Konfigureerige numbrijadad järgmiselt.

1. Avage Finance'is jaotis **Organisatsiooni haldus** > **Numbrijadad** > **Numbrijadad**.
2. Valige filtris **Ala** valik **Projektid**.
3. Valige filtris **Viide** valik **Arve ettepanek**.
4. Kasutage välja **Ettevõte** iga juriidilise isiku filtreerimiseks koos sisselülitatud Project Operationsi Dataverse'i integratsiooniga.
5. Avage **Numbrijada üksikasjad** ja määrake vahekaardil **Üldine** järgnev.

    - **Luba kasutaja muudatused: väiksemale arvule** = **Jah**
    - **Luba kasutaja muudatused: suuremale arvule** = **Jah**

Projekti arve ettepaneku read lisatakse süsteemi poolt perioodilise protsessi **Koondtabelist importimine** (**Projektihaldus ja raamatupidamine** > **Perioodiline** > **Project Operationsi integreerimine** > **Koondtabelist importimine**) abil. Selle protsessi saab käivitada käsitsi või kasutades perioodilist ajakava. Süsteem ei lisa ridu arve ettepaneku dokumendile enne, kui kõik read on arveldamiseks valmis. Aja- ja materjalitehingud on arveldamiseks valmis alles siis, kui need sisestatakse töölehe **Project Operationsi integreerimine** abil.

## <a name="format-and-print-invoice-proposals"></a>Arve ettepanekute vormindamine ja printimine

Projekti arvestaja projekti arve väljatrükki kohandada, kasutades lehte **Arve ettepaneku vormindamine** ja prindihalduse võimalusi.

### <a name="format-invoice-proposals"></a>Arve ettepanekute vormindamine

Leht **Arve ettepanekute vormindamine** võimaldab kuvada kliendi projekti arvel kohandatud rühmitamiskandeid.

1. Valige lehel **Projekti arve ettepanek** jaotis **Printimine** > **Arve ettepaneku vormindamine**.
2. Projekti arve väljatrükile uue rühmitamise loomiseks valige **Uus**.
3. Valige väljal **Üksikasjad/kokkuvõte** selle rühmitamise suvandid.

    - Kliendiarve tehingu üksikasjade printimiseks valige **Üksikasjad**.
    - Kliendiarve tehingu kokkuvõtte printimiseks valige **Kokkuvõte**.

> [!NOTE]
> Välja **Üksikasjad/kokkuvõte** valik lehel **Arve ettepaneku vormindamine** alistab lehe **Arve ettepanekud** väljal **Arve vorming** valitud üksikasjaliku arve või kokkuvõtliku arve printimise valiku.

- Valige tehinguread, mida kaasata vahekaardi **Saadaolevad tehingud** sellesse jaotisesse ja valige **Kaasa tehingud**, et teisaldada need vahekaardile **Valitud tehingud**.
- Jaotiste järjestuse muutmiseks valige käsud **Nihuta üles** ja **Nihuta alla**.
- Vormindatud arve vaatamiseks valige **Prindi eelvaade**.

### <a name="print-management"></a>Prindihaldus

Prindihaldus kasutab erinevaid aruandefaile, et printida, määrata sihtkohti ja kohandada arve jalusteksti. Prindihalduse saab seadistada mooduli tasandil, kuid neid sätteid saab konkreetse kliendi, lepingu või arve puhul üle kirjutada. Sellele funktsioonile juurdepääsu saamiseks lehel **Projekti arve ettepanek** valige **Printimine** > **Prindihaldus**.

Prindihalduse seadistamine kuvatakse puuvaatena, kus igal sõlmetasemel kuvatakse korrigeerimiseks saadaolevad dokumendid. Saate mooduli, kliendi, lepingu või arve ettepaneku dokumendi tasandil määrata kohandatud väljatrükke. Algdokumendi väljatrüki muutmiseks laiendage soovitud sõlme ja valige **Algüksus**. Valige väljal **Aruande vorming** printimiseks kasutatav aruande vorming. Kohandatud aruandevorminguid saate kasutada [Äridokumendihalduse raamistiku](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management) abil.

## <a name="post-invoice-proposals"></a>Arve ettepanekute sisestamine

Kui arve on läbi vaadatud ja redigeeritud ning arve ettepaneku read on rahuldavad, kontrollige arve kogusummasid ja käibemaksu. Valige grupis **Üksikasjad** valik **Kogusummad** ja seejärel valige arve sisestamiseks käsk **Sisesta**.

Arve vaatamiseks enne sisestamist tühjendage märkeruut **Sisestamine**. Arvele prinditakse **Proforma**, et näidata, et tegu on näidisarvega. Arve printimiseks märkige ruut **Prindi arve**.

Lisaks lehele **Arve ettepanek** saab arve ettepanekuid sisestada ka perioodilise töö **Arve ettepanekute sisestamine** abil. Selle töö leidmiseks avage **Projektihaldus ja raamatupidamine** > **Perioodiline** > **Projekti arved** > **Arve ettepanekute sisestamine**.

Sellel lehel on kuvatud kõik sisestamisvalmis arve ettepanekud. Arve ettepanekute sisestamise saate ajastada, valides suvandi **Partii**. Seadistage **Partiitöötluse parameeter** väärtusele **Jah** ja määrake partiitöötluse korduvus valides suvandi **Korduvus**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
