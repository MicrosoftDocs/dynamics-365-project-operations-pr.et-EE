---
title: Projekti jaoks mittelaopõhiste materjalide tellimine ostutellimusi kasutades
description: See artikkel selgitab, kuidas saate tellida projekti jaoks mittelaopõhiseid materjale kasutades ostutellimusi.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929807"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Projekti jaoks hanke kategooriate või mittelaopõhiste materjalide tellimine kasutades ostutellimusi

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Teie organisatsiooni hankeosakond võib kasutada kaupade ja teenuste tellimuste jälgimiseks [ostutellimusi](/dynamics365/supply-chain/procurement/purchase-order-overview). Hanke kategooriate või mittelaopõhiste materjalide ostutellimused saab projektile omistada. Nende müügitellimuste eest arve esitamisel kirjendatakse kulu selle projekti suhtes.

## <a name="prerequisites"></a>eeltingimused
Projekti ostutellimuste funktsiooni lubamiseks läbige järgmised juhised.

1. Minge rakenduses Dynamics 365 Finance tööruumi **Funktsioonide haldus**.
2. Leidke funktsioonide loendist ja valige funktsioon **Project Operationsis projekti ostutellimuste lubamine ressursipõhiste/mittelaopõhiste stsenaariumite jaoks**.
3. Valige **Luba**.
4. Konfigureerige mittelaopõhised materjalid ja ootel hankijate arved, nagu on kirjeldatud teemas [Mittelaopõhiste materjalide ja ootel hankija arvete konfigureerimine](configure-materials-nonstocked.md).
5. Hankekategooriate konfigureerimine, nagu on kirjeldatud jaotises [Hankekategooriate kasutamine projekti ostutellimuste ja ootel hankija arvetega](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Projekti ostutellimuse loomine projekti ostutellimuste loendist

1. Rakenduses Finance avage **Projektihaldus ja raamatupidamine** > **Projektid** > **Kõik projektid** ja valige projekt.
2. Toimingipaani vahekaardi **Haldus** grupis **Uus** valige **Kauba ülesanne** > **Ostutellimus**.
3. Lehel **Ostutellimuse loomine** valige hankija, kelle jaoks soovite ostutellimuse luua, sisestage muu vajalik teave ja valige seejärel **OK**.
4. Lehel **Ostutellimus** ruudustikus **Ostutellimuse read** valige **Lisa rida**.
5. Sisestage vastavalt vajadusele kauba number või hankekategooria, kogus, ühik, ühikuhind ja muu teave.

    > [!NOTE]
    > Projekti ostutellimustega saab kasutada ainult hankekategooriaid, mittelaopõhiseid kaupu ja teenuseid. Laopõhiseid kaupu ei toetata.

6. Jätkake vastavalt vajadusele esemete lisamisega või hankekategooriatega ja kinnitage ostutellimus.

    Kaupade ja teenuste vastuvõtmised saab registreerida toote vastuvõtmise loomise ja kirjendamise kaudu.

    > [!NOTE]
    > Toote vastuvõtmisi ei salvestata teenuse Microsoft Dataverse projekti tegelike andmete seas ja need ei mõjuta projekti alammoodulit.

    Kui tarnija on saatnud ostutellimusel olevate esemete ja teenuste eest arve, saab hankeosakond luua ostutellimuse jaoks arve, avades tegevuspaanil **Arve** > **Loo** > **Arve**. Lisateavet ootel hankijate arvete kohta vt teemast [Mittelaopõhiste materjalide ostmine ootel hankijaarveid kasutades](pending-vendor-invoices.md).
