---
title: Tulu kajastamise ülevaade
description: Selles artiklis antakse teavet tulude tuvastamise kohta Project Operationsis.
author: sigitac
ms.date: 11/16/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 22486693226256f765589b272e6df36aceaf9c1c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926265"
---
# <a name="revenue-recognition-overview"></a>Tulu kajastamise ülevaade

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Rakenduses Dynamics 365 Project Operations erinevad tulu kajastamise põhimõtted projekti või projekti osa valitud arveldusmeetodi põhjal. Selles artiklis antakse teavet tulude tuvastamise kohta Project Operationsis.

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