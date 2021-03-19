---
title: Projektile ressursside pakkumine
description: Selles teemas kirjeldatakse projektile ressursside pakkumist.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 2003f6f06912b0c47eb942aae17e509b00e19487
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283003"
---
# <a name="propose-project-resources"></a>Projektile ressursside pakkumine

[!include [banner](../includes/psa-now-project-operations.md)]

Ressursihaldurid saavad projektijuhile ressursi pakkuda ressursitaotluse kaudu.

1. Tehke taotluse ruudustikust või taotlusest endast valik **Ressursside leidmine**
2. Valige lehel **Ajakava abimees** ressurss ja seejärel tehke paani **Ressursi broneeringu loomine** väljal **Broneeringu olek** valik **Broneeri**.

    ![Soovitatud ressurss on valitud.](media/Resource-Management-image62.png)

Ilmnevad järgmised olekuvärskendused.

- Lehel **Ajakava abimees** värskendatakse olekuindikaatoreid näitamaks, et broneering on soovituslik, mitte fikseeritult broneeritud.

    ![Soovitatud broneeringu olekuindikaatorid lehel Ajakava abimees](media/Resource-Management-image63.png)

- Ressursitaotluses muudetakse olekuks **Vajab ülevaatamist**.

    ![Ressursitaotluse olek muudeti väärtusele Vajab ülevaatamist.](media/Resource-Management-image64.png)

- Projekti vahekaardil **Meeskond** muudetakse üldiste meeskonnaliikmete väärtus **Taotluse olek** väärtusele **Vajab ülevaatamist**.

    ![Üldiste meeskonnaliikmete taotluse olek muudeti vahekaardil Meeskond väärtusele Vajab ülevaatamist](media/Resource-Management-image48.png)

Projektijuht saab ettepaneku vastu võtta või tagasi lükata.

Ressursihaldurid saavad ressursitaotluste töötlemisel kasutada kõiki järgmiseid meetodeid.

- Pakkuda nõudluse rahuldamiseks mitmeid ressursse, kui nõutavate tundide täitmiseks pole saadaval ühte ainukest ressurssi. Seejärel jaotatakse pakutud tunnid mitme ressursi vahel, mis suudavad nõutavate tundide nõudlust rahuldada. Selle stsenaariumi korral ei saa tunnid kattuda.
- Pakkuda vähem ressursse, kui on vaja. Selle stsenaariumi korral on pakutud ressursi võimsus väiksem kui nõutavad tunnid, mille taotleja määras. Seega, kui taotleja võtab pakutud ressursid vastu, luuakse ülejäänud nõudluse hõivamiseks täitmata ressursi nõue.
- Broneerida nõudluse rahuldamiseks mitmeid ressursse, kui töö lõpule viimiseks pole saadaval ühte ainukest ressurssi.
- Broneerida vähem ressursse, kui on vaja. Sel juhul on broneeritud tunde vähem kui nõutud tunde. Süsteem juhendab teid, et pakuksite broneeringute asemel ressursse, et taotleja saaks järelejäänud nõudlust kontrollida ja jälgida.

## <a name="billable-utilization"></a>Tasustatav kasutus

Ressurssidel võib olla tasustatav sihtkasutus. See sihtkasutus on määratletud kas ressursi vaikerolli atribuudina või määratud iga broneeritava ressursi kirjele. Kasutuse arvutused põhinevad tegelikel tundidel, mida ressursid on kinnitatud ajakandeid kasutades edastanud.

Kasutuse arvutamiseks kasutatakse järgmiseid valemeid.

- Tasustatav kasutus = arveldatavad tegelikud tunnid ÷ ressursivõimsus
- Mittetasustatav kasutus = tegelik aeg koos arveldustüübi ID-ga = mittetasustatav, täiendav või pole saadaval ÷ ressursivõimsus
- Sisemine = tegelik aeg ilma müügilepinguta ÷ ressursivõimsus
- Ressursivõimsus = ressursi töötunnid – kontorist väljasolek – puhkepäevad

Vaate **Ressursikasutus** leiate paanilt **Ressursid**.

![Ressursikasutuse vaade](media/Resource-Management-image65.png)

Iga ruudustiku lahter esindab perioodis (nt päev, nädal või kuu) oleva ressursi tasustatavat kasutusprotsenti. Lahtrite värvimiseks kasutatakse järgmisi valemeid.

- **Roheline:** tasustatav kasutus \>= ressursi sihtkasutus
- **Kollane:** sihtkasutus – 20 \<= tasustatav kasutus \< sihtkasutus
- **Punane:** tasustatav kasutus \< sihtkasutus – 20

Kuna vaade **Ressursikasutus** põhineb ajakavapaneelil, saate oma tulemuste filtreerimiseks kasutada ajakavapaneeli filtreerimise võimalusi.

Ruudustik nõuab, et määraksite sihtkasutuse kas rollile või konkreetsele ressursile. Selle seadistamiseks tehke valikud **Ressursid** \> **Ressursi rollid**.

Peale selle tuleb igale broneeritavale ressursile määrata vaikeroll. Avage **Ressursid** \> **Ressursid**. Kontrollige vahekaardil **Project Service**, et ressursi roll oleks määratletud ja selle väli **On vaikimisi** oleks määratud väärtusele **Jah**. Saate lisada veel rolle, kus väärtus **On vaikimisi = Ei**. Roll, kus väärtust **On vaikimisi = Jah**, kasutatakse ressursi kasutuse hindamiseks selle rolli eesmärgi suhtes.

![Vaikeroll on määratud](media/Resource-Management-image67.png)

Vahekaardil **Project Service** saate ressursi jaoks määrata ka eraldi sihtkasutuse. Seejärel kasutab kasutuse arvutus seda sihtkasutust, et hinnata ressursi sihti, mitte ressursi vaikerolli sihti.

Ressursi jaoks kuvatakse kasutus ainult juhul, kui sellel ressursil on ruudustikus kuvatud perioodi jooksul kinnitatud, arveldatavat aega.

## <a name="resource-availability"></a>Ressursi saadavus

On ülioluline, et ressursihaldurid saaksid vaadata ressursside saadavust ja värskendada broneeringuid. Mõnel juhul ametlik nõudlus puudub (ressursitaotlus), kuid ressursihaldur peab vastama kavandamata nõudlusele, mis esitatakse selliste kanalite nagu meil, telefonikõne või kiirsõnumid kaudu. Ressursihaldurid kasutavad ajakavapaneeli ressursside ja broneeringute värskendamiseks.

Ressurssi töötundide alusel arvutatakse ressursi saadavust. Ressursibroneeringud tarbivad ressursside võimsust.

![Ajakavapaneel](media/Resource-Management-image68.png)

Ajakavapaneel kasutab broneeringute, saadavuse ja ülebroneerimiste ning ka broneeringute oleku kuvamiseks värve ja varjustust. Ajakavapaneeli üks säte võimaldab teil kuvada legendi.

Kui ajakavapaneelil kuvatakse konkreetse broneeritava ressursi kõrval parempoole suunatud nool, saab ressurssi laiendada, et kuvada selle töö üksikasju, millele ressurss on broneeritud.

![Broneeritav ressurss on ajakavapaneelil laiendatud](media/Resource-Management-image69.png)

Kuna rakendus Dynamics 365 Project Service Automation kasutab mootorit Universal Resource Scheduling, ja kui teil on installitud ka rakendus Dynamics 365 Field Service, saate vaadata üksikasju projektide ressursibroneeringute, töötellimuste ja muude olemite kohta, millele olete kavandamise laiendanud.

![Projektide ressursibroneeringute ja töötellimuste üksikasjad](media/Resource-Management-image70.png)

Konkreetse ressursi kohta lisateabe saamiseks paremklõpsake seda, et avada ressursikaart.

![Ressursikaart](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]