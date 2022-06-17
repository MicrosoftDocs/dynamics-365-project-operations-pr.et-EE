---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 33, V3
description: Selles artiklis loetletakse funktsioonid ja parandused, mis on saadaval project service automation update release 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d9c282e8b95b111ce71fb441e4dbb2d04f904e0f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915411"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse funktsioonid ja parandused, mis on project service automation V3, Update Release 33 jaoks uued või muudetud. Selle versiooni järgunumber on V3.10.54.98 ja see on üldsusele isevärskenduse kaudu kättesaadav juulis 2021.

## <a name="update-release-33"></a>Värskenduste väljalase 33

### <a name="bug-fixes"></a>Veaparandused

**Aeg ja kulu**

Lahendatud on järgmised probleemid.

- Kaks lukus välja **msdyn_description** ja **msdyn_externaldescription** on pärast esitamist redigeeritavad.
- Kuvatakse tõrketeade, kui luuakse kulu, mis pole projektiga seotud.
- Ajakirje loomisel muutub ressursi roll passiivseks rolliks.
- Tagasi võetud ja kustutatud kuluga seotud töölehe ridasid ei kustutata.
- Värskendage suvandis **Ajakirje kiirloomisvorm** vaadet **Projktiülesande loend**, et muuta vaikimisi kuvatav kuupäev ülesande algusuupäevaks.
- Kui loote ajakirje broneeritatava ressursi vahekaardil **Seotud**, luuakse ajakirje valesti sisselogitud kasutaja jaoks, mitte broneeritava ülemressursi jaoks.
- Dialoogiboksi **Hulgikinnitamise MDD** jaoks lisatakse uued väljad.

**Projekti kavandamine**

Lahendatud on järgmised probleemid.
- Projekti loomise aeglane jõudlus, kui projekti töötunnimalle rakendatakse keerukate kalendritega.
- Kui alguskuupäev on lõpukuupäevast suurem, kuvatakse koopia projektimallis iga välja kellaaja komponendi erinevuse tõttu tõrge.

**Ressursihaldus**

Lahendatud on järgmised probleemid.
- Ressursikasutuse päringus kasutatakse vale parameetrit ja XML toob ruudustikus **Ressursikasutus** kaasa valed filtritulemused.
- Kinnitus **Broneeringute laiendamne** kuvab broneeringute jaoks vale lõpukuupäeva.

**Müük**

Lahendatud on järgmised probleemid.
- Kui kategooria hind luuakse puuduvate väärtustega, kuvatakse tõrketeade.
- Kui lepingurea vahe-eesmärk luuakse ilma tellimuse reata, kuvatakse tõrketeade.
