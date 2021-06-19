---
title: Projekti arvete võlgnevuste haldamine
description: See teema sisaldab teavet erinevate saadaolevate vaadete kohta, mida kasutada projektide arveldamise mahajäämuse haldamisel.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddd0b62133139a8d9d8d09920986890bd8616808
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003941"
---
# <a name="manage-project-billing-backlog"></a>Projekti arvete võlgnevuste haldamine 

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakendusel Dynamics 365 Project Operations on eraldi vaated, mille abil arvete võlgnevusi hallata. Arvete võlgnevuste haldamiseks valige lingid jaotise **Arveldamine** alas **Müük**. 

Saadaval on järgmised vaated.

- Honorarid ja ettemaksed
- Saadaolevad honorarid ja ettemaksed
- Fikseeritud hinna vahe-eesmärgid
- Toodete arvete võlgnevused
- Ajakavast mahajäämus ja materjali arvete võlgnevused

## <a name="retainers-and-advances"></a>Honorarid ja ettemaksed

Vaates **Honorarid ja ettemaksed** loetletakse kõigis süsteemi projekti lepingutes ja ettemaksetes olevad honorarid ja ettemaksed. Pärast seda, kui honorar või ettemaks on arveldatud, muutub ettemakse summa kasutamiseks kättesaadavaks.

## <a name="available-retainers-and-advances"></a>Saadaolevad honorarid ja ettemaksed

Vaates **Saadaval honorarid ja ettemaksed** loetletakse kõigis süsteemi projekti lepingutes ja ettemaksetes saadaolevad honorarid ja ettemaksed. Pärast seda, kui honorar või ettemaks on arveldatud, muutub ettemakse summa kasutamiseks kättesaadavaks ja see lisatakse loendisse. Pärast seda, kui honorar või ettemakse on täielikult ära kasutatud, eemaldatakse see loendist.

## <a name="fixed-price-milestones"></a>Fikseeritud hinna vahe-eesmärgid

Vaates **Fikseeritud hinnaga vahe-eesmärgid** loetletakse kõigi süsteemi projektide lepinguridade fikseeritud hinnaga vahe-eesmärgid. Ühte või mitut vahe-eesmärke saab selles vaates märgistada kui **Arveldamiseks valmis** või **Pole arveldamiseks valmis**. Kui märgite vahe-eesmärgi olekuks **Arveldamiseks valmis**, muutub see kättesaadavaks arve mustandina.

Kui mitme kliendi lepinguridadel on fikseeritud hinnaga arveldusmeetod, luuakse lepingurea iga kliendi jaoks vahe-eesmärk. Vahe-eesmärgi saab luua ja seejärel jagada konkreetseteks kliendiga seotud vahe-eesmärgi kirjeteks. Jagamine on sisemine ja vastab lepingurea iga kliendi jaoks määratletud arvestatud protsendile. Vaates **Fikseeritud hinna vahe-eesmärgid** kuvatakse konkreetse kliendiga seotud vahe-eesmärgi kirjed. Kõik need vahe-eesmärgi kirjed saab märkida kui **Arveldamiseks valmis**, sellest vaatest eraldi. Kui üks või mitu seotud vahe-eesmärgi jagamist märgitakse kui **Arveldamiseks valmis**, päise olek värskendatakse olekust **Töös** olekuks **Ei ole alustatud**. Kui kõik vahe-eesmärkide jagamised on arveldatud, värskendatakse päise vahe-eesmärk, nii et selle olek on **Lõpetatud**.

Selles vaates kuvatakse arve mustandi vahe-eesmärk, mille arvelduse olek on **Kliendi arve on loodud**. Arve mustandi kinnitamisel värskendatakse kirje arveldamise olekuks **Kliendi arve on postitatud**. Ärge värskendage seda oleku väärtust kohandatud koodi abil. Rakendus Project Operation ei tööta õigesti, kui oleku väärtused on värskendatud kohandatud koodiga.

## <a name="product-billing-backlog"></a>Toodete arvete võlgnevused

Vaade **Toodete arvete võlgnevused** loetle kõik tootepõhised lepinguread kõikide süseemi projektilepingute üleselt. Ühe või mitu projektipõhist lepingurida saab selles vaates märgistada kui **Arveldamiseks valmis** või **Pole arveldamiseks valmis**. Kui märgite projektipõhise lepingurea olekuks **Arveldamiseks valmis**, muutub see kättesaadavaks arve mustandina.

Arve mustandil olev projektipõhine lepingurida kuvatakse selles vaates arvelduse olekuga **Kliendi arve on loodud**. Kui arve mustand kinnitatakse, muutub selle kirje arveldamise olekuks **Kliendi arve on sisestatud**. Ärge värskendage seda oleku väärtust kohandatud koodi abil. Rakendus Project Operation ei tööta õigesti, kui oleku väärtused on värskendatud kohandatud koodiga.

## <a name="time-and-material-billing-backlog"></a>Ajakavast mahajäämus ja materjali arvete võlgnevused

Vaade **Ajakavast mahajäämus ja materjali arvete võlgnevused** loetleb kõik arveldamata müügi tegelikud näitajad kõikid süsteemi projektilepingute üleselt, mille arve pole esitatud. Ühe- või mitmekordseid arveldamata müügi tegelikke näitajaid saab selles vaates märgistada kui **Arveldamiseks valmis** või **Pole arveldamiseks valmis**. Arveldamata müügi tegeliku näitaja märgistamine kui **Arveldamiseks valmis** muudab selle kättesaadavaks arve mustandina esitamiseks.

Arveldamata müüginäitajad, mille valiku **Ei saa ületada** olekuks on **Nurjunud**, ei saa märkida kui **Arveldamiseks valmis**. Kui näitajad peavad olema märgitud kui **Arveldamiseks valmis**, lähtestage olekuks määratud lepingurea tegelikud näitajad. ja seejärel hinnake uuesti olekut **Ei saa ületada**.

Kui mitme kliendiga sõlmitud lepinguridadel on aja- ja materjalikulu arveldamise meetod, siis luuakse aja ja kulu kinnitamisel iga lepingurea jaoks iga kliendi kohta üks arveldamata müügi näitaja, mis on iga kliendi jaoks määratletud arvestatud protsendina. Vaates **Aja- ja materjalikuluga arvete võlgnevus** näete neid kindlat klienti puudutavaid arveldamata müügi näitajaid. Kõik need arveldamata müügi tegelike näitajate kirjed saab märkida kui **Arveldamiseks valmis**, sellest vaatest eraldi.

Arve mustandil olev arveldamata müügi näitaja kuvatakse selles vaates arvelduse olekuga **Kliendi arve on loodud**. Kui arve mustand kinnitatakse, muutub selle kirje arveldamise olekuks **Kliendi arve on sisestatud**. Ärge värskendage seda oleku väärtust kohandatud koodi abil. Rakendus Project Operation ei tööta õigesti, kui oleku väärtused on värskendatud kohandatud koodiga.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
