---
title: Päevarahad
description: Selles teemas antakse teavet kuluhalduses kasutatavate päevarahade reeglite kohta.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908058"
---
# <a name="per-diems"></a>Päevarahad

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_


Päevaraha on hüvitis, mida makstakse töötajale, kes töö tõttu reisib. Kuluhalduses saate erinevate reisi olukordade jaoks luua päevaraha. Päevarahade määrad võivad põhineda aastaajal, reisisihtkohal või mõlemal. Päevarahade reegli loomisel saate määrata, et teatud protsent päevarahade hinnast jäetakse maksmata, kui töötaja saab tasuta einet või teenust. Samuti saate määrata minimaalse ja maksimaalse tundide arvu, mille võrra päevaraha töötaja reisile rakendada saab.

## <a name="configuration"></a>Konfiguratsioon 

1. Päevarahade sihtkohtade lisamiseks minge jaotisse **Seadistus** > **Arvutused ja koodid** > **Päevarahade sihtkohad**.
2. Valige iga ülaltoodud asukoha kohta päevarahade määr ja valuuta, mis kehtib hotelli, toitlustuse ja muude kulude tarbeks kindla algus-ja lõppkuupäeva vahel. Päevarahade määrad ja valuutad konfigureeritakse jaotises **Seadistus** > **Arvutused ja koodid** > **Päevarahad**.
3. Konfigureerige lehel **Päevarahade sihtkohad** päevarahade määra tasemed. Päevarahade määra tasemed võimaldavad teil määratleda hotelli-, eine- ja muude kulude päevaraha jagamise protsendi. 
4. Hommikusöögi, lõunasöögi või õhtusöögi jaoks söögikorra protsentuaalse vähendamise määramiseks värskendage lehe **Kuluhalduse parameetrid** vahekaardi **Päevarahad** välju. 
    
## <a name="submit-expenses-using-per-diem"></a>Kulude esitamine päevarahade abil
Päevarahade kasutamiseks kulude esitamiseks kasutage kuluaruande loomisel kulukategooriat **Päevarahad**. Sisestage **Päevarahad alates kuupäevast**, **Päevarahad kuupäevani** ja **Päevarahade sihtkoht**. Summa arvutatakse vastavalt päevarahade määradele valitud asukoha jaoks ja eine vähendamine arvutatakse päevaraha määrade tasemete põhjal.
