---
title: Allhankelepingute haldus rakenduses Project Operations
description: Selles teemas antakse terviklik ülevaade allhankelepingute haldusprotsessi kohta tüüpiliselt projektipõhistes organisatsioonides.
author: rumant
ms.date: 08/02/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d595e948b7be9a6822827f4841e737d3c0e1476b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593009"
---
# <a name="subcontract-management-in-project-operations"></a>Allhankelepingute haldus rakenduses Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Selles teemas antakse terviklik ülevaade allhankelepingute haldusprotsessi kohta projektipõhistes organisatsioonides. Teenuste allhange järgib tavaliselt järgmisel diagrammil esitatud äriprotsessi voogu.

![Allhankelepingute sõlmimisprotsessi voog](../media/SubcontractingProcessFlow.png)

Järgmises loendis on toodud allhankelepingute sõlmimise protsessi üksikasjalik kirjeldus.

1. Projektijuht sõlmib hankijaga allhankelepingu. Vaikimisi kasutatakse allhankelepingut sõlmides hankijakirjele lisatud hinnakirju. Hankija kontol on seosetüüp **Hankija** või **Tarnija**.
2. Projektijuht saab kõik ostud täpsustada allhankelepingu reaüksustena. Allhankelepingu read võivad olla aja, kulude või toodete jaoks. Allhankelepingu rea tehinguklass määratleb, mille jaoks rida on.
3. Hankija kontohaldur ja projektijuht saavad allhankelepingut itereerida. Hinnakirju saab kohandada ostuhinnakirjades, mis on allhankelepingule manustatud.
4. Kui allhankeleping on ajapõhine, seostab hankija kontohaldur selles või hilisemas protsessi punktis hankija kontaktid iga allhankelepingu reaga. See seos annab teavet projektijuhile, kes töötab allhankelepinguga. Kui hankija kontakt seostatakse allhankelepingu reaga, loob süsteem kontaktist automaatselt broneeritava ressursi, kui broneeritavat ressurssi pole veel olemas.
5. Iga allhankelepingu rea arveldamisviisiks võib olla **Fikseeritud hind** või **Aeg ja materjal**. Fikseeritud hinnaga allhankelepingu ridade jaoks seadistatakse vahe-eesmärgi põhise arve ajakava.
6.  Pärast allhankelepingu seadistamist ja läbirääkimiste lõpetamist see kinnitatakse. Kinnitatud allhankelepinguid ei saa redigeerida, kuid muudatuste ilmnemisel saab allhankelepingu "redigeerimiseks uuesti avada", mis seab lepingu olekuks **Kinnitatud** asemel uuesti **Mustand** ja läbirääkimised saab uuesti avada. 
7.  Projektile üldise meeskonnaliikme loomisel saab selle meeskonnaliikme siduda allhankelepingu reaga. See näitab, et üldine meeskonnaliikmega on vaja täita allhankelepingu töömaht.
8.  Nimega meeskonnaliikmeid saab luua otse projektis või luua nad broneerides neid ressursi kavandamise kasutuskeskkondade kaudu. Kui nimega projekti meeskonnaliige on lepinguline töötaja, on võimalik siduda see allhankelepingu reaga. See toob välja allhankelepingu rea saadaoleva mahu.
9.  Allhankelepingu ressursid saavad logida aega, kulusid ja materjali kasutamist projektides ja projekti ülesannetes ning seejärel esitada need kinnitamiseks. See on töötajate puhul sarnane. Aja kirjendamisel saab lepinguline töötaja valida kindla allhankelepingu ja allhankelepingu rea.
10. Kinnitamisel kirjendab allhankelepingute kinnitatud ajad projekti tegelikud kulud vastavalt lepingulise töötaja ostuhinnale või tema projekti juures täidetud rollile.
11. Hankija arveid ja hankija arvete reaüksuseid saab süsteemis registreerida hankija ressursside või hankija tarnitud toodete kohta. Hankija arve read peavad vastama projektile ja aja, kulu, toote/materjali, vahe-etapi või tasu tehinguklassile. Valikuliselt võivad hankija arve read viidata ka allhankelepingu reale.
12. Süsteem seostab automaatselt kõik allhankelepingu reale ja projektile vastavad tegelikud kulud hankija arvega. See hõlbustab kolmesuunalist vastendamise ja kontrollimise protsessi.
13. Seejärel saab projektijuht vaadata läbi automaatselt vastendatud projekti tegelikud andmed, eemaldada või lisada muid projekti tegelikke kulusid ja viia kontrollimisprotsessi lõpule.
14. Kõigi ridade kontrollimisprotsessi lõpetamine märgib hankija arve olekuks **Maksmiseks valmis**. Selles etapis saab hankija arve ja read edastada raamatupidamis- või makstavate arvete süsteemi makse hankijale töötlemiseks. Varem registreeritud projekti kulud tühistatakse ja hankija arve rea tegelikud kulud kirjendatakse projektile.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Kogusepõhised allhankelepingute read ja tööpõhised allhankelepingute read

Allhankelepingu rida võib olla kogusepõhine või tööpõhine. 

Kui allhankelepingu rida on **kogusepõhine** saab allhankelepingu real ostetava aja, kulu või materjali kogust kasutada mistahes projekti juures.

Kui allhankelepingu rida on **tööpõhine**, vastendatakse allhankelepingu rida projektiplaanis sõlmega esindatava tööga. Allhankelepingu rea väärtus on kõigi töö teostamiseks vajalike komponentide summa. Need modelleeritakse allhankelepingu rea üksikasjadena ja need võivad olla aja, kulude või materjalide kogumid. Tööpõhise allhankelepingu rea korral on allhankelepingu rida mõeldud ühele projektile. Seda tüüpi allhanked on currenlty, mida Project Operations ei toeta.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

