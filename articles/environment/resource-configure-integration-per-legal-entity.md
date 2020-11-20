---
title: Project Operationsi integratsiooni konfigureerimine vastavalt juriidilise isikule
description: Selles teemas kirjeldatakse Project Operationsis integratsiooni seadistamist vastavalt juriidilisele isikule.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122878"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Project Operationsi integratsiooni konfigureerimine vastavalt juriidilise isikule 

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See teema selgitab vajalikke etappe, mis on vajalikud Dynamics 365 Project Operationsi konfigureerimiseks vastavalt juriidilisele isikule.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Funktsiooni võtmete lubamine rakenduses Dynamics 365 Finance

Nõutavate funktsioonide lubamiseks toimige järgmiselt.

1. Avage rakenduses Dynamics 365 Finance tööruum **Funktsioonihaldus**.
2. Leidke ja lubage jaotises **Funktsioonide loend** järgmised funktsioonid.
  
    - **Mitme lepingurea lubamine projekti jaoks**
    - **Project Operationsi lubamine lahenduses Dynamics 365 Customer Engagement**

> [!NOTE]
> Kui te ei näe loendis valikut **Funktsiooni võtmed** veenduge, et teie Finance'i versioon vastab minimaalsetele versiooni nõuetele (rakenduse versioon 10.0.13 koos kõigi rakendatud kvaliteedivärskendustega, või uuem). Valige funktsioonide loendi värskendamiseks suvand **Otsi värskendusi**.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Juriidilisele isikule Project Operationsi juurutamise stsenaariumi määratlemine

Saate lahenduses Dynamics 365 Customer Engagement Project Operationsi lubada juriidilise isiku tasandil. Teil võib olla üks juriidiline isik, kes kasutab Project Operationsi lahenduses Dynamics 365 Customer Engagement ressursipõhiste/mitteaktsiapõhiste stsenaariumite jaoks. Samas keskkonnas võib teil olla veel üks juriidiline isik, kes kasutab Project Operationsi ressursi/tootmise tellimuste stsenaariumite jaoks.

1. Minge rakenduses Dynamics 365 Finance jaotisse **Projektijuhtimine ja raamatupidamine** > **Seadistamine** > **Globaalsed projektijuhtimise ja raamatupidamise parameetrid**.
2. Valige saadaolevate juriidiliste isikute loendis olemid, kus lubatakse mitu lepingurida ja Project Operationsi funktsioonid lahenduses Dynamics 365 Customer Engagement. Jätke valimata juriidilised olemid, mis kasutavad Project Operationsi ressursi/tootmise tellimuste stsenaariumite jaoks.

> [!NOTE]
> Juriidilise isiku saab valida ainult juhul, kui tal pole olemasolevaid projekte.

## <a name="configure-project-management-and-accounting-parameters"></a>Projektijuhtimise ja raamatupidamise parameetride konfigureerimine

Iga lahenduses Dynamics 365 Customer Engagement Project Operationsi kasutav juriidiline isik vajab vaikimisi määratud parameetrite kogumit. Need parameetrid on konfigureeritud vahekaardil **Project Operations** lehel **Projektijuhtimise ja raamatupidamise parameetrid**. Parameetrid on järgmised.

  - **Arveldustüübi vaikesätted**: Project Operations kasutab fikseeritud arveldustüübi vaikeväärtuste kogumit, mis tuleb vastendada Finance'is rea atribuutidega. Looge kirje iga arveldustüübi kohta: **Määramata**, **Tasustatav**, **Mittearveldatav**, **Tasuta** ja **Pole saadaval**.
  - **Projekti kategooria vaikesätted**: valige iga kandetüübi jaoks kasutatavad projekti vaikekategooriad. Neid vaikeväärtusi kasutatakse **Project Operationsi integreerimise töölehel** ja nendes prognoosides, kus projekti tegelikuks näitajaks ei ole tehingu kategooriat määratud.
  - **Prognoosid**: valige prognoosi mudel, mida kasutatakse aja- ja kuluprognoosideks.
