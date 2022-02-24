---
title: Täienduse kaalutlused – üleminek Microsoft Dynamics 365 Project Service Automationi versioonilt 2.x või 1.x versioonile 3
description: Selles teemas antakse teavet kaalutluste kohta, mida peate tegema, kui täiendate Project Service Automationi versiooni 2.x või 1.x versioonile 3.
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c0c1e07bacb4867254a12436cf3bff58989e117f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144152"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Täienduse kaalutlused – üleminek PSA versioonilt 2.x või 1.x versioonile 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation ja Field Service
Nii Dynamics 365 Project Service Automation kui ka Dynamics 365 Field Service kasutavad ressursside ajastamiseks lahendust Universal Resourcing Scheduling (URS). Kui teie eksemplaris on Project Service Automation ja Field Service, värskendage mõlemad lahendused uusimale versioonile. Project Service Automationi puhul on see versioon 3.x. Field Service'i puhul on see versioon 8.x. Project Service Automationi või Field Service'i täiendamisega installitakse uusim URS-i versioon. Kui samas eksemplaris ei uuendata nii Project Service Automationi kui ka Field Service'i uusimatele versioonidele, võib ilmneda vastuolulist käitumist.

## <a name="resource-assignments"></a>Ressursimääramised
Project Service Automation versioonis 2 ja 1 salvestati ülesanded **Ülesande olemis** tütarülesannetena (ehk rea ülesannetena) ning need olid kaudselt seotud olemiga **Ressursi määramine**. Rea ülesanne oli nähtav tööjaotuse struktuuril (WBS) määramise hüpikaknas.

![Reaülesanded WBS-is Project Service Automationi versioonis 2 ja versioonis 1](media/upgrade-line-task-01.png)

Project Service Automationi versioonis 3 on muutunud skeem, mille alusel määratakse broneeritavaid ressursse ülesannetele. Rea ülesanne on iganenud ning olemis **Ülesanne** oleva ülesande ja olemis **Ressursi määramine** oleva meeskonnaliikme vahel on otsene 1:1 suhe. Projekti meeskonnaliikmetele määratud ülesanded salvestatakse nüüd otse olemisse Ressursi määramine.  

Need muudatused mõjutavad kõikide nende olemasolevate projektide täiendamist, millel on projekti meeskonnas ressursi määramised nimega broneeritavate ressursside ja üldiste ressursside jaoks. Selles teemas on välja toodud kaalutlused, mida peate oma projektidega seoses arvesse võtma, kui täiendate versioonile 3. 

### <a name="tasks-assigned-to-named-resources"></a>Nimega ressurssidele määratud ülesanded
Kui kasutate aluseks olevat ülesande olemit, võimaldavad versioonis 2 ja 1 olevad ülesanded meeskonnaliikmetele määrata muid rolle kui neile määratud vaikerollid. Näiteks Heidi Kukk, kellele on vaikimisi määratud programmihalduri roll, saab määrata ka arendaja rolli. Versioonis 3 on nimega meeskonnaliikme roll alati vaikeroll, seega kõigi ülesannete puhul, millele Heidi Kukk määratakse, kasutatakse tema programmihalduri vaikerolli.

Kui olete määranud ressursi ülesandele, mis ei kuulu versioonis 2 ja 1 tema vaikerolli alla, määratakse täiendamise käigus nimega ressursile vaikeroll kõigi ülesannete määramiste jaoks, olenemata versioonis 2 määratud rollist. Selle määramise tõttu erinevad väljaarvutatud prognoosid versiooni 2 või 1 ja versiooni 3 vahel, sest prognoosid arvutatakse välja ressursi rolli, mitte rea ülesande määramise järgi. Näiteks versioonis 2 on Airi Saarele määratud kaks ülesannet. Rea ülesandel olev roll ülesande 1 jaoks on arendaja ja ülesande 2 jaoks programmihaldur. Airi Saare vaikeroll on programmihaldur.

![Ühele ressursile on määratud mitu rolli](media/upgrade-multiple-roles-02.png)

Kuna arendaja ja programmihalduri rollid on erinevad, on kulude ja müügi prognoosid järgmised.

![Ressursi rollide kulude prognoosid](media/upggrade-cost-estimates-03.png)

![Ressursi rollide müügi prognoosid](media/upgrade-sales-estimates-04.png)

Kui lähete üle versioonile 3, asendatakse broneeritava ressursi meeskonnaliikme ülesandes olevad rea ülesanded ressursside määramistega. Määramises kasutatakse broneeritava ressursi vaikerolli. Järgmisel pildil on näha, kuidas Airi Saar, kellel on programmihalduri rolli, on ressurss.

![Ressursimääramised](media/resource-assignment-v2-05.png)

Kuna prognoosid põhinevad ressursi vaikerollil, võivad müügi ja kulude prognoosid muutuda. Järgmisel pildil ei näe te enam **Arendaja** rolli, kuna roll on nüüd võetud broneeritava ressursi vaikerollist.

![Vaikerollide kulude prognoosid](media/resource-assignment-cost-estimate-06.png)
![Vaikerollide müügi prognoosid](media/resource-assignment-sales-estimate-07.png)

Kui täiendus on lõpule jõudnud, saate meeskonnaliikme rolli redigeerida muuks rolliks, kui vaikimisi määratud. Kui aga muudate meeskonnaliikmete rolle, muudetakse need ära kõigis neile määratud ülesannetes, sest versioonis 3 ei saa meeskonnaliikmetele määrata mitu rolli.

![Ressursi rolli värskendamine](media/resource-role-assignment-08.png)

See kehtib ka nende rea ülesannete puhul, mis määrati nimega ressurssidele, kui muudate ressursi organisatsiooniüksuse vaikimisi määratud üksuselt muuks organisatsiooniüksuseks. Kui täiendus versioonile 3 on lõpule jõudnud, kasutatakse määramises ressursi vaikimisi määratud organisatsiooniüksust, mitte rea ülesandele määratud organisatsiooniüksust.

### <a name="tasks-assigned-to-generic-resources"></a>Üldistele ressurssidele määratud ülesanded
Versioonis 2 ja 1 saate ülesandele määrata rolli ja organisatsiooniüksuse ning seejärel kasutada funktsiooni **Loo meeskond**, et luua ülesandele määratud atribuutide järgi üldised ressursid. Versioonis 3 saate luua üldised meeskonnaliikmed koos rolli ja organisatsiooniüksusega ning seejärel määrata meeskonnaliikmed ülesannetele.

Versioonis 2 ja 1 saavad üldiste ressurssidega projektid olla kahes olekus või ülesande tasemel olla kombinatsioon mõlemast olekust. Teil saavad olla näiteks järgmised stsenaariumid.

- Ülesanded, millele on määratud rollid ja organisatsiooniüksused, ent seostuva ressursi määramist pole tehtud.
- Üldise meeskonnaliikme ressursi määramistega ülesanded, mis määrati üldise ressursi loomisega, kasutades funktsiooni **Loo meeskond**.

Enne kui alustate täiendusega, soovitame teil uuesti luua meeskonna iga projekti jaoks, millel on ülesanded määratud üldistele ressurssidele või mille suhtes pole veel meeskonna loomise protsessi käivitatud.

Nende ülesannete puhul, mis määratakse üldistele meeskonnaliikmetele ja mis loodi funktsiooni **Loo meeskond** abil, jätab täiendus üldise ressursi meeskonda ja määramise üldisele meeskonnaliikmele. Soovitame teil pärast täiendust, kuid enne ressursitaotluse broneerimist või esitamist luua ressursinõude üldise meeskonnaliikme jaoks. See säilitab kõik need üldistele meeskonnaliikmetele tehtud organisatsiooniüksuste määramised, mis on projekti lepingut sõlmivast organisatsiooniüksusest erinevad.

Näiteks projektis Project Z on lepingut sõlmivaks organisatsiooniüksuseks Jõgi US. Projektiplaanis määratakse juurutusfaasis olevatele testülesannetele tehnilise konsultandi roll ja määratud organisatsiooniüksus on Jõgi India.

![Juurutusfaasi organisatsiooni määramine](media/org-unit-assignment-09.png)

Pärast juurutusfaasi määratakse integreerimise testülesanne tehnilise konsultandi rolli, aga organisatsiooniüksuseks seatakse Jõgi US.  

![Integreerimise testülesande organisatsiooni määramine](media/org-unit-generate-team-10.png)

Kui loote projekti jaoks meeskonna, luuakse ülesannetes olevate erinevate organisatsiooniüksuste tõttu kaks üldist meeskonnaliiget. Jõgi India ülesanded määratakse tehnilisele konsultandile 1 ja Jõgi USA ülesanded tehnilisele konsultandile 2.  

![Loodud üldised meeskonnaliikmed](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> Project Service Automationi versioonis 2 ja 1 ei säilita meeskonnaliige organisatsiooniüksust, vaid see jääb alles rea ülesandes.

![Versiooni 2 ja versiooni 1 reaülesanded Project Service Automationis](media/line-tasks-12.png)

Organisatsiooniüksust näete prognooside vaates. 

![Organisatsiooniüksuse prognoosid](media/org-unit-estimates-view-13.png)
 
Kui täiendus on lõpuni jõudnud, lisatakse üldisele meeskonnaliikmele vastav rea ülesandel olev organisatsiooniüksus üldisele meeskonnaliikmele ja rea ülesanne eemaldatakse. Seetõttu soovitame teil enne täiendamist luua või uuesti luua meeskonna iga üldisi ressursse sisaldava projekti jaoks.

Nende ülesannete puhul, mis on määratud rollile sellise organisatsiooniüksusega, mis erineb lepingut sõlmivast organisatsiooniüksusest, ja kus meeskond pole loodud, loob täiendus rolli jaoks üldise meeskonnaliikme, aga kasutab meeskonnaliikme organisatsiooniüksuse jaoks lepingut sõlmivat üksust. Viidates tagasi Project Z näitele, on määratud lepingut sõlmivale organisatsiooniüksusele Jõgi US ja projektiplaani testülesannetele koos juurutusfaasiga tehnilise konsultandi roll ning organisatsiooniüksus on määratud Jõgi Indiale. Integreerimise testülesandele, mis viiakse lõpuni pärast juurutusfaasi, määratakse tehnilise konsultandi rolli. Organisatsiooniüksus on Jõgi USA ja meeskonda pole loodud. Täiendamise käigus luuakse üks üldine meeskonnaliige, tehniline konsultant, kellele on määratud kõigi kolme ülesande tunnid, ja Jõgi US-i organisatsiooniüksus ehk projekti lepingut sõlmiv organisatsiooniüksus.   
 
Kui muudate loomata meeskonnaliikmete erinevate ressurssi organisatsiooniüksuste vaikeväärtusi, soovitame teile meeskonna luua või uuesti luua nende projektide jaoks, mis sisaldavad enne täiendamist üldisi ressursse, nii et organisatsiooniüksuste määramised ei läheks kaotsi.

