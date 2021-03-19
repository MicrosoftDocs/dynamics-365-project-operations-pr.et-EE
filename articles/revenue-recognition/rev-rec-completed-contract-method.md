---
title: Tulukalkulatsioonide haldamine
description: See teema sisaldab teavet selle kohta, kuidas töötada projektide tulukalkulatsioonidega.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b63346f56db8b906e5aa45940465bdb18e3df480
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278998"
---
# <a name="manage-revenue-estimates"></a>Tulukalkulatsioonide haldamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Tulukalkulatsioone on võimalik luua, arvutada, kirjendada, pöörata ümber või eemaldada. Seda saate teha käsitsi või perioodilise protsessi kasutades. See teema sisaldab teavet selle kohta, kuidas töötada projektide tulukalkulatsioonidega.

### <a name="manage-revenue-estimates-manually"></a>Tulukalkulatsioonide käsitsi haldamine

Valige fikseeritud hinnaga tulukalkulatsiooniga projektis või lehel **Prognoosi päring** (**Projektihaldus ja raamatupidamine** > **Aruanded ja päringud** > **Hinnangute päringud ja aruanded**) suvand **Hinnangud**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Tulukalkulatsioonide haldamine perioodilisi protsesse kasutades

Minge jaotisse **Projektihaldus ja raamatupidamine** > **Perioodiline** > **Hinnangud** ja valige vastav protsess.

## <a name="create-a-revenue-estimate"></a>Tulukalkulatsiooni loomine

Tulukalkulatsiooni loomiseks toimige järgmiselt. 

1. Avage jaotis **Projektihaldus ja raamatupidamine** > **Perioodiline** > **Hinnangud**.
2. Tehke valik **Uus**. Valige lehel **Hinnangu loomine** järgmised parameetrid.

   - **Perioodi kood**: see kood määratleb, kui sageli hinnangud sisestatakse.
   - **Hinnangu kuupäev**: hinnangu töötlemise kuupäev.
   - **Pidev**: valige see märkeruut, et luua hinnangud ainult siis, kui hinnang sisestati eelmisel perioodil, või kui hinnag on esimene loodav hinnang. Kui see pole valitud, luuakse hinnangud ka juhul, kui eelmise perioodi hinnanguid ei kirjendatud.
   - **Kulu meetodi lõpetamiseks**: määratlege, kuidas allesjäänud projekti tööd hinnata. Lisateavet leiate jaotisest [Kulu meetodi lõpetamiseks](cost-complete-methods.md).
   - **Lõpetamise meetod**: valige lõpetamise meetod järgmiste valikute seast.
     - **Automaatne**: lõpuleviimise protsent arvutatakse automaatselt ja põhineb arvutusse kaasatud kuluridadel. Kulumall määratleb kaasatud kuluread.
     - **Käsitsi**: lõpuleviimise protsent võrdub viimase hinnangu lõpuleviimise protsendiga. Pärast hinnangu loomist saate muuta **käsitsi arvutamist** lehel **Hinnangud**.
     - **Kulumallist**: automaatsete ja käsitsi kasutatavate meetodite kombinatsioon. See suvand määratakse automaatselt või käsitsi, olenevalt kulumalli vaikeväärtusest.
   - **Prognoosi mudel**: valige hinnangu jaoks prognoosi mudel.
   - **Hinnangute loendi printimine**: saate luua ja kuvada hinnangute loendi. Loend sisaldab praeguse funktsiooni olekut. Saate printida aruande hinnangu kohta mis tahes hoiatused. Järgmised tingimused põhjustavad hinnangu loendis hoiatuste ilmumist.
     - Lõpuleviimise protsent suurem kui 100%.
     - Lõpuleviimise protsent väiksem kui 0%.
     - Negatiivne summa veerus **Lõpule viia**.
     - Hinnang ilma vastava lepingusummata.
     - Hinnang ilma lisatud kulukalkulatsioonita.
   - **Teabelogi kuvamine**: valige see suvand, kui soovite saada sõnumi, mis sisaldab teavet projekti käitamisel töödeldud kalkuleeritud projektide kohta.


## <a name="post-wip-or-accruals"></a>WIP kirjendamine või viitvõlad

Pärast hinnangute kalkuleerimist neid hallatakse, need vähenevad või suurenevad. Saate seejärel kirjendada WIP, kui töötate hindamise põhimõttega **Lõpetatud leping** või kirjendada viitvõlad, kui töötate hindamise põhimõttega **Lõpule viimise protsent**.
  
Hinnangu perioodi olek muutuv olekult **Loodud** olekule **Kirjendatud**.

## <a name="reverse-wip-or-accruals"></a>Ümberpööratud WIP või viitvõlad

Kasutage ümberpööramise valikut, et krediteerida juba kirjendatud WIP-d või viitvõlgu, ja looge seejärel perioodi jaoks hinnangud.

> [!NOTE]
> Perioodi ümberpööramiseks, mis on teiste perioodide vahel, pöörake vajalikud hinnangute perioodid ümber ja kirjendage need siis uuesti. Kuna kõik järgnevad perioodid sõltuvad eelmise perioodi hinnangutest, ärge jätke ühtegi ajavahemikku vahele.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Projekti hinnangu likvideerimine ja projekti lõpetamine

Hinnangu protsessi viimane samm on kõrvaldada hinnanguline projekt ja lõpetada fikseeritud hinnaga projekt, kui lõpuleviimise protsent jõuab 100 protsendini.

Likvideerimise käitamisel toimub järgnev.

- Lõpetatud lepinguga fikseeritud hinnaga projekti puhul WIP väärtused saldo kontodelt kaovad ning kirjendatakse tulu- ja kulukontodele.
- Lõpuleviimise protsendiga fikseeritud hinnaga projekti puhul eemaldatakse viitvõlad tulu- ja kulukontodelt.

Hinnang muutub olekusse **Likvideeritud**.

> [!NOTE]
> Erijuhtudel võib protsent ulatuda üle 100 protsendi. Sellisel juhul vähendage lõpuleviimise protsenti, kasutades selleks **kulu lõpetamiseks nulli määramise meetodit**, et jõuda 100 protsendini.

## <a name="reverse-elimination"></a>Ümberpööratud likvideerimine

1. Avage **Projektijuhtimine ja raamatupidamine** > **Perioodiline** > **Hinnangud** > **Ümberpööratud likvideerimine**. 
2. Toimingupaani vahekaardi **Toiming** rühmas **Haldus** valige suvand **Hinnang**. 
3. Valige suvand **Ümberpööratud likvideerimine**.

Sellel lehel saate pöörata ümber kõik likvideerimises koos konkreetse hinnangu kuupäevaga ja koos hinnangu olekuga **Likvideeritud**. Pärast vastavate väljade valimist tehingu olek muutub.

See muudab automaatselt projekti olekuks **Pooleli**, kui projekti etapiks on määratud lõpetatud. Projekti ajavahemiku hinnangu olek muutub tagasi väärtusele **Kirjendatud**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]