---
title: Projektipõhised müügivõimaluse read
description: Selles teemas antakse teavet projektipõhiste müügivõimaluse ridadega töötamise kohta.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 04e091a58f72a99fb17f37b95f9cac2b4476757b79965177854423361f416d51
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996341"
---
# <a name="project-based-opportunity-lines"></a>Projektipõhised müügivõimaluse read

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_


Projektipõhised müügivõimaluste read on saadaval ainult projektipõhistes müügivõimalustes. Projektipõhise müügivõimaluse kirjetel on välja **Tüüp** väärtuseks seadistatud **Tööpõhine**.

Projektipõhise müügivõimaluse read on reaüksused, mis tarnitakse kliendile projekti abil. Kuid projekti ei saa siduda projektipõhise müügivõimaluse reaga. Projekte saab siduda reaüksustega **Hinnapakkumise** etapist edasi, sest tavaliselt ilmneb müügivõimalus tehingu elutsükli varases staadiumis. Määratlemine, kui palju projekte kasutatakse kliendile töö pakkumiseks, on otsus, mis tehakse müügi etapis hiljem. Müügivõimaluse faasi abil saate tuvastada kliendi jaoks eraldi kohaletoimetamise komponendid. Nende komponentide tarnimiseks kasutatavate projektide tegelikku arvu käsitlevaid otsuseid saab edasi lükata, kuni töö kohta on teada rohkem teavet.

Allpool on projektipõhise müügivõimaluse rea väljad.

| **Väli** | **Asukoht** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- | --- |
| Toote tüüp | Vahekaart Üldine (peidetud) | See on suvandikomplekti väli. Kui teil on Dynamics 365 Operations installitud, on üks saadaolev võimalus **Projektipõhine teenus**.  | Selle välja väärtuseks seatakse **Projektipõhine teenus**, kui loote projektipõhise ridade ruudustiku kaudu projektipõhise müügivõimaluse rea. <br> Kui muudate või alistate selle väärtuse, ei lubata projekti funktsionaalsust teie projektipõhistele reaüksustele. |
| Müügivõimalus | Vahekaart Üldine | See väli on kirjutuskaitstud ja viitab peamise müügivõimaluse kirjele, mille juurde see reaüksus kuulub. | Sellest väljast puudub allavoolu mõju. |
| Nimetus | Vahekaart Üldine | See on muudetav tekstiväli, mida saab kasutada rea üksusele lühikese identiteedi andmiseks | See väärtus viiakse hinnapakkumise reale üle, kui loote selle müügivõimaluse põhjal hinnapakkumise |
| Kliendi eelarve | Vahekaart Üldine | Selle muudetavat valuuta välja abil saab jälgida summat, mida klient on nõus selle reaüksuse eest kulutama. | See väärtus viiakse hinnapakkumise rea vastavale väljale üle, kui loote selle müügivõimaluse põhjal hinnapakkumise |
| Arveldusmeetod | Vahekaart Üldine | Sellel redigeeritaval väljal on järgmised võimalikud väärtused.</br>- Aeg ja materjal</br>- Fikseeritud hind | See väärtus viiakse hinnapakkumise rea vastavale väljale üle, kui loote selle müügivõimaluse põhjal hinnapakkumise. Pärast hinnapakkumise rea loomist on väli lukus ja seda ei saa muuta. Määrake selle välja väärtus nii täpselt kui võimalik. Kui peate hinnapakkumise real selle välja väärtust muutma, kustutage ja looge hinnapakkumise rida uuesti. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]