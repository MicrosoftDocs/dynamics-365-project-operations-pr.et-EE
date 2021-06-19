---
title: Projektipõhise lepingurea prognoosimine – liht
description: See teema sisaldab teavet projektipõhise lepingurea prognoosimise kohta.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e745bb5cb8e620e54f236aabdc006414c21290d3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003380"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Projektipõhise lepingurea prognoosimine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakenduses Dynamics 365 Project Operations sisaldab projektipõhine lepingurida üksikasju, mis aitavad hinnata projektipõhise lepingurea täitmiseks vajaliku töö kulu ja potentsiaalset tulu.

Projektipõhise lepingurea prognoosimiseks avage projekktipõhise **lepingurea** vahekaardile **Lepingurea üksikasi**.  Projektipõhise lepingurea prognoosi loomiseks on kaks moodust.

   - Luua prognoos otse lepingureal, lisades lepingurea üksikasjad käsitsi.
   - Luues projekti ja projektiplaani ning seejärel seostades projekti ja ülesanded projekti lepingureaga. See võimaldab protsessi, mille abil saate lepingureale sisestatud komponentide põhjal importida projektiplaani prognoosi lepingureale.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Prognoosi loomine otse projektipõhisel lepingureal

Prognooside loomiseks otse projektipõhisele lepingureale toimige järgmiselt.

1. Avage lepingurida ja valige vahekaary **Lepingurea üksikasi**. Sellel vahekaardil loodavad read summeeritakse ja kuvatakse selle **lepingurea** suvandina **Lepinguline väärtus**. 
2. Andmeruudustikus **Lepingurea üksikasjad** valige suvand **Uus lepingurea üksikasi**. Avaneb kiirloomise liugur. Lehel **Lepingurea üksikasjad** on saadaval järgmised väljad.

| Väli | Asukoht | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- | --- |
| **Kirjeldus** | **Kiirloomine** | Konkreetse prognoosi kirjeldus. | See väärtus läheb vaikimisi seotud lepingurea üksikasjaks, mis luuakse automaatselt. |
| **Kande liik** | **Kiirloomine** | See on projektipõhise lepingurea vahekaardil **Üldine** kaasatud kandeklasside loend. | See väärtus läheb vaikimisi seotud lepingurea üksikasjaks, mis luuakse automaatselt. |
| **Vali toode** | **Kiirloomine** | Kehtib, kui kandeklass on **Materjal**. Saate määrata, kas see prognoosirida on **olemasoleva** (kataloogi) toote või **sisestatava** toote jaoks. | See väärtus läheb vaikimisi seotud lepingurea üksikasjaks, mis luuakse automaatselt. |
| **Toode** | **Kiirloomine** | Toote ID tootekataloogist. See väli on lubatud ainult juhul, kui valite väljal **Toote valimine** väärtuse **Olemasolev toode**. ID-d kasutatakse lepingu projekti hinnakirjast müügihinna toomiseks. | See väärtus läheb vaikimisi seotud lepingurea üksikasjaks, mis luuakse automaatselt. |
| **Sisestatav toode** | **Kiirloomine** | Tekstiväli, kuhu toote nime sisestamiseks. See väli on lubatud ainult juhul, kui valite väljal **Toote valimine** väärtuse **Sisestatav**.| See väärtus läheb vaikimisi seotud lepingurea üksikasjaks, mis luuakse automaatselt. |
| **Roll** | **Kiirloomine** | Selle töö teostava või seda kulu kandva isiku roll. | See väärtus läheb vaikimisi seotud lepingurea üksikasjaks, mis luuakse automaatselt.|
| **Kategooria** | **Kiirloomine** | Töö või kulu kategooria. |See väärtus läheb vaikimisi seotud lepingurea üksikasjaks, mis luuakse automaatselt.|
| **Alguskuupäev** | **Kiirloomine** | Töö alguskuupäev. | See väärtus läheb vaikimisi seotud lepingurea üksikasjaks, mis luuakse automaatselt. |
| **Lõppkuupäev** | **Kiirloomine** | Töö lõpukuupäev. | See väärtus läheb vaikimisi seotud lepingurea üksikasjaks, mis luuakse automaatselt. |
| **Ressursi üksus** | **Kiirloomine** | Ressursiühik, mis tekitab selle kulu ja annab sellega töötamiseks ressurssi. |See väärtus läheb vaikimisi seotud lepingurea üksikasjaks, mis luuakse automaatselt ja mida kasutatakse kuluhinna toomisel. |
| **Üksuse ajakava** | **Kiirloomine** | Töö, toote või kulu ühikurühm. Ühikud kuuluvad ühikute ajakavasse või ühikute rühma. Näiteks *miilid* ja *kilomeetrid (km)* on ühikud, mis kuuluvad vahemaad kirjeldavate ühikute rühma. | See väärtus läheb vaikimisi seotud lepingurea üksikasjaks, mis luuakse automaatselt. |
| **Üksus** | **Kiirloomine** | Töö, toote või kulu ühik. | See väärtus läheb vaikimisi seotud lepingurea üksikasjaks, mis luuakse automaatselt. |
| **Kogus** | **Kiirloomine** | Töö, toote või kulu kogus. | See väärtus läheb vaikimisi seotud lepingurea üksikasjaks, mis luuakse automaatselt. |
| **Ühiku hind** | **Kiirloomine** | Tööd tegeva rolli arve määr, toote ühiku hind või toote või kulukategooria müügihind. See väli läheb vaikimisi väärtusele **Aeg**, mis põhineb alguskuupäeval kehtiva projekti hinnakirja rolli hinnareal oleva hinnakujunduse dimensiooni kombinatsioonil. **Kulude** jaoks on selle välja vaikeväärtus tehingukategooria hinnaseadistus projekti hinnakirjas, mis alguskuupäeval kehtib. Kui tehingu kategooria hinnakujunduse meetod pole **hind ühiku kohta**, siis vaikesäte puudub ja see väli jäetakse tühjaks. Toodete puhul põhineb selle välja vaikeväärtus projekti hinnakirja real **Hinnakirjaüksus**, mis kehtib alguskuupäeval.| Tööd tegeva rolli kulumäär või kulukategooria ühiku kulu või toote ühikukulu. See väli läheb vaikimisi väärtusele **Aeg**, mis põhineb alguskuupäeval kehtivale lepinguüksusele lisatud kulu hinnakirja rolli hinnareal oleva hinnakujunduse dimensiooni kombinatsioonil. Kulude jaoks on põhineb välja vaikeväärtus omahinnakirja kategooria hinnareal, mis on lisatud lepinguüksusele, mis alguskuupäeval kehtib. Kui tehingu kategooria hinnakujunduse meetod pole hind ühiku kohta, siis vaikesäte puudub ja see väli jäetakse tühjaks. Toodete korral põhineb selle välja vaikeväärtus alguskuupäeval kehtivale lepinguüksusele lisatud kulu hinnakirja real **Hinnakirjaüksus**.|
| **Hinnanguline maks** | **Kiirloomine** | Selle töö või kulu eeldatav maks. | Selle töö või kulu eeldatav maks. |
| **Summa** | **Kiirloomine** | Kui väljad **Kogus** ja **Hind** on tühjaks jäetud, saate selle välja väärtuse lisada. Kui väljad **Kogus** ja **Hind** on täidetud, siis väli **Summa** on kirjutuskaitstud ja arvutatakse järgmiselt: **(kogus \* ühiku hind) + maks**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Lepingurea üksikasjade hindade uuendamine

Kui muudate hindu projekti hinnakirjas, mis on lisatud lepingule või lepinguüksuse omahinnakirjas, saate muudatuste kajastamiseks värskendada üksiku lepingurea üksikasjade hindu. Valige lehel **Leping** suvand **Arvuta ümber**. Kuvatakse hoiatus, mis annab teile teada, et kõigi selle lepingu lepinguridade hinnad lähtestatakse. Valige **Jah**, et värskendada nii müügi kui ka kulu lepingurea üksikasjade hindu.

## <a name="access-contract-line-details-for-cost"></a>Juurdepääs kulu lepingurea üksikasjadele

Valige vahekaardil **Lepingurea üksikasjad** ruudustikus rida, et kuvada andmeruudustiku tööriistaribal toimingud. Andmeruudustiku tööriistariba esimene toiming on **Ava kulu üksikasi**. Selle lepingurea üksikasja seostuva kulumäära ja summa vaatamiseks valige **Ava kulu üksikasi**. 

> [!NOTE]
> Väärtuse **Kulu** lepungurea üksikasja ressursiettevõtte, ressursi üksuse, koguse, kuupäevade, rolli või kategooria väärtuse muutmine muudab ka vastavaid väärtuse **Müük** lepingurea üksuses.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Kulu ja müügi leingurea üksikasjade valuuta

Suvandi **Müük** lepingurea üksikasi määrab vaikevaluuta projekti hinnakirjast, mis kehtib lepingurea üksikasja alguskuupäeval.

Suvandi **Kulu** lepingurea üksikasi määrab vaikevaluuta lepingu lepinguüksuse hinnakirjast, mis kehtib suvandi **Kulu** lepingurea üksikasja alguskuupäeval.

Tasuvusarvutused teisendavad **kulu** ja **müügi** lepingurea üksikasjade summad keskkonna põhivaluutasse, et teatada lepingu üldistest ja eeldatavatest marginaalidest.

> [!NOTE]
> Kuupäeval kehtivate valuutamäärade puudumise tõttu võivad esineda valuuta ümardamisvead ja muutunud marginaalid. Kasutage neid arvutusi ainult projektilepingutes, kuna need on hinnangulised ja need pole tegelikult seadusejärgsed või muul viisil mõeldud aruandluseks, mille puhul on vaja vahetuskursside täpsemat ümardamist ja kehtivuse kuupäeva tõhusust.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
