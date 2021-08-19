---
title: Kuidas määrata veebirakenduses ülesandele broneeritavat ressurssi
description: Ülevaade võimalustest, kuidas saate broneeritud ressursse määrata.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 25cf017c53d7db23e467b3b610e2990e56e95cb56bdf9820e427dfeeeb979637
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987701"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Kuidas määrata veebirakenduses (Project Service v2.x) ülesandele reserveeritavat ressurssi?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Rakenduses Project Service on kaks võimalust ülesandele ressursi määramiseks. Saate ressursi reserveerida meeskonnaliikmena ja seejärel selle ülesandele määrata. Või saate ülesannetele rolli määramisega luua üldise meeskonnaliikme, luua meeskonna ja seejärel täita toetavad nõuded nimelise ressursiga.

Pange tähele, et kui soovite määrata reserveeritavat ressurssi ülesandele, peab reserveeritava ressursi meeskonnaliikmel olema piisavalt saadaval reserveeringuid. Reserveeringu olek peab olema kinnitamise tüübiga Fikseeritult reserveerimine ja olekuga Kinnitatud. Kui ressursi jaoks pole piisavalt reserveeringuid, siis eemaldab rakendus Project Service ülesande ja kuvab järgmise tõrketeate.

*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project* (Ei saanud ressurssi ülesandele määrata – järgmistele ressurssidele pole projekti suhtes piisavalt tunde reserveeritud)

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Ressursi reserveerimine meeskonnaliikmena ja seejärel ressursi määramine ülesandele

Selle meetodiga saate lisada ressursi projekti meeskonnale ja seejärel määrata projekti ajakavas ülesanded ressursile. Seda saate teha järgmiselt.
1.  Lisage meeskonnaliikmete ruudustikus uus meeskonnaliige, klõpsates nuppu **Uus**.
2.  Valige meeskonnaliikme kiirloomise ekraanil reserveeritava ressursi nimi ja määrake roll.
3.  Valige kuupäevade väärtused **Alates** ja **Kuni**.

    > [!div class="mx-imgBorder"] 
    > ![Kuvatõmmis meeskonnaliikme lisamisest.](media/FAQ-Resources-to-Tasks2-1.png "Kuvatõmmis meeskonnaliikme lisamisest")
 
4.  Valige ressursi reserveerimiseks üks järgmistest eraldamismeetoditest.
    - **Täisvõimsus** reserveerib määratud ajavahemikuks ressursi täieliku võimsuse.
    - **Protsendimaht** reserveerib määratud ajavahemikuks teatud protsendi ressursi võimsusest.
    - **Jaga ühtlaselt tundide järgi** reserveerib ressursi määratud arvu tundideks, jagades aega määratud ajavahemikus ühtlaselt igale päevale.
    - **Jaga eesmine koormus tundide järgi** reserveerib ressursi määratud arvu tundideks, jagades aega määratud ajavahemikus nii, et suurem koormus jääks algusesse.

    Ärge valige suvandit **Pole**, kuna see lisab ressursi meeskonnale, kuid ei loo reserveeringuid, mis hõivaks ressursi võimsuse.
5.  Valige käsk **Salvesta**.

    Pange tähele, et reserveeringu tunde peab olema piisavalt, et hõlmata ressursile määratavate ülesannete panusetunde ja ajavahemikke. Kui need pole kooskõlas, ei saa te ressurssi ülesandele määrata.

6.  Klõpsake ülesande tööjaotuse struktuuris (WBS) ressursilahtri ripploendit. Seejärel tehke järgmist. 

    1. Valige suvand **Lisa**.
    2. Valige jaotise **Ressursid** alt ripploend ja valige meeskonnaliige, kelle enne lisasite.
    3. Valige **OK**. Meeskonnaliige on nüüd ülesandele määratud.

    > [!div class="mx-imgBorder"] 
    > ![Kuvatõmmis WBS-iga ressursside lisamisest.](media/FAQ-Resources-to-Tasks2-2.png "Kuvatõmmis WBS-iga ressursside lisamisest")
 
Näete meeskonnaliikmete ruudustikus jaotise Määratud tunnid all ressursi määratud tundide koguaega. See on väiksem kui ressursile reserveeritud tunnid või sellega võrdne. 

> [!div class="mx-imgBorder"] 
> ![Kuvatõmmis ressursile määratud tundidest.](media/FAQ-Resources-to-Tasks2-3.png "Kuvatõmmis ressursile määratud tundidest")
 
Kui ülesanne, mida püüate ressursile reserveerida, algab pärast ressursi reserveeringute lõppkuupäeva, siis ei kuvata ressurssi ripploendis.

Pange tähele, et saate määrata ressurssi enamatele tundidele kui tema reserveeritud tunnid, kui sellel ressursil on üle jäänud määramata võimsust. Sellisel juhul määratakse ressurssi kuni tema reserveeringuteni vaid osaliselt. Näete neid üle jäänud määramata ülesannete tunde, kui lisate tööjaotuse struktuurile veeru Mehitamata tunnid.

Kui ressursid määratakse oma reserveeritud tundidele (nende reserveeritud tunnid võrduvad nende määratud tundidega), siis näete järgmist tõrketeadet, kui üritate neile rohkem ülesandeid määrata.

*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.* (Ei saanud ressurssi ülesandele määrata – järgmistele ressurssidele pole projekti suhtes piisavalt tunde reserveeritud.)

Peale selle lisatakse projektijuhi vaikerolliga meeskonnaliige, kes lisatakse meeskonnale projekti loomisel, ilma ühegi reserveeringuta ja talle ei saa määrata ühtegi ülesannet. Teda ei kuvata ülesannete ressursside ripploendites.

Kui soovite seda ressurssi määrata, siis peate ta meeskonnast eemaldama ja seejärel uuesti lisama ükskõik millise eraldamismeetodiga peale Pole. Projektijuht lisatakse projekti loomisel meeskonda, et tagada, et projektil oleks vaikimisi vähemalt üks projekti kinnitaja.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Üldise meeskonnaliikme loomine ülesannete rolli määramistega

See meetod tagab, et ressurssidel oleks ülesannete jaoks piisavalt reserveeringuid. Esmalt loote kohatäite või üldise ressursi, mis kirjeldab nimelise ressursi tunnuseid, keda soovite ülesannetele tööle määrata. Selleks loote pärast ülesannetele rollide määramist meeskonna. Seda saate teha järgmiselt.

1. Valige tööjaotuse struktuuris ülesanne.
2. Valige ressursilahtris ripploendi ikoon **Määratud roll**.
3. Valige ripploend **Roll** ja seejärel roll üldisele ressursile.
4. Valige **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Kuvatõmmis WBSi abil ressursi lisamisest.](media/FAQ-Resources-to-Tasks2-4.png "Kuvatõmmis WBSi abil ressursi lisamisest")
 
Kui olete lõpetanud WBS-is ülesannetele rollide määramise, valige käsk **Projektimeeskonna loomine**. Rakendus Project Service loob rollide, organisatsiooniüksuste ressursside ja projekti kalendri põhjal vähima arvu üldiseid meeskonnaliikmeid, koondades selleks ülesande määranguid.

> [!div class="mx-imgBorder"] 
> ![Kuvatõmmis projektimeeskonna loomisest.](media/FAQ-Resources-to-Tasks2-5.png "Kuvatõmmis projekti meeskonna loomisest")
 
Meeskonnaliikmete ruudustikus näete üldise ressursitüübiga ressursse koos rolli ja ametikoha nimega. Kui töö lõpetamiseks on rolli jaoks vaja kahte ressurssi, siis loob meeskonna loomise funktsioon kaks meeskonnaliiget ja kasutab nende eristamiseks ametikoha nime.

> [!div class="mx-imgBorder"] 
> ![Kuvatõmmis kahe üldise ressursi lisamisest.](media/FAQ-Resources-to-Tasks2-6.png "Kuvatõmmis kahe üldise ressursi lisamisest")
 
Saate avada üldise meeskonnaliikme varuressursi nõude, kui valite suvandi Ressursinõue all oleva lingi.

> [!div class="mx-imgBorder"] 
> ![Kuvatõmmis varuressursi nõude avamisest.](media/FAQ-Resources-to-Tasks2-7.png "Kuvatõmmis varuressursi nõude avamisest")

Valige üldise ressursi jaoks suvand **Reserveeri** ja seejärel saate kasutada ajakavapaneeli, et leida ning reserveerida päris ressurss. Samuti saate esitada nõude ressursihaldurile täitmiseks, kui valite käsu **Esita taotlus**.

Kui üldine ressurss on täidetud nimelise ressursiga, siis eemaldatakse üldine ressurss meeskonnast ja üldisele ressursile määratud ülesanded määratakse nimelisele ressursile, mis täitis üldise ressursi ressursinõude.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]