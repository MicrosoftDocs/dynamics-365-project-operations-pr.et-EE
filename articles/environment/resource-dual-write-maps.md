---
title: Rakenduse Project Operations topeltkirjutamise vastenduse versioonid
description: Selles artiklis on toodud loend kahekordse kirjutamisega kaartidest, mis on vajalikud Dynamics 365 Project Operations.
author: sigitac
ms.date: 07/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b86b9ecdc63989189c76dd8380024aa44c7641a5
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621076"
---
# <a name="project-operations-dual-write-map-versions"></a>Rakenduse Project Operations topeltkirjutamise vastenduse versioonid

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Rakenduse Dynamics 365 Project Operations kasutamine ressursi-/logimata stsenaariumide jaoks nõuab, et keskkonnas töötaks topeltkirjutusega kaartide komplekt. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Eeltingimuste kaardid: topeltkirjutatav juhtimislahendus

Järgmised kaardid on Project Operationsi lahenduse jaoks nõutavad eeltingimused. Käitage oma keskkonnas kindlasti järgmises tabelis loetletud kaarte ja mis tahes seostuvaid tabelikaarte.

| Tabelivastendus | Algne sünkroonimine |
| --- | --- |
| Pearaamat (msdyn_ledgers) | Nõuab tabelikaardi ja kõigi eeltingimuste algset sünkroonimist. Master esialgseks sünkroonimiseks on finance and operationsi rakendused. |
| Juriidilised isikud (cdm_companies) | Pole nõutav. Süsteem asustab selle olemi automaatselt, kui keskkonnad on seotud topeltkirjutusega. |
| Kliendid V3 (kontod) | Pole vajalik ettevalmistuse jaoks. |
| Tarnijad V2 (msdyn_vendors) | Pole vajalik ettevalmistuse jaoks. |

1. Valige kaartide loendist kõigi eeltingimustega kaart Pearaamat **(msdyn\_ledgers)** ja valige märkeruut **Algne sünkroonimine**. Tehke väljal **Master for initial sync** valik **Finance and operationsi rakendused** nii pearaamatukaardi kui ka kõigi eeltingimuste kaartide jaoks. Valige **Käivita**.

![Pearaamatu vastenduse sünkroonimine.](media/DW6.png)

2. Ülaltoodud tabelis loetletud ülejäänud tabelikaartide puhul järgige samu suuniseid. Ärge märkige nende kaartide käivitamisel ruutu **Algne sünkroonimine**.

## <a name="project-operations-dual-write-maps"></a>Project Operationsi topeltkirjutuse kaardid

Järgmised kaardid on Project Operationsi lahenduse jaoks nõutavad eeltingimused. Topeltkirjendamise vastendamise versioonid on loetletud alates Project Operationsi 2021. a mai värskendusest, versioon 4.10.0.186.

| Olemikaart | Uusim versioon | Algne sünkroonimine | Nõutav Dynamics 365 Finance versioon |
| --- | --- | --- | --- |
| Projekti kande seoste integreerimise olem (msdyn\_transactionconnections) | 1.0.0.0 | Pole vajalik ettevalmistuse jaoks. ||
| Projekti lepingupäised (müügitellimused) | 1.0.0.1 | Pole vajalik ettevalmistuse jaoks. ||
| Projekti lepinguread (salesorderdetails) | 1.0.0.0 | Pole vajalik ettevalmistuse jaoks. ||
| Projekti rahastamisallikas (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Pole vajalik ettevalmistuse jaoks. ||
| Projekti integratsioonitabel materjaliprognooside jaoks (msdyn\_ estimate lines) | 1.0.0.0 | Pole vajalik ettevalmistuse jaoks. ||
| Projekti arve ettepanekud V2 (arved) | 1.0.0.3 | Pole vajalik ettevalmistuse jaoks. ||
| Project Operationsi integreerimise tegelikud näitajad (msdyn_actuals) | 1.0.0.15 | Pole vajalik ettevalmistuse jaoks. |10.0.29 või uuemad|
| Project Operationsi integratsiooni lepingurea vahekokkuvõtted (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | Pole vajalik ettevalmistuse jaoks. ||
| Project Operationsi integratsiooni olem kuluprognooside jaoks (msdyn_estimatelines) | 1.0.0.2 | Pole vajalik ettevalmistuse jaoks. ||
| Project Operationsi integreerimise olem tunniprognooside jaoks (msdyn_resourceassignments) | 1.0.0.5 | Pole vajalik ettevalmistuse jaoks. ||
| Project Operationsi integreerimise projekti kulukategooriate ekspordi olem (msdyn_expensecategories) | 1.0.0.1 | Pole vajalik ettevalmistuse jaoks. ||
| Project Operationsi integreerimise projekti kulude ekspordi olem (msdyn_expenses) | 1.0.0.3 | Pole vajalik ettevalmistuse jaoks. ||
| Project Operationsi integreerimise projekti tarnija arve ekspordist (msdyn_projectvendorinvoices) | 1.0.0.2 | Pole vajalik ettevalmistuse jaoks. |10.0.29 või uuemad|
| Project Operationsi integratsioon projekti tarnija arve rea ekspordist (msdyn_projectvendorinvoices) | 1.0.0.5 | Pole vajalik ettevalmistuse jaoks. | 10.0.29 või uuemad |
| Projekti ressursside rollid kõigile ettevõtetele (bookableresourcecategories) | 1.0.0.1 | Nõuab tabelikaardi jaoks algset sünkroonimist, et sünkroonida projektijuhi ja meeskonna liikme ressursirollid, mis on ettevalmistamise ajal Dynamics 365 Dataverse’i keskkonnas asustatud. Dataverse on algse sünkroonimise põhiallikas. ||
| Projektiülesanded (msdyn_projecttasks) | 1.0.0.4 | Pole vajalik ettevalmistuse jaoks. ||
| Projektitehingute kategooriad (msdyn_transactioncategories) | 1.0.0.0 | Pole vajalik ettevalmistuse jaoks. ||
| Projektid V2 (msdyn_projects) | 1.0.0.2 | Pole vajalik ettevalmistuse jaoks. ||

Loetletud kaartide käivitamiseks tehke järgmist.

1. Lubage projekti ressursirollid **kõigile ettevõtetele (bookableresourcecategories)** tabelikaardil, kuna see kaart nõuab algset sünkroonimist. Valige väljal **Algse sünkroonimise ülem** väärtus **Ühisandmeteenus**. 

 ![Ressursirolli tabelikaardi sünkroonimine.](media/6ResourceInitialSync.jpg)

 Enne järgmise etapi juurde liikumist oodake, kuni kaardi olek on **Töötab**.

2. Valige kõik ülejäänud nõutavad kaardid. Nende filtreerimiseks võite neid topeltkirjutuse kaardiloendis filtreerida, kasutades parempoolses ülanurgas märksõna **projekt**. Saate valida kõik kaardid ja seejärel käivitada. Lisateavet leiate teemast [Mitme tabelikaardi haldamine](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Lubage ja käivitage kindlasti ka seostuvad olemikaardid.

### <a name="project-operations-dual-write-map-versions"></a>Rakenduse Project Operations topeltkirjutamise vastenduse versioonid

Kasutage oma keskkonnas alati kaardi uusimat versiooni. Kui esineb mõni järgmistest tingimustest, ei pruugi teatud funktsioonid ja võimalused õigesti töötada.

- Kaart pole aktiveeritud.
- Kaardi viimane versioon pole aktiveeritud. 
- Seostuvad tabelikaardid pole aktiveeritud.

Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelikaardi versioonid** valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kasutusvalmis tabelikaarti, peate muudatused uuesti rakendama. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)
