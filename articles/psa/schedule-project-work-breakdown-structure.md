---
title: Tööjaotuse struktuuriga projekti ajastamine
description: Tööjaotuse struktuuriga projekti plaanimine Project Service'is
author: ruhercul
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
ms.openlocfilehash: 896f19746bde1ba6cf2acd6d558137f4271a5cd99424043053eefe128d3b4250
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996791"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Tööjaotuse struktuuriga projekti plaanimine (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projekti ajakavas on andmed selle kohta, millist tööd on vaja teha, millised ressursid töö teevad ja ajapiirid, milles töö tuleb ära teha. Projekti ajakava kajastab kogu tööd, mis on seotud projekti õigeaegse valmimisega. Üks esimesi toiminguid projekti algatamise faasis on koostada projekti ajakava. Projekti ajakava loomiseks peate koostama tööjaotuse struktuuri.  
  
 Koostage tööjaotuse struktuuriga projekti struktuur, mis aitab teha järgmist.  
  
- Jagada tööd hallatavateks ülesanneteks  
  
- Hinnata ülesande täitmiseks vajalikku aega  
  
- Määrata ülesande sõltuvusi ja kestust  
  
- Määrata iga ülesande täitmiseks vajalikke rolle  
  
  Projekti ajakava tööjaotuse struktuuris näeb tuttav välja ning sellel on interaktiivne Gantti diagramm.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Projektile tööjaotuse struktuuri loomine  
 Saate luua tööjaotuse struktuuri, mis kajastab projekti ülesannete järjekorda. Tööjaotuse struktuur sisaldab ülesandeid, iga ülesande nõudmisi ja tulu ning kulu andmeid. Tööjaotuse struktuuri saate lisada järgmisi väärtusi.  
  
-   Ülesannete järjestus hierarhias  
  
-   Muud ülesanded (kui on), mis tuleb enne ülesande alustamist täita  
  
-   Ülesande alguskuupäev, lõppkuupäev ja kestus  
  
-   Ülesande jaoks vajalik tundide arv  
  
-   Vajalikud töötaja oskused ja haridus  
  
-   Töötajad, kes on tööülesandele määratud  
  
-   Eeldatav tulu ja kulud  
  
## <a name="task-types"></a>Ülesannete tüübid  
Tööjaotuse struktuuri koostamisel kasutatakse järgmisi ülesannete tüüpe.  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Projekti juursõlm** | Projekti ülataseme kokkuvõtteülesanne. Kõik muud projekti ülesanded luuakse selle alla. Juurülesande nimi on projekti nimi. Juursõlme panus, kuupäevad ja kestus põhinevad selle all oleva hierarhia väärtustel. Juursõlme atribuute saab muuta või juursõlme saab kustutada. | 
| **Kokkuvõtvad ehk konteinerülesanded** | Kokkuvõttev ülesanne on alamülesannetega ülesanne. Kokkuvõtval ülesandel pole oma tööpanust ega maksumust. Selle tööpanus ja maksumus koosneb alamülesannete koondväärtusest. Kokkuvõtva ülesande nime saab muuta, kuid panust, kuupäevi ega kestust ei saa muuta, kuna need arvutatakse automaatselt. Kokkuvõtva ülesande kustutamisel kustutatakse ülesanne ja kõik selle alamülesanded.|  
| **Lehesõlme ülesanded** | Lehesõlme ülesanne kajastab projekti kõige üksikasjalikumat tööd. Sellel on arvestuslik panus, plaanitud hulk ressursse, plaanitud algus- ja lõppkuupäevad ning kestus.|

  
## <a name="task-hierarchy"></a>Ülesannete hierarhia  
 Ülesannete hierarhia loomisel on teil järgmised võimalused.  
  
- **Ülesande lisamine**.   Saate lisada ülesande ülesannete hierarhias valitud kohta. Kui te kohta ei vali, kuvatakse teie uus ülesanne lõpus.  
  
- **Ülesande taandamine**.   Saate ülesande taandada, muutes selle otse ülesande kohal oleva ülesande alamülesandeks.  
  
- **Ülesande eendamine**   Saate ülesande eendada, et see poleks enam algse põhiülesande alamülesanne.  
  
- **Nihuta üles ja Nihuta alla**.   Saate nihutada ülesandeid peamise ülesande hierarhias üles ja alla. Ülesande üles või alla nihutamisel puudub mõju selle panusele, maksumusele, kuupäevadele või kestusele.  
  
## <a name="task-attributes"></a>Ülesande atribuudid  
 Ülesande nimi kirjeldab tööd, mida on vaja teha. Mitmesuguste ülesande atribuutide abil saab kirjeldada ülesande ajakava ja personalinõudeid.  
  
### <a name="schedule-attributes"></a>Atribuutide plaanimine

 - Saate määrata väärtusi valikutele **Panuse tunnid**, **Ressursside arv**, **Alguskuupäev**, **Lõppkuupäev** ja **Kestus** ülesande ajakava määratlemiseks. 
 - **Panus** on ülesande lõpuleviimiseks eeldatavalt kuluv tundide arv.
 - **Ressursside arv** on hinnanguline väärtus, mille projektijuht ülesandele lisab, et saada parim võimalik ajakava. 
 - **Kestus** (päevades) näitab ülesande täitmiseks vajalikku tööpäevade arvu.  
  
### <a name="staffing-attributes"></a>Personaliatribuudid

 - **Roll**, **Ressursi organisatsiooniüksus**, **Ressursside arv** ja **Ressursid** kirjeldavad ülesande personalivajadusi. 
 - **Roll** kirjeldab ülesande sooritamiseks vajalikku ressursi tüüpi. 
 - **Ressursi organisatsiooniüksus** tähistab organisatsiooniüksust, millest selle ülesande jaoks ressursid tuleks võtta; see mõjutab ka ülesande eeldatavat maksumust ja müügihinda, kuna seda arvestatakse ühiku müügihinna määramisel ressursile. 
 - **Ressursid** sisaldavad üldist ressurssi või nimelist ressurssi, kui see leitakse.  
  
## <a name="task-dependencies"></a>Ülesande sõltuvused  
 Saate luua eelkäija seoseid tööjaotuse struktuuri ülesannete vahel. Saate määrata ülesannete eelkäija väljale vähemalt ühe väärtuse, et näidata ülesandeid, millest see sõltub. Eelkäija väärtuse määramisel ülesandele saab ülesanne alata alles siis, kui eelkäijatest ülesanded on lõpetatud. Selle sõltuvuse määramisel ülesandele arvutatakse ülesande plaanitav alguskuupäev ümber kõigi selle eelkäijate hiliseimaks lõppkuupäevaks. Eelkäijaga seotud mõju ajakavale pole ülesandele määratletud ajakavarežiimiga piiratud.  
  
## <a name="task-mode"></a>Ülesande režiim  
 Ülesande režiim on üks olulistest teguritest, mis määravad ajakava lehesõlme ülesanded. Igal ülesandel on kaks režiimi: automaatne plaanimisrežiim ja käsitsi plaanimisrežiim.  
  
-   **Automaatne plaanimine**.   Kui määrate ülesande režiimiks automaatse plaanimise, kasutab ülesande plaanimismootor plaanimisreegleid järgmistel ülesande atribuutidel ülesande ajakava määratlemiseks.  
  
    -   Eelkäijad  
  
    -   Panus  
  
    -   Ressursside arv  
  
    -   algus- ja lõppkuupäevad;  
  
-   **Plaanimise reeglid**.   Eelkäijateta lehesõlme ülesande alguskuupäev on vaikimisi projekti ajakava alguskuupäev. Lehesõlme ülesande kestuseks arvutatakse alati algus- ja lõppkuupäeva vaheline päevade arv. Kui ülesanne on automaatselt ajastatud, järgib plaanimismootor järgmisi reegleid.  
  
    -   Ülesande algus- ja lõppkuupäev peavad alati olema projekti plaanimiskalendrile vastavad tööpäevad  
  
    -   Eelkäijatega ülesande alguskuupäev on vaikimisi selle eelkäijate hiliseim lõppkuupäev  
  
    -   Panus = inimeste arv * kestus * projektikalendri standardtööpäeva tundide arv  
  
-   **Käsitsi plaanimine**.   Mõnikord võib olla vaja neist reeglitest erinevalt tegutseda. Sellisel juhul saate määrata ülesande režiimi käsitsi plaanimise. Sellega lõpetab plaanimismootor teiste plaanimisatribuutide väärtuste arvutamise. Ülesannete eelkäijate seadistamine mõjutab alati sõltuva ülesande alguskuupäeva.  
  
## <a name="create-a-work-breakdown-structure"></a>Tööjaotuse struktuuri loomine  
  
1.  Minge jaotisse **Project Service > Projektid**.  
  
2.  Klõpsake projekti, millega soovite töötada.  
  
3.  Valige kuva ülaosas asuvalt ribalt projekti nime kõrval olev allanool ja seejärel klõpsake valikut Tööjaotuse struktuur.  
  
4.  Ülesande lisamiseks klõpsake käsku **Lisa ülesanne**. Täitke ülesande väljad ja klõpsake siis käsku **Salvesta**.  
  
5.  Jätkake ülesannete lisamist, kuni tööjaotuse struktuur on valmis. Tööjaotuse struktuuri loomisel saate ülesannete korraldamiseks teha järgmist.  
  
    -   Valige ülesanne ja klõpsake käsku **Taanda**, et nihutada see teise ülesande alla, või käsku Eenda, et nihutada see taseme võrra üles.  
  
    -   Valige ülesanne ja klõpsake käsku **Nihuta üles** või **Nihuta alla**, et nihutada seda loendis üles või alla.  
  
    -   Gantti diagrammi peitmiseks klõpsake valikut **Peida Gantt**, selle uuesti kuvamiseks klõpsake valikut **Kuva Gantt**.  
  
    -   Saate valida Gantti diagrammi jaoks muu ajavahemiku jaotises **Ajaskaala**.  
  
6.  Tööjaotuse struktuuris määratud rollide lisamiseks projekti meeskonnaliikmetele klõpsake käsku **Loo projektimeeskond**.  
  
7.  Kui olete muudatuste tegemise lõpetanud, klõpsake kuva paremas alanurgas käsku **Salvesta**.  
  
### <a name="see-also"></a>Vt ka  
 [Projektijuhi juhend](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]