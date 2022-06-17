---
title: Arvete võlgnevuste haldamine
description: Selles artiklis antakse teavet selle kohta, kuidas vaadata projektitoimingute arvelduse mahajäämust ja sellega töötada.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5be05639650bb5b9d646067e8d83bada60824081
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929368"
---
# <a name="manage-billing-backlog"></a>Arvete võlgnevuste haldamine

_ **Rakendub:** Project Operations ressursipõhiste/mitteladustatavate stsenaariumite jaoks

Rakendusel Dynamics 365 Project Operations on eraldi vaated, mille abil arvete võlgnevusi hallata. Arvete võlgnevuste haldamiseks valige lingid jaotise **Arveldamine** alas **Müük**. 

Saadaval on järgmised vaated.

- Honorarid ja ettemaksed
- Saadaolevad honorarid ja ettemaksed
- Fikseeritud hinna vahe-eesmärgid
- Ajakavast mahajäämus ja materjali arvete võlgnevused

## <a name="retainers-and-advances"></a>Honorarid ja ettemaksed

Vaade **Honorarid ja ettemaksed** loetleb kõikide projektilepingute honorarid ja ettemaksed. Pärast seda, kui honorar või ettemaks on arveldatud, muutub ettemakse summa kasutamiseks kättesaadavaks.

## <a name="available-retainers-and-advances"></a>Saadaolevad honorarid ja ettemaksed

Vaade **Saadaolevad honorarid ja ettemaksed** loetleb kõikide projektilepingute kõik saadaolevad honorarid ja ettemaksed. Pärast seda, kui honorar või ettemaks on arveldatud, muutub ettemakse summa kasutamiseks kättesaadavaks ja see lisatakse loendisse. Kui honorari või ettemakse summa on täielikult kasutatud, eemaldatakse see loendist.

## <a name="fixed-price-milestones"></a>Fikseeritud hinna vahe-eesmärgid

Vaade **Fikseeritud hinna vahe-eesmärgid** loetleb kõikide projekti lepinguridade fikseeritud hinnaga vahe-eesmärgid. Sellest vaatest saab ühe või mitu vahe-eesmärki märkida kui **Arveldamiseks valmis** või **Pole arveldamiseks valmis**. Kui märgite vahe-eesmärgi olekuks **Arveldamiseks valmis**, muutub see kättesaadavaks arve mustandina.

Kui mitme kliendi lepinguridadel on fikseeritud hinnaga arveldusmeetod, luuakse lepingurea iga kliendi jaoks vahe-eesmärk. Vahe-eesmärgi saab luua ja seejärel jagada konkreetseteks kliendiga seotud vahe-eesmärgi kirjeteks. Jagamine on sisemine ja vastab lepingurea iga kliendi jaoks määratletud arvestatud protsendile. Vaates **Fikseeritud hinna vahe-eesmärgid** kuvatakse konkreetse kliendiga seotud vahe-eesmärgi kirjed. Kõik need vahe-eesmärgi kirjed saab märkida kui **Arveldamiseks valmis**, sellest vaatest eraldi. Kui üks või mitu seotud vahe-etapi jaotust on märgitud kui **Arveldamiseks valmis**, värskendatakse päise olek valikult **Pole alustatud** olekule **Pooleli**. Kui kõik vahe-etapi jaotised on arveldatud, värskendatakse päise etapi olekuks **Lõpule viidud**.

Selles vaates kuvatakse arve mustandi vahe-eesmärk, mille arvelduse olek on **Kliendi arve on loodud**. Arve mustandi kinnitamisel värskendatakse kirje arveldamise olekuks **Kliendi arve on postitatud**. 

> [!NOTE] 
> Ärge värskendage seda olekuväärtust kohandatud koodi abil. Rakendus Project Operation ei tööta õigesti, kui oleku väärtused on värskendatud kohandatud koodiga.

## <a name="time-and-material-billing-backlog"></a>Ajakavast mahajäämus ja materjali arvete võlgnevused

Vaade **Ajakavast mahajäämus ja materjali arvete võlgnevused** loetleb kõik arveldamata müügi tegelikud näitajad kõikid süsteemi projektilepingute üleselt, mille arve pole esitatud. Ühe- või mitmekordseid arveldamata müügi tegelikke näitajaid saab selles vaates märgistada kui **Arveldamiseks valmis** või **Pole arveldamiseks valmis**. Arveldamata müügi tegeliku näitaja märgistamine kui **Arveldamiseks valmis** muudab selle kättesaadavaks arve mustandina esitamiseks.

Arveldamata müüginäitajad, mille valiku **Ei saa ületada** olekuks on **Nurjunud**, ei saa märkida kui **Arveldamiseks valmis**. Kui tegelikud andmed tuleb märkida kui **Arveldamiseks valmis**, lähtestage kinnitatud lepingurea teiste tegelike tulemuste olek ja hinnake seejärel olek **Mitte ületada** uuesti.

Kui mitme kliendiga sõlmitud lepinguridadel on aja- ja materjalikulu arveldamise meetod, siis luuakse aja ja kulu kinnitamisel iga lepingurea jaoks iga kliendi kohta üks arveldamata müügi näitaja, mis on iga kliendi jaoks määratletud arvestatud protsendina. Vaates **Aja- ja materjalikuluga arvete võlgnevus** näete neid kindlat klienti puudutavaid arveldamata müügi näitajaid. Kõik need arveldamata müügi tegelike näitajate kirjed saab märkida kui **Arveldamiseks valmis**, sellest vaatest eraldi.

Arveldamata müügi tegelik väärtus, mis on arve mustandil, kuvatakse selles vaates arve olekuga **Kliendiarve on loodud**. Kui arve mustand kinnitatakse, muutub selle kirje arveldamise olekuks **Kliendi arve on sisestatud**. 

> [!NOTE] 
> Ärge värskendage seda olekuväärtust kohandatud koodi abil. Rakendus Project Operation ei tööta õigesti, kui oleku väärtused on värskendatud kohandatud koodiga.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
