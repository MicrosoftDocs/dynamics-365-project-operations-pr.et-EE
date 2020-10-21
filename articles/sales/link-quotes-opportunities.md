---
title: Projekti hinnapakkumiste loomine müügivõimalustest
description: Selles teemas antakse teavet müügivõimalusest projekti hinnapakkumise loomise kohta.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898527"
---
# <a name="create-project-quotes-from-opportunities"></a>Projekti hinnapakkumiste loomine müügivõimalustest

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Hinnapakkumisi saab luua projekti müügivõimalustest järgmistel viisidel.

- Lehe **Projekti müügivõimalus** vahekaardilt **Hinnapakkumised**
- Müügivõimaluse müügiprotsessi voost
- Olemasoleva hinnapakkumise müügivõimaluse viidet värskendades

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>Projekti müügivõimaluse lehe vahekaardilt Hinnapakkumised

Müügivõimalusest projekti hinnapakkumise loomiseks tehke järgmist.

1. Avage leht **Projekti müügivõimalus** ja valige vahekaart **Hinnapakkumised**. 
2. Valige andmeruudustikus **Hinnapakkumised** suvand **+**, et luua müügivõimaluse põhjal uus projekti hinnapakkumine. Kõik müügivõimaluste read ja seotud projekti hinnakirjad kopeeritakse müügivõimalusest uude hinnapakkumisesse.

## <a name="from-the-opportunity-sales-process-flow"></a>Müügivõimaluse müügiprotsessi voost

Müügivõimalusest müügiprotsessi voost hinnapakkumise loomiseks tehke järgmist.

1. Avage müügivõimaluse müügiprotsessi voos müügivõimalus.
2. Valige etapp **Kinnita sobivaks**. 
3. Valige **Järgmine** ja valige seejärel **+ Loo**, et luua uus hinnapakkumine. Enamus selle uue hinnapakkumise vahekaardil **Kokkuvõte** olevast teabest pärineb vaikimisi müügivõimalusest. 
4. Sisestage kogu nõutud teave, mis puudub, või värskendage vastavalt vajadusele vahekaardil **Kokkuvõte** vaikimisi väärtused.
5. Valige **Salvesta**. Uus hinnapakkumine luuakse ja seostatakse müügivõimalusega. Nüüd saate vaadata hinnapakkumise teavet lehe **Müügivõimalus** vahekaardil **Hinnapakkumised**. 

   Müügivõimaluse müügiprotsess liigub järgmisse etappi, **Soovitus**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>Olemasoleva hinnapakkumise müügivõimaluse viidet värskendades

Olemasoleva hinnapakkumise saab siduda müügivõimalusega. Olemasoleva hinnapakkumise müügivõimaluse teabe värskendamiseks tehke järgmist.

1. Avage leht **Hinnapakkumine** ja valige vahekaart **Kokkuvõte**.
2. Väljal **Müügivõimalus** valige müügivõimalus, mille soovite hinnapakkumisega siduda. Hinnapakkumist saate vaadata müügivõimaluse ruudustikus **Hinnapakkumine**. 
3. Müügivõimaluse müügiprotsessi kasutamisel saab müügivõimaluse teisaldada järgmisse etappi, **Soovitus**. 

   Kui teisaldate müügivõimaluse sellesse etappi, saate selle hinnapakkumise valida selle müügivõimalusega seostatud hinnapakkumiste loendist. Selle hinnapakkumise valimine näitab, et liigute sellega edasi.

   Kõik teised müügivõimalusega seotud hinnapakkumised on endiselt saadaval ja aktiivsed, kuni üks neist on võidetud. Saate liigutada müügiprotsessi tagasi eelmisesse etappi (**Kinnita sobivakd**) ja valida mõne muu hinnapakkumise sellega edasi liikumiseks.
