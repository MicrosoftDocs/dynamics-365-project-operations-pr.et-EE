---
title: Kulupoliitika määratlemine
description: Saate määratleda kulupoliitika, mida teie töötajad peavad kuluaruandeid ja reisitellimusi esitades järgima.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 30b3a0e1547ca7043b1433da2b4ebf02f2b473a1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075026"
---
# <a name="define-expense-policies"></a>Kulupoliitika määratlemine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Saate määratleda poliitika, mida teie töötajad peavad kuluaruandeid ja reisitellimusi esitades järgima.         
Kulupoliitika rakendamine aitab teil tõhusalt kulusid hallata.         

Näiteks saate New York City hotellikuludele sisse seada poliitika, mis määratleb, et kulud öö kohta ei tohi ületada 250 dollarit.       
Kui töötaja esitab kuluaruande või reisitellimuse, kus toa hind ületab seda summat, teavitab süsteem sellest         
töötajat, et kulu poliitikas olev summa on ületatud. Töötaja saadava sõnumi saate konfigureerida        
poliitikat määratledes.      
        
Saate määratled kolme tüüpi poliitikaid:         
        
- **Hoiatus** : võimaldab töötajal kuluaruande või reisitellimuse esitada, kuid kulu märgitakse kõigile kinnitajatele ja         
  hilisemaks aruandluseks.        

- **Tõrge** : nõuab, et töötaja peaks enne kuluaruande või reisitellimuse esitamist kulu üle vaatama, et see vastaks poliitikale.        
 
 - **Põhjendus** : nõuab, et töötaja või haldur sisestaks enne kuluaruande või reisitellimuse esitamist põhjenduse poliitika summa ületamise kohta.        

## <a name="policy-tips"></a>Poliitika näpunäited
Siin on mõned soovitused, mis aitavad teil kulude haldamiseks uut poliitikat luua. 

- Poliitikad ei kehti tagasiulatuvalt, mis tähendab, et poliitika ei kohaldu, kui see on loodud pärast kulu tekkimise kuupäeva. Näiteks saate luua uue poliitika täna, et kehtestada maksimaalseks toidukuluks 50 dollarit. Kõiki eile sisestatud kulusid ei kontrollita selle poliitika suhtes.
- Üksikasjaliku kulukategooria jaoks poliitika loomisel arvestage, et saate lisada kulurea tüübi tingimuse. Teatud poliitikad (nt kviitungi nõudmine) ei pruugi konkreetsete ridade jaoks mõistlik olla. Sellisel juhul rakendatakse seda poliitikat ainult päisereale või mitte-üksikasjalikule reale. 
- Kulude haldamise poliitikaid hinnatakse vaikimisi selle allika olemi suhtes. Kontsernisiseste stsenaariumide puhul saate määrata poliitika, mida saab selle asemel hinnata sihtkoha olemi (laenaja olemi) suhtes. Et käivitada poliitikad sihtkoha olemi suhtes, lülitage sisse funktsioon **Hinda kulupoliitikat laenava juriidilise isiku suhtes** tööruumis **Funktsioonihaldus**.

## <a name="when-to-evaluate-policies"></a>Millal poliitikaid hinnada

Kulude haldamise parameetrites saate valida, et hinnata kulu haldamise poliitikat rea salvestamisel või kuluaruande esitamisel. Kui otsustate hinnata siis, kui rida salvestatakse, kuvatakse kasutajatele varem, mida nad peavad tegema, et oma kuluaruanne korraga lõpule viia. Vastasel juhul saate poliitika hindamist edasi lükata ja aega säästa, kui valideerite end töövoo esitamise ajal lõpus.
