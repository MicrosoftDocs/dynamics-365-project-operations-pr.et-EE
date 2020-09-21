---
title: Müügiprotsessid
description: Selles teemas antakse teavet põhiliste müügiprotsessi kohta.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: a169dee5-f4a7-42c8-9bf1-7f0018cc25cb
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: eaaa4b8fe6577ff572489ac0c6abac3c4e970c63
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750978"
---
# <a name="sales-processes"></a>Müügiprotsessid

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektil põhinevas organisatsioonis kasutatavad müügiprotsessid erinevad tootel põhinevas organisatsioonis kasutatavatest müügiprotsessidest. See erinevus ilmneb seetõttu, et projektipõhistele organisatsioonidele mõeldud müügi tsüklid on pikemad ja vajavad kohandatud hindamismeetodeid, et analüüsida ja luua iga tehingu jaoks hinnapakkumisi. Rakendus Dynamics 365 Project Service Automation kasutab mõnda sama funktsiooni, mida kasutatakse rakenduse Dynamics 365 Sales müügiprotsessi jaoks. Järgmiselt on toodud mõned näited.

- Müügivihje olemit kasutatakse müügiprotsessi jälgimiseks.
- Sobivaid müügivihjeid jälgitakse müügivõimalustena. Müügiprotsessi saab alustada ka müügivõimalusest.
- Kõik müügivõimalusega seostuvad artefaktid on kasutusel. Need artefaktid hõlmavad müükide meeskonda, huvirühmi, tõenäosust, hinnangut, müügietappi ja äriprotsesse.
- Müügivõimaluse jaoks luuakse mitu hinnapakkumist.
- Hinnapakkumine märgitakse kui **Suletud võidetuna**, et luua müügitellimus. PSA puhul kohandatakse müügitellimust ja seda nimetatakse projekti lepinguks.

Järgmisel pildil on kujutatud tüüpiline müügiprotsess projektil põhinevas organisatsioonis.

> ![Müügiprotsess projektil põhinevas organisatsioonis](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Müügi hindamine
Müügi väärtust saab hinnata varem tarnitud projektide ja projektide keerukuse alusel. Projektide puhul, mis hõlmavad laiendusi eelmiste projektidega või projektidele, mille puhul tarnija asjatundlikkus on suur ja kasutatakse tuntud töömalle, saate kasutada lihtsamat hindamisprotsessi. Keerulisemate projektide korral on tavaliselt pikem ostuprotsess. Seetõttu on müügi hindamise protsessis rohkem faase. Selle protsessi alguses kasutab müügimeeskond kontohaldurite ja valdkonnaekspertide (SME-d) panust, et hakata koostama kõrgetasemelist hinnangut iga hinnapakkumise töö komponendi kohta. Nende tööde komponente esindavad hinnapakkumise read. 

Hinnapakkumise jaoks saate luua kõrgetasemelise hinnangu. Lõpuks asendatakse see kõrgetasemeline hinnang üksikasjalikuma hinnanguga, mis põhineb projekti plaanil, mille loote standardiseeritud projekti malle kasutades. Need mallid aitavad teil koostada ajakava ning määratleda hinnapakkumise ja selle komponentide rahalised väärtused (hinnapakkumiste read). 

Saate projekti jaoks luua mitu hinnapakkumist ja rühmitada need ühe müügivõimaluse olemi tüübi alla. Lõpuks on üks nendest hinnapakkumistest tähistatud kui **Suletud võidetuna**, ja luuakse projekti leping või tööavaldus (SOW). Projekti lepingus on iga komponendi (lepingurea) jaoks lepinguline väärtus, mille klient on tarnimiseks aktsepteerinud. SOW luuakse tavaliselt rakenduse Microsoft Word dokumendina. Kõik arved, mis saadetakse kliendile projekti tarnimise käigus, viitavad projekti lepingule või SOW-le.

Saate luua ka alternatiivseid hinnapakkumisi ühe müügivõimaluse olemi tüübi alusel või seadistada süsteemi nii, et hinnapakkumise võitmisel luuakse projekti leping. Sel juhul saate projekti lepingu kirjele manustada Wordi dokumendi, esindab SOW-i.

![Hinnapakkumise sulgemine projekti lepingu loomiseks](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Müügiprotsessi konfigureerimine
Äriprotsessi voogusid (BPF-id) saate kasutada rakenduses Microsoft Dynamics 365, et oma müügiprotsessi konfigureerida. BPF-id annavad teie töötajatele juhendava visuaalse liidese, mida nad saavad kasutada, et teisaldada tehinguid edasi teie ettevõtte jaoks tüüpilistes etappides.

Näiteks võivad teie ettevõtte müügiprotsessis olla järgmised kuus etappi.

1. Kinnita sobivaks
2. Hinnang
3. Sisemine läbivaatus
4. Leping
5. Üleandmine
6. Sule

Neid kuut etappi esindavad noolsulud (\>), mille valite iga loodava müügivõimaluse olemi tüübi laiendamiseks.

![Äriprotsessi konfigureerimine rakenduses Dynamics 365](media/basic-guide-3.png)
 
Teie organisatsioon võib sama tehingu kujutamisel kasutada erinevaid olemeid. Müügiprotsessi alguses esindab tehingut müügivõimaluse olem. Aja möödudes ja üksikasjade ilmumisel võite ühe või mitme hinnapakkumise loomiseks kasutada kõrgetasemelisi hinnanguid. Kui ettevõttesisesed ja kliendi huvirühmad vaatavad ühe neist hinnapakkumistest läbi, esindab tehingut hinnapakkumise olem. Pärast seda, kui klient on hinnapakkumise vastu võtnud, esindab tehingut projekti leping või SOW. Selle käitumise toetamiseks on BPF-id struktureeritud nii, et iga protsessi etapp on seotud erineva andmebaasi tabeliga.

Müügiprotsessi etappi **Sobima** saab varundada müügivõimaluse olem. Etappe **Hinnang** ja **Sisemine ülevaatus** saab varundada hinnapakkumise olem. Etappe **Leping**, **Tarne** ja **Sulgemine** saab varundada projekti lepingu olem.

Kui liigutate tehinguid läbi etappide, palutakse teil luua asjakohane olemikirje, mis juhendab teid protsessi läbimisel. Etapid võivad olla tingimuslikud. Näiteks kui vajate hinnapakkumise sisemist ülevaatamist ainult siis, kui hinnapakkumine kasutab kohandatud hinnakirja, saate selle tingimuse konfigureerida äriprotsessi sobivas etapis. Etapp **Sisemine ülevaatus** kuvatakse seejärel ainult nende hinnapakkumiste puhul, mis kasutavad kohandatud hinnakirja. Kõigi muude tehingute ja hinnapakkumiste puhul järgnevad etapid **Hinnang** ja **Leping**.

> [!NOTE]
> Rakenduses PSA on konkreetsed lehed müügivõimaluse, hinnapakkumise, tellimuse ja arve olemite jaoks. Peate nende olemite projekti teabelehtede abil looma Project Service’i müügivõimalused, hinnapakkumised, tellimused ja arved. Kui kasutate kirje loomiseks mõnda muud lehte, ei saa te seda kirjet lehelt **Projekti teave** avada. Kui soovite kirje lehel **Projekti teave** avada, peate kirje kustutama ja looma selle uuesti kasutades lehte **Projekti teave**. Lehel **Projekti teave** on iga olemi tüübi äriloogikas tagatud, et kirje välja **Tüüp** väärtus on seatud õigesti ja kõik kohustuslikud mõisted on õigesti lähtestatud.

> ![Uue tellimuse projekti teave](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Rakenduste Project Service Automation ja Sales erinevused
Kuigi PSA-s kasutatakse müügiprotsessi käigus rakenduses Sales müügiprotsessi põhivõimalusi, on sellel projektipõhiste organisatsioonide äritegevuse erinevuste tõttu mõned olulised erinevused. Järgmiselt on toodud mõned näited.

- **Projekti hinnapakkumised** – rakenduses Project Service Automation suletakse hinnapakkumine pärast projekti lepingu loomist hinnapakkumisest. Rakenduses Sales saate pärast võitmist hinnapakkumise avatuna hoida. Selle erinevuse põhjus on see, et hinnapakkumise ja projekti lepingu sobitamine on projektipõhiste organisatsioonide jaoks parem. 
- **Aktiveerimine ja läbivaatamine** – rakenduses PSA ei toetata projekti hinnapakkumistele aktiveerimist ega läbivaatamisi. Rakenduses Sales saab hinnapakkumise lukustada, et vältida täiendavaid muudatusi.
- **Hinnapakkumise sulgemine kaotatud või võidetud** – kui rakenduses PSA sulgetakse projekti hinnapakkumine kui võidetud või kaotatud, jääb müügivõimalus avatuks. Kõik muud müügivõimaluse hinnapakkumised on suletud kui kaotatud. Rakenduses Sales, kui hinnapakkumine on suletud kui võidetud või kaotatud, on kasutajal võimalus teha müügivõimalusega seotud toiminguid. Olenevalt kasutaja sisestusest võib aluseks olev müügivõimalus olla suletud või avatuks jäänud.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Hinnapakkumiste ja projekti plaanide läbivaatamiste jälgimine müügitsükli jooksul
Rakenduses PSA ei saa jälgida hinnapakkumises tehtud läbivaatamisi. Selle asemel peate märkima, et olemasolev hinnapakkumine on **Suletud kui kaotatud** ja seejärel looma uue hinnapakkumise. Võite kopeerida hinnapakkumise või kloonida projektil põhineva hinnapakkumise, kasutades rakendust PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Hinnapakkumiste ja projekti lepingute kommentaaride ja kinnituste jälgimine
Hinnapakkumiste ja projekti lepingute läbivaatamist ja kinnitamist saate hallata kirje seina ning postituste abil. Teie organisatsioon saab luua kohandatud töövooge ja lisandmooduleid, et määrata, suunata, laiendada ja hallata teatiste läbivaatuse ja kinnitamise tööüksusi.
