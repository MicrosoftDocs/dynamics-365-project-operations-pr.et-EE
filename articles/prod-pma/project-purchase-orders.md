---
title: Projekti ostutellimused
description: Selles artiklis kirjeldatakse mitmesuguseid meetodeid, mida saate kasutada projekti jaoks ostutellimuste loomiseks. Kasutatav meetod oleneb ostutellimuse eesmärgist ja millal ostetud üksuseid kasutatakse ning need projekti kuludesse kantakse.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074944"
---
# <a name="purchase-orders-for-a-project"></a>Projekti ostutellimused

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse mitmesuguseid meetodeid, mida saate kasutada projekti jaoks ostutellimuste loomiseks. Kasutatav meetod oleneb ostutellimuse eesmärgist ja millal ostetud üksuseid kasutatakse ning need projekti kuludesse kantakse.

### <a name="methods-for-creating-a-purchase-order"></a>Ostutellimuse loomise meetodid

Saate kasutada ühte järgmistest meetoditest, et luua suvandis Projektihaldus ja raamatupidamine ostutellimus. Ostutellimuse eesmärk määratleb, millal ostutellimust kasutatakse, ja seega, millal kantakse üksused projekti kuludesse.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Meetod</th>
<th>Eesmärk</th>
<th>Üksuste kasutamine</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Looge ostutellimus otse projektist.</td>
<td>Kasutage seda meetodit väliselt tarnijalt üksuste ostmiseks projektis kasutamiseks. Ostutellimuse saate luua kahel viisidel.
<ul>
<li>Projektist endast. Sellisel juhul on projekt juba ostutellimuse jaoks määratletud.</li>
<li>Navigeerides projekti ostutellimusele. Ostutellimuse loomiseks peate valima nii hankija kui ka projekti.</li>
</ul></td>
<td>Üksused võetakse kasutusele, kui tarnija arvet värskendatakse.</td>
</tr>
<tr class="even">
<td>Looge ostutellimus müügitellimusest.</td>
<td>Kasutage seda meetodit üksuste ostmiseks, kui loote projektist müügitellimuse.</td>
<td>Üksused võetakse kasutusele, kui müügitellimuse eest on kliendile saadetud arve.</td>
</tr>
<tr class="odd">
<td>Müügitellimuse loomine üksuse nõudest.</td>
<td>Kasutage seda meetodit üksuste ostmiseks, kui loote projektist üksuse nõude.</td>
<td>Üksused võetakse kasutusele, kui üksuse nõude saatelehte värskendatakse.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Hankija arve või saatelehe uuendamisel palutakse teil uuendada saateleht nõutavale üksusele.

Lisateavet vt teemast [Üksuse nõudest ostutellimuse üksuste vastuvõtmine](tasks/receive-items-purchase-order-item-requirement.md).
