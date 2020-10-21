---
title: Müügiprotsesside ülevaade
description: Selles teemas antakse teavet põhiliste müügiprotsessi kohta.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app: ''
ms.openlocfilehash: e66d96a940f3b22d5d1f3372d2b6767a4482d925
ms.sourcegitcommit: 7750485f8685a2ca5e1b3c165ead24a3b583c447
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3891120"
---
# <a name="sales-processes-overview"></a>Müügiprotsesside ülevaade

Projektil põhinevas organisatsioonis kasutatavad müügiprotsessid erinevad tootel põhinevas organisatsioonis kasutatavatest müügiprotsessidest. See ilmneb seetõttu, et projektipõhistele organisatsioonidele mõeldud müügi tsüklid on pikemad ja vajavad kohandatud hindamismeetodeid, et analüüsida ja luua iga tehingu jaoks hinnapakkumisi. Rakendus Dynamics 365 Project Operations kasutab mõnda sama järgmist funktsiooni, mida kasutatakse müügiprotsessi jaoks.

- Müügivihje kirjet kasutatakse müügiprotsessi jälgimiseks.
- Sobivaid müügivihjeid jälgitakse müügivõimalustena.
- Kõik müügivõimalusega seostuvad artefaktid on juurdepääsetavad. Need artefaktid hõlmavad müükide meeskonda, huvirühmi, tõenäosust, hinnangut, müügietappi ja äriprotsesse.
- Müügivõimaluse jaoks luuakse mitu hinnapakkumist.
- Hinnapakkumisele antakse olek **Suletud võidetuna**, et luua müügitellimus. Project Operationsi puhul kohandatakse müügitellimust ja seda nimetatakse projekti lepinguks.

## <a name="estimate-a-sale"></a>Müügi hindamine
Müügi väärtust saab hinnata varem tarnitud projektide ja projektide keerukuse alusel. Projektide puhul, mis hõlmavad laiendusi eelmiste projektidega või projektidele, mille puhul tarnija asjatundlikkus on suur ja kasutatakse tuntud töömalle, saate kasutada lihtsamat hindamisprotsessi. Keerulisemate projektide korral on tavaliselt pikem ostuprotsess. Seetõttu on müügi hindamise protsessis rohkem faase. Selle protsessi alguses kasutab müügimeeskond kontohaldurite ja valdkonnaekspertide (SME-d) panust, et koostada kõrgetasemeline hinnang iga hinnapakkumise töö komponendi kohta. Nende tööde komponente esindavad hinnapakkumise read. 

Hinnapakkumise jaoks saate luua kõrgetasemelise hinnangu. Lõpuks asendatakse see kõrgetasemeline hinnang üksikasjalikuma hinnanguga, mis põhineb projekti plaanil, mille loote standardiseeritud projekti malle kasutades. Need mallid aitavad teil koostada ajakava ning määratleda hinnapakkumise ja selle komponentide rahalised väärtused (hinnapakkumiste read). 

Saate projekti jaoks luua mitu hinnapakkumist ja rühmitada need ühe müügivõimaluse kirje tüübi alla. Lõpuks on üks nendest hinnapakkumistest tähistatud kui **Suletud võidetuna**, ja luuakse projekti leping või tööavaldus (SOW). Projekti lepingus on iga komponendi (lepingurea) jaoks lepinguline väärtus, mille klient on tarnimiseks aktsepteerinud. SOW luuakse tavaliselt rakenduse Microsoft Word dokumendina. Kõik arved, mis saadetakse kliendile projekti tarnimise käigus, viitavad projekti lepingule või SOW-le.

Saate luua ka alternatiivseid hinnapakkumisi ühe müügivõimaluse olemi kirje alusel või seadistada süsteemi nii, et hinnapakkumise võitmisel luuakse projekti leping. Sel juhul saate projekti lepingu kirjele manustada Wordi dokumendi, esindab SOW-i.

## <a name="configure-the-sales-process"></a>Müügiprotsessi konfigureerimine
Äriprotsessi voogusid saate kasutada oma müügiprotsessi konfigureerimiseks. Need vood pakuvad juhendatud visuaalset kasutajaliidest, et viia tehinguid edasi läbi müügiprotsessi etappide.

Näiteks võivad teie ettevõtte müügiprotsessis olla järgmised kuus etappi.

1. Sobivaks kinnitamine
2. Hinnang
3. Sisemine läbivaatus
4. Leping
5. Üleandmine
6. Saate dialoogiakna sulgeda
 
Teie organisatsioon võib sama tehingu kujutamisel kasutada erinevaid olemeid. Müügiprotsessi alguses esindab tehingut müügivõimaluse olem. Aja möödudes ja üksikasjade ilmumisel võite ühe või mitme hinnapakkumise loomiseks kasutada kõrgetasemelisi hinnanguid. Kui ettevõttesisesed ja kliendi huvirühmad vaatavad ühe neist hinnapakkumistest läbi, esindab tehingut hinnapakkumise olem. Pärast seda, kui klient on hinnapakkumise vastu võtnud, esindab tehingut projekti leping või SOW. Selle käitumise toetamiseks on BPF-id struktureeritud nii, et iga protsessi etapp on seotud erineva andmebaasi tabeliga.

Müügiprotsessi etappi **Sobima** saab varundada müügivõimaluse olem. Etappe **Hinnang** ja **Sisemine ülevaatus** saab varundada hinnapakkumise olem. Etappe **Leping**, **Tarne** ja **Sulgemine** saab varundada projekti lepingu olem.

Kui liigutate tehinguid läbi etappide, palutakse teil luua asjakohane olemikirje, mis juhendab teid protsessi läbimisel. Etapid võivad olla tingimuslikud. Näiteks kui vajate hinnapakkumise sisemist ülevaatamist ainult siis, kui hinnapakkumine kasutab kohandatud hinnakirja, saate selle tingimuse konfigureerida äriprotsessi sobivas etapis. Etapp **Sisemine ülevaatus** kuvatakse seejärel ainult nende hinnapakkumiste puhul, mis kasutavad kohandatud hinnakirja. Kõigi muude tehingute ja hinnapakkumiste puhul järgnevad etapid **Hinnang** ja **Leping**.

> [!NOTE]
> Project Operationsil on konkreetsed lehed müügivõimaluse, hinnapakkumise, tellimuse ja arve olemi kirjete jaoks. Need kirjed peate looma nende olemite projekti andmete lehekülgede abil. Vastasel juhul ei saa te kirjeid lehelt **Projekti andmed** avada. Kui soovite kirje avada lehelt **Projekti andmed**, peate kirje kustutama ja looma selle uuesti lehel **Projekti andmed**, kus iga olemi tüübi äriloogika tagab, et kirje väli **Tüüp** on õigesti seadistatud ja kõik kohustuslikud mõisted on õigesti lähtestatud.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Hinnapakkumiste ja projekti plaanide läbivaatamiste jälgimine müügitsükli jooksul
Rakenduses Project Operations ei saa jälgida hinnapakkumises tehtud läbivaatamisi. Selle asemel peate märkima, et olemasolev hinnapakkumine on **Suletud kui kaotatud** ja seejärel looma uue hinnapakkumise. Võite kopeerida hinnapakkumise või kloonida projektil põhineva hinnapakkumise.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Hinnapakkumiste ja projekti lepingute kommentaaride ja kinnituste jälgimine
Hinnapakkumiste ja projekti lepingute läbivaatamist ja kinnitamist saate hallata kirje seina ning postituste abil. Teie organisatsioon saab luua kohandatud töövooge ja lisandmooduleid, et määrata, suunata, laiendada ja hallata teatiste läbivaatuse ja kinnitamise tööüksusi.
