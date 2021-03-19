---
title: Projekti ajasisestuse mobiilne tööruum
description: Selles teemas kirjeldatakse, kuidas kasutada Projecti ajakirjete mobiilset tööruumi. See tööruum võimaldab kasutajatel oma mobiilsideseadme kaudu sisestada ja salvestada aega projekti jaoks.
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7eae471cf42f02e64844a4682cc8ed02cbb14c34
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288869"
---
# <a name="project-time-entry-mobile-workspace"></a>Projekti ajasisestuse mobiilne tööruum

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas kasutada **Projecti ajakirjete** mobiilset tööruumi. See tööruum võimaldab kasutajatel oma mobiilsideseadme kaudu sisestada ja salvestada aega projekti jaoks.

See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Dynamics 365 Unified Ops. 

## <a name="overview"></a>Ülevaade
Igapäevase töö osana on projekti ressursid sageli kohapeal või reisivad. **Projekti ajakirje** mobiilne tööruum võimaldab kasutajatel sisestada enda poolt valitud mobiilsideseadmel oma arveldatav ja mitte-arveldatav aeg projekti kohta. Seega saavad projekti ressursid salvestada ajakandeid igal ajal ja kõikjal. Nad saavad vaadata ka juba salvestatud ajakirjeid. 

Täpsemalt saavad kasutajad teha mobiilses tööruumis **Projekti ajakirje** teha järgmisi ülesandeid.

-   Sisestada mis tahes valitud kuupäeva jaoks mõne kindla toimingu jaoks kulutatud tundide arvu.
-   Otsida projekti nime või kliendi alusel, et leida aja sisestamiseks projekt.
-   Määrata kulutatud aja kategooria ja tegevus.
-   Salvestada aeg projekti jaoks arveldatavaks või mitte-arveldatavaks.
-   Vajaduse korral sisestada kõik välised ja sisemised kommentaarid.

## <a name="prerequisites"></a>Eeltingimused
Eeltingimused erinevad sõltuvalt teie organisatsioonis juurutatud Microsoft Dynamics 365 versioonile.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Eeltingimused, kui kasutate rakendust Dynamics 365 Finance
Kui teie organisatsiooni jaoks on juurutatud Finance, peab süsteemiadministraator avaldama **Projecti aja sisestamise** mobiilse tööruumi. Juhiseid vaadake teemast [Mobiilse tööruumi avaldamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Eeltingimused kui kasutate versiooni 1611 koos Platformi värskendusega 3 või hilisemaga
Kui teie organisatsioonis on juurutatud versioon 1611 koos Platformi uuendusega 3 või hilisemaga, peab süsteemiadministraator lõpule viima järgmised eeltingimused. 

<table>
<thead>
<tr class="header">
<th>Eeltingimus</th>
<th>Roll</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>KB 4018050 rakendamine.</td>
<td>Süsteemihaldur</td>
<td>KB 4018050 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Projecti ajakirje</strong> KB 4018050 rakendamiseks peab teie süsteemiadministraator järgima järgmisi juhiseid.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Laadige metaandmete kiirparandus alla portaalist Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installige metaandmete kiirparandus</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Looge juurutatav pakett</a>, mis sisaldab mudeleid <strong>ApplicationSuite</strong> ja <strong>ProjectMobile</strong>, ja seejärel laadige LCS-i üles juurutatav pakett.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Rakendage juurutatav pakett</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Avaldage <strong>Projecti ajakirje</strong> mobiilne tööruum.</td>
<td>Süsteemihaldur</td>
<td>Vt <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilse tööruumi avaldamine</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiilirakenduse allalaadimine ja installimine

Mobiilirakenduse Finance and Operations allalaadimine ja installimine

-   [Androidi telefonidele](https://go.microsoft.com/fwlink/?linkid=850662)
-   [iPhone’idele](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logige mobiilirakendusse sisse
1.  Käivitage oma mobiilsideseadmes rakendus.
2.  Sisestage oma Dynamics 365 URL.
3.  Esmakordsel sisselogimisel küsitakse teilt kasutajanime ja parooli. Sisestage oma identimisteave.
4.  Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid. Pange tähele, et kui teie süsteemiadministraator avaldab uue tööruumi hiljem, tuleb teil mobiilsete tööruumide loendit värskendada.

[![Tõmbeliigutusega värskendamine](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Sisestage aeg, kasutades Projecti ajakirje mobiilset tööruumi
1.  Valige oma mobiilsideseadmes tööruum **Projekti aja sisestamise**.
2.  Valige **Aja sisestus**. Näidatud on selle jooksva nädala kalendri kuupäevad.
3.  Valige valitud kuupäeval suvand **Toimingud**&gt;**Uus kirje**.
4.  Sisestage salvestatavate tundide arv.
5.  Valige ajakirje jaoks projekt. Loendis on toodud projektid, mis on laaditud rakendusse võrguühenduseta kasutamiseks. Vaikimisi laaditakse 50 üksust, kuid arendaja saab seda numbrit muuta. Lisateavet vt: [Mobiilne platvorm](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Kui teie projekti loendis pole, valige **Otsi**. Otsige nime järgi või vahetage projekti nime või kliendi järgi otsingule.
7.  Valige kategooria. Loendis on toodud kategooriad, mis on laaditud rakendusse võrguühenduseta kasutamiseks. Vaikimisi laaditakse 50 üksust, kuid arendaja saab seda numbrit muuta. Lisateavet vt: [Mobiilne platvorm](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Kui teie kategooriat loendis pole, valige **Otsi**. Otsige kategooria järgi või vahetage kategooria nime järgi otsingule.
9.  Valige tegevus. Loendis on toodud tegevused, mis on laaditud rakendusse võrguühenduseta kasutamiseks. Vaikimisi laaditakse 50 üksust, kuid arendaja saab seda numbrit muuta. Lisateavet vt: [Mobiilne platvorm](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Kui teie tegevust loendis pole, valige **Otsi**. Otsige tegevuse numbri järgi või vahetage otsingule eesmärgi põhjal.

11. Valige rea atribuut.
12. Valikuline: sisestage kõik välised ja sisemised kommentaarid.
13. Valige nupp **Valmis**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]