---
title: Ettemaksud või honoraril põhinevad lepingud
description: Selles teemas antakse teavet Project Operationsi honoraril põhinevaid lepingumudelite ja ettemaksu kohta.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1aee64bf683b7d8d0bcde284f2d5d484e689c4d2
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596097"
---
# <a name="advances-and-retainer-based-contracts"></a>Ettemaksud või honoraril põhinevad lepingud


_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations toetab honoraril põhinevaid lepinguid. Honoraril põhinev leping on kokkulepitud võrdselt jaotatud maksete kogum, mille kohta esitatakse kliendile arveid kogu projekti kestuse vältel. Seda tüüpi lepingut kasutatakse tavaliselt aja- ja materjalide või tarbimisel põhinevate arveldusmudelite puhul, kus on vaja anda kliendile prognoositav arvete- ja maksegraafik. Iga perioodi kogunenud tegelikud tulud viiakse vastavusse kliendilt saadud maksetega perioodi alguses. Vastavalt aja- ja materjalikulu põhisele arveldusmudeli kontseptsioonile, võivad igal perioodil tekkinud tulu väärtused vastavalt tekkinud kuludele erineda. Kui kogunenud tulu ületab perioodi alguses saadud summa, võib projekti tarniv ettevõte:

- Esitada kliendile arve ainult ületanud summas 
- Lükata tulu vastavsusseviimine edasi järgmisse arveldusperioodi ja teha projekti lõpus ühe lõpliku arve mistahes allesjäänud tasakaalustamata tulu kohta.

Peamiseks erinevuseks Project Operationsi honoraril põhineva lepingumudeli ja fikseeritud hinnaga lepingumudeli vahel on see, et fikseeritud hinnaga lepingumudelis ei ole arve summa seotud tekkinud kuludega. Arveldamisel järgitakse vahe-eesmärkidel põhinevat lähenemisviisi, mis on joondatud selle perioodi kulutustega. Honoraril põhinevas lepingus kirjendatakse tulu, mida saab arveldada, võttes aluseks lepingurea arveldamise meetodi. Kui arveldamise meetod põhineb aja- ja materjalikulul, on arveldatav tulu seotud mistahes antud ajaperioodi tekkinud kuludega ja võib periooditi erineda. Kliendile esitatakse aga arve ainult perioodilise honorari summa kohta. Süsteem kasutab perioodi lõpus teist arvet, et viia vastavusse perioodi jooksul registreeritud arveldatav tulu selle summaga, mille kohta kliendile perioodi alguses arve esitati.

Selle meetodi eeliseks on see, et kliendi kulud on honorari ajakava ajal prognoositavad, vastupidiselt tüüpilisele aja- ja materjalikulul põhinevale mudelile. Projekti kättetoimetaval organisatsioonil on ka teatud ruum mistahes ulatuse suurenemisega seotud kulude katmiseks, mida fikseeritud hinnamudel neil teha ei lubaks.

Lisaks perioodilisele honoraril põhinevale ajakavale saab Project Operations registreerida kliendilt ühekordse ettemakse ja ühitada see erinevate projekti kulukomponentidega.

Project Operationsi honorar pole kasutamiseks saadaval enne, kui see on kliendiga arveldatud. Seda näitavad järgmised väljad ettemaksete ja honoraride andmeruudustikus.

| Väli | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- |
| Saadaolev summa | Summa, mis on honorari või ettemakse kirjes kasutamiseks saadaval. | Kuni ettemakse või honorar ei ole arveldatud, ei saa seda kasutada, mis tähendab, et saadaolev summa on null. |
| Kasutatud summa | Summa, mis on honoraril või ettemaksel juba kasutatud. | Ettemakset või honorari saab tegelike kuludega ühitada arvel, millel on mõned osad märgitud kui juba kasutatuks või tarbituks. Ülejäänud ettemakse või honorari summa on saadaval, et ühitada see tulevase arve tegelike kuludega. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]