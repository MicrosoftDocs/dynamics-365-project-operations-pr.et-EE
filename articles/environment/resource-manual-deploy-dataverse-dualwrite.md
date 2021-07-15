---
title: Rakenduse Project Operations Dataverse käsitsi juurutamine koos topeltkirjutuse toega
description: Selles teemas selgitatakse, kuidas rakendust Project Operations Dataverse käsitsi juurutada, et see toetaks topeltkirjutamist.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274003"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Rakenduse Project Operations Dataverse käsitsi juurutamine koos topeltkirjutuse toega

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles teemas selgitatakse, kuidas juurutada käsitsi rakendust Microsoft Dynamics 365 Project Operations teenuses Microsoft Dataverse, et see toetaks topeltkirjutamist. Project Operations tuvastab keskkonna konfiguratsiooni ja lisab eeltingimuste täitumisel topeltkirjutamise lisatoe.

Kui olete teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu juurutamise ajal järginud selles teemas toodud juhiseid, saate Microsoft Power Platformi integratsiooni juurutamise (varem tuntud kui Common Data Service keskkond) vahele jätta.

Project Operationsi teenuses Dataverse juurutamise protsess, et see toetaks topeltkirjutust, omab nelja peamist etappi.

1. [Looge teenuses Dataverse uus keskkond, mis toetab topeltkirjutust](#create).
2. [Lisage keskkonnale topeltkirjutuse eeltingimused](#prerequisites).
3. [Lisage rakendus Project Operations Dataverse](#dataverse).
4. [Siduge oma keskkonnad](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Teenuses Dataverse uue keskkonna loomine, mis toetab topeltkirjutust

Selle toimingu lõpuleviimiseks peate administraatorina sisse logima.

1. Avage [Power Platformi halduskeskus](https://admin.powerplatform.com) ja logige administraatorina sisse.
2. Looge uus keskkond ja pange sellele nimi.
3. Valige keskkonna tüüp. Kui registreerusite prooviversiooni jaoks, valige **Prooviversioon (kordustellimusel põhinev)**.
4. Kinnitage juurutuspiirkond.
5. Lubage suvand **Loo selle keskkonna joaks andmebaas**. 
6. Kinnitage keel ja seejärel kontrollige, kas valuuta ühtib teie rakenduste Finance and Operations valuutaga.
7. Lubage suvand **Dynamics 365 rakendused** ja veenduge, et välja **Juuruta need rakendused automaatselt** väärtuseks oleks seatud **Puudub**.
8. Lisage turberühm, kui turberühm on nõutav.
9. Keskkonna loomiseks valige nupp **Salvesta**.
10. Oodake, kuni juurutamine on lõpule jõudnud ja keskkond jõuab olekusse **Valmis**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Keskkonnale topeltkirjutuse eeltingimuste lisamine

Topeltkirjutuse tugi sisaldab lisavälju, mis põhiolemitele lisatakse, näiteks olem **Ettevõte**. Kui lisate olemasolevasse keskkonda topeltkirjutamise toe, peate võib-olla toe lubamiseks andmeid värskendama. Lisateavet andmete alglaadimise kohta vaadake teemast [Ettevõtte andmete alglaadimine](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Lisateavet topeltkirjutamise kohta vaadake teemast [Topeltkirjutamise süsteemi nõuded](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Viige see toiming lõpule, et lisada oma keskkonda topeltkirjutuse eeltingimused.

1. Avage äsja loodud keskkond ja avage seejärel **Ressurss** \> **Dynamics 365 rakendused**.
2. Valige rakenduste loendist **Topeltkirjutuse tuumlahendus** ja installige see.
3. Oodake, kuni installimine on lõpule jõudnud. Seejärel valige rakenduste loendist **Topeltkirjutuse rakendamise korraldamise lahendus** ja installige see.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Rakenduse Project Operations Dataverse lisamine

Selle toimingu saate teha ainult juhul, kui olete enne Project Operationsi installimist teinud eelnevad toimingud. Installimise ajal analüüsib süsteem keskkonna konfiguratsiooni ja lisab vajaduse korral topeltkirjutuse toe.

1. Avage varem loodud keskkond ja avage seejärel **Ressurss** \> **Dynamics 365 rakendused**.
2. Valige rakenduste loendist **Microsoft Dynamics 365 Project Operations** ja installige see.

## <a name="link-your-environments"></a><a name="link"></a>Keskkondade sidumine

Pärast Dataverse’i keskkonna juurutamist saate häälestada oma Finance and Operationsi rakendustes seose. Järgige juhiseid teemas [Oma keskkondade sidumiseks topeltkirjutuse viisardi kasutamine](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
