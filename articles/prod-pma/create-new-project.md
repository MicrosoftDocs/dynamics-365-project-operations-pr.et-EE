---
title: Luua uut projekti
description: See artikkel annab teavet uue projekti loomise kohta.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cbe7ea7d6ee57b3494494a2758dbcb7ded735dc1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919687"
---
# <a name="create-a-new-project"></a>Luua uut projekti

[!include [banner](../includes/banner.md)]

Uue projekti loomiseks tehke järgmist.

1. Lehel **Projektihaldus** valige **Uus projekt** ja sisestage järgmised väärtused.

    - **Projekti tüüp:** aeg ja materjal
    - **Projekti nimi:** XYZ värskenduse 2. etapp
    - **Projekti rühm:** TM\_WIP
    - **Projekti lepingu ID:** 00000002

2. Valige käsk **Loo projekt**.

## <a name="assign-a-resource-to-a-project"></a>Ressursi määramine projektile

1. Lehel **Töötajad** loendis **Töötajad** valige töötaja, kelle jaoks oskuseid seadistasite, ja avage töötaja kirje.
2. Valige toimingupaanil vahekaardil **Projekt** rühmas **Seadistamine** suvand **Määra projekt**.
3. Vahekaardi **Ressursi valideerimise projekti ülesanded** vahekaardi **Projektid** väljal **Lisa projekt valitud projektide hulka** filtreerige projektil **XYZ värskenduse 2. etapp**.
4. Paanil **Ülejäänud projektid** valige projekt ja valige seejärel noolenupp, et lisada see paanile **Valitud projektid** .

Saate ressursile määrata kategooriaid ka vastavalt vajadusele. Kategooria tüüp on kas **Kulu** või **Tulu**. Kategooria tüübi määrab teie organisatsioon. Kui ühtegi kategooriat pole ressursi jaoks määratud, otsib rakendus Finance vaikimisi kategooriat tunnihinna ja tulu kohta.

## <a name="set-up-project-resource-and-role-characteristics"></a>Projekti ressursi ja rolli omaduste seadistamine

Projektijuht saab projekti jaoks vajalike rollide loomiseks kasutada projekti ressursside funktsiooni. Rolle saab kasutada juhul, kui kinnitatud ressursid on ressursside reserveerimisel endiselt tundmatud. Rolle saab ajutiselt reserveerida plaanitud ressurssidena, et saaksite projekti kavandamise etappidega jätkata.

[![Rolli näide.](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Stsenaarium:** Contoso palgati lõpetama aja- ja materjalikulu projekti, millel on kinnitatud projekti põhikiri. Noorem-projektijuht endiselt lõpetab projekti ulatust. Ressursihaldur määratleb praegu konkreetsed ressursid, mis reserveeritakse uue projektiga töötamiseks. Projekti kriitilise iseloomu tõttu taotles projekti sponsor ühe rollina vanem-projektijuhti. Ressursihaldur peab hankima uue ressursi ja määrama süsteemis rolli juhul, kui noorem-projektijuht vajab projekti kavandamise ajal ressursi teavet.

Järgmised juhised näitavad, kuidas ressursihaldur saab seadistada vanem-projektijuhi rolli ja seostada ressursi omadused sellega. Hiljem saab rolli kasutada saadaolevate ressursside otsimiseks, mis vastavad ressursi nõutavatele pädevustele.

1. Lehel **Seadistamise rollid** valige **Uus projekt** ja sisestage järgmised väärtused.

    - **Rolli ID:** vanem-projektijuht
    - **Kirjeldus:** vanem-projektijuht

2. Valige käsk **Loo**.
3. Valige roll **Vanem-projektijuht** ja valige seejärel **Konfigureeri tunnused**.
4. Väljal **Tunnuste tüüp** valige **Oskus**.
5. Väljale **Saadaolevad tunnused** sisestage otsitav oskus.
6. Väljal **Tunnuse tüüp** valige **Sertifikaat**.
7. Väljale **Saadaolevad tunnused** sisestage otsitav sertifikaadi tüüp.

## <a name="assign-a-project-resource-to-a-project"></a>Projekti ressursi määramine projektile

1. Lehel **Kõik projektid** valige projekt **XYZ värskenduse 2. etapp**.
2. Vahekaardil **Projektimeeskond ja kavandamine** valige suvand **Lisa**.
3. Väljale **Roll** sisestage **Meeskonnaliige**.
4. Valige suvand **Broneeri kalendrist**.
5. Lehel **Ressursi saadavus** valige **Kuva sätted**.
6. Lehel **Redigeeri kuvamissätted** sisestage järgmised väärtused.

    - **Kuupäeva vahemiku vaate vorming:** päev
    - **Kuva saadaolevad kirjeldused:** jah
    - **Kuva allesjäänud võimsus:** jah

7. Valige ressursside loendist ressurss.
8. Valige **Fikseeritud reserveering** ja **Täisvõimsus**.

## <a name="assign-a-resource-to-a-default-role"></a>Ressursi määramine vaikerollile

Projekti või ressursi haldamisega abistamiseks võivad juhid veelgi rohkem minna süvitsi ressursside puhul, mida saab projekti jaoks broneerida. Saate seostada vaike-rolli olemasoleva ressursiga või värskelt omandatud ressursiga. Näiteks, kui Daniel palgati, olid tal kogemus ja oskused täita ärianalüütiku rolli. Ressursihaldur määras selle rolli Danielile vaike-rolliks. Seega lisaks ressursihaldur Daneli ärianalüütikute kogumile, kes olid saadaval projektidega töötamiseks.

Ressursi reserveerimise ajal saavad projektijuhid filtreerida projektidega töötamiseks saadaolevate rollidega ressursse. Nad saavad kasutada seda teavet ühe kriteeriumina, kui nad teostavad ressursi täitmisel mitme tunnusega otsuste analüüsimist. Nad saavad lisada filtrile ka teisi ressursi omadusi, et otsida teatud projekti jaoks konkreetsete oskuste, hariduse ja kogemusega ressursse.

**Stsenaarium:** kinnitatud projekt on käivitatud ja vanem-projektijuhi roll oli reserveeritud planeeritud ressursina projekti kavandamise etapis. Ressursihaldur on nüüd hankinud ressursi vanem-projektijuhi rolli täitmiseks.

1. Lehel **Ressursside loend** valige **Daniel Kangur**.
2. Lehel **Ressursi roll** valige **Uus projekt** ja sisestage järgmised väärtused.

    - **Jõustub:** sisestage praegune kuupäev.
    - **Aegub:** sisestage **Mitte kunagi**.
    - **Roll:** sisestage **Vanem-projektijuht**.

3. Valige käsk **Salvesta** ja sulgege seejärel leht.
4. Vahekaardil **Pädevused** lisage oskus **Projektihaldus** ja sertifikaat **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]