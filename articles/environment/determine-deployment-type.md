---
title: Juurutamise tüübi määratlemine
description: Selles teemas antakse teavet, et aidata teha kindlaks oma ettevõtte projektitoimingute õige juurutamistüüp.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2da6af3240d8e561d01b1fcd8d32b657dbac1588
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479559"
---
# <a name="determine-your-deployment-type"></a>Juurutamise tüübi määratlemine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

> [!IMPORTANT]
> Pärast litsentsi ostmist alustage siit, et määrata parim Dynamics 365 Project Operationsi juurutamise mudel kasutades [Juhendatud paigalduse voogu](https://aka.ms/provisionprojectoperations).
> Pärast juhendatud installimisvoo lõpetamist suunatakse teid õigesse haldusportaali, et saaksite oma installimise lõpule viia. Installimise lõpuleviimiseks lugege juurutuse üksikasju.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Dynamicsi olemasolevad kliendid, kes kasutavad rakendust Dynamics 365 Project Service Automation
Project Operations sisaldab võimalusi, mis tarnitakse koos rakendusega Project Service Automation. 2021. aasta väljalaske 1. laine klientidele väljastatakse versiooniuuenduse tee.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Rakenduse Dynamics 365 Finance olemasolevad kliendid, kes kasutavad projektihaldust ja raamatupidamist 

Rakenduse Finance olemasolevad kliendid, kes kasutavad projektihalduse ja raamatupidamise funktsiooni, saavad jätkata selle endisel kujul kasutamist. Vaadake teemat [Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks](#pma).


## <a name="deployment-regions"></a>Juurutamise piirkonnad
Project Operationsi juurutust toetavate piirkondade määratlemiseks vaadake teemat [Dynamics 365-e ja Power Platformi aruande geograafiline kättesaadavus](https://dynamics.microsoft.com/en-us/geographic-availability/). Valige **Kuva aruanne** ja laiendage **Dynamics 365 > Operationsi rakendused > Dynamics 365 Project Operations**, et vaadata toetatud piirkondi.

## <a name="deployment-types"></a>Juurutustüübid
Project Operations toetab teie vajadustele vastamiseks mitut juurutamise võimalust. Olenemata sellest, kas olete rakenduse Dynamics 365 uus või juba aktiivne klient, Project Operations saab teie vajadusi toetada.

Meie [juurutuse küsimustik](https://aka.ms/provisionprojectoperations) aitab teil teha kindlaks õige juurutuse. Tulemused suunavad teid ühe järgmiste juurutustüübi juurde.

- [Lihtjuurutamine – tehing fiktiivsele arveldusele](#lite)
- [Project Operations ressursi/mitteaktsia stsenaariumite jaoks](#integrated)
- [Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks](#pma)

Project Operations toetab juriidilise olemi tasemel konfguratsioonide kaudu samas keskkonnas ladustatavat/tootmistellimuste stsenaariumeid ja mitteladustatavaid/ressursipõhiseid stsenaariumeid. Näiteks saab Contoso kasutada ladustatud/tootmistellimuse võimalusi oma USA tootmisettevõttes (juriidiline olem = Contoso tootmine Ameerika Ühendriikides). Contoso saab kasutada ladustatud/tootmistellimuse võimalusi oma Contoso robotõlgade hooldamise asutuses Ühendkuningriigis (juriidiline olem = Contoso robootika Ühendkuningriigis).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Lihtjuurutamine – tehing näidisarveldusele

Lite’i juurutus sisaldab järgmisi võimalusi.

- Rakenduse Dynamics 365 Sales kogemusi ületavate projektide müügiprotsess
- Projekti planeerimine Microsoft Pro veebirakendust kasutades
- Mitmedimensiooniline hinnakujundus
- Ühtne ressursihaldus
- Aja jälgimine
- Põhikulu
- Näidisarvedamine ja ja kliendile suunatud arveldamine 

#### <a name="deployment-steps"></a>Juurutamise sammud
Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.

Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](lite-preview-subscription-sign-up.md) ja [Uue keskkonna ettevalmistamine](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations ressursi/mitteaktsia stsenaariumite jaoks
Project Operations ressursipõhiste/mitteladustatavate stsenaariumite jaoks hõlmavad järgmisi võimalusi.
 
- Rakenduse Dynamics 365 Sales ületavate projektide müügiprotsess
- Projekti planeerimine Microsoft Pro veebirakendust kasutades
- Mitmedimensiooniline hinnakujundus
- Ühtne ressursihaldus
- Aja jälgimine
- Põhikulu
- Täiskulu
- Kviitungi OCR
- Näidisarvedamine ja ja kliendile suunatud arveldamine 
- Projektide tulude kajastamine

#### <a name="deployment-steps"></a>Juurutamise sammud
Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.

Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](resource-sign-up-preview-subscription.md) ja [Uue keskkonna ettevalmistamine](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks

- Projekti kavandamise WBS-i kasutades
- Ressursihaldus
- Aja jälgimine
- Täiskulu
- Kviitungi OCR
- Täisarveldus
- Tulu kajastamine
- Tootmistellimused
- Materjalide tugi

#### <a name="deployment-steps"></a>Juurutamise sammud
Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.

Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ja [Uue keskkonna ettevalmistamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
