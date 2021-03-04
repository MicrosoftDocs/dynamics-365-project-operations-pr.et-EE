---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 12, V3
description: Selles teemas antakse teavet selle kohta, mida on uut rakenduse Project Service Automation värskenduse väljaandes 12, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: daf0e6c7a4b1b953cb808cfefab74475c47d3996
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143823"
---
# <a name="project-service-automation-update-release-12-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 12, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast rakenduse Dynamics 365 Project Service Automation (PSA) värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskust ja avage värskenduse installimiseks lahenduste leht. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 12 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgunumber on V3.10.2.34 ja see on oktoobris 2019 automaatvärskendusega kõigile saadaval.

## <a name="update-release-12"></a>Värskenduste väljalase 12

### <a name="bug-fixes"></a>Veaparandused

- Aeg ja kulu

    - Parandatud: ajakirje tõrketeateid on värskendatud asjakohasema konteksti abil.
    - Parandatud: ajakirje ruudustik ja ajakava kuvavad vajadusel vertikaalset kerimisriba õigesti.
    - Parandatud: edastatud kulu- ja ajakirjeid saab kinnitada.
    - Parandatud: kinnituse kinnitamise dialoogisõnumi tühistamine on parandatud ja see kuvab kinnitamise olekut, kui seda on muudetud olekust **kinnitatud** olekusse **edastatud**.
    - Parandatud: väljad **hind**, **ühik** ja **kogus** on nüüd kulukirjes pärast kinnitamist lukustatud.

- Projektijuhtimine

    - Parandatud: toiming **uus** on põhivormilt **meeskonnaliige** eemaldatud.
    - Parandatud: ressursi määramised on värskendatud ja võtavad arvesse ebatäpseid ümardamisvigu, mis viivad ülesande lõpukuupäeva nihkeni.
    - Parandatud: ülesande ruudustikul tuuakse asjakohased serveripoolsed tõrked kasutajale välja.
    - Parandatud: ülesande inimeste valijas renderdatakse nüüd meeskonnaliikme nimi, mitte ametikoha nimi.

- Ressursihaldus

    - Parandatud: mallist loodud projektide ressursivajaduste üksikasjad kasutavad nüüd projekti kalendrit.
    - Parandatud: oskused ja pädevused tulevad nüüd vaikimisi rolli põhiandmetest selle rolli jaoks loodud ressursi nõudetele.

- Sales

    - Parandatud: põhivormist **Leping** on leitud topelt objekti ID-d.
    - Parandatud: loogikat on värskendatud, et muuta vahekaart **hinnapakkumise analüüs** nähtavale, nii et see kuvaks vahekaardi metaandmete seadistust.
    - Parandatud: tegeliku kirje arvestuskuupäev tuleb nüüd aja-/kulukirje kuupäevast ja mitte kinnitamise kuupäevast.


[!INCLUDE[footer-include](../includes/footer-banner.md)]