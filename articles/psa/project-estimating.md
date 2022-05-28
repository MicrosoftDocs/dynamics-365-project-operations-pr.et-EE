---
title: Projekti kulud ja tulud
description: Selles teemas antakse teavet projekti kulude ja tulude prognoosimise kohta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ecac3a08b2405e697eb260bbab991458dbe69f4e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581877"
---
# <a name="project-costs-and-revenue"></a>Projekti kulud ja tulud

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekti prognoosid annavad finantsülevaate töö kohta, mis on projekti ajakavas prognoositud ja plaanitud. Lehe **Projektid** vahekaardil **Prognoosid** kuvatakse teie poolt plaanitava töö kulude ja tulude mõju. Samuti pakub see teavet paljude eelmääratletud dimensioonide kohta. 

> ![Vahekaart Prognoosid.](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Projekti omahind ja müügiväärtused

Hinnakirjad määravad projektides kasutatavate rollide kulu- ja arveldusmäärad. Töö kulude ja tulude mõju saate määratleda, võttes aluseks positsiooni nimega seotud rollid ning ülesande jaoks määratud nimega ressursi. Kui teil on ülesandeid, millel pole ühtegi määramist (üldiseid või nimega), ei saa te kuluhinnanguid ega müügiprognoose hankida. Omahind ja müügiväärtused arvestavad hinnakirjas määratletud kuupäeva.

### <a name="default-cost-price"></a>Vaikimisi omahind  

Iga projekt kuulub organisatsioonile. See organisatsioon kuvatakse projekti väljal **Lepingut sõlmiv üksus**. Lepingut sõlmiva üksusega seotud hinnakirja kasutatakse üksuse omahinna määramiseks. Prognoosiridadel määratud kuupäeva jaoks rollidele õigete omahindade määramiseks otsige kulude hinnakirjast rolli, ühiku ja organisatsiooniüksuse kombinatsiooni. 

Selleks et saaks arvutada nende omahinna, tuleb kõik ülesanded määrata ressursile. Kõigi määramata ülesannete omahinnaks on 0,00.

Kui rolli, ühiku ja organisatsiooniüksuse kombinatsioon ei tagasta lepingut sõlmiva üksuse hinnakirjast omahinda, ignoreerib süsteem ühikut. Selle asemel otsib see ainult rolli ja organisatsiooniüksuse kombinatsiooni. Omahinna leidmisel kasutatakse teisendamise tegureid, et teisendada see selleks ühikuks, mille valisite prognoosireal.

Kui rolli ja organisatsiooniüksuse kombinatsioon ei tagasta omahinda, ignoreerib süsteem organisatsiooniüksust. Selle asemel otsib see rolli ja ühiku kombinatsiooni, et määrata vaikehind (pärast mis tahes teisenduse rakendamist).

Kui süsteem rolli hinda ei leia, määratakse prognoosireal olev omahind vaikeväärtusele **0,00**. Kõik projekti kuluhinnangu ridadel olevad kulusummad talletatakse lepingut sõlmiva üksuse valuutas.

> [!NOTE]
> Vaikimisi talletab Microsoft Dynamics 365 kulusummad teie põhivaluutas. Kuid vahekaardil **Prognoosid** kuvatavad kulusummad on lepingut sõlmiva üksuse valuutas.  

### <a name="default-sales-price"></a>Vaikimisi müügihind 

Müügi hinnakirja määrab kas see müügiolem, millega projekt on seotud, või projekti klient. Kui müügiolem (nt müügivõimalus, hinnapakkumine või leping) on projektiga seotud, määrab müügiolemi müügihinna see hinnakiri, mis on seotud hinnapakkumise või lepinguga. Kui hinnapakkumisel või lepingul on kohandatud hinnakiri, kasutatakse projekti prognooside vaikimisi müügihinnakirjana seda hinnakirja. Kui müügiolemitega seosed puuduvad, kasutatakse projekti vaikimisi müügihinnakirjana parameetrite vaikimisi müügihinnakirja, mis ühtib projektis määratletud kliendi valuutaga.

Igal prognoosireal on sellega seotud ressursiühik. Ressursiühik viitab organisatsiooniüksusele, millest ressursse ülesande lõpule viimiseks broneeritakse. Seotud rollide müügihinna määramiseks otsige müügihinnakirjast rolli, ühiku ja ressursiühiku kombinatsiooni. Kui ülesandele määramised puuduvad, on ülesande müügihind 0,00.

Kui rolli, ühiku ja ressursiühiku kombinatsioon ei tagasta müügihinnakirjast müügihinda, ignoreerib süsteem ühikut. Selle asemel otsib see ainult rolli ja ressursiühiku kombinatsiooni. Müügihinna leidmisel kasutatakse teisendamise tegureid, et teisendada see selleks ühikuks, mille valisite müügiprognoosi real. 

Kui rolli ja ressursiühiku kombinatsioon ei tagasta müügihinnakirjast müügihinda, ignoreerib süsteem ressursiühikut. Selle asemel otsib see rolli ja ühiku kombinatsiooni, et määrata vaikehind (pärast mis tahes teisenduse rakendamist).

Kui süsteem rolli hinda ei leia, määratakse prognoosireal olev müügihind vaikeväärtusele **0,00**.

Vahekaardil **Prognoosid** on ruudustiku vaade, mis kuvab prognoosiread. Ruudustikus on veerud ühik, omahind kokku ja müügihind kokku, nagu on toodud alljärgneval joonisel. 

> ![Vahekaardi Prognoosid ruudustiku vaade.](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Ajafaasidega ülevaade projekti prognoosidest

Projekti prognooside ajafaasi vaade kuvab ruudustiku vaatest prognoosi andmed ajaskaala üleselt, teie valitud ajateljel. Vaikimisi liigendatakse prognoosi andmed dimensioonis **Roll**.

> ![Projekti prognooside ajafaasi vaade.](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Prognoositud panuse jaotamine ülesande režiimi põhjal

Ajafaasi vaates jaotate ülesandele prognoositava kogupanuse, eraldades panuse tunnid valitud ajateljel ühiku ajaperioodi kohta. Ülesande režiim määrab, kuidas panus jaotatakse ülesande kestuse üleselt. Kaks eraldamise tüüpi on **Ühtlane** ja **Töötundidel põhinev**.

### <a name="work-hours-based-allocation"></a>Töötundidel põhinev eraldamine
 
Ülesande režiimi automaatses plaanimises määratakse ülesande ressursside päevased vaiketunnid täistöötundide määra kohaselt. See käitumine kehtib juhul, kui panus eraldatakse nii, et see jagatakse ajafaasi vaates ülesande kestuse üleselt. Näiteks, kui hindate, et ülesanne viiakse lõpule ajateljel **Päev** ühe ressursi poolt, ei ületa päevale eraldatud panus päeva töötunde, mis on määratud projekti kalendris. Seega tagab panuse eraldamine alati, et ressursse kasutatakse hinnanguliselt terve päev.

### <a name="even-allocation"></a>Ühtlane eraldamine

Käsitsi plaanitud ülesande režiimis projektikalendri töötunde ei kasutata. Selle asemel põhineb ülesande ajakava kasutaja panusel. Selliste ülesannete puhul puuduvad piiravad tegurid panuse eraldamisel ühiku ajaperioodi kohta valitud ajateljel. Ülesande kogupanus jaotatakse võrdselt ja eraldatakse valitud ajateljel igale ühiku ajaperioodile. Sel viisil määrab panuse jaotuse ülesandes määratletud ülesande režiim või panuse eraldamine ühiku ajaperioodi kohta ajafaasiga prognoosides.

## <a name="grouping-and-time-phasing-options"></a>Rühmitamise ja ajafaaside valikud

Ajafaasi vaade kuvab panuse, kuluhinnangute ja müügiprognooside jaotuse iga päeva, nädala, kuu või aasta põhjal. Vaikimisi liigendatakse prognoosi andmed dimensioonis **Roll**. Kuid te saate ka kasutada suvandit **Rühmitusalus**, et liigendada kahes teises dimensioonis: **Kategooria** ja **Ressurss**.

Nii ruudustiku vaates kui ka ajafaasi vaates saate valida, milliseid välju kuvatakse. Iga ajaploki kokkuvõtted kuvatakse projekti allservas. Need kuvavad päeva, nädala, kuu või aasta prognoositava kogupanuse, kulud ja müügid. Vaikimisi kasutatav omahind ja müügihind on kuupäeva-efektiivsed. Teisisõnu muutuvad need iga ressursi puhul vastavalt teie valitud ajafaasi vaatele.

## <a name="expense-estimates"></a>Kuluprognoosid

Ruudustiku vaate nupp **Lisa uus kuluprognoos** võimaldab teil talletada kõik projektiga kaasnevad, kuid mitte otseselt tööga seotud kulud. Saate talletada kuluprognoosid konkreetse ülesande või kogu projekti jaoks. Valige kulukategooriad ja esialgne kuupäev, mil kulu esineda võib. Kui seotud kulude hinnakirjas ja müügihinnakirjas on vaikehinnad (või kui hinnalisandi protsendid on kulukategooriate jaoks määratletud), sisetatakse need seostamise toimumisel prognoosireale automaatselt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
