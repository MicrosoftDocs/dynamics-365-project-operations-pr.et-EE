---
title: Tulu kajastamise ülevaade
description: Selles teemas antakse teavet tulu kajastamise kohta rakenduses Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 3d2fcf434a5086595e40f50afc2366eb806168085ae9212b5d25e3e9bd02e2c6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988646"
---
# <a name="revenue-recognition-overview"></a>Tulu kajastamise ülevaade

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Rakenduses Dynamics 365 Project Operations erinevad tulu kajastamise põhimõtted projekti või projekti osa valitud arveldusmeetodi põhjal. Selles teemas antakse teavet tulu kajastamise kohta rakenduses Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Aja ja materjali arveldusmeetodi kasutavad arvestatavad kanded

- Kulude ja tulude kajastamine on seotud. Tehingu kulu ja arveldamata müük sisestatakse kasutades [Project Operationsi integreerimise töölehte](../project-accounting/project-operations-integration-journal.md).
- Projekti kulu ja tulu profiil määratlevad, kas arveldamata müügi kanded sisestatakse pearaamatusse. Kui valitud on **Viitlaekumine**, kasutab süsteem sisestamise ajal kontosid **WIP müügiväärtus** ja **Viitlaekumise müügiväärtus**. Järgnev on selle meetodi näide.  

  | Kande tüüp | Deebet/kreedit | Summa |
  | --- | --- | --- |
  | WIP müügiväärtus | Deebet | 100 |
  | Viittulu müügiväärtus | Kreedit | 100 |

- Tulu kajastatakse arveldamise ajal. Süsteem kasutab kirjendamise ajal kontot **Arveldatud tulu**. Järgnev on selle meetodi näide.  

  | Kande tüüp | Deebet/kreedit | Summa |
  | --- | --- | --- |
  | Kliendi saldo | Deebet | 120 |
  | Tasutav käibemaks | Kreedit | 20 |
  | Arveldatud tulu | Kreedit | 100 |

- Kui tulu kajastatakse arveldamata müügi kirjendamise ajal, pöörab süsteem arveldamise ajal viitlaekumise ümber.

  | Kande tüüp | Deebet/kreedit | Summa |
  | --- | --- | --- |
  | WIP müügiväärtus | Kreedit | 100 |
  | Viittulu müügiväärtus | Deebet | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Fikseeritud hinnaga arveldusmeetodi kasutavad arvestatavad kanded

- Kulude ja tulude kajastamine on eraldi. Tehingu kulu sisestatakse kasutades [Project Operationsi integreerimise töölehte](../project-accounting/project-operations-integration-journal.md). Arveldamata müügitehinguid ei looda.
- Tulu saab kajastada arveldamise ajal, kui projektikulu ja tuluprofiilis on suvand **Projekti lõpule viimise arvutamiseks kasutatud põhimõte** on määratud valikule **Pole WIP**. Kasutage seda meetodit ainult lühiajaliste lihtsate projektide jaoks.
- Tulu saab kajastada kasutades fikseeritud hinnaga tulukalkulatsioone kas meetodiga **Lõpetatud leping** või **Tulu kajastamise lõpetamise protsent**.

## <a name="additional-resources"></a>Lisaressursid
[Arveldatavate projektide raamatupidamise konfigureerimise artikkel](../project-accounting/configure-accounting-billable-projects.md)

[Fikseeritud hinnaga tulukalkulatsiooni projektid](rev-rec-percentage-completion-method.md)

[Tulukalkulatsioonide haldamine](rev-rec-completed-contract-method.md)

[Kulu meetodi lõpetamiseks](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]