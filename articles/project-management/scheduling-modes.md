---
title: Plaanimisrežiimid
description: Selles teemas antakse teavet arvete plaanimisrežiimide kohta.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116702"
---
# <a name="scheduling-modes"></a>Plaanimisrežiimid

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


Dynamics 365 Project Operations annab organisatsioonidele võimaluse määratleda, kuidas nad haldavad tööjaotuse struktuuris tööülesannete põhimuutujate muudatusi. Lähtudes organisatsiooni konkreetsetest vajadustest, saavad projektijuhid projekti loomisel ajakava režiimis muudatusi teha.

Rakenduses Project Operations on saadaval kolm plaanimisrežiimi.

  - Fikseeritud kestus (see on vaikerežiim)
  - Fikseeritud panus (*töö*)
  - Fikseeritud ühikud

Kindla ajastamisrežiimi määratlusega seotud väärtused on määratletud järgmise valemiga.

  Panus = kestus × ühikud

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
