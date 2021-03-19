---
title: Tootekataloogi hinnakiri
description: Selles teemas antakse teavet tootekataloogi hinna kohta rakenduses Dynamics 365 Project Service Automation (PSA).
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: e3a070f2e0a13e2caff2157b200c334bc4418f0b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284038"
---
# <a name="product-catalog-pricing"></a>Tootekataloogi hinnakiri 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Hinnakirjad ja hinnakirjaüksused toetavad tootekataloogi hinda. Enamasti kasutatakse seda funktsiooni projekti hinnapakkumiste ja projekti lepingute kataloogipõhiste ridade jaoks.

Projektil põhinevate ridade puhul kajastab leping lepingut pärast selle võitmist. Kuna läbirääkimiste protsess eelneb tavaliselt võidule, kopeeritakse hinnapakkumisega seotud hind alati nii nagu on uude hinnakirja ja lisatakse lepingule. Seda uut hinnakirja ei saa muuta väljaspool lepingu reguleerimisala. See piirang aitab kaitsta intressimäära kaarti, mis on kokku lepitud mis tahes hindade muudatuste põhjal, mis ilmnevad põhihinnakirjas.

Tooted tuleb seadistada nii, et neil oleksid tootekataloogi vaikimisi kulu ja hinnakiri. Vaikimisi kulu ja hinnakirja hindade konfigureerimiseks peate kasutama loendi hinda, standardkulu ja praegust kulu. Vaikimisi kasutatakse hinnakirja hindu hinnapakkumise real või projekti lepingurea korral ainult juhul, kui süsteem ei leia hinnapakkumise või projekti lepingu jaoks hinnakirja rida selle toote jaoks.

Tootekataloogi ridade omahinda saab muuta hinnapakkumiste vahel. See võimalus on oluline, kuna kui te kulusid täpselt ei jälgi, ei saa te projekti kaasamisel määrata operatiivset kasumit. Vaikimisi on toote standardhind omahind. Vaikimisi kasutatava omahinda saab hinnapakkumise real uuendada juhul, kui selle hinnapakkumise jaoks on teistsugune kulumäär.

## <a name="price-list-items"></a>Hinnakirjaüksused

Tooteid saate tootekataloogist lisada erinevatesse hinnakirjadesse. Toodete hinnakirja read viitavad alati kindlale ühikule. Hinnakirjaüksuse toote hinda saab konfigureerida valuuta summana. Alternatiivina saab seda konfigureerida loendi hinna, praeguse kulumäära või standardse kulumäära funktsioonina.

PSA toetab mitmesuguseid ümardamise võimalusi, kui hinnad on konfigureeritud loendi hinna, standardkulu või praeguse kulu funktsioonina. Lisaks mitme hinna meetodi ja ümardamise suvandi kasutamisele saate allahindluse loendeid seostada hinnakirja üksustega. 

> ![Toodete lisamine tootekataloogist erinevatesse hinnakirjadesse](media/basic-guide-16.png)

Kui loote hinnapakkumise jaoks uue kohandatud hinnakirja, valides lehel **Projekti hinnapakkumine** valiku **Kohandatud hinnakiri**, teeb PSA hinnakirja koopia ning uue hinnakirja päise välja **olem** väärtuseks seatakse **Müügiolem**. Uue hinnakirja nimi lisatakse hinnapakkumise nimele ja ajatemplile. Samuti saate kasutada uue hinnakirja nime ja hinnapakkumise nime kohandatud töövoogudes, et käivitada kohandatud hinnakujundust kasutavatele hinnapakkumistele täiendavat ülevaadet ja kinnitusi.

 
## <a name="default-product-price-list"></a>Toote vaikehinnakiri
Igal kliendi kirjel on väli **Vaikehinnakiri**, kus saate määrata hinnakirja, mis vastab kliendi valuutale. PSA puhul ei sisestata sellele väljale automaatselt vaikeväärtust. Kui konkreetse kliendiga on olemas kohandatud hinnakujunduse leping, saate seda välja kasutada hinnakirja seostamiseks selle kliendiga.

Müügivõimaluse, hinnapakkumise ja projekti lepingu olemid kasutavad vaikimisi toodete hinnakirja sisestamiseks järgmist tellimust. Sama tellimust kasutatakse projekti hinnakirja jaoks.

1.  Hinnapakkumine
2.  Müügivõimalus
3.  Klient
4.  PSA globaalsätted

Vaikimisi loetleb hinnapakkumise väli **Toode** kõik hinnapakkumise toodete hinnakirja aktiivsed tooted. Kui toode on inaktiveeritud või kui see on toote mustand, siis seda loendis pole, isegi kui see on hinnakirjas. 

Tootekataloogi read lisatakse arve ridadena esimesel arvel, mis on loodud projekti lepingu jaoks. Arve mustandi korral saab neid arve ridu kustutada. Sel juhul kuvatakse read järgneval arvel, kuni need arveldatakse, või kuni kliendile saadetakse arve. PSA puhul ei saa arve rea osalist kogust arveldada. Kui projekti lepingujärgsed toote seeriad on arveldatud, luuakse tegelikud näitajad. Need tegelikud näitajad pole seostatud projekti olemiga lingitud. Teisisõnu ei sõltu tootepõhise projekti lepinguread mis tahes projektil põhinevast kasutusest. PSA ei jälgi materjalide tarbimist projektides.


[!INCLUDE[footer-include](../includes/footer-banner.md)]