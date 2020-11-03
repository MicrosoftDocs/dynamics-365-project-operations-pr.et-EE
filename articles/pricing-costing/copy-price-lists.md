---
title: Hinnakirjade kopeerimine
description: Selles teemas antakse teavet, kuidas Project Operationsis hinnakirju kopeerida.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91ee798a206ea5200780c8ebafc8f99cd9a3e219
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074995"
---
# <a name="copy-price-lists"></a>Hinnakirjade kopeerimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operationsis saate hinnakirjadest koopiaid luua. Näiteks saate luua eeloleva aasta hinnakirjad, kasutades selleks jooksva aasta hinnakirja.  Soovi korral võite kopeerida arve määrade ja müügihindade hinnakirja kulude hinnakirjast. 

Hinnakirjast koopia tegemiseks toimige järgmiselt.

1. Avage hinnakiri, millest soovite koopia teha, ja valige **Koopeeri**.
2. Sisestage hinnakirja kopeerimiseks vajalik teave. Järgmises tabelis on toodud teave, mida peaksite teabe sisestamisel silmas pidama.

| Väli | Asjakohasus, eesmärk ja juhised | Allavoolu mõjud |
| --- | --- | --- |
| Nimetus | Algse hinnakirja nimi, mille on lisatud **koopia**. | Hinnakiri sisaldab seda väärtust kõigil loendilehekülgedel ja rippmenüüvalikutel. |
| Kontekst | Sisestage eesmärgi hinnakirja soovitud kontekst. | Hinnakirja, mille kontekstiks on seatud **Kulu** , kasutatakse kulude prognooside ja tegelike kulude hinna otsimiseks. Hinnakirja, mille kontekstiks on seatud **Müük** , kasutatakse müükide prognooside ja tegelike müükide hinna otsimiseks. Kliendi, hinnapakkumiste või lepingu projekti hinnakirjale saab lisada ainult hinnakirju, mille kontekstiks on seatud **Müük**. |
| Alguskuupäev | Hinnakirja kehtivuse alguskuupäev. | Koos väljaga **Lõppkuupäev** kasutatakse seda välja, määramaks, milline hinnakiri on teatud prognoosile või tegelikule reale kohaldatav. |
| Lõppkuupäev | Hinnakirja kehtivuse lõppkuupäev. | Koos väljaga **Alguskuupäev** kasutatakse seda välja, määramaks, milline hinnakiri on teatud prognoosile või tegelikule reale kohaldatav. |
| Valuuta | Algse hinnakirja valuuta. Seda saab muuta. | Selle muutmisel teisendatakse kõik saadud tööjõu, kulude ja tootekataloogi üksuste hinnaread kopeerimise ajal eesmärgi hinnakirja valuutaks. |
| Ajaühik | Algse hinnakirja valuuta. Seda saab muuta. | Selle muutmisel teisendatakse kõik saadud tööjõu üksuste hinnaread kopeerimise ajal eesmärgi hinnakirja üksuseks. Kasutatakse algse hinnakirja ajaühiku ja eesmärgi hinnakirja ajaühiku üksuse seadistusest teisendamist. |
| Kirjeldus | Algse hinnakirja kirjeldus, mille on lisatud **koopia**. See on tekstiväli ja see võimaldab teil hinnakirja mitme reaga kirjeldada. | See väli kuvatakse hinnakirja vaates **Seostatud** erinevates üksustes, millel on seotud hinnakirjad. |

3. Salvestage hinnakiri. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Uuendage hinnakirja, rakendades kõigile hindadele hinnalisand

1. Vahekaartidelt **Roll** , **Kategooria** ja **Hinnakirjaüksus** saate valida suvandi **Värskenda hindasid** , et rakendada kõigile andmeruudustiku hindadele hinnalisand. 
2. Sisestage avanevas dialoogiboksis hinnalisand. Hindade vähendamiseks teatud protsendi võrra saate sisestada ka negatiivse hinnalisandi protsendi. 
3. Klõpsake dialoogiboksis nuppu **OK** ja veenduge, et andmeruudustikus olevad hinnad kajastaksid teie tehtud muudatusi.
