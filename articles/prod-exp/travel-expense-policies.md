---
title: Kulupoliitikate seadistamine
description: Saate rakenduses Microsoft Dynamics 365 Finance seadistada kulupoliitikad, mida teie töötajad peavad kuluaruandeid ja reisitellimusi esitades järgima.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6240a7be175800ce6f3b066de9e935ab370629ef
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650089"
---
# <a name="set-up-expense-policies"></a>Kulupoliitikate seadistamine

[!include [banner](../includes/banner.md)]

Saate määratleda poliitika, mida teie töötajad peavad kuluaruandeid ja reisitellimusi esitades järgima.         
Kulupoliitika rakendamine aitab teil tõhusalt kulusid hallata.         

Näiteks saate New York City hotellikuludele sisse seada poliitika, mis määratleb, et kulud öö kohta ei tohi ületada 250 dollarit.       
Kui töötaja esitab kuluaruande või reisitellimuse, kus toa hind ületab seda summat, teavitab süsteem sellest        
töötajat, et kulu poliitikas olev summa on ületatud. Töötaja saadava sõnumi saate konfigureerida        
poliitikat määratledes.      
        
Saate määratled kolme tüüpi poliitikaid:         
        
- Hoiatus - võimaldab töötajal kuluaruande või reisitellimuse esitada, kuid kulu märgitakse kõigile kinnitajatele ja        
  hilisemaks aruandluseks.        

- Tõrge - nõuab, et töötaja peaks enne kuluaruande või reisitellimuse esitamist kulu üle vaatama, et see vastaks poliitikale.       
 
 - Põhjendus - nõuab, et töötaja või haldur sisestaks enne kuluaruande või reisitellimuse esitamist põhjenduse poliitika summa ületamise kohta.        

## <a name="policy-tips"></a>Poliitika näpunäited
Siin on mõned soovitused, mis aitavad teil kulude haldamiseks uut poliitikat luua. 
* Poliitikad ei kehti tagasiulatuvalt ja poliitika ei kohaldu, kui see on loodud pärast kulu tekkimise kuupäeva. Näiteks kui loote täna uue poliitika, et jõustada maksimaalseks eine kuluks 50 USD, siis ei kontrollita selle poliitika suhtes mistahes olemasolevaid kulusid, mis on sisestatud eile seisuga.
* Üksikasjaliku kulukategooria jaoks poliitika loomisel arvestage, et saate lisada kulurea tüübi tingimuse. Mõni poliitika, näiteks kviitungi nõudmine, ei pruugi olla üksikasjalike ridade jaoks otstarbekas ja seda peaks rakendama ainult päisereale või mitte-üksikasjalikule reale. 
* Kulude haldamise poliitikaid hinnatakse vaikimisi selle allika olemi suhtes. Kontsernisiseste stsenaariumide puhul saate määrata poliitika, mida saab selle asemel hinnata sihtkoha olemi (laenaja olemi) suhtes. Et käivitada poliitikad sihtkoha olemi suhtes, lülitage sisse funktsioon "Hinda kulupoliitikat laenava juriidilise isiku suhtes" tööruumis **Funktsioonihaldus**.

## <a name="when-to-evaluate-policies"></a>Millal poliitikaid hinnada

Kulude haldamise parameetrites on võimalus hinnata kulu haldamise poliitikat rea salvestamisel või kuluaruande esitamisel. Kui otsustate hinnata siis, kui rida salvestatakse, kindlustab see, et kasutajatele kuvatakse varem, mida nad peavad tegema, et oma kuluaruanne korraga lõpule viia. Vastasel juhul saate poliitika hindamist edasi lükata ja aega säästa, kui valideerite end töövoo esitamise ajal lõpus.
