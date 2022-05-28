---
title: Toote hinnakirjad
description: Selles teemas jagatakse teavet kataloogi hinnakujunduse hinnakirjade kohta, mida kasutatakse projekti hinnapakkumiste ja lepingute jaoks.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4feb7638dd7b6826e575d83457ae7f74ef6793bf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593239"
---
# <a name="product-price-lists"></a>Toote hinnakirjad

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

 Rakenduses Project Operations toetavad olemid **Toote hinnakirjad** ja seotud hinnakirjaüksused toodete hinnakujunduse funktsiooni projektipõhise hinnapakkumise ja lepinguridadega. Projektides kasutatavate toodete puhul kasutatakse projekti hinnakirjade hinnakirjaüksuseid. 

Tooted tuleb seadistada nii, et neil oleksid tootekataloogi vaikimisi kulu ja hinnakiri. Kasutage vaikimisi kulu ja hinnakirja hindade konfigureerimiseks loendi hinda, standardkulu ja praegust kulu. Vaikimisi kasutatakse hinnakirja hindu hinnapakkumise real või projekti lepingurea korral ainult juhul, kui süsteem ei leia hinnapakkumise või projekti lepingu jaoks hinnakirja rida selle toote jaoks.

Tootekataloogi ridade omahinda saab muuta hinnapakkumiste vahel. See võimalus on oluline, kuna kui te kulusid täpselt ei jälgi, ei saa te projekti kaasamisel määrata operatiivset kasumit. Vaikimisi on toote standardhind omahind. Vaikimisi kasutatava omahinda saab hinnapakkumise real uuendada juhul, kui selle hinnapakkumise jaoks on teistsugune kulumäär.

## <a name="price-list-items"></a>Hinnakirjaüksused

Tooteid saate tootekataloogist lisada erinevatesse hinnakirjadesse. Toodete hinnakirja read viitavad alati kindlale ühikule. Hinnakirjaüksuse toote hinda saab konfigureerida valuuta summana. Alternatiivina saab seda konfigureerida loendi hinna, praeguse kulumäära või standardse kulumäära funktsioonina.

Hinnakujunduse funktsionaalsus toetab mitmesuguseid ümardamise võimalusi, kui toote hinnad on konfigureeritud loendi hinna, standardkulu või praeguse kulu funktsioonina. Lisaks mitme hinna meetodi ja ümardamise suvandi kasutamisele saate allahindluse loendeid seostada hinnakirja üksustega. 

 
## <a name="default-product-price-list"></a>Toote vaikehinnakiri
Igal kliendi kirjel on väli **Vaikehinnakiri**, kus saate määrata hinnakirja, mis vastab kliendi valuutale. Sellele väljale ei sisestata automaatselt vaikeväärtust. Kui konkreetse kliendiga on olemas kohandatud hinnakujunduse leping, saate seda välja kasutada hinnakirja seostamiseks selle kliendiga.

Müügivõimaluse, hinnapakkumise ja projekti lepingu olemid kasutavad vaikimisi toodete hinnakirja sisestamiseks järgmist tellimust. Sama tellimust kasutatakse projekti hinnakirja jaoks.

1.  Hinnapakkumine
2.  Müügivõimalus
3.  Klient
4.  Globaalsätted 

Vaikimisi loetleb hinnapakkumise väli **Toode** kõik hinnapakkumise toodete hinnakirja aktiivsed tooted. Kui toode on inaktiveeritud või kui see on toote mustand, siis seda loendis pole, isegi kui see on hinnakirjas. 

Tootekataloogi read lisatakse arve ridadena esimesel arvel, mis on loodud projekti lepingu jaoks. Arve mustandi korral saab neid arve ridu kustutada. Sel juhul kuvatakse read järgneval arvel, kuni need arveldatakse, või kuni kliendile saadetakse arve. Te ei saa arve rea osalist kogust arveldada. Kui projekti lepingujärgsed toote seeriad on arveldatud, luuakse tegelikud näitajad. Need tegelikud näitajad pole seostatud projekti olemiga lingitud. Teisisõnu ei sõltu tootepõhise projekti lepinguread mis tahes projektil põhinevast kasutusest. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
