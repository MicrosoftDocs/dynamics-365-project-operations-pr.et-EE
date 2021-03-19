---
title: Kuluhalduse mobiilne tööruum
description: Selles teemas kirjeldatakse, kuidas kasutada kuluhalduse mobiilset tööruumi. See tööruum võimaldab kasutajatel jäädvustada kviitung ja see üles laadida, et nad saaksid selle hiljem kuluaruandele lisada. Lisaks saavad kasutajad kiiresti luua manustatud kviitungit kasutades kulurea ja luua ning hallata oma kuluaruandeid.
author: suvaidya
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2d257ced3dadb320c501bfd5f64dcd8f21c1a4d3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272023"
---
# <a name="expense-management-mobile-workspace"></a>Kuluhalduse mobiilne tööruum

Selles teemas kirjeldatakse, kuidas kasutada mobiilset tööruumi **Kuluhaldus**. See tööruum võimaldab kasutajatel jäädvustada kviitung ja see üles laadida, et nad saaksid selle hiljem kuluaruandele lisada. Lisaks saavad kasutajad kiiresti luua manustatud kviitungit kasutades kulurea ja luua ning hallata oma kuluaruandeid. Lisaks saavad kinnitajad kasutada mobiilset tööruumi **Kuluhaldus**, et vaadata neile määratud kuluaruandeid ning kas need kuluaruanded kinnitada või tagasi lükata.


See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Dynamics 365 Unified Ops.


## <a name="overview"></a>Ülevaade

Paljud organisatsioonid nõuavad, et töötaja poolt hüvitamiseks esitatavale reisimise või äriga seotud kuluaruandele lisataks kviitungi koopia. Mobiilne tööruum **Kuluhaldus** võimaldab kasutajatel oma valitud mobiiliseadmes kiiresti luua uusi kuluridasid, kasutades manustatud kviitungi fotot. Teise võimalusena saavad kasutajad jäädvustada kviitungi foto ja lisada selle kuluaruandele hiljem. Töötajad saavad lisaks luua ja hallata oma kuluaruandeid ning seejärel esitada need kinnitamiseks ja hüvitamiseks, kasutades oma mobiiliseadet.


Eelkõige võimaldab mobiilne tööruum **Kuluhaldus** kasutajatel täita järgmisi ülesandeid.

- Tehke kviitungist foto ja laadige see üles rakendusse Dynamics 365 Finance. Saate lisada selle foto kuluaruandele hiljem.
- Laadida jäädvustatud kviitungina üles faili. Saate lisada selle faili kuluaruandele hiljem.
- Luua manustatud kviitungit kasutades uue kulurea. Saate seejärel hiljem lisada reaüksuse kuluaruandele ja esitada selle kinnitamiseks ning hüvitamiseks.

Saate kasutada järgmisi funktsioone.

- Luua uue kuluaruande.
- Lisada kuluaruandele krediitkaarditehingud ja teised varem loodud kulud.
- Looge kuluaruande jaoks uusi kulusid.
- Lisada kuluaruandes olevale mis tahes kulule kviitungi kas tehes kviitungist fot või laadides jäädvustatud kviitungina üles faili.
- Olenevalt ettevõtte kulupoliitikast lisada kulule külaliste nimekiri.
- Olenevalt ettevõtte kulupoliitikast loendada kulud.
- Esitada kuluaruande kinnitamiseks ja hüvitamiseks.
- Kinnitada või lükata tagasi kuluaruandeid, millele olete määratud kinnitajaks.

## <a name="prerequisites"></a>Eeltingimused
Eeltingimused erinevad sõltuvalt teie organisatsioonis juurutatud versioonist.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Eeltingimused, kui kasutate rakendust Dynamics 365 Finance 
Kui teie organisatsiooni jaoks on juurutatud rakendus Finance, peab süsteemiadministraator avaldama mobiilse tööruumi **Kuluhaldus**. Juhiseid vaadake teemast [Mobiilsete tööruumide avaldamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Eeltingimused kui kasutate versiooni 1611 koos platvormi värskendusega 3 või hilisemaga
Kui teie organisatsioonis on juurutatud versioon 1611 koos platvormi uuendusega 3 või hilisemaga, peab süsteemiadministraator lõpule viima järgmised eeltingimused. 

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
<td>KB 4019015 rakendamine.</td>
<td>Süsteemihaldur</td>
<td>KB 4019015 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Kuluhaldus</strong>. KB 4019015 rakendamiseks peab teie süsteemiadministraator järgima järgmisi juhiseid.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Laadige metaandmete kiirparandus alla portaalist Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Installige metaandmete kiirparandus</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Looma juurutatava paketi</a>, mis sisaldab mudeleid <strong>ApplicationSuite</strong> ja <strong>ExpenseMobile</strong>, ja seejärel laadima LCS-i üles juurutatav pakett.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Rakendage juurutatav pakett</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Avaldama mobiilse tööruumi <strong>Kuluhaldus</strong>.</td>
<td>Süsteemihaldur</td>
<td>Vt <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilse tööruumi avaldamine</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Mobiilirakenduse Dynamics 365 for Operations allalaadimine ja installimine
Mobiilirakenduse Dynamics 365 Unified Ops allalaadimine ja installimine.

- [Androidi telefonidele](https://go.microsoft.com/fwlink/?linkid=850662)
- [iPhone’idele](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logige mobiilirakendusse sisse
1. Käivitage oma mobiilsideseadmes rakendus.
2. Sisestage oma Dynamics 365 URL.
4. Esmakordsel sisselogimisel küsitakse teilt kasutajanime ja parooli. Sisestage oma identimisteave.
5. Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid. Pange tähele, et kui teie süsteemiadministraator avaldab uue tööruumi hiljem, tuleb teil mobiilsete tööruumide loendit värskendada.


[![Tõmbeliigutusega värskendamine](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Kviitungi jäädvustamine mobiilse tööruumiga Kuluhaldus

1. Avage oma mobiiliseadmes tööruum **Kuluhaldus**.
2. Valige **Jäädvusta kviitung**.
3. Valige **Tee foto** või **Vali pilt**.
4. Järgige ühte härgmistest sammudest.

    - Kui valisite suvandi **Tee foto**, järgige järgmisi samme.

        1. Teid suunatakse oma mobiiliseadme kaamerasse, et saaksite teha kviitungist foto. Kui olete foto tegemise lõpetanud, valige foto aktsepteerimiseks **OK**.
        2. Valikuline: sisestage foto nimi ja sisestage soovitud märkmed.

    - Kui valisite suvandi **Vali pilt**, järgige järgmisi samme.

        1. Valige loendist pilt.
        2. Valikuline: sisestage pildi nimi ja sisestage soovitud märkmed.

5. Valige nupp **Valmis**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Kulude kiire sisestamine mobiilse tööruumiga Kuluhaldus
1. Avage oma mobiiliseadmes tööruum **Kuluhaldus**.
2. Valige **Kiire kulu sisestamine**.
3. Valige kulukategooria. Näete kulukategooriate loendit, mis on laaditud rakendusse võrguühenduseta kasutamiseks. Vaikimisi laaditakse 50 üksust, kuid arendaja saab seda numbrit muuta. Arendajad peaksid lisateavet vaatama teemast [Mobiilne platvorm](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Kui teie kategooriat loendis pole, valige suvand **Otsing**, et otsida võrgust. Otsige kulukategooriat või vahetage kulutüübi järgi otsimisse.
4. Sisestage kulu tehingu kuupäev.
5. Valikuline: sisestage kulu jaoks kaupleja.
6. Sisestage kulu summa.
7. Valige kulu valuuta. Näete valuutakoodide loendit, mis on laaditud rakendusse võrguühenduseta kasutamiseks. Vaikimisi laaditakse 400 valuutat, kuid arendaja saab seda numbrit muuta. Arendajad peaksid lisateavet vaatama teemast [Mobiilne platvorm](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Kui teie valuutat loendis pole, valige suvand **Otsing**, et otsida võrgust. Otsige valuuta järgi või vahetage nime järgi otsingule.
8. Valige **Tee foto** või **Vali pilt**.
9. Järgige ühte härgmistest sammudest.

    - Kui valisite suvandi **Tee foto**, suunatakse teid oma mobiiliseadme kaamerasse, et saaksite teha kviitungist foto. Kui olete foto tegemise lõpetanud, valige foto aktsepteerimiseks **OK**.
    - Kui valisite suvandi **Vali pilt**, valige loendist soovitud pilt.

10. Valige nupp **Valmis**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Kuluaruande kinnitamine kasutades mobiilset tööruumi Kuluhaldus (kui kasutate 2017. a juulu värskendust)
1. Avage oma mobiiliseadmes tööruum **Kuluhaldus**.
2. **Kulude kinnitused** kuvavad kuluaruannete arvu, mis on teile kinnitamiseks määratud. Seda arvu värskendatakse ligikaudu iga 30 minuti tagant. Valige **Kulude kinnitused**.

    Kuvatakse kuluaruannete loend, mis on teile kinnitamiseks määratud.
    
3. Valige kuluaruanne, et vaadata selle kulude üksikasju.
4. Valige kulu, et vaadata selle üksikasju. Kulu kohta kuvatav teave sisaldab kogu kviitungi, külaliste ja üksikasjaliku loetelu üksikasju.
5. Tagasi lehel **Kuluaruanne** valige kuluaruande kinnitamine või tagasi lükkamine.
6. Sisestage kinnitamistoimingu mis tahes kommentaarid.
7. Valige nupp **Valmis**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Uue kuluaruande loomine loomine ja selle kinnitamiseks esitamine kasutades mobiilset tööruumi Kuluhaldus (kui kasutate 2017. a juuli värskendust)
1. Avage oma mobiiliseadmes tööruum **Kuluhaldus**.
2. Valige **Kulu sisestamine**.
3. Valige **Uus aruanne** või valige loendist olemasolev kuluaruanne.
4. Uute kuluaruannete jaoks sisestage eesmärk ja mis tahes olemasolev lisateave. See teave erineb olenevalt viisist, kuidas kuluhaldus on teie ettevõttes konfigureeritud.
5. Valige nupp **Valmis**.
6. Olemasolevate kulude (nt krediitkaardi tehingute) kuluaruandele lisamiseks valige suvand **Manusta**.
7. Valige loendist üks või mitu kulu.
8. Valige nupp **Valmis**.
9. Aruandele uue kulu lisamiseks valige **Uus kulu**.
10. Valige kulukategooria. Näete kulukategooriate loendit, mis on laaditud rakendusse võrguühenduseta kasutamiseks. Vaikimisi laaditakse 50 üksust, kuid arendaja saab seda numbrit muuta. Arendajad peaksid lisateavet vaatama teemast [Mobiilne platvorm](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Kui teie kategooriat loendis pole, valige suvand **Otsing**, et otsida võrgust. Otsige kulukategooriat või vahetage kulutüübi järgi otsimisse.
11. Valikuline: sisestage kulu jaoks kaupleja.
12. Sisestage kulu tehingu kuupäev.
13. Sisestage kulu summa.
14. Valige kulu valuuta. Näete valuutakoodide loendit, mis on laaditud rakendusse võrguühenduseta kasutamiseks. Vaikimisi laaditakse 400 valuutat, kuid arendaja saab seda numbrit muuta. Arendajad peaksid lisateavet vaatama teemast [Mobiilne platvorm](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Kui teie valuutat loendis pole, valige suvand **Otsing**, et otsida võrgust. Otsige valuuta järgi või vahetage nime järgi otsingule.
15. Valige nupp **Valmis**.
16. Kulule täiendavate üksikasjade lisamiseks valige suvand **Lisa rohkem üksikasju**. Saadaolevad väljad olenevad teie ettevõttes konfigureeritud kuluhaldusest.
17. Kui ettevõtte poliitika nõuab kulu jaoks kviitungit, valige suvand **Kviitungid** ja järgige seejärel järgmisi samme.

    1. Valige **Jäädvusta kviitung** või **Manusta kviitung**.
    2. Järgige ühte härgmistest sammudest.

        - Kui valisite suvandi **Jäädvusta kviitung**, järgige järgmisi samme.

            1. Valige **Tee foto** või **Vali pilt**.
            2. Järgige ühte härgmistest sammudest.

                - Kui valisite suvandi **Tee foto**, järgige järgmisi samme.

                    1. Teid suunatakse oma mobiiliseadme kaamerasse, et saaksite teha kviitungist foto. Kui olete foto tegemise lõpetanud, valige foto aktsepteerimiseks **OK**.
                    2. Valikuline: sisestage foto nimi ja sisestage soovitud märkmed.

                - Kui valisite suvandi **Vali pilt**, järgige järgmisi samme.

                    1. Valige loendist pilt.
                    2. Valikuline: sisestage pildi nimi ja sisestage soovitud märkmed.

            3.  Valige nupp **Valmis**.

        - Kui valisite suvandi **Manusta kviitung**, järgige järgmisi samme.

            1.  Valige loendist üks või mitu pilti.
            2.  Valige nupp **Valmis**.

    3. Valige nupp **Tagasi**, et naasta kulude üksikasjadesse.

18. Kui ettevõtte poliitika nõuab kulu jaoks külalisi, valige suvand **Külalised** ja järgige seejärel järgmisi samme.

    1. Valige suvand **Külalised**, **Varasemad külalised** või **Kaastöötajad**.
    2. Järgige ühte härgmistest sammudest.

        - Kui valisite suvandi **Külalised**, järgige järgmisi samme.

            1. Sisestage külalise nimi.
            2. Valikuline: sisestage külalise organisatsioon ja/või riik.
            3. Valikuline: sisestage külalise ametinimetus.
            4. Valige nupp **Valmis**.

        - Kui valisite suvandi **Varasemad külalised**, järgige järgmisi samme.

            1. Valige lonedist üks või mitu varasemat külalist. Näete varasemate külaliste loendit, mille olete lisanud eelmistele kuluaruannetele, mille olete võrguühenduseta kasutamiseks oma rakendusse laadinud. Vaikimisi laaditakse 50 üksust, kuid arendaja saab seda numbrit muuta. Arendajad peaksid lisateavet vaatama teemast [Mobiilne platvorm](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Kui teie varasemat külalist loendis pole, valige suvand **Otsing**, et otsida võrgust. Otsige nime järgi või vahetage organisatsiooni, riigi või ametinimetuse järgi otsingule.
            2. Valige nupp **Valmis**.

        - Kui valisite suvandi **Kaastöötajd**, järgige järgmisi samme.

            1. Valige loendist üks või mitu kaastöötajat. Näete kaastöötajate loendit, mis on laaditud rakendusse võrguühenduseta kasutamiseks. Vaikimisi laaditakse 50 üksust, kuid arendaja saab seda numbrit muuta. Arendajad peaksid lisateavet vaatama teemast [Mobiilne platvorm](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Kui teie kaastöötajat loendis pole, valige suvand **Otsing**, et otsida võrgust. Otsige nime järgi või vahetage ettevõtte või ametinimetuse järgi otsingule.
            2. Valige nupp **Valmis**.

    3. Valige nupp **Tagasi**, et naasta kulude üksikasjadesse.

19. Kui ettevõtte poliitika nõuab, et kulu oleks üksikasjalikult loetletud, valige suvand **Täpsusta** ja järgige seejärel järgmisi samme.

    1. Valige üksikasjalikuks loeteluks esimene kuupäev.
    2. Valige **Lisa täpsustamine**.
    3. Valige kulu üksikasjalikuks loeteluks alamkategooria. Näete alamkategooriate loendit, mis on laaditud rakendusse võrguühenduseta kasutamiseks. Vaikimisi laaditakse 50 üksust, kuid arendaja saab seda numbrit muuta. Arendajad peaksid lisateavet vaatama teemast [Mobiilne platvorm](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Kui teie alamkategooriat loendis pole, valige suvand **Otsing**, et otsida võrgust. Otsige kulu alamkategooria nime järgi.
    4. Sisestage üksikasjalikuks loeteluks tehingu summa.
    5. Kui see on vajalik, muutke tehingu kuupäeva.
    6. Valige nupp **Valmis**.
    7. Korrake eelnevaid samme, kuni olete lõpetanud valitud kuupäeva jaoks kõikide üksikasjalike loetelude lisamise.
    8. Täiendavate päevade jaoks saate valida suvandi **Kopeer järgmisele päevale**, et kopeerida üksikasjaliku loendi järgmisele päevale. Teise võimalusena saate valida üksikasjalikuks loetlemiseks kuupäeva ja lisada seejärel üksikasjalikud loetelud sarnaselt esimesele kuupäevale.
    9. Pärast kulu üksikasjalikku loetlemist valige nupp **Tagasi**, et naasta kulu üksikasjadesse.

20. Valige nupp **Tagasi**, et naasta kulude lehele **Kuluaruanne**.
21. Korrake eelnevaid samme, kuni olete kõigi kulude lisamise lõpetanud.
22. Valige käsk **Esita**.
23. Sisestage kinnitaja jaoks mis tahes kommentaarid.
24. Valige nupp **Valmis**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]