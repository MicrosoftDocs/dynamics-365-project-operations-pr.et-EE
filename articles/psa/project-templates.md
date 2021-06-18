---
title: Projektimallid
description: Selles teemas antakse teavet selle kohta, kuidas kasutada projektimalle kiireks projekti seadistamiseks.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: bedcbc76d932a81e0c78bb58ce6a161446a26dde
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998271"
---
# <a name="project-templates"></a>Projektimallid 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektimall on eelmääratletud raamistik, mis aitab teil projekti alustada kiiresti ja hõlpsalt. Eelmääratletud malli abil saate luua uue projekti ühe klõpsuga. Nagu projektidegi puhul peate projektimallidele määratlema eeltingimused. Peate igale projektimallile määratlema projektikalendri ja organisatsioonis tuleb eelmääratleda rollid ning hinnakirjad, et malli komponendid sisaldaksid kasulikke andmeid.

Projektimall koosneb kolmest komponendist: ajakava, projekti prognoosid ja projektimeeskonna liikmed.

## <a name="schedule"></a>Kavanda

Projektimalli ajakava elemendid on samad, nagu projekti ajakavas. Saate luua ülesannete hierarhia, seostada rolle ülesannetega, määratleda ajakava atribuute ja määrata sõltuvusi. Projektimalli ajakava toetab ka iga ülesande jaoks ülesande režiime. Seetõttu toetab see kavandamismootorit. Projektiga tuleb seostada projektikalender. Töögraafiku loomisel pole projektimalli ja projekti vahel mingit erinevust.

## <a name="project-estimates"></a>Projekti prognoosid

Projektimalli projektiprognoosid töötavad sarnaselt projekti projektiprognoosidele. Kuid oma- ja müügihinnad võetakse parameetrites määratletud vaikimisi kulu- ning müügihinnakirjadest.

## <a name="creating-a-project-from-a-template"></a>Projekti loomine mallist
 
Projekti loomiseks projektimallist on mitu võimalust.

- Projekti loomisel hinnapakkumisest saate valida dialoogiboksis **Kiirloomine: projekt** projektimalli.

> ![Dialoogiboks Kiirloomine: projekt](media/project-11.png)

- Projekti loomisel suvandiga **Uus projekt**, kuvatakse enne kirje salvestamist leht **Projekt**. Valige väljal **Vali mall** üks organisatsiooni eelmääratletud projektimallidest.
- Kasutage lehel **Malliolem** suvandit **Loo projekt mallist**.

## <a name="copying-components-of-template-to-project"></a>Mallikomponentide kopeerimine projekti

Projektimalli komponentide kopeerimisel projekti võib projekti sätetest olenevalt ilmneda mõni erand.

### <a name="copying-the-schedule"></a>Ajakava kopeerimine

Kui projektil on mallist erinev projektikalender, rakendatakse ajakava kopeerimisel projektimallist ülesande ajakavale projekti kalendrist pärinevad töötunnid. Sel viisil kohandatakse ajakava ühtivaks projekti varukalendriga. Sellele sarnaselt rakendub ajakava esimesele ülesandele projekti alguskuupäev ja ülejäänud hierarhia ajakava värskendatakse mallis toodud kestuse ning sõltuvuste põhjal. 

### <a name="copying-project-estimates"></a>Projekti prognooside kopeerimine 

Projekti prognoosiridade üleselt kopeerimisel värskendatakse hinnakirju. Kulude hinnakirja korral põhinevad need värskendused projekti omaval üksusel. Müügihinnakirja korral põhinevad need kliendil. Müügiolemiga seotud projektide korral määratakse ühiku oma- ja müügihinnad nende hinnakirjade põhjal.

### <a name="copying-a-project-team"></a>Projektimeeskonna kopeerimine

Projektimeeskonna kopeerimisel projektimallist projekti kopeeritakse üldised ressursid koos mallis määratletud oskuste ja pädevustega. Üldiseid ressursi määramisi säilitatakse samamoodi, nagu nad olid projektimallis. Nimega ressursse projektimallides ei toetata.


[!INCLUDE[footer-include](../includes/footer-banner.md)]