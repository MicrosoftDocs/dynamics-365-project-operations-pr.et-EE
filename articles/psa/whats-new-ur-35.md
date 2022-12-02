---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 35, V3
description: Selles artiklis loetletakse funktsioonid ja parandused, mis on saadaval rakenduse Microsoft Dynamics 365 Project Service Automation värskenduse väljaandes 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 28b4a5ccbfff83c9b1a18cb0b4062af9cdaf8f6e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912833"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 35, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse Project Service Automationi värskenduse väljalaske 35, V 3 uued või muudetud funktsioonid ja parandused. Selle versiooni järgunumber on V3.10.56.110 ja see on üldsusele isevärskenduse kaudu kättesaadav septembris 2021.

## <a name="update-release-35"></a>Värskenduste väljalase 35

### <a name="bug-fixes"></a>Veaparandused

Lahendatud on järgmised probleemid.

**Aeg ja kulu**

- Projekti kinnitaja saab lugemisõiguse tõrke, kui ta kinnitab kulukirjed rolliga **Projekti kinnitaja**.
- Projekti kinnitaja saab kirjutusõiguse tõrke **msdyn_projectapproval**, kui ta tühistab kinnitatud ajakirje rolliga **Projekti kinnitaja**.
- Kui valite käsu **Kopeeri nädal** ajakirjes telefonidele mõeldud Dynamics 365 - Project ressursside keskuse rakenduse moodulis, ilmneb järgmine tõrge: "...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE."
- **Uuesti proovimise** poliitika kinnitab automaatselt varem tagasilükatud kirjed.
- Alamruudustik **Kinnitamiskomplektid** kuvab mitterakendatavaid linditoiminguid.
- Ikoonid **Projekti ülesanne** ja **Ressursi roll** puuduvad olemist **Ajakirje**.
- Ressursimääramiste importimisel ei ole imporditud ajakirjetel käsitsi režiimi tööülesannete kaudu loodud määramistel õige kestus.
- **Kustuta** puudub lehelt **Ajakirjete täpsem otsing**.
- **Salvesta** puudub lehelt **Ajakirje teave**. See probleem takistab lehe sulgemisel muudatuste salvestamist.

**Projekti kavandamine**

- Ruudustikud **Ressursi määramine** ja **Ressursi vastavusseviimine** ei sorteeri rühmitatud atribuute tähestikulises järjekorras.
- Tööülesandeid ei saa luua, kui kuupäeva käitumist on kohandatud olekusse **Ainult kuupäev**.

**Ressursihaldus**

- Kui installitud on nii Dynamics 365 Field Service kui ka Project Service Automation, tekivad ülekatte probleemid, kui **Ressursinõude seostatud vaade** on seotud pealehega.
- Topeltklõpsamine nupul **Salvesta** dialoogikastis **Meeskonnaliikme kiirloomine** takistab ressursinõude loomist.

**Müük**

- Kui kustutate olekuga **Võidetud** hinnapakkumisega seotud tööülesande, antakse erand.
