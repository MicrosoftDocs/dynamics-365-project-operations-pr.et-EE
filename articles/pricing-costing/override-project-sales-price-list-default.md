---
title: Projekti müügi hinnakirjade tühistamine
description: See teema sisaldab teavet kohandatud müügi hinnakirjade loomise kohta.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: af9baca540d89f4e5e616bdfdd6111bef29abe28
ms.sourcegitcommit: 656a9d03f260c29e988e2ff05b6e07ae0365d6d0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672226"
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