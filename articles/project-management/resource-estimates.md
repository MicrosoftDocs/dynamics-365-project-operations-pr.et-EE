---
title: Projektide ressursi aja finantsprognoosid
description: See artikkel annab teavet, kuidas aja finantsprognoose arvutatakse.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03416feb178d883bba57dc14692049503b151ffd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913523"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Projektide ressursi aja finantsprognoosid

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Aja finantsprognoosid arvutatakse kolme teguri alusel. 

- Projektiplaani igale lehele määratud üldise või nimelise meeskonnaliikme tüüp. 
- Töö tüüp või keerukus.
- Ressursi ülesandele määramise panuse jaotumine. 

Kaks esimest tegurit mõjutavad ressursi määramise ühikukulu või arve määra. Ressursi määramise ühikukulu või arve määr on määratletud määratud ressursi atribuutidega. Need atribuudid sisaldavad organisatsiooniüksust, kuhu ressurss kuulub, ja ressursi standardrolli. Samuti saate lisada ressursile oma ettevõtte jaoks olulisi kohandatud atribuute (nt standardnimetus või kogemuse tase) ja lasta neil mõjutada ühikukulu või määramise arvelduskulu.
Lisaks ressursi atribuutidele võivad üksuse arvelduskulu või määramise kulumäära mõjutada töö atribuudid (nt ülesanne). Näiteks kui teatud tööülesanded on keerukamad, on nendele konkreetsetele ülesannetele ressursi määramise tulemuseks kõrgem ühikukulu või arveldusmäär kui vähem keerukamatel.   

Kolmas tegur tagab selle määraga tundide koguse. Juhtumites, kus ülesanne katab kahte hinnaperioodi, on tõenäoline, et selle ülesanne ressursi määramise esimese osa kulud ja hind arvestatakse ülesande teisest osast erinevalt. Iga ressursi määramise panuse prognoosimine on kompleksne väärtus, mis salvestatakse igapäevaste vahendite jaotusega.

Üksikasjalikke juhiseid töö ja ressursside kohandatud atribuutide hinnakujunduse ja kulude kogumina häälestamise kohta vaadake teemast [Hinnadimensioonide ülevaade](../pricing-costing/pricing-dimensions-overview.md).

Iga ressursi määramise finantsprognoos arvutatakse **ülesande määr/tund korrutatuna tundide arvuga.**  Sarnaselt panuse prognoosile on iga ressursi määramise kulu ja tulu finantsprognoos keerukas väärtus, mis salvestatakse igapäevase rahasumma jaotusega päeva kohta. 

## <a name="summarizing-financial-estimates-for-time"></a>Aja finantsprognooside summeerimine
Lehe ülesande aja finantsprognoos on kõigi selle ülesande ressursi määramiste finantsprognooside summa.

Ülemülesande kokkuvõtte aja finantsprognoos on kõigi selle alamülesannete finantsprognooside summa. See on projekti eeldatav tööjõukulu. 

![Ressursi prognoosid.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Vaikimisi omahinna ja kulu valuuta

Vaikimisi omahind pärineb projekti lepinguüksusele lisatud hinnakirjadest. Projekti kuluvaluuta on alati projekti lepinguüksuse valuuta. Ressursi määramisel salvestatakse kulu finantsprognoos projekti kuluvaluutas. Mõnikord erineb valuuta, milles kulumäär hinnakirjas on häälestatud, projekti kuluvaluutast. Sel juhul teisendab rakendus valuuta, milles projekti valuuta omahind on seadistatud. Ruudustikus **Prognoosid** kuvatakse ja summeeritakse kõik kuluprognoosid projekti kuluvaluutas. 

## <a name="default-bill-rate-and-sales-currency"></a>Arvelduskulu ja müügivaluuta vaikeväärtused

Vaikemüügihind pärineb seotud projektilepingule lisatud projekti hinnakirjadest, kui tehing on võidetud, või seotud projekti hinnapakkumisest, kui tehing on veel müügieelses etapis. Projekti müügivaluuta on alati projekti hinnapakkumise või projektilepingu valuutas. Ressursi määramisel salvestatakse müügi finantsprognoos projekti müügivaluutas. Erinevalt kulust ei saa hinnakirjas seadistatud müügihinnad kunagi erineda projekti müügivaluutast. Valuuta teisendamiseks stsenaariumi pole. Ruudustikus **Prognoosid** kuvatakse ja summeeritakse kõik müügiprognoosid projekti müügivaluutas. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
