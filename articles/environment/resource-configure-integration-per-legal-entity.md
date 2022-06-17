---
title: Project Operationsi integratsiooni konfigureerimine vastavalt juriidilise isikule
description: Selles artiklis antakse teavet juriidilise isiku integratsiooni häälestamise kohta Project Operationsis.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914673"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Project Operationsi integratsiooni konfigureerimine vastavalt juriidilise isikule 

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel juhendab teid toimingutes, mis on vajalikud juriidilise isiku konfigureerimiseks Dynamics 365 Project Operations.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Funktsiooniklahvide lubamine Dynamics 365 Finance

Nõutavate funktsioonide lubamiseks toimige järgmiselt.

1. Avage Dynamics 365 Finance **funktsioonihalduse** tööruum.
2. Leidke ja lubage jaotises **Funktsioonide loend** järgmised funktsioonid.
  
    - **Mitme lepingurea lubamine projekti jaoks**
    - **Projektitoimingute lubamine Dynamics 365 Customer Engagement**

> [!NOTE]
> Kui te ei näe loendis valikut **Funktsiooni võtmed** veenduge, et teie Finance'i versioon vastab minimaalsetele versiooni nõuetele (rakenduse versioon 10.0.13 koos kõigi rakendatud kvaliteedivärskendustega, või uuem). Valige funktsioonide loendi värskendamiseks suvand **Otsi värskendusi**.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Juriidilisele isikule Project Operationsi juurutamise stsenaariumi määratlemine

Saate lubada projektitoimingud Dynamics 365 Customer Engagement juriidilise isiku tasandil. Teil võib olla üks juriidiline isik, kes kasutab project Operationsi Dynamics 365 Customer Engagement ressursi-/ladustamata põhistsenaariumide puhul. Samas keskkonnas võib teil olla veel üks juriidiline isik, kes kasutab Project Operationsi ressursi/tootmise tellimuste stsenaariumite jaoks.

1. Avage Dynamics 365 Finance **projektijuhtimise ja raamatupidamise** > **seadistus** > **Globaalne projektijuhtimise ja raamatupidamise parameetrid**.
2. Valige saadaolevate juriidiliste isikute loendis olemid, kus lubatakse mitu lepingurida ja project Operations Dynamics 365 Customer Engagement funktsioonides. Jätke valimata juriidilised olemid, mis kasutavad Project Operationsi ressursi/tootmise tellimuste stsenaariumite jaoks.

> [!NOTE]
> Juriidilise isiku saab valida ainult juhul, kui tal pole olemasolevaid projekte.

## <a name="configure-project-management-and-accounting-parameters"></a>Projektijuhtimise ja raamatupidamise parameetride konfigureerimine

Iga juriidiline isik, kes kasutab project Operationsi Dynamics 365 Customer Engagement, vajab vaikeparameetrite kogumit. Need parameetrid on konfigureeritud vahekaardil **Project Operations** lehel **Projektijuhtimise ja raamatupidamise parameetrid**. Parameetrid on järgmised.

  - **Arveldustüübi vaikesätted**: Project Operations kasutab fikseeritud arveldustüübi vaikeväärtuste kogumit, mis tuleb vastendada Finance'is rea atribuutidega. Looge kirje iga arveldustüübi kohta: **Määramata**, **Tasustatav**, **Mittearveldatav**, **Tasuta** ja **Pole saadaval**.
  - **Projekti kategooria vaikesätted**: valige iga kandetüübi jaoks kasutatavad projekti vaikekategooriad. Neid vaikeväärtusi kasutatakse **Project Operationsi integreerimise töölehel** ja nendes prognoosides, kus projekti tegelikuks näitajaks ei ole tehingu kategooriat määratud.
  - **Prognoosid**: valige prognoosi mudel, mida kasutatakse aja- ja kuluprognoosideks.


[!INCLUDE[footer-include](../includes/footer-banner.md)]