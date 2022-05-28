---
title: Kuludokumentide töötlemine
description: Selles teemas antakse teavet kviitungite tähemärkide optilise tuvastamise (OCR) töötlemise kohta. Selle funktsiooni eesmärk on parandada kasutajakogemust kuluaruannete loomisel rakenduses Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 067432106742447d2b8fa215ec05bf05f4b41e70
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684315"
---
# <a name="expense-receipt-processing"></a>Kuludokumentide töötlemine

Kulude sisetamist on täiustatud kviitungite tähemärkide optilise tuvastamise (OCR) töötlemise juurutamisega. See funktsioon on mõeldud kuluaruannete loomisel kasutuskogemuse parandamiseks.

## <a name="key-features"></a>Põhifunktsioonid

- Kviitungitelt ekstraktitakse kaupmehe nim, kuupäev ja kogusumma.
- Funktsioon proovib vastendada mitteseotud kviitungid mitteseotud kulutehingutega.
- Kasutajad võivad kviitungitest luua käsitsi sisestatud kulutehinguid.

## <a name="usage-examples"></a>Näited kasutuse kohta

Kui soovite kuluaruande loomisel automaatselt manustada sinna ka krediitkaardi tehingute kviitungid, tehke järgmist.

  1. Avage tööruum **Kuluhaldus**.
  2. Kontrollige vahekaardil **Kviitungid**, kas manustamata kviitungeid on. Vahekaardil **Kviitungid** saate kviitungeid ka üles laadida.
  3. Kontrollige vahekaardil **Kulud**, kas manustamata kulusid on. Tavaliselt impordib kuluhaldur need kulud krediitkaardi pakkujalt.
  4. Valige **Uus kuluaruanne**. Pange tähele, et saate nüüd kuluaruande loomisel kaasata ka kulud ja kviitungid. Kui lisate nii kulud kui ka kviitungid, käivitatakse kviitungite automaatne vastendamine kuludega.

Kulu loomiseks või kulu kviitungi kaudu vastendamiseks tehke järgmist.

  1. Manustage kviitung kuluaruande vahekaardile **Kviitungid**, valides suvandi **Lisa kviitungeid**.
  2. Pange tähele kviitungi üleslaaditud pildi all suvandeid **Loo** ja **Vastenda**.

      - Valige **Loo**, et luua käsitsi sisestatud kulukanne ja täitke arvelt saadud väärtused.
      - Kui valite suvandi **Vastenda**, proovib süsteem vastendada olemasoleva kulu kviitungiga.

## <a name="installation"></a>Installimine

See funktsioon töötab koos funktsiooniga **Kuluaruannete ümberkujundamine**, et aidata lihtsustada kulu kogemust. See funktsioon on saadaval ainult Tier 2+ keskkondades, milleks on on Liivakasti ja tootmine.

Nende täiustatud kuluvõimaluste kasutamiseks installige 365 Finance'i lisandmoodul Microsoft Dynamics Kuluhaldusteenus ja lülitage oma eksemplari funktsioonid sisse. Lisandmoodulile pääsete ligi oma projektist teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu.

1. Logige LCS-i sisse ja avage soovitud keskkond.
2. Minge jaotisse **Kõik üksikasjad**.
3. Valige käsk **Säilita** või Kerige alla kiirkaardile **Keskkonna lisandmoodulid**.
4. Valige käsk **Installi uus lisandmoodul**.
5. Valige jaotis **Kuluhaldusteenus**.
6. Järgige installiviisardi juhiseid ja nõustuge tingimustega.
7. Valige käsk **Installi**.

Lülitage välja tööruumis **Funktsioonide haldus** sisse järgmised funktsioonid.

- Ümberkujundatud kuluaruanded
- Automaatne vastendamine ja kviitungist kulu loomine

Nende funktsioonide sisselülitamisel tehakse järgmised toimingud.

- Olemasolev tööruum **Kuluhaldus** asendatakse uue tööruumiga.
- Lisatakse uus menüü element kulu välja nähtavuse kohta.
- Saate siiski avada eelmise lehe **Kuluaruanded**, avades jaotise **Kuluhaldus > Minu kulud > Kuluaruanded**.
- Töövood ja kõik kinnitused viivad teid ikka olemasolevate kuluaruannete lehele.
- Kviitungeid töödeldakse Microsoft Azure Cognitive Services'i kaudu ja metaandmed eraldatakse ning lisatakse.
- Lisatakse suvand, mis võimaldab luua kuluaruande, mis sisaldab vastendatud kinnitamata kviitungeid.
- Suvand, mis lisatakse kuluaruannetesse, võimaldab teil luua kviitungi põhjal kulurea või üritab vastendada olemasoleva kviitungi olemasoleva kulureaga.

Lisateavet kuluaruannete ümberkujundamise funktsiooni kohta leiate teemast [Kuluaruannete ümberkujundamine](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

**Kas Microsoft kasutab oma mudelite jaoks minu andmeid?**

Ei, Microsoft on oma kviitungite töötlemise teenuse jaoks loonud üldise masinõppe mudeli. See mudel ei põhine teie üleslaetud kviitungitel.

**Kus see funktsioon on saadaval ja töödeldud?**

Praegu toetatakse seda Ameerika Ühendriikides.

**Kuhu minu kviitungid lähevad?**

Finance kontakteerub rakendusega Cognitive Services, et eraldada väljade andmeid. Rakendus Cognitive Services säilitab töötlemisel teie kviitungi koopiat kuni 24ks tunniks. Pärast töötlemise lõpuleviimist eemaldab Cognitive Services kviitungi. Kviitungid talletatakse endiselt rakenduses Finance.

Lisateavet leiate teemast [Kviitungite mõitsmise lubamine vormituvastaja uue võimalusega](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]