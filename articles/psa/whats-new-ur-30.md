---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 30, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 30, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010421"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 30, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution.md).

Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 30 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgu number on V3.10.51.61 ja on üldiselt saadaval 2021. a aprilli enesevärskenduse kaudu.

## <a name="update-release-30"></a>Värskenduste väljalase 30

### <a name="bug-fixes"></a>Veaparandused

**Aeg ja kulu**

Lahendatud on järgmised probleemid.

- Lehel **Kiirloomine** ajakirje loomisel ja salvestamisel esineb tõrge, kui väli **Roll** on eemaldatud.
- Ajakirje filter rakendab filtri tehtemärgi valesti.
- Kopeeritud ajalehti ei kuvata automaatselt, kui valite ajakirje juhtelemendil suvandi **Kopeeri nädal**.

**Ressursihaldus**

Lahendatud on järgmised probleemid.

- Broneeringu pikendamisel on fikseeritud broneeringule määratud broneeringu olek vale. Broneeringu pikendamine arvestab broneeringu olekuga, mis on määratletud broneeringu häälestamise metaandmetes kui **Kinnitatud**.
- Kui kehtivat broneeringu olekut ei määrata, siis tõrketeadet ei lokaliseerita õigesti.

**Projektijuhtimine**

Lahendatud on järgmised probleemid.

- Projekte ei saa luua ühes valuutas ja see ei saa sisaldada seotud ülesandeid teises valuutas.

**Müük**

Lahendatud on järgmised probleemid.

- Hinnakirja kopeerimisel hindu ei värskendata.
- Võidetud hinnapakkumise sulgemine nurjub, kui kulu üksikasjadel on päritolu väärtus.
- Olemil **Projekti ülesanne** on suvand **Prognoositav kulu** nimetatud ümber olemiks **Plaanitud kulu (alus)**.
- Arvete loomisel ja kustutamisel luuakse nullviite erand.
