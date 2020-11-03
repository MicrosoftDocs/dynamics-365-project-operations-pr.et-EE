---
title: Projekti kulu ja tulu prognooside määramine
description: Projekti kulu ja tulu prognooside määramine Project Service'is
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1652b39b6c8a703bf198a990eb9047eff9dc9f4c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074964"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Projekti kulu ja tulu prognooside määramine 

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projektiprognoosid annavad finantsülevaate prognoositavast ja plaanitud tööst projekti tööjaotuse struktuuris. Prognooside vaade annab teavet plaanitud töö kulude ja tulude mõju kohta. Hinnanguvaade annab tööriista teabe vaatamiseks mitmesuguste eelmääratletud dimensioonide kohta, et teavitada teid kõige paremini projekti finantsmõjust.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Projekti maksumus ja müügiväärtus  
Funktsiooni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] hinnakirjad määratlevad projektides kasutatavate rollide kulud ja arveldusmäärad. Projekti tööjaotuse struktuuri ülesannetega seotud rollide põhjal saate määrata kaasneva töö kulu ja tulu mõju.  
  
## <a name="cost-price-defaulting"></a>Omahinna vaikeväärtusele määramine  
Iga projekt kuulub organisatsioonile (näidatud projekti **omanikust üksuses** ). Omanikust organisatsiooniüksusega seotud hinnakiri määrab üksuse omahinna. Funktsioon [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] määrab rollide jaoks omahinnad, otsides rolli, ühiku ja organisatsiooniüksuse kombinatsiooni omahinna hinnakirjas, et saada prognoosi ridadel oleva kuupäeva seisuga õige omahind.  
  
Kui rolli, ühiku ja organisatsiooniüksuse kombinatsioon ei anna omanikust üksuse hinnakirjast omahinda, eiratakse ühikut, eelistades rolli ja organisatsiooniüksuse kombinatsiooni. Kui omahind on olemas, teisendatakse hing prognoosi real valitud ühikusse.  
  
Kui rolli ja organisatsiooniüksuse kombinatsioon ei anna omahinda, eelistatakse organisatsiooniüksusele rolli ja ühiku kombinatsiooni ja hind määratakse vaikesätteks pärast vajaduse korral teisendamist.  
  
 Kui rolli puhul hinda pole, määratakse omahinnaks prognoosi real vaikesäte 0,00.  
  
 Kõik projekti kuluprognoosi ridadel olevad kulusummad on omanikust organisatsiooniüksuse valuutas.  
  
## <a name="sales-price-defaulting"></a>Müügihinna vaikeväärtusele määramine  
Müügihinnakiri põhineb müügiüksusel, millega projekt on seotud. Hinnapakkumise või lepinguga seotud müügihinnakiri määrab üksuse müügihinna. Kui hinnapakkumisel või lepingul on kohandatud hinnakiri, on see projekti prognooside vaike-müügihinnakiri. Kui puudub seos müügiüksustega, on parameetrisätetes konfigureeritud vaike-müügihinnakiri projekti vaike-müügihinnakiri. Iga prognoosi reaga on seotud ressursi organisatsiooniüksus, mis tähistab seda organisatsiooniüksust, millest ressursid ülesande täitmiseks broneeritakse. Seotud rollide müügihind määratakse, otsides rolli, ühiku ja ressursi organisatsiooniüksuse kombinatsiooni müügihinnakirjas, et saada prognoosi ridadel oleva kuupäeva seisuga õige müügihind.  
  
Kui rolli, ühiku ja ressursi organisatsiooniüksuse kombinatsioon ei anna müügihinnakirjast müügihinda, eirab süsteem ühikut ja otsib rolli ning ressursi organisatsiooniüksuse kombinatsiooni. Kui müügihind leitakse, teisendatakse see müügiprognoosi real valitud ühikusse.  
  
Kui süsteem rolli hinda ei leia, peab müügihind olema prognoosi real vaikesäte 0,00.  
  
Prognooside vaatel on ruudustikuvaade, milles kuvatakse prognoosi ridade lame ruudustik, kus on ühik ning kogumaksumus ja müügihind.  
  
## <a name="time-phased-view-of-project-estimates"></a>Ajafaasidega ülevaade projekti prognoosidest  
Projekti prognooside ajafaasidega ülevaates liigendatakse ruudustikuvaate prognooside andmeid vaikimisi rolli järgi ja need kuvavad prognoosi andmed valitud ajaskaala ajajoonel.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Panuse prognoosi eraldamine ülesande režiimi põhjal  
Ajafaasidega vaates jaotatakse ülesande puhul prognoositav koondpanus, eraldades teatud arvu panusetunde ühiku ajaperioodi kohta valitud ajaskaalal. Project Service’is määrab ülesande režiim, kuidas panus ülesande kestusele eraldatakse. Kaks eraldamise tüüpi on ühtlane eraldamine ja töötundidel põhinev eraldamine  
  
## <a name="work-hours-based-allocation"></a>Töötundidel põhinev eraldamine  
Ülesanderežiimi automaatne plaanimine määrab, et ülesande jaoks prognoositud ressursside arvu kasutatakse eeldatavasti päevas kõigi töötundide vältel. See kehtib panuse eraldamisel, jagades selle samuti ajafaaside vaates ülesannete kestusega. Näiteks ajaskaalal Päev ei ületa päevale eraldatud panus ülesande puhul, mille eeldatavasti täidab üks ressurss, projektikalendris päeva kohta määratletud töötunde. Seega tagab panuse eraldamine alati, et ressursside kasutus määratakse terveks päevaks.  
  
## <a name="even-distribution"></a>Ühtlane jaotus  
Käsitsi plaanitud ülesande režiim ei arvesta töötunde, projektikalendrit ega ülesandele määratletud ressursside arvu. Ülesande ajakava põhineb kasutaja sisestusel. Selliste ülesannete puhul puuduvad panuse eraldamisel ühiku ajaperioodi kohta valitud ajaskaalal piiravad tegurid. Ülesande panus kokku jagatakse võrdselt ja eraldatakse valitud ajaskaalal iga ühiku ajavahemikule.  
  
Sel viisil määratleb ülesandes määratletud ülesande režiim panuse jaotuse või panuse eraldamise ühiku ajaperioodi kohta ajafaasidega prognoosides.  
  
## <a name="grouping-and-time-phasing-options"></a>Rühmitamise ja ajafaaside valikud  
See vaade aitab mõista panuse, kulude ja müügi prognooside jaotust päeva, nädala, kuu või aasta põhjal. Valik Rühmitusalus võimaldab prognooside andmete liigendamist kahes teises dimensioonis: kategooria ja ressurss. Nii ruudustikuvaates kui ka ajafaaside vaates saate valida kuvatavaid välju. Iga ajaploki koondväärtused kuvatakse all, näidates panuse prognoositavat kulu kokku. ja päeva, nädala, kuu või aasta müüki.  
  
Vaikeväärtustele seadmisel jõustuvad omahind ja müügihind teatud kuupäeval – kui rollide määrad muutuvad, on seda paremini näha ajafaaside vaates kui prognoositavate andmete kuvamisel liigendtabelis Ressurss ja nädalate kaupa ajafaasidesse jagatuna.  
  
## <a name="expense-estimates"></a>Kuluprognoosid  
Projektis tekkiv kulu, mis pole otseselt seotud tööjõukuluga, saab kajastada projekti prognoosides ruudustikuvaates. Valiku **Kuluprognoosi lisamine** abil ruudustikuvaates saate seda teha. Kuluprognoosid saab kajastada konkreetse ülesande või terve projekti kohta. Saate valida neil ridadel kulukategooriad ja valida esialgse kuupäeva, millal kulu peaks tekkima. Kui seotud kulul ja müügihinnakirjas on kulukategooriatele määratud vaikehinnad või hinnalisandi protsendid, lähtestatakse need seostamisel prognoosi real vaikeväärtustele.  
  
### <a name="see-also"></a>Vt ka  
 [Projektijuhi juhend](../psa/project-manager-guide.md)
