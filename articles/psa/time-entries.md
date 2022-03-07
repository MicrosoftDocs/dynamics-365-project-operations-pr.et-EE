---
title: Ajakirjete loomine
description: Selles teemas kirjeldatakse, kuidas luua ajakirjeid.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0d0e21d0964788564d3db9173c3a0b3378cd0049b4455a23ccc1bccd1c21d9e7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990401"
---
# <a name="create-time-entries"></a>Ajakirjete loomine

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Varasemates Dynamics 365 Project Service Automation versioonides sisestati ajakirjeid kord nädalas. Project Service Automation versioonis 3 sisestatakse ajakirjeid iga päev. Kuid pärast paari ajakirje loomist saate neid luua või kopeerida hulgi kaupa.

## <a name="create-a-time-entry"></a>Loo ajakirje

Ajakirje loomiseks tehke järgmist.

1. Valige lehel **Ajakirjed** suvand **Uus**.
2. Sisestage dialoogiboksi **Kiirloomine: ajakirje** ajakirje kestus minutites, tundides või päevades. Kestus tuleb sisestada järgmises vormingus: *x* minut(it), *x* tund(i) või *x* päev(a). Tunde ja päevi saab sisestada ka kümnendkohtade kasutamisega, näiteks *x,x* tundi või *x,x* päeva.
3. Valige ajakirje tüüp ja projekt, mille jaoks ajakirjet sisestate.
4. Otsige väljast **Projektiülesanne** selle ajakirje jaoks sobiv ülesanne.

    > [!NOTE]
    > Kui loote ajakirje ülesande jaoks, mis pole kasutajale määratud, valige väljast **Projektiülesanne** nupp **Otsi**, valige suvand **Muuda vaadet** ja valige seejärel kõigi ülesannete loendi nägemiseks suvand **Kõik aktiivsed projektiülesanded**.

5. Kui on vaja sisestada kirjeldus, tehke seda, ja seejärel valige suvand **Salvesta ja Sule**.

Pärast ajakirje loomist ja salvestamist saate seda redigeerida ajakirje ruudustikus. Ajakirje ruudustik toetab kahte vormingut.

- Saate ajakirjed sisestada vormingus **hh:**. See vorming teisendatakse seejärel tundideks ja murdosadeks.
- Saate otse sisestada tunnid ja murdosad.

Pange tähele, et tunni murdosad ei ole minutid. Seega 1,5 tundi on 1 tund ja 30 minutit. Sama reegel kehtib päeva murdosade kohta. Üks päev on 24 tundi ja 0,5 päeva on 12 tundi.

## <a name="bulk-create-time-entries"></a>Ajakirjete loomine hulgi kaupa

Pärast paari ajakirje loomist saate neid kopeerida, et luua hulgi kaupa veelgi ajakirjeid.

1. Valige lehel **Ajakirjed** suvand **Kopeeri nädal**.
2. Ajakirjete kopeerimiseks määrake väljades **Perioodi algus**, **Alguskuupäev** ja **Lõppkuupäev** kuupäevavahemik.
3. Määrake väljades **Perioodi lõpp** ja **Alguskuupäev** kuupäev, mille jaoks soovite ajakirjeid luua.
4. Valige suvand **Kopeeri**, et luua nende ajakirjete koopia, mis vastavad väljal **Perioodi lõpp** määratud nädalapäevale. Näiteks viimase nädala esmaspäeva ajakirje kopeeritakse selle nädala esmaspäeva, mis on määratud väljal **Perioodi lõpp**.

## <a name="import-data-for-time-entries"></a>Ajakirjete impordi andmed

Saate importida projekti broneeringute ja ülesannete andmeid. Andmete importimisel saate määrata imporditavate broneeringute kuupäevavahemiku ja seejärel eraldi valida broneeringud, mis tuleks luua ajakirjete **mustanditena**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Rühmitamise, sortimise, otsimise ja filtreerimise võimalused

Saate ajakirjeid rühmitada ja filtreerida veergudes määratud dimensioonide järgi. Valige väljast **Rühmitusalus** dimensioon, mida soovite ajakirjete filtreerimiseks kasutada. Saate ajakirjeid sortida ka tõusvas või kahanevas järjekorras, kasutades veerupäises olevat sortimisnoolt. Peale selle saate ka kirjeid kuvada või peita, kui vajutate veerupäistes olevat nuppu **Filtreeri** ja sisestate seejärel väljale **Otsi** teksti, mida tuleks kasutada ajakirjete otsimiseks projekti nime, projekti ülesande, ajakirje või ressursi järgi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]