---
title: Projektipõhised lepingurea prognoosimine
description: See teema sisaldab teavet projektipõhise lepingurea prognooside kohta.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24299d997074efcff3776168652809d490c81b17
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180457"
---
# <a name="estimate-a-projectbased-contract-line"></a>Projektipõhised lepingurea prognoosimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_ 

Rakenduses Dynamics 365 Project Operations sisaldab projektipõhine lepingurida üksikasju, mis aitavad hinnata projektipõhise lepingurea täitmiseks vajaliku töö kulu ja potentsiaalset tulu.

Projektipõhise lepingurea prognoosimiseks avage projekktipõhise **lepingurea** vahekaardile **Lepingurea üksikasi**.  Projektipõhise lepingurea prognoosi loomiseks on kaks moodust.

   - Luua prognoos otse lepingureal, lisades lepingurea üksikasjad käsitsi.
   - Luues projekti ja projektiplaani ning seejärel seostades projekti ja ülesanded projekti lepingureaga. See võimaldab protsessi, mille abil saate lepingureale sisestatud komponentide põhjal importida projektiplaani prognoosi lepingureale.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Prognoosi loomine otse projektipõhisel lepingureal

1. Avage lepingurida ja valige vahekaary **Lepingurea üksikasi**. Sellel vahekaardil loodavad read summeeritakse ja kuvatakse selle **lepingurea** suvandina **Lepinguline väärtus**. 
2. Andmeruudustikud **Lepingurea üksikasjad** valige suvand **+ Uus lepingurea üksikasi**. Avaneb kiirloomise liugur. Vormil **Lepingurea üksikasjad** on saadaval järgmised read.

| Väli | Asukoht | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- | --- |
| **Kirjeldus** | **Kiirloomine** | Konkreetse prognoosi kirjeldus. | Selle välja vaikeväärtus on automaatselt loodud kuludega seotud lepingurea üksikasi. |
| **Kande klass** | **Kiirloomine** | See ripploend on tehinguklasside loend, mis sisaldub projektipõhise lepingurea vahekaardil **Üldine**. | Selle välja vaikeväärtus on automaatselt loodud kuludega seotud lepingurea üksikasi. |
| **Roll** | **Kiirloomine** | Selle töö teostava või seda kulu kandva isiku roll. | Selle välja vaikeväärtus on automaatselt loodud kuludega seotud lepingurea üksikasi. |
| **Kategooria** | **Kiirloomine** | Töö või kulu kategooria. | Selle välja vaikeväärtus on automaatselt loodud kuludega seotud lepingurea üksikasi. |
| **Alguskuupäev** | **Kiirloomine** | Töö alguskuupäev. | Selle välja vaikeväärtus on automaatselt loodud kuludega seotud lepingurea üksikasi. |
| **Lõppkuupäev** | **Kiirloomine** | Töö lõpukuupäev. | Selle välja vaikeväärtus on automaatselt loodud kuluga seotud lepingurea üksikasi. |
| **Ressursiettevõte** | **Kiirloomine** | Ressursiettevõtte või juriidiline olem, mis kannab kulu ja pakub sellega töötamiseks ressursi. | Selle välja vaikeväärtus on automaatselt loodud kuludega seotud lepingurea üksikasi. Seda välja kasutatakse ka omahinna hankimiseks. |
| **Ressursi üksus** | **Kiirloomine** | Ressursi üksus, mis kannab selle kulu ja pakub sellega töötamiseks ressursi. | Selle välja vaikeväärtus on automaatselt loodud kuludega seotud lepingurea üksikasi. Seda välja kasutatakse ka omahinna hankimiseks. |
| **Üksuse ajakava** | **Kiirloomine** | Töö või kulu ühikurühm. Ühikud kuuluvad ühikute ajakavasse või ühikute rühma. Näiteks *miilid* ja *kilomeetrid (km)* on ühikud, mis kuuluvad vahemaad kirjeldavate ühikute rühma. | Selle välja vaikeväärtus on automaatselt loodud kuludega seotud lepingurea üksikasi. |
| **Ühik** | **Kiirloomine** | Töö või kulu ühik. | Selle välja vaikeväärtus on automaatselt loodud kuludega seotud lepingurea üksikasi. |
| **Kogus** | **Kiirloomine** | Töö või kulu kogus. | Selle välja vaikeväärtus on automaatselt loodud kuludega seotud lepingurea üksikasi. |
| **Ühiku hind** | **Kiirloomine** | Tööd teostava rolli või kulukategooria müügihinna arveldusmäär. Selle välja vaikeväärtus pärineb rollil põhineva **ajal** ja projekti hinnakirja ressursiüksuse kombinatsioonil, mis alguskuupäeval kehtib. Kulude jaoks on selle välja vaikeväärtus tehingukategooria hinnaseadistus projekti hinnakirjas, mis alguskuupäeval kehtib. Kui tehingu kategooria hinnakujunduse meetod pole **hind ühiku kohta**, siis vaikesäte puudub ja see väli jäetakse tühjaks. | Tööd teostava rolli või kulukategooria ühikupõhise hinna kulumäär. Selle välja vaikeväärtus on **rollil põhineb aeg** ja ressursiüksuse ühiku kombinatsioon omahinnakirja rolli hinnareal, mis on lisatud alguskuupäeval jõus olevale lepinguüksusele. Kulude jaoks on põhineb välja vaikeväärtus omahinnakirja kategooria hinnareal, mis on lisatud lepinguüksusele, mis alguskuupäeval kehtib. Kui tehingu kategooria hinnakujunduse meetod pole hind ühiku kohta, siis vaikesäte puudub ja see väli jäetakse tühjaks. |
| **Hinnanguline maks** | **Kiirloomine** | Kasutaja sisestatud selle töö või kulu prognoositav maks. | Kasutaja sisestatud selle töö või kulu prognoositav maks. |
| **Summa** | **Kiirloomine** | Kasutaja saab selle välja selle väärtuse saab lisada, kui väljad **Kogus** ja **Hind** on jäetud tühjaks. Kui väljad **Kogus** ja **Hind** on täidetud, siis väli **Suma** on kirjutuskaitstud ja arvutatakse järgmiselt: **(kogus \* ühiku hind) + maks**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Lepingurea üksikasjade hindade uuendamine

Kui muudate hindu projekti hinnakirjas, mis on lisatud lepingule või lepinguüksuse omahinnakirjas, saate muudatuste kajastamiseks värskendada üksiku lepingurea üksikasjade hindu. Valige lehel **Leping** suvand **Arvuta ümber**. Avaneb hoiatus, mis teatab, et selle lepingu kõikide lepinguridade hinnad lähtestatakse. Valige **Jah**, et värskendada nii müügi kui ka kulu lepingurea üksikasjade hindu.

## <a name="access-contract-line-details-for-cost"></a>Juurdepääs kulu lepingurea üksikasjadele

Valige vahekaardil **Lepingurea üksikasjad** ruudustikus rida, et kuvada andmeruudustiku tööriistaribal toimingud. Andmeruudustiku tööriistariba esimene toiming on **Ava kulu üksikasi**. Selle lepingurea üksikasja seostuva kulumäära ja summa vaatamiseks valige **Ava kulu üksikasi**. 

> [!NOTE]
> Väärtuse **Kulu** lepungurea üksikasja ressursiettevõtte, ressursi üksuse, koguse, kuupäevade, rolli või kategooria väärtuse muutmine muudab ka vastavaid väärtuse **Müük** lepingurea üksuses.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Kulu ja müügi leingurea üksikasjade valuuta

Suvandi **Müük** lepingurea üksikasi määrab vaikevaluuta projekti hinnakirjast, mis kehtib lepingurea üksikasja alguskuupäeval.

Suvandi **Kulu** lepingurea üksikasi määrab vaikevaluuta lepingu lepinguüksuse hinnakirjast, mis kehtib suvandi **Kulu** lepingurea üksikasja alguskuupäeval.

Tasuvusarvutused teisendavad **kulu** ja **müügi** lepingurea üksikasjade summad keskkonna põhivaluutasse, et teatada lepingu üldistest ja eeldatavatest marginaalidest.

> [!NOTE]
> Kuupäeval kehtivate valuutamäärade puudumise tõttu võivad esineda valuuta ümardamisvead ja muutunud marginaalid. Kasutage neid arvutusi projektilepingutes ainult ligikaudsena ja mitte tegeliku seadusjärgse või muu aruandluse jaoks, mis nõuab ümardamises suuremat täpsust ja vahetuskursside kehtivuse kuupäeva teadlikkust.
