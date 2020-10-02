---
title: Müügi hinnakirja seadistamine
description: Selles teemas antakse teavet projekti hinnakujunduse müügi hinnakirjade kohta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896456"
---
# <a name="sales-price-list-setup"></a>Müügi hinnakirja seadistamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Projekti hinnapakkumiste ja lepingute puhul on projekti hinnakirjas teistsugune hinna alistamise muster kui toodete hinnakirjas. Tootekataloogil põhineval hinnapakkumise real saate hinna alistada rollidele ja kategooriatele otse pakkumise real, sest iga hinnapakkumise rida osutab täpselt ühele kataloogiüksusele. Projektil põhineva hinnapakkumise ei saa te siiski otse hinnapakkumiste real olevate rollide ja kategooriate hinda alistada. Võite kasutada projekti hinnakirja, et töötada kahe erineva alistamise mustriga.

> [!NOTE]
> Soovitame, et teil oleks oma projekti ressursside ja kataloogiüksuste jaoks eraldi hinnakiri nende kahe käitumise erinevuste tõttu, kui te alistate hinnakujunduse.

Kõigil järgmistest olemitest võib projekti hinnakujunduseks olla üks või mitu seotud müügi hinnakirja.

- Klient (konto) 
- Müügivõimalus 
- Hinnapakkumine 
- Projektileping

Nende olemite seotust hinnakirjaga näitavad projekti hinnakirjad. Saate seostada ühe või mitu hinnakirja kliendi, müügivõimaluse, hinnapakkumise ja projekti lepingu müügi olemitega.

Vaikimisi projekti hinnakirja ei sisestata kliendi kirjesse automaatselt. Siiski saate projekti hinnakirja käsitsi manustada kliendi kirjele. Sellegipoolest peaksite projekti hinnakirja käsitsi lisama ainult siis, kui teil on kliendiga kohandatud hinnakujunduse leping. 

Kui projekti hinnakiri on seotud müügiesindaja, valideeritakse järgmine teave.

- Hinnakirjal on kontekst **Müük**. 
- Hinnakirja valuuta ühtima kliendi valuutaga. 

Projekti lepingu järgmist järjestuss kasutatakse selleks, et seada seotud projekti hinnakiri automaatselt.

1. Hinnapakkumine
2. Müügivõimalus
3. Klient 
4. Globaalsätted 

Kui projekti hinnakiri on vaikimisi sisestatud, kinnitab süsteem, et valuuta vastab kliendi valuutale ja et vaikimisi määratud hinnakirjad sisaldavad konteksti **Müük**.

Saate seostada mitu projekti hinnakirja kliendi, müügivõimaluse, hinnapakkumise ja projekti lepingu olemitega. See võimalus toetab kuupäevapõhiseid vaikimisi hindu pikaajalise projektilepingu jaoks, mille puhul võib inflatsiooni tõttu tekkivate hinnavärskenduste arvestamiseks vajada mitut hinnakirja. Kui aga kliendi, müügivõimaluse, hinnapakkumise või projekti lepingu olemiga seostatud hinnakiri sisaldab kattuvat jõustumiskuupäeva, võivad vaikimisi hinnad valed olla. Seetõttu peaksite veenduma, et projekti hinnakiri, millel on kattuvad jõustumiskuupäevad, pole nende olemitega seostatud.
