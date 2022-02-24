---
title: Rakenduse Project Operations topeltkirjutamise vastenduse versioonid
description: Selles teemas loetletakse rakenduse Dynamics 365 Project Operations jaoks vajalikud topeltkirjutamise kaardid.
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938971"
---
# <a name="project-operations-dual-write-map-versions"></a>Rakenduse Project Operations topeltkirjutamise vastenduse versioonid

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Rakenduse Dynamics 365 Project Operations kasutamine ressursi-/logimata stsenaariumide jaoks nõuab, et keskkonnas töötaks topeltkirjutusega kaartide komplekt. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Eeltingimuste kaardid: topeltkirjutatav juhtimislahendus

Järgmised kaardid on Project Operationsi lahenduse jaoks nõutavad eeltingimused. Käitage oma keskkonnas kindlasti järgmises tabelis loetletud kaarte ja mis tahes seostuvaid tabelikaarte.

| Tabelivastendus | Algne sünkroonimine |
| --- | --- |
| Pearaamat (msdyn_ledgers) | Nõuab tabelikaardi ja kõigi eeltingimuste algset sünkroonimist. Algse sünkroonimise ülem on rakendus Finance and Operations. |
| Juriidilised isikud (cdm_companies) | Pole nõutav. Süsteem asustab selle olemi automaatselt, kui keskkonnad on seotud topeltkirjutusega. |
| Kliendid V3 (kontod) | Pole vajalik ettevalmistuse jaoks. |
| Tarnijad V2 (msdyn_vendors) | Pole vajalik ettevalmistuse jaoks. |

1. Valige kaartide loendist kõigi eeltingimustega kaart Pearaamat **(msdyn\_ledgers)** ja valige märkeruut **Algne sünkroonimine**. Valige väljal **Algse sünkroonimise põhirakendused** rakendus **Finance and Operations** nii pearaamatu kui ka kõigi eeltingimuste kaartide jaoks. Valige **Käivita**.

![Pearaamatu vastenduse sünkroonimine](media/DW6.png)

1. Ülaltoodud tabelis loetletud ülejäänud tabelikaartide puhul järgige samu suuniseid. Ärge märkige nende kaartide käivitamisel ruutu **Algne sünkroonimine**.

## <a name="project-operations-dual-write-maps"></a>Project Operationsi topeltkirjutuse kaardid

Järgmised kaardid on Project Operationsi lahenduse jaoks nõutavad eeltingimused.

| **Olemikaart** | **Uusim versioon** | **Algne sünkroonimine** |
| --- | --- | --- |
| Projekti kande seoste integreerimise olem (msdyn\_transactionconnections) | 1.0.0.0 | Pole vajalik ettevalmistuse jaoks. |
| Projekti lepingupäised (müügitellimused) | 1.0.0.1 | Pole vajalik ettevalmistuse jaoks. |
| Projekti lepinguread (salesorderdetails) | 1.0.0.0 | Pole vajalik ettevalmistuse jaoks. |
| Projekti rahastamisallikas (msdyn_projectcontractsplitbillingrules) | 1.0.0.1 | Pole vajalik ettevalmistuse jaoks. |
| Project Operationsi integreerimistabel materjaliprognooside jaoks (msdyn\_estimatelines) | 1.0.0.0 | Pole vajalik ettevalmistuse jaoks. |
| Projekti arve ettepanekud V2 (arved) | 1.0.0.2 | Pole vajalik ettevalmistuse jaoks. |
| Project Operationsi integreerimise tegelikud näitajad (msdyn_actuals) | 1.0.0.14 | Pole vajalik ettevalmistuse jaoks. |
| Project Operationsi integreerimise lepingurea vahekokkuvõtted (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | Pole vajalik ettevalmistuse jaoks. |
| Project Operationsi integreerimise olem kuluprognooside jaoks (msdyn_estimateslines) | 1.0.0.2 | Pole vajalik ettevalmistuse jaoks. |
| Project Operationsi integreerimise olem tunniprognooside jaoks (msdyn_resourceassignments) | 1.0.0.5 | Pole vajalik ettevalmistuse jaoks. |
| Project Operationsi integreerimise projekti kulukategooriate ekspordi olem (msdyn_expensecategories) | 1.0.0.2 | Pole vajalik ettevalmistuse jaoks. |
| Project Operationsi integreerimise projekti kulude ekspordi olem (msdyn_expenses) | 1.0.0.2 | Pole vajalik ettevalmistuse jaoks. |
| Project Operationsi integreerimise projekti tarnija arve ekspordist (msdyn_projectvendorinvoices) | 1.0.0.0 | Pole vajalik ettevalmistuse jaoks. |
| Project Operationsi integratsioon projekti tarnija arve rea ekspordist (msdyn_projectvendorinvoices) | 1.0.0.0 | Pole vajalik ettevalmistuse jaoks. |
| Projekti ressursside rollid kõigile ettevõtetele (bookableresourcecategories) | 1.0.0.1 | Nõuab tabelikaardi jaoks algset sünkroonimist, et sünkroonida projektijuhi ja meeskonna liikme ressursirollid, mis on ettevalmistamise ajal Dynamics 365 Dataverse’i keskkonnas asustatud. Dataverse on algse sünkroonimise põhiallikas. |
| Projektiülesanded (msdyn_projecttasks) | 1.0.0.4 | Pole vajalik ettevalmistuse jaoks. |
| Projektitehingute kategooriad (msdyn_transactioncategories) | 1.0.0.0 | Pole vajalik ettevalmistuse jaoks. |
| Projektid V2 (msdyn_projects) | 1.0.0.1 | Pole vajalik ettevalmistuse jaoks. |

Loetletud kaartide käivitamiseks tehke järgmist.

1. Lubage projekti ressursirollid **kõigile ettevõtetele (bookableresourcecategories)** tabelikaardil, kuna see kaart nõuab algset sünkroonimist. Valige väljal **Algse sünkroonimise ülem** väärtus **Ühisandmeteenus**. 

 ![Ressursirolli tabelikaardi sünkroonimine](media/6ResourceInitialSync.jpg)

 Enne järgmise etapi juurde liikumist oodake, kuni kaardi olek on **Töötab**.

2. Valige kõik ülejäänud nõutavad kaardid. Nende filtreerimiseks võite neid topeltkirjutuse kaardiloendis filtreerida, kasutades parempoolses ülanurgas märksõna **projekt**. Saate valida kõik kaardid ja seejärel käivitada. Lisateavet leiate teemast [Mitme tabelikaardi haldamine](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Lubage ja käivitage kindlasti ka seostuvad olemikaardid.

### <a name="project-operations-dual-write-map-versions"></a>Rakenduse Project Operations topeltkirjutamise vastenduse versioonid

Kasutage oma keskkonnas alati kaardi uusimat versiooni. Kui esineb mõni järgmistest tingimustest, ei pruugi teatud funktsioonid ja võimalused õigesti töötada.

- Kaart pole aktiveeritud.
- Kaardi viimane versioon pole aktiveeritud. 
- Seostuvad tabelikaardid pole aktiveeritud.

Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelikaardi versioonid** valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kasutusvalmis tabelikaarti, peate muudatused uuesti rakendama. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)
