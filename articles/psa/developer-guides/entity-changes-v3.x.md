---
title: Olemi, juhtelemendi ja kasutajaliidese muudatused (Project Service Automation 3.x)
description: Selles artiklis kirjeldatakse project service automation 3.x lahenduse muudatusi Microsoft Dynamics.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8f54d263666c4fb999464f98c0138fc008dbbbd2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926863"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Olemi, juhtelemendi ja kasutajaliidese muudatused (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Rakenduse Microsoft Dynamics Project Service Automation (PSA) 3.x väljaandes on tehtud palju muudatusi olemitele, juhtelementidele, vaadetele ja kasutajaliidesele. See artikkel annab teavet nende oluliste muudatuste kohta.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Põhi- ja tütarüksuste seosed müügidokumendi, müügidokumendi rea, müügidokumendi rea üksikasjade olemite jaoks
Enne versiooni 3.0 välja antud rakenduse Dynamics 365 Project Service Automation (PSA) versioonides rakendati osa müügidokumentide, müügidokumentide ridade ja müügidokumentide rea üksikasjade olemite vahelistest seostest stringiväljade kaudu, mis sisaldaks seotud üksuse GUID stringi esitust. Selle põhjuseks olid platvormi piirangud, mis nõudsid lahenduse serveri ja kliendi pooltel märkimisväärset kohandatud koodi, et muuta need suhted sarnasteks tüüpiliste rakenduse Dynamics CRM olemisuhetega ja panna stringi väljad toimima nagu otsinguväljad.

PSA 3.0 on värskendatud, et võimendada müügi- ja müügidokumendi rea olemite vahel uusi olemi seoseid.

Kuna otsinguvälja saab nüüd kasutada olemitele viitavate viidete näitamiseks, ei pea neid välju, mis hoidsid seostatud olemi eelmises versioonis olevat stringi väärtust, enam vaja ning seega on need aegunud. Kohandatud kliendi- ja serveripoolne kood, mis käsitleb pärand stringiväljade määratletud seoseid, on ka aegunud.

### <a name="entity-schema-changes"></a>Olemi skeemi muudatused
Järgmises tabelis on üks-ühele loend aegunud stringi väljadest ja olemite uutest otsinguväljadest. 

 Olem |   Aegunud väli (string) | Uus väli (otsinguväli)
--- | --- | ---
invoicedetail (arve rida) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (tegelik) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (projekti lepingu rea arve ajakava) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (projekti lepingu rea vahekokkuvõte) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (fakt) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (arve rea üksikasjad) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (töölehe rida) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (projekti lepingu rea ressursikategooria) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (projekti lepingu rea üksikasjad) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (projekti lepingu rea tehingukategooria) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (projekti lepingu rea tehingu klassifikatsioon) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (hinnapakkumise rea arve ajakava) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (hinnapakkumise rea ressursikategooria) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (hinnapakkumise rea vahekokkuvõte) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (hinnapakkumise rea üksikasjad) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (hinnapakkumise rea tehingukategooria) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (hinnapakkumise rea tehingu klassifikatsioon) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (tellimuse rida) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Aegunud kohandatud vaated ja juhtelemendid
Järgmised kohandatud vaated ja juhtelemendid ning nendega seotud artefaktid on aegunud.

- Tasuline vaade.
- Kohandatud ruudustiku juhtnupud hinnapakkumise rea üksikasjade kuvamiseks pakkumise rea lehel **Projekti teave**.
- Kohandatud ruudustiku juhtnupud projekti lepingu rea üksikasjade kuvamiseks müügi tellimuse rea lehel **Projekti teave**.

> [!NOTE]
> Aegunud ressursside täieliku loendi leiate teemast [Aegunud veebiressursid rakenduses Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Unified Client Interface’i rakenduse moodul
Unified Client Interface’i (UCI) rakenduste moodulite kasutuselevõtu korral on PSA saidi vastendamise kirjed süsteemist eemaldatud.  
Funktsioonid, mis on seotud vormi vahetamisega müügivõimaluse, hinnapakkumise, tellimuse, arve jaoks, on aegunud, kuna see pole enam nõutav, sest UCI rakenduse moodul sisaldab ainult vormide PSA versioone.  

Järgmised veebiressursid on aegunud.

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Aegunud ressursside täieliku loendi leiate teemast [Aegunud veebiressursid rakenduses Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
