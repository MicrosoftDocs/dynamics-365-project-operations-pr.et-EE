---
title: Organisatsiooniüksused
description: See artikkel läheb organisatsiooniüksuste mõistet ja selgitatakse, kuidas luua ja hooldada organisatsiooniüksusi rakenduses Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921619"
---
# <a name="organizational-units-overview"></a>Organisatsiooniüksuste ülevaade

Rakenduse Microsoft Dynamics 365 Project Operations mõistes on *organisatsiooniüksus* professionaalse teenusettevõtte eraldiseisev rühm või allüksus, kus on tasutatavad töötajad, kellel on kulumäärad.

Professionaalsete teenustega tegelevate ettevõtete puhul, kes kasutavad tehnilisi ressursse erinevates tegevusvaldkondades või ärivaldkondades, võib rolli täitmise maksumus erineda, olenevalt praktikaalast või ärivaldkonnast, kus roll täidetakse. Selle stsenaariumi korral aitab organisatsiooniüksuste kontseptsioon, pakkudes võimalust arveldatavate rollide komplekti rühmitamiseks ettevõtte allüksust, millel on nende rollide jaoks selge kulustruktuur.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Organisatsiooniüksuste mõiste rakenduses Project Operations

Rakenduses Project Operations on organisatsiooniüksusel kindel valuuta ja konkreetsed omahinnakirjad.

Organisatsiooniüksuse valuuta on esmane valuuta, mida kasutatakse kulude jälgimiseks.

Iga organisatsiooniüksusega saab siduda ühe või mitu kulude hinnakirja. Rakendus Project Operations seab organisatsiooniüksusele lisatavale hinnakirjale järgmised piirangud.

- Hinnakirjad peavad olema organisatsiooniüksuse valuutas.
- Hinnakirjad peavad olema omahinnakirjad.

Lisaks sisaldab ressursiolem organisatsiooniüksuse atribuuti. Igale kasutajale saab määrata vaid ühe organisatsiooniüksuse.

### <a name="roles-of-organizational-units"></a>Organisatsiooniüksuste rollid

Organisatsiooniüksusel on rakenduses Project Operations kaks rolli.

- **Tellija** – organisatsiooniüksus, mis esindab ettevõtet või allüksust, kes vastutab peamiselt müügitegevuse ning töö ja teenuste pakkumise eest kliendile. Tellija tuvastatakse väljal **Tellija**, mis asub lehtede **Müügivõimalus**, **Hinnapakkumine**, **Projekti leping** ja **Projekt** päises.
- **Ressursiüksus** – organisatsiooniüksus, millele ressurss kuulub või millesse see on määratud. See organisatsiooniüksus võib pakkuda ressursse töökirjelduse (SOW-d) ja tellija omanduses olevate projektide teatud rollide jaoks.

![Lepingut sõlmivad üksused ja ressursiühikud.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Organisatsiooniüksuse KKK

Siit leiate vastused paljudele korduma kippuvatele küsimustele organisatsiooniüksuste kohta.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Kuidas on rakenduse Project Operations organisatsiooniüksuse olem seotud Dynamics 365-s juba olemasoleva organisatsiooni olemiga?

Dynamics 365 organisatsiooni olem tähistab globaalse Dynamics 365 eksemplari nime. Tavaliselt on see globaalse ettevõtte nimi.

Organisatsiooniüksuse olem esindab globaalses ettevõttes rühma või allüksust. Sellel rühmal või allüksusel on nende rollide jaoks rollide komplekt ja hinnakiri ning need rollid ja hinnakirjad erinevad ettevõtte muude rühmade või allüksuste rollidest ja hinnakirjadest.

Kui rakendus Project Operations on installitud, luuakse organisatsiooni põhjal vaikimisi organisatsiooniüksus. Kõik olemasolevad ressursid määratakse vaikimisi organisatsiooniüksusele. Kui rakendusse Dynamics 365 imporditakse uusi Active Directory kasutajaid või ressursse, määrab kasutaja importimise protsess need vaikimisi rakenduses Project Operations kasutatavale organisatsiooniüksusele.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Kuidas organisatsiooniüksuse olem erineb äriüksuse olemist?

Dynamics 365-s on äriüksuse olem turvaline konstruktsioon. Äriüksusega kasutaja ühing määratleb olemid ja olemi kirjed, millele kasutajal on juurdepääs. Samuti määratleb see õigused (loomine, lugemine, kirjutamine, kustutamine, lisamine, lisamine millelegi, määramine või ühiskasutus), mis kasutajal on nende olemi kirjete jaoks.

Organisatsiooniüksus olem esindab ettevõtte rühma või allüksust, millel on sellele määratud töötajate jaoks erinevad kulumäärad. Organisatsiooniüksuse ja ressursi seos määratleb ressursi kulu projektiga seostamiseks.

Kui rakendate Dynamics 365, optimeerige äriüksuste hierarhia jaoks turvakontroll ja kasutajate määramine äriüksustesse. Määrake kõik kasutajad, kes peavad tavaliselt sama äriüksuse samale kirjete komplektile juurde pääsema. Organisatsiooniüksus ei mõjuta turvakontrolli ega juurdepääsu.

**Näide, mis näitab üht potentsiaalset erinevust organisatsiooniüksuste ja äriüksuste modelleerimisel**

Jõgi, Ltd.-l on edukas Microsofti tehnoloogia kasutamise kogemus. Marko ja Brita on mõlemad C\# arendajad, kuid Brita asub Ameerika Ühendriikides, samas kui Marko elab Indias. Enamik projektikohustusi nõuavad nii Contoso India kui ka Contoso USA ressursse ning Prakash ja Tricia nõuavad selle praktikavaldkonna projektidele samaväärset turvalisuse taset. Kuid Jõgi India arendajate kulu erineb oluliselt Jõgi USA arendajate kuludest.

Siin on optimaalne viis selle stsenaariumi kujundamiseks rakenduste Dynamics 365 ja Project Operations abil.

1. Looge Microsofti tehnoloogiline tegevus äriüksusena ning seostage sellega Marko ja Brita. Sel aitate tagada, et mõlemal töötajal oleks sama turvatase, et kõigile selle ala projektidele juurde pääseda. Mõlemal on võimalik kontrollida edenemist ning aruande aega, kulusid, materjalikasutust ja tööülesannete värskendusi.
2. Looge kaks organisatsiooniüksust, et aidata tagada projekti kulu õigesti kajastamine.
3. Seostage Tricia ettevõttega Contoso US ja Prakash ettevõttega Contoso India.
4. Määrake vastavad kulu hinnakirjad mõlemale organisatsiooniüksusele. Sel viisil saate aidata tagada, et Marko ja Brita projektile kirjendatud kulud kajastavad täpselt Contoso USA ja Contoso India vahelise erinevuse kulusid.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Kas organisatsiooniüksused on rakenduses Dynamics 365 seotud müügipiirkondadega?

Müügipiirkondade ja organisatsiooniüksuste vahel pole seoseid ega suhteid. Müügipiirkond on tavaliselt geograafiline ala, kus müük aset leiab. Müügi hinnakirja saab seostada iga müügipiirkonnaga.

Organisatsiooniüksus on ettevõtte sisemine rühm või allüksus, mis jälgib teatud rollide kulusid, mis on seotud müügiga teistele allüksustele või välistele klientidele.

**Näide, mis näitab üht potentsiaalset erinevust organisatsiooniüksuste ja müügiterritooriumite modelleerimisel**

Jõgi, Ltd.-l on kaks arenduskeskust: Jõgi USA ja Jõgi India. Nende kahe arenduskeskuse ressursside kulu erineb suuresti. Contoso müüb oma infotehnoloogia (IT) teenuseid paljudel rahvusvahelistel turgudel, näiteks Ladina-Ameerikas, Põhja-Ameerikas, Aasia ja Vaikse ookeani piirkonnas, Lääne-Euroopas ja Lähis-Idas. Sama projekti rollide arveldusmäärad võivad nendel turgudel olla väga erinevad. Jõgi USA ja Jõgi India tuleks seadistada organisatsiooniüksustena ja igal organisatsiooniüksusel peaks olema oma kulude hinnakiri. Aasia ja Vaikse ookeani piirkond, Ladina-Ameerika, Põhja-Ameerika, Lääne-Euroopa ja Lähis-Ida tuleks seadistada müügipiirkondade järgi ja igal müügipiirkonnal peaks olema oma müügi hinnakiri.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Miks on hinnakirja ja organisatsiooniüksuse seostamisel piirangud?

Müügihinnad on tavaliselt kordumatud geograafiliste piirkondade või turgude jaoks, kus teenuseid müüakse. Ettevõtte sisemistel allüksustel ei ole tavaliselt omaenda müügihindasid sama tüüpi teenuste jaoks. Kuid sisemistel allüksustel on erinev müüdud kaupade kulu (omahinnad), olenevalt sellest, millised on nende töötajate oskused ja töötingimused selles piirkonnas, kus nad töötavad. Kuna organisatsiooniüksused on kujundatud ettevõtte sisemiste allüksustena, võivad neil olla ainult kulu hinnakirjad.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Miks me ei saa müügi hinnakirja seostada organisatsiooniüksustega?

Rakenduses Project Operations saab müügi hinnakirju seostada klientide ja müügipiirkondadega. Tehingute olemid, näiteks nagu müügivõimalus, hinnapakkumine, projekti leping ja projektipõhised müügi hinnakirjad, mis on lisatud kliendikontole või müügipiirkonnale, et määrata kindlaks projekti kaasamise arvemäärad ja võimalik tulu.

Kulu hinnakirjad on seostatud organisatsiooniüksustega. Tehingute olemid, nagu näiteks müügivõimalus, hinnapakkumine, projekti leping ja projektipõhised müügi hinnakirjad, mis on lisatud tellijale, et määratleda projektiga seotuse kulu.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Kas organisatsiooniüksused on rakenduses Project Operations hierarhilised?

Ei. Praeguses rakenduse Project Operations väljaandes ei ole organisatsiooniüksused hierarhilised. Seetõttu ei saa te järgmisi ülesandeid täita:

- Konfigureerige vaikimisi omahindade sisestamise muster, mis läbib hierarhiat ülespoole.
- Aruanne tulude või kulude kohta, mis on koondatud organisatsiooniüksuse hierarhia eri tasanditele.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Oleme suur rahvusvaheline ettevõte, millel on keerukas mitmetasandiline hierarhia kulukeskuste, allüksuste ja arvete osakondade jaoks. Kuidas saame organisatsiooniüksuste kontseptsiooni kõige paremini kasutada rakenduse Project Operations praeguses versioonis? kasutada?

Kui teil on kulukeskuste, allüksuste, arvete osakondade jne keerukas hierarhia, seadistage selle hierarhia lehed eraldiseisvate organisatsiooniüksustena.

Järgmine näide illustreerib tüüpilist hierarhiat.

**Jõgi India**

- SAP-praktika

    - Tehnilised konsultandid
    - Funktsionaalsed konsultandid

- Microsofti tehnoloogiapraktika

    - Tehnilised konsultandid
    - Funktsionaalsed konsultandid

**Jõgi US**

- SAP-praktika

    - Tehnilised konsultandid
    - Funktsionaalsed konsultandid

- Microsofti tehnoloogiapraktika

    - Tehnilised konsultandid
    - Funktsionaalsed konsultandid

Kui teie hierarhia meenutab seda näidet, peate selle seadistama lameda loendina, nagu siin näidatud.

- Jõgi India – SAP-praktika – tehnilised konsultandid
- Jõgi India – SAP-praktika – funktsionaalsed konsultandid
- Jõgi India – Microsofti tehnoloogiapraktika funktsionaalsed konsultandid
- Jõgi India – Microsofti tehnoloogiapraktika funktsionaalsed konsultandid
- Jõgi USA – SAP-praktika – tehnilised konsultandid
- Jõgi USA – SAP-praktika – funktsionaalsed konsultandid
- Jõgi USA – Microsofti tehnoloogiapraktika tehnilised konsultandid
- Jõgi USA – Microsofti tehnoloogiapraktika funktsionaalsed konsultandid

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Me oleme väike professionaalne teenindusettevõte, mis tegutseb ainult ühe allüksusena. Kuidas saame organisatsiooniüksuste kontseptsiooni kõige paremini kasutada rakenduse Project Operations praeguses versioonis? kasutada?

Kui teie ettevõte tegutseb ühe üksusena, millel on üks kulude hinnakiri, ei pea te organisatsiooniüksusi seadistama. Rakenduse Project Operations installimine loob ühe vaikimisi organisatsiooniüksuse, millel on organisatsiooniga sama nimi. Kõik olemasolevad ressursid määratakse vaikimisi organisatsiooniüksusele. Iga kord, kui süsteem nõuab, et valitaks organisatsiooniüksus, valitakse vaikimisi organisatsiooniüksus.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Kui projekt luuakse hinnapakkumise või projekti lepingurea põhjal, tuleneb vaiketellija hinnapakkumisest või projekti lepingust. Milline on vaikimisi lepingu sõlmimise üksus, kui projekt luuakse enne müügiüksusi, näiteks hinnapakkumist või projekti lepingut?

Kui projekt luuakse eraldi, põhineb projekti vaiketellija selle loonud kasutajal. See kasutaja on ka vaikimisi projektijuht. Kui projekt on vastendatud mõne sellise müügi olemiga (nt hinnapakkumise või projekti lepinguga), põhineb projekti tellija üksus hoopis müügiüksusel. Sellisel juhul võidakse projekti prognoosid ümber arvutada, kuna kulude hinnakirja kasutatakse hinnanguliste kulu muudatuste arvutamiseks, kui muudetakse tellijat. Müügi hinnakirja abil arvutatakse prognoositavad müügihinnad, mida muudetakse nii, et need oleksid hinnapakkumises oleva projekti hinnakirjaga sünkroonis.

Projekti väljad **Tellijad** ja **Valuuta** on redigeerimiseks suletud, kuna need peavad olema sünkroonitud olemi (hinnapakkumise või projekti leping) väärtustega, millega projekt on vastendatud.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Organisatsiooniüksuste loomine ja haldamine rakenduses Project Operations

Rakenduses Project Operations organisatsiooniüksuse loomiseks järgige neid samme.

1. Minge jaotisse **Sätted \> Organisatsiooniüksused**.
2. Tehke valik **Uus**.
3. Sisestage alale **Üldine** organisatsiooniüksuse väljale **Nimi**. Seejärel määrake teised väljad vastavalt vajadusele.
4. Kirje loomiseks valige **Salvesta**, et saaksite selle redigeerimist jätkata.
5. Valige jaotises **Omahinnakirjad** hinnakirja lisamiseks valikut plussmärk (**+**). Siin saate lisada ainult hinnakirju, millel on **Kulu** kontekst.
6. Klõpsake väljal **Nimi** nuppu **Otsi** ja valige hinnakiri, mida soovite sellele organisatsiooniüksusele kättesaadavaks teha. Vajadusel jätkake hinnakirjade lisamist.
7. Kui olete hinnakirjade lisamise lõpetanud, valige lehe alumises paremas nurgas **Salvesta**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
