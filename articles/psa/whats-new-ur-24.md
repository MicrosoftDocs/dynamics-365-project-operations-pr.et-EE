---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 24, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 24, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6c8348e65307f63a251f97bf1ea17578e7026da8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074908"
---
# <a name="project-service-automation-update-release-24-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 24, v3

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 24 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgunumber on V 3.10.42.43 ja see on oktoobris 2020 automaatvärskendusega kõigile saadaval.

## <a name="update-release-24"></a>Värskenduste väljalase 24

### <a name="bug-fixes"></a>Veaparandused

**Sales**

Lahendatud on järgmised probleemid.

- Toodete vaikehinnakirja määramisel esines probleem.
- Hinnapakkumise võitmise jõudlus on manustatud hinnakirja ja rolli hinnakirjete koopia tõttu aeglane.
- **Projektileping/müügikeskus** > **Tootereaüksuste / tellimuserea kogus** ümardatakse automaatselt lähima täisarvuni.
- Laiendage hinnakirja lugemisel süsteemi õigusteni.
- Kopeerige kliendi aadressiväljad **address1_freighttermscode** ja **address1_shippingmethodcode** hinnapakkumisele/tellimusele. 


**Aeg ja kulu**

Lahendatud on järgmised probleemid.

- **Ajakirje ruudustik** ei toeta ajafunktsiooni **Ainult kuupäev**.
- **Ajakirjet** ei värskendata automaatselt. Nõutav on käsitsi värskendamine.
- Ajakirjeid ei saa ülesandest importida, kui ressursi määramistes on paus (0 tundi).
- Ajakirje loomisel määrake algus samale väärtusele kui **msdyn_date**.
- Lubage uuesti ajakirje hulgiredigeerimine.

**Ressursihaldus**

Lahendatud on järgmised probleemid.

- Päevasisese broneeringu oleku värskendamise proovimine ilma vajaduseta annab nullviite erandi.
- Viga suvandi **Vastavusseviimise vaade** laadimisel.


**Projektijuhtimine**

Lahendatud on järgmised probleemid.

- Kui vahetate suvandis **Projekti ajakava** valikult **Käsitsi** valikule **Automaatne** , siis automaatset salvestamist ei viida lõpuni.
- Kulumäära ei tohiks suvandis **Projekti jälgimise ruudustik** arvutada hälbe suunas.
- Veergude **Hinnangute silt** vastuoluline käitumine laadimise ajal võrreldes tüübi **Ajafaas** muutumisega.
- Projekti tegelik kulu ei pruugi kajastada kogusummasid suvandist **Tegelikud summad**.
- **Hinnanguline lõpukuupäev** vahekaardil **Kokkuvõte** ei ühti suvandiga **WBS-i ajakava**.
- **Tegeliku tööaja värskendamine** ei tööta õigesti taandel õigesti.
- Juur- **äriüksusest** väljaspool olev projektijuht ei saa projekti luua.
- Tööülesande või kategooria muudatused suvandis **Kuluhinnangud** ei jää püsima.
- **Lepingu koopia** kopeerib arve ajakavad ja käitamise oleku.
- Nupp **Värskenda tegelikud näitajad** arvutab kokkuvõtte ülesanded valesti.
- Microsoft Projecti lisandmoodul: parandage nullviite tõrge, kui mõnel meeskonnaliikmel on tühi ressursiühik.
