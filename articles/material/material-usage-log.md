---
title: Projektides ja projektiülesannetes materjali kasutuse kirjendamine
description: Selles teemas antakse teavet selle kohta, kuidas logida projektides ja projektiülesannetes materjalide kasutamist.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 60aed9aa82eeb0339e71b0171719e765a63d91e7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579669"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Projektides ja projektiülesannetes materjali kasutuse kirjendamine

_**Rakendub:** Project Operationsi ressursipõhiste/mittelaopõhiste stsenaariumide korral, lihtjuurutamine – tehing näidisarveldusele_

Kuna projektimeeskond töötab projekti ülesannete kaudu, siis nad tarbivad või kasutavad materjale. Materjalide kasutuslogi võimaldab seda kasutust registreerida nii, et projektijuht saaks selle heaks kiita ja esitada lõpuks selle eest kliendile arve. 

Kataloogi või sisestatavate kasutamise kirjendamiseks ja nende kinnitamiseks toimige järgmiselt. 

1. Valige navigeerimispaanil **Materjali kasutus** ja valige seejärel **Uus**.
2. Sisestage lehel **Uus materjal kasutus** vajalik materjalide kasutusteave ja valige seejärel nupp **Salvesta**.

Järgmine tabel sisaldab teavet väljade kohta lehel **Materjalide kasutuslogi**. 

| **Väli** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- |
| Kirjeldus | Kindla materjali kasutuse kirjeldus. | Sellel väljal puudub allavoolu mõju. |
| Kuupäev | Materjali eeldatav kasutamise kuupäev. | Sellel väljal puudub allavoolu mõju. |
| Project | Aktiivsete projektide loend. | Materjali kasutuslogi jaoks projekti valimine mõjutab välja **Ülesanne**, et kuvada ainult projektis sisalduvad ülesanded. |
| Toiming | Projekti ülesannete loend koos kokkuvõtte ja lehe ülesannetega. | Materjali kasutuslogi jaoks ülesande valimine mõjutab ülesande tegelikku materjali kulu ja tegelikku materjali müüki. Kui see väli on tühi, jälgitakse ja summeeritakse vastavat materjali kasutuskulu ning müüki ainult projekti tasandil. |
| Vali toode | Määrake, kas see materjali kasutus on **olemasoleva** (kataloogi) toote või **sisestatava** toote jaoks. | See väli määratleb tootetüübi. |
| Toode | Toote ID tootekataloogist. Kui valite toote ID, värskendatakse väli **Toote valimine** automaatselt valikule **Olemasolev toode**. ID-d kasutatakse hinnakirjast kulu ja müügihinna toomiseks. | Sellel väljal puudub allavoolu mõju. |
| Sisestatava toote kirjeldus | Tekstiväli, kuhu saab kirjutada toote nime. See väli on saadaval juhul, kui valite väljal **Toote valimine** **sisestatava** toote.| Sellel väljal puudub allavoolu mõju. |
| Broneeritav ressurss| Ressurss, mis kasutas seda materjali projektis. Selle välja vaikeväärtus on sisse logitud kasutaja broneeritav ressurss, kuid seda saab muuta, et salvestada kasutust projektimeeskonna teiste liikmete nimel. | Sellel väljal puudub allavoolu mõju. |
| Ühikurühm | Selle välja vaikeväärtus pärineb ühikurühmast, mis on häälestatud kataloogitoote vaikevalikuks. Saate selle välja värskendada, et valida mõne muu ühikurühma. | Sellel väljal puudub allavoolu mõju. |
| Üksus | Selle välja vaikeväärtus on valitud toote vaikeühik. Saate selle välja värskendada, et valida mõne muu ühiku. | Ühiku muutmise tulemuseks on erinev vaikimisi ühikuhind ja kulu. |
| Kogus | Toote kogus, mida on projektis või projektiülesandes kasutatud. | Sellel väljal puudub allavoolu mõju. |
| Ühiku kulu | Valitud toote ja ühiku kombinatsiooni ühikukulu, mis on häälestatud rakendatavas kuluhinnakirjas. | Ühikukulu kuvatakse alati projekti kuluvaluutas. Kui hinnakirjas puudub kombineeritud toote ühiku kulu ja ühik, on ühiku kuluks vaikimisi 0,00. |
| Kogukulu | Kulusumma, mis arvutatakse kui kogus \* ühikukulu.| Kulusumma kuvatakse alati projekti kuluvaluutas. |


## <a name="submit-material-usage-for-review-and-approval"></a>Materjali kasutuse läbivaatamiseks ja kinnitamiseks esitamine 
Pärast kogu oma materjali kasutuse jäädvustamist ja olete valmis laskma selle heaks kiita, peate edastama kasutusteabe läbivaatamiseks.

1. Avage **Materjali kasutuslogi** ja valige üks või mitu kirjet. Või märkige päises oleva märkeruudu abil kõik materjali kasutuskirjed.
2. Valige käsk **Esita**. Süsteem töötleb valitud kirjeid ja loob seejärel materjalide kasutamise kinnitamise taotlused.

## <a name="recall-a-material-usage-log"></a>Materjali kasutuslogi tagasikutsumine

Vajaduse korral saate edastatud materjali kasutuse tagasi kutsuda. Materjali kasutuse kirje tagasikutsumises vajalik aeg oleneb kinnitamise etapist.  Kui kinnitaja pole kirjet veel kinnitanud, võib tagasikutsumine toimuda kohe. Samas kui kirje on juba kinnitatud, palutakse kinnitajal kinnitada tagasikutsumine ja tühistada tehing.

1. Avage **Materjali kasutus** ja valige materjali kasutuslogide loendist tagasikutsumiseks materjali kasutus.
2. Tehke valik **Kutsu tagasi**. Kui materjali kasutuskirje pole veel kinnitatud, kutsub süsteem selle kohe tagasi. Kui materjalikirje on juba kinnitatud, luuakse tagasikutsumise taotlus, et teavitada kinnitajat, et soovite selle materjali kasutuse tagasi kutsuda. Kinnitaja kinnitab seejärel, et tagasikutsumine on võimalik, ja kirje tagastatakse.

## <a name="delete-a-material-usage-log"></a>Materjali kasutuslogi kustutamine

Materjali kasutuslogid, mis pole veel esitatud, saab kustutada. Juba edastatud materjali kasutuslogi kustutamiseks peate selle esmalt tagasi kutsuma.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
