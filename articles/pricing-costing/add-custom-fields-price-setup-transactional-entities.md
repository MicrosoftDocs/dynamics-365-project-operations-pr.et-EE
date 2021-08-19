---
title: 'Nõutavate kohandatud väljade lisamine hinna seadistusele ja ülekande olemitele '
description: Selles teemas kirjeldatakse, kuidas lisada olemitele ja vormidele ning vaadetele nõutavaid kohandatud välja viiteid.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 36c95913cc72e293c3015e1b9d3055aac476eebb4cf7d7993741d3cb61de0e13
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006151"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Nõutavate kohandatud väljade lisamine hinna seadistusele ja ülekande olemitele 

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Selles teemas eeldatakse, et olete läbinud toimingud teemas [Hinnakujunduse dimensioonidena kasutamiseks mõeldud kohandatud väljade ja olemite loomine](create-custom-fields-entities-pricing-dimensions.md). Kui te pole neid toiminguid lõpetanud, minge tagasi, viige need lõpuni ja seejärel tulge selle teema juurde tagasi. 

Selles teemas kirjeldatakse protseduure, kuidas lisada olemitele ja kasutajaliidese (UI) elementidele (nt vormidele ja vaadetele) nõutavaid kohandatud välja viiteid.

## <a name="add-custom-pricing-dimension-fields"></a>Kohandatud hinnakujunduse dimensioonide väljade lisamine 
Pärast kohandatud väljade ja olemite loomist on järgmiseks etapiks hindade seadistamise ja ülekande olemite teadlikkus kohandatud olemitest või suvandikomplekti loomisest, luues viite välju. Sõltuvalt sellest, kas teie hinnakujunduse dimensioonide loend sisaldab suvandikomplekt mõõtmeid või olemi dimensioone või mõlemat, järgige ainult **Suvandikomplekti põhjal kohandatud hinnakujunduse dimensioonide** või **Vastavalt olemile kohandatud hinnakujunduse** etappe või mõlemaid.

### <a name="option-set-based-custom-pricing-dimensions"></a>Suvandikomplekti põhjal kohandatud hinnakujunduse dimensioonid
Kui kohandatud hinnakujunduse dimensioon on suvandikomplekti põhine, lisage see põhiüksustele väljana. Järgmises toimingus kasutatakse **ressursi tööasukohta** ja **ressursi tööaega** suvandikomplekti aluseks olevate hinnakujunduse dimensioonidena. Need tuleb esmalt lisada väljadena hinnakujunduse olemitele, **Rolli hind** ja **Rolli hinna hinnalisand**.

1. Valige Projecti toimingutes **Sätted** > **Lahendused** ja topeltklõpsake suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**. 
2. Valige Solution Exploreris vasakpoolsel navigeerimispaanil **Olemid > Rolli hind**.
3. Laiendage üksust **Rolli hind** ja valige suvand **Väljad**.
4. Valige **Uus**, et luua uus väli, mille nimi on **Ressursi töö asukoht**, ja valige välja tüübiks **Suvandikomplekt**. 
5. Valige **Kasuta olemasolevat suvandikomplekti**, valige suvandikomplekt **Ressursi töö asukoht** ja valige seejärel **Salvesta**.
6. Kui soovite selle välja lisada olemisse **Rolli hinna hinnalisand**, korrake etappe 1–5. 
7. Korrake etappe 1–5 suvandikomplekti **Ressursi töötunnid** jaoks.

> [!IMPORTANT]
> Kui lisate välja rohkem kui ühele olemile, kasutage kõigi olemite jaoks sama välja nime. 

> ![Ressursi tööasukoha lisamine rolli hinnale.](media/RWL-Field.png)

Projekti müügi ja prognoosimise faasides kasutatakse hinnapakkumise/projekti väärtuse hindamiseks **kohalike** ja **kohapealsete** tööde lõpuleviimiseks nõutavat töökoormust, mis on seotud **regulaarsete tundide** ja **ületunnitööga**. Väljad **Ressursi töö asukoht** ja **Ressursi tööaeg** lisatakse hinnangu olemitele, **hinnapakkumise rea üksikasjadele**, **lepingurea üksikasjadele**, **projekti meeskonnaliikmetele** ja **hinnangu reale**.

1. Valige Projecti toimingutes **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**. 
2. Valige Solution Exploreris vasakul navigeerimispaanil **Olemid > Hinnapakkumise rea üksikasi**.
3. Laiendage olemit **Hinnapakkumise rea üksikasi** ja valige **Väljad**.
4. Valige **Uus**, et luua uus väli, mille nimi on **Ressursi töö asukoht**, ja valige välja tüübiks **Suvandikomplekt**. 
5. Valige **Kasuta olemasolevat suvandikomplekti** ja **Ressursi tööasukoht** ja valige seejärel **Salvesta**.
6. Korrake etappe 1–5, et lisada see väli olemitesse **Projekti lepingurea üksikasi**, **Projekti meeskonnaliige** ja **Hinnangurida**.
7. Korrake etappe 1–6 suvandikomplekti **Ressursi tööaeg** jaoks. 

> ![Ressursi tööasukoha lisamine hinnangureale.](media/RWL-Default-Value.png)

Kohaletoimetamiseks ja arveldamiseks peab lõpetatud töö täpselt hinnatud olema, et valida, kas see teostati projekti tegelikes näitajates **kohalikult** või **kohapeal**, ja kas see viidi lõpule **tavaliste tundide** või **ületunnitöö** ajal. Väljad **Ressursi tööasukoht** ja **Ressursi töötunnid** tuleks lisada olemitesse **Ajakirje**, **Tegelik**, **Arve rea üksikasi** ja **Töölehe rida**.

1. Valige **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**.
2. Valige Solution Exploreris vasakpoolsel navigeerimispaanil **Olemid > Ajakirje**.
3. Laiendage olemit **Hinnapakkumise rea üksikasjad** ja valige **Väljad**.
4. Valige **Uus**, et luua uus väli, mille nimi on **Ressursi töö asukoht**, ja valige välja tüübiks **Suvandikomplekt**. 
5. Valige **Kasuta olemasolevat suvandikomplekti**, valige suvandikomplekt **Ressursi töö asukoht** ja valige seejärel **Salvesta**.
6. Korrake etappe 1–5, et lisada see väli olemitele **Tegelik**, **Arve rea üksikasjad** ja **Töölehe rida**.
7. Korrake etappe 1–6 suvandikomplekti **Ressursi tööaeg** jaoks. 

> ![Ressursi tööasukoha lisamine ajakirjele.](media/RWL-time-entry.png)

See lõpetab suvandikomplektipõhiste kohandatud dimensioonide jaoks nõutava skeemi muutmise.

## <a name="entity-based-custom-pricing-dimensions"></a>Olemipõhise kohandatud hinnakujunduse dimensioonid

Kui kohandatud hinnakujunduse dimensioon on olem, lisatakse dimensiooni olemi ja põhiliste olemite vahel 1 : N seosed. Kui kasutate standardse ametinimetuse näidet, on mõistlik eeldada, et igale töötajale määratakse standardne ametinimetus. SAs-i tulemusena on teil vaja 1 : N seost standardsest ametinimetusest broneeritavasse ressurssi või N : 1 seost, kui see on loodud broneeritavast ressursist standardsesse ametinimetusse.

1. Valige Projecti toimingutes **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**. 
2. Valige Solution Exploreris vasakpoolsel navigeerimispaanil **Olemid > Standardne ametinimetus**.
3. Laiendage olemit **Standardne ametinimetus** ja valige **1 : N seosed**.
4. Valige **Uus**, et luua uus 1 : N seos nimega **Standardne ametinimetus broneeritavale ressursile**. Sisestage nõutud teave ja valige seejärel **Salvesta**.

> ![Standardse ametinimetuse lisamine viiteväljana broneeritavale ressursile.](media/ST-BR.png)

Standardne ametinimetus tuleb lisada ka hindamisolemitele, **rolli hinnale** ja **rolli hinna hinnalisandile**. See on lõpule viidud ka kasutades olemite **Standardne ametinimetus** ja **Rolli hind** ning **Standardne ametinimetus** ja **Rolli hinna hinnalisand** vahelisi 1 : N seoseid.

1. Valige Solution Exploreris vasakpoolsel navigeerimispaanil **Olemid > Standardne ametinimetus**.
2. Laiendage olemit **Standardne ametinimetus** ja valige **1 : N seosed**.
3. Valige **Uus**, et luua uus 1 : N seos nimega **Standardne ametinimetus rolli hinnale**. Sisestage nõutud teave ja valige seejärel **Salvesta**.
4. Korrake etappe 1–4, et luua 1 : N seoseid olemite **Standardne ametinimetus** ja **Rolli hinna hinnalisand** vahel.

Projekti müügi- ja hinnangufaasis on hinnapakkumise/projekti hindamiseks vaja iga standardse ametinimetuse jaoks töökoormuse kalkulatsiooni. See tähendab, et vajalikud on 1 : N seosed standardsete ametinimetuste ja iga järgmise hinnangu olemi vahel. 

- **Hinnapakkumise rea üksikasjad**
- **Projekti lepingurea üksikasi**
- **Projektimeeskonna liige**
- **Prognoosi rida**

5. Korrake etappe 1–5, et luua 1 : N seoseid olemite **Standardne ametinimetus**, **Hinnapakkumise rea üksikasi**, **Projekti lepingureaüksikasjad**, **Projekti meeskonnaliige** ja **Hinnangurida** vahel.

> ![Standardse ametinimetuse lisamine viiteväljana hinnangureale.](media/ST-Estimate-Line.png)

  Kohaletoimetamise ja arveldamise faasides peab iga standardse ametinimetuse tehtud töö täpselt projekti tegelikele hindadele vastama. See tähendab, et on vaja 1 : N seoseid olemite **Standardne ametinimetus**, **Ajakirje**, **Tegelik**, **Arve rea üksikasjad** ja **Töölehe rida** vahel.

6. Korrake etappe 1–6, et luua 1 : N seost olemite **Standardne ametinimetus**, **Ajakirje**, **Tegelik**, **Arve rea üksikasjad** ja **Töölehe rida** vahel.

> ![Standardse ametinimetuse lisamine viiteväljana ajakirjele.](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Dimensiooniväärtuse vaikeväärtuse seadmine platvormi vastendusfunktsioonide abil
Ajakirje puhul oleks süsteemi vaikimisi standardne ametinimetus arveldatava ressursi ajakirjest, mis salvestab ajakirjet. Järgmiste juhiste abil saate lisada välja vastendusi 1 : N seosele **broneeritavast ressursist** **ajakirjesse**.

1. Valige Solution Exploreris vasakpoolsel navigeerimispaanil **Olemid > Standardne ametinimetus**.
2. Laiendage olemit **Standardne ametinimetus** ja valige **1 : N seosed**.
3. Topeltklõpsake suvandit **Broneeritav ressurss ajakirjesse**. Valige lehel **Seos** suvand **Kasuta väljavastendusi**. 
4. Valige **Uus**, et luua uue välja vastendamine välja **Standardne ametinimetus** olemis **Broneeritav ressurss** ja viitevälja **Standardne ametinimetus** olemis **Ajakirje** vahel. 

> ![Välja vastenduste seadistamine, et lubada standardse ametinimetuse sisestamist broneeritud ressursilt ajakirjele.](media/ST-Mapping2.png)

See lõpetab suvandikomplektipõhiste kohandatud dimensioonide jaoks nõutava skeemi muutmise.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Kohandatud väljade lisamine vormidele, vaadetele ja ärireeglitele

Pärast seda, kui olete kõik vajalikud skeemid muutnud, on järgmiseks etapiks teha väljad UI-des nähtavaks, lisades väljad vormidele ja vaadetele.

1. Avage vorm või vaade. Valige parempoolsel navigeerimispaanil väli ja lohistage see vormi lõuendile. 
2. Vaate redigeerimisel kasutage parempoolset navigeerimispaani, valige **Lisa väljad** ja valige dialoogiboksis **Väljaloend** soovitud väljad ning valige **Ok**.

Järgmises tabelis on esitatud terviklik loend kasutusvalmis vormidest ja vaadetest olemitelt, mida on vaja uute väljadega värskendada. Kui teil on nende olemite kohandustes täiendavaid vaateid või vorme, lisage uued väljad ka neile.

| Entity        | Vormid, mis vajavad uut välja   |Vaated, mis vajavad uut välja      |
| ------------------------------|---------------------------------|----------------------------------|
|  Rolli hind|• Teave |• Aktiivse ressursikategooria hinnad<br> • Ressursikategooria hinna seostatud vaade|
|  Rolli hinna hinnalisand|• Teave|• Aktiivse rolli hinna hinnalisand<br>• Rolli hinna hinnalisandi seostatud vaade|
|  Hinnapakkumise rea üksikasi|• Projekti teave<br>• Projekti kiirloomine|• Aktiivse hinnapakkumise rea üksikasjad<br>• Kombineeritud hinnapakkumise rea üksikasjad<br>• Hinnapakkumise rea üksikasjade seostatud vaade|
|  Projekti lepingurea üksikasjad|• Projekti teave<br>• Projekti kiirloomine|• Kombineeritud lepingurea üksikasjad<br>• Aktiivse lepingurea üksikasjad<br>• Lepingurea üksikasjade seostatud vaade|
|  Projektimeeskonna liige|• Teave<br>• Uus vorm|• Aktiivsed projekti meeskonnaliikmed<br>• Projekti meeskonnaliikmed<br>• Projekti meeskonnaliikmete seostatud vaade|
|  Ajakirje|• Teave<br>• Ajakirje loomine|• Minu ajakirjed kuupäeva järgi<br>• Minu selle nädala ajakirjed<br>• Ajakirjed kinnitamiseks|
|  Töölehe rida|• Teave<br>• Kiirloomine|• Aktiivse töölehe read<br>• Töölehe rea seostatud vaade|
|  Arve rea üksikasjad|• Teave<br>• Kiirloomine|• Aktiivse arve rea üksikasjad<br>• Arveldatavad arvekanded<br>• Tasuta arvekanded<br>• Arve rea üksikasjade seostatud vaade<br>• Mittearveldatavad arvekanded|
|  Tegelik|• Teave<br>• Aktiivsed tegelikud näitajad|• Tegelik seostatud vaade|

Sõltuvalt sellest, mida olete määratlenud, tuleb ärireeglitele lisada ka kohandatud väljad. Üks valmislahenduse näide on ärireegel **Olekul põhineva ajakirje redigeeritavus**. See reegel määratleb, millised väljad tuleb lukustada, kui ajakirje on mitte-redigeeritavas olekus (nt **kinnitatud**). Lisage sellele ärireeglile väljad, et need väljad oleksid redigeerimiseks lukus, kui ajakirje on muus olekus kui **mustand** või **tagastatud**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]