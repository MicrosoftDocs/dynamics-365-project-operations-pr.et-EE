---
title: Hinnapakkumised ja hinnapakkumise read
description: Selles teemas antakse teavet hinnapakkumiste ja hinnapakkumiste ridade kohta.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e5b0dfb3db2ddc6d43545a0f1f9429e343e830b5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291119"
---
# <a name="quotes-and-quote-lines"></a>Hinnapakkumised ja hinnapakkumise read

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Rakenduses Dynamics 365 Project Service Automation on kahte tüüpi hinnapakkumisi: projekti hinnapakkumised ja müügipakkumised. Kaks tüüpi erinevad järgmistel viisidel.

- Müügipakkumiste puhul on ainult üks ruudustik rea üksuste jaoks. Projekti hinnapakkumise puhul on kaks ruudustikku rea üksuste jaoks: üks projekti ridade ja teine toote ridade jaoks.
- Müügipakkumine toetab aktiveerimist ja läbivaatamisi. Projekti hinnapakkumine ei toeta neid protsesse.
- Müügipakkumistele saate lisada mitu tellimust. Projekti hinnapakkumisele saate lisada ainult ühe projekti lepingu.
- Võite võita müügipakkumise ja hoida seotud müügivõimaluse avatuna. Pärast projekti hinnapakkumise võitmist suletakse seotud müügivõimalus.
- Müügipakkumine ei sisalda mõningaid väljasid ja mõisteid, mis on kaasatud projekti hinnapakkumises. Väljad sisaldavad järgmisi: **Hankeüksus**, **Kontohaldur** ja **Maksja: kontakti nimi**.  
- Müügipakkumisi ja projekti hinnapakkumisi tuvastab ka suvandikomplekti põhine väli, mille nimi on **Tüüp**. Müügipakkumise puhul on sellel väljal väärtus **Kaubal põhinev**. Projekti hinnapakkumise puhul on sellel väärtus **Tööl põhinev**.

Selles teemas keskendutakse projekti hinnapakkumiste üksikasjadele.

Projekti hinnapakkumisel PSA-s võib olla mitu rea üksust või hinnapakkumise rida. Tegelikult on projekti hinnapakkumisel rea üksuste jaoks kaks ruudustikku. Üks ruudustik on projektil põhinevate ridade jaoks, mis võimaldavad üksikasjalikke hindamisi. Teine ruudustik on tootel põhinevate ridade jaoks, ms kasutavad lihtsat ühikuhinnal ja kogusel põhinevat lähenemisviisi.

- **Projektil põhinev** – summa (hinnapakkumise väärtus) määratakse pärast seda, kui hindate palju tööd on vaja teha. Saate hinnata tööd kõrgel tasemel või hinnata seda otse iga hinnapakkumise rea all olevate rea üksikasjadena. Lõpuks saate hinnata projekti ja projekti plaani abil tööd, mis põhineb algsetel hinnangutel. Projekti põhiste hinnapakkumiste ridu leidub ainult projekti põhistes hinnapakkumistes, mis on loodud rakendusega Project Service Automation. Seda tüüpi hinnapakkumise rida on kohandatud vorm sisestatavate hinnapakkumise ridade jaoks, mis on saadaval rakenduses Microsoft Dynamics 365 Sales.
- **Tootel põhinev** – summa (hinnapakkumise väärtus) määratakse müüdud ühikute koguse ja toote ühiku müügihinna põhjal. Toode tootel põhineval real võib olla pärit rakenduse Sales tootekataloogist või see võib olla teie määratletud toode. Seda tüüpi hinnapakkumise rida on saadaval ka projektil põhinevates hinnapakkumistes, mis on loodud rakendusega PSA.

Hinnapakkumise summa on tootel põhinevate ridade ja projektil põhinevate ridade kogusumma.

> [!NOTE]
> Rakenduses PSA ei nõuta hinnapakkumisi ega hinnapakkumise ridu. Projekti protsessi saab käivitada projekti lepinguga (müüdud projekt). Siiski on müügivõimalus alati nõutav, olenemata sellest, kas alustate hinnapakkumise või projekti lepinguga.

## <a name="project-based-quote-lines"></a>Projektil põhineva hinnapakkumise read

Projektil põhineval hinnapakkumise real rakenduses PSA on järgmised arveldusmeetodid.

- Aeg ja materjal
- Fikseeritud hind

### <a name="time-and-material"></a>Aeg ja materjal

Aja- ja materjalikulu arveldusmeetod põhineb tarbimisel. Selle arveldusmeetodi valimisel esitatakse kliendile arve projektiga kaasnevate kulude põhjal. Arveid luuakse kuupäeval põhineva perioodilise sagedusega. Müügiprotsessi jooksul annab aja- ja materjalikulu komponendi hinnapakkumise väärtus kliendile ainult hinnangulise lõppkulu. Hankija ei kohustu projekti lõpule viima täpselt hinnapakkumise väärtusega. Aja- ja materjalikulu komponendid suurendavad kliendi riski. Kliendid võiksid oma riski minimeerimiseks läbi rääkida täiendavad mitte ületamise klauslid. PSA ei toeta mitte ületamise klauslite seadistamist.

### <a name="fixed-price"></a>Fikseeritud hind

Fikseeritud hinnaga arveldusmeetodi korral kohustub hankija projekti kliendi jaoks kindlaksmääratud hinnaga tarnima. Kliendile arveldatakse fikseeritud hinnaga hinnapakkumise rea hinnapakkumise väärtus, olenemata kuludest, mis hankijale selle hinnapakkumise rea tarnimisega kaasnevad. Fikseeritud hinnaga hinnapakkumise rea väärtus on arveldatud ühel järgmistest viisidest. 

- Ühekordse summeeritud summana projekti alguses või lõpus või projekti vahekokkuvõtte saavutamisel. 
- Fikseeritud väärtuse võrdsete osamaksetena hinnapakkumise real kuupäevapõhise sagedusega. Need osamaksed on tuntud kui perioodilised vahekokkuvõtted.
- Osamaksetena, millel on rahaline väärtus, mis on joondatud töö edenemise või projektiga saavutatud konkreetsete vahekokkuvõtete järgi. Sellisel juhul võib iga osamakse väärtus erineda, kuid need kõik peavad fikseeritud väärtusega hinnapakkumise real sobima.

PSA toetab kõiki kolme tüüpi arve ajakavasid fikseeritud hinnaga hinnapakkumise ridade jaoks.

## <a name="transaction-classification"></a>Tehingu klassifikatsioon

Professionaalsed teenindusorganisatsioonid esitavad oma klientidele hinnapakkumisi ja arveid vastavalt kulude klassifikatsioonile. Rakenduses PSA on kulud esindatud järgmise tehingu klassifikatsiooniga.

- **Aeg** – see klassifikatsioon tähistab projekti tööjõu või inimressursi ajakulu.
- **Kulu** – see klassifikatsioon tähistab kõiki muid projekti kulusid. Kuna kulud võivad olla üldjoontes klassifitseeritud, on enamikul organisatsioonidel alamkategooriad (nt reisimine, autorent, hotell või kontoritarbed).
- **Tasu** – see klassifikatsioon tähistab mitmesuguseid üldkulusid, karistusi ja muid kaupu, mille eest on kliendile arve esitatud. 
- **Maksud** – see klassifikatsioon tähistab maksude summasid, mille kasutajad lisavad kulu sisestamisel.
- **Materjalikulu kanne** – see klassifikatsioon esindab kinnitatud projekti arvel olevate tootegruppide tegelikke ridu.
- **Vahekokkuvõte** – seda klassifikatsiooni kasutab rakenduses PSA fikseeritud hinnaga arveldusloogika.

Iga hinnapakkumise reaga saab seostada ühe või mitu neist tehingu klassifikatsioonidest. Pärast hinnapakkumise võitmist kantakse tehingu klassifikatsiooni ja hinnapakkumise rea vaheline vastendamine üle lepingu reale.
 
> ![Ekraanipilt tehingutüüpide vastendamisest hinnapakkumise ja lepingu ridadele](media/basic-guide-5.png)
  
Näiteks võib hinnapakkumine sisaldada kahte järgmist hinnapakkumise rida. 
- Nõustamistöö, mis kasutab aja- ja materjali arveldusmeetodit, kus rakendatakse aja- ja tasutehingute klassifikatsioone. Näiteks arveldatakse kõigi rakenduse **Dynamics AX Implementation** näidisprojekti aja- ja teenustasud kliendile vastavalt aja- ja materjalikulule. 
- Seotud reisikulud, mis kasutavad fikseeritud hinnaga arveldusmeetodit. Näiteks arveldatakse kõigi rakenduse **Dynamics AX Implementation** näidisprojekti reisikulude eest fikseeritud rahalise väärtusega.

> [!NOTE]
> Hinnapakkumise rea või lepingu reaga seotud projekti ja tehingu klassifikatsioonide **Aeg**, **Kulu** ja **Tasu** kombinatsioon peab olema kordumatu. Kui sama projekti ja tehingu klassi kombinatsioon on seotud rohkem kui ühe lepingu rea või hinnapakkumise reaga, ei tööta PSA õigesti.

## <a name="billing-types"></a>Arve tüübid

Väli **Arve tüüp** määratleb PSA-s arvelduse mõiste. See on suvandikomplekt, millel on järgmised võimalikud väärtused.

- **Arveldatav** – kulu, mis on kogunenud selle rolli või kategooriaga, on otsene kulu, mis juhib projekti täitmist ja selle töö eest maksab klient. Makset saab hallata nii ajalise kui ka materiaalse kulu põhjal või fikseeritud hinnaga kokkuleppena. Kuid selle aja kulutanud töötaja saab vastava krediidi oma arveldatava tulususe eest.
- **Mittearveldatav** – selle rolli/kategooria kogunenud kulusid peetakse otseseks kuluks, mis juhib projekti täitmist, isegi kui klient seda fakti ei tunnista ega selle töö eest maksa. Selle aja kulutanud töötaja ei saa vastavat krediiti arveldatava tulususe eest.
- **Tasuta** – selle rolli/kategooria kogunenud kulusid peetakse otseseks kuluks, mis juhib projekti täitmist, ja klient tunnistab seda fakti. Selle aja kulutanud töötaja saab vastavat krediiti arveldatava tulususe eest. Seda kulu kliendile ei esitata.
- **Pole saadaval** – selle valiku abil jälgitakse kulusid, mis tekivad siseprojektidega, mis ei vaja tulude jälgimist.

## <a name="invoice-schedule"></a>Arve ajakava

Arve ajakava on rida kuupäevi, mil projekti arveldamine toimub. Soovi korral saate luua ka rakenduses PSA hinnapakkumise real arve ajakava. Igal hinnapakkumise real võib olla oma arve ajakava. Arve ajakava loomiseks tuleb esitada järgmised atribuudi väärtused.

- Arveldamise alguskuupäev 
- Tarnekuupäev, mis tähistab projekti arveldamise lõppkuupäeva
- Arve sagedus

PSA kasutab neid kolme atribuudi väärtust, et luua esialgne kuupäevade kogum, et arveldamist saaks luua.

## <a name="invoice-frequency"></a>Arve sagedus

Arve sagedus on olem, mis talletab atribuutide väärtusi, mis aitavad väljendada arvete loomise sagedust. Arve sageduse olemit väljendavad või määratlevad järgmised atribuudid.

- **Periood** – toetatud on perioodid igakuine, kahe nädala järel ja iganädalane. 
- **Tsüklite arv perioodis** perioodide iganädalane ja kahe nädala järel jaoks saate määrata ainult ühe tsükli perioodi kohta. Perioodi igakuine jaoks saate määrata üks kuni neli tsüklit perioodi kohta. 
- **Päevi tsüklis** – päevad, millal arve esitamist tuleks teostada. Seda atribuuti saab konfigureerida kahel viisil.
  - **Nädalapäevad** – näiteks saate täpsustada, et arvete esitamine toimub igal esmaspäeval või igal teisel esmaspäeval. Kliendid, kes peavad arve esitamise määrama tööpäeval, võivad eelistada sellist konfiguratsiooni. 
  - **Kalendripäevad** – näiteks saate täpsustada, et arvete esitamine toimub iga kuu seitsmendal ja kahekümne esimesel päeval. Mõni organisatsioon võib eelistada sellist konfiguratsiooni, kuna see aitab tagada, et arvete esitamine töötaks fikseeritud ajakavaga iga kuu.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Fikseeritud hinnaga hinnapakkumise rea arve ajakava

Fikseeritud hinnaga hinnapakkumise rea puhul saate kasutada ruudustikku **Arve ajakava**, et luua arvete esitamise vahekokkuvõtted, mis võrduvad hinnapakkumise rea väärtusega.

- Võrdse jaotusega arvete esitamise vahekokkuvõtete loomiseks valige arve sagedus, sisestage hinnapakkumise rea arveldamise alguskuupäev ja valige hinnapakkumise päisest jaotisest **Kokkuvõte** suvand **Soovitud täitmise kuupäev**. Seejärel valige **Loo perioodilised vahekokkuvõtted**, et luua valitud arve sageduse põhjal võrdselt jaotatud vahekokkuvõtted. 
- Ühekordse summaga arvete esitamise etapi loomiseks looge vahekokkuvõte ja seejärel sisestage hinnapakkumise rea väärtus vahekokkuvõtte summana.
- Projekti plaanis konkreetsete ülesannete põhjal arvete esitamise vahekokkuvõtete loomiseks looge vahekokkuvõte ja vastendage see projekti ajakava elemendiga arvete esitamise verstaposti kasutajaliideses.


[!INCLUDE[footer-include](../includes/footer-banner.md)]