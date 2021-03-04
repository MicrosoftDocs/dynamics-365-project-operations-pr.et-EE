---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 21, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 21, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: b1194c1cf1997b68030fe88360c6ebb756c715fd
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147018"
---
# <a name="project-service-automation-update-release-21-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 21, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 21 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgu number on V 3.10.32.50 ja on üldiselt saadaval 2020. a juuni enesevärskenduse kaudu.

## <a name="update-release-21"></a>Värskenduste väljalase 21

### <a name="bug-fixes"></a>Veaparandused

**Aeg ja kulu**

Lahendatud on järgmised probleemid.

- Armatuurlaudadel **ajakirje ruudustiku juhtelemendi** majutamisel ei kasuta ruudustik armatuurlaua ruudustiku ümbrise täislaiust.
- **Ajakirje** ruudustiku juhtelement ei kuva konkreetsete ajavööndite jaoks kirjeid.
- Hilisemad ajakirjed kui kl 21.00 ilmuvad valel päeval.
- Kasutajad ei saa kulusid esitada, kui kulukategoorial **Nõutav kuludokument** puudub väärtus.

**Ressursihaldus**

Lahendatud on järgmised probleemid.

- Passiivsed broneeringud kuvatakse vaates **Vastavusseviimine**.
- Üldisel ressursi täitmisel puudus valideerimine, et tagada kehtiva broneeringu oleku olemasolu.

**Projektijuhtimine**

Lahendatud on järgmised probleemid.

- **Projekti** vormi ruudustikud (**Ressursi määramine**, **Ülesanne**, vaade **Vastavusseviimine**, **Kuluprognoosid**) jäävad redigeeritavaks ka siis, kui projekt pole aktiivne.
- Dubleeritud kliente ei saa liita klientidega, kes on seotud kinnitatud projektilepingutega.
- Kui lisatakse klient, kellel puudub kehtiv kalender, süsteem ei tagasta kasutajasõbralikku tõrketeadet.
- Ülesande ruudustiku nupp **Lisa ülesanne** on lubatud, kui projekt on seotud **Microsoft Projecti lisandmooduliga**.
- Panus kasvab kontrollimatult juhul, kui kategooria ülesanne määratakse ressursile, millel on roll, millel pole omahinda määratud.

**Sales**

Tehtud on järgmised täiustused.

- **Arve sagedus** ja **Arveldamise algus** on teisaldatud vahekaardile **Arve ajakava**.

Lahendatud on järgmised probleemid.

- **Müügihind kokku** on null (0) suvandi **Kategooria** jaoks, olgugi suvandi **Roll** müügihind kokku ei ole null.
- Kliendid ei saa muuta välja **Arve olek** väärtuseks **Arveldamiseks valmis**, kui muu kohandatud protsess värskendab täiendavat välja.
- Nupp **Värskenda arve ridu** saab korduval valimisel luua mitu dubleeritud rida.
- Nupp **Värskenda hindasid** ei tööta vormi **Kiirvaade** andmeruudustikus **Rolli hinnad**.
- **Müügihinnakirja resolutsiooni** loogika käsitseb ajavööndeid valesti, mille tulemuseks on hinnakirjade vale valimine.
- Projekti suvand **Tegelik kulu kokku** võib pärast ühekordse sisestuse kinnitamist olla murdosa summa võrra vale.
- **Hinna lahenduse** loogika ei esita kasutajasõbralikke tõrketeateid, kui **toodud rolli hind** ei oma väärtuseid väljadel **Põhiühik** ja **Hind põhiühikutes**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]