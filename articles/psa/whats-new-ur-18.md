---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 18, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 18, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: b35c2f8f67e1bb75493a8787f1c4d8c2baf74d51
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280753"
---
# <a name="project-service-automation-update-release-18-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 18, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 18 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgu number on V3.10.8.12 ja on üldiselt saadaval 2020. a aprilli enesevärskenduse kaudu.

## <a name="update-release-18"></a>Värskenduste väljalase 18

### <a name="bug-fixes"></a>Veaparandused

**Aeg ja kulu**

- Parandatud. Suvandid **Võta tagasi**, **Taotle** ja **Tühista kinnitus** liigub läbi erandite koos ebaselgete tõrketeadetega.
- Parandatud. Kui kulu suvand **Tühista kinnitus** nurjub, ilmneb vastav erandi tõrge.
- Parandatud. Ajakirje ruudustik käsitseb pärast oktoobris suveaja vahetust Austraalias mittetööpäevi valesti.
- Parandatud. Vale vaikeloogika takistab kulude esitamist.
- Parandatud. Kui aja sisestamise kinnitus nurjub, jääb kinnitus olekusse **Ootel**.
- Parandatud. SQL-i tõrked hulgikinnitustes (tupik/aegumine).
- Parandatud. Olulised kasutuskeskkonna jõudlusprobleemid, mille põhjustavad värskendusi tegevad meeskonnaliikmed ajakirjete kinnitamisel.

**Projektijuhtimine**

- Parandatud. Ajavööndi teatis on viidud vaatest **Vastavusse viimine** põhivormile **Projekt**.
- Parandatud. Kalendrimall ei lähtesta uue projektivormi avamisel õigesti vaikesätetele.
- Parandatud. Chromiumi-põhistes brauserites ei saa kasutajad hõlpsalt valida kustutamiseks eelkäija ülesandeid.
- Parandatud. Suvandi **Projekt tühjast mallist** loomine või kopeerimine toob seoseta ülesanded.
- Parandatud. Konkreetsetes servajuhtumites põhjustab uue ülesande loomine ülesande ruudustikust duplikaatkirjete loomist.
- Parandatud. Käsitsi režiimis ei saa kasutajad uuendada ülesande alguskuupäevasi hilisemaks kui praegune salvestatud kuupäev.

**Ressursihaldus**

- Parandatud. Vaate **Vastavusse viimine** vahekokkuvõtte rida arvutab pärast broneeringute pikendamist broneeringute hälbe valesti.
- Parandatud. Vaade **Vastavusse viimine** kuvab ressursi ülesanded valesti, kui broneeritaval ressursil on kalender, mis ei ühti projekti kalendriga.

**Sales**

- Parandatud. Kui ajakirjed kinnitatakse uuesti (**Kinnita > Tühista >** uuesti kinnitamine), luuakse mittearvestatava tegeliku duplikaat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]