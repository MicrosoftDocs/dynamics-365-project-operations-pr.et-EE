---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 12, V3
description: Selles artiklis antakse teavet selle kohta, mis on uut Project Service Automation Update Release 12, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 28539b2e1331c8509e40aaf771f4d88d6f54e022
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922631"
---
# <a name="project-service-automation-update-release-12-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 12, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast rakenduse Dynamics 365 Project Service Automation (PSA) värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskust ja avage värskenduse installimiseks lahenduste leht. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse funktsioonid ja parandused, mis on project Service Automation V3, Update Release 12 jaoks uued või muudetud. Selle versiooni järgunumber on V3.10.2.34 ja see on oktoobris 2019 automaatvärskendusega kõigile saadaval.

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
