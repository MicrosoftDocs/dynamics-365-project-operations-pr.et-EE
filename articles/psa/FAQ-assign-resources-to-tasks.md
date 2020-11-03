---
title: Ülesandele ressurssi määramine
description: Selles teemas kirjeldatakse, kuidas määrata ülesannetele ressursse.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075145"
---
# <a name="assign-a-resource-to-a-task"></a>Ülesandele ressurssi määramine

Rakenduses Microsoft Dynamics 365 Project Service Automation on kolm võimalust ülesandele ressursi määramiseks.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Ressursi broneerimine meeskonnaliikmena ja seejärel ressursi määramine ülesandele

Saate lisada ressursi projekti meeskonnale ja seejärel määrata projekti ajakavas ressurss ülesannetele.

1. Lisage vahekaardil **Meeskonnaliige** uus meeskonnaliige, klõpsates nuppu **Uus**. 

2. See avab paneeli **Meeskonnaliikme kiirloomine** , kus saate valida broneeritava ressursi nime ja määrata rolli. 

    Valige ressursi broneerimiseks üks järgmistest eraldamismeetoditest.

    - **Täisvõimsus** reserveerib määratud ajavahemikuks ressursi täieliku võimsuse.
    - **Protsendimaht** reserveerib määratud ajavahemikuks teatud protsendi ressursi võimsusest.
    - **Jaga ühtlaselt tundide järgi** broneerib ressursi määratud arvu tundideks, jagades aega määratud ajavahemikus ühtlaselt igale päevale.
    - **Jaga eesmine koormus tundide järgi** reserveerib ressursi määratud arvu tundideks, jagades aega määratud ajavahemikus nii, et suurem koormus jääks algusesse.
    - Suvand **Pole** lisab ressursi meeskonnale, kuid ei loo reserveeringuid, mis hõivaks tema võimsuse.

3. Valige ülesande ruudustikus **Ajakava** ressursilahtrist ikoon **Ressurss** ja seejärel jaotisest **Meeskonnaliige** see meeskonnaliige, kelle just lisasite. 

> [!NOTE]
> Vahekaartidel **Meeskonnaliikmed** kui ka **Sobitamine** näidatakse ressursi broneeritud ja määratud tunde. Tunnid peaksid olema samad, kuid see pole nõutav, sest broneeringud ja määrangud ei ole tihedalt ühendatud. Kui need on erinevad, siis esitab vahekaart **Sobitamine** teile üksikasju, näiteks kui määrate ressurssi rohkematele tundidele, kui olete broneerinud. Vajaduse korral saate nende andmete põhjal teha parandusi, näiteks pikendada ressursi broneeringuid või muuta määrangut.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Üldise meeskonnaliikme loomine ülesannete määramistega

Kui loote üldise meeskonnaliikme ülesande määramise kaudu, loote te kohatäite või üldise ressursi, mis kirjeldab nimega ressursi tunnuseid, keda soovite ülesannetele tööle määrata. Seejärel loote nõude (või esitate nõude taotlusega), mida kasutatakse nimega ressursi otsimiseks ja broneerimiseks.

1. Valige ülesande ruudustikus **Ajakava** ressursilahtrist ikoon **Ressurss**.

2. Sisestage nimi kohatäite ressursi nime jaoks. Nt programmihaldur.

3. Valige **Loo** ja määrake väljal **Projekti meeskonnaliikme kiirloomine** üldise ressursi roll.

4. Saate jätkata sellele kohatäite ressursile ülesannete määramist, kui valite ressursi ülesandele jaotisest **Ressursivalija**. Need on loetletud jaotises **Meeskonnaliikmed**.

5. Kui olete üldise ressursi määramisega lõpetanud, valige üldine ressurss vahekaardilt **Meeskond** ja valige käsk **Loo nõue** , et luua üldise ressursi jaoks ressursinõue.

6. Valige üldise ressursi jaoks käsk **Reserveeri**. Seejärel saate kasutada ajakavapaneeli, et otsida ja broneerida päris ressurssi. Samuti saate esitada nõude ressursihaldurile täitmiseks.

7. Kui üldine ressurss on täidetud nimelise ressursiga, siis eemaldatakse üldine ressurss meeskonnast ja üldisele ressursile määratud ülesanded määratakse nimelisele ressursile, mis täitis üldise ressursi ressursinõude.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Nimega ressursi määramine kõikide broneeritavate ressursside loendist

Saate kasutada **Ressursivalija** otsinguvälja, et otsida kõiki broneeritavaid ressursse ja neid ülesandele määrata.

Sel viisil määratud ressursid lisatakse meeskonda ilma broneeringuta. See on sarnane meeskonnaliikmete lisamise ja mitte eraldamise meetodi valimisega. Neid kuvatakse vahekaartidel **Meeskond** ja **Sobitamine** ressurssidena, millel on vaid määrangud ja broneeringute puudujääk. Reserveerige neid, kui soovite nende saadavaolekut kasutada.

1. Valige ülesande ruudustikus **Ajakava** ressursilahtrist ikoon **Ressurss**.

2. Alustage nime tippimist. Nime otsingutulemused kuvatakse jaotise **Muud ressursid** all olevas **Ressursivalijas**.

3. Valige loendist ressurss, mille soovite ülesandele määrata.
