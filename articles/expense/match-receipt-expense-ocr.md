---
title: Kviitungi jäädvustamine OCR-i kasutades
description: See artikkel annab teavet kviitungite tähemärkide optilise tuvastamise (OCR) töötlemise kohta.
author: suvaidya
ms.date: 11/10/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ee16a43fa544af793676072f304d732359d3d9ec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917801"
---
# <a name="capture-a-receipt-using-ocr"></a>Kviitungi jäädvustamine OCR-i kasutades

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Kulude sisetamist on täiustatud kviitungite tähemärkide optilise tuvastamise (OCR) töötlemise juurutamisega. See funktsioon on mõeldud kuluaruannete loomisel kasutuskogemuse parandamiseks.

## <a name="key-features"></a>Põhifunktsioonid

- Süsteem ekstraktib kviitungitelt kaupmehe nime, kuupäeva ja kogusumma.
- Süsteem proovib vastendada mitteseotud kviitungid mitteseotud kulutehingutega.
- Võite kviitungitest luua käsitsi sisestatud kulutehinguid.

## <a name="attach-receipts-to-an-expense-report"></a>Kviitungite manustamine kuluaruande külge

Kui soovite kuluaruande loomisel automaatselt manustada sinna ka krediitkaardi tehingute kviitungid, täitke järgmised etapid.

  1. Avage tööruum **Kuluhaldus**.
  2. Kontrollige vahekaardil **Kviitungid**, kas manustamata kviitungeid on. Vahekaardil **Kviitungid** saate kviitungeid ka üles laadida.
  3. Kontrollige vahekaardil **Kulud**, kas manustamata kulusid on. Tavaliselt impordib kuluhaldur need kulud krediitkaardi pakkujalt.
  4. Valige **Uus kuluaruanne**. Pange tähele, et saate nüüd kuluaruande loomisel kaasata ka kulud ja kviitungid. Kui lisate nii kulud kui ka kviitungid, käivitatakse kviitungite automaatne vastendamine kuludega.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Looge või vastendage kviitungid kuluaruandesse
Kulu loomiseks või kulu kviitungi kaudu vastendamiseks toimige järgmiselt.

  1. Manustage kviitung kuluaruande vahekaardile **Kviitungid**, valides suvandi **Lisa kviitungeid**.
  2. Pange tähele kviitungi üleslaaditud pildi all suvandeid **Loo** ja **Vastenda**.

      - Valige **Loo**, et luua käsitsi sisestatud kulukanne ja täitke arvelt saadud väärtused.
      - Kui valite suvandi **Vastenda**, proovib süsteem vastendada olemasoleva kulu kviitungiga.

## <a name="installation"></a>Installimine

Nende täiustatud kulude võimaluste kasutamiseks installige Microsoft Dynamics 365 Finance jaoks kuluhaldusteenuse lisandmoodul ja lülitage sisse oma eksemplari funktsioonid. Lisandmoodulile pääsete ligi oma projektist teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu.

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

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

**Kas Microsoft kasutab oma mudelite jaoks minu andmeid?**

Ei, Microsoft on oma kviitungite töötlemise teenuse jaoks loonud üldise masinõppe mudeli. See mudel ei põhine teie üleslaetud kviitungitel.

**Kus see funktsioon on saadaval ja töödeldud?**

Selle funktsiooni saadavus erinevates piirkondades on loetletud järgmises tabelis. Kui teie piirkond ei ole hetkel toetatud, esitage taotlus, et seada OCR-teenuse saadavus teie piirkonnas prioriteediks. 

| Regioon | Toetatud                         |
|--------|-----------------------------------|
| USA    | Ja                               |
| CAN    | Ja                               |
| Ühendkuningriigid     | Ja                               |
| AUS    | Ja                               |
| EL     | Osaliselt. Ainult ingliskeelsed kviitungid. |
| Aasia   | No                                |
| Jaapan  | No                                |
| Aafrika | No                                |

**Kuhu minu kviitungid lähevad?**

Finance kontakteerub rakendusega Cognitive Services, et eraldada väljade andmeid. Rakendus Cognitive Services säilitab töötlemisel teie kviitungi koopiat kuni 24ks tunniks. Pärast töötlemise lõpuleviimist eemaldab Cognitive Services kviitungi. Kviitungid talletatakse endiselt rakenduses Finance.

Lisateavet leiate teemast [Kviitungite mõitsmise lubamine vormituvastaja uue võimalusega](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
