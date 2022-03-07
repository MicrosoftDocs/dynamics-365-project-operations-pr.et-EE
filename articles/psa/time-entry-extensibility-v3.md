---
title: Iganädalaste ajakirjete kohandamine
description: Selles teemas kirjeldatakse, kuidas rakendada organisatsiooni tegevust toetavaid ärireegleid.
author: stsporen
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
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
ms.openlocfilehash: fa2ef927e0234919ee4777f24c60569fb33a8570f6d48be6aef356df4f08a6e7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002281"
---
# <a name="customize-weekly-time-entry"></a>Iganädalaste ajakirjete kohandamine 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 Project Service Automation versioonis 3.3 tutvustas Microsoft uudset ruudustikku, mis võimaldab projekti ressurssidel kiiresti aega sisestada, korraga kuni ühe nädala kohta. Uus iganädalane ajakirje ruudustik saab kuvada kirjete kokkuvõtted kuupäeva, rea või nädala järgi. Ressursid saavad teha nädala jooksul ajakirjetest koopiaid ja kopeerida need hulgi kaupa ka eelmistest nädalatest. Süsteemikohandajad saavad vaadet kohandada, lisades välju, otsinguid muudele olemitele ja rakendades kohandatud ärireegleid organisatsiooni tegevuse toetamiseks.

Ajakirje ja uus iganädalane ruudustik on kättesaadav saidikaardi kaudu. Mittelaiendatav kohandatud ajakirje kogemus, mis oli osa varasematest PSA versioonidest, on asendatud laiendatava iganädalase ajakirje ruudustikuga ja samuti teistsuguse kirjutuskaitstud ruudustiku ja kalendri kogemusega. Tänu sellele muudatusele saavad kasutajad sisestada aega nädalate kaupa.

## <a name="page-layout"></a>Lehe paigutus
Uus iganädalane ajakirje ruudustik on kohandatud juhtelement, millel on tööriistariba ja kaks peamist jaotist: **Dimensioonid** ja **Kestus**. Tööriistaribal on nupp, mis rakendub ainult selle kohandatud juhtelemendi puhul ajakirje ruudustiku jaoks. Seevastu lehe ülaosas asuval toimingupaanil olevad nupud rakenduvad kolme tüüpi juhtelementidele, mida ajakirje jaoks toetatakse: iganädalase ajakirje juhtelemendile, kirjutuskaitstud juhtelemendile ja kalendri juhtelemendile.

### <a name="dimensions"></a>Mõõtmed
Jaotises **Dimensioonid** kuvatakse veerupäistena kõik dimensioonid, mille suhtes saab aega sisestada. Valmiskujul toetatakse järgmisi dimensioone.

- Projekt
- Projekti ülesanne
- Roll
- Tüüp
- Kirje olek

Jaotis **Dimensioonid** ei luba tekstisisest redigeerimist. Seda jaotist toetab vaade, mis võimaldab lisada kohandatud välju iganädalase ajakirje ruudustikku. Lisateavet kohandatud väljade lisamise kohta leiate selle teema hilisemast jaotisest „Laiendatavus”.

### <a name="duration"></a>Kestus
Jaotises Kestus kuvatakse nädalapäevad veerupäistena. Selles jaotises lubatakse tekstisisest redigeerimist. Pärast sobivate dimensioonidega ajakirje rea loomist saavad kasutajad kiiresti tekstisiseselt sisestada aja, mis nad nendele dimensioonidele kulutasid.

## <a name="create-a-new-time-entry"></a>Uue ajakirje loomine
Ajakirje ruudustikus uue ajakirje loomiseks vajutage suvandit **Uus**. Ilmub dialoogiboks **Ajakirje kiirloomine**. Selles dialoogiboksis saavad kasutajad valida ajakirje kuupäeva ja seejärel sisestada dimensioonide **Projekt**, **Projekti ülesanne**, **Roll** ja **Kestus** kohta andmed minutites, tundides või päevades, tippides **h**, **m** või **d** koos numbriga. Kasutajad saavad sisestada ka kirjelduse ja kommentaarid, mida saab ajakirje kohta väliselt jagada. Kui kasutajad salvestavad oma muudatused, kuvatakse nende dimensioonide suhtes sisestatud väärtused jaotises **Dimensioonid**. Kestuse teave, mille nad sisestasid väljale **Kestus**, kuvatakse kuupäeval, mille jaoks ajakirje loodi.

Süsteemivaated toetavad otsinguvälju. Näiteks kui kasutaja siseneb projekti, seatakse välja **Projekti ülesanne** vaikimisi väärtuseks vaade **Koopia**. Kui soovite luua ajakirjeid selliste ülesannete jaoks, mis pole kasutajale määratud, klõpsake otsingu dialoogikastis valikut **Muuda vaadet** ja seejärel valige vaade **Kõik aktiivsed projektiülesanded**.

## <a name="edit-a-time-entry"></a>Ajakirje redigeerimine
Mõne ajakirjete lehel oleva välja üksikasju, näiteks **kirjeldust** ja **väliseid kommentaare**, ei kuvata iganädalase ajakirje ruudustikus. Selle asemel ilmub nendesse kestuse lahtritesse, millel on need täiendavad andmed olemas, väike kolmnurkne tähis. Valige lahter ja seejärel klõpsake valikut **Redigeeri üksikasju**, et näha üksikasju paanil **Kiirredigeerimine**. Selleks et redigeerida või värskendada kindlat ajakirjet, mis ei kuulu iganädalase ajakirje ruudustikku, peavad kasutajad avama paani **Kiirredigeerimine**.

## <a name="copy-a-time-entry-row"></a>Ajakirje rea kopeerimine
Kui esimene ajakirje rida on loodud, saavad kasutajad kogu rea uude ritta kopeerimiseks klõpsata valikut **Kopeeri rida**. Kui rida kopeeritakse sel viisil, kopeeritakse ka dimensioonid ja kestused. Kasutajad saavad klõpsata ka valikut **Redigeeri rida**, et värskendada jaotises **Kestus** tekstisiseseid dimensiooniväärtusi ja kestusi.

## <a name="open-a-time-entry"></a>Ajakirje avamine
Selleks et toetada optimaalset ja kiirsisestust kõige olulisemates väljades, kuvatakse iganädalase ajakirje ruudustikus valitud dimensioonide ning ajaliste kestuste alamhulk. Ühe ajakirje kõigi üksikasjade vaatamiseks klõpsake suvandi **Redigeeri kirjet** alt käsku **Ava**.

## <a name="submit-a-time-entry"></a>Ajakirje esitamine
Kasutajad saavad esitada ühe ajakirje või ajakirjete rühma, valides lahtriploki või terve ajakirje rea ning seejärel käsku **Esita**. Esitatud ajakirjed kuvatakse kirjetena, mis on kinnitajate **kinnitamise** lehel kinnitamise ootel. Kui ajakirjed on edukalt esitatud, ei saa neid enam redigeerida.

## <a name="recall-a-time-entry"></a>Ajakirje tagasivõtmine
Saate esitatud ajakirjeid tagasi võtta. Saate tagasi võtta ühe ajakirje, ajakirjete ploki või terve ajakirjete rea. Tagasivõetud ajakirjed on ressurssidele redigeerimiseks saadaval.

## <a name="time-entry-status"></a>Ajakirje olek
Uute ajakirjete olekuks määratakse automaatselt **Mustand**. Kui ajakirje on esitatud, värskendatakse selle olek olekuks **Esitatud**. Kui esitatud ajakirje on kinnitatud, värskendatakse selle olek olekuks **Kinnitatud**. Kui ajakirje lükatakse tagasi, värskendatakse selle olek olekuks **Tagastatud** ning kirjet saab parandada ja uuesti esitada. Kustutada saab ainult neid ajakirjeid, mille olek on **Mustand**.

## <a name="view-rejection-comments"></a>Tagasilükkamise kommentaaride vaatamine
Kui kinnitaja lükkab ajakirje tagasi, võib kinnitaja lisada tagasilükkamise kommentaarid, mis aitavad ressursil tagasilükkamise põhjust mõista. Ajakirje tagasilükkamise kommentaaride vaatamiseks klõpsake valikut **Ava kirje**. Tagasilükkamise kommentaarid kuvatakse ajaskaalal. Ressurss võib ajaskaalal vastata tagasilükkamise kommentaaridele enne, kui ta kirje uuesti esitab.

## <a name="copy-week"></a>Nädala kopeerimine
Pärast paari ajakirje loomist saavad kasutajad valida suvandi **Kopeeri nädal**, et luua hulgi kaupa veelgi ajakirjeid. Ilmub dialoogiboks **Kopeeri**. Ajakirjete kopeerimiseks kasutage jaotises **Perioodi algus** välju **Alguskuupäev** ja **Lõppkuupäev**, et määrata kuupäevavahemik. Määrake jaotise **Perioodi lõpp** väljal **Alguskuupäev** kuupäev, mille jaoks soovite ajakirjeid luua. Seejärel klõpsake käsku **Kopeeri**. Välja „Perioodi lõpp” määratud kuupäeva jaoks luuakse väljal „Perioodi algus” oleva vastava nädalapäeva ajakirjete koopia. Näiteks viimase nädala esmaspäeva ajakirje kopeeritakse selle nädala esmaspäeva, mis on määratud väljal „Perioodi lõpp”.

## <a name="import"></a>Importimine
Sama tavalist protsessi kasutatakse ka broneeringutest, määramistest ja vahetustest importimisel. Kasutajad saavad määrata kuupäevavahemiku, millest broneeringuid imporditakse. Seejärel peavad nad eraldi valima broneeringud, mis tuleks kopeerida ajakirjete mustanditesse. Eelmises väljaandes kuvati soovitatud ajakirjed ruudustikus ja kalendris ning need kadusid seansi värskendamisel.

## <a name="extensibility"></a>Laiendatavus
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Muude olemite otsingutega kohandatud väljade lisamine
Iganädalase ajakirje ruudustikku kohandatud välja lisamiseks on vaja läbi teha kolm etappi.

1.  Lisage kohandatud väli kiirloomise dialoogiboksi.
2.  Konfigureerige ruudustikku kohandatud välja kuvamiseks.
3.  Lisage kohandatud väli vajaduse järgi rea või lahtri muutmise ülesande voogu.

Samuti peate veenduma, et uuel väljal oleksid rea või lahtri muutmise ülesande voos olemas nõutud kinnitused. Selles etapis peate ka välja lukustama, võttes aluseks ajakirje oleku.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Lisage kohandatud väli kiirloomise dialoogiboksi
Peate lisama kohandatud välja dialoogiboksi Ajakirje kiirloomine. nii et kasutajad saavad sisestada sellele väärtuse, kui nad lisavad nupu **Uus** abil ajakirjeid.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigureerige ruudustikku kohandatud välja kuvamiseks
Iganädalase ajakirje ruudustikku kohandatud välja lisamiseks on kaks viisi. Üks võimalus on kohandada vaadet **Minu iganädalased ajakirjed** ja lisada sinna kohandatud väli. Saate valida kohandatud välja asukoha ja suuruse ruudustikus, kui redigeerite vaates neid atribuute.

Teine võimalus on luua uus kohandatud ajakirje vaade ja seada see vaikevaateks. Peale nende veergude, mida soovite ruudustikus näha, peaks see vaade sisaldama ka välju **Kirjeldus** ja **Välised kommentaarid**. Saate valida ruudustiku asukoha, suuruse ja sortimise vaikejärjekorra, kui redigeerite vaates neid atribuute. Seejärel konfigureerige selle vaate kohandatud juhtelementi nii, et see oleks **Ajakirje ruudustiku** juhtelement. Lisage see juhtelement vaatesse ja valige see veebirakenduse, telefoni ja tahvelarvuti jaoks. Seejärel konfigureerige iganädalase ajakirje ruudustiku parameetrid. Seadke välja **Alguskuupäev** väärtuseks **msdyn_date**, välja **Kestus** väärtuseks **msdyn_duration** ja välja **Olek** väärtuseks **msdyn_entrystatus**. Vaikevaate jaoks on välja **Kirjutuskaitstud olekuloendi** väärtuseks seatud **192350002, 192350003, 192350004**, välja **Rea muutmise ülesande voog** väärtuseks **msdyn_timeentryrowedit** ja välja **Lahtri muutmise ülesande voog** väärtuseks **msdyn_timeentryedit**. Saate neid välju kohandada kirjutuskaitstud oleku lisamiseks või eemaldamiseks või mõne muu ülesandepõhise kogemuse (TBX) kasutamiseks, et ridu või lahtreid redigeerida. Need väljad peaksid olema seotud staatilise väärtusega.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Kohandatud välja lisamine sobivasse muutmise ülesande voogu
Redigeerimiseks kasutatavad TBX-i lehed leiate jaotisest **Protsessid**. Vaikelehed on **Project Service – ajakirje rea redigeerimine** ja **Project Service – ajakirje redigeerimine**. Saate neid vaikelehti redigeerida või luua uusi kohandatud TBX-i lehti.

> [!NOTE] 
> Mõlemad valikud eemaldavad olemistest **Projekt** ja **Projekti ülesanne** mõned valmisfiltreerimised, et kõik olemite otsinguvaated oleksid nähtavad. Valmis, kuvatakse ainult asjakohased otsinguvaated.

Peate kohandatud välja jaoks määrama sobiva ülesandevoo. Kui lisasite välja ruudustikku, peaks see kõige tõenäolisemalt minema rea muutmise ülesande voogu, mida kasutatakse nende väljade jaoks, mida rakendatakse tervele ajakirjete reale. Kui kohandatud väljal on iga päev kordumatu väärtus (nt kohandatud väli **Lõppaja** jaoks), peaks see minema lahtri muutmise ülesande voogu.

Kohandatud välja lisamiseks ülesandevoogu lohistage **välja** element lehel sobivasse asukohta ja seadistage selle atribuudid. Seadke atribuudi **Allikas** väärtuseks **Ajakirje** ja atribuut **Andmeväli** kohandatud väljale. Atribuut **Väli** määrab TBX-i lehel kuvatava nime. Väljale tehtud muudatuste salvestamiseks klõpsake käsku **Rakenda**. Seejärel klõpsake lehele tehtud muudatuste salvestamiseks käsku **Värskenda**.

Kui soovite kasutada uut kohandatud TBX-i lehte, looge uus protsess. Seadke kategooria väärtuseks **Äriprotsessi voog**, olemi väärtuseks **Ajakirje** ja äriprotsessi tüübi väärtuseks **Protsessi käivitamine ülesandevoona**. Jaotises **Atribuudid** tuleb atribuudi **Lehe nimi** väärtuseks seada lehe kuvatav nimi. Kõikide asjakohaste väljade lisamine TBX-i lehele. Salvestage ja aktiveerige protsess ning seejärel värskendage vastava töövoo kohandatud juhtelemendi atribuut protsessis väärtusele **Nimi**.

### <a name="add-new-option-set-values"></a>Uute suvandikomplekti väärtuste lisamine
Valmisväljale uute suvandikomplekti väärtuste lisamiseks avage välja redigeerimisleht ja seejärel valige jaotisest **Tüüp** suvandikomplekti kõrval olev käsk **Redigeeri**. Seejärel lisage uus suvand, millel on kohandatud silt ja värv. Kui soovite lisada uue ajakirje oleku, on valmisvälja nimi **Kirje olek**, mitte **Olek**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Uue ajakirje oleku määramine kirjutuskaitstuks
Selleks et määrata uue ajakirje olek kirjutuskaitstuks, lisage atribuudile **Kirjutuskaitstud olekuloend** uus ajakirje väärtus (arv, mitte silt). Ajakirjete ruudustiku redigeeritav osa lukustatakse uue olekuga ridade jaoks.
Seejärel lisage ärireeglid, et lukustada kõik väljad TBX-i lehtedel **Ajakirje rea redigeerimine** ja **Ajakirje redigeerimine**. Saate nende lehtede ärireeglitele ligi, kui avate lehe äriprotsessi voo redaktori ja valite suvandi **Ärireeglid.** Saate lisada olemasolevate ärireeglite tingimusele uue oleku või uuele olekule uue ärireegli.

### <a name="add-custom-validation-rules"></a>Kohandatud valideerimisreeglite lisamine
Olemas on kahte tüüpi valideerimisreegleid, mida saate lisada iganädalase ajakirje ruudustiku kogemusse: • kliendipoolsed ärireeglid, mis töötavad kiirloomise dialoogiboksides ja TBX-i lehtedel • serveripoolsed lisandmooduli kinnitused, mis rakenduvad kõikidele ajakirjete värskendustele

#### <a name="business-rules"></a>Ärireeglid
Ärireeglite abil saate välju lukustada ja avada, sisestada väljade vaikeväärtused ning määrata kinnitused, mis nõuavad ainult praeguse ajakirje kirje teavet. Saate TBX-i lehe ärireeglitele ligi, kui avate lehe äriprotsessi voo redaktori ja valite suvandi **Ärireeglid.** Saate redigeerida olemasolevaid ärireegleid või lisada uue ärireegli. Veelgi enam kohandatud kinnituste jaoks saate kasutada ärireeglit ka JavaScript käivitamiseks.

#### <a name="plug-in-validations"></a>Lisandmooduli kinnitused
Peaksite kasutama lisandmoodulite kinnitusi kõikide nende kinnituste jaoks, mis vajavad rohkem konteksti, kui on olemas ühes ajakirje kirjes, või nende kinnituste jaoks, mida soovite käivitada ruudustikus tekstisiseste värskenduste kohta. Valideerimise lõpuleviimiseks looge olemisse **Ajakirje** kohandatud lisandmoodul.

> [!IMPORTANT] 
> Kui värskendamisel nurjub lisandmooduli valideerimine, takistab TBX-i lehtede teadaolev probleem praegu kasutajatel teavet parandamast ja valimast uuesti suvandit Valmis. Selleks et vältida seda olukorda nii palju kui võimalik, seadistage lahendusega ärireegli kinnitused.


[!INCLUDE[footer-include](../includes/footer-banner.md)]