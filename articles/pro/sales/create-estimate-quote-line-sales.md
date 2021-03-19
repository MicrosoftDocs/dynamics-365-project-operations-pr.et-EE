---
title: Projektipõhise hinnapakkumise rea prognoosimine
description: See teema sisaldab teavet, kuidas luua projektipõhisel hinnapakkumise real prognoosi.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dbd3876e555ee6bc70308ef11a3528a5dd8b6a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273508"
---
# <a name="estimating-a-project-based-quote-line"></a>Projektipõhise hinnapakkumise rea prognoosimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Projektipõhine hinnapakkumise rida sisaldab üksikasju, mis aitavad prognoosida hinnapakkumise rea esitamisega seotud töö kulu ja potentsiaalset tulu.

Projektipõhise hinnapakkumise rea prognoosimiseks valige projektipõhise hinnapakkumise real vahekaart **Hinnapakkumise rea üksikasjad**. Projektipõhisel hinnapakkumise real on prognoosi loomiseks kaks võimalust.

- Prognoosi käsitsi otse hinnapakkumise real loomine, kasutades hinnapakkumise rea üksikasju 
- Looge projekt ja projekti plaan ning seejärel seostage projekt ja projekti ülesanded hinnapakkumise reaga. Teie esitatava teabe põhjal projekti plaani prognooside hinnapakkumise reale importimise toiming saab olema lubatud.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Prognooside loomine otse projektipõhisel hinnapakkumise real

Projektipõhisel hinnapakkumise real prognoosi loomiseks valige vahekaart **Hinnapakkumise rea üksikasjad**. Reaüksus, mille sellel vahekaardil loote, arvutab kokku selle hinnapakkumise rea hinnapakkumise väärtuse. 

Hinnapakkumise rea üksikasjade looiseks valige andmeruudustikus **Hinnapakkumise rea üksikasjad** suvand **+ Uus hinnapakkumise rea üksikasi**. Avaneb kiirloomise liugur. Vormil **Hinnapakkumise rida** on järgmised väljad.

| **Väli** | **Asukoht** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- | --- |
| Kirjeldus | Kiirloomine | Konkreetse prognoosi kirjeldus. | See väli läheb vaikimisi seotud kulu hinnapakkumise rea üksikasjale, mis on automaatselt loodud. |
| Kande klass | Kiirloomine | See ripploend sisaldab projektipõhise hinnapakkumise rea vahekaardil **Üldine** sisalduvaid tehinguklasse.  | See väli läheb vaikimisi seotud kulu hinnapakkumise rea üksikasjale, mis on automaatselt loodud. |
| Roll | Kiirloomine | Isik, kes selle töö teostab või kulu tekitab. | See väli läheb vaikimisi seotud kulu hinnapakkumise rea üksikasjale, mis on automaatselt loodud. |
| Kategooria | Kiirloomine | Töö või kulu kategooria. | See väli läheb vaikimisi seotud kulu hinnapakkumise rea üksikasjale, mis on automaatselt loodud. |
| Alguskuupäev | Kiirloomine | Töö alguskuupäev. | See väli läheb vaikimisi seotud kulu hinnapakkumise rea üksikasjale, mis on automaatselt loodud. |
| Lõppkuupäev | Kiirloomine | Töö lõpukuupäev. | See väli läheb vaikimisi seotud kulu hinnapakkumise rea üksikasjale, mis on automaatselt loodud. |
| Ressursi üksus | Kiirloomine | Ressursiüksus, kes selle kulu tekitav ja esitab sellega töötamiseks ressursid. | See väli läheb vaikimisi seotud kulu hinnapakkumise rea üksikasjale, mis on automaatselt loodud. Seda välja kasutatakse ka omahinna hankimiseks. |
| Üksuse ajakava | Kiirloomine | Töö või kulu ühikurühm. Ühikud kuuluvad ühikute ajakavasse või ühikute rühma. Näiteks on miilid ja kilomeetrid ühikud, mis kuuluvad vahemaad kirjeldavate ühikute rühma. | See väli läheb vaikimisi seotud kulu hinnapakkumise rea üksikasjale, mis on automaatselt loodud. |
| Üksus | Kiirloomine | Töö või kulu ühik. | See väli läheb vaikimisi seotud kulu hinnapakkumise rea üksikasjale, mis on automaatselt loodud. |
| Kogus | Kiirloomine | Töö või kulu kogus | See väli läheb vaikimisi seotud kulu hinnapakkumise rea üksikasjale, mis on automaatselt loodud. |
| Ühiku hind | Kiirloomine | Tööd tegeva rolli arveldusmäär või kulukategooria müügihind. See väli läheb vaikimisi rollil põhinevale ajale ja projekti hinnakirja ressursiüksuse kombinatsioonile, mis alguskuupäeval kehtib. Kulude jaoks läheb see väli projekti hinnakirja tehingukategooria hinna seadistuses vaikeväärtusele, mis alguskuupäeval kehtib. Kui tehingu kategooria hinnakujunduse meetod pole hind ühiku kohta, siis vaikesäte puudub ja see väli jäetakse tühjaks. | Tööd tegeva roll kulumäär või kulukategooria kulu ühiku kohta. See väli läheb vaikimisi rollil põhinevale ajale ja hinnapakkumise hinnaloendi lepinguüksuse hinna ressursiüksuse kombinatsioonile, mis alguskuupäeval kehtib. Kulude jaoks läheb see väli lepinguüksuse omahinna hinnakirja tehingukategooria hinna seadistuses vaikeväärtusele, mis alguskuupäeval kehtib. Kui tehingu kategooria hinnakujunduse meetod pole hind ühiku kohta, siis vaikesäte puudub ja see väli jäetakse tühjaks. |
| Hinnanguline maks | Kiirloomine | Selle töö või kulu jaoks saate eeldatava maksu sisestada käsitsi. | Sellest väljast puudub allavoolu mõju. |
| Summa | Kiirloomine | Saate sisestada sellele väljale teavet käsitsi, kui väljad **Kogus** ja **Hind** on jäetud tühjaks. Kui need väljad pole tühjad, muutub see väli kirjutuskaitstuks ja arvutatakse (kogus \* ühikuhind) + käibemaks. | Sellest väljast puudub allavoolu mõju. |

## <a name="update-prices-on-quote-line-details"></a>Hinnapakkumise rea üksikasjade hindade värskendamine

Kui muutsite hinnapakkumisele lisatud projekti hinnakirjas või lepinguüksuse omahinna hinnakirjus hindu, saate valida suvandi **Arvuta uuesti** lehel **Hinnapakkumine**, et värskendada selle muudatuse kajastamiseks üksiku hinnapakkumise rea üksikasjade hindu. Kui valite suvandi **Arvuta ümber**, siis kuvatakse hoiatus, mis teatab, et kõigi selle hinnapakkumise ridade hinnapakkumise rea üksikasjade hinnad lähtestatakse. Valige **Jah**, et värskendada hindu nii müügi kui ka hinnapakkumise rea üksikasjade jaoks.

## <a name="access-quote-line-details-for-cost"></a>Juurdepääs kulu hinnapakkumise rea üksikasjadele

Valige vahekaardil **Hinnapakkumise rea üksikasjad** ruudustikus rida, et lubada andmeruudustiku tööriistaribal mõned toimingud. Andmeruudustiku tööriistariba esimene toiming, kui suvandis **Ava kulu üksikasjad** on valitud hinnapakkumise rea üksikasi. Valige **Ava kulu üksikasi**, et näha selle hinnapakkumise reaga seostuvat kulumäära ja summat.

> [!NOTE]
> Kulu hinnapakkumise rea üksikasja ressursi üksuse, koguse, kuupäevade, rolli või kategooria väärtuste muutmine muudab vastavaid väärtuseid müügi hinnapakkumise rea üksiaksjades.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Kulu ja müügi hinnapakkumise rea üksikasjade valuuta

Müügi hinnapakkumise rea üksikasjade valuuta tuleb vaikimisi projekti hinnakirjast, mis on hinnapakkumise rea üksikasja alguskuupäeval aktiivne.

Kulu hinnapakkumise rea üksikasjade valuuta tuleb vaikimisi hinnapakkumise lepinguüksuse hinnakirjast, mis on müügi hinnapakkumise rea üksikasja alguskuupäeval aktiivne.

Tasuvuse arvutustes teisendatakse hinnapakkumise rea üksikasjad kulu ja müügi kohta keskkonna põhivaluutasse, et teavitada hinnapakkumise üldisest eeldatavast marginaalist.

See võib põhjustada kuupäeval kehtivate valuutamäärade puuduse tõttu valuuta ümardamise tõrkeid ja muutmise marginaale. Kasutage neid arvutusi projekti hinnapakkumistes ainult ligikaudsena ja mitte tegeliku seadusjärgse või muu aruandluse jaoks, mis nõuab vahetuskursside ümardamise ja teadlikkuse suuremat täpsust.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]