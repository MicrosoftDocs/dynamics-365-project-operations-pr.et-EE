---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 22, V3
description: Selles artiklis loetletakse Project Service Automationi värskenduse väljalaske 22, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 733ee6e0d3583f21d0f58f9651920be3e3fd8cb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930635"
---
# <a name="project-service-automation-update-release-22-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 22, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse Project Service Automationi V3 värskenduse väljalaske 22 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgu number on V 3.10.33.48 ja on üldiselt saadaval 2020. a juuni enesevärskenduse kaudu.

## <a name="update-release-22"></a>Värskenduste väljalase 22

### <a name="bug-fixes"></a>Veaparandused



**Aeg ja kulu**

Lahendatud on järgmised probleemid.

- **Ajakirjeid** ei lisata pärast importimist automaatselt ajakirjete ajakavasse.
- **Ajakirje** ruudustiku kuupäeva valija ei tuvasta kasutaja piirkondlikke seadistusi.

**Ressursihaldus**

Lahendatud on järgmised probleemid.

- Käsitsi režiimis kontuuride **Ressursi määramine** muudatusi ei tuvastata **ressursi nõuete** loomisel.
- **Ressursi päringud** ei toeta kohandatud taotluse olekuid.

**Projektijuhtimine**

Lahendatud on järgmised probleemid.

- EstimateGridControl topeltklõpsamine ei sõelu Hollandi vormingu numbreid õigesti.
- Määratud tunde ei värskendata õigesti, kui määramisi muudetakse Microsoft Projecti töölaua klientrakenduse lisandmoodulit kasutades.
- Ruudustikud Projekti jälgimine ja Prognoosid kuvavad vale müügi valuutakoodi, kui lepingu valuuta erineb kliendi valuutast ja organisatsioon on konfigureeritud kuvama valuutatähiste asemel valuutakoodid.
- Meeskonnaliikme lõppkuupäev lisab ühe päeva, kui töö ajakava on 24 tundi päevas.
- Projekti ajakavas ülesandele tehingu kategooria lisamine ei käivita automaatset salvestamist.
- Projektimalli meeskonnaliikme lisamisel kuvatakse järgmine tõrge: „Ressursinõudeid ei saa seostada projektimallidega”. 
- Lindireegli skript „msdyn.Approval.CanApproveOrReject” kuvab aegumise tõrke.

**Sales**

Lahendatud on järgmised probleemid.

- Valideerimise tõrketeadet ei kuvata, kui vormil/olemis Uus hinnapakkumise projekti hinnakiri on otsingus Hinnakiri valitud suvand Omahinnakiri.
- Võidetuna hinnapakkumise sulgemine navigeeri loodud lepingu juurde, kui hinnapakkumisele manustatud BPF on viimases etapis.
- Suvandi **Arveldamata müük** tagasipööramine on seotud algse kuluga, kui ajakirje võetakse tagasi.
- Pärast nupu **Kinnita** valimist arve olek ei muutu olekule **Kinnitatud** enne, kui arve värskendatakse.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
