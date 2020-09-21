---
title: Täiendamise avaleht
description: Selles teemas kirjeldatakse, kust leida olulist teavet Dynamics 365 Project Service Automation uute ja muudetud funktsioonide kohta ning kuidas täiendada uusimale versioonile.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751000"
---
# <a name="upgrade-home-page"></a>Täiendamise avaleht

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Üleminek PSA versioonilt 2.x või 1.x versioonile 3.x

### <a name="new-instances"></a>Uued eksemplarid

Alates 17. maist 2019: kui uue eksemplari ettevalmistamisel valitakse Project Service Automation, installitakse vaikimisi versioon 3.x.

### <a name="existing-instances"></a>Olemasolevad eksemplarid

Varem pidi kliendid, kellel on PSA versiooni 2.x eksemplar ja vajasid värskendamist versioonile 3.x, mis on PSA ühtse kliendiliidese põhine (UCI) versioon, võtma ühendust Microsofti toega ning esitama oma eksemplari üksikasjad, et tugi saaks võimaldada eksemplari täienduse versioonile 3.x. 2020 a. 1. märtsi seisuga saavad kliendid, kellel on PSA versiooni 2.x eksemplar ja vajavad värskendamist versioonile 3.x värskendada oma eksemplarid otse administreerimisportaalist ilma, et oleks vaja Microsofti tugiteenusega ühendust võtta.  

> [!NOTE]
> PSA versioon 3.x sisaldab olulisi muudatusi. See põhineb ühtse kasutajaliidese raamistikul, mis aitab pakkuda täiustatud kasutuskogemust. Rakenduse uus versioon pakub ühtset kasutajaliidest (UI) ja järgib kiirelt reageeriva veebidisaini põhimõtteid, et tagada igasuguse ekraanisuuruse või seadme puhul optimaalne vaatamiskogemus. Rakenduses on tehtud ka muid muudatusi. Muudatusi on tehtud näiteks ka hinnakujunduses, ressursside broneerimises ja määramises, ajas, kuludes ning kinnitustes.

Enne kui alustate täiendusprotsessi, soovitame teil ära teha järgmised ülesanded.

- Kontrollige, kas nii Dynamics 365 Field Service kui ka Project Service Automation on tuvastatud eksemplarile installitud. Kui mõlemad lahendused on installitud, peaksite enne eksemplari tavapärase kasutamise jätkamist plaanima mõlema täiendamist.
- Vaadake järgmised teemad tähelepanelikult üle. Kui olete teadlik versioonidevahelistest erinevustest ja mõistate neid, aitab see teil täiendusprotsessi teha. Nendes teemades kirjeldatakse PSA-s tehtud olulisi muudatusi ning esitatakse kaalutlusi ja soovitusi versioonile 3.x ülemineku plaanimiseks.

    - [Mis on uut või muudetud Project Service Automation versioonis 3?](whats-new-changed-v3.md)
    - [Täienduse kaalutlused – üleminek Project Service Automation versioonilt 2.x või 1.x versioonile 3](upgrade-v3.md)

- Enne tootmiseksemplari täiendamist täiendage oma liivakasti eksemplari, et hinnata juurutamisel ilmnevaid muudatusi.

Kui olete eelmainitud teemad läbi vaadanud ja olete valmis täiendama PSA versioonile 3.x või UCI-põhisele versioonile, esitage Microsofti tugiteenusele oma avaldus, et muuta täiendus halduskeskuse kaudu kättesaadavaks. Esitage taotluses oma eksemplari üksikasjad.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Vanemad PSA versioonid (PSA versioon 2.x) äsja loodud eksemplaris

Alates 17. maist 2019 on kõikidel uutel eksemplaridel vaikekliendina UCI. Selle muudatusega joondamiseks valmistatakse vaikimisi ette PSA versioon 3.x ja Field Service’i versioon 8.x, sest need versioonid on loodud UCI kliendiga töötamiseks.

Alates 1. märtsist 2020 ei saa Dynamics PSA kliendid enam uusi keskkondi luua vanade PSA versioonidega, nagu näiteks PSA versiooniga 2.x või vanemaga. Iga uus keskkond saab saada ainult PSA versiooni 3.x.

> [!NOTE]
> Selleks et saada Field Service’i ja PSA rakenduste vanemaid versioone kasutades parimat kogemust, minge lehele **Süsteemisätted** ning valige välja **Kasuta ainult uut ühtset kasutajaliidest (soovitatav)** sätteks **Ei**, sest need versioonid ei ole loodud UCI-s õigesti laadimiseks. Kui olete UCI välja lülitanud, saate neid Field Service’i ja PSA versioone avada ning käivitada vana veebikliendi kaudu. UCI kliendi väljalülitamise juhised leiate jaotisest [Luba ainult ühtne kasutajaliides](../admin/enable-unified-interface-only.md).
