---
title: Alltöövõtjate seadistamine broneeritavate ressurssidena
description: Selles teemas kirjeldatakse, kuidas seadistada ja hallata süsteemi kasutajatest ja kontaktidest loodud alltöövõtja ressursse, et neid saaks rakenduses Microsoft Dynamics 365 Project Operations seostada allhankelepingutega.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c765e3c423e440f092c92f9bab75304914b0609447f1dc1c014f98801561b7a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994181"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Alltöövõtjate seadistamine broneeritavate ressurssidena

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Järgige neid juhiseid, et määrata rakenduses Microsoft Dynamics 365 Project Operations alltöövõtjad broneeritavate ressurssidena.

1. Avage **Projekt** \> **Ressursid** ja tehke valik **Uus**.
2. Valige lehe **Uus broneeritav ressurss** väljal **Ressursitüüp** üks järgmistest suvanditest.

    - **Kasutaja** – valige see ressursitüüp, kui alltöövõtjal on vaja rakendusele Project Operations juurdepääsu aja või kulude sisestamiseks. Kui valite suvandi **Kasutaja**, vajab alltöövõtja süsteemile juurdepääsemiseks kehtivat litsentsi.
    - **Kontakt** või **Konto** – valige üks nendest ressursitüüpidest, kui alltöövõtjal pole rakendusele Project Operations vaja juurde pääseda, kuid peab olema saadaval projekti tööülesannete määramiseks või broneeringuteks. Ükski neist ressursitüüpidest ei anna süsteemile juurdepääsu. Valige **Konto**, mis esindab hankija ettevõtet broneeritava ressursina. Valige **Kontakt**, et esindada hankija üksikuid töötajaid.

3. Sõltuvalt valitud ressursitüübist peate valima vastava kasutaja-, konto- või kontaktikirje.
4. Tehke väljal **Töötaja tüüp** valik Lepinguline töötaja, et seadistada alltöövõtja broneeritava ressursina.

    > [!NOTE]
    > Kui jätate välja **Töötaja tüüp** tühjaks, loetakse broneeritavat ressurssi töötajaks.

5. Kui valisite töötaja tüübiks **Lepinguline töötaja**, valige hankija, kelle jaoks ressurss töötab.
6. Valige ressursi ajavöönd ja seejärel tehke valik **Salvesta**. Broneeritavale ressursile töötundide malli määramiseks saate teha loendilehel **Broneeritav ressurss** valiku **Seadista kalender**.

Allhankelepingu reaga seostamiseks peab broneeritav ressurss vastama järgmistele tingimustele.

- Broneeritav ressurss peab olema lepinguline töötaja.
- Broneeritav ressurss ressursitüübiga **Kontakt** peab olema hankija kontoga kontaktina seostatud. Broneeritav ressurss ressursitüübiga **Kasutaja** ei pea olema hankija kontoga kontaktina seostatud.
- Broneeritava ressursi välja **Hankija** väärtus peab vastama alltöövõtja välja **Hankija** väärtusele.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Värskendage töötaja ja hankija vastendamise tüüpi broneeritavate ressursside jaoks

Broneeritava ressursi väli **Töötaja tüüp** määratleb, kas broneeritav ressurss on lepinguline töötaja või töötaja. Väli **Hankija** määratleb hankija konto, millega broneeritav ressurss on seostatud. Seostades broneeritava ressursi hankijaga kontaktina, näitate, et kontakt on hankija ettevõtte töötaja.

Kui broneeritava ressursi välju **Töötaja tüüp** ja **Hankija** muudetakse, mõjutavad muudatused mis tahes tulevasi valideerimisi uutes kirjetes, mida broneeritav ressurss loob, nt ajakirjetes. Muudatused ei muuda kehtetuks olemasolevaid kirjeid.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]