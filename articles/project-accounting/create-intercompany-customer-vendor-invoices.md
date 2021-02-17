---
title: Kontsernisisese kliendi ja hankija arvete loomine
description: Selles teemas antakse teavet kontsernisiseste kliendi ja hankija arvete koostamise kohta.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f1560469d2bdbb8e81dc26c16b272c44446ab20a
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595456"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Kontsernisisese kliendi ja hankija arvete loomine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Laenuandja juriidilise isiku projekti raamatupidaja loob kontsernisisese kliendi arve projekti kulud, mis kantakse üle laenuvõtvale olemile. Pärast seda, kui kontsernisisese kliendi arve kinnitatakse ja sisestatakse, saadab laenav juriidiline isik kontsernisisese arve laena võtvale juriidilisele isikule.

Laenu andva juriidilise isiku projekti raamatupidaja saab seadistada pakktöötluse, et luua kontsernisiseseid arveid korduval alusel. Projekti raamatupidaja määratleb kontsernisisesed arved pakktöötluse kriteeriumide (nt konkreetsete projektide) jaoks.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Kontsernisisese kliendi arve käsitsi loomine projekti kannete jaoks 

Kasutage seda toimingut, et luua käsitsi kontsernisiseseid kliendi arveid projekti kannete jaoks. Saate otsida tunde, mille töötajad on sisestanud laenu võtvate juriidiliste isikute projektidele ja kuludele, mille on tekitanud laenu võtvad juriidilised isikud teie nimel. Saate otsida juriidilise isiku nime, projekti lepingu numbrit, projekti numbrit, kuupäevavahemiku või nende suvandite mis tahes kombinatsiooni. Valige otsingutulemustes kontsernisisesele arvele lisatavad kanded.

1. Minge rakenduses Dynamics 365 Finance jaotisse **Projekti haldus ja raamatupidamine** > **Projekti arved** > **Kontsernisisesed kliendi arved**. Valige tegevuspaani loendis **Kontsernisisese kliendi arved** suvand **Uus**.
2. Valige lehe **IC-arve loomine** väljal **Juriidiline isik** laenu võttev juriidiline isik.
3. Valikuline: sisestage konkreetne projekti leping ja projekti number.
4. Piiritlege otsingut kuupäevavahemiku valimisega. Sisestage kindlaid kuupäevi väljadele **Alguskuupäev** ja **Lõppkuupäev**. Otsingutulemites kuvatakse ainult selle kuupäevavahemiku jooksul konteeritud kontsernisisesed kanded.
5. Seadke **Projekti töölehe täiendav parameeter** väärtusele **Jah** ja valige **Otsi**.
6. Valige otsingutulemites kontsernisises arve soovitusse kaasatavad kanded ja seejärel klõpsake nuppu **OK**.
7. Lehel **Kontsernisisese kliendi arve** kuvatakse otsingutulemustes valitud kontsernisiseste projektikanded. Kui soovite enne arve saatmist laenu võtvale juriidilisele isikule tehinguid muuta, toimige järgmiselt.
  
    1. Avage leht **Arve soovituse loomine**. Valige praeguse arve jaoks veel kontsernisiseseid tehinguid ja valige seejärel **Lisa rida**.
    2. Rea eemaldamiseks valige see ja klõpsake siis nuppu **Eemalda**.
    3. Kommentaare, põhjusi, finantsdimensioone ja muud teavet valitud rea kohta saate vaadata kiirkaardil **Arve read**.
    
8. Kontsernisisese kliendi arve konteerimiseks valige tegevuspaanil **Postita**.

> [!NOTE]
> Kui teie organisatsioon nõuab, et kontsernisisesed arved vaadatakse üle enne nende konteerimist, võib süsteemiadministraator seadistada kontsernisiseste arvete töövoo. Kui töövoog pole kontsernisiseste arvete jaoks seadistatud, saate kontsernisisese arve konteerida.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Pakett-töö loomine kontsernisiseste arvete jaoks

Kõigi laenava juriidiliste isikute jaoks saate korraga luua mitu kontsernisisest arvet. Funktsiooni Otsing abil saate otsida näiteks kõiki laenatud töötajate sisestatud tehinguid, mis on seotud muude juriidiliste isikute hallatavate projektidega. Seejärel saate iga laenava juriidilise olemi jaoks luua otsingutulemustes kuvatud tehingute jaoks kontsernisisese arve.

1. Minge jaotisse **Projekti haldus ja raamatupidamine** > **Perioodiline** > **Projekti arved** > **Kontsernisiseste kliendiarvete loomine**.
2. Lehel **Kontsernisiseste kliendiarvete loomine** väljal **Ettevõte** valige arve juriidiline isik. Kui te ei vali ettevõtet, kuvatakse kõigi laenavate juriidiliste isikute kohta kõik otsingukriteeriumile vastavad tehingud.
3. Valige jaotises **Loo üks arve**, kas soovite luua ühe arve iga projekti põhjal või laenava juriidilise olemi põhjal.
4. Valikuline: kindla projekti ja projekti lepingu valimiseks, et luua kontsernisisesed arved, klõpsake nuppu **Vali**. Valige lehe **Päring** väljal **Kriteerium** projekti leping, projekti number või mõlemad ja seejärel klõpsake nuppu **OK**.
5. Seadistage vahekaardil **Pakktöötlus** pakktöötlus, et luua kontsernisiseseid arveid korduval alusel. Lisateavet leiate teemast [Pakktöötluse töö esitamine vormilt](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Kontsernisiseste arvete konteerimiseks valige tegevuspaanil käsk **Postita**.

> [!NOTE]
> Kui teie organisatsioon nõuab, et kontsernisisesed arved vaadatakse üle enne nende konteerimist, võib süsteemiadministraator seadistada kontsernisiseste arvete töövoo. Kui töövoog pole kontsernisiseste arvete jaoks seadistatud, saate kontsernisisesed arved konteerida.

## <a name="post-the-intercompany-vendor-invoice"></a>Kontsernisisese hankija arve sisestamine

Laenava juriidilise isiku projekti raamatupidaja saab üle vaadata kontsernisisesed ootel hankija arved, kui vastav kontsernisisese kliendi arve on sisestatud. Avage jaotises Rahandus laenamise juriidiline isik: **Ostureskontro** > **Arved** > **Hankija ootel arved**. Ooteloleva arve number vastab kontsernisisese kliendi arve numbrile. Veenduge, et arve oleks õige, ja seejärel konteerige arve. Kontsernisisese hankija arve konteerimisel luuakse projekti alammoodul ja pearaamatu kanne, mis kajastab laenusaaja juriidilise isiku tehingukulusid.