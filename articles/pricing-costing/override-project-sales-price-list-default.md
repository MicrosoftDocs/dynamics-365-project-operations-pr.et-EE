---
title: Projekti müügi hinnakirjade tühistamine
description: Selles artiklis antakse teavet kohandatud müügihinnakirjade loomise kohta.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8d0a769f415679b08f3228fcb14fbbbd37533ebc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911913"
---
# <a name="override-project-sales-price-lists"></a>Projekti müügi hinnakirjade tühistamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

## <a name="customer-specific-project-price-lists"></a>Kliendipõhise projekti hinnakiri

Rakenduses Dynamics 365 Project Operations on võimalik seadistada kliendipõhised hinnakirja kokkulepped konto kirje projekti hinnakirjadeks.

Alas **Müük** kliendipõhise hinnakirja seadistamiseks liikuge konto kirjele.

1. Avage loendi leht **Kontod**.
2. Leidke ja topeltklõpsake kliendi kirjet, et avada suvandi **Konto** üksikasjade leht.
3. Vahekaardil **Projekti hinnakirjad** valige **+ Uus projekti hinnakiri**.
4. Valige lehel **Uus projekti hinnakiri** rippmenüüst hinnakiri. Seal sisalduvad ainult hinnakirjad, mille kontekstiks on määratud **Müük** ja mille valuuta vastab konto valuutale.
5. Pange seosele nimi ja valige seejärel käsk **Salvesta**. Luuakse kliendipõhine projekti hinnakiri. Seda hinnakirja kasutatakse projekti hinnapakkumistes projekti hindade või selle kliendi jaoks loodud lepingute vaikeväärtuste jaoks, kus hinnapakkumise või projektilepingu loomise kuupäev jääb hinnakirja kehtivuse kuupäevavahemikku.

## <a name="custom-pricing-on-project-quotes"></a>Projekti hinnapakkumiste kohandatud hinnakujundus

Projekti hinnapakkumistes võib teil olla projekti hinnakujundus, mis algab vaikimisi standardse hinnakirjaga, mile vaikeväärtused pärinevad kliendilt või projekti parameetritest.

Kui vajate konkreetse hinnapakkumise projektiga seotud töö jaoks kohandatud hinda, saate hankida selle seostatud olemi projekti hinnakirjadest.

Hinnapakkumisele spetsiifilise projekti hinnakujunduse häälestamiseks tehke järgmist.

1. Avage projekti hinnapakkumine ja valige vahekaart **Projekti hinnakirjad**.
2. Valige andmeruudustikus suvand **Loo kohandatud hinnakujundus**.

Kõik hinnapakkumisega seotud projekti hinnakirjad kopeeritakse uutesse hinnakirjadesse. Uute hinnakirjade nimed kajastavad hinnapakkumise nime koos hinnakirjade loomise ajatempliga.

Saate kasutada iga sellist hinnakirja ja teha kohandusi töö (rolli hind) ja kulu (kategooria hind) hindadele. Need hinnad kehtivad ainult sellele projekti hinnapakkumisele.

## <a name="price-lists-on-a-project-contract"></a>Projektilepingu hinnakirjad

Projektilepingus on projekti hinnakujunduse vaikeväärtused alati pärit lepingu nimega kohandatud hinnakirjast ja luuakse nimele lisatud ajatempliga. See on tõene, kui leping loodi hinnapakkumise võitmise ajal või kui leping loodi nullist. Vajaduse korral saate selle kohandatud hinnakirjaga seose eemaldada ja seostada selle asemel projektilepinguga standardse hinnakirja.

Kui seostate hinnapakkumise või lepingu projekti hinnakirjad standardse hinnakirjaga, mõjutavad kõik hinnakirja hindade muudatused kõiki hinnapakkumisi ja lepinguid, mis seda hinnakirja kasutavad.


[!INCLUDE[footer-include](../includes/footer-banner.md)]