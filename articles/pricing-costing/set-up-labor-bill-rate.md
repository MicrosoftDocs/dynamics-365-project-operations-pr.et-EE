---
title: Tööjõukulu arveldusmäärade seadistamine
description: Selles teemas kirjeldatakse tööjõukulu määrade seadistamist Project Operationsis.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7d2dd7b6001ddb475d381d35a4863dcc4b322214
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004661"
---
# <a name="set-up-labor-bill-rates"></a>Töö arvelduskulu seadistamine

_ **Rakendub:** Project Operations ressursipõhiste/mitteladustatavate stsenaariumite jaoks

Igale hinnakirjale on seadistatud rolli hinnad või tööjõu määrad, mis kehtivad hinnakirja päises toodud kontekstile ja kehtivuskuupäevadele. Aja arvemäärasid Dynamics 365 Project Operationsis saab seadistada ainult ühes valuutas, mis on hinnakirja päise valuuta.

1. Müügihinna loendis töö arvelduskulu häälestamiseks avage **Müük** > **Kliendid** > **Hinnakirjad** ja valige **Uus**, et luua uus hinnakiri. 
2. Valige andmeruudustiku vahekaardil **Rolli hinnad** suvand **Uus rolli hind**. 
3. Sisestage paanil **Kiirloomine** rolli ja organisatsiooni üksuse kombinatsioon, mille jaoks teil on arveldusmäära seadistada vaja.

   Järgmises tabelis on rolli hinna rea vahekaardi **Üldine** väljad ja paan **Kiirloomine**, mida peate müügi hinnakirjale rolli hindade loomisel meeles pidama.

    | Väli | Asukoht | Kirjeldus | Allavoolu mõjud |
    | --- | --- | --- | --- |
    | Roll | Vahekaart **Üldine** ja paan **Kiirloomine** | Valige roll, mille jaoks soovite arveldusmäära määrata. | Sissetuleva prognoosi või tegeliku näitaja roll vastendatakse rolli vaikimisi arveldusmäära saamiseks selle reaga. |
    | Ressursiettevõte | Vahekaart **Üldine** ja paan **Kiirloomine** | Valige ettevõte või juriidiline isik, kellelt roll pärineb. Näiteks Fabrikam India arendaja või Fabrikam USA arendaja. | Sissetuleva prognoosi või tegeliku näitaja ressursiettevõte vastendatakse rolli vaikimisi arveldusmäära saamiseks selle reaga. |
    | Ressursi üksus | Vahekaart **Üldine** ja paan **Kiirloomine** | Valige ettevõtte organisatsiooniüksus või allüksus, kellelt roll pärineb. Näiteks Fabrikam India robootika allüksuse arendaja või Fabrikam USA tarkvara allüksuse arendaja. | Sissetuleva prognoosi või tegeliku näitaja ressursiüksus vastendatakse rolli vaikimisi arveldusmäära saamiseks selle reaga. |
    | Hind | Vahekaart **Üldine** ja paan **Kiirloomine** | Seadistage rollile, ressursiettevõttele ja ressursiüksuse kombinatsioonile arveldusmäär. Näiteks on Fabrikam India arendaja arveldusmäär 100 USD või Fabrikam USA arendaja arveldusmäär 150 USD. | Hind on vaikimisi arveldusmäär, mille vaikeväärtuseks on sissetuleva prognoosi või tehinguklassi Aeg tegeliku rea ühiku hind. |
    | Valuuta | Vahekaart **Üldine** ja paan **Kiirloomine**| Vaikimisi tuleb valuuta väärtus müügi hinnakirja päise valuutast. Müügi hinnakirjas ei saa valuutat alistada. | See valuuta on vaikimisi valuuta, mille vaikeväärtuseks on sissetuleva tehinguklassi Aeg tegeliku müügi rea hind. |
    | Üksuse ajakava | Vahekaart **Üldine** ja paan **Kiirloomine** | Ühiku ajakavaks on vaikimisi Aeg ja seda ei saa rolli hinna olemis muuta, sest seda kasutatakse määrade ajaühikute kaupa väljendamiseks. | Sellel väljal puudub allavoolu mõju. |
    | Üksus | Vahekaart **Üldine** ja paan **Kiirloomine** | Üksuse väärtus tuleb müügi hinnakirja päise väljalt **Ajaüksus**. Aga selle väärtuse saab tühistada. Näiteks Fabrikam India arendaja arveldusmäär on 1000 USD-i **India päeva** kohta. Fabrikam USA arendajal arveldusmäär on 1500 USD **USA päeva** kohta. | Kui ühiku hinna vaikeväärtuseks on sissetulev prognoos või tegeliku näitaja rida, kasutab süsteem ühiku hinna arvestamiseks ühikute süsteemi ja teisendamist baasühikuteks. Näiteks on prognoos 10 **India Days** võrra tööd India arendajale ja üksus India päev on määratletud kui 10 tundi. Kui hinnastatakse seda prognoosi rida, arvutab rakendus prognoosi ühikuhinna kui 1000 USD/10 tundi = 100 USD tunnis. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Hinnastamise üleviimine või arveldusmäärade seadistamine teiste organisatsiooniüksuste või allüksuste ressurssidele 

Projektipõhised ettevõtted kasutavad sageli erinevate juriidiliste isikute ja juriidilise isiku erinevate allüksuste töötajaid projektidega töötamisel. Projekte võidakse täita teatud juriidilisest isikust ja allüksusest, samas kui projektidega töötavad töötajad või konsultandid võivad pärineda kas samast juriidilisest isikust ja allüksusest või erinevast. Projekt võib koosneda ka erinevatest juriidilistest isikutest ja allüksustest pärit inimeste kombinatsioonist. Project Operationsis on juriidiline üksus, millele kuulub projekti kättetoimetamine **Omanikust ettevõtte** ja allüksus, millele kuulub täitmine, on **Lepingut sõlmiv üksus**. Kõik muud juriidilised isikud, mis pakuvad ressursse, on **Ressursiettevõtted** ja ressursse pakkuvad allüksused on **Ressursiüksused**. Tänu tööjõukulude erinevustele erinevates geograafilistes piirkondades ja tööturgudel kogu maailmas, seadistatakse tööjõukulu arveldusmäärad samuti erinevates geograafiates erinevalt.

Näiteks Fabrikam India robootika allüksuse arendaja, kes töötab USA projektiga, arveldatav tasu on 100 USD tunnis. Fabrikam USA robootika allüksuse arendaja, kes töötab USA projektiga, arveldatav tasu on 150 USD tunnis. 

### <a name="example-set-up-a-bill-rate"></a>Näide: arveldusmäära seadistamine 

1. Saate luua müügi hinnakirja nimega *Fabrikam USA arveldusmäärad* ja seadistada kehtivuskuupäeva.
2. Sisestage müügi hinnakirja järgmine teave.

    | Roll | Ressursiettevõte | Ressursiühik | Arveldusmäär |
    | --- | --- | --- | --- |
    | Arendaja | Fabrikam India | Fabrikam India-Robotics | 100 dollarit |
    | Arendaja | Fabrikam Philippines | Fabrikam Philippines-Robotics | 90 USD |
    | Arendaja | Fabrikam US | Fabrikam US-Robotics | 150 USD |

3. Lisage müügi hinnakiri **Fabrikam USA arveldusmäärad** projekti lepingu või teatud konto projekti hinnakirjale.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
