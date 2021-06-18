---
title: Projekti hinnapakkumise rea prognoosimine
description: Selles teemas antakse teavet projekti hinnapakkumiste real prognoosi loomise kohta.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: adb5a7f113b15abd2fe7364fa9b592d2c02db389
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000701"
---
# <a name="estimate-a-project-quote-line"></a>Projekti hinnapakkumise rea prognoosimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Projektipõhine hinnapakkumise rida sisaldab üksikasju, mis aitavad prognoosida hinnapakkumise rea esitamisega seotud töö kulu ja potentsiaalset tulu.

Projektipõhise hinnapakkumise rea prognoosimiseks valige hinnapakkumise real vahekaart **Hinnapakkumise rea üksikasjad**. Projektipõhisel hinnapakkumise real prognoosi loomiseks on kaks võimalust.

   - Prognoosi käsitsi otse hinnapakkumise real loomine, kasutades hinnapakkumise rea üksikasju. 
   - Looge projekt ja projekti plaan ning seejärel seostage projekt ja projekti ülesanded hinnapakkumise reaga. Teie esitatava teabe põhjal projekti plaani prognooside hinnapakkumise reale importimise toiming saab olema lubatud.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Prognooside loomine otse projektipõhisel hinnapakkumise real

Prognooside loomiseks otse projektipõhisele hinnapakkumise reale toimige järgmiselt.

1. Projektipõhisel hinnapakkumise real prognoosi loomiseks valige vahekaart **Hinnapakkumise rea üksikasjad**. Reaüksus, mille sellel vahekaardil loote, arvutab kokku selle hinnapakkumise rea hinnapakkumise väärtuse. 
2. Hinnapakkumise rea üksikasjade looiseks valige andmeruudustikus **Hinnapakkumise rea üksikasjad** suvand **Uus hinnapakkumise rea üksikasi**. Avaneb kiirloomise liugur. Lehel **Hinnapakkumise rida** on järgmised väljad.

| **Väli** | **Asukoht** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- | --- |
| Kirjeldus | Kiirloomine | Konkreetse prognoosi kirjeldus. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Kande klass | Kiirloomine | See ripploend sisaldab projektipõhise hinnapakkumise rea vahekaardil **Üldine** sisalduvaid tehinguklasse.  | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Vali toode | Kiirloomine | Kehtib, kui kandeklass on **Materjal**. Saate valida määrangu, et see prognoosirida on **olemasoleva** (kataloogi) toote või **sisestatava** toote jaoks. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Toode | Kiirloomine | Toote ID tootekataloogist. See väli on lubatud ainult juhul, kui valite väljal **Toote valimine** väärtuse **Olemasolev**. ID-d kasutatakse hinnapakkumise projekti hinnakirjast müügihinna toomiseks. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Sisestatav toode | Kiirloomine | Tekstikast, kuhu saab kirjutada toote nime. See väli on lubatud ainult juhul, kui valite väljal **Toote valimine** väärtuse **Sisestatav**.| See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Roll | Kiirloomine | Selle isiku roll, kes selle töö teostab või selle kulutuse teeb. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Kategooria | Kiirloomine | Töö või kulu kategooria. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Alguskuupäev | Kiirloomine | Töö alguskuupäev. | See väli läheb vaikimisi hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Lõppkuupäev | Kiirloomine | Töö lõpukuupäev. | See väli läheb vaikimisi hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Ressursiettevõte | Kiirloomine | Ressursiettevõte või juriidiline olem, mis tekitab selle kulu ja annab sellega töötamiseks ressurssi. | Väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt ja mida kasutatakse kuluhinna toomisel. |
| Ressursi üksus | Kiirloomine | Ressursiühik, mis tekitab selle kulu ja annab sellega töötamiseks ressurssi. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt ja mida kasutatakse kuluhinna toomisel. |
| Üksuse ajakava | Kiirloomine | Töö, toote või kulu ühikurühm. Ühikud kuuluvad ühikute ajakavasse või ühikute rühma. Näiteks on miilid ja kilomeetrid ühikud, mis kuuluvad samasse kaugust kirjeldavasse ühikute rühma. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Üksus | Kiirloomine | Töö, toote või kulu ühik. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Kogus | Kiirloomine | Töö, toote või kulu kogus. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Ühiku hind | Kiirloomine |Tööd tegeva rolli arve määr, toote ühiku hind või toote või kulukategooria müügihind. Välja **Aeg** vaikeväärtus põhineb alguskuupäeval kehtiva projekti hinnakirja rolli hinnareal oleva hinnakujunduse dimensiooni kombinatsioonil. **Kulude** puhul on vaikeväärtuseks projekti hinnakirjas selle kandekategooria hinna seadistamine, mis kehtib alguskuupäeva jaoks. Kui tehingu kategooria hinnakujunduse meetod pole hind ühiku kohta, siis vaikesäte puudub ja see väli jäetakse tühjaks. Toodete puhul põhineb selle välja vaikeväärtus projekti hinnakirja real **Hinnakirjaüksus**, mis kehtib alguskuupäeval.| Tööd tegeva rolli kulumäär, kulukategooria ühiku kulu või toote ühikukulu. Väli **Aeg** põhineb alguskuupäeval kehtivale lepinguüksusele lisatud kulu hinnakirja rolli hinnareal oleva hinnakujunduse dimensiooni kombinatsioonil. Kulude korral põhineb vaikeväärtus alguskuupäeval kehtivale lepinguüksusele lisatud kulu hinnakirja kategooria hinnareal. Kui tehingukategooria hinnakujundusmeetod pole ühiku hind, siis vaikeväärtust pole ja see väli jääb tühjaks. Toodete korral põhineb selle välja vaikeväärtus alguskuupäeval kehtivale lepinguüksusele lisatud kulu hinnakirja real **Hinnakirjaüksus**.|
| Hinnanguline maks | Kiirloomine | Selle töö või kulu jaoks saate eeldatava maksu sisestada käsitsi. | Sellel väljal puudub allavoolu mõju. |
| Summa | Kiirloomine | Saate sisestada sellele väljale teavet käsitsi, kui väljad **Kogus** ja **Hind** on jäetud tühjaks. Kui need väljad pole tühjad, muutub see väli kirjutuskaitstuks ja arvutatakse (kogus \* ühikuhind) + käibemaks. | Sellel väljal puudub allavoolu mõju. |

## <a name="update-prices-on-quote-line-details"></a>Hinnapakkumise rea üksikasjade hindade värskendamine

Kui muutsite hinnapakkumisele lisatud projekti hinnakirjas või lepinguüksuse omahinna hinnakirjus hindu, saate valida suvandi **Arvuta uuesti** lehel **Hinnapakkumine**, et värskendada selle muudatuse kajastamiseks üksiku hinnapakkumise rea üksikasjade hindu. Kui valite suvandi **Arvuta ümber**, kuvatakse hoiatus, mis annab teile teada, et hinnapakkumise rea hinnad lähtestatakse kõigi selle hinnapakkumise ridade jaoks. Valige **Jah**, et värskendada hindu nii müügi kui ka hinnapakkumise rea üksikasjade jaoks.

## <a name="access-quote-line-details-for-cost"></a>Juurdepääs kulu hinnapakkumise rea üksikasjadele

Kulu hinnapakkumise rea üksikasjadele juurdepääsuks tehke järgmist.

1. Valige vahekaardil **Hinnapakkumise rea üksikasjad** ruudustikus rida, et lubada toimingud alamruudustiku tööriistaribal. 
2. Valige **Ava kulu üksikasi**, et näha selle hinnapakkumise reaga seostuvat kulumäära ja summat.

> [!NOTE]
> Kulu hinnapakkumise rea üksikasja ressursi üksuse, koguse, kuupäevade, rolli või kategooria väärtuste muutmine muudab vastavaid väärtuseid müügi hinnapakkumise rea üksiaksjades.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Kulu ja müügi hinnapakkumise rea üksikasjade valuuta

Hinnapakkumise rea üksikasjades oleva valuuta projekti hinnakirjas määratud müügi vaikesummade jaoks, mis kehtib hinnapakkumise rea üksikasjade alguskuupäeval.

Hinnapakkumise rea üksikasjades oleva valuuta hinnapakkumise lepinguüksuse hinnakirjas määratud kulu vaikesummade jaoks, mis kehtib kulu hinnapakkumise rea üksikasjade alguskuupäeval.

> [!NOTE]
> Tasuvuse arvutustes teisendatakse hinnapakkumise rea üksikasjad kulu ja müügi kohta keskkonna põhivaluutasse, et teavitada hinnapakkumise üldisest eeldatavast marginaalist. Kuupäeval kehtivate valuutamäärade puudumise tõttu võivad esineda valuuta ümardamisvead ja muutunud marginaalid. Kasutage neid arvutusi ainult projekti hinnapakkumistes, kuna need on hinnangulised ja need pole tegelikult seadusejärgsed või muul viisil mõeldud aruandluseks, mille puhul on vaja vahetuskursside täpsemat ümardamist ja kehtivuse kuupäeva tõhusust.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
