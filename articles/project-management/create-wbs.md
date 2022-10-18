---
title: Tööjaotuse struktuuri loomine
description: Selles artiklis selgitatakse, kuidas luua tööjaotuse struktuur (WBS), mis hõlmab uue plaanimisliidese põhijuhtelemente.
author: ruhercul
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 19d2dfeff39fd3c5edd5124c27134a9fe360e4d1
ms.sourcegitcommit: 8f4841387deea2998589b7365c3373585a16cb0e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/12/2022
ms.locfileid: "9655183"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Tööjaotuse struktuuri (WBS) loomine

Projekti ajakavas on andmed selle kohta, millist tööd on vaja teha, millised ressursid töö teevad ja aeg, mille jooksul töö tuleb ära teha. Ajakava kajastab kogu tööd, mis on seotud projekti õigeaegse valmimisega. Dynamics 365 Project Operationsis loote projekti ajakava tehes järgmist.

  - Töö jaotamine hallatavateks tööülesanneteks.
  - Iga tööülesande jaoks vajamineva aja hindamine.
  - Tööülesannete sõltuvuste määramine.
  - Tööülesannete kestuse määramine.
  - Tööülesande tegemiseks vajalike üldiste ressursside hindamine. 

Projekti ajakava luuakse lehe **Projekt** vahekaardil **Ajakava**.

## <a name="tasks"></a>Ülesanded

Esimese sammuna projekti ajakava loomisel on jagada töö hallatavateks osadeks. Project Operationsi ajakava toetab järgmisi funktsioone.

- Kokkuvõtvad ehk konteinerülesanded
- Lehesõlme ülesanded

### <a name="summary-tasks"></a>Koondülesanded

Koondülesanded võivad talletada teisi koondülesandeid või lehesõlme ülesandeid. Neil ei ole oma töömahtu ega kulusid. Selle asemel on nende töömaht ja maksumus konteinerite tööülesannete töömahu ja kulude koondamine. Kokkuvõtte tööülesande alguskuupäev on konteineri tööülesannete alguskuupäev ja lõppkuupäev on konteineri tööülesannete lõppkuupäev. Kokkuvõtva tööülesande nime saab redigeerida, kuid ajastamise atribuute, sh maht, kuupäevad ja kestus, ei saa redigeerida. Kokkuvõtva tööülesande kustutamisel kustutatakse ka kõik selle konteineri tööülesanded.

### <a name="leaf-node-tasks"></a>Lehesõlme ülesanded

Lehe ülesanne kajastab projekti kõige üksikasjalikumat tööd. Sellel on arvestuslik panus, ressursid, plaanitud algus- ja lõppkuupäevad ning kestus.

## <a name="create-a-task-hierarchy"></a>Ülesande hierarhia loomine

### <a name="add-a-task"></a>Ülesande lisamine

Ühe või mitme tööülesande lisamiseks tehke järgmist.

1. Avage **Projektid** ja valige ning avage selle projekti kirje, millele soovite ajakava luua. 
2. Valige vahekaart **Tööülesanded**. 
3. Valige **Lisa uus tööülesanne**, sisestage tööülesande nimi ja vajutage sisestusklahvi Enter.
2. Sisestage mõne muu tööülesande nimi ja vajutage uuesti sisestusklahvi Enter, kuni teil on täielik tööülesannete loend.

### <a name="manage-hierarchy-of-a-task"></a>Tööülesande hierarhia haldamine

Kui ülesanne on taandatud, saab sellest vahetult selle kohal oleva ülesande tütar. Ülesande ajakava ID arvutatakse seejärel ümber, nii et see põhineb selle uue peamise ajakava ID-l ja järgneb liigenduse nummerdamise skeemile. Peamine ülesanne on nüüd koondülesanne. Seetõttu muutub see oma tütarülesannete ümberarvestuseks. Kui tööülesanne on ülendatud, pole see enam selle peamise ülesande tütar. Seejärel arvutatakse ajakava ID ümber nii, et see peegeldaks tööülesande värskendatud sügavust ja positsiooni hierarhias. Eelmise peamise ülesande maht, kulu ja kuupäev arvutatakse ümber, nii et need ei sisalda seda toimingut.

Tööülesande taandamiseks või ülendamiseks tehke järgmist.

1. Valige lehel **Projekt** vahekaardil **Tööülesanded** jaotises **Koondülesanded** kolm vertikaalset punkti tööülesande nime kõrval ja seejärel valige **Muuda alamülesandeks**. 
2. Valige tööülesanne, mida soovite taandada või edendada. Mitme tööülesande valimiseks valige tööülesanne, vajutage ja hoidke all klahvi Ctrl ning valige siis täiendavad tööülesanded.
2. Tööülesannete koondülesannete alla või sealt välja liigutamiseks valige käsk **Taanda** või **Ülenda alamülesanne**.

### <a name="move-tasks-up-and-down"></a>Ülesannete üles ja alla liigutamine

Ülesandeid saab tööjaotuse struktuuri mis tahes tasemele teisaldada ühel kahest viisist:

- Valige üks või enam tööülesannet ning lohistage need soovitud asukohta.
- Valige üks või enam tööülesannet, tehke paremklõps ja valige **Lõika**, valige ajakavas sihtkoha lahter ja seejärel paremklõpsake ning valige **Kleebi**.

## <a name="task-attributes"></a>Ülesande atribuudid

Ülesande nimi kirjeldab tööd, mida on vaja teha. Project Operationsis kirjeldatavad ülesandega seostatud atribuudid ülesande ajakava ja töötajate vajadusi.

## <a name="schedule-attributes"></a>Atribuutide plaanimine

Atribuudid **Maht**, **Alguskuupäev**, **Lõppkuupäev** ja **Kestus** määravad ülesande ajakava.

Järgmises tabelis on toodud täiendavad ajakava atribuudid.

| **Lõplik kuvatav nimi** | **Lõplik kirjeldus** |
| --- | --- |
| Tehtud töö (tunnid) | Tööülesande jaoks lõpuleviidud töö tundides. |
| Kestus | Kuvab ülesande kestuse päevades. |
| Tööpanus kokku | Töölesande töömaht kokku tundides. |
| Lõpeta | Lõpukuupäev ja kellaaeg. |
| % lõpetatud | Tööülesande lõpuleviidud osa protsent. |
| Projektisalv | Ülesande töölauda saab rühmitada salve järgi, nii et igal salvel oleks oma veerg. |
| Tehaolev töö (tunnid) | Tööülesande tehaolevate tööde maht tundides. |
| Algusesse | Alguskuupäev ja kellaaeg. |
| Nimetus | Tööülesande nimi. |
| ID | Tööjaotuse struktuuris sisalduva ülesande ID. |

Administraatorina saate tööülesande olemis määratleda kohandatud välju. Kuid välju ei saa ajakava ruudustikus kuvada. Kohandatud väljade nägemiseks lisage need **Projekti ülesande** üksikasjade lehele.

## <a name="staffing-attributes"></a>Personaliatribuudid

Personaliatribuute saab kasutada ajakava välja **Ressursid** kaudu. Saate otsida olemasolevat ressurssi või valida käsu **Loo** ja siis lisada paneelil **Kiirloomine** uue ressursina projekti meeskonnaliikme.  Kui otsite ressurssi ressursivalija abil ülesannete ruudustikus, tahvlivaates või ganttis, tagastab otsing kas olemasolevad projektimeeskonna liikmed või aktiivsed broneeritavad ressursid.

Väljad **Roll**, **Ressursiühik** ja **Positsiooni nimi** on kasutusel ülesandega seotud vajaduste kirjeldamiseks. Neid personaliatribuute koos ülesannete ajakavaga kasutatakse selleks, et leida selle toimingu jaoks saadaolevaid ressursse.

   - **Roll**: määrake ülesande tegemiseks vajaliku ressursi tüüp.,
   - **Ressursiühik**: määrake ühik, millest ülesandega seotud ressursid tuleks määrata. See atribuut mõjutab ülesande maksumust ja müügihinda juhul, kui ressursi kulu ja arve määr seatakse vastavalt ressursiühikule.
   - **Positsiooni nimi**: sisestage üldisele ressursile sõbralik nimi, mis on selle ressursi kohatäiteks, mis lõppkokkuvõttes tööd tegema hakkab.

Väljal **Ressursid** on üldise ressursi või nimega ressursi positsiooni nimi, kui see on leitud.

Väljal **Kategooria** on väärtused, mis näitavad, et ülesannet saab rühmitada. See väli ei mõjuta ajakava ega personali. Selle asemel kasutatakse seda välja ainult aruandluses.

## <a name="task-dependencies"></a>Ülesande sõltuvused

Project Operationsi ajakava abil saate luua ülesannete vahel eelkäijate seoseid. Väli **Eelkäia** kasutab ühe või mitu väärtust, et näidata ülesandeid, millest ülesanne sõltub. Eelkäija väärtuse määramisel ülesandele saab ülesanne alata alles siis, kui eelkäijatest ülesanded on lõpetatud. Sõltuvuse tõttu lähtestatakse ülesande planeeritud alguskuupäev kuupäevani, mil eelkäija ülesanded on lõpule viidud.

Ülesande režiim ei mõjuta rakenduse eelkäija / sõltuvate ülesannete algus- ja lõppkuupäevale tehtud värskendusi.

## <a name="understanding-the-impacts-of-duration-resource-calendars-and-project-calendars-on-tasks"></a>Kestuse, ressursikalendrite ja projektikalendrite mõju mõistmine ülesannetele
Ülesande kestus on määratletud kui töötundide arv ülesande alguskuupäeva algusaja ja lõppkuupäeva lõpuaja vahel.   Veebiprojekt määratleb kestuse mõõtühikud järgmiselt:

| **Kestuse mõõtmine** | **Kogus**|
|----------------------------------------------------|----------------------|
| Tundi päevas | 8 |
| Tunnid nädalas |  40 |
| Päevad kuus |  20 |

Määramata ülesanded plaanitakse projekti kalendri abil. Kuid esmasel ressursimääramisel värskendatakse ülesande ajastamist nii, et see vastaks ressursi kalendrile. Ülesandega ülesande hilisemaid muudatusi reguleerib [projekti plaanimisrežiim](scheduling-modes.md). Lisateavet kalendrite mõju kohta ülesannetele leiate teemadest [Ressursikalendrid Projecti veebirakenduses](https://techcommunity.microsoft.com/t5/project-blog/resource-calendars-in-project-for-the-web/ba-p/3269686) ja Ülesannete algusajad ja [teie projektid!](https://techcommunity.microsoft.com/t5/project-blog/task-start-times-amp-your-projects/ba-p/3269665)


## <a name="accessibility-and-keyboard-shortcuts"></a>Hõlbustusfunktsioonid ja kiirklahvid

**Ajakava** ruudustik on täielikult juurdepääsetav ja seda saab kasutada ekraanilugeja, näiteks Narrator, JAWS või NVDA. Saate liikuda läbi ruudustiku ala nooleklahvide abil (nagu rakenduses Microsoft Excel), saate kasutada tabeldusklahvi, et interaktiivse kasutajaliidese elemente edasi arendada, ning võite kasutada allanoolt, sisestusklahvi või tühikut, et valida ja avada rippmenüüd.

## <a name="project-limitations"></a>Projekti piirangud 
Kui kasutate Project Operationsis tööjaotuse struktuuri, peaksite olema kursis järgmiste piirangutega. Need piirangud kehtivad projektidele ja ülesannetele. Lisateavet leiate teemast [Project for the web piirangud ja piirid](/project-for-the-web/project-for-the-web-limits-and-boundaries).

| **Väli**                                          |  **Piirang**           |
|----------------------------------------------------|----------------------|
| Projekti ülesannete maksimaalne koguarv                  | 500                  |
| Projekti maksimaalne kogukestus               | 3650 päeva (10 aastat) |
| Projekti ressursside maksimaalne koguarv              | 300                  |
| Projekti linkide maksimaalne koguarv (ainult järglane) | 600                  |
| Projekti kohandatud väljade maksimaalne koguarv          | 10                   |
| Kontroll-loendiüksuste maksimum ülesande kohta                   | 20                   |

**Ülesande piirangud**

| **Väli**                               |   **Piirang**           |
|-----------------------------------------|-----------------------|
| Maksimaalne hierarhiatase                 | 10 taset             |
| Maksimaalne linkide arv (eelkäija + järglane) | 20                    |
| Lehe ülesande maksimaalne kestus           | 1250 päeva             |
| Kokkuvõtva ülesande maksimaalne kestus      | 3650 päeva (10 aastat)  |
| Ülesandele määratud maksimaalne ressursside arv    | 20 ressurssi          |
| Ülesande toetatud kuupäevavahemik         | 1/1/2000–12/31/2149 |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
