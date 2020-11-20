---
title: Broneeringute ja määramiste vastavusse viimine
description: Selles teemas antakse teavet tegelike näitajate kohta.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f5255b4aa2c6c8b7fa7320da2e10b2ed23a88fdd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120448"
---
# <a name="reconcile-bookings-and-assignments"></a>Broneeringute ja määramiste vastavusse viimine

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektimeeskonna liikme projekti broneeringud ja projekti ülesannete määramised on lõdvalt seotud. Seega võib ressursil olla ülesannete määramisi, mis ei vasta broneeringutele ja broneeringuid, mis ei vasta ülesannete määramistele. Ideaaljuhul on projekti broneeringud ja määramised joondatud, nii et ressurssidel on ülesannete määramiste tegemiseks kooskõlastatud võimsus. Kuid reaalsus on see, et broneeringud võivad ilmneda vastavalt saadavusele ja ülesannete ajastus võib projekti edenedes muutuda. Seega võimaldab lõtv seotus paindlikkust.

Projekti broneeringute ja ülesannete määramiste lõdva seotuse tõttu on projektiolemisse lisatud vahekaart **Vastavusseviimine**. See vahekaart aitab projektijuhtidel ühitada oma meeskonna jaoks meeskonnaliikmete broneeringuid ja määramisi.

Iga nimega meeskonnaliikme jaoks kuvab vahekaart **Vastavusseviimine** broneeringud ja määramised kuni üksiku ülesande määramiseni. See näitab tunde lahtrites, mis võivad esindada ajavahemikke kuude ja päevade kaupa.

Väljal **Ajaskaala** saate teha valiku **Kuu**, **Nädal** või **Päev**. Vaikimisi on valitud **Nädal**. Vaikeväärtust saate muuta, kui valite nupu **Sätted**. Vahekaardi **Vastavusseviimine** avamisel kuvatakse seal praegune kuupäev, kuid te saate kalendri juhtelemendi abil liikuda ajas edasi või tagasi. Kui projekti alguskuupäev on tulevikus, kuvatakse vahekaardi avamisel see kuupäev. Kalendri juhtelemendil on ka suvandeid, mis võimaldavad teil liikuda projekti algus- ja lõppkuupäevade juurde.

Saate kasutada iga ressursi puhul laiendaja juhtelemente, et kuvada selle ressursi broneeringute üksikasjad. Samuti saate laiendada iga ressursi määramised üksiku ülesande tasemele.

Vahekaardi **Vastavusseviimine** allosas kuvatakse projekti üldine netosumma ja vahekaart sisaldab ka kogusumma veergu. Iga ressursi puhul võtab vahekaart meeskonnaliikme projekti broneeringute ja selle meeskonnaliikme ülesannete määramiste ümberarvestuse erinevuse. Ideaalis peaks erinevus olema 0 (null). Teisisõnu ei tohiks ressursi broneeringute ja tema ülesannete määramiste vahel olla erinevust. Erinevused tähistatakse värvi ja varjustusega, et oleks võimalik välja kutsuda kaks tingimust.

- **Broneeringu puudujääk** – broneeringu puudujäägid ilmnevad siis, kui ressursil on rohkem määramisi kui broneeringuid. Kuna seda võimsust pole reserveeritud, saab projektijuht seda tingimust parandada, pikendades ressursi broneeringuid puudujäägi katteks.
- **Liigsed broneeringud** – üleliigsed broneeringud ilmnevad, kui ressurss on projektile broneeritud, kuid seda pole ülesannetele määratud. See tingimus võib olla vastuvõetav, kui näiteks ressurss on broneeritud enne ülesande määramise toimumist. Kuid muudel juhtudel ei pruugi ressursi määramine plaanis olla. Sellisel juhul peaks projektijuht kaaluma ressursi broneeringute tühistamist, et võimsust saaks kasutada mõne muu projekti jaoks.

> [!NOTE]
> Nende tingimuste legend võib olla peidetud, et jätta ruudustikule rohkem ruumi. Sellisel juhul saate legendi nähtavaks muuta, kui valite nupu **Sätted**.

Mõnel juhul, kui väli **Ajaskaala** on määratud tasemele, mis on suurem kui **Päev**, võib erinevused arvutada nullina (0). Näiteks tasemel **Kuu** võib ressursi netoerinevus olla 0 (null), mis näitab, et broneeringud on määramistega võrdsed. Kuid kui te vaatate taset **Nädal**, võite näha, et seal on määramised 0 (null) tundi ja broneeringud 40 tundi esimesel kuu nädalal, kuid määramine 40 tundi ja broneerimine 0 (null) tundi kuu teisel nädalal. Kuigi selle kuu broneeringud ja määramised on võrdsed, seisneb erinevus nädalas.

Kõrgemate ajatasemete vaatamisel kuvatakse vahekaardil **Vastavusseviimine** lahtrite indikaator, mis teavitab teid, et madalamatel ajatasemetel on erinevusi. Näiteks kuvatakse järgmisel joonisel lahtri indikaator 2018. aasta oktoobrikuu lahtris ressursile, mille nimi on Iris Mäe. Seega näete, et kuigi ressursi broneeringud ja määramised on tasemel **Kuu** summeerituna võrdsed, ei ühti need madalamatel tasemetel.

![Sobimatud broneeringud ja määramised igakuisel tasemel](media/reconcile-assignments-01.JPG)

Topeltklõpsake lahtrit, et suumida järgmisele madalamale tasemele ja vaadata erinevust. Näiteks kui topeltklõpsate 2018. aasta oktoobrikuu erinevust Iris Mäe jaoks, lähete süvitsi tasemele **Nädal**. Seejärel näete, et ressursil on broneeritud 16 tundi, kuid oktoobri kahel esimesel nädalal pole ühtegi määramist, ja on 16 tundi määramisi, kuid mitte ühtegi broneeringut oktoobri kolmandal nädalal.

![Sobimatud broneeringud ja määramised iganädalasel tasemel](media/reconcile-assignments-02.JPG)

Järgmiselt kõrgemalt tasemelt välja suumimiseks saate lahtrit paremklõpsata. Samuti saate lahtri indikaatori välja lülitada, kui valite nupu **Sätted**. 

Projekti erinevuste vahel liikumiseks saate kasutada ka ruudustiku kohal olevaid nuppe **Eelmine** ja **Järgmine**. Nende nuppude kasutamiseks peate esmalt valima ressursi. Valige nupp **Järgmine**, et minna järgmisele selle ressursi broneeringute ja määramiste vahelisele erinevusele. Eelmise erinevuse juurde minemiseks tehke valik **Eelmine**.

Olukordades, kus teil on ressursi jaoks ülesannete määramised, kuid mitte broneeringuid, saate valida broneeringu puudujäägi ja seejärel teha valiku **Pikenda broneeringut**. Seejärel saate vaadata broneeringut, mis on vajalik ressursi puudujäägi kõrvaldamiseks. Samuti saate vaadata ressursi broneeringuid praeguse projekti ja muude projektide kohta. Ressursile broneeringu tegemiseks praegust saadavust arvesse võtmata klõpsake nuppu **OK**. Projektijuht või ressursihaldur saab seejärel kasutada ajakavapaneeli, et hallata olukordi, kus ressursi broneeringud ületavad võimsust, kuna ressursi broneeringuid pikendati.

## <a name="managing-with-time-zones"></a>Ajavööndite haldamine
Selleks et tagada täpsed ja prognoositavad tulemused broneeringu pikendamisel, peavad olema täidetud kaks peamist eeltingimust:  

- Kasutaja peab konfigureerima oma seadme ajavööndi, et see vastaks teie süsteemi isikupärastamise sätetes määratletud ajavööndile.
 
  ![Ajavööndi sätted operatsioonisüsteemis Windows 10](media/reconcile-assignments-03.png)

  ![Ajavööndi sätted isikupärastamise sätetes](media/reconcile-assignments-04.png)
 
- Broneeritaval ressursil peab olema vähemalt üks minut tööaega, mis kattub kontuuridega, mida kasutatakse taotletud laienduse määratlemiseks. Näiteks on järgmises näites toodud ülevaate ressursse tööajaga, mis jääb vahemikku 9:00 ja 19:00. 

  ![Ressursi kontuuride võrdlus](media/reconcile-assignments-05.png)

Järgnev tabel näitab järgmist.

- Projekti kalendri mall.
- Ressurss A: sellel ressursil on sama kalender ja see on projektiga samas ajavööndis. Broneeringute algusaeg on 9:00.
- Ressursid B: see ressurss asub erinevas ajavööndis kui projekt ja seetõttu algab oma ajavööndis kell 7:00. Kuid broneeringud algavad kell 9:00, kuna see on määramise kontuuri varaseim alguskellaaeg.
- Ressursid C ja D: ressursid asuvad ka erinevates ajavööndites, nii üksteisest kui ka projektist erinevates, ning nende broneeringud ei alga varem kui nende vastavad saadaolevad alguskellaajad.

|Olem  |Calendar  |
|-|-|
|Projekti kalendri mall   | ![projekti kalender](media/reconcile-assignments-06.png) |
|Ressurss A  | ![Ressursi A kalender](media/reconcile-assignments-06.png) |
|Ressurss B  |  ![Ressursi B kalender](media/reconcile-assignments-07.png) |
|Ressurss C  |  ![Ressursi C kalender](media/reconcile-assignments-08.png) |
|Ressurss D  | ![Ressursi D kalender](media/reconcile-assignments-09.png)  |
 
Kui liigute vastavusse viimise vaatesse, siis kuvatakse ressursimääramisi ja seotud broneeringu puudujääke.
 ![Vastavusseviimise vaade enne pikendamist](media/reconcile-assignments-10.png)

Pärast broneeringu pikendamise funktsiooni käivitamist iga ressursi puhul, pikendatakse edukalt iga ressursi broneeringuid. Põhjus on selles, et iga ressursi tööaeg kattus puudujäägi kontuuriga.
 ![Vastavusseviimise vaade pärast broneeringu pikendamist](media/reconcile-assignments-11.png) 

Kuid broneeringute üksikasjade täpsem vaatlemine näitab erinevusi broneeringute algusajas. Broneeringud ei alga varem kui määramise kontuuri alguskellaaeg ega varem kui ressursi saadaolev alguskellaaeg.
 ![Ajakavapaneelil olevate ressursside uued broneeringud](media/reconcile-assignments-12.png)
