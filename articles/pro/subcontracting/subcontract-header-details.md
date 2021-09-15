---
title: Allhankelepingute päise üksikasjad
description: Selles teemas kirjeldatakse Project Operationsis allhankelepingu päises antud funktsionaalsust.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323636"
---
# <a name="header-details-for-subcontracts"></a>Allhankelepingute päise üksikasjad

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Selles teemas kirjeldatakse rakenduses Dynamics 365 Project Operations allhankelepingu päises antud funktsionaalsust.

Kui projektijuht projekte kavandab ja käivitab, võib ta palgata alltöövõtjaid ja osta hankijatelt tooteid ja teenuseid. Kui projektijuhil on vaja tooteid või teenuseid osta, võib ta Project Operationsis allhankelepingu luua.

Allhankelepingu loomiseks läbige järgmised etapid.

1. Valige navigeerimispaanil **Allhankelepingud** ja tehke lehel **Allhankeleping** valik **Uus**.
2. Sisestage nõutud teave ja valige seejärel **Salvesta**.

    Järgmine tabel sisaldab teavet allhankelepingu päise lehe väljade kohta.

    | **Väli** | **Kirjeldus** |
    | --- | --- | 
    | Nimetus | Allhankelepingu nimi. |
    | Kirjeldus | Allhankelepingul ostetavate teenuste ja toodete lühikirjeldus. |
    | Tarnija | Selle ettevõtte nimi, millelt tooteid ja teenuseid ostetakse. Sellel kontokirjel on seosetüüp **Hankija** või **Tarnija**. |
    | Allhankelepingu kuupäev | Allhankelepingu loomise kuupäev. |
    | Oleku põhjus | Allhankelepingu olek. |
    | Valuuta | Toodete ja teenuste ostmisvaluuta. Selle välja vaikeväärtus saadakse hankija kontolt, kuid seda saab muuta. Projekti hinnakirjad, mida kasutatakse allhankelepingul toodete ja teenuste hinnakujunduses, peaksid olema selles valuutas. Mistahes muus valuutas hinnakirju ei saa allhankelepinguga seostada. Sellel allhankelepingul tekkinud toodete ja teenuste kulud kirjendatakse projektis selles valuutas. |
    | Lepingut sõlmiv üksus | Ettevõtte allüksus, mis sõlmib hankijaga ostulepingu või allhankelepingu. |
    | Maksetingimused | Selle allhankelepingu põhjal väljastatud hankija arvete maksetingimused. Selle välja vaikeväärtus saadakse hankija kontolt kirjest. |
    | Makse aadress | Aadress, kuhu hankija arvete makse saadetakse. Selle välja vaikeväärtus saadakse hankija kontolt kirjest. |
    | Maksja nimi | Hankija ettevõtte isiku või allüksuse nimi, kes arve saadab. Selle välja vaikeväärtus saadakse hankija konto kirjest ja seda kasutatakse selle allhankelepingu jaoks loodud hankija arvete peamise kontakti nimena. |
    | Maksja aadress | Aadress sellelt hankijatelt tulevatel arvetel. Selle välja vaikeväärtus saadakse hankija kontolt kirjest. Seda aadressi kasutatakse ka sellest allhankelepingust loodud hankija arvete arve saatja aadressina. |
    | Vahesumma | Kui allhankelepingul ei ole ridu, sisestage sellele väljale väärtus, mis näitab tellimuse vahesummat enne makse. Kui allhankelepingul on ridu, on see väli kirjutuskaitstud. Kuvatav summa on kõikide allhankelepingu ridade vahesumma. |
    | Kogumaks | Kui allhankelepingul ei ole ridu, sisestage sellele väljale väärtus, mis näitab selle allhankelepingu makse. Kui allhankelepingul on ridu, on see väli kirjutuskaitstud. Kuvatav summa on kõikide allhankelepingu ridade maksude summa. |
    | Kogusumma |  See arvutatud väli kuvab allhankelepingu kogusummat koos maksudega.  |
    | Kinnitamise kuupäev | Allhankelepingu kinnitamise kuupäev.  |
    | Taotleja | Selle välja väärtuseks on vaikimisi allhankelepingu loonud kasutaja nimi. Allhankelepingu looja saab seda väärtust muuta, et näidata isikut, kelle nimel ta allhankelepingu sõlmib.  |
    | Hankija kontohaldur | hankija konto esmase kontakti nimi. Selle välja vaikeväärtus saadakse hankija kontolt kirjest. Kasutaja saab selle välja väärtust muuta, et valida allhankelepingu hankija kontohalduriks erinev kontakt. Saab konfigureerida nii, et meiliteavitused ja hinnaläbirääkimised saadetakse sellele kontaktile. |


