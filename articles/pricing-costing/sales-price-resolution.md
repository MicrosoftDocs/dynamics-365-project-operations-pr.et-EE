---
title: Projektipõhiste prognooside ja tegelike hindade müügihindade määramine
description: Selles artiklis antakse teavet selle kohta, kuidas määratakse projektipõhiste prognooside ja tegelike näitajate müügihinnad.
author: rumant
ms.date: 09/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f0b95c651983230cbf340f2c06089a287b2c8a10
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475364"
---
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Projektipõhiste prognooside ja tegelike hindade müügihindade määramine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Microsofti Dynamics 365 Project Operations prognooside ja tegelike hindade määramiseks kasutab süsteem esmalt kuupäeva ja valuutat sissetulevas hinnangus või tegelikus kontekstis, et määrata kindlaks müügihinnakiri. Konkreetselt tegelikus kontekstis kasutab **süsteem tehingu kuupäeva** välja, et määrata, milline hinnakiri on rakendatav. **Sissetuleva või tegeliku hinnangu tehingukuupäeva** väärtust võrreldakse hinnakirjas olevate **väärtustega Efektiivne algus (sõltumatu ajavöönd)** ja **Efektiivne lõpp (sõltumatu ajavöönd**). Pärast hinnakirja määramist määrab süsteem müügi- või arvemäära.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Müügimäärade määramine tegelikel ja hinnangulistel ridadel aja jaoks

Aja **hinnanguline kontekst** viitab:

- Hinnapakkumise rea üksikasjad aja **kohta**.
- Lepingu rea üksikasjad aja **kohta**.
- Projekti ressursside määramised.

Aja **tegelik kontekst** viitab:

- Sissekande ja paranduse töölehe read aja **jaoks**.
- Tööleheread, mis luuakse ajakirje edastamisel.
- Arve rea üksikasjad aja **kohta**. 

Pärast müügi hinnakirja määramist teeb süsteem arve vaikemäära sisestamiseks järgmised toimingud.

1. Süsteem vastab väljade **Roll**, **Resourcing Company** ja **Resourcing Unit** kombinatsioonile hinnangus või tegelikus kontekstis ajas **ja** hinnakirjas olevate rolli hinnaridade suhtes. See vaste eeldab, et kasutate arvehindade jaoks valmishinna dimensioone. Kui olete konfigureerinud hinnakujunduse nii, et see põhineb muudel väljadel peale rolli **,** ettevõtte **ja ressursiüksuse** või **nende kõrval**, kasutatakse seda väljade kombinatsiooni vastava rolli hinnarea toomiseks.
1. Kui süsteem leiab rolli hinnarea, millel on arve määr kombinatsioonide Roll **,** Resourcing Company **ja** Resourcing Unit **jaoks**, kasutatakse seda arve määra vaikearve määrana.

> [!NOTE]
> Kui konfigureerite väljade **Roll**, **Resourcing Company** ja **Resourcing Unit** erineva prioriseerimise või kui teil on muid kõrgema prioriteediga dimensioone, muutub eelnev käitumine vastavalt. Süsteem toob rolli hinnakirjed, mille väärtused vastavad igale hinnadimensiooni väärtusele prioriteedi järjekorras. Read, millel on nende dimensioonide jaoks nullväärtused, jäävad viimaseks.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Müügimäärade määramine kulu tegelikel ja hinnangulisel ridadel

Hinnanguline kulukontekst **viitab**:

- Hinnapakkumise rea üksikasjad kulu **kohta**.
- Lepingu rea üksikasjad kulu **jaoks**.
- Projekti kuluprognoosi read.

Kulu **tegelik kontekst** viitab järgmisele:

- Sissekande ja paranduse töölehe read kulu **jaoks**.
- Töölehe read, mis luuakse kulukirje esitamisel.
- Arve rea üksikasjad kulu **jaoks**. 

Pärast müügi hinnakirja määramist täidab süsteem ühiku vaikehinna sisestamiseks järgmised toimingud.

1. Süsteem sobitab väljade **Kategooria** ja **Ühik** kombinatsiooni kulu **hinnangulisel real** hinnakirjas olevate kategooria hinnaridade suhtes.
1. Kui süsteem leiab kategooria hinnarea, millel on kategooria **ja** ühiku **kombinatsiooni müügimäär**, kasutatakse seda müügimäära vaikemüügimäärana.
1. Kui süsteem leiab vastava kategooria hinnarea, võidakse vaikemüügihinna sisestamiseks kasutada hinnakujundusmeetodit. Järgmises tabelis on näidatud project operationsi kuluhindade vaikekäitumine.

    | Kontekst | Hinnakujundusmeetod | Vaikimisi hind |
    | --- | --- | --- |
    | Hinnang | Ühiku hind | Põhineb kategooria hinnajoonel. |
    |        | Omahinnaga | 0.00 |
    |        | Juurdehindlus üle omahinna | 0.00 |
    | Tegelik | Ühiku hind | Põhineb kategooria hinnajoonel. |
    |        | Omahinnaga | Põhineb tegelikel seotud kuludel. |
    |        | Juurdehindlus üle omahinna | Kategooria hinnareas määratletud juurdehindlus rakendatakse tegeliku seotud kulu ühikukulumäärale. |

1. Kui süsteem ei **vasta kategooriate** ja **ühiku** väärtustele, määratakse müügimääraks **vaikimisi 0** (null).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Müügimäärade määramine materjali tegelikel ja hinnangulistel ridadel

Materjali **hinnanguline kontekst** viitab:

- Hinnapakkumise rea üksikasjad materjali **jaoks**.
- Lepingu rea üksikasjad materjali **jaoks**.
- Projekti materjali hinnanguread.

Materjali **tegelik kontekst** viitab:

- Sissekande ja paranduse töölehe read materjali **jaoks**.
- Tööleheread, mis luuakse materjali kasutamise logi esitamisel.
- Arve rea üksikasjad materjali **jaoks**. 

Pärast müügi hinnakirja määramist täidab süsteem ühiku vaikehinna sisestamiseks järgmised toimingud.

1. Süsteem sobitab materjali **hinnangureal** olevate väljade Toode **ja** Ühik **kombinatsiooni** hinnakirja kaubaridade suhtes.
1. Kui süsteem leiab hinnakirja kaubarea, millel on toote ja ühiku **kombinatsiooni müügimäär, ja kui hinnastamismeetodiks** on **Valuutasumma**, kasutatakse hinnakirja real määratud müügihinda.**·** 
1. **Kui väljade Toode** ja **Ühik** väärtused ei ole vasted või kui hinnakujundusmeetod on midagi muud kui **valuutasumma**, määratakse müügimääraks **vaikimisi 0** (null). Selline käitumine ilmneb seetõttu, et Project Operations toetab ainult **valuutasumma** hinnastamise meetodit materjalide puhul, mida projektis kasutatakse.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
