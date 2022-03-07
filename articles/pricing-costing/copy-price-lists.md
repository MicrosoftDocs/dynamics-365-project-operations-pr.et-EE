---
title: Hinnakirjade kopeerimine
description: Selles teemas antakse teavet, kuidas Project Operationsis hinnakirju kopeerida.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad09bdce563a48843b3ed96e7aaabd9c0d5960336b9e1c74fddb9b61f760f4cd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003721"
---
# <a name="copy-price-lists"></a>Hinnakirjade kopeerimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Hinnakirjade koopiaid saate luua rakenduses Dynamics 365 Project Operations. Näiteks saate luua eeloleva aasta hinnakirjad, kasutades selleks jooksva aasta hinnakirja.  Soovi korral võite kopeerida arve määrade ja müügihindade hinnakirja kulude hinnakirjast. 

Hinnakirjast koopia tegemiseks toimige järgmiselt.

1. Avage hinnakiri, millest soovite koopia teha, ja valige **Koopeeri**.
2. Sisestage hinnakirja kopeerimiseks vajalik teave. Järgmises tabelis on toodud teave, mida peaksite teabe sisestamisel silmas pidama.

| Väli | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- |
| Nimetus | Algse hinnakirja nimi, mille on lisatud **koopia**. | Hinnakiri sisaldab seda väärtust kõigil loendilehekülgedel ja rippmenüüvalikutel. |
| Kontekst | Sisestage eesmärgi hinnakirja soovitud kontekst. | Hinnakirja, mille kontekstiks on seatud **Kulu**, kasutatakse kulude prognooside ja tegelike kulude hinna otsimiseks. Hinnakirja, mille kontekstiks on seatud **Müük**, kasutatakse müükide prognooside ja tegelike müükide hinna otsimiseks. Kliendi, hinnapakkumiste või lepingu projekti hinnakirjale saab lisada ainult hinnakirju, mille kontekstiks on seatud **Müük**. |
| Alguskuupäev | Hinnakirja kehtivuse alguskuupäev. | Koos väljaga **Lõppkuupäev** kasutatakse seda välja, määramaks, milline hinnakiri on teatud prognoosile või tegelikule reale kohaldatav. |
| Lõppkuupäev | Hinnakirja kehtivuse lõppkuupäev. | Koos väljaga **Alguskuupäev** kasutatakse seda välja, määramaks, milline hinnakiri on teatud prognoosile või tegelikule reale kohaldatav. |
| Valuuta | Algse hinnakirja valuuta. Seda saab muuta. | Selle muutmisel teisendatakse kõik saadud tööjõu, kulude ja tootekataloogi üksuste hinnaread kopeerimise ajal eesmärgi hinnakirja valuutaks. |
| Ajaühik | Algse hinnakirja valuuta. Seda saab muuta. | Selle muutmisel teisendatakse kõik saadud tööjõu üksuste hinnaread kopeerimise ajal eesmärgi hinnakirja üksuseks. Kasutatakse algse hinnakirja ajaühiku ja eesmärgi hinnakirja ajaühiku üksuse seadistusest teisendamist. |
| Kirjeldus | Algse hinnakirja kirjeldus, mille on lisatud **koopia**. See on tekstiväli ja see võimaldab teil hinnakirja mitme reaga kirjeldada. | See väli kuvatakse hinnakirja vaates **Seostatud** erinevates üksustes, millel on seotud hinnakirjad. |

3. Salvestage hinnakiri. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Uuendage hinnakirja, rakendades kõigile hindadele hinnalisand

1. Hinnakirja vahekaartidel **Roll**, **Kategooria** ja **Hinnakirjaüksus** saate valida suvandi **Värskenda hindu**, et rakendada andmeruudustiku kõikidele hindadele hinnalisand. 
2. Sisestage avanevas dialoogiboksis hinnalisand. Hindade vähendamiseks teatud protsendi võrra saate sisestada ka negatiivse hinnalisandi protsendi. 
3. Valige dialoogi lehel **OK** ja kinnitage seejärel, et andmeruudustiku hinnad vastavad teie tehtud muudatustele.


[!INCLUDE[footer-include](../includes/footer-banner.md)]