---
title: Projektimalli loomine
description: Projektimalli loomine Project Service'is
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 07/19/2022
ms.topic: article
ms.author: ruhercul
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
ms.openlocfilehash: 8159e0390441e5029f9beb0228cffcbc4d683479
ms.sourcegitcommit: 278740b352f1ed9618ee5c79597c8f449984d6f4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177420"
---
# <a name="create-a-project-template-project-service"></a>Projektimalli loomine (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projektimallid säästavad teie aega, kui ettevõte teeb regulaarselt pakkumisi sarnast tüüpi projektidele. Need pakuvad projekti tüübi puhul standardset rollikomplekti ja hinnangulist tundide arvu. Kontohaldurid ja projektijuhid saavad luua projektimalli alusel projekte või kopeerida malli ja luua enda oma.  
  
## <a name="components-of-project-template"></a>Projektimalli komponendid
 Projektimall koosneb kolmest osast.  
  
- **Tööjaotuse struktuur**: projektimalli tööjaotuse struktuur sisaldab sama elemendikomplekti mis projekt. Saate luua ülesandehierarhia, seostada rollid ülesandega, määratleda ajakava atribuute, seada sõltuvusi ja vaadata kõiki Ganttis olevaid andmeid. Projektimallide tööjaotuse struktuur toetab ka iga ülesande ülesanderežiime. Töögraafiku loomisel ei ole projektimalli ja projekti vahel vahet.  
  
- **Projektiprognoosid**: mallide projektiprognoosid toimivad samal moel, nagu projektides, välja arvatud see, et hinnakirjad oma- ja müügihindade vaikeväärtuste määramiseks on alati funktsiooni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameetrites määratletud omahinna ja müügihinna vaikehinnakirjad. Ülejäänud funktsioonid on samad mis projektis.  
  
- **Projektimeeskonna moodustamine**: projektimalli jaoks projektimeeskonna moodustamisel ei saa mallis broneerida nimelist ressurssi. Saate kasutada tööjaotuse struktuuris olevat valikut **Projektimeeskonna loomine**, et luua üldiste ressursside kogum. Saate ka määrata üldiste ressursside puhul nõutavad oskused ja pädevused. Projektimallides ei saa üldist ressurssi asendada reserveeritava ressursiga.  

## <a name="create-a-project-template-from-an-existing-project"></a>Projektimalli loomine olemasolevast projektist
Projektimalli saate luua projektist järgmistel viisidel.

- **Tööjaotuse struktuur**: projektist tuletatud malli tööjaotuse struktuur kopeerib kõik ülesanded ja sõltuvused. Loodud ülesanded põhinevad üldistel meeskonnaliikmetel, kes lisatakse projektimeeskonnale projektimalli loomisel.
- **Projekti prognoosid**: kui olemasolevast projektist luuakse projektimall, kopeeritakse lähteprojekti prognoosid projektimalli.
- **Projektimeeskonna liikmed**: kui olemasolevast projektist luuakse mall, asendatakse kõik nimega meeskonnaliikmed organisatsiooni üldise ressursiga. Kõik ametikohtade nimed ja rollid säilitatakse.

## <a name="create-a-project-from-a-template"></a>Projekti loomine mallist  
 Mallist saate projekti luua järgmistel viisidel.  
  
-   Projekti loomisel hinnapakkumisest saate valida projektimalli projekti kiirloomise vormil.  
  
-   Projekti loomisel, klõpsates valikut **Uus projekt**, kuvatakse enne kirje salvestamist projektivorm. Siin saate klõpsata välja **Valige mall**, et valida soovitud mall teie organisatsioonis eelmääratletud projektimallide loendist.  
  
-   Klõpsake lehel **Projektimall** valikut **Projekti loomine mallist**, et luua projekt mallist.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Malli komponentide kopeerimine projekti.  
 Malli komponentide kopeerimisel projekti peate teadma järgmist.  
  
 **Tööjaotuse struktuuri kopeerimine**: kui kopeerite projektimallist tööjaotuse struktuuri ja projektil on mallist erinev kalender, rakendatakse ülesannete ajakavale projekti kalendrist pärit töötunnid. See kohandab ajakava projekti varukalendri järgi. Samamoodi rakendub tööjaotuse struktuuri esimesele ülesandele projekti alguskuupäev, nii et ülesandehierarhia ajakava ülejäänud osa värskendatakse malli tööjaotuse struktuuris määratud kestuse ja sõltuvuste põhjal.  
  
 **Projektiprognooside kopeerimine**: kui kopeerite kogu projektiprognoosi ridade ulatuses, värskendatakse hinnakirju omahinnakirja puhul projekti omanikust üksuse põhjal ja müügihinnakirja puhul kliendi põhjal. Ühiku omahind ja müügihind määratakse nende hinnakirjade põhjal müügiüksusega seostatud projektidele.  
  
 **Projektimeeskonna kopeerimine**: projektimeeskonna kopeerimisel mallist projekti kopeeritakse üldised ressursid koos mallis määratletud oskuste ja pädevustega. Säilitatakse ka üldised ressursimäärangud, nagu need on projektimallis.  
  
### <a name="see-also"></a>Vt ka  
 [Projektijuhi juhend](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
