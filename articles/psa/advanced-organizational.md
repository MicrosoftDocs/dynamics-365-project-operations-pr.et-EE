---
title: Organisatsiooniüksused
description: Selles teemas antakse teavet rakenduses Dynamics 365 Project Service Automation organisatsiooniliste üksuste kohta.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.openlocfilehash: 3be18adfa1d346bdabae7e89375ca2c5a2dbda95
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009611"
---
# <a name="organizational-units"></a>Organisatsiooniüksused 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Rakenduse Dynamics 365 Project Service Automation mõistes on organisatsiooniüksus professionaalse teenusettevõtte eraldiseisev rühm või allüksus, kus on tasutatavad töötajad, kellel on kulumäärad.

Professionaalsetele teenusettevõtetele, kes kasutavad tehnilisi ressursse erinevates tegevus- või ettevõtlusvaldkondades, võib ühe tegevus- või ettevõtlusvaldkonna kuluroll erineda teise tegevus- või ettevõtlusvaldkonna kulurollist. Selle stsenaariumi puhul on abi organisatsiooniüksuste kontseptsioonist, mis pakub võimaluse rühmitada arveldatavad rollid ettevõtte allüksuse jaoks, millel on nende rollide jaoks eraldi kulustruktuur.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Organisatsiooniüksuste põhiatribuudid ja seosed

PSA puhul: PSA-s on organisatsiooniüksusel kindel valuuta ja kulude hinnakiri.

Organisatsiooniüksuse valuuta on esmane valuuta, mida kasutatakse kulude jälgimiseks.

Iga organisatsiooniüksusega saab siduda ühe või mitu kulude hinnakirja. PSA seab organisatsiooniüksusele lisatavale hinnakirjale järgmised piirangud.

- Hinnakirjad peavad olema organisatsiooniüksuse valuutas.
- Hinnakirjad peavad olema kulude hinnakirjad.

Lisaks on ressursi olemi organisatsiooniüksuse jaoks olemas atribuut. Igale kasutajale saab määrata vaid ühe organisatsiooniüksuse.

## <a name="roles-of-organizational-units"></a>Organisatsiooniüksuste rollid

Organisatsiooniüksusel on PSA-s kaks rolli.

- **Tellija** – organisatsiooniüksus, mis esindab ettevõtet või allüksust, kes vastutab peamiselt müügitegevuse ning töö ja teenuste pakkumise eest kliendile. Tellija tuvastatakse väljal **Tellija**, mis asub lehtede **Müügivõimalus**, **Hinnapakkumine**, **Projekti leping** ja **Projekt** päises.
- **Ressursiüksus** – organisatsiooniüksus, millele ressurss kuulub või millesse see on määratud. See organisatsiooniüksus võib pakkuda ressursse töökirjelduse (SOW-d) ja tellija omanduses olevate projektide teatud rollide jaoks.

> ![Tellijad ja ressursiüksused](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Organisatsiooniüksuste KKK

Siit leiate vastused paljudele korduma kippuvatele küsimustele organisatsiooniüksuste kohta.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Kuidas on PSA organisatsiooniüksuse olem seotud Dynamics 365-s juba olemas oleva organisatsiooni olemiga?

Microsoft Dynamics 365 organisatsiooni olem tähistab globaalse Dynamics 365 eksemplari nime. Tavaliselt on see globaalse ettevõtte nimi.

Organisatsiooniüksuse olem esindab globaalses ettevõttes rühma või allüksust. Sellel rühmal või allüksusel on nende rollide jaoks rollide komplekt ja hinnakiri ning need rollid ja hinnakirjad erinevad ettevõtte muude rühmade või allüksuste rollidest ja hinnakirjadest.

Kui PSA on installitud, luuakse organisatsiooni põhjal vaikimisi organisatsiooniüksus. Kõik olemasolevad ressursid määratakse vaikimisi organisatsiooniüksusele. Kui rakendusse Dynamics 365 imporditakse uusi Active Directory kasutajaid või ressursse, määrab kasutaja importimise protsess need vaikimisi PSA-s kasutatavale organisatsiooniüksusele.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Kuidas organisatsiooniüksuse olem erineb äriüksuse olemist?

Dynamics 365-s on äriüksuse olem turvaline konstruktsioon. Äriüksusega kasutaja ühing määratleb olemid ja olemi kirjed, millele kasutajal on juurdepääs. Samuti määratleb see õigused (loomine, lugemine, kirjutamine, kustutamine, lisamine, lisamine millelegi, määramine või ühiskasutus), mis kasutajal on nende olemi kirjete jaoks.

Organisatsiooniüksus olem esindab ettevõtte rühma või allüksust, millel on sellele määratud töötajate jaoks erinevad kulumäärad. Organisatsiooniüksuse ja ressursi seos määratleb ressursi kulu projektiga seostamiseks.

Kui rakendate Dynamics 365, optimeerige äriüksuste hierarhia jaoks turvakontroll ja kasutajate määramine äriüksustesse. Määrake kõik kasutajad, kes peavad tavaliselt sama äriüksuse samale kirjete komplektile juurde pääsema. Organisatsiooniüksus ei mõjuta turvakontrolli ega juurdepääsu.

#### <a name="example-of-organizational-units-and-business-units"></a>Organisatsiooni- ja äriüksuste näide

Contoso, Ltd.-l on edukas Microsofti tehnoloogia kasutamise kogemus. Marko ja Brita on mõlemad C\# arendajad, kuid Brita asub Ameerika Ühendriikides, samas kui Marko elab Indias. Kuna enamike projektide puhul on osalemiseks vaja nii Contoso India kui ka Contoso USA ressursse ning Prakash ja Tricia vajavad sama turvataset, et selle tegevusala projektidele juurde pääseda. Kuid Contoso India arendajate kulu erineb oluliselt Contoso USA arendajate kuludest.

Siin on optimaalne viis selle stsenaariumi kujundamiseks Dynamics 365 ja PSA abil.

1. Looge Microsofti tehnoloogiline tegevus äriüksusena ning seostage sellega Marko ja Brita. Sel viisil tagate, et mõlemal töötajal oleks sama turvatase, et kõigile selle ala projektidele juurde pääseda. Mõlemal on võimalik kontrollida edenemist ning aruande aega, kulusid ja tööülesannete värskendusi. 
2. Looge kaks organisatsiooniüksust, et tagada projekti kulu õigesti kajastamine. 
3. Seostage Tricia Contoso USA-ga ja Prakash Contoso Indiaga.
4. Määrake vastavad kulu hinnakirjad mõlemale organisatsiooniüksusele. Nii saate tagada, et Prakashi ja Tricia projektile kirjendatud kulud kajastaksid täpselt Contoso USA ja Contoso India vahelise erinevuse kulusid.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Kas organisatsiooniüksused on rakenduses Dynamics 365 seotud müügipiirkondadega?

Müügipiirkondade ja organisatsiooniüksuste vahel pole seoseid ega suhteid. Müügipiirkond on tavaliselt geograafiline ala, kus müük aset leiab. Müügi hinnakirja saab seostada iga müügipiirkonnaga.

Organisatsiooniüksus on ettevõtte sisemine rühm või allüksus, mis jälgib teatud rollide kulusid, mis on seotud müügiga teistele allüksustele või välistele klientidele.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Organisatsiooniüksuste ja müügipiirkondade näide

Contoso, Ltd.-l on kaks arenduskeskust: Contoso USA ja Contoso India. Nende kahe arenduskeskuse ressursside kulu on väga erinev.

Contoso müüb oma IT-teenuseid paljudel rahvusvahelistel turgudel, nagu Ladina-Ameerika, Põhja-Ameerika, Aasia ja Vaikse ookeani piirkond, Lääne-Euroopa ja Lähis-Idas. Sama projekti rollide arveldusmäärad võivad nendel turgudel olla väga erinevad.

Contoso USA ja Contoso India tuleks häälestada organisatsiooniüksustena ja igal organisatsiooniüksusel peaks olema oma kulude hinnakiri. Aasia ja Vaikse ookeani piirkond, Ladina-Ameerika, Põhja-Ameerika, Lääne-Euroopa ja Lähis-Ida tuleks seadistada müügipiirkondade järgi ja igal müügipiirkonnal peaks olema oma müügi hinnakiri.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Miks on hinnakirja ja organisatsiooniüksuse seostamisel piirangud? 

Müügihinnad on tavaliselt kordumatud geograafiliste piirkondade või turgude jaoks, kus teenuseid müüakse. Ettevõtte sisemistel allüksustel ei ole tavaliselt omaenda müügihindasid sama tüüpi teenuste jaoks. Kuid sisemistel allüksustel on erinev müüdud kaupade kulu (omahinnad), olenevalt sellest, millised on nende töötajate oskused ja töötingimused selles piirkonnas, kus nad töötavad. Kuna organisatsiooniüksused on kujundatud ettevõtte sisemiste allüksustena, võivad neil olla ainult kulu hinnakirjad.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Miks me ei saa müügi hinnakirja seostada organisatsiooniüksustega?

PSA-s saab müügi hinnakirju seostada klientide ja müügipiirkondadega. Tehingute olemid, nagu müügivõimalus, hinnapakkumine, projekti leping ja projektipõhised müügi hinnakirjad, mis on lisatud kliendikontole või müügipiirkonnale, et määratleda arveldusmäärad ja potentsiaalne tulu projektiga seotusest.

Kulu hinnakirjad on seostatud organisatsiooniüksustega. Tehingute olemid, nagu müügivõimalus, hinnapakkumine, projekti leping ja projektipõhised müügi hinnakirjad, mis on lisatud tellijale, et määratleda projektiga seotuse kulu.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Kas organisatsiooniüksused on PSA-a hierarhilised?

Ei. Praeguses PSA väljaandes ei ole organisatsiooniüksused hierarhilised. See tähendab, et te ei saa teha järgmist.

- Konfigureerida mustrit, mis on seotud hierarhiat ületavate kulude vaikeväärtusega. 
- Esitada tulu või kulu ümberarvestuse aruandeid organisatsiooniüksuse hierarhia erinevatel tasemetel.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Oleme suur rahvusvaheline ettevõte, millel on keerukas mitmetasandiline hierarhia kulukeskuste, allüksuste ja arvete osakondade jaoks. Kuidas saaksime rakenduse Project Service seda versiooni organisatsiooniüksuste seisukohast parimal võimalikul viisil kasutada?

Kui teil on kulukeskuste, allüksuste, arvete osakondade jne keerukas hierarhia, seadistage selle hierarhia lehed eraldiseisvate organisatsiooniüksustena.
Järgmine näide illustreerib tüüpilist hierarhiat.

**ContosoIndia**

  - SAP-praktika 

    - Tehnilised konsultandid 
    - Funktsionaalsed konsultandid 
    
  - Microsofti tehnoloogiapraktika 

    - Tehnilised konsultandid
    - Funktsionaalsed konsultandid 
    
**Contoso USA**

 - SAP-praktika 

    - Tehnilised konsultandid 
    - Funktsionaalsed konsultandid 
    
 - Microsofti tehnoloogiapraktika 

    - Tehnilised konsultandid 
    - Funktsionaalsed konsultandid 
 
Kui teie hierarhia on sarnane, peate selle seadistama lameda loendina, nagu siin näidatud.
- Contoso India – SAP-praktika – tehnilised konsultandid 
- Contoso India – SAP-praktika – funktsionaalsed konsultandid       
- Contoso India – Microsofti tehnoloogiapraktika funktsionaalsed konsultandid 
- Contoso India – Microsofti tehnoloogiapraktika funktsionaalsed konsultandid 
- Contoso USA – SAP-praktika – tehnilised konsultandid  
- Contoso USA – SAP-praktika – funktsionaalsed konsultandid  
- Contoso USA – Microsofti tehnoloogiapraktika tehnilised konsultandid 
- Contoso USA – Microsofti tehnoloogiapraktika – tehnilised konsultandid

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Me oleme väike professionaalne teenindusettevõte, mis tegutseb ainult ühe allüksusena. Kuidas saaksime PSA praegust versiooni organisatsiooniüksuste seisukohast parimal võimalikul viisil kasutada?

Kui teie ettevõte tegutseb ühe üksusena, millel on üks kulude hinnakiri, ei pea te organisatsiooniüksusi seadistama. PSA installimise ajal loob Dynamics 365 ühe vaikimisi organisatsiooniüksuse, millel on organisatsiooniga sama nimi. Kõik olemasolevad ressursid määratakse vaikimisi organisatsiooniüksusele. Iga kord, kui süsteem nõuab, et valitaks organisatsiooniüksus, valitakse vaikimisi organisatsiooniüksus.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Kui projekt luuakse hinnapakkumise või projekti lepingurea põhjal, tuleneb vaiketellija hinnapakkumisest või projekti lepingust. Mis on vaiketellijaks, kui projekt luuakse enne müügi olemeid (nt hinnapakkumise või projekti leping)?

Kui projekt luuakse eraldi, põhineb projekti vaiketellija selle loonud kasutajal. See kasutaja on ka vaikimisi projektijuht. Kui projekt on vastendatud mõne sellise müügi olemiga (nt hinnapakkumise või projekti lepinguga), põhineb projekti tellija selle asemel müügi olemil. Sellisel juhul võidakse projekti prognoosid ümber arvutada, kuna kulude hinnakirja kasutatakse hinnanguliste kulu muudatuste arvutamiseks, kui muudetakse tellijat. Hinnakirja abil arvutatakse prognoositavad müügihinnad, mida muudetakse nii, et need oleksid hinnapakkumises oleva projekti hinnakirjaga sünkroonis.

Projekti väljad **Tellijad** ja **Valuuta** on redigeerimiseks suletud, kuna need peavad olema sünkroonitud olemi (hinnapakkumise või projekti leping) väärtustega, millega projekt on vastendatud.


[!INCLUDE[footer-include](../includes/footer-banner.md)]