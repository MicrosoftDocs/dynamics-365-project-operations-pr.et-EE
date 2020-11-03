---
title: Rakenduse Project Finder Mobile funktsioonide lubamine
description: Rakenduse Project Finder Mobile funktsioonide lubamine Project Service'i jaoks
author: JohnPBurrows
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
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074963"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Rakenduse Project Finder Mobile funktsioonide lubamine (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Teie ressursid saavad rakendust Project Finder Mobile kasutada oma telefonis koos rakendusega [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], et leida uusi projekte, millega töötada, ja värskendada oma oskusekomplekte.  
  
 Rakendus on saadaval [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]’idele, [!INCLUDE[tn_android](../includes/tn-android.md)]-telefonidele ja [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)]’ile.  
  
 Peate määrama oma organisatsiooniüksuse jaoks parameetrite sättes mõne suvandi, et võimaldada kasutajatel vaadata projektide ressursinõudeid ja värskendada oma oskusi.  
  
> [!NOTE]
>  Rakendus Project Finder Mobile töötab ainult koos teenusega [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] (mitte asutusesiseste installide puhul).  
  
1. Minge jaotisse **Project Service > Parameetrid**.  
  
2. Klõpsake parameetrite sättel, mida soovite kasutada rakenduse Project Finder Mobile funktsioonide lubamiseks.  
  
3. Määrake alal **Üldine** valiku **Ressurssidele nähtavad ressursinõuded** sätteks **Jah**.  
  
4. Määrake valiku **Luba ressursil oskuste värskendamine** sätteks **Jah**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   See on globaalne säte. Projektijuhid saavad üksiku projekti nähtavuse selle projekti lehel **Projektimeeskond**.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Meiliteatised  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] saadab ressursitaotlusi puudutavad meilid järgmistel aegadel järgmistele adressaatidele.  
  
|Adressaat|Üritus|  
|---------------|-----------|  
|Projektijuht|- Kui ressurss registreerub rakenduse Project Finder Mobile abil projektile.|  
|Ressurss|- Kui projektitöö, millele ressurss on registreerunud, on teine ressurss juba teinud.<br />- Kui tema oskuste kinnitustaotlus on kinnitatud või tagasi lükatud.<br />- Kui tema projektile registreerumise taotlus on kinnitatud või tagasi lükatud.|  
  
## <a name="privacy-notice"></a>Privaatsusavaldus  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Vt ka  
 [Ressursside seadistamine](../psa/set-up-resources.md)