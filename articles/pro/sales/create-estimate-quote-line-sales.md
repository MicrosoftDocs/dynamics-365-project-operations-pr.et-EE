---
title: Projektipõhise hinnapakkumise rea prognoosimine
description: See teema sisaldab teavet, kuidas luua projektipõhisel hinnapakkumise real prognoosi.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a8e2b56b4a97ce184fc36145fffe63db8772bdef8bb89f9b60ddaf43db0c1ba4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997286"
---
# <a name="estimating-a-project-based-quote-line"></a>Projektipõhise hinnapakkumise rea prognoosimine

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Projektipõhine hinnapakkumise rida sisaldab üksikasju, mis aitavad prognoosida hinnapakkumise rea esitamisega seotud töö kulu ja potentsiaalset tulu.

Projektipõhise hinnapakkumise rea prognoosimiseks valige projektipõhise hinnapakkumise real vahekaart **Hinnapakkumise rea üksikasjad**. Projektipõhisel hinnapakkumise real on prognoosi loomiseks kaks võimalust.

- Prognoosi käsitsi otse hinnapakkumise real loomine, kasutades hinnapakkumise rea üksikasju. 
- Looge projekt ja projekti plaan ning seejärel seostage projekt ja projekti ülesanded hinnapakkumise reaga. Teie esitatava teabe põhjal projekti plaani prognooside hinnapakkumise reale importimise toiming saab olema lubatud.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Prognooside loomine otse projektipõhisel hinnapakkumise real

Projektipõhisel hinnapakkumise real prognoosi loomiseks valige vahekaart **Hinnapakkumise rea üksikasjad**. Reaüksus, mille sellel vahekaardil loote, arvutab kokku selle hinnapakkumise rea hinnapakkumise väärtuse. 

Hinnapakkumise rea üksikasjade looiseks valige andmeruudustikus **Hinnapakkumise rea üksikasjad** suvand **Uus hinnapakkumise rea üksikasi**. Avaneb kiirloomise liugur. Järgmises tabelis on toodud üksikasjad lehe **Hinnapakkumise rea üksikasi** väljade kohta ja kuidas väärtused funktsiooni mõjutavad.

| **Väli** | **Asukoht** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- | --- |
| Kirjeldus | Kiirloomine | Konkreetse prognoosi kirjeldus. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Kande klass | Kiirloomine | See ripploend sisaldab tehingu klasse, mis sisalduvad projektipõhise hinnapakkumise rea vahekaardil **Üldine**.  | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Vali toode | Kiirloomine | Kehtib, kui kandeklass on **Materjal**. Saate valida määrangu, et see prognoosirida on **olemasoleva** (kataloogi) toote või **sisestatava** toote jaoks. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Toode | Kiirloomine | Toote ID tootekataloogist. See väli on lubatud ainult juhul, kui valite väljal **Toote valimine** väärtuse **Olemasolev**. ID-d kasutatakse hinnapakkumise projekti hinnakirjast müügihinna toomiseks. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Sisestatav toode | Kiirloomine | Tekstikast, kuhu saab kirjutada toote nime. See väli on lubatud ainult juhul, kui valite väljal **Toote valimine** väärtuse **Sisestatav**.| See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Roll | Kiirloomine | Selle isiku roll, kes selle töö teostab või selle kulutuse teeb. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Kategooria | Kiirloomine | Töö või kulu kategooria. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Alguskuupäev | Kiirloomine | Töö alguskuupäev. | See väli läheb vaikimisi hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Lõppkuupäev | Kiirloomine | Töö lõpukuupäev. | See väli läheb vaikimisi hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Ressursi üksus | Kiirloomine | Ressursiühik, mis tekitab selle kulu ja annab sellega töötamiseks ressurssi. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt ja mida kasutatakse kuluhinna toomisel. |
| Üksuse ajakava | Kiirloomine | Töö, toote või kulu ühikurühm. Ühikud kuuluvad ühikute ajakavasse või ühikute rühma. Näiteks on miilid ja kilomeetrid ühikud, mis kuuluvad samasse kaugust kirjeldavasse ühikute rühma. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Üksus | Kiirloomine | Töö, toote või kulu ühik. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Kogus | Kiirloomine | Töö, toote või kulu kogus. | See väärtus läheb vaikimisi seotud hinnapakkumise rea üksikasjaks, mis luuakse automaatselt. |
| Ühiku hind | Kiirloomine |Tööd tegeva rolli arve määr, toote ühiku hind või toote või kulukategooria müügihind. Selle välja vaikeväärtus on **Aeg**, mis põhineb alguskuupäeval kehtiva projekti hinnakirja rolli hinnareal oleva hinnakujunduse dimensiooni kombinatsioonil. **Kulude** puhul on vaikeväärtuseks projekti hinnakirjas selle kandekategooria hinna seadistamine, mis kehtib alguskuupäeva jaoks. Kui tehingukategooria hinnakujundusmeetod pole ühiku hind, siis vaikeväärtust pole ja see väli jääb tühjaks. Toodete puhul põhineb vaikeväärtus projekti hinnakirja real **Hinnakirjaüksus**, mis kehtib alguskuupäeval.| Tööd tegeva rolli kulumäär, kulukategooria ühiku kulu või toote ühikukulu. Selle välja vaikeväärtus on **Aeg**, mis põhineb alguskuupäeval kehtiva projekti hinnakirja rolli hinnareal oleva hinnakujunduse dimensiooni kombinatsioonil. **Kulude** puhul on vaikeväärtuseks projekti hinnakirjas selle kandekategooria hinna seadistamine, mis kehtib alguskuupäeva jaoks. Kui tehingukategooria hinnakujundusmeetod pole ühiku hind, siis vaikeväärtust pole ja see väli jääb tühjaks. Toodete puhul põhineb vaikeväärtus projekti hinnakirja real **Hinnakirjaüksus**, mis kehtib alguskuupäeval.|
| Hinnanguline maks | Kiirloomine | Selle töö või kulu jaoks saate eeldatava maksu sisestada käsitsi. | Sellel väljal puudub allavoolu mõju. |
| Summa | Kiirloomine | Saate sisestada sellele väljale teavet käsitsi, kui väljad **Kogus** ja **Hind** on jäetud tühjaks. Kui need väljad pole tühjad, muutub see väli kirjutuskaitstuks ja arvutatakse (kogus \* ühikuhind) + käibemaks. | Sellel väljal puudub allavoolu mõju. |


## <a name="update-prices-on-quote-line-details"></a>Hinnapakkumise rea üksikasjade hindade värskendamine

Kui olete hinnapakkumisele lisatud projekti hinnakirjas või lepinguüksuse omahinnakirjas hindu muutnud, saate selle muudatuse kajastamiseks valida lehel **Hinnapakkumine** hindade värskendamiseks suvandi **Arvuta ümber**. Kui valite suvandi **Arvuta ümber**, kuvatakse hoiatus, mis annab teile teada, et hinnapakkumise rea hinnad lähtestatakse kõigi selle hinnapakkumise ridade jaoks. Valige **Jah**, et värskendada hindu nii müügi kui ka hinnapakkumise rea üksikasjade jaoks.

## <a name="access-quote-line-details-for-cost"></a>Juurdepääs kulu hinnapakkumise rea üksikasjadele

Valige vahekaardil **Hinnapakkumise rea üksikasjad** ruudustikus rida, et lubada andmeruudustiku tööriistaribal mõned toimingud. Andmeruudustiku tööriistariba esimene toiming, kui suvandis **Ava kulu üksikasjad** on valitud hinnapakkumise rea üksikasi. Valige **Ava kulu üksikasi**, et näha selle hinnapakkumise reaga seostuvat kulumäära ja summat.

> [!NOTE]
> Kulu hinnapakkumise rea üksikasja ressursi üksuse, koguse, kuupäevade, rolli või kategooria väärtuste muutmine muudab vastavaid väärtuseid müügi hinnapakkumise rea üksiaksjades.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Kulu ja müügi hinnapakkumise rea üksikasjade valuuta

Müügi hinnapakkumise rea üksikasjade valuuta tuleb vaikimisi projekti hinnakirjast, mis on hinnapakkumise rea üksikasja alguskuupäeval aktiivne.

Kulu hinnapakkumise rea üksikasjade valuuta tuleb vaikimisi hinnapakkumise lepinguüksuse hinnakirjast, mis on müügi hinnapakkumise rea üksikasja alguskuupäeval aktiivne.

Tasuvuse arvutustes teisendatakse hinnapakkumise rea üksikasjad kulu ja müügi kohta keskkonna põhivaluutasse, et teavitada hinnapakkumise üldisest eeldatavast marginaalist.

> [!MÄRKUS
> > Kuupäeval kehtivate valuutamäärade puudumise tõttu võivad esineda valuuta ümardamisvead ja muutunud marginaalid. Kasutage neid arvutusi ainult projektilepingutes, kuna need on hinnangulised ja need pole tegelikult seadusejärgsed või muul viisil mõeldud aruandluseks, mille puhul on vaja vahetuskursside täpsemat ümardamist ja kehtivuse kuupäeva tõhusust.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
