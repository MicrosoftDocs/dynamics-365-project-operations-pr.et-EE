---
title: Projektide ja broneeringute haldamine kalendris Office 365
description: Kuidas hallata projekte ja broneeringuid kalendris Office 365?
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: fd4119693875fb851c7bd3f34287db7d81237140
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074990"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Projektide ja broneeringute haldamine kalendris (projektiteenus)

> [!Note]
> IGANENUD: see funktsioon on iganenud ega ole enam saadaval.

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendris saate vaadata kohtumiste ajakava, projektide ja töö broneeringud ning väliteeninduse töökäsu ülesandeid.  
  
 Kui kõik asub ühes kohas, on oma päeva haldamine lihtne. Kõik koosolekud, kohtumised, broneeringud ja ülesanded on olemas teie [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendris.  
  
 Kui kasutate lisandmoodulit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], võite sisestada ka oma isiklikud kohtumised Project Service’i aja sisestamise vaates. Nii saavad projektijuhid ja ressursihaldurid teada, millal olete projektis osalemiseks saadaval. Samuti säästab see aega, kuna teil pole tarvis oma isiklike kohtumiste teavet kaks korda sisestada. Saate hõlpsasti oma isiklikud kohtumised kalendrist Project Service’i aja sisestamise vaatesse importida.  
  
 Kalender sünkroonib projektide ja töökäskude broneeringud järgmise nelja nädala ulatuses. Seda sätet ei saa muuta.  
  
 Sünkroonimine on toetatud ainult ühes suunas, PSA-st teie [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendrisse. Saate sünkroonida vastupidises järjekorras. 
  
 Lisateavet [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendri kasutamise kohta vaadake jaotisest [Outlooki veebirakenduse kalender ettevõtetele](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Seadistamine  
 Enne kui saate oma broneeringuid [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendris vaadata ja hallata, peate mõned asjad seadistama.  
  
- Teil peab olema lahenduse [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] üldadministraatori või süsteemiadministraatori identimisteave.  
  
- Teie administraator peab konfigureerima meiliserveri profiili ja iga kasutaja peab konfigureerima oma postkasti. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Meilitöötluse häälestamine serveripoolse sünkroonimise kaudu](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Lülitage sisse sünkroonimine teenus oma organisatsiooni jaoks (administraatori ülesanne)  
  
1.  Klõpsake põhimenüüs valikuid **Sätted** > **Haldus**.  
  
2.  Klõpsake valikut **Süsteemisätted**.  
  
3.  Klõpsake vahekaarti **Sünkroonimine**.  
  
4.  Märkige lause **Valige, kas lubada ressursireserveeringute sünkroonimine koos** all ruut **Sünkrooni ressursireserveering Outlookiga**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Lülitage sisse sünkroonimine oma kasutajaprofiili jaoks (kasutaja ülesanne)  
  
1.  Klõpsake nuppu **Sätted** ekraani ülemises parempoolses nurgas.  
  
2.  Klõpsake **Suvandid**.  
  
3.  Klõpsake vahekaarti **Sünkroonimine**.  
  
4.  Märkige lause **Ressursireserveeringu sünkroonimine Outlookiga** all ruut **Sünkrooni ressursireserveering Outlookiga**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Isiklike kohtumiste importimine (kasutaja ülesanne)  
 Saate oma isiklikud kohtumised kalendrist Project Service Automation aja sisestamise vaatesse importida.  
  
1. Avage [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalender ja klõpsake nuppu **Impordi andmed**.  
  
2. Valige filrtite kuval suvand **Kohtumised Exchange’ist** ja klõpsake seejärel nuppu **Rakenda**.  
  
3. Süsteem kopeerib jooksva nädala kohtumised aja sisestamise vaatesse soovituslike sissekannetena. Kui soovite lisada andmeid mõnda muusse nädalasse, klõpsake **Eelmine** või **Järgmine**.  
  
4. Valige kohtumine, mida soovite lisada Project Service Automation aja sisestamise vaatesse.  
  
5. Valige hüpikaknas **Ajakirje** sobivad suvandid, et teisendada kohtumine Project Service Automation aja sisestamise vaate jaoks.  
  
6. Klõpsake nuppu **Salvesta**.  
  
### <a name="see-also"></a>Vt ka  
 [Aja-, kulu- ja koostööjuhend](../psa/time-expense-collaboration-guide.md)
