---
title: Kontsernisisese arvelduse ülevaade
description: Selles teemas on toodud teave ja näited projektide kontsernisisese arveldamise kohta.
author: sigitac
ms.date: 11/19/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b7bb4384657c71552390bbc3d60f3c5d0e4136b4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586247"
---
# <a name="intercompany-invoicing-overview"></a>Kontsernisisese arvelduse ülevaade

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Teie organisatsioonis võib olla mitu allüksust, tütarettevõtet ja muud juriidilist isikut, kes edastavad üksteisele tooteid ja teenuseid projektidele. Teenust või toodet pakkuva juriidilise isiku nimi on *laenu andev juriidiline olem*. Teenust või toodet saava juriidilise isiku nimi on *laenav juriidiline olem*.

Järgmisel joonisel on kujutatud tüüpiline stsenaarium, kus kaks juriidilist olemit Jõgi Robootika USA (laenav juriidiline olem) ja Jõgi Robootika UK (laenu andev juriidiline olem) jagavad ressursse, et viia ellu projekt kliendi Seiklusmängud jaoks. Selle stsenaariumi korral on Jõgi Robootika USA sõlminud lepingu tegema tööd ettevõtte Seikusmängud heaks.

![Kontsernisisesed arved.](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations kasutab kontsernisiseste tehingute töötlemiseks järgmist voogu.

1. Laenu andva juriidilise olemi ressursid kirjendavad kontsernisisesed aja- või kulutehingud broneerides aega ja kulusid laenava juriidilise olemi projektide suhtes.
2. Aja- ja kulumaksumused kirjendatakse laenu andvas ettevõttes, kasutades laenava ettevõtte üksuse omahinnakirja.
3. Kontsernisisesed arveldamata müügitehingud kirjendatakse laenu andvas ettevõttes, kasutades laenava ettevõtte üksuse omahinnakirja.
4. Arveldamata tulu kirjendadatakse laenavas ettevõttes, kasutades projektilepingu müügihinnakirja. Kliendile saab esitada arve arveldamata tulu kirjendamisel. Klient ei pea ootama kontsernisiseste arvete töötlemise lõpuleviimiseni.
5. Kontsernisisesed kliendiarved luuakse laenu andvas ettevõttes perioodiliselt. Arved luuakse käsitsi või perioodiliste automaatsete protsesside abil. Igale laenavale juriidilise olemile saab luua ühe arve või projekti põhjal saab luua eraldi arve.
6. Kui kontsernisisene kliendiarve kirjendatakse laenu andvas juriidilises olemis, luuakse laenavas juriidilises olemis vastav ootel olev hankija arve. Ootel oleva jankija arve kulud kirjendatakse projekti pearaamatus, kui arve sisestatakse.

Järgmisel joonisel on toodud kontsernisisene arveldamine, kuna see on seotud raamatupidamise sündmustega ja eeldatavate pearaamatu sisestustega.

![Kontsernisisene voog.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Lisaressursid

- [Kontsernisisese arveldamise konfigureerimine](configure-intercompany-invoicing.md)
- [Kontsernisiseste kannete kirjendamine](create-intercompany-transactions.md)
- [Kontsernisisese kliendi ja hankija arvete loomine](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]