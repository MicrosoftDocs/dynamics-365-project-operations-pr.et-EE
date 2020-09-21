---
title: Projektimalli loomine
description: Projektimalli loomine Project Service'is
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ba15d6d5-a43b-456a-9488-db6e92023fa1
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 50e12d65d5ed957565485413490b8d9f0e2f47ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750924"
---
# <a name="create-a-project-template-project-service"></a>Projektimalli loomine (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projektimallid säästavad teie aega, kui ettevõte teeb regulaarselt pakkumisi sarnast tüüpi projektidele. Need pakuvad projekti tüübi puhul standardset rollikomplekti ja hinnangulist tundide arvu. Kontohaldurid ja projektijuhid saavad luua projektimalli alusel projekte või kopeerida malli ja luua enda oma.  
  
## <a name="components-of-project-template"></a>Projektimalli komponendid
 Projektimall koosneb kolmest osast.  
  
- **Tööjaotuse struktuur**: projektimalli tööjaotuse struktuur sisaldab sama elemendikomplekti mis projekt. Saate luua ülesannete hierarhia, seostada rolle ülesandega, määratleda ajakava atribuute, määrata sõltuvusi ja kuvada kõik andmed Gantti diagrammil. Projektimallide tööjaotuse struktuur toetab ka iga ülesande puhul ülesanderežiime. Projektimalli ja projekti vahel pole töö ajakava loomisel mingit erinevust.  
  
- **Projektiprognoosid**: mallide projektiprognoosid toimivad samal moel, nagu projektides, välja arvatud see, et hinnakirjad oma- ja müügihindade vaikeväärtuste määramiseks on alati funktsiooni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameetrites määratletud omahinna ja müügihinna vaikehinnakirjad. Ülejäänud funktsioonid on samad mis projektis.  
  
- **Projektimeeskonna moodustamine**: projektimalli jaoks projektimeeskonna moodustamisel ei saa mallis broneerida nimelist ressurssi. Saate kasutada tööjaotuse struktuuris olevat valikut **Projektimeeskonna loomine**, et luua üldiste ressursside kogum. Saate ka määrata üldiste ressursside puhul nõutavad oskused ja pädevused. Projektimallides ei saa üldist ressurssi asendada reserveeritava ressursiga.  
  
## <a name="create-a-project-from-a-template"></a>Projekti loomine mallist  
 Malli põhjal projekti loomiseks on järgmised võimalused.  
  
-   Projekti loomisel hinnapakkumisest saate valida projektimalli projekti kiirloomise vormil.  
  
-   Projekti loomisel, klõpsates valikut **Uus projekt**, kuvatakse enne kirje salvestamist projektivorm. Siin saate klõpsata välja **Valige mall**, et valida soovitud mall teie organisatsioonis eelmääratletud projektimallide loendist.  
  
-   Klõpsake lehel **Projektimall** valikut **Projekti loomine mallist**, et luua projekt mallist.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Malli komponentide kopeerimine projekti.  
 Malli komponentide kopeerimisel projekti peate teadma järgmist.  
  
 **Tööjaotuse struktuuri kopeerimine**: kui kopeerite projektimallist tööjaotuse struktuuri ja projektil on mallist erinev kalender, rakendatakse ülesannete ajakavale projekti kalendrist pärit töötunnid. See kohandab ajakava projekti varukalendri järgi. Samamoodi rakendub tööjaotuse struktuuri esimesele ülesandele projekti alguskuupäev, nii et ülesandehierarhia ajakava ülejäänud osa värskendatakse malli tööjaotuse struktuuris määratud kestuse ja sõltuvuste põhjal.  
  
 **Projektiprognooside kopeerimine**: kui kopeerite kogu projektiprognoosi ridade ulatuses, värskendatakse hinnakirju omahinnakirja puhul projekti omanikust üksuse põhjal ja müügihinnakirja puhul kliendi põhjal. Ühiku omahind ja müügihind määratakse nende hinnakirjade põhjal müügiüksusega seostatud projektidele.  
  
 **Projektimeeskonna kopeerimine**: projektimeeskonna kopeerimisel mallist projekti kopeeritakse üldised ressursid koos mallis määratletud oskuste ja pädevustega. Säilitatakse ka üldised ressursimäärangud, nagu need on projektimallis.  
  
### <a name="see-also"></a>Vt ka  
 [Projektijuhi juhend](../project-service/project-manager-guide.md)
