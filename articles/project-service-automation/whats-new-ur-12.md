---
title: Mida on uut rakenduse Project Service Automation värskenduse väljaandes 12, v3
description: Selles teemas antakse teavet selle kohta, mida on uut rakenduse Project Service Automation värskenduse väljaandes 12, v3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750965"
---
# <a name="project-service-automation-v3-update-release-12"></a>Rakenduse Project Service Automation V3, värskenduse väljaanne 12
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
