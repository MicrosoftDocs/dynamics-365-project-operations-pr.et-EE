---
title: Projektimeeskonna loomine
description: Selles teemas antakse teavet projektimeeskonna loomise ja haldamise kohta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7eb9101352afd27b527bf6b8acc6f92198f44ea
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075121"
---
# <a name="create-a-project-team"></a>Projektimeeskonna loomine

[!include [banner](../includes/banner.md)]

Varem projektis seadistatud rollide kasutamiseks peab projektijuht seostama rollid projektiga. Projektile võib määrata mitu rolli. Segaduse vältimiseks sildistatakse need rollid reserveerimise ajal automaatselt. Näiteks kui projektijuht nõuab kolme tarkvarainseneri, luuakse automaatselt kolm rolli Tarkvarainsener, millel on sildid **tarkvarainsener 1** , **tarkvarainsener 2** ja **tarkvarainsener 3** , kuna nende sildid luuakse automaatselt. Kui rolli omadused olid varem rollile määratud, rakendatakse need ressursi otsingu ajal justkui filter. Otsingu veelgi täpsemaks muutmiseks saab lisada vastavalt vajadusele täiendavaid tunnuseid.

Kuvamissätteid saab samuti kohandada, et anda ressursi saadavusest parem vaade. Saadavust võib kuvada tundide, päevade, nädalate, kuude, kvartalite ja aastate lõikes. Lisaks on olemas võimalus kuvada ressursside saadaolev ja allesjäänud võimsus. See suvand on kasulik ajahalduse jaoks, kui prognoosite saadaolevat aega tegevuste või ressursi kättesaadavuse kohta.

Projektijuht saab valida lehel rolli ja seejärel vaba ressursi olemasolul, mis nõudega ühtib, valida ressursi reserveerimine rolli täitmiseks. Pange tähele, et ressursse ei pea kavandamise etapis sellel hetkel reserveerima. WBS-i loomisel saate rolle asendada projekti töötajate ressurssidega. Kui rollid asendatakse WBS-is töötajatest ressurssidega, siis ressursi seadistus värskendab automaatselt projektimeeskonda loendit ja ajakava.

[![Projektimeeskonna loend, mis sisaldab nii rolle kui ka tegelikke ressursse](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektijuhil on mitmeid võimalusi projekti jaoks ressursi broneerimiseks, nagu **Järelejäänud võimsus** , **Täisvõimsus** , **Võimsuse protsent** ja **Konkreetsed tunnid**. Kui ressursi määramised muutuvad, saab neid broneeringu võimalusi igal ajal tühistada. Toetatud on kahte tüüpi broneeringud.

- **Fikseeritud broneering** – ressursi broneerimine kiideti heaks ja kinnitati, et teatud aja jooksul töötab seal.
- **Esialge broneerimine** – ressursi broneerimised määrati esialgu töötama konkreetse aja jooksul.

Järgmises toimingus kirjeldatakse, kuidas luua projektimeeskonda.

## <a name="create-a-project-team"></a>Projektimeeskonna loomine

1. Loendi lehel **Kõik projektid** valige projekt ja valige seejärel **Redigeeri**.
2. Vahekaardil **Projektimeeskond ja ajastamine** väljal **Ajakava lõpukuupäev** sisestage ajakava algusaeg pluss üks kuu. Näiteks kui ajakava alguskuupäev on 24. juuni 2017 (24.6.2017), sisestage **24/07/2017**.
3. Valige suvand **Lisa**.
4. Paanil **Projektile rollide lisamine** väljal **Roll** valige **Vanem-projektihaldur**.
5. Valige **Nõutav pädevus**.
6. Lehel **Omaduste valimine** valitakse vaikimisi eelnevalt vanem-projektijuhi rollile määratud omadused. Valige **OK**.
7. Lehel **Projektile rollide lisamine** väljale **Ressursside arv** sisestage **1**.
8. Väljal **Ressurss** näitab otsing kõiki ressursse, millel on nõutavad omadused olemas. Valige suvad **Daniel Kangur** ja seejärel valige käsk **Loo**.
9. Lehel **Projekt** valige **Lisa**.
10. Paanil **Projektile rollide lisamine** väljal **Roll** valige **Meeskonnaliige**. Väljale **Ressursside arv** sisestage **5**.
11. Valige käsk **Loo**.
12. Lehel **Projektid** valige **Täida ressurss**.

## <a name="monitor-project-teams"></a>Projektimeeskondade jälgimine
1. Lehel **Kõik projektid** valige link **Projekti ID** projekti **XYZ värskenduse 2. etapp** jaoks.
2. Kiirkaardil **Projektimeeskond ja ajastamine** veenduge, et loetletud projektiressursid oleksid õiged.
