---
title: Projekti hinnapakkumiste haldamine
description: Selles teemas antakse teavet projekti hinnapakkumiste kohta.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eab780241953bbabab199e146c94a15e272e35c9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579577"
---
# <a name="manage-project-quotes"></a>Projekti hinnapakkumiste haldamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Rakenduses Dynamics 365 Project Operations on projekti hinnapakkumised loodud aitamaks projektipõhise töö ettepanekute koostamisel. Project Operationsi projekti hinnapakkumise struktuur on loodud projekti hinnapakkumistele koos järgmiste komponentidega.

  - Hinnapakkumise read, mis määratlevad töö eraldi komponendid, mis esitatakse kõrgetasemeliste komponentidena.
  - Hinnapakkumise rea üksikasjad, mis määratlevad ja hindavad iga kõrgetasemelise komponendi või hinnapakkumise rea tööd. Töö ajakava või kuupäeva hinnangud ja finantsaspektid on seotud selle hinnapakkumise reaga.
  - Iga hinnapakkumise rea jaoks seadistatakse lepingulised mudelid ja tasustatavad komponendid. See seadistus aitab hinnata iga hinnapakkumise rea ja kogu hinnapakkumise tulu, kulutuste ja tasuvuse jaotumist.

## <a name="view-all-project-based-quotes"></a>Kõikide projektipõhiste hinnapakkumiste vaade

Kõigi projekti hinnapakkumiste loendit saab vaadata loendi **Hinnapakkumised** lehel. 

1. Minge jaotisse **Müük** > **Hinnapakkumised**. Kuvatakse loend kõikide teie projekti hinnapakkumistega. 
2. Kasutage hinnapakkumise teiste filtreeritud vaadete valimiseks suvandit **Vaatevahetaja**. Kohandatud filtri kriteeriumide abil saate konfigureerida oma vaateid ja navigeerimise suvandeid.

Hinnapakkumisi saab luua või kustutada sellelt loendi lehelt või üksikasjade lehtedelt.

 > [!NOTE]
 > Hinnapakkumisi, millega on seotud projektid, ülesanded, hinnangud, töölehed ja/või tegelikud andmed, ei saa kustutada. Samuti, kui hinnapakkumine on suletud kui Võidetud või Kadunud, ei saa seda enam kustutada ega muuta. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
