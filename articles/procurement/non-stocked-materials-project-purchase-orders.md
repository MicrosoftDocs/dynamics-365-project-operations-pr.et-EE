---
title: Projekti jaoks mittelaopõhiste materjalide tellimine ostutellimusi kasutades
description: Selles teemas selgitatakse, kuidas saate tellida projekti jaoks mittelaopõhiseid materjale ostutellimusi kasutades.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563017"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Projekti jaoks mittelaopõhiste materjalide tellimine ostutellimusi kasutades

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Teie organisatsiooni hankeosakond võib kasutada kaupade ja teenuste tellimuste jälgimiseks [ostutellimusi](/dynamics365/supply-chain/procurement/purchase-order-overview). Mittelaopõhiste materjalide ostutellimused saab projektile omistada. Nende müügitellimuste eest arve esitamisel kirjendatakse kulu selle projekti suhtes.

## <a name="prerequisites"></a>eeltingimused
Projekti ostutellimuste funktsiooni lubamiseks läbige järgmised juhised.

1. Avage rakenduses Dynamics 365 Finance tööruum **Funktsioonihaldus**.
2. Leidke funktsioonide loendist ja valige funktsioon **Project Operationsis projekti ostutellimuste lubamine ressursipõhiste/mittelaopõhiste stsenaariumite jaoks**.
3. Valige **Luba**.
4. Konfigureerige mittelaopõhised materjalid ja ootel hankijate arved, nagu on kirjeldatud teemas [Mittelaopõhiste materjalide ja ootel hankija arvete konfigureerimine](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Projekti ostutellimuse loomine projekti ostutellimuste loendist

1. Rakenduses Finance avage **Projektihaldus ja raamatupidamine** > **Projektid** > **Kõik projektid** ja valige projekt.
2. Toimingipaani vahekaardi **Haldus** grupis **Uus** valige **Kauba ülesanne** > **Ostutellimus**.
3. Lehel **Ostutellimuse loomine** valige hankija, kelle jaoks soovite ostutellimuse luua, sisestage muu vajalik teave ja valige seejärel **OK**.
4. Lehel **Ostutellimus** ruudustikus **Ostutellimuse read** valige **Lisa rida**.
5. Sisestage vastavalt vajadusele kauba number, kogus, ühik, ühikuhind ja muu teave.

    > [!NOTE]
    > Projekti ostutellimustega saab kasutada ainult mittelaopõhiseid esemeid ja teenuseid. Laos olevaid esemeid ja hankekategooriaid ei toetata.

6. Jätkake vastavalt vajadusele esemete lisamisega ja kinnitage ostutellimus.

    Kaupade ja teenuste vastuvõtmised saab registreerida toote vastuvõtmise loomise ja kirjendamise kaudu.

    > [!NOTE]
    > Toote vastuvõtmisi ei salvestata teenuse Microsoft Dataverse projekti tegelike andmete seas ja need ei mõjuta projekti alammoodulit.

    Kui tarnija on saatnud ostutellimusel olevate esemete ja teenuste eest arve, saab hankeosakond luua ostutellimuse jaoks arve, avades tegevuspaanil **Arve** > **Loo** > **Arve**. Lisateavet ootel hankijate arvete kohta vt teemast [Mittelaopõhiste materjalide ostmine ootel hankijaarveid kasutades](pending-vendor-invoices.md).
