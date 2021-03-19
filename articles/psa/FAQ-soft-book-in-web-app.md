---
title: Kuidas ressursse rakenduse versioonis 2.x esialgselt reserveerida?
description: Selles artiklis kirjeldatakse, kuidas Project Service’iga projektimeeskonna liikmeid esialgselt reserveerida.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 18a1176c131e233f62f74dc0dd8a6aa3ee561da5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286018"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Kuidas ressursse veebirakenduses (Project Service'i rakendus v2.x) esialgselt reserveerida?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Saate ressurssi esialgselt projektimeeskonda reserveerida, andmaks teada, et planeerite ressursi projekti määrata. Esialgselt reserveerimised ei lisa ressursile koormust. Esialgselt reserveeritud meeskonnaliikmetele pole võimalik projekti ülesandeid määrata. Ülesandeid saab määrata ainult sellistele ressurssidele, kellel on olek Fikseeritult reserveeritud ja kinnitamise tüüp Kinnitatud (eeldusel, et neil on ülesande täitmiseks piisavalt fikseeritult reserveeritud tunde).

Esialgselt reserveeritud meeskonnaliikmed kuvatakse ruudustikus Meeskonnaliige koos nende esialgselt reserveeritud tundidega veerus Esialgselt reserveerimine. Nad kuvatakse ka ajakavapaneelil. Need ei lisa ressursile koormust, kuna esialgselt reserveerimine ei lisa ressursile koormust.

Rakenduse Project Service versiooniga 2.x on meeskonnaliikme esialgseks projekti reserveerimiseks kolm võimalust. Saate esialgselt reserveerida ajakavapaneelil, funktsiooniga Reserveeringute haldamine või üldise ressursi loomisega. Neid meetodeid on kirjeldatud allpool.

## <a name="soft-book-with-the-schedule-board"></a>Esialgselt reserveerimine ajakavapaneelil

Tehke ajakavapaneelil ressursi esialgselt reserveerimiseks järgmist. 
1. Avage ajakavapaneel.
2. Valige ajakavapaneeli alumise paneeli Broneeringu nõuded vahekaart Projekt.
3. Leidke projekt, kuhu soovite ressursi esialgselt reserveerida. Kui teil on mitu projekti, klõpsake veeru Projekt päist ja kasutage projekti otsimiseks filtreerimistööriista.
4. Klõpsake projekti ja lohistage see ressursi ajaruudustikku.
5. See avab paremal paneeli Ressursi broneeringu loomine. Täpsustage algus- ja lõppkuupäeva, valige broneeringu olekuks Esialgne ja määrake tunnid. 
6. Klõpsake valikut Broneeri.
7. Projekti naastes kuvatakse ressurss veerus Esialgselt reserveerimine meeskonnaliikmena koos esialgselt reserveeritud tundidega.

Pange tähele, et te ei saa neile tööjaotuse struktuuris (WBS) ülesandeid määrata, kuna selleks peaks ressurss olema kindlalt reserveeritud.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Esialgselt reserveerimine funktsiooniga Reserveeringute haldamine

Tehke funktsiooniga Reserveeringute haldamine esialgselt reserveerimiseks järgmist.
1. Klõpsake meeskonnaliikme ruudustikus käsku Uus.
2. Valige reserveeritav ressurss, roll, algus-/lõppkuupäev.
3. Valige mis tahes eraldusmeetod peale valiku Puudub.
- Täiskoormus
- Osakoormus
- Jaga ühtlaselt tundide järgi
- Jaga eesmine koormus tundide järgi
4. Klõpsake nuppu Salvesta. Näete ressurssi meeskonnaruudustikus ja tunde olekuga Fikseeritud.
5. Klõpsake ressursi reserveerimiste haldamiseks valikut Reserveeringute haldamine.
6. Kui ajakavapaneel avatakse, laiendage ressurssi ressursi reserveerimiste vaatamiseks. Reserveerimine kuvatakse olekuga Fikseeritud.
7. Paremklõpsake reserveerimist ja valige jaotises Oleku muutmine Esialgselt reserveerimine ja seejärel Esialgne. Nüüd on broneeringu olek Esialgne.
8. Pärast ajakavapaneeli sulgemist näete, et ressursi tunnid meeskonnaliikme ruudustikus on muudetud olekust Fikseeritud olekusse Esialgne.
Pange tähele, et kui reserveerite ressursi meeskonda ja määrate talle WBS-is ülesandeid, eemaldatakse ressursile määratud ülesanded reserveeringute haldamises tehtud kindlast esialgseks muutmise järel, kuna ülesandeid saab määrata ainult kindalt reserveeritud ressurssidele.

## <a name="soft-book-by-creating-a-generic-resource"></a>Esialgselt reserveerimine üldise ressursi loomisega

Saate luua esialgse reserveerimise, kui loote üldise ressursi meeskonnaliikme, täidate ajakavapaneeli või ressursitaotluse ja muudate reserveerimisel tüüpi.
Seda saate teha järgmiselt.

1. Määrake rollidele, millele soovite üldiseid meeskonnaliikmeid luua, ülesanded projekti WBS-is.
2. Klõpsake valikut Projektimeeskonna loomine.
3. Valige projekti meeskonnaliikme ruudustikus üldine ressurss ja klõpsake valikut Broneeri.
4. Valige ajakavapaneelil ressurss, mille soovite broneerida.
5. Muutke ajakavapaneeli paneelil Ressursi broneeringu loomine reserveerimise olekuks Esialgne.
6. Klõpsake valikut Broneeri või Broneeri ja välju.

Pärast ajakavapaneeli sulgemist näete, et valitud ressurss lisati koos esialgselt reserveerimise ja määratud tundidega meeskonda. Samuti näete, et üldine ressurss jääb meeskonda, märkimaks, et esialgselt reserveeritud meeskonnaliikmele on ülesanded määratud.

Kui olete valmis esialgselt reserveeritud meeskonnaliikme ressursi kindlaks meeskonnaliikmeks määrama, et talle ülesandeid määrata, tehke järgmist.

1. Valige ressurss ja klõpsake valikut Reserveeringute haldamine.
2. Kui ajakavapaneel avatakse, laiendage ressurssi ressursi reserveerimiste vaatamiseks. Reserveerimine kuvatakse olekuga Esialgne.
3. Paremklõpsake reserveerimist ja valige jaotises Reserveeringute haldamine Fikseeritult reserveerimine ja seejärel Fikseeritud. Nüüd on broneeringu olek Fikseeritud.
4. Pärast ajakavapaneeli sulgemist näete, et ressursi tunnid meeskonnaliikme ruudustikus on muudetud olekust Esialgne olekusse Fikseeritud. Nüüd saate ressursile ülesandeid määrata (eeldusel, et kindlalt reserveeritud tunnid ja ülesande täitmiseks kuluvad tunnid on omavahel kooskõlas). Pange tähele, et kui järgisite üldise ressursi täitmiseks ülalpool 3. üksuses toodud toiminguid esialgselt reserveeritud ressursi muutmiseks kindlaks reserveerimiseks, siis eemaldatakse üldine meeskonnaliige meeskonnast.


[!INCLUDE[footer-include](../includes/footer-banner.md)]