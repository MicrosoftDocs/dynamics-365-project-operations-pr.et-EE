---
title: Valuuta
description: Selles artiklis antakse teavet selle kohta, kuidas projektitoimingutes valuutatüüpe lisada ja eemaldada.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0fbfd1039fe0a7401376bb8c27b118297fdc87f5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921527"
---
# <a name="currency"></a>Valuuta

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_



Valuutad määratlevad tootekataloogis olevate toodete hinna ja tehingute (nt müügitellimuste) maksumuse. Kui teie kliendid asuvad maailma eri paikades, lisage tehingute haldamiseks nende valuutad. Lisage valuutad, mis on teie praegusteks ja tulevasteks ärivajadusteks kõige sobivamad.  

> [!NOTE]
> Kui teie keskkond on Common Data Service'i keskkond, te olete Power Platformi halduskeskuses ja valite lehe **Valuutad** (**Keskkonnad** > [valige keskkond] > **Sätted** > **Ettevõte** > **Valuutad**), on leht tühi. Seda selle tõttu, et teenuse Common Data Service keskkondades ei toetata valuuta seadmist.

## <a name="add-a-currency"></a>Valuuta lisamine  
Enne selle toimingu käivitamist kontrollige, et teie turberoll sisaldab süsteemiadministraatori õigusi. 

1. Power Platformi halduskeskuses valige keskkond. 
2. Valige **Sätted** > **Ettevõte**.
3. Valige **Valuutad**.  
4. Tehke valik **Uus**.  
5. Sisestage nõutavad andmed.  


   |          Väli          |                                                                                                                                                                                                                                                                                                                                                                            Kirjeldus                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Valuuta tüüp**    | - **Süsteem** – valige see suvand, kui soovite kasutada Dynamics 365 mudelipõhistes rakendustes saadaval olevaid valuutasid. Valige valuuta otsimiseks nupp **Otsing**. Kui valite valuutakoodi, lisatakse **Valuuta nimi** ja **Valuutatähis** automaatselt valitud valuuta kohta.<br />- **Kohandatud** – valige see suvand, kui soovite lisada valuutat, mis ei ole Dynamics 365 mudelipõhistes rakendustes saadaval. Sellisel juhul peate sisestama valikute **Valuutakood**, **Valuuta täpsus**, **Valuuta nimi**, **Valuutatähis** ja **Valuutavahetus** väärtused käsitsi. |
   |    **Valuutakood**    |                                                                                                                                                                                                                                                                                                                                            Valuuta lühivorm. Näide: **USD** Ameerika Ühendriikide dollari kohta.                                                                                                                                                                                                                                                                                                                                            |
   | **Valuuta täpsus**  |                                                                                                                                                                                  Sisestage kümnendkohtade arv, mida selle valuuta puhul kasutada soovite.  Võite lisada väärtuse vahemikus 0–4. **Märkus.** Kui olete määranud dialoogiboksis **Süsteemisätted** täpsuse väärtuse, kuvatakse siin see väärtus.                                                                                                                                                                                  |
   |    **Valuuta nimi**    |                                                                                                                                                                                                                                         Kui valisite Dynamics 365 mudelipõhistes rakendustes saadaval olevate valuutade loendist valuuta koodi, kuvatakse siin valitud koodile vastava valuuta nime. Kui valisite valuutatüübiks **Kohandatud**, sisestage valuuta nimi.                                                                                                                                                                                                                                          |
   |   **Valuutatähis**   |                                                                                                                                                                                                                                                                      Kui valisite valuutakoodi olemasolevate valuutade loendist, kuvatakse siin valitud valuuta tähis. Kui valisite valuutatüübiks **Kohandatud**, sisestage uue valuuta tähis.                                                                                                                                                                                                                                                                       |
   | **Valuutavahetus** |                                                                                                                                                                                                                                     Sisestage valitud valuuta väärtus ühe USA dollari kohta. See on summa, millega valitud valuuta baasvaluutaks arvutab. **NB!**  Värskendage seda väärtust nii sageli, kui vajalik, et vältida oma kannetes ebatäpseid arvutusi.                                                                                                                                                                                                                                      |


6. Kui olete lõpetanud, valige käsuribalt käsk **Salvesta** või **Salvesta ja sule**.  

   > [!TIP]
   >  Valuuta muutmiseks valige valuuta ja seejärel sisestage või valige uued väärtused.  

## <a name="delete-a-currency"></a>Valuta kustutamine  

1. Power Platformi halduskeskuses valige keskkond. 
2. Valige **Sätted** > **Ettevõte**.
3. Valige **Valuutad**.  
4. Valige kuvatavate valuutade loendist kustutatav valuuta.  
5. Valige **Kustuta**.  
6. Kinnitage kustutamine.  

> [!IMPORTANT]
>  Te ei saa kustutada valuutasid, mida kasutavad teised kirjed; need saab ainult inaktiveerida. Inaktiveerimisel ei eemaldata olemasolevates kirjetes (nt müügivõimalustes või tellimustes) talletatud valuutateavet. Kuid te ei saa valida inaktiveeritud valuutat uute kannete jaoks.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]