---
title: Projekti ajakavad
description: Selles teemas kirjeldatakse ajakava loomist.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 9a6b27050a19d8a7f2ed35f74b42bb4f371ad069
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074991"
---
# <a name="project-schedules"></a>Projekti ajakavad 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekti ajakavas on andmed selle kohta, millist tööd on vaja teha, millised ressursid töö teevad ja aeg, mille jooksul töö tuleb ära teha. Projekti ajakava kajastab kogu tööd, mis on seotud projekti õigeaegse valmimisega. Rakenduses Dynamics 365 Project Service Automation saate luua projekti ajakava, jagades töö hallatavateks ülesanneteks, hinnates iga ülesande sooritamiseks kuluvat aega, määrates ülesande sõltuvused, seadistades tööülesande kestuse ja hinnates üldisi ressursse, mis ülesandeid teevad. Projekti ajakava luuakse projekti lehe vahekaardil **Ajakava.**
 
## <a name="tasks"></a>Tööülesanded

Esimese sammuna projekti ajakava loomisel on jagada töö hallatavateks osadeks. PSA ajakava toetab järgmisi funktsioone.

- Projekti juursõlm
- Kokkuvõtvad ehk konteinerülesanded
- Lehesõlme ülesanded

### <a name="project-root-node"></a>Projekti juursõlm

Projekti juursõlm on projekti ülataseme kokkuvõtte tööülesanne. Kõik muud projekti ülesanded luuakse selle alla. Juursõlme nimi on alati projekti nimele määratud. Juursõlme panus, kuupäevad ja kestus põhinevad selle all oleva hierarhia väärtustel. Juursõlme atribuute ei saa redigeerida. Juursõlme ei saa ka kustutada.

### <a name="summary-or-container-tasks"></a>Kokkuvõtvad ehk konteinerülesanded 

Kokkuvõtlikel tööülesannetel on allüksused või konteineri tööülesanded. Neil ei ole oma töömahtu ega kulusid. Selle asemel on nende töömaht ja maksumus konteinerite tööülesannete töömahu ja kulude koondamine. Kokkuvõtte tööülesande alguskuupäev on konteineri tööülesannete alguskuupäev ja lõppkuupäev on konteineri tööülesannete lõppkuupäev. Kokkuvõtva tööülesande nime saab redigeerida, kuid ajastamise atribuute (maht, kuupäevad ja kestus) ei saa redigeerida. Kokkuvõtva tööülesande kustutamisel kustutatakse ka kõik selle konteineri tööülesanded.

### <a name="leaf-node-tasks"></a>Lehesõlme ülesanded

Lehe ülesanne kajastab projekti kõige üksikasjalikumat tööd. Sellel on arvestuslik panus, ressursid, plaanitud algus- ja lõppkuupäevad ning kestus.
 
## <a name="creating-a-task-hierarchy"></a>Ülesande hierarhia loomine

Ülesannete hierarhia loomisel on teil järgmised võimalused.

- Nupp **Lisa ülesanne**
- Nupp **Taandeülesanne**
- Nupp **Väljaulatuv ülesanne**
- Nupud **Nihuta üles** ja **Nihuta alla**
- Hõlbustusfunktsioonid ja kiirklahvid

### <a name="add-task"></a>Ülesande lisamine

Nupp **Lisa ülesanne** võimaldab luua hierarhias uue ülesande. Kui te kohta ei vali, sisestatakse teie uus ülesanne lõppu. 

Igale ülesandele määratakse ajakava ID. Ajakava ID tähistab ülesande sügavust ja positsiooni hierarhias. See kasutab liigendatud nummerdust. Esimesel tasemel projekti juursõlmes olevate ülesannete jaoks kasutatakse numeratsiooniskeemi 1, 2, 3 ja nii edasi. Esimese taseme ülesannete jaoks kasutatakse numeratsiooniskeemi 1.1, 1.2, 1.3 ja nii edasi.

### <a name="indent-task"></a>Taandeülesanne

Kui ülesanne on taandatud, saab sellest vahetult selle kohal oleva ülesande tütar. Ülesande ajakava ID arvutatakse seejärel ümber, nii et see põhineb selle uue peamise ajakava ID-l ja järgneb liigenduse nummerdamise skeemile. Peamine ülesanne on nüüd kokkuvõtlik tööülesanne või konteineri tööülesanne. Seetõttu muutub see oma tütarülesannete ümberarvestuseks.

### <a name="outdent-task"></a>Väljaulatuv ülesanne 

Kui tööülesanne on eemaldatud, pole see enam selle peamise ülesande tütar. Seejärel arvutatakse ajakava ID ümber nii, et see peegeldaks tööülesande värskendatud sügavust ja positsiooni hierarhias. Eelmise peamise ülesande maht, kulu ja kuupäev arvutatakse ümber, nii et need ei sisalda seda toimingut.

### <a name="move-up-and-move-down"></a>Nihuta üles ja Nihuta alla 

Nupud **Nihuta üles** ja **Nihuta alla** muudavad ülesande paigutust peamises hierarhias. Seda tüüpi muudatused ei mõjuta ülesande mahtu, kulusid, kuupäevi ega kestust. Mõjutatud on ainult ülesande ajakava ID. Seejärel arvutatakse ajakava ID ümber nii, et see peegeldaks tööülesande värskendatud sügavust ja positsiooni hierarhias.

### <a name="accessibility-and-keyboard-shortcuts"></a>Hõlbustusfunktsioonid ja kiirklahvid

**Ajakava** ruudustik on täielikult juurdepääsetav ja seda saab kasutada ekraanilugeja, näiteks Narrator, JAWS või NVDA. Saate liikuda läbi ruudustiku ala nooleklahvide abil (nagu rakenduses Microsoft Excel), saate kasutada tabeldusklahvi, et interaktiivse kasutajaliidese elemente edasi arendada, ning võite kasutada allanoolt, sisestusklahvi või tühikut, et valida rippmenüü ja seda käivitada. Ka veerupäised on interaktiivsed. Veergude peitmiseks ja kuvamiseks saate veeru päistes kasutada tabeldusklahvi ja nooleklahve ning kasutada tööriistaribal nuppu tegevus. Lisaks saate kasutada järgmisi kiirklahve.

- **Värskenda** : ALT + SHIFT + F5
- **Lisa** : ALT + SHIFT + Insert
- **Kustuta** : ALT + SHIFT + Delete
- **Nihuta üles/alla** : ALT + SHIFT + ülesnool/allanool
- **Taane/väljaulatuv** : ALT_SHIFT + vasak/parem nool
- **Laienda/ahenda hierarhiad** : ALT + SHIFT + pluss-/miinusklahvid

## <a name="task-attributes"></a>Ülesande atribuudid

Ülesande nimi kirjeldab tööd, mida on vaja teha. PSA puhul kirjeldatakse ülesandega seostatud atribuute ülesande ajakava ja töötajate vajadusi.

> ![Ülesande atribuudid](media/project-2.png)
 
### <a name="schedule-attributes"></a>Atribuutide plaanimine

Atribuudid **Maht** , **Alguskuupäev** , **Lõppkuupäev** ja **Kestus** määravad ülesande ajakava.

Täiendavad ajakava atribuudid on järgmised.

- **Panuse tunnid** : sisestage ülesande lõpuleviimiseks vajalike tundide kalkulatsioon. 
- **Kestus** : määrake ülesande lõpuleviimiseks vajalike tööpäevade arv.
- **Ajakava ID** : seda automaatselt genereeritud ID-d kasutatakse ülesannete tellimiseks hierarhias. Ülesannetevahelised sõltuvused haldavad tegelikku tööjärjestust.
 
### <a name="staffing-attributes"></a>Personaliatribuudid

Personaliatribuute saab kasutada ajakava välja **Ressursid** kaudu. Saate otsida olemasolevat ressurssi või klõpsata käsku **Loo** ja siis paneelil **Kiirloomine** lisada uue ressursina projekti meeskonnaliikme.

Väljad **Roll** , **Ressursiühik** ja **Positsiooni nimi** on kasutusel ülesandega seotud vajaduste kirjeldamiseks. Neid personaliatribuute koos ülesannete ajakavaga kasutatakse selleks, et leida selle toimingu jaoks saadaolevaid ressursse.

**Roll** – määrake, millist tüüpi ressurssi toimingu jaoks vaja on.

**Ressursiühik** – määrake ühik, millest ülesandega seotud ressursid tuleks määrata. See atribuut mõjutab ülesande maksumust ja müügihinda juhul, kui ressursi kulu ja arve määr seatakse vastavalt ressursiühikule.

**Positsiooni nimi** – sisestage üldisele ressursile sõbralik nimi, mis on selle ressursi kohatäiteks, mis lõppkokkuvõttes tööd tegema hakkab.

Väljal **Ressursid** on üldise ressursi või nimega ressursi positsiooni nimi, kui see on leitud.

Väljal **Kategooria** on väärtused, mis näitavad, et ülesannet saab rühmitada. See väli ei mõjuta ajakava ega personali. Seda kasutatakse ainult aruandluseks.

### <a name="task-dependencies"></a>Ülesande sõltuvused 

Rakenduse PSA ajakava abil saate luua ülesannete vahel eelkäijate seoseid. **Eelkäija** väli jaotises **Ülesanded** võtab ühe või mitu väärtust, et näidata ülesandeid, millest ülesanne sõltub. Eelkäija väärtuse määramisel ülesandele saab ülesanne alata alles siis, kui eelkäijatest ülesanded on lõpetatud. Sõltuvuse tõttu lähtestatakse ülesande planeeritud alguskuupäev kuupäevani, mil eelkäija ülesanded on lõpule viidud.

Ülesande režiim ei mõjuta rakenduse eelkäija / sõltuvate ülesannete algus- ja lõppkuupäevale tehtud värskendusi.

## <a name="task-mode"></a>Ülesande režiim 

Ülesande režiim määratleb lehtede sõlmpunktide ajastamise kavandamise. Igal ülesandel on kaks režiimi: automaatne plaanimisrežiim ja käsitsi plaanimisrežiim.

### <a name="auto-scheduling"></a>Automaatne plaanimine 
 
Kui määrate ülesande režiimiks **Automaatne plaanimine** , kasutab ülesande plaanimismootor plaanimisreegleid järgmistel ülesande atribuutidel ülesande ajakava määratlemiseks.

#### <a name="scheduling-rules"></a>Plaanimise reeglid

Eelkäijateta lehesõlme ülesande alguskuupäev on vaikimisi projekti ajakava alguskuupäev. Lehesõlme ülesande kestuseks arvutatakse alati algus- ja lõppkuupäeva vaheline päevade arv. Kui ülesanne on automaatselt ajastatud, järgib plaanimismootor järgmisi reegleid.

- Ülesande algus- ja lõppkuupäev peavad alati olema projekti plaanimiskalendrile vastavad tööpäevad. 
- Eelkäijatega ülesande alguskuupäev on vaikimisi selle eelkäijate hiliseim lõppkuupäev.
- Maht arvutatakse selle valemi abil: inimeste arv × kestus × tunnid projekti kalendris standardses tööpäevas.

### <a name="manual-scheduling"></a>Käsitsi plaanimine.

Kui automaatse kavandamise reeglid ei vasta teie vajadustele, saate tööülesande režiimi seada väärtusele **Käsitsi ajastatud**. Sellega lõpetab plaanimismootor teiste plaanimisatribuutide väärtuste arvutamise. Sõltumata töörežiimist, kui määrate ülesannete jaoks eelkäijad, mõjutate alati sõltuva ülesande alguskuupäeva.
