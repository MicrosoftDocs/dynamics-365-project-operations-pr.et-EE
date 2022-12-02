---
title: Väline ajastamine
description: See artikkel annab teavet arvete välise ajastamise kohta.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736983"
---
# <a name="external-scheduling"></a>Väline ajastamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Väline ajastamisrežiim võimaldab teil luua, ajakohastada ja kustutada tööde jaotusstruktuuridega (WBS) seotud üksusi, kuid ilma praeguste piiranguteta, mida Microsoft Project for the Web rakendab. Samuti pakub see piiratud kinnitamist. Seda režiimi peaksid kasutama ainult järgmised kliendid.

- Kliendid, kellel on vahendid, mis on vajalikud WBS-i määratlemiseks väljaspool rakenduse Project Operations poolt pakutavat ajakava loogikat.
- Kliendid, kes peavad haldama ajakava hierarhiat, sõltuvusi või ülesannete kestust

> [!IMPORTANT]
> Andmed, mis ei ole korrektselt sisestatud WBS-iga seotud üksustesse, ei pruugi olla kuvatud ressursside kooskõlastamise ruudustikus, hinnangute ruudustikus, jälgimisruudustikus või ressursside määramise ruudustikus.

## <a name="configuration"></a>Konfiguratsioon

See funktsioon on vaikimisi sisse lülitatud. Kuid projektide kastivälisel avalehel ei ole seotud väli vaikimisi nähtav. Välja lubamiseks avage Maker portali projektiüksuse pealeht, valige väli **Ajastamismootor** ja seejärel muutke väli **Vaikimisi nähtav**. Kui te ei kasuta valmis projekti pealehte, redigeerige oma olemasolevat lehte ja lisage sinna väli **Ajastamismootor**.

## <a name="settings"></a>Sätted

Välise ajastamisrežiimi kasutamiseks peate kõigepealt looma uue projekti ja valima projekti pealehel olevas rippmenüüst **Väliselt ajastatud**. Kui see režiim on projektile määratud, ei saa seda enam muuta.

## <a name="viewing-the-wbs"></a>WBS-i vaatamine

Kui projekt on väliselt ajastatud, on juurdepääs Project for the Webile selle projekti jaoks piiratud. WBS-i vaatamiseks peate minema jälgimisvõrku, kus on näidatud kogu WBS.

## <a name="creating-and-editing-the-wbs"></a>WBS-i loomine ja redigeerimine

Kui projekti jaoks on sisse lülitatud väline ajakava, peate määratlema andmed kõigi WBS-iga seotud üksuste, sealhulgas ülesannete, meeskonnaliikmete, ressursside määramise ja sõltuvuste kohta.

Järgneval joonisel on näidatud projekti planeerimise andmemudel.

![Projekti planeerimise andmemudel.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Funktsionaalsed piirangud

Järgmised toimingud ei ole lubatud väliselt ajastatud projektide puhul.

### <a name="project-planning"></a>Projekti kavandamine

- **Projekti kopeerimine** – See toiming ei ole toetatud väliselt ajastatud projektide puhul.
- **Projekti teisaldamine** – projekti alguskuupäeva muutmine ei muuda ülesannete algust ega ressursside määramist WBS-is.
- **Projektijuhi värskendamine** – projekti avalehel tehtud projektijuhi muudatused ei loo automaatselt uut projektimeeskonna liiget enne, kui projekt on teisendatud.
- **Projekti töötundide malli värskendamine** – projekti töötundide malli muutmine ei arvuta projekti ajakava ümber.
- **Ressursi määramise kontuurid** – ressursside määramise loomine ei värskenda automaatselt välja **mdyn\_PlannedWork**. Seda välja kasutatakse kontuuride salvestamiseks ressursside määramise jaoks. Kui näitate ressursi määramise ruudustikus või ressursi vastavuse ruudustikus ajafaasilist pingutust, peate määratlema kehtivad ressursi määramise kontuurid. Need kontuurid peavad olema õigesti vormindatud, et need käivitaksid nii kulukontuuride kui ka müügihinna kontuuride arvutamise. Soovitame luua testprojekti, mille ajastab Project for the Web, ja seejärel vaadata üle seotud andmed, et kinnitada nõudeid ja vormingut.

### <a name="resource-management"></a>Ressursihaldus

- **Üldine ressursi täitmine** – väliselt ajastatud projektide puhul üldist ressursside täitmist ei toetata. Aktiivsete avatud nõuete täitmise katsed loovad uusi projektimeeskonna liikmeid, kuid see ei kustuta üldist meeskonnaliiget ega asenda üldist meeskonnaliiget olemasolevate ressursiülesannete puhul.
- **Meeskonna liikme kustutamine** – meeskonnaliikme kustutamine ei kustuta automaatselt ressursimääranguid.

### <a name="quoting-and-contracting"></a>Hinnapakkumine ja lepingute sõlmimine

- **Hinnapakkumise rea ja lepingurea üksikasjade importimine** – kui projektist imporditakse hinnapakkumise või lepingurea üksikasjad, on rakendust testitud nii, et see toetab WBA-s maksimaalselt 500 ülesannet, võttes aluseks 20 ülesande piirangu ühe ülesande kohta.

### <a name="actuals-and-invoicing"></a>Tegelikud näitajad ja arveldamine

- Kuigi WBS-i ja finantstehingutevahelised olemasolevad kinnitamised ei muutu, on oluline, et järgiksite valmis andmemudelit, et tagada kõigi järgnevate tehingute ootuspärane toimimine.
