---
title: Ressursi võimsuse sünkroonimine
description: Selles teemas antakse teavet ressursi võimsuse sünkroonimise kohta kalendrites ja projektides.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288554"
---
# <a name="synchronize-resource-capacity"></a>Ressursi võimsuse sünkroonimine

[!include [banner](../includes/banner.md)]

Ressursi sünkroonimise protsess aitab tagada, et teave kalendrist ja põhikalendrist liiguks alla projekti ressursi ajastamisse. Kui kalendrit muudetakse, teevad protsessid projekti ressursside ajastamisse nõutavaid värskendusi. Protsessid aitavad ka parandada jõudlust, kuna kalendri ressursi teave sünkroonitakse eelnevalt. Seetõttu toimuvad ressursside kavandamise teabe värskendused kiiremini. Soovitame ajastada protsessid partiidena, mitte üks korraga. Vastasel juhul on oht, et keegi unustab kaasavad kuupäevad, millal teavet viimati sünkrooniti. Kui kaasavaid kuupäevi ei kasutata, võib kuupäevade sünkroonimise ajal esineda vahesid.

![Kalendri sünkroonimine](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Ressursi võimsuse sünkroonimise ümberarvestused

Sünkroniseerimisprotsess on loodud sünkroonima kogu ressursi kalendri teabe. See teave hõlmab põhikalendri teavet mis tahes muudatuste kohta projekti ressursi kalendri võimsuse tabelis. Kui projekti lisatakse uusi ressursse, aitab sünkroonimine tagada, et saadaval oleks värskendatud kalendri teave. Seda sünkroonimist saab teha igal ajal.

Me soovitame kasutada partiid. Valikud on võimsuse reserveeringute sünkroonimise ajal saadaval.

1. Valige **Projektihaldus ja raamatupidamine** &gt; **Perioodiline** &gt; **Võimsuse sünkroonimine** &gt; **Ressursside võimsuse sünkroonimise ümberarvestused**.
2. Määrake järgmises tabelis valikud.

    | Suvand      | Kirjeldus |
    |-------------|-------------|
    | Perioodi kood | Võite ka valida pearaamatu kuupäevaintervalli koodi, et määrata sünkroniseerimisprotsessi algus- ja lõpukuupäevad ressursi võimsuse ümberarvestuste jaoks. |
    | Alguskuupäev  | Sisestage ressursi võimsuse ümberarvestuse sünkroniseerimisprotsessi alguskuupäev. |
    | Lõppkuupäev    | Sisestage ressursi võimsuse ümberarvestuse sünkroniseerimisprotsessi lõpukuupäev. |

[![Sünkroonimisprotsess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]