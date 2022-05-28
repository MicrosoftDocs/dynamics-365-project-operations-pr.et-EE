---
title: Projekti jaoks mittelaopõhiste materjalide tellimine ostutellimusi kasutades
description: Selles teemas selgitatakse, kuidas saate tellida projekti jaoks mittelaopõhiseid materjale ostutellimusi kasutades.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2aa8fb94e2f9cbf91182f3f169339284d3eb9f44
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612698"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Projekti hankekategooriate või ladustamata materjalide tellimine projekti ostutellimuste abil

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Teie organisatsiooni hankeosakond võib kasutada kaupade ja teenuste tellimuste jälgimiseks [ostutellimusi](/dynamics365/supply-chain/procurement/purchase-order-overview). Hankekategooriate või laoväliste materjalide ostutellimusi võib seostada projektiga. Nende müügitellimuste eest arve esitamisel kirjendatakse kulu selle projekti suhtes.

## <a name="prerequisites"></a>eeltingimused
Projekti ostutellimuste funktsiooni lubamiseks läbige järgmised juhised.

1. Avage Dynamics 365 Finance **funktsioonihalduse** tööruum.
2. Leidke funktsioonide loendist ja valige funktsioon **Project Operationsis projekti ostutellimuste lubamine ressursipõhiste/mittelaopõhiste stsenaariumite jaoks**.
3. Valige **Luba**.
4. Konfigureerige mittelaopõhised materjalid ja ootel hankijate arved, nagu on kirjeldatud teemas [Mittelaopõhiste materjalide ja ootel hankija arvete konfigureerimine](configure-materials-nonstocked.md).
5. Konfigureerige hankekategooriad nii, nagu on kirjeldatud jaotises [Hankekategooriate kasutamine projekti ostutellimuste ja ootel hankija arvetega](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Projekti ostutellimuse loomine projekti ostutellimuste loendist

1. Rakenduses Finance avage **Projektihaldus ja raamatupidamine** > **Projektid** > **Kõik projektid** ja valige projekt.
2. Toimingipaani vahekaardi **Haldus** grupis **Uus** valige **Kauba ülesanne** > **Ostutellimus**.
3. Lehel **Ostutellimuse loomine** valige hankija, kelle jaoks soovite ostutellimuse luua, sisestage muu vajalik teave ja valige seejärel **OK**.
4. Lehel **Ostutellimus** ruudustikus **Ostutellimuse read** valige **Lisa rida**.
5. Sisestage vastavalt vajadusele kauba number või hankekategooria, kogus, ühik, ühiku hind ja muu teave.

    > [!NOTE]
    > Projekti ostutellimustega saab kasutada ainult hankekategooriaid, ladustamata kaupu ja teenuseid. Ladustatud kaupu ei toetata.

6. Jätkake kaupade või hankekategooriate lisamist vastavalt vajadusele ja kinnitage ostutellimus.

    Kaupade ja teenuste vastuvõtmised saab registreerida toote vastuvõtmise loomise ja kirjendamise kaudu.

    > [!NOTE]
    > Toote vastuvõtmisi ei salvestata teenuse Microsoft Dataverse projekti tegelike andmete seas ja need ei mõjuta projekti alammoodulit.

    Kui tarnija on saatnud ostutellimusel olevate esemete ja teenuste eest arve, saab hankeosakond luua ostutellimuse jaoks arve, avades tegevuspaanil **Arve** > **Loo** > **Arve**. Lisateavet ootel hankijate arvete kohta vt teemast [Mittelaopõhiste materjalide ostmine ootel hankijaarveid kasutades](pending-vendor-invoices.md).
