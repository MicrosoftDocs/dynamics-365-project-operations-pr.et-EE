---
title: Juurutustüübid
description: Selles teemas antakse teavet, et aidata teha kindlaks oma ettevõtte projektitoimingute õige juurutamistüüp.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948828"
---
# <a name="deployment-types"></a>Juurutustüübid

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

> [!IMPORTANT]
> Pärast litsentsi ostmist alustage siit, et määratleda rakenduse Dynamics 365 Project Operations jaoks parim juurutuse mudel, kasutades [juhendatavat installimisvoogu](https://aka.ms/provisionprojectoperations).
> Pärast juhendatud installimisvoo lõpetamist suunatakse teid õigesse haldusportaali, et saaksite oma installimise lõpule viia. Installimise lõpuleviimiseks lugege allolevaid juurutuse üksikasju.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Dynamicsi olemasolevad kliendid, kes kasutavad rakendust Dynamics 365 Project Service Automation
Project Operations sisaldab võimalusi, mis tarnitakse koos rakendusega Project Service Automation. Tulevikus antakse nendele klientidele välja versiooniuuenduse tee.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Rakenduse Dynamics 365 Finance olemasolevad kliendid, kes kasutavad projektihaldust ja raamatupidamist 

Rakenduse Finance olemasolevad kliendid, kes kasutavad projektihalduse ja raamatupidamise funktsiooni, saavad jätkata selle kasutamist samal kujul. Vaadake teemat [Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks](#pma).

Project Operations toetab teie vajadustele vastamiseks mitut juurutamise võimalust. Olenemata sellest, kas olete rakenduse Dynamics 365 uus või juba aktiivne klient, Project Operations saab teie vajadusi toetada.

Meie [juurutuse küsimustik](https://aka.ms/provisionprojectoperations) aitab teil teha kindlaks õige juurutuse. Tulemused suunavad teid ühe järgmiste juurutustüübi juurde.

- [Lihtjuurutamine – tehing fiktiivsele arveldusele](#lite)
- [Project Operations ressursi/mitteaktsia stsenaariumite jaoks](#integrated)
- [Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks](#pma)

Project Operations toetab juriidilise olemi tasemel konfguratsioonide kaudu samas keskkonnas ladustatavat/tootmistellimuste stsenaariumeid ja mitteladustatavaid/ressursipõhiseid stsenaariumeid. Näiteks saab Contoso võimendada ladustatud/tootmistellimuse võimalusi oma USA tootmisettevõttes (juriidiline olem = Contoso tootmine Ameerika Ühendriikides) ja mitteladustatavaid/ressursipõhiseid võimalusi oma Contoso robotõlgade hooldamise asutuses Suurbritannias (juriidiline olem = Contoso robootika Ühendkuningriigis).

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>Lihtjuurutamine – tehing näidisarveldusele
Lite’i juurutus sisaldab järgmisi võimalusi.

- Projekti planeerimine Microsoft Pro veebirakendust kasutades
- Mitmedimensiooniline hinnakujundus
- Ühtne ressursihaldus
- Aja jälgimine
- Põhikulu
- Arvesoovitus

### <a name="deployment-steps"></a>Juurutamise sammud.
Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.

Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](lite-preview-subscription-sign-up.md) ja [Uue keskkonna ettevalmistamine](lite-deployment.md). 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>Project Operations ressursi/mitteaktsia stsenaariumite jaoks
Project Operations ressursipõhiste/mitteladustatavate stsenaariumite jaoks hõlmavad järgmisi võimalusi.
  
- Projekti planeerimine Microsoft Pro veebirakendust kasutades
- Mitmedimensiooniline hinnakujundus
- Ühtne ressursihaldus
- Aja jälgimine
- Põhikulu
- Täiskulu
- Kviitungi OCR
- Täisarveldus
- Tulu kajastamine

### <a name="deployment-steps"></a>Juurutamise sammud.
Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.

Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](resource-sign-up-preview-subscription.md) ja [Uue keskkonna ettevalmistamine](resource-provision-new-environment.md). 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks

- Projekti kavandamise WBS-i kasutades
- Ressursihaldus
- Aja jälgimine
- Täiskulu
- Kviitungi OCR
- Täisarveldus
- Tulu kajastamine
- Tootmistellimused
- Materjalide tugi

### <a name="deployment-steps"></a>Juurutamise sammud.
Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.

Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ja [Uue keskkonna ettevalmistamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



