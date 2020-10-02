---
title: Tooted
description: Selles teemas antakse teavet tootekataloogi kohta, mida saate kasutada klientidele teie ettevõtte pakutavate toodete ja hinnakujunduse kohta info jagamiseks.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 28397fd49ad4cdb2c820ef4b6f198f410995ba0f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898706"
---
# <a name="products"></a>Tooted

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Tooted on teie ettevõtte selgroog. Tootekataloog rakenduses Dynamics 365 Sales Professional on toodete ja nende hinnateabe kogum. Muutke müügiesindajatele müügitulemuste suurendamine lihtsamaks, luues kiiresti tootekataloogi.

## <a name="add-a-product"></a>Toote lisamine

1.  Veenduge, et teil oleks Sales Manager Professional või süsteemiadministraatori roll, et saaksite Dynamics 365 Sales Professional tooteid lisada.
2.  Valige saidikaardil jaotises **Seadistus** valik **Tooted**.
3.  Valige **Lisa toode** ja täitke järgmised andmed.

    -  **Nimi**
    -  **Toote ID**
    -  **Ema**: valige tootele tootekogumi ematootepere. Kui loote tooteperre alamtoote, lisatakse siia peamise tootepere nimi. Seda ei saa pärast kirje salvestamist muuta.
    -  **Kehtivuse algus**/**Kehtivuse lõpp**: määratlege periood, mille jooksul toode kehtib, valides kuupäevad **Kehtivuse algus** ja **Kehtivuse lõpp**.
    -  **Ühikurühm**: valige ühikurühm. Ühikurühm on mitmesuguste ühikute kogum, milles toodet müüakse, ja määratleb, kuidas eraldi üksusi suuremateks kogusteks rühmitatakse. Näiteks kui lisate tootena seemned, võis teil olla loodud ühikurühm nimega „Seemned” ja selle põhiühikuks määratud „pakk”.
    -  **Vaikeühik**: valige levinuim ühik, milles toodet müüakse. Ühikud on kogused või mõõtühikud, milles tooteid müüte. Näiteks kui lisate tooteks seemned, saate neid müüa pakkide, kastide või kaubaalustena. Iga selline üksus on tooteühik. Kui seemneid müüakse enamasti pakkidena, valige see ühikuks.
    -  **Vaikehinnakiri**: uue toote korral on see väli kirjutuskaitstud. Vaikehinnakirja valimiseks peate esmalt täitma kõik kohustuslikud väljad ja seejärel kirje salvestama. Ehkki see pole kohustuslik, on mõistlik määrata pärast tootekirje salvestamist iga toote jaoks vaikehinnakiri. Kui kliendikirje ei sisalda hinnakirja, saab Sales sel viisil kasutada hinnapakkumiste, tellimuste ja arvete koostamiseks vaikehinnakirja.
    -  **Toetatud kümnendkohad**: sisestage täisarv vahemikus 0–5. Kui toodet ei saa väiksemateks kogusteks jagada, sisestage 0. Välja **Kogus** täpsust hinnapakkumisel, tellimusel või arve toote-/teenuserea kirjel kontrollitakse selle välja väärtuse suhtes, kui tootel puudub seotud hinnakiri.
    -  **Teema**: saate selle toote seostada mõne teemaga. Teemade abil saate tooteid kategoriseerida ja aruandeid filtreerida.

4.  Valige **Salvesta**.
5.  Minge vahekaardile **Täiendavad üksikasjad**, valige jaotises **Hinnakirjaüksused** ikoon **Rohkem käske** ja seejärel valige **Lisa uus hinnakirjaüksus**.
7.  Valige vahekaardil **Täiendavad üksikasjad** jaotises **Toote seos** ikoon **Rohkem käske** ja seejärel valige **Lisa uus toote seos.**
8.  Sisestage vormil **Uus toote seos** järgmised üksikasjad ja valige käsuribal käsk **Salvestaja sule**.

    -   **Seotud toode**: valige toode, mille soovite lisada seostuva tootena olemasolevale tootekirjele, millega töötate.
    -   **Müügiseose tüüp**: valige, kas soovite lisada toote lisamüügi, ristmüügi, tarviku või asendustootena.
    -   **Suund**: valige, kas toodetevaheline seos on ühe- või kahesuunaline. Ühesuunalise valimise korral näidatakse toodet, mille valite jaotisest **Seostatud toode**, olemasoleva toote puhul soovitusena, kuid mitte vastupidi.

9.  Valige toote vormil **Salvesta.**

## <a name="import-products"></a>Impordi tooted

Saate kasutada importimise malle, et tuua hulgi toote andmeid rakendusse Dynamics 365 Sales.

## <a name="revise-a-product"></a>Toote muutmine

Hoidke toodete varud ajakohasena, muutes vajaduse järgi kiiresti toodete atribuute ja avaldades andmed uuesti, et teie müügiesindajad näeksid viimaseid varude muudatusi.

1.  Veenduge, et teil on üks järgmistest turberollidest või sellega võrdväärsed õigused: süsteemiadministraator, süsteemikohandaja, müügijuht, müügi asepresident, turunduse asepresident või peadirektor/ärijuht.
2.  Valige saidikaardil **Tooted**.
3.  Avage aktiivne toode, mida soovite muuta, ja valige käsuribal valik **Muuda**.
4.  Dialoogiboksis **Muutmise kinnitamine** valige suvand **Kinnita**. Selle tulemusena määratakse toote olekuks **Läbivaatusel**.
5.  Kui olete muudatuste tegemise lõpetanud, valige käsuribal **Avalda**.

    > [!TIP]
    > Muudatuste ennistamiseks ja toote viimase aktiivse versiooniga jätkamiseks valige **Ennista.** Seejärel määratakse olekuks uuesti **Aktiivne**.

## <a name="clone-a-product"></a>Toote kloonimine 

Uue toote loomisel saate olemasoleva kloonimisega aega säästa. See loob algsest kirjest koopia kõigi üksikasjadega peale nime ja ID.

1.  Veenduge, et teil on üks järgmistest turberollidest või sellega võrdväärsed õigused: süsteemiadministraator, süsteemikohandaja, müügijuht, müügi asepresident, turunduse asepresident või peadirektor/ärijuht.
2.  Valige saidikaardil **Tooted**.
3.  Valige toote kirje, mida soovite kloonida, ja seejärel valige käsuribalt nupp **Klooni**. Ilmub kinnituse dialoogiboks.
4.  Tehke valik **Kinnita**.

Uus tootekirje avaneb algse kirjega samade üksikasjadega peale nime ja ID.

## <a name="retire-a-product"></a>Toote aegunuks määramine 

Kui teie organisatsioon enam toodet ei müü, määrake see aegunuks, et see enam teie müügiesindajatele kättesaadav poleks.

1.  Veenduge, et teil oleks süsteemiadministraatori või Sales Professional juhi roll või sellega võrdväärsed õigused.
2.  Valige saidikaardil **Tooted**.
3.  Avage aktiivne toode, mida soovite kasutuselt kõrvaldada, ja valige käsuribal valik **Kõrvalda kasutuselt**.
4.  Dialoogiboksis **Aegumise kinnitamine** valige suvand **Kinnita**.


## <a name="delete-a-product"></a>Toote kustutamine

Toote müügi lõpetamiseks kustutage see.

> [!IMPORTANT]
> Kustutatud kirjet ei saa taastada.

1.  Veenduge, et teil oleks süsteemiadministraatori või Sales Professional juhi roll või sellega võrdväärsed õigused.
2.  Valige saidikaardil **Tooted**.
3.  Valige toote kirje, mida soovite kustutada, ja seejärel valige käsuribalt nupp **Kustuta**.
4.  Valige dialoogiboksis **Kinnita kustutamine** nupp **Jätka**.
 
 ## <a name="quantity-factors-for-products"></a>Toodete koguselised tegurid

Koguse faktorid toetavad kordustellimuste põhiste toodete müüki. Kordustellimusel põhinevate toodete puhul väljendatakse hinnapakkumise või projekti lepingurea kogust kasutaja kuude arvuna.

Tavaliselt talletatakse kordustellimuse tarkvara hinda kataloogis ühe kasutaja kuu hinnana. Kuid selle asemel võite kasutada ka muid aja kirjeldusi. Müügiprotsessi jooksul on hind hinnapakkumise real tavaliselt ühe kasutaja hind kuus, mille IT müügiagent oli kokku leppinud ja diskonteerinud. Igal lepingul on erinev arv kasutajaid ja kordustellimuse kuude arv on erinev. Kogus, mida kasutatakse hinnapakkumise rea summa arvutamiseks, on kasutajate arvu ja kordustellimuse kuude arvu toode.

Koguselised tegurid sõltuvad toote atribuutidest. Toote teatud atribuutide konfigureerimisel saate tähistada nende atribuutide alamhulka või kõiki atribuute, näiteks koguselised tegurid.

Süsteem kinnitab, et ainult arvandmed või toote atribuudid, millel on arvuline andmetüüp, märgistatakse koguse tegurina. Kui toode, mille jaoks on konfigureeritud koguselised tegurid, lisatakse hinnapakkumise reale, muutub  hinnapakkumise rea väli **Hinnapakkumine** kirjutuskaitstuks. Pärast koguseid sisaldavatele toote atribuutidele väärtuste sisestamist arvutatakse hinnapakkumise rea kogus.

Näiteks juhul, kui on olemas järgmised atribuudid. 

- **Kasutajate arv**: kasutajate arv 
- **Kuude arv**: kordustellimuse kuude arv
- **Toote SKU** 

Atribuute **Kasutajate arv** ja **Kuude arv** saab märgistada koguse tegurina, redigeerides tootesarja atribuute. 
