---
title: Edenemisel põhinevate arvete jaoks täpsemate lepingute loomine
description: Selles teemas kirjeldatakse, kuidas luua projekti lepinguid, et saaksite luua klientidele arveid vastavalt lõpuleviidud töö protsendile.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3b445488100e0a8335a05505405953b173ff836c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999666"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Edenemisel põhinevate arvete jaoks täpsemate lepingute loomine
[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua projekti lepinguid, et saaksite luua klientidele arveid vastavalt lõpuleviidud töö protsendile. Arve summad arvutatakse automaatselt projekti jaoks seadistatud eelarve töökategooriate jaoks. Arve ajastamine määratakse kliendiga projekti lepingu üle läbirääkimisi pidades.

Selle teema toimingute abil saate seadistada lepingu, seostatud projekti ja arveldamise reeglid, mis arvutavad arve summasid projekti jaoks määratud eelarveliste töökategooriate jaoks.

Kui olete lepingu ja projekti loonud, saate projekti üksikasjad seadistada. Näiteks saate määratleda tegevused ja määrata projektile töötajad.

## <a name="example"></a>Näide

Teie organisatsioon on tarkvara arendamise ettevõte. Nõustute välja töötama kliendi palgaarvestuse paketi, mille kogu tasu on 20 000 USA dollarit (USD). Teie organisatsioon nõustub esitama kliendile arve, kui olete teatud protsendi projektist lõpule viinud. Seadistate töö jaoks järgmised projekti kategooriad, et saaksite neid arveldusprotsessis kasutada.

- Nõustamine
- Kujundus
- Installimine

Seadistate ka arveldusreeglid, mis arvutavad automaatselt arve summad iga kategooria jaoks lõpuleviidud tööde protsendi ulatuses.

Eelarve haldur loob projekti kategooriate jaoks eelarve. Lõpetatud töö kogus arvutatakse automaatselt protsendina tegelikest töödest võrreldes eelarveliste summadega.

## <a name="prerequisites"></a>Eeltingimused

Enne, kui loote projekti, mis kasutab arveldusreegleid, peate seadistama arveldusreeglite numbriseeriad ja tasu töölehe, mida kasutatakse edenemisel arvete sisestamiseks.

1. Avage jaotis **Projektijuhtimine ja raamatupidamine** \> **Seadistamine** \> **Projektijuhtimise ja raamatupidamise parameetrid**.
2. Määrake lehe **Projektijuhtimise ja raamatupidamise parameetrid** vahekaardil **Numbriseeriad** numbriseeria, mida soovite kasutada arvete esitamise reeglite loomisel.
3. Avage jaotis **Projektihaldus ja raamatupidamine** \> **Töölehed** \> **Tasu**.
4. Valige lehel **Tasu tööleht** käsk **Uus** ja sisestage töölehe nimi.

## <a name="create-a-contract-for-progress-billings"></a>Edenemisel arvelduse jaoks leping loomine

Selle toimingu abil saate luua fikseeritud hinnaga projekti lepingu. Loote projekti arve, kui projektiga lõpuleviidud töö jõuab teatud protsendini.

1. Avage **Projektijuhtimine ja raamatupidamine** \> **Projektid** \> **Projekti lepingud**.
2. Valige lehel **Projekti lepingud** suvand **Uus**.
3. Määrake dialoogiaknas **Uus projekti leping** järgmised väljad.

    - **Nimi**
    - **Rahastamise tüüp**
    - **Rahastamise allikas**
    - **Müügi valuuta** - vaikimisi kasutatakse seda valuutat projekti lepinguga seotud kliendi arvete jaoks. Soovi korral saate aga teatud kliendi arve müügi valuutat muuta.

4. Valige **OK**. Teave kopeeritakse lehe **Projekti lepingud** päisesse.
5. Täitke lehel **Projekti lepingud** ülejäänud nõutav teave projekti kohta.

## <a name="create-a-project-for-progress-billings"></a>Edenemisel arvelduse jaoks projekti loomine

Projekti lepinguga seotud projekti ja mis tahes allprojektide loomiseks toimige järgmiselt.

1. Minge jaotisse **Projektijuhtimine ja raamatupidamine** \> **Projektid** \> **Kõik projektid**.
2. Valige lehel **Kõik projektid** suvand **Uus**.
3. Valige dialoogiakna **Uus projekt** väljal **Projekti tüüp** suvand **Aeg ja materjal**.
4. Valige projektirühm. Projektirühm määratleb sisestamise teabe nende projektide kohta, mis on rühmale määratud.
5. Valige käsk **Loo projekt**.
6. Pärast projekti loomist määrake projekti etapiks **Töötluses**.

## <a name="create-a-budget-for-a-project"></a>Projektile eelarve loomine

Eelarve kategooriaid kasutatakse automaatselt arve summade arvutamiseks iga kategooria jaoks lõpuleviidud tööde protsendi ulatuses. Järgige neid juhiseid, et luua prognoositava kulu jaoks eelarve kategooriad.

1. Minge jaotisse **Projektijuhtimine ja raamatupidamine** \> **Projektid** \> **Kõik projektid**.
2. Valige ja avage lehel **Kõik projektid** soovitud projekt.
3. Valige lehe **Projektid** toimingupaani vahekaardi **Plaan** rühmas **Eelarve** suvand **Projekti eelarve**.
4. Sisestage lehel **Projekti eelarve** igale projekti kategooriale prognoositav kulu.

## <a name="create-billing-rules-for-progress-billings"></a>Edenemisepõhise arvelduse jaoks arveldusreeglite loomine

1. Avage **Projektijuhtimine ja raamatupidamine** \> **Projektid** \> **Projekti lepingud**.
2. Valige ja avage lehel **Projekti lepingud** projekti leping.
3. Valige projekti lepingu lehe kiirvahekaardil **Arveldusreeglid** käsk **Lisa**.
4. Valige lehe **Arveldusreegel** väljal **Rea tüüp** suvand **Edenemine**.
5. Sisestage kiirvahekaardi **Arveldusreegli rea üksikasjad** väljale **Lepingu väärtus** lepingu koguväärtus.
6. Valige väljal **Kategooria** kategooria tasu tehingu sisestamiseks.
7. Valige väljal **Projekt** see projekt, mis kasutab seda arveldusreeglit.
8. Valikuline: arvelduseegli määramine täiendavatele projektidele. Valige kiirkaardi **Projekt** jaotises **Saadaolevad projektid** projekt ja seejärel valige parempoolne noolenupp, et lisada projekt jaotisse **Valitud projektid**.
9. Valikuline: protsendi summa arvutamine, mille klient arvel maksetest kinni on pidanud. Valige kiirvahekaardil **Maksete kinnipidamise tingimused** rahastamise allikas ja seejärel sisestage väljale **Kinnipidamise protsent** kinnipidamise protsent.
10. Korrake neid juhiseid, et luua projekti lepingu jaoks täiendavaid arveldusreegleid.


[!INCLUDE[footer-include](../includes/footer-banner.md)]