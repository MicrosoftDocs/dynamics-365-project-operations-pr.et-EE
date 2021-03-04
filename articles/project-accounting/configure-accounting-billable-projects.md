---
title: Arveldatavate projektide raamatupidamise konfigureerimine
description: See teema sisaldab teavet arveldatavate projektide raamatupidamise valikute kohta.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 47bb5671c7b80c0e96f3f65e9c4d25f6da8184a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131968"
---
# <a name="configure-accounting-for-billable-projects"></a>Arveldatavate projektide raamatupidamise konfigureerimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Rakendust Dynamics 365 Project Operations toetab arveldatavate projektide erinevaid raamatupidamise valikuid, mis hõlmavad aja- ja materjalikulu ning fikseeritud hinnaga kandeid.

- **Aja- ja materjalikulu kanded**: need kanded arveldatakse töö edenemise ajal projekti tundide, kulude, kaupade või tasude põhjal. Need kannete kulud saab vastendada iga kande tuluga ja projekti arveldamine toimub töö edenedes. Projekti tulu saab ka koguda ka kande toimumise ajal. Arveldamise ajal tulu kajastatakse ja kui see on kohaldatavad, siis viittulu arvestatakse maha.
- **Fikseeritud hinnaga kanded**: need kanded arveldatakse vastavalt projekti lepingul põhinevale arvete ajakavale. Fikseeritud hinnaga kannete tulu saab kajastada arveldamisel või arvutada ja sisestada perioodiliselt vastavalt **lõpetatud lepingu** või **lõpetatud protsendi meetoditele**.

Projekt loetakse arveldatavaks, kui see on seostatud ühe või mitme lepingureaga. Projekti lepingurida määratleb enda jaoks, millist tüüpi makseviis ja kandetüübid on lubatud.

Näiteks Fabrikami robootika on võitnud projekti lepingu ettevõttega Adatum Corporation seadmete optimeerimiseks. Adatum maksab fikseeritud summa 10 000 eurot, et katta tekkivad projekti kulud. See on fikseeritud hinnaga arveldusmeetod. Projekti aeg ja tasud arveldatakse vastavalt kasutusele. See on aja- ja materjalikannete arveldusmeetod. Kogu tööd jälgitakse ühe projekti all nimega Adatum, seadmete optimeerimine.

Projekti meeskonnaliige esitab kaheksa tundi tööd projektile Adatum, seadmete optimerimine. Kui projektijuht kinnitab selle aja, kasutab süsteem tegelike näitajate kannete, arve ja konto loomiseks aja ja materjali arveldusmeetodit. Seda kannet ei kaasata fikseeritud hinna tulu hinnangulisse arvutusse.

Teine projektimeeskonna liige esitab seoses projektiga Adatum, seadmete optimeerimine reisikulud summas 2000 eurot. Kui projektijuht kinnitab selle esituse, kasutab süsteem tegelike näidete kannete ja selle projei kulu jaoks konto loomiseks fikseeritud hinna arveldusmeetodit. Kliendile ei saadeta selle tehingu põhjal arvet. Selle asemel arveldatakse need kasutades eraldi konfigureeritud arveldamise vahe-eesmärke. See kulukanne koos kuluhinnangutega kaasatakse fikseeritud hinna tulu hinnangulisse arvutusse.

Projektikannete raamatupidamise põhimõtted on määratletud projekti kulu ja tuli profiilides. Iga projektikande puhul määratleb süsteem vastava projekti kulu ja tulu profiili, kasutades konfigureeritud projekti kulu ja tulu profiili reegleid.

## <a name="define-project-cost-and-revenue-profiles"></a>Projekti kulu ja tulu profiilide määratlemine 

Projektu kulu ja tulu profiilid määravad projekti kannete raamatupidamise reeglid. Need profiilid on konfigureeritud projektihalduses ja raamatupidamises. 

Tehke järgmist, et luua uus projekti kulu ja tulu profiil. 

1. Avage **Projektihaldus ja raamatupidamine** > **Seadistamine** > **Postitamine** > **Projekti kulu ja tulu profiilid**. 
2. Valige **Uus**, et luua uus projekti kulu ja tulu profiil.
3. Sisestage väljale **Nimi** profiili nimetus ja lühikirjeldus.
4. Väljal **Arveldusmeetod** valige **Aeg ja materjal** või **Fikseeritud hind**.
5. Laiendage kiirvahekaarti **Pearaamat**. Sellel vahekaardil olevatel väljadel määratletakse raamatupidamise põhimõtted, mida kasutatakse Project Operationsi integreerimise töölehte kasutades projekti kannete töölehele sisestamisel ja seejärel projekti arve soovituse kaudu arveldamisel.
6. Valige kiirkaardi **Pearaamat** järgmistel väljadel vastav teave.

    - **Järelkulu – tund**.

       - *Ilma pearaamatuta*: ajakannete kulu ei sisestata pearaamatusse, kui Project Operationsi integreerimise tööleht postitatakse. Samas saab raamatupidaja postitada kulud kasutades hiljem kulude postitamise funktsiooni.
       - **Saldo**: ajakannete kulu debiteeritakse pearaamatu kontotüübiga *WIP – kulu väärtud* ja krediteeritakse pearaamatu postitamise seadistuses *palgaarvestuse kohtoga*. Raamatupidaja kasutab järelkulu funktsiooni, et teisaldada see kulu saldo kontolt perioodiliselt kasumiaruandesse.
       - **Kasumiaruanne**: Project Operationsi integratsiooni töiölehe postitamisel debiteeritakse ajatehingu kulu pearaamatu kontotüübiga *Kulu* ja krediteeritakse *palgaarvestuse kontoga*, mis on määratletud vahekaardil **Kulu** lehel **Pearaamatu postitamise seadistus** (**Projektihaldus ja raamatupidamine** \> **Seadistamine** \> **Postitamine** \> **Pearaamatu postitamise häälestus**). See on kõige tavalisem aja- ja materjalikulu kannete seadistus.
        - *Mitte kunagi pearaamat*: ajakande kulusid ei postitata kunagi pearaamatusse.

    - **Järelkulud – kulu**.

         - **Saldo**: Project Operationsi integratsiooni töölehe postitamisel debiteeritakse kulukande kulu pearaamatu kontotüübiga *WIP –kulu väärtus*, mis on määratletud vahekaardil **Kulu** lehel **Pearaamatu postitamise seadistus** ja krediteeritakse töölehe rea tasaarvelduskontoga. Vaikimisi kulu tasaarvelduskontod on määratletud jaotises **Projektihaldus ja raamatupidamine** > **Seadistamine** \> **Postitamine** \> **Kulude vaikimisi tasaarvelduskonto**. Raamatupidaja kasutab **järelkulu** funktsiooni, et teisaldada see kulu saldo kontolt perioodiliselt kasumiaruandesse.
        - **Kasumiaruanne**: Project Operationsi integratsiooni töölehe postitamisel debiteeritakse kulukande kulu pearaamatu kontotüübiga *Kulu*, mis on määratletud vahekaardil **Kulu** lehel **Pearaamatu postitamise seadistus** ja krediteeritakse töölehe rea tasaarvelduskontoga. Vaikimisi kulu tasaarvelduskontod on määratletud jaotises **Projektihaldus ja raamatupidamine** \> **Seadistamine** \> **Postitamine** \> **Kulude vaikimisi tasaarvelduskonto**.
       
    - **Arveldamine kontol**.

        - **Saldo**: projekti arve ettepaneku postitamisel krediteeritakse kontopõhine tehing (arveldamise vahe-eesmärk) pearaamatu konto tüübil *WIP arveldatud – kontol*, mis on määratletud vahekaardil **Tulu** lehel **Pearaamatu postitamise häälestamine** ja debiteeritakse kliendi saldo kontolt.
         - **Kasumiaruanne**: projekti arve ettepaneku postitamisel krediteeritakse kontopõhine tehing (arveldamise vahe-eesmärk) pearaamatu konto tüübil *Arveldatud tulu – kontol*, mis on määratletud vahekaardil **Tulu** lehel **Pearaamatu postitamise häälestamine** ja debiteeritakse kliendi saldo kontolt. Kliendi saldo kontod on määratletud jaotises **Müügireskonto** \> **Seadistamine** \> **Kliendi postitamise profiilid**.

   Kui määrate aja ja materjali arveldusmeetoditele postitamise profiilid, on teil võimalik koguda tulu vastavalt tehingu tüübile (tund, kulu ja tasu). Kui valik **Viittulu** on seatud valikule **Jah**, salvestatakse Project Operationsi integratsiooni töölehe arveldamata müügitehingud üldisesse pearaamatusse. Müügiväärtus debiteeritakse kontol **WIP – müügiväärtuse konto** ja krediteeritakse kontol **Viittulu – müügiväärtus**, mis seadistati lehel **Pearaamatusse postitamise seadistus** vahekaardil **Tulu**. 
  
  > [!NOTE]
  > Valik **Viittulu** on saadaval ainult juhul, kui vastav kandetüüp **Kulu** sisestatakse kasumiaruande kontole.
    
7. Laiendage kiirvahekaarti **Prognoos**. Sellel vahekaardil olevatel väljadel määratletakse fikseeritud hinnaga tulude kalkulatsiooni sätted. Selle vahekaardi väljad rakenduvad ainult projekti kulu ja tulu profiilidele koos arveldusmeetodiga **Fikseeritud hind**.
8. Valige kiirkaardi **Prognoos** järgmistel väljadel vastav teave.

    - **Projekti lõpuleviimise arvutustes kasutatavad põhimõtted**.

        - **Lõpetatud leping**: kulude ühtimist ja tulu kajastamist ei toimu enne projekti lõppu. Kulud kajastuvadsaldos kui WIP, kuni projekti lõpuleviimiseni.
        - **Lõpetatud protsent**: viittulu arvutatakse ja sisestatakse pearaamatusse igal perioodil vastavalt projekti lõpuleviimise protsendile. L'puleviimise protsedndi arvutamiseks on saadaval mitu võimalust. Need meetodid võivad olla konfiguratsiooni põhjal automaatsed või käsitsi.
        - **WIP puudub**: seda seadistust kasutatakse lühikese ajavahemikuga fikseeritud hindadega projektide jaoks ja kus arve ja kulud toimuvad samal perioodil. Antud juhul välja **Kontopõhine arveldamine** väärtus kiirkaardil **Pearaamat** määratakse automaatselt valikule **Kuluaruanne**, et tagada arveldamisel tulu äratundmine. Tulu prognoosimise protsessi ei kasutata selle projekti kasumiaaruande profiili jaoks.

    - **Ühtiv põhimõte**: see väli määratleb, kuidas arvutatud müügiväärtus (iittulu) pearaamatusse postitatakse.

        - Kasutades põhimõtet **Müügiväärtus**, arvutab süsteem müügiväärtuse vastendades kulude ja tuluga ning seejärel postitab selle ühe summana.
        - **Tootmise ja kasumi** põhimõtte kasutamisse jaotab süsteem müügiväärtuse realiseeritud kuludeks ja arvutatud kasumiks. Need sisestatakse eraldi.

    - **Kulumallid**: lubage projekti kannete rühmitamine vastavalt kandetüübile ja projekti kategooriale ning määratlege nende rühmade protsentuaalse lõpuleviimise arvutamise reeglid.
    - **Perioodi tähised**: määratlege konkreetse projekti kulu ja tuluprofiili tuluprognooside hinnangute arvutamise sagedus.
    - **Prognoosi kategooriad**: kasutatakse projekti tehingute postitamise mügiväärtuste (viittulu) postitamiseks. Esmalt konfigureerige tehingu tüübi **Tasuta** spetsiaalne projekti kategooria ja seejärel määrake lipp **Prognoos** selle projekti kategooria jaoks. Järgmisena valige sõltuvalt valitud ühtivast põhimõttest selle projekti kategooria projekti kulu- või tulu profiili väärtus **Müük** või väli **Kulu**.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Projekti kulu ja tulu profiilide näidiskonfiguratsioonid

Aeg ja materjalid – WIP puudub

![Kulu ja tulu profiil: aeg ja materjalid – WIP puudub](media/time-material-no-wip.png)

Aeg ja materjalid – WIP (tulu)

![Kulu ja tulu profiil: aeg ja materjalid – WIP](media/time-material-with-wip.png)

Fikseeritud hind – WIP puudub

![Kulu ja tulu profiil: fikseeritud hind – WIP puudub](media/fixed-price-no-wip.png)

Fikseeritud hind – lõpetatud leping

![Kulu ja tulu profiil: fikseeritud hind – lõpetatud leping](media/fixed-price-completed-contract.png)

Fikseeritud hind – protsentuaalne lõpuleviimine

![Kulu ja tulu profiil: fikseeritud hind – protsentuaalne lõpuleviimine](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Raamatupidamissündmuse näidised projekti kulu ja tulu profiilide näidise jaoks.

| Raamatupidamissündmus                  | Aeg ja materjal – WIP puudub                       | Aeg ja materjal – WIP                                                                                           | Fikseeritud hind – WIP puudub                                            | Fikseeritud hind – lõpetatud leping                                                                            | Fikseeritud hind – protsentuaalne lõpuleviimine                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Ajakannete töölehele kandmine    | Deebet – kulu <br>Krediit – palgaarvestuse jaotus          | Deebet – kulu <br>Krediit – palgaarvestuse jaotus <br>Deebet – WIP müügiväärtus <br>Krediit – viittulu müügiväärtus                | Deebet – kulu <br>Krediit – palgaarvestuse jaotus                         | Deebet – kulu <br>Krediit – palgaarvestuse jaotus                                                                    | Deebet – kulu <br>Krediit – palgaarvestuse jaotus                       |
| kulukannete töölehele kandmine | Deebet – kulu <br>Krediit – kulu tasaarvelduskonto | Deebet – kulu <br>Krediit – kulu tasaarvelduskonto <br>Deebet – WIP müügiväärtus <br>Krediit – viittulu müügiväärtus      | Deebet – kulu <br>Krediit – kulu tasaarvelduskonto                 | Deebet – kulu<br> Krediit – kulu tasaarvelduskonto                                                            | Deebet – kulu <br>Krediit – kulu tasaarvelduskonto               |
| Kliendile arve esitamine                | Deebet – kliendi bilanss <br>Krediit – arveldatud tulu | Deebet – kliendi bilanss <br>Krediit – arveldatud tulu <br>Krediit – WIP müügi väärtuse deebet – iittulu müügiväärtus | Deebet – kliendi bilanss <br>Krediit – arveldatud tulu – kontol | Deebet – kliendi bilanss <br>Krediit – WIP – arveldatud kontol                                                  | Deebet – kliendi bilanss <br>Krediit – WIP – arveldatud kontol    |
| Järeltulu hinnang             | Pole rakendatav                                   | Pole rakendatav                                                                                                    | Pole rakendatav                                                  | Deebet – WIP kulu väärtus <br>Krediit – kulu                                                                         | Deebet – WIP müügiväärtus <br>Krediit – viittulu müügiväärtus |
| Eemalda                         | Pole rakendatav                                   | Pole rakendatav                                                                                                    | Pole rakendatav                                                  | Kreedit – WIP kulu väärtus <br>Deebet – kulu <br>Krediit – viittulu – müügiväärtus <br>Deebet – WIP – arveldatud kontol | Deebet – WIP – arveldatud kontol <br>Kreedit – WIP müügiväärtus     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Projekti kulu ja tulu profiili reeglite konfigureerimine

Projekti kulu ja tulu profiili reeglid määratlevad projekti kulu ja tulu profiili, mida tuleb kasutada iga tasustatava projekti tehingute töötlemisel. Määratlege reeglid, avades **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Postitamine** \> **Projekti kulu ja tulu profiili reeglid**.

Reegleid saab määratleda projekti lepingu, projekti rühma või kindla projekti alusel. Süsteem valib alati suurima granulaarsusega reeli esimesena.


[!INCLUDE[footer-include](../includes/footer-banner.md)]