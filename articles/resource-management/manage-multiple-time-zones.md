---
title: Ajavööndite haldamine
description: Projekti loomisel põhineb selle ajavöönd rakendatud töötunni mallis määratletud ajavööndil.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074894"
---
# <a name="manage-time-zones"></a>Ajavööndite haldamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


## <a name="projects"></a>Projektid

Projekti loomisel põhineb selle ajavöönd rakendatud töötunni mallis määratletud ajavööndil. **Projektis** on kuupäevad alati seotud igale vahekaardile sisse logitud kasutaja ajavööndiga, välja arvatud vahekaardil **Ülesanne**. Tööjaotuse struktuuri kuvamisel kuvatakse kuupäevad alati projekti ajavööndis.

## <a name="tasks"></a>Ülesanded

Ülesande loomisel kontrollivad algusaega, lõpuaega ja tundi/päeva projekti töötunnid. Näiteks kui ülesanne luuakse projektiga, mille ajavöönd on –8 PST ja selle töötunnid on esmaspäevast reedeni 9.00–17.00, arvestavad kõik ülesanded, mis on loodud ilma määramiseta, projekti kalendri algusaja ja lõpuajaga.

## <a name="manage-resources-with-time-zones"></a>Ajavöönditega ressursside haldamine

Suvandi **Broneeringu pikendamine** kasutamisel täpsete ja prognoositavate tulemite jaoks on vaja täita kaks olulist eeltingimust.  

- Kasutaja peab konfigureerima oma seadme ajavööndi, et see vastaks süsteemi suvandis **Isikupärastamise sätted** määratletud ajavööndile.
 
  ![Ajavööndi sätted operatsioonisüsteemis Windows 10](media/reconcile-assignments-03.png)

  ![Ajavööndi sätted isikupärastamise sätetes](media/reconcile-assignments-04.png)
 
- Broneeritaval ressursil peab olema vähemalt üks minut tööaega, mis kattub kontuuridega, mida kasutatakse taotletud laienduse määratlemiseks. Näiteks järgmised ressursid, mille tööaeg jääb vahemikku 9.00–19.00. 

  ![Ressursi kontuuride võrdlus](media/reconcile-assignments-05.png)

Järgnev tabel näitab järgmist.

- Projekti kalendri mall
- Ressurss A: sellel ressursil on sama kalender ja see on projektiga samas ajavööndis. Broneeringute algusaeg on 9:00.
- Ressurss B: see ressurss asub erinevas ajavööndis kui projekt ja alustab oma ajavööndis kell 7.00. Kuid broneeringud algavad kell 9:00, kuna see on määramise kontuuri varaseim alguskellaaeg.
- Ressursid C ja D: ressursid asuvad erinevates ajavööndites, mõlemad erinevad üksteise ja projekti ajavööndist, ja nende broneeringud ei alga varem kui nende vastavad saadavuse algusajad.

|Olem  |Calendar  |
|-|-|
|Projekti kalendri mall   | ![projekti kalender](media/reconcile-assignments-06.png) |
|Ressurss A  | ![Ressursi A kalender](media/reconcile-assignments-06.png) |
|Ressurss B  |  ![Ressursi B kalender](media/reconcile-assignments-07.png) |
|Ressurss C  |  ![Ressursi C kalender](media/reconcile-assignments-08.png) |
|Ressurss D  | ![Ressursi D kalender](media/reconcile-assignments-09.png)  |
 
Kui liigute vaatesse **Vastavusse viimine** , kuvatakse ressursi määramised ja seostatud broneeringu puudujäägid.

![Vastavusseviimise vaade enne pikendamist](media/reconcile-assignments-10.png)

Kui iga ressursi jaoks on kasutatud broneeringu pikendamise funktsiooni, pikendatakse iga ressursi broneeringuid, kuna iga ressursi tööajad kattuvad puudujäägi kontuuridega.

![Vastavusseviimise vaade pärast broneeringu pikendamist](media/reconcile-assignments-11.png) 

Pange tähele, et broneeringute üksikasjade täpsem vaatamine näitab, et broneeringute algusaeg on erinev. Broneeringud ei alusta varem kui määramise kontuuri algusaeg ja mitte varem kui ressursi saadavuse algusaeg.

![Ajakavapaneelil olevate ressursside uued broneeringud](media/reconcile-assignments-12.png)
