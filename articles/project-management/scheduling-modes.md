---
title: Plaanimisrežiimid
description: Selles teemas antakse teavet arvete plaanimisrežiimide kohta.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981430"
---
# <a name="scheduling-modes"></a>Plaanimisrežiimid

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


Dynamics 365 Project Operations annab organisatsioonidele võimaluse määratleda, kuidas nad haldavad tööjaotuse struktuuris tööülesannete põhimuutujate muudatusi. Lähtudes organisatsiooni konkreetsetest vajadustest, saavad projektijuhid projekti loomisel ajakava režiimis muudatusi teha.

Rakenduses Project Operations on saadaval kolm plaanimisrežiimi.

  - Fikseeritud kestus (see on vaikerežiim)
  - Fikseeritud töö
  - Fikseeritud ühikud

Kindla ajastamisrežiimi määratlusega seotud väärtused on määratletud järgmise valemiga.

  Pingutus (*töö*) = kestus × ühikud

Projekti plaanimisrežiimi määratlemisel määrate ühe nendest väärtustest, mida ei saa seejärel muuta. Selle väärtuse konstandina hoidmine seab sellele väärtusele prioriteedi, mis teavitab süsteemi seda mitte muutma, kui teised kaks väärtust muutuvad. Järgnev tabel annab teavet konkreetse režiimi valimise mõjude kohta.

| **Kinnita see ülesanne**             | **Kui muudate ühikuid**   | **Kui muudate kestust** | **Kui muudate pingutust**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Fikseeritud ühikutega ülesanne     | Kestus arvutatakse ümber. | Jõupingutus arvutatakse ümber.    | Kestus arvutatakse ümber. |
| Fikseeritud jõupingutusega ülesanne    | Kestus arvutatakse ümber. | Ühikud arvutatakse ümber.    | Kestus arvutatakse ümber. |
| Fikseeritud kestusega ülesanne  | Jõupingutus arvutatakse ümber.   | Jõupingutus arvutatakse ümber.    | Ühikud arvutatakse ümber.   |

Lisateavet antud režiimi konfliktide kohta leiate teemast [Täpsema ajastamise jaoks ülesandetüübi muutmine](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). Teemas kasutatakse terminit **Töö** termini **Jõupingutus** asemel.

## <a name="change-the-organizations-scheduling-mode"></a>Ettevõtte plaanimisrežiimi muutmine

Ettevõtte plaanimisrežiimi määratlemiseks tehke järgmist.

1. Minge jaotisesse **Sätted** \> **Üldine** \> **Parameetrid** ja valige seejärel projekti parameeter. 
2. Valige lehel **Projekti parameetrid** organisatsiooni jaoks ajastamise vaikerežiim ja seejärel määratlege võimalus, et projektijuht saab uue projekti loomisel selle sätte alistada.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Projekti plaanimisrežiimi sätte muutmine

Kui organisatsioon lubab projektijuhil ajastamise vaikerežiimi alistada, saab projektijuht selle muudatuse teha uue projekti loomisel. Pärast projekti salvestamist ei saa plaanimisrežiimi muuta.

## <a name="copied-projects"></a>Kopeeritud projektid

Kuna projekt luuakse projekti kopeerimistoimingu ajal, ei saa projektijuht plaanimisrežiimi seada. Sihtprojekt on alati vaikimisi organisatsioonitasandil määratletud režiimil.

## <a name="copied-tasks"></a>Kopeeritud tööülesanded

Kui tööülesanne kopeeritakse ühest projektist teise, pärib ülesanne sihtprojekti ajastamisrežiimi.
