---
title: Toote hinnakirjad
description: Selles teemas jagatakse teavet kataloogi hinnakujunduse hinnakirjade kohta, mida kasutatakse projekti hinnapakkumiste ja lepingute jaoks.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: c0f30bec159254c078024549b7b0dd0c048ef65d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275353"
---
# <a name="product-price-lists"></a>Toote hinnakirjad

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Hinnakirjad ja hinnakirjaüksused toetavad tootekataloogi hinda. Enamasti kasutatakse seda funktsiooni projekti hinnapakkumiste ja projekti lepingute kataloogipõhiste ridade jaoks.

Projektil põhinevate ridade puhul kajastab leping lepingut pärast selle võitmist. Kuna läbirääkimiste protsess eelneb tavaliselt võidule, kopeeritakse hinnapakkumisega seotud hind alati nii nagu on uude hinnakirja ja lisatakse lepingule. Seda uut hinnakirja ei saa muuta väljaspool lepingu reguleerimisala. See piirang aitab kaitsta intressimäära kaarti, mis on kokku lepitud mis tahes hindade muudatuste põhjal, mis ilmnevad põhihinnakirjas.

Tooted tuleb seadistada nii, et neil oleksid tootekataloogi vaikimisi kulu ja hinnakiri. Kasutage vaikimisi kulu ja hinnakirja hindade konfigureerimiseks loendi hinda, standardkulu ja praegust kulu. Vaikimisi kasutatakse hinnakirja hindu hinnapakkumise real või projekti lepingurea korral ainult juhul, kui süsteem ei leia hinnapakkumise või projekti lepingu jaoks hinnakirja rida selle toote jaoks.

Tootekataloogi ridade omahinda saab muuta hinnapakkumiste vahel. See võimalus on oluline, kuna kui te kulusid täpselt ei jälgi, ei saa te projekti kaasamisel määrata operatiivset kasumit. Vaikimisi on toote standardhind omahind. Vaikimisi kasutatava omahinda saab hinnapakkumise real uuendada juhul, kui selle hinnapakkumise jaoks on teistsugune kulumäär.

## <a name="price-list-items"></a>Hinnakirjaüksused

Tooteid saate tootekataloogist lisada erinevatesse hinnakirjadesse. Toodete hinnakirja read viitavad alati kindlale ühikule. Hinnakirjaüksuse toote hinda saab konfigureerida valuuta summana. Alternatiivina saab seda konfigureerida loendi hinna, praeguse kulumäära või standardse kulumäära funktsioonina.

PSA toetab mitmesuguseid ümardamise võimalusi, kui hinnad on konfigureeritud loendi hinna, standardkulu või praeguse kulu funktsioonina. Lisaks mitme hinna meetodi ja ümardamise suvandi kasutamisele saate allahindluse loendeid seostada hinnakirja üksustega. 

Kui loote hinnapakkumise jaoks uue kohandatud hinnakirja, valides lehel **Projekti hinnapakkumine** valiku **Kohandatud hinnakiri**, tehakse hinnakirjast koopia ning uue hinnakirja päise välja **olem** väärtuseks seatakse **Müügiolem**. Uue hinnakirja nimi lisatakse hinnapakkumise nimele ja ajatemplile. Samuti saate kasutada uue hinnakirja nime ja hinnapakkumise nime kohandatud töövoogudes, et käivitada kohandatud hinnakujundust kasutavatele hinnapakkumistele täiendavat ülevaadet ja kinnitusi.

 
## <a name="default-product-price-list"></a>Toote vaikehinnakiri
Igal kliendi kirjel on väli **Vaikehinnakiri**, kus saate määrata hinnakirja, mis vastab kliendi valuutale. Sellele väljale ei sisestata automaatselt vaikeväärtust. Kui konkreetse kliendiga on olemas kohandatud hinnakujunduse leping, saate seda välja kasutada hinnakirja seostamiseks selle kliendiga.

Müügivõimaluse, hinnapakkumise ja projekti lepingu olemid kasutavad vaikimisi toodete hinnakirja sisestamiseks järgmist tellimust. Sama tellimust kasutatakse projekti hinnakirja jaoks.

1.  Hinnapakkumine
2.  Müügivõimalus
3.  Klient
4.  Globaalsätted 

Vaikimisi loetleb hinnapakkumise väli **Toode** kõik hinnapakkumise toodete hinnakirja aktiivsed tooted. Kui toode on inaktiveeritud või kui see on toote mustand, siis seda loendis pole, isegi kui see on hinnakirjas. 

Tootekataloogi read lisatakse arve ridadena esimesel arvel, mis on loodud projekti lepingu jaoks. Arve mustandi korral saab neid arve ridu kustutada. Sel juhul kuvatakse read järgneval arvel, kuni need arveldatakse, või kuni kliendile saadetakse arve. Te ei saa arve rea osalist kogust arveldada. Kui projekti lepingujärgsed toote seeriad on arveldatud, luuakse tegelikud näitajad. Need tegelikud näitajad pole seostatud projekti olemiga lingitud. Teisisõnu ei sõltu tootepõhise projekti lepinguread mis tahes projektil põhinevast kasutusest. Materjalide tarbimist projektides ei jälgita.


[!INCLUDE[footer-include](../includes/footer-banner.md)]