---
title: Ressursimääramiste loomine
description: See artikkel annab teavet üldiste ja nimeliste ressursside määramise kohta.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811988"
---
# <a name="create-resource-assignments"></a>Ressursimääramiste loomine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


Ressursimääramine on otsene projektimeeskonna liikme otsene seostamine lehe ülesandega. See artikkel annab teavet ressursside määramise eri viiside kohta.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Üldise meeskonnaliikme loomine ülesannete määramistega


Ülesande määramise kaudu üldise meeskonnaliikme loomisel loote te kohatäite või üldise ressursi. See üldine ressurss kirjeldab nimetatud ressursi omadusi, millega soovite lõpuks ülesannetega töötada. Seejärel loote nõude või esitate taotluse, kasutades nõuet, mida kasutatakse nimega ressursi otsimiseks ja broneerimiseks.

1. Valige ülesande ruudustikus Ajakava ressursilahtrist ikoon **Ressurss**.
2. Tippige kohatäiteressursi nimena kasutatav nimi. Nt programmihaldur.
3. Valige **Loo** ja määrake väljal **Projekti meeskonnaliikme kiirloomine** üldise ressursi roll.
4. Määrake sellele kohatäite ressursile vastavalt vajadusele ülesanded, valides ressursi ülesandele jaotisest **Ressursivalija**. Jaotises **Meeskonnaliikmed** loetletud ressursid.
5. Kui olete üldise ressursi määramise lõpetanud, valige vahekaardil **Meeskond** üldine ressurss ja seejärel valige **Loo nõue, et luua üldallikale ressursinõue** .
6. Valige üldise ressursi jaoks suvand **Reserveeri** ja seejärel kasutage ajakavapaneeli, et leida ning reserveerida päris ressurss. Samuti saate esitada nõude ressursihaldurile täitmiseks.
7. Kui üldine ressurss on nimega ressursiga täielikult täidetud, eemaldatakse üldine ressurss meeskonnast. (Ressursinõude osalise täitmise tulemuseks ei ole ressursimääramine.) Üldise ressursi ülesandemäärangud määratakse nimetatud ressursile, mis vastas üldise ressursi ressursinõudele.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Nimega ressursi määramine kõikide broneeritavate ressursside loendist

Saate kasutada **Ressursivalija** otsinguvälja, et otsida kõiki aktiivseid broneeritavaid ressursse ja neid mis tahes lehe ülesandele määrata. Sel viisil määratud ressursid lisatakse meeskonda ilma broneeringuta. See on sarnane meeskonnaliikmete lisamise ja eraldamise meetodiks **Pole** valimisega. Ressurss kuvatakse vahekaartidel **Meeskond**, **Ressursi määramine** ja **Sobitamine** ressurssidena, millel on vaid määrangud ja broneeringute puudujääk. Reserveerige neid, kui soovite nende saadavaolekut kasutada.

1. Liikuge tööpaanilt, paneellilt või ajajoonelt lahtrisse **Määratud:**.
2. Hakake tippima otsinguväljale nime. Nime otsingutulemused kuvatakse jaotise **Muud ressursid** all olevas **Ressursivalijas**.
3. Valige ressurss, mille soovite ülesandele määrata, või valige ressursi nimi suvandist **Muud meeskonna ressursid**.

## <a name="editing-resource-assignment-contours"></a>Ressursi määramise kontuuride redigeerimine

Vaikimisi, kui ressursid on määratud graafikus olevale ülesandele, jaotatakse nende panus lineaarselt igale ressursile, võttes aluseks selle ressursi töötunnid ja projekti ajakava režiimi. Projektijuht saab ressursimääramisruudustiku abil täpsustada igale ühele või mitmele ülesandele määratud ressursi panuse prognoose erinevatel ajaskaaladel. See funktsioon aitab projektijuhtidel koostada täpsemaid kulu- ja müügiprognoose, mida juhivad ressursi määramise kontuurid, mis luuakse ressursi ülesandele määramisel. Lisaks saavad projektijuhid hõlpsamini kajastada ressursinõudlust, mis on vajalik nõudluse loomiseks ressursinõudes.

### <a name="navigation"></a>Navigeerimine

Kontuuri redigeerimisruudustikule juurdepääsemiseks valib **projektijuht kõigepealt projekti avalehel vahekaardi Tööülesanded** ja seejärel vahekaardi **Ülesanded** .

![Vahekaart Ülesanded projekti avalehe vahekaardil Tööülesanded.](media/AssignmentGrid.png)

Ruudustik toetab rühmitamiseks kahte meetodit: rühmitage ressursi **järgi ja** rühmage ülesande **järgi.** Erinevalt ruudustikuvaatest pole veerud konfigureeritavad. Ainsad nähtavad veerud on **Määratud**, Ülesande nimi **, Ülesande algus,** **Ülesande** lõpp ja **Ülesande** **panus.**

Kui võrk on algselt renderdatud, algab see kõige varasemast määramiskontuurist. Kui teie ajakava ei sisalda ülesandeid, millel on pingutus, on ruudustik tühi ega renderda midagi.

![Tühi määramisruudustik.](media/emptyassignmentgrid.png)

Kui soovite vaadata oma kontuure ja erinevaid ajaskaalasid, on saadaval ka kirjutuskaitstud ressursimäärangute ruudustik ja ressursside vastavusseviimise ruudustik.

### <a name="resource-calendars"></a>Ressursside kalendrid

Konkreetse päeva kontuuri redigeerimise võimalust reguleerivad ressursi tööpäevad, mis kajastuvad nende kalendris. Kui lahter on antud ressursi jaoks keelatud, pole sellel ressursil sellel perioodil tööpäevi.

Ressursi kontuurid võivad ulatuda kaugemale määratud ülesande praegustest algus- ja lõppkuupäevadest. Kui kontuuri värskendatakse nii, et see on pärast ülesande viimast lõppkuupäeva või ülesande varaseimat alguskuupäeva, muudetakse vastavalt vajadusele ülesande lõpp- või alguskuupäeva. Kui aga kontuuri värskendatakse nii, et see on eelkäijaga lingitud ülesande alguskuupäevast varasem, siis värskendamine nurjub, kuna ülesanne käivitab ülesande käivitamise enne eelkäija lõpuleviimist ja seda käitumist praegu ei toetata.

### <a name="co-authoring"></a>Kaasautorlus

Ressursimääranguruudustiku muudatused kajastuvad automaatselt kõigis seotud vaadetes, sh diagrammi-, ajaskaala-, tahvli- ja ruudustikuvaadetes. Kui projekti vaatab korraga üle mitu kasutajat, kajastuvad kõik ühe kasutaja tehtud muudatused ruudustikus. Seevastu kõik ressursi määramise ruudustikus tehtud muudatused kuvatakse kõigile teistele kasutajatele, kes vaatavad projekti samal seansil.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
