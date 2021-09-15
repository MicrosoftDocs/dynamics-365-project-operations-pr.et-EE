---
title: Allhankelepingute sõlmimine 2021 a. oktoobri varajase juurdepääsu väljaandes
description: Selles teemas antakse ülevaade 2021. aasta oktoobri varajase juurdepääsuga väljaande osaks olevatest allhankelepingute sõlmimise võimalustest rakenduses Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383690"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Allhankelepingute sõlmimine 2021 a. oktoobri varajase juurdepääsu väljaandes

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Selles teemas antakse ülevaade 2021. aasta oktoobri varajase juurdepääsuga väljaande osaks olevatest allhankelepingute sõlmimise võimalustest rakenduses Dynamics 365 Project Operations. See funktsioonikomplekt pole valmis tootmises ega reaalajas keskkondades kasutamiseks, seega jäävad need funktsioonid varajase juurdepääsuga väljaandesse kuni täieliku funktsioonikomplekti välja andmiseni. Soovitame tungivalt mitte kasutada allahnkelepingute sõlmimise funktsioonikomplekti reaalajas tootmisstsenaariumide puhul seni, kuni eelversiooni bänner on eemaldatud. 

Järgmises loendis antakse ülevaade sellest, mis on praegu 2021. aasta oktoobri varajase juurdepääsu väljaandes saadaval.

1. Projektijuht sõlmib hankijaga allhankelepingu. Vaikimisi kasutatakse allhankelepingut sõlmides hankijakirjele lisatud hinnakirju. Hankija kontol on seosetüüp **Hankija** või **Tarnija**.

2. Projektijuht saab kõik ostud täpsustada allhankelepingu reaüksustena. Allhankelepingu read võivad olla aja, kulude või toodete jaoks. Allhankelepingu rea tehinguklass määratleb, mille jaoks rida on.

3. Hankija kontohaldur ja projektijuht saavad allhankelepingut itereerida. Hinnakirju saab kohandada ostuhinnakirjades, mis on allhankelepingule manustatud.

4. Kui allhankeleping on ajapõhine, seostab hankija kontohaldur selles või hilisemas protsessi punktis hankija kontaktid iga allhankelepingu reaga. See seos annab teavet projektijuhile, kes töötab allhankelepinguga. Kui hankija kontakt seostatakse allhankelepingu reaga, loob süsteem kontaktist automaatselt broneeritava ressursi, kui broneeritavat ressurssi pole veel olemas.

5. Iga allhankelepingu rea arveldamisviisiks võib olla **Fikseeritud hind** või **Aeg ja materjal**. Fikseeritud hinnaga allhankelepingu ridade jaoks seadistatakse vahe-eesmärgi põhise arve ajakava.

Ülejäänud toiminguid allhankelepingute sõlmimise äriprotsessi voos, mis on ülevaates välja toodud, ei ole hetkel saadaval. Uute funktsioonide lisamisel seda teemat värskendatakse. 

Järgmisel pildil on kujutatud allhankelepingute sõlmimise varajase juurdepääsu väljaannet algusest lõpuni äriprotsessile vastandatuna.

![Allhankelepingute sõlmimisprotsessi voog](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Kogusepõhiste ja tööpõhiste allhankelepingu ridade varajase juurdepääsu väljaanne
2021. aasta oktoobrikuu varajase juurdepääsu väljaandes toetatakse ainult kogusepõhiseid allhankelepingu ridu. See tähendab, et allhankelepingu rida saab kasutada selleks, et osta hankijalt aega, kulusid või materjale, aga mitte kogu tööd. See tähendab ka, et allhankelepingu rea ostetavat kogust (ajaühikut, kulusid või materjali kogust) saab kasutada süsteemi mistahes projekti juures.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
