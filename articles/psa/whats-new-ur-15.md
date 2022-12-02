---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 15, V3
description: See artikkel annab teavet selle kohta, mida on uut rakenduse Project Service Automation värskenduse väljaandes 15, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: b87cae2cd8913457c2931d1661a57509d1398d29
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915639"
---
# <a name="project-service-automation-update-release-15-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 15, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast rakenduse Dynamics 365 Project Service Automation (PSA) värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskust ja avage värskenduse installimiseks lahenduste leht. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse PSA V3 värskenduse väljalaske 15 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgunumber on V3.10.5.28 ja see on jaanuaris 2020 automaatvärskendusega kõigile saadaval.

## <a name="update-release-15"></a>Värskenduste väljalase 15 

### <a name="enhancements"></a>Täiustused

- Projektijuhtimine

### <a name="bug-fixes"></a>Veaparandused

- Aeg ja kulu

  - Parandatud: lisada laadimise tõrke käsitlemine vastavusseviimise vaatesse.
  - Parandatud: projekti ressursside keskus: nimetada ebaselguse vähendamiseks ümber **Summa**.
  - Parandatud: reguleerida vaadet **Ajakirje kopeerimise veerud**, et see sisaldaks tüüpi.
  - Parandatud: aja kirje kestuse redigeerimine ruudustiku vaates põhjustab kümnendnumbreid kasutades mõne arvu korral tundmatu vea.

- Projektijuhtimine

  - Parandatud: **Kasuta jälgimise aknas** suvandi rippmenüü laieneb nüüd vastavalt valikute laiusele.
  - Parandatud: projektide haldamisel +13 ajavööndis võivad ülesannete arvutused kuvada ebatäpseid tulemusi.
  - Parandatud: **Meeskonnaliikme lõpuaeg** 24-tunnise kalendri kasutamisel on parandatud.
  - Parandatud: **BPF** uuesti aktiveeritud **msdyn_project** põhivormis.
  - Parandatud: määramiste arvestamine ei ignoreeri enam ühte päeva.
  - Parandatud: projekti vormile on lisatud uus teavituste bänner, kui kasutaja ja projekti ajavöönd erineb.

- Sales

  - Parandatud: kulude prognoosi kategooria otsingut saab kasutada duplikaatide filtreerimiseks.
  - Parandatud: kood **PluginDomain. ExecuteInTryCatchBlock(..)**-is ei peida enam erandi päritolu.
  - Parandatud: ei saa enam veateadet **Projekti otsingus** vormil **Hinnapakkumise rida**, kui projekte on rohkem kui 1000.
  - Parandatud: **Prognooside** ruudustik tööprognooside ja kuluprognooside kohta näitab nüüd õiget valuuta sümbolit.
  - Parandatud: kui organisatsioon värskendab PSA-d värskenduse väljaandega 14 või värskenduse väljaandega 15, ei ole vahekaart **Kavandamine** enam vormil **Projekt** tühi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
