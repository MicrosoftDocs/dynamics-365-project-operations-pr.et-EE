---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 32, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 32, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129661"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 32, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 32 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgu number on V3.10.53.108 ja see on üldiselt saadaval isevärskenduse kaudu 2021. aasta juunis.

## <a name="update-release-32"></a>Värskenduste väljalase 32

### <a name="bug-fixes"></a>Veaparandused

#### <a name="general"></a>Üldist

- Kui oluline värskendus nurjub, tuleks blokeerida ainult rakenduse peamised sisestuspunktid, et tagada ühiskasutuses olemite juurdepääs.

#### <a name="time-and-expense"></a>Aeg ja kulu

Lahendatud on järgmised probleemid.

- **TimeEntriesImportFromResourceAssignment** ei säilita ressursi määramise kontuuri sektori algus- ja lõpuaega.
- Kui valite ruudustikus **Ajakirje** suvandi **Avatud kirje**, võib teiste vormide valimine olla teile takistatud.
- Kuigi impordite määramised ajakirjetele, võib kliendikoodi päring luua pika URL-i, mis põhjustab päringu nurjumist.
- Ruudustikus **Ajakirje** ei jää fookus pärast väärtuse lahtrist kustutamist ruudustikule.
- Nupp **Hülga** on kaasaegse kinnitamine vaatest **Kinnitamise töötlemine** eemaldatud.
- Ajakirje hulgikinnituse stabiilsust ja jõudlust mõjutavad blokeeringud ja olemiga **Ajakirje** seotud kohanduste sobiva käsitsemise nurjumine.

#### <a name="project-planning"></a>Projekti kavandamine

- Null-viite erand luuakse juhul, kui värskendate projekti, mille väljal **Lepinguüksus** on tühi väärtus.
- **Värskenda projekti kogusummasid** arvutab projekti allesjäänud kulud ja ülejäänud müügid valesti.
- Ülearused hinnaarvutused mõjutavad jõudlust, mis on seotud ressursi määramise kontuuride värskendustega.

#### <a name="resource-management"></a>Ressursihaldus

Järgmised probleemid on parandatud.

- Kui broneeritava ressursi kalendrivõimsus on suurem kui 1, tuvastab Project Service Automation võimsuse valesti kui 0 (null). Seega leiab ajakavavaates aset lõputu tsükkel.

#### <a name="sales"></a>Müük

Lahendatud on järgmised probleemid.

- Kohandatud tehingutüübiga töölehe rea loomisel luuakse järgmine nullviite erand: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Rolle ja kategooriaid, mis on inaktiveeritud enne hinnapäringu kopeerimist, ei tohiks vastkopeeritud hinnapakkumise laaditavatesse rollidesse ega kategooriatesse lisada.
- Dokumendi kuupäeva ja raamatupidamiskuupäeva ei joondatud alguskuupäevaga, mis on toodud otse mustandarvel loodud arve rea üksikasjades.
- Nullviite erandid luuakse stsenaariumides, mis on seotud rollide ja kategooriate inaktiveerimisega enne hinnapakkumise kopeerimist.
- Toiming **Värskenda hinnad** lehel **Projektid** ei värskenda kuluprognoose ega materjalide hinnanguid.
