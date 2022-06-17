---
title: Rollide seadistamine tööjaotuse struktuuri mallidel
description: Selles artiklis antakse teavet rolliteabe häälestamise kohta tööjaotuse struktuurimallides.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8721c5e5798c2b80c6f3eb65cef118d1ade5e680
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920791"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Rollide seadistamine tööjaotuse struktuuri mallidel

[!include [banner](../includes/banner.md)]

Projektijuhid saavad seadistada tööjaotuse struktuuri (WBS) malle, mida nad saavad rakendada, kui nad loovad uute projektide jaoks WBS-i. Projektijuhid saavad malli luues lisada rolle. Kasutage WBS-i mallile rolli määramiseks järgmist toimingut.

1. Valige **Projektijuhtimine ja raamatupidamine** > **Seadistamine** > **Projektid** > **Tööjaotuse struktuuri mallid**.
2. Valige valitud WBS-i malli jaoks suvand **Üksikasjad**.
3. Valige loendist tööülesanne ja seejärel väljal **Roll** valige ülesandele määramiseks roll.

## <a name="work-with-a-wbs"></a>WBS-iga töötamine

Saate luua uue WBS-i või kopeerida WBS-i olemasolevast WBS-i mallist. Projektijuht saab ressursse hõlpsalt hallata, määrates WBS-is uutele ülesannetele rollid. Rolle saab asendada kas pärast ressursi hankimist või pärast seda, kui kinnitatud ülesandega töötav ressurss on tuvastatud. See paindlikkus võimaldab projektijuhtidel teha järgmisi ülesandeid.

- Tuvastada ressursside arvu, mis on WBS-i tööpakettide jaoks nõutavad.
- Prognoosida projekti kulud.
- Määrata esialgne eelarve.
- Prognoosida rollide ja ressursside põhjal tegevuse kestust.
- Töötada välja mõned projekti haldamise kavad, mis põhinevad saadaoleval projekti teabel.

WBS-i on lisatud täiendavad valikud, et saaksite neid paremini kasutada.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Suvand</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressursimääramised</td>
<td>Saate vaadata WBS-i tööülesannete jaoks määratud ressursse, kuupäevi, tundide arvu ja reserveeringu tüüpi.</td>
</tr>
<tr class="even">
<td>Meeskonna automaatne loomine</td>
<td>Saate automaatselt lisada plaanitud ressursse, kasutades tööülesannetega seotud rolle. Finance soovitab plaanitud ressursse automaatselt, kasutades mitme kriteeriumiga otsuste analüüsi, mis põhineb rollidel. Pärast seda, kui rollid ja mahud (tunnid) on WBS-is ülesannete jaoks määratud ning pärast struktuuri vabastamist valige <strong>Loo meeskond automaatselt</strong>. Nõutav arv planeeritud ressursse lisatakse WBS-i ja vahekaardile <strong>Projekti ja meeskonna ajastamine</strong>.</td>
</tr>
<tr class="odd">
<td>Ressurss (ripploend)</td>
<td>Lehel <strong>Ressursi määramise käivitamine</strong> saate valida ressursid fikseeritud broneerimiseks või esialgseks broneerimiseks, olenevalt konkreetsest kestusest. Saate kohandada vaate sätteid, et näha ja määrata ressursi tegevuste kestuse. Saate ressursse valida ja määrata tööpaketi tasemel, kasutades järgmisi valikuid.
<ul>
<li><strong>Aktsepteeri</strong> – kinnitage tööülesande jaoks määratud ressursi muudatused.</li>
<li><strong>Tühista</strong> – tühistage tööülesande jaoks määratud ressursi muudatused.</li>
<li><strong>Määra automaatselt</strong> – saadaolev töötajate ressurss, millel on ühtiv roll, valitakse automaatselt ja määratakse valitud tööülesandele.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Lehel **Kõik projektid** valige projekt **XYZ värskenduse 2. etapp**.
2. Valige **Plaan** > **Tegevused** > **Tööjaotuse struktuur**.
3. Valige **Uus**, et lisada WBS-i järgmised esimese taseme tegevused.

    - Algatamine
    - Kavandamine
    - Täitmine
    - Jälgimine ja kontroll
    - Sule

4. Määrake kuupäevad ja mahud (tunnid), nagu järgmisel joonisel on näidatud.

    [![Kuupäevade ja pingutuse seadistamine.](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Valige ülesanderida **Algatamine** ja seejärel väljal **Roll** valige suvand **Vanem-projektijuht**.
6. Valige **Avalda**.
7. Valige samal real väljal **Ressurss** suvand **Danel Kangur** ja seejärel valige nupp **Nõustun**.
8. Valige ülesanderida **Planeerimine** ja seejärel väljal **Roll** valige suvand **Ärianalüüs**.
9. Valige käsk **Avalda** ja seejärel valige käsk **Loo meeskond automaatselt**.
10. Avanevas sõnumiväljas valige **Jah**.
11. Kontrollige, et välja **Ressurss** väärtuseks oleks **Ärianalüütik 1**.
12. Ressursi **Ärianalüütuk 1** puhul avage otsing ja valige **Käivita ressursi määramidśed**. Seejärel valige ülesande jaoks töötaja.
13. Valige **Esialgne määramine** &gt; **Täisvõimsus**.

    > [!NOTE] 
    > Teile ei kuvata hoiatust, et määratud ressurss on nüüd 2, kuna ressursside arvuks jääb 1.

14. Kontrollige lehel **Tööjaotuse struktuur** ressursi määramist WBS-ile ja seejärel valige käsk **Salvesta**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]