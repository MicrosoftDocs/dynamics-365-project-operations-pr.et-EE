---
title: Mis on uut novembris 2020 – Project Operations Lite’i juurutamine – tehing näidisarveldusele
description: See teema sisaldab teavet Project Operations Lite’i juurutuse – tehing näidisarveldusele 2020. aasta novembri väljalaskes saadaolevate kvaliteedi värskenduste kohta.
author: sigitac
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa95406a27e6d32d2be75303904547b59f24c8b2
ms.sourcegitcommit: 64d0de964a9b66c015ffcf1db62cbb6216cb3187
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367171"
---
# <a name="whats-new-november-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Mis on uut novembris 2020 – Project Operations Lite’i juurutamine – tehing näidisarveldusele

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Järgmises tabelis on toodud rakenduse Project Operations CDS-i keskkonna versiooni 4.4.0.70 värskendused.

| Funktsiooni ala                 | Viitenumber | Kvaliteedi värskendus                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Müügivõimaluste haldus       | 2036993          | Prognoosi rida ja ressursi määramise pelinguread on võidetud hinnapakkumistel värskendatud, kui hinnapakkumise rea tüüp on **Kõik ülesanded**.                                                 |
|   Müügivõimaluste haldus       | 2071514          | Fikseeritud hinnaga vahe-eesmärgi jaoks ei saa luua arvet lepingus, kus ülesandepõhine arveldamine on lubatud.                                                                          |
| Arveldamine ja hinnakujundus          | 2070392          | Arve projekti lepinguread suurenevad iga kord, kui valitakse suvand **Värskenda arve tehinguid**.                                                                       |
| Projekti kavandamine             | 2043336          | Projektimeeskonna liikme kirjet ei saa kustutada.                                                                                                                                    |
| Projekti kavandamine             | 2046013          | Vastuoluline prognooside sildi veergude käitumine laadimise vs. ajafaasi tüüpi muutuse ajal.                                                                                   |
| Projekti kavandamine             | 2046647          | Algus- ja lõpuajad on tunni võrra paigast ära, kui ressursinõuded luuakse projektimeeskonna liikmetest.                                                                      |
| Projekti kavandamine             | 2053879          | (Iga eelseisva CDS-i väljastamise kohta) PublishUnassignedAssignments katkestab ülesande salvestamise proovimise vea „ConditionOperator.In-i jaoks edastatud väärtus on tühi” korral. |
| Projekti kavandamine             | 2055501          | Suvandi **Projekti alguskuupäev** tühjaks jätmine põhjustab ajakava tõrget.                                                                                                      |
| Projekti kavandamine             | 2066817          | Vahekaardi **Ülesanded** inimeste valijat kasutades ei saa luua üldist ressurssi.                                                                                               |
| Projekti kavandamine             | 2067034          | Nupp **Kuva üksikasjad** pole lehel **Ülesande üksikasjad** saadaval.                                                                                                         |
| Ressursihaldus          | 2046667          | Üldisi meeskonnaliikmeid ei kustutata isegi pärast kõikide ressursside täitmist.                                                                                                     |
| Aja- ja kiirsisestuse kirje | 2047499          | Ajakirje lehe nupp **Uus** avan lehe **Uus meili signatuur**.                                                                                               |
| Aja- ja kiirsisestuse kirje | 2059859          | Kulukirje loomisel avaneb ootamatu hüpikaken.                                                                                                                         |
| Muu                        | 2044181          | [Ostutellimuse desinstallimine] Kui proovite desinstallida **msdyn_ProjectServiceCore_Patch** ja msdyn Projektiteenuse põhilahendusi, ilmneb tõrge „Kirje pole saadaval”.        |