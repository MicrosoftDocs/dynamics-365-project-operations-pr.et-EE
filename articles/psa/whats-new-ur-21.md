---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 21, V3
description: Selles artiklis loetletakse funktsioonid ja parandused, mis on saadaval jaotises Project Service Automation Update Release 21, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7d7c098a4572aa4f5730ffdbdab77b2897cdfeff
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918813"
---
# <a name="project-service-automation-update-release-21-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 21, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse funktsioonid ja parandused, mis on project Service Automation V3, Update Release 21 jaoks uued või muudetud. Selle versiooni järgu number on V 3.10.32.50 ja on üldiselt saadaval 2020. a juuni enesevärskenduse kaudu.

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
