---
title: Logimata materjalide ja ootel hankija arvete konfigureerimine
description: Selles artiklis selgitatakse, kuidas lubada ladustamata materjale ja ootel hankija arveid.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6473ef3510f0d3641a2d61b6a1b1f28980993277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913753"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Logimata materjalide ja ootel hankija arvete konfigureerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

## <a name="minimum-version-requirement"></a>Versiooni miinimumnõue

Logimata materjalide ja ootel tarnija arvete kasutamiseks rakenduse Dynamics 365 Project Operations logimata/ressursipõhiste stsenaariumide korral on vaja järgmisi versioone.

Dynamics 365 Dataverse’i lahendused.

- Project Operations – 4.9.0.221 või uuem
- Topeltkirjutusrakenduse korraldamislahendus – 2.2.2.23 või uuem

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) või uuem. Veenduge, et teie rahanduskeskkond oleks ajakohane ja kõik kvaliteedivärskendused oleks rakendatud versiooni miinimumnõuete kohaselt.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Käitage topeltkirjutuse kaarte logimata materjalide ja hankija arve integreerimiseks

Selles jaotises antakse teavet logimata materjalide ja tarnija arvete jaoks vajalike kaartide kohta. Veenduge, et uues [keskkonnas](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) artiklis Säte loetletud eeltingimuskaardid töötaksid teie keskkonnas.

1. Minge jaotisse Lifecycle Services (LCS), liikuge oma LCS-i projekti ja minge lehele **Keskkonna üksikasjad**.
2. Valige jaotises **Common Data Service’i keskkonnateave** suvand **Link CDS-iga rakendustele**. Pärast lingi valimist suunatakse teid vastenduste olemite loendisse.
3. Veenduge, et järgmised kaardid töötaks. Kui need ei tööta, käivitage need ja lisage kindlasti kõik seostuvad tabelikaardid.

    - CDS-i välja antud eraldi tooted (tooted)
    - Tarnijad v2 (msdyn_vendors)
    - Project Operationsi tabel materjalide prognooside jaoks (msdyn_estimatelines)
    - Project Operationsi integreerimise projekti tarnija arve ekspordist (msdyn_projectvendorinvoices)
    - Project Operationsi integratsioon projekti tarnija arve rea ekspordist (msdyn_projectvendorinvoices)
    - Project Operationsi integreerimise tegelikud näitajad (msdyn_actuals). Veenduge, et töötaksite kaardiversiooniga 1.0.0.14 või uuemaga. Kaardi aktiivset versiooni saate vaadata veerus **Versioon** lehel **Topeltkirjutamine**. Saate kaardi uue versiooni aktiveerida, valides **tabelikaardi versiooni** ja salvestades seejärel valitud versiooni.

Kui kasutate standardseid demoandmeid, peate algse sünkroonimise korral peatama ja taaskäivitama ka järgmised olemikaardid.
  - Maksepäevade CDS V2 (msdyn_paymentdays)
  - Maksegraafik (msdyn_paymentschedules)
  - Maksetingimused (msdyn_paymentterms)
  - Hankijarühmad (msdyn_vendorgroups)
  - Ühikud (uom)

> [!NOTE]
> Hankijarühmade ja ühikute algse sünkroonimise korral võib mõne olemasoleva demoandmekomplekti kirje sünkroonimine nurjuda. Võite nurjumisi ignoreerida, kuna need ei takista teil Project Operationsiga demoandmeid kasutamast.

## <a name="configure-prerequisites-in-dataverse"></a>Eeltingimuste konfigureerimine rakenduses Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Aktiveerige töövoog, et luua ettevõtted hankija olemi põhjal

Topeltkirjutamise korraldamise lahendus pakub [hankijate põhiintegreerimise](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Selle funktsiooni eeltingimusena tuleb hankija andmed luua olemis **Kontod**. Aktiveerige malli töövooprotsess, et luua tarnijad tabelis **Kontod**, nagu on kirjeldatud jaotises [Hankijate kujunduse vahetamine](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Määra tooted loomisel aktiivseks

Logimata materjalid peavad olema konfigureeritud **Välja antud toodetena** jaotises Rahandus. Topeltkirjutamise korraldamise lahendus pakub [välja antud toodete integreerimise Dataverse’i tootekataloogi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping) valmislahendust. Vaikimisi sünkroonitakse jaotise Rahandus tooted Dataverse’i mustandisse. Kui soovite toote sünkroonida aktiivse olekuga, et seda saaks otse kasutada materjali kasutusdokumentides või ootel hankija arvetes, avage jaotis **Süsteem** > **Haldus** > **Süsteemihaldus** > **Süsteemi sätted** ja määrake vahekaardil **Müük** suvandi **Loote tooted aktiivse olekuga** väärtuseks **Jah**.

## <a name="configure-prerequisites-in-finance"></a>Eeltingimuste konfigureerimine jaotises Rahandus

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Luba ootel hankija arvete funktsioonivõti

Tehke järgmised toimingud, et lubada ootel hankija arve ridadele projekti üksikasjade lisamise funktsioon.

1. Minge Rahanduses tööruumi **Funktsioonide haldus**.
2. Otsige funktsiooniloendist funktsiooni **Luba ootel tarnija arved Project Operationsi ressursipõhiste/logimata stsenaariumide jaoks** ja valige suvand **Luba**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Olemite kategooriarühmade ja projektikategooriate määratlemine

Konfigureerige selle rühma abil vähemalt üks kategooriarühm **olemi** kandetüübi jaoks ja vähemalt üks projektikategooria. Lisateavet leiate teemast [Projektikategooriate konfigureerimine](../project-accounting/configure-project-categories.md#category-groups).

Vaadake üle projekti kulu- ja tuluprofiilid ja konfigureerige olemite kannete jaoks sisestuse konfigureerimine. Lisateavet leiate teemast [Arveldatavate projektide raamatupidamisarvestuse konfigureerimine](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Sisestatava toote seadistamine

Project Operationsis saate kirjendada materjalide prognoose ja kasutamist väljastatud tootekataloogis konfigureeritud kataloogitoodete ja sisestatavate toodete jaoks. Sisestavate toodete kasutamiseks on vaja ühte välja antud toodet, mis on sel eesmärgil konfigureeritud jaotises Rahandus. Sisestatava toote konfigureerimiseks tehke järgmist. Korrake neid samme iga juriidilise isiku puhul, kes kasutab Project Operationsi ressursi/logimata stsenaariumide jaoks.

1. Minge jaotisesse **Tooteteabe haldus** > **Tooted** > **Välja antud tooted** ja valige **Uus**.
2. Valige väljal **Toote tüüp** **Üksus** ja väljal **Toote alamtüüp** väärtus **Toode**.
3. Sisestage toote number (WRITEIN) ja toote nimi (sisestatav toode).
4. Valige üksuse mudelirühm. Veenduge, et teie valitud kauba mudeli rühmas oleks välja **varude poliitika laotoote** väärtuseks seatud **Väär**.
5. Valige väärtused väljade **Üksuse rühm**, **Mäluruumi dimensioonirühma** ja **Jälgimise dimensioonirühm** jaoks. Kasutage valikut **Hoiustamise mõõdud** ainult suvandi **Koht** jaoks ja väljal **Jälgimise mõõtmed** valige **Puudub**.
6. Valige väärtused väljal **Laoühik**, **Ostuühik** ja **Müügiühik** ning seejärel salvestage oma muudatused.
7. Määrake vahekaardil **Plaan** tellimuse vaikesätted ja vahekaardil **Varud** vaikeasukoht ja ladu.
8. Minge jaotisse **Projekti haldus ja raamatupidamine** > **Seadistus** > **Projektihalduse ja -raamatupidamise parameetrid** ja avage **Project Operations on Dynamics 365 Dataverse**. 
9. Valige vahekaardi **Materjalid** väljal **Sisestatav toode** see toode, mille lõite.
10. Avage oma Dataverse’i keskkonna saidikaardil **Tooted** üksus ja leidke sisestatava toote kirje. 
11. Avage kirje üksikasjad ja määrake toote olekuks **Kasutuselt kõrvaldatud**. See toote olek takistab selle kirje juhuslikku kasutamist otse materjali prognoosides ja kasutusdokumentides.

### <a name="set-up-a-procurement-integration-account"></a>Hangete integreerimise konto seadistamine

Hanke integreerimise kontot kasutatakse kliirimiskontona projektile omistatud ridadega ootel oleva tarnija arve postitamisel.

Kui süsteem postitab ootel oleva hankija arve, kasutatakse seda kontot projekti kulusumma jaoks. Hankija arve üksikasju töödeldakse Dataverse’is ja luuakse vastav projekti tegelik töö. Projekti tegelik teave lisatakse Project Operationsi integreerimise töölehele. Integreerimise töölehe postitamisel kustutatakse summa hanke integreerimise kontolt ja kantakse projekti maksumusesse.

1. Hanke integreerimise konto seadistamiseks avage **Projekti haldus ja raamatupidamine** > **Seadistamine** > **Projektihalduse ja -raamatupidamise parameetrite seadistamine** ja avage **Project Operations on Dynamics 365 Dataverse**. 
2. Valige vahekaart **Materjalid** ja valige väärtus väljal **Hangete integreerimise konto**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Üksuse projektikategooria vaikeväärtuste seadistamine

1. Avage jaotises Rahandus **Projekti haldusse ja raamatupidamine** > **Seadistus** > **Projektihalduse ja -raamatupidamise parameetrite seadistamine** ja avage **Project Operations on Dynamics 365 Dataverse**. 
2. Valige väärtus vahekaardi **Projekti kategooria vaikeväärtused** väljal **Üksus**. Seda projektikategooriat kasutatakse oluliste kannete jaoks, kui projekti kategooriat ei määrata projekti tegelike kirjete jaoks.
