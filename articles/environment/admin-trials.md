---
title: Project Operationsi prooviversioonidele registreerumine
description: Selles teemas kirjeldatakse, kuidas juurutada rakenduse Dynamics 365 Project Operations prooviversiooni.
author: ruhercul
ms.date: 08/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e9c0d81591061f0ff01200dd5fd634a4a9ff31e4
ms.sourcegitcommit: 0e5de344f2040075ba431918a4499a80510458d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/25/2021
ms.locfileid: "7418452"
---
# <a name="sign-up-for-project-operations-trials"></a>Project Operationsi prooviversioonidele registreerumine 

_**Kehtib järgmiste puhul:** Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks, lihtjuurutus – tehing näidisarveldusele, Project Operations ressursi-/tootmispõhiste stsenaariumite jaoks_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse, kuidas tellida partneri pakkumise eelvaadet ja juurutada Dynamics 365 Project Operations keskkonda.

Uue Project Operationsi prooviversiooniga saate automaatselt juurutada ükskõik millise kolmest toetatud juurutusstsenaariumist, täites küsimustiku, mis soovitab parimat juurutusviisi. Selles teemas antakse teavet selle kohta, kuidas teha järgmisi asju.

- Lunastada oma prooviversiooni pakkumine.
- Käivitada ettevalmistus.
- Konfigureerida topeltkirjutamine.
- Saada Project Operationsi kohta rohkem teada. 

Järgmises tabelis on esitatud uue prooviversiooni pakkumise üksikasjad.

| **Pakutav üksus**               | **Üksikasjad**                                  |
|------------------------------|----------------------------------------------|
| Pakkumise tüüp                   | See pakkumise tüüp on Administraatori müügivihje, seega on lunastamiseks vaja rentniku administraatorit. |
| Pakkumise kasutamine                    | Üks kord rentniku kohta                          |
| Pakkumise kestus               | 30 kalendripäeva                             |
| Lunastamisi rentniku kohta       | 1                                            |
| Kasutajate arv              | 25                                           |
| Laiendus                    | 1 laiendus, 30 kalendrit päeva               |
| Proovikeskkondade arv | 3                                            |


## <a name="admin-trial-details"></a>Administraatori prooviversiooni üksikasjad
Järgmises tabelis on ära toodud prooviversiooni üksikasjad ja juhised, kuidas neid iga juurutustüübi puhul rakendada.

| **Üksus**                      | **Lite**                                     | **Mittelaopõhised materjalid** | **Laopõhised materjalid** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Esitatud seadistuse andmed           | Ja                                          | Ja                       | Jah (USSI)            |
| Tehingupõhised andmed            | No                                           | No                        | No                    |
| Ettevalmistamise aeg minutites  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Eeltingimused
Järgmised eeltingimused on rakenduse Dynamics 365 Project Operations prooviversiooni juurutamiseks nõutavad.

- Rakenduse [Dynamics 365 Project Operations - eelversiooni prooviversioon](https://www.aka.ms/try-po) kasutajaks registreerimine.
- Kasutajal, kes eelvaate juurutab, peab olema Azure'i rentniku globaalse administraatori õigused.

> [!IMPORTANT]
> Seda toimingut peab tegema ainult üks inimene organisatsioonis, rentniku administraator. Kui te pole selle väljalaske tellija, oodake, kuni teie organisatsioon on registreeritud ja teile on saadetud kasutaja mandaat.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - eelversiooni prooviversioon 

Enne alustamist logige brauserisse kasutaja töökontoga sisse selles rentnikus, kuhu Project Operationsi prooviversiooni soovite.

1. Lunastage esimese pakkumise kood **Dynamics 365 Project Operations - eelversiooni prooviversioon**, kleepides selle brauseri URL-i.

    ![Lunasta pakkumine](./media/16RedeemFirstOfferNew.png)

2. Kinnitage oma tellimus.

    ![Tellimuse kinnitamine](./media/17ConfirmOrderNew.png)

  Näete kinnitust, et pakkumise lunastamine õnnestus.

   ![Kinnitamine](./media/18OrderConfirmationNew.png)

  Teid suunatakse [Power Platformi halduskeskusesse](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Küsimustik ja ettevalmistamine

1.  Avage [Power Platformi halduskeskus](https://admin.powerplatform.com/projectoperationstrial) ja täitke küsimustik.  
2.  Vaadake soovitatav juurutamistüüp üle ja valige ettevalmistuste käivitamiseks valikut **Alusta seadistust**.
3.  Vaadake üle tingimused ja valige suvand **Käivita**.

   Pärast ettevalmistamise käivitumist suunatakse teid Power Platformi halduskeskuse keskkondade loendisse. Ettevalmistuse ajal on teie keskkonna olekuks **Eksemplari ettevalmistamine**.
 
  Pärast ettevalmistamise lõpuleviimist on teie keskkonna olekuks **Valmis**.
 
4.  Pärast ettevalmistamise lõpuleviimist valige vastav Microsoft Dataverse'i URL ja rakendustekomplekti Finance and Operations URL-id juurutuse valideerimiseks.

## <a name="demo-data-installation"></a>Näidisandmete installimine

Järgmiste linkide abil saate juurdepääsu nii mittelaopõhiste materjalide kui ka lihtjuurutamisega stsenaariumide demo andmepakettidele. 
- [Mittelaopõhiste materjalide demoandmed](resource-apply-pro-setup-config-data.md)
- [Lihtjuurutuse demoandmed](lite-apply-demo-setup-config-data.md)

## <a name="configuring-dual-write"></a>Topeltkirjutuse konfigureerimine
Konfigureerige oma topeltkirjutuse vastendused ainult mittelaopõhiste materjalide juurutamistele. Lisateavet leiate teemast [Rakenduse Project Operations topeltkirjutamise vastenduse versioonid](resource-dual-write-maps.md).

## <a name="assign-licenses"></a>Litsentside määramine

Järgmiste toimingute lõpuleviimiseks on teil vaja oma organisatsiooni Microsoft 365 portaali administraatori juurdepääsu.

1. Oma kasutajatele litsentside määramiseks avage [Microsoft 365 halduskeskus](https://portal.office.com/).

   ![Halduskeskuse avaleht](./media/14AdminPortal.png)

2. Valige lehel **Aktiivsed kasutajad** need kasutajad, kellele soovite litsentsi määrata.

   ![Litsentside määramine](./media/15AssignLicenses.png)

3. Kontrollige, et **Dynamics 365 Project Operations eelversiooni** litsents oleks valitud ja seejärel valige **Salvesta muudatused**.

## <a name="additional-resources"></a>Lisaressursid

Järgmistest ressurssidest on Project Operationsi teekonna alustamisel palju abi.

- [Videosari - Project Operationsi ülevaade, süvenemine funktsioonidesse ja tegevuskava](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Juurutamise tüübi määratlemine](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Mis siis, kui rakendustekomplekti Finance and Operations keskkonna jaoks läheb vaja AML-i või ELM-i?

- Partnerid, kes vajavad täieliku keskkonna elutsükli haldamise võimalusi, vt uue partneri pakkumise ülevaatamiseks jaotist [Partneri liivakastilitsentsi taotlus](https://experience.dynamics.com/requestlicense). 
- Partnerid, kes soovivad saada rohkem teavet sisemiste kasutusõiguste kohta, vt jaotist [Sisemiste kasutusõiguste pilve- ja tarkvaraeelised (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Kas ma saan oma prooviversiooni pikendada rohkemaks kui 30 päeva?
Prooviversiooni pikendamiseks toimige järgmiselt.

1. Avage **Microsoft 365 halduskeskuses** jaotis **Arveldamine** > **Teie tooted**.
2. Valige **Dynamics 365 Project Operations (CE) - eelversiooni prooviversioon**.
3. Tehke jaotises **Aegumiskuupäev** valik **Pikenda kuupäeva**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Kas ma saan lihtjuurutuselt üle minna ressursi-/mittelaopõhise stsenaariumi juurutusele?
Praegu ei toetata keskkonna üleviimist lihtjuurutuselt mittelaopõhisele juurutusele.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Kas ma saan oma Finance'i keskkondadele juurdepääsu teenusele Lifecycle Services (LCS)?  
Ei. Nende prooviversioonide puhul käsitletakse juurutamist läbi Power Platformi halduskeskuse. Juurdepääs Finance'i keskkonnale on piiratud.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Kas saan installida oma prooviversiooni olemasolevale keskkonnale?
Kui teil on olemasolev keskkond, lubatakse teil installida lihtjuurutus olemasoleva müügi Dataverse'i keskkonnale Power Platformi halduskeskusest.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
