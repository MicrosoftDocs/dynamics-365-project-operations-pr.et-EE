---
title: Organisatsiooniüksused
description: Selles teemas kirjeldatakse organisatsiooniüksuste mõistet ja selgitatakse, kuidas luua ja hallata Organisatsiooniüksusi Microsoftis Dynamics 365 Project Operations.
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
ms.openlocfilehash: 9a8c503dc6286f40c80ed9b7a8a04974ff7e50b4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581371"
---
# <a name="organizational-units-overview"></a>Organisatsiooniüksuste ülevaade

Microsoftis Dynamics 365 Project Operations *on organisatsiooniüksus* professionaalses teenindusettevõttes eraldiseisev rühm või divisjon, mis kasutab arveldatavaid ressursse, millel on omahind.

Professionaalsete teenindusettevõtete jaoks, kes kasutavad tehnilisi ressursse erinevates praktikavaldkondades või ärivaldkondades, võivad rolli täitmise kulud varieeruda sõltuvalt praktikavaldkonnast või ärivaldkonnast, kus roll on täidetud. Selle stsenaariumi puhul aitab organisatsiooniüksuste kontseptsioon, pakkudes võimalust rühmitada arveldatavate rollide kogum ettevõtte divisjonis, millel on nende rollide jaoks selge kulustruktuur.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Organisatsiooniüksuste kontseptsioon Project Operationsis

Project Operationsis on organisatsiooniüksusel kindel valuuta ja konkreetsed omahinnakirjad.

Organisatsiooniüksuse valuuta on esmane valuuta, mida kasutatakse kulude jälgimiseks.

Iga organisatsiooniüksusega saab siduda ühe või mitu kulude hinnakirja. Projektitoimingud seavad organisatsiooniüksusega seostatavatele hinnakirjadele järgmised piirangud.

- Hinnakirjad peavad olema organisatsiooniüksuse valuutas.
- Hinnakirjad peavad olema omahinnakirjad.

Lisaks sisaldab olem Ressurss organisatsiooniüksuse atribuuti. Igale kasutajale saab määrata vaid ühe organisatsiooniüksuse.

### <a name="roles-of-organizational-units"></a>Organisatsiooniüksuste rollid

Organisatsiooniüksusel on Project Operationsis kaks rolli:

- **Tellija** – organisatsiooniüksus, mis esindab ettevõtet või allüksust, kes vastutab peamiselt müügitegevuse ning töö ja teenuste pakkumise eest kliendile. Tellija tuvastatakse väljal **Tellija**, mis asub lehtede **Müügivõimalus**, **Hinnapakkumine**, **Projekti leping** ja **Projekt** päises.
- **Ressursiüksus** – organisatsiooniüksus, millele ressurss kuulub või millesse see on määratud. See organisatsiooniüksus võib pakkuda ressursse töökirjelduse (SOW-d) ja tellija omanduses olevate projektide teatud rollide jaoks.

![Lepingut sõlmivad üksused ja ressursiühikud.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Organisatsiooniüksuse KKK

Siit leiate vastused paljudele korduma kippuvatele küsimustele organisatsiooniüksuste kohta.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Kuidas on olem Organisatsiooniüksus Project Operationsis seotud olemiga Organisatsioon, mis on rakenduses Dynamics 365 juba olemas?

Dynamics 365 olem Organisatsioon tähistab globaalse Dynamics 365 eksemplari nime. Tavaliselt on see globaalse ettevõtte nimi.

Organisatsiooniüksuse olem esindab globaalses ettevõttes rühma või allüksust. Sellel rühmal või allüksusel on nende rollide jaoks rollide komplekt ja hinnakiri ning need rollid ja hinnakirjad erinevad ettevõtte muude rühmade või allüksuste rollidest ja hinnakirjadest.

Kui Project Operations on installitud, luuakse organisatsioonil põhinev vaikeorganisatsiooniüksus. Kõik olemasolevad ressursid määratakse vaikimisi organisatsiooniüksusele. Kui Dynamics 365-sse imporditakse uusi Active Directory kasutajaid või ressursse, määrab kasutaja impordiprotsess need Project Operationsi vaikeorganisatsiooniüksusele.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Mille poolest erineb olem Organisatsiooniüksus olemist Äriüksusest?

Dynamics 365-s on äriüksuse olem turvaline konstruktsioon. Äriüksusega kasutaja ühing määratleb olemid ja olemi kirjed, millele kasutajal on juurdepääs. Samuti määratleb see õigused (loomine, lugemine, kirjutamine, kustutamine, lisamine, lisamine millelegi, määramine või ühiskasutus), mis kasutajal on nende olemi kirjete jaoks.

Organisatsiooniüksus olem esindab ettevõtte rühma või allüksust, millel on sellele määratud töötajate jaoks erinevad kulumäärad. Organisatsiooniüksuse ja ressursi seos määratleb ressursi kulu projektiga seostamiseks.

Kui rakendate Dynamics 365, optimeerige äriüksuste hierarhia jaoks turvakontroll ja kasutajate määramine äriüksustesse. Määrake kõik kasutajad, kes peavad tavaliselt sama äriüksuse samale kirjete komplektile juurde pääsema. Organisatsiooniüksus ei mõjuta turvakontrolli ega juurdepääsu.

**Näide, mis näitab ühte võimalikku erinevust organisatsiooniüksuste ja äriüksuste modelleerimisel**

Jõgi, Ltd.-l on edukas Microsofti tehnoloogia kasutamise kogemus. Marko ja Brita on mõlemad C\# arendajad, kuid Brita asub Ameerika Ühendriikides, samas kui Marko elab Indias. Enamik projekti tegevustest nõuab ressursse nii Contoso Indiast kui ka Contoso USA-st ning Prakash ja Tricia nõuavad sama tasemel turvalisust juurdepääsu projektidele selles tegevusvaldkonnas. Kuid Jõgi India arendajate kulu erineb oluliselt Jõgi USA arendajate kuludest.

Siin on optimaalne viis selle stsenaariumi kujundamiseks Dynamics 365 ja Project Operationsi abil.

1. Looge Microsofti tehnoloogiline tegevus äriüksusena ning seostage sellega Marko ja Brita. Sel viisil aitate tagada, et mõlemal töötajal on sama tasemel turvajuurdepääs kõigile selle praktikavaldkonna projektidele. Mõlemad saavad kontrollida edenemist ja teatada ajast, kuludest, materjalikasutusest ja ülesannete värskendustest.
2. Looge kaks organisatsiooniüksust, mis aitavad tagada projekti maksumuse õige kajastamise.
3. Seostage Triciat Contoso USA ja Prakashiga Contoso Indiaga.
4. Määrake vastavad kulu hinnakirjad mõlemale organisatsiooniüksusele. Sel viisil aitate tagada, et Prakashi ja Tricia projektis registreeritud kulud kajastavad täpselt Contoso USA ja Contoso India kulude erinevust.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Kas organisatsiooniüksused on rakenduses Dynamics 365 seotud müügipiirkondadega?

Müügipiirkondade ja organisatsiooniüksuste vahel pole seoseid ega suhteid. Müügipiirkond on tavaliselt geograafiline ala, kus müük aset leiab. Müügi hinnakirja saab seostada iga müügipiirkonnaga.

Organisatsiooniüksus on ettevõtte sisemine rühm või allüksus, mis jälgib teatud rollide kulusid, mis on seotud müügiga teistele allüksustele või välistele klientidele.

**Näide, mis näitab ühte võimalikku erinevust organisatsiooniüksuste ja müügiterritooriumide modelleerimisel**

Jõgi, Ltd.-l on kaks arenduskeskust: Jõgi USA ja Jõgi India. Ressursside maksumus on nende kahe arenduskeskuse vahel väga erinev. Contoso müüb oma infotehnoloogia (IT) teenuseid paljudel rahvusvahelistel turgudel, näiteks Ladina-Ameerikas, Põhja-Ameerikas, Aasia ja Vaikse ookeani piirkonnas, Lääne-Euroopas ja Lähis-Idas. Sama projekti rollide arveldusmäärad võivad nendel turgudel olla väga erinevad. Jõgi USA ja Jõgi India tuleks seadistada organisatsiooniüksustena ja igal organisatsiooniüksusel peaks olema oma kulude hinnakiri. Aasia ja Vaikse ookeani piirkond, Ladina-Ameerika, Põhja-Ameerika, Lääne-Euroopa ja Lähis-Ida tuleks seadistada müügipiirkondade järgi ja igal müügipiirkonnal peaks olema oma müügi hinnakiri.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Miks on hinnakirja ja organisatsiooniüksuse seostamisel piirangud?

Müügihinnad on tavaliselt kordumatud geograafiliste piirkondade või turgude jaoks, kus teenuseid müüakse. Ettevõtte sisemistel allüksustel ei ole tavaliselt omaenda müügihindasid sama tüüpi teenuste jaoks. Kuid sisemistel allüksustel on erinev müüdud kaupade kulu (omahinnad), olenevalt sellest, millised on nende töötajate oskused ja töötingimused selles piirkonnas, kus nad töötavad. Kuna organisatsiooniüksused on kujundatud ettevõtte sisemiste allüksustena, võivad neil olla ainult kulu hinnakirjad.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Miks me ei saa seostada müügihinnakirju organisatsiooniüksustega?

Project Operationsis saab müügihinnakirju seostada klientide ja müügiterritooriumidega. Tehinguolemid nagu Müügivõimalus, Pakkumine, Projektileping ja Projekt kasutavad kliendikontole või müügiterritooriumile lisatud müügihinnakirju, et määrata projekti töövõtu arvemäärad ja potentsiaalne tulu.

Kulu hinnakirjad on seostatud organisatsiooniüksustega. Tehinguolemid (nt Müügivõimalus, Pakkumine, Projektileping ja Projekt) kasutavad projektitöö kulude määramiseks lepinguüksusega seotud omahinnakirju.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Kas organisatsiooniüksused on Project Operationsis hierarhistlikud?

Ei. Praeguses Project Operationsi väljaandes pole organisatsiooniüksused hierarhaatilised. Seetõttu ei saa te teha järgmisi toiminguid.

- Konfigureerige hierarhiat läbivate vaikeomahindade sisestamise muster.
- Aruande tulu või kulu, mis on ümber kujundatud organisatsiooniüksuse hierarhia erinevatel tasanditel.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Oleme suur rahvusvaheline ettevõte, millel on keeruline, mitmetasandiline kulukeskuste, osakondade ja arvelduskontorite hierarhia. Kuidas saame kõige paremini kasutada organisatsiooniüksuste kontseptsiooni Project Operationsi praeguses versioonis?

Kui teil on keeruline kulukeskuste, osakondade, arvelduskontorite hierarhia jne, seadistage selle hierarhia lehesõlmed eraldi organisatsiooniüksustena.

Järgmises näites on kujutatud tüüpiline hierarhia.

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

Kui teie hierarhia sarnaneb selle näitega, peate selle seadistama lameda loendina, nagu on näidatud siin.

- Jõgi India – SAP-praktika – tehnilised konsultandid
- Jõgi India – SAP-praktika – funktsionaalsed konsultandid
- Jõgi India – Microsofti tehnoloogiapraktika funktsionaalsed konsultandid
- Jõgi India – Microsofti tehnoloogiapraktika funktsionaalsed konsultandid
- Jõgi USA – SAP-praktika – tehnilised konsultandid
- Jõgi USA – SAP-praktika – funktsionaalsed konsultandid
- Jõgi USA – Microsofti tehnoloogiapraktika tehnilised konsultandid
- Jõgi USA – Microsofti tehnoloogiapraktika funktsionaalsed konsultandid

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Me oleme väike professionaalne teenindusettevõte, mis tegutseb ainult ühe allüksusena. Kuidas saame kõige paremini kasutada organisatsiooniüksuste kontseptsiooni Project Operationsi praeguses versioonis?

Kui teie ettevõte tegutseb ühe üksusena, millel on üks kulude hinnakiri, ei pea te organisatsiooniüksusi seadistama. Project Operationsi installimine loob ühe vaikeorganisatsiooniüksuse, millel on organisatsiooniga sama nimi. Kõik olemasolevad ressursid määratakse vaikimisi organisatsiooniüksusele. Iga kord, kui süsteem nõuab, et valitaks organisatsiooniüksus, valitakse vaikimisi organisatsiooniüksus.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Kui projekt luuakse hinnapakkumise või projekti lepingurea põhjal, tuleneb vaiketellija hinnapakkumisest või projekti lepingust. Mis on vaikelepingu üksus, kui projekt luuakse enne müügiolemeid (nt Pakkumine või Projektileping) ?

Kui projekt luuakse eraldi, põhineb projekti vaiketellija selle loonud kasutajal. See kasutaja on ka vaikimisi projektijuht. Kui projekt vastendatakse müügiolemiga (nt hinnapakkumise või projektilepinguga), põhineb projekti lepinguüksus hoopis müügiolemil. Sellisel juhul võidakse projekti prognoosid ümber arvutada, kuna kulude hinnakirja kasutatakse hinnanguliste kulu muudatuste arvutamiseks, kui muudetakse tellijat. Müügihinnakirja kasutatakse muudetavate müügiprognooside arvutamiseks nii, et need oleksid kooskõlas hinnapakkumise projekti hinnakirjaga.

Projekti **väljad Lepinguühik** ja **Valuuta** on redigeerimiseks lukustatud, kuna need peavad olema sünkroonis selle müügiolemi (pakkumine või projektileping) väärtustega, millega projekt vastendatakse.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Organisatsiooniüksuste loomine ja haldamine Project Operationsis

Organisatsiooniüksuse loomiseks Project Operationsis tehke järgmist.

1. **Avage sätted \> Organisatsiooniüksuste üksus.**
2. Tehke valik **Uus**.
3. Sisestage ala Üldine **väljale** **Nimi** organisatsiooniüksuse nimi. Seejärel seadke teised väljad vastavalt vajadusele.
4. Kirje loomiseks valige **Salvesta**, et saaksite selle redigeerimist jätkata.
5. Hinnakirja lisamiseks valige jaotises **Omahinnakirjad** plussmärk (**+**). Siia saate lisada ainult hinnakirjad, millel on **kulukontekst**.
6. Valige väljal **Nimi** **nupp Otsing** ja valige hinnakiri, mille soovite organisatsiooniüksusele kättesaadavaks teha. Jätkake hinnakirjade lisamist vastavalt vajadusele.
7. Kui olete hinnakirjade lisamise lõpetanud, valige lehe paremas allnurgas **Salvesta**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
