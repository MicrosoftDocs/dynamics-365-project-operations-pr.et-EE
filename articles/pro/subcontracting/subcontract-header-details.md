---
title: Allhankelepingute päise üksikasjad
description: Selles teemas kirjeldatakse Project Operationsis allhankelepingu päises antud funktsionaalsust.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee863d31b45e7de962488fe804202ddfe580eb04
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501321"
---
# <a name="header-details-for-subcontracts"></a>Allhankelepingute päise üksikasjad

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Selles teemas kirjeldatakse rakenduses Dynamics 365 Project Operations allhankelepingu päises antud funktsionaalsust.

Kui projektijuht projekte kavandab ja käivitab, võib ta palgata alltöövõtjaid ja osta hankijatelt tooteid ja teenuseid. Kui projektijuhil on vaja tooteid või teenuseid osta, võib ta Project Operationsis allhankelepingu luua.

Allhankelepingu loomiseks läbige järgmised etapid.

1. Valige navigeerimispaanil **Allhankelepingud** ja tehke lehel **Allhankeleping** valik **Uus**.
2. Sisestage nõutud teave ja valige seejärel **Salvesta**.

    Järgmine tabel sisaldab teavet lehe **Allhankelepingu päis** väljade kohta.

    | Väli | Kirjeldus |Funktsionaalne mõju |
    |---|------|---| 
    | Nimetus | Allhankelepingu nimi. | Kõigis allhankelepingu ripploendis on allhankelepingu nimi loetletud esimeses veerus, et aidata allhankelepingut tuvastada. | 
    | Kirjeldus | Allhankelepingul ostetavate teenuste ja toodete lühikirjeldus. | Pole |
    | Tarnija | Selle ettevõtte nimi, millelt tooteid ja teenuseid ostetakse. Sellel kontokirjel on seosetüüp **Hankija** või **Tarnija**. | Vastavalt valitud hankijale sisestatakse vaikeväärtused automaatselt järgmistele väljadele:<br/> **• Valuuta** </br> **• Hinnakirjad** </br> **• Maksetingimused**</br> **• Makse aadress**</br> **• Maksja aadress**</br> **• Maksja nimi** </br>**• Hankija kontohaldur**|
    | Allhankelepingu kuupäev | Allhankelepingu loomise kuupäev. | Allhankelepingu kuupäeva kasutatakse õige ostu hinnakirja valimiseks kas seotud hankijatele lisatud hinnakirjadest või projekti parameetritest. |
    | Oleku põhjus | Allhankelepingu olek. | Olek määratleb, kus allhankeleping ettevõtte tegevuses paikneb ning kas seda saab redigeerida. <br/>Väärtused hõlmavad järgmist.<br>• **Mustand**: lepinguid saab redigeerida. Saate redigeerida ainult neid lepinguid, mille olek on **Mustand**.<br/>• **Kinnitatud**: läbirääkimised tarnijaga on lõpetatud ja allhankeleping on kohaletoimetamiseks kinnitatud. <br/>• **Suletud**: allhankelepingu kohaletoimetamine on lõpule viidud.<br/>• **Tühistatud**: allhankeleping tühistati ja tarne pole kavandatud.  | 
    | Valuuta | Valuuta, milles tooted ja teenused ostetakse. Vaikeväärtus sisestatakse hankija kontolt automaatselt, kuid seda saab muuta. | Allhankelepingu valuutat kasutatakse ostu hinnakirja valimiseks kas seotud hankijatele lisatud hinnakirjadest või projekti parameetritest. Allhankelepinguga saab seostada hinnakirju teises valuutas. Aja, kulutuste ja materjalide kulu, mille tarnija ressursid selle allhankelepingu järgi tarnivad, kirjendatakse projektis selles valuutas. Pärast allhankelepingu kirje salvestamist saab allhankelepingu valuutat muuta.|
    | Lepingut sõlmiv üksus | Ettevõtte allüksus, mis sõlmib hankijaga ostulepingu või allhankelepingu. | Pole |
    | Maksetingimused | Selle allhankelepingu raames väljastatud hankija arvete maksetingimused. Vaikeväärtus sisestatakse hankija konto kirjelt automaatselt. | Allhankelepingu maksetingimused kopeeritakse selle allhankelepinguga seotud hankija arvetele. Maksetingimusi saab uuendada, kui allhankeleping on olekus **Mustand**. | 
    | Makse aadress | Hankija aadress, kellele maksed tuleb saata. Vaikeväärtus sisestatakse hankija konto kirjelt automaatselt. | Allhankelepingu makseaadress kopeeritakse makseaadressina kõigile selle allhankelepingu jaoks loodud hankija arvetele. Makseaadressi saab uuendada, kui allhankeleping on olekus **Mustand**.|
    | Maksja nimi | Hankija ettevõtte isiku või allüksuse nimi, kes arve saadab. Vaikeväärtus sisestatakse hankija konto kirjelt automaatselt. | Allhankelepingu väärtus **Maksja nimi** kopeeritakse selle allhankelepinguga seotud hankija arvetele. Seda välja saab uuendada, kui allhankeleping on olekus **Mustand**.|
    | Arve saaja aadress | Hankijalt saadud arvetel kasutatav aadress. Vaikeväärtus sisestatakse hankija konto kirjelt automaatselt. | See aadress on hankija arvetel „arve saatja” aadress, mis on loodud selle allhankelepingu jaoks. |
    | Vahesumma | Kui allhankelepingul ridasid pole, sisestage tellimuse vahesumma enne maksusid. Kui allhankelepingul on ridu, on see väli kirjutuskaitstud. Näidatav summa on allhankelepingu kõikide ridade vahesumma. | Pole |
    | Kogumaks | Kui allhankelepingul ridasid pole, sisestage selle allhankelepingu maksud kokku. Kui allhankelepingul on ridu, on see väli kirjutuskaitstud. Näidatav summa on allhankelepingu kõikide ridade maksude summa. | Pole |
    | Kogusumma | See arvutatud väli kuvab allhankelepingu kogusummat koos maksudega. | Pole |
    | Kinnitamise kuupäev | Allhankelepingu kinnitamise kuupäev. | Pole |
    | Taotleja | Vaikimisi on see väli määratud kasutajanimele, kes allhankelepingu loob. Samas saab allhankelepingu looja väärtust muuta, et näidata isikut, kelle nimel nad allhankelepingu loovad. | Pole |
    | Hankija kontohaldur | hankija konto esmase kontakti nimi. Vaikeväärtus sisestatakse hankija konto kirjelt automaatselt. Võite valida allhankelepingu hankija kontohalduriks erineva lepingu. | Saate seadistada meiliteatisi, et teavitada kontakti, kui allhankelepingule on hinna läbirääkimiste tulemusena tehtud muudatusi. |
