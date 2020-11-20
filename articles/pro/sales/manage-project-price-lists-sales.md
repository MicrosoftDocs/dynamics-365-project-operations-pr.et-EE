---
title: Projekti hinnapakkumiste projekti hinnakirja haldamine – liht
description: Selles teemas kirjeldatakse tööd hinnapakkumiste projekti hinnakirjadega. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ff830c63f7acf4cc23ac75d44afa9c3553b8724
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175976"
---
# <a name="manage-project-price-lists-on-project-quotes---lite"></a>Projekti hinnapakkumiste projekti hinnakirja haldamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Projekti hinnapakkumised on loodud toetama mitut kuupäevapõhist müügi hinnakirja. Dynamics 365 Project Operationsiga lisatakse uus seotud olem nimega **Projekti hinnakirjad**. Sellel olemil on üks-mitmele-seos projekti hinnapakkumisega.

Projekti hinnakirju kasutatakse projekti aja ja kulutehingute hinnastamiseks. Kui hinnapakkumisel on üks või mitu projekti hinnakirja, kasutatakse neid hinnakirju hinnapakkumise rea kaudu hinnapakkumisega seotud aja ja kuluprognooside ning tegelike näitajate hinnastamiseks.

Kui projekti hinnapakkumisel pole projekti hinnakirju, kuvatakse hoiatusteade. Teates on kirjas, et kuna projekti hinnakiri puudub, siis teie prognoositavat ja tegelikku projekti tööd ja kulusid ei hinnastata. Selle asemel on neil null (0) müügihind.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Projekti hinnakirja seostamine projekti hinnapakkumisega või selle lahti sidumine

Projektipõhiste tööde ja kulude prognoosimiseks kindla hinnakirja loomiseks või valimiseks läbige järgmised etapid.

1. Valige hinnapakkumise vahekaart **Projekti hind** ja seejärel valige alamruudustikul **+ Lisa uus projekti hinnakiri**.
2. Valige kiirloomise lehel hinnakiri. Ripploendis kuvatakse kõik hinnakirjad, mille kontekstiks on seadistatud **Müük** ja mille valuuta vastab hinnapakkumise valuutale.
4. Sisestage projekti hinnakirja seose kirjeldus ja valige **Salvesta ja Sule**.

Luuakse projekti hinnakirja seos.

Seda protsessi saate korrata juhul, kui peate projekti hinnapakkumisega seostama rohkem kui ühe projekti hinnakirja. Looge mitu projekti hinnakirja ainult juhul, kui teil on igale seotud projekti hinnakirjale erinev efektiivne kuupäev.

> [!NOTE]
> Project Operations ei toeta projekti hinnakirjade kattuva kuupäeva efektiivsust. Kui antud kuupäevaga tehingu jaoks on mitu projekti hinda, määratakse selle tehingu hind vaikimisi nulliks (0).
Projekti hinnakirja seose eemaldamiseks valige projekti hinnakiri ja seejärel valige **Kustuta hinnapakkumise projekti hinnakiri**. Hinnakiri eemaldatakse hinnapakkumise projekti hinnakirjade hulgast, kuid hinnakirja iseennast ei kustutata. Kustutatakse ainult seos hinnapakkumisega.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Hinnapakkumisele vaikimisi projekti hinnakirja seadistamine

Projekti hinnakirju saab seadistada projekti hinnapakkumisele vaikimisi. See seadistus tagab, et kõik teie organisatsiooni hinnapakkumised algavad alati selle hinnaperioodi standardsest hinnakirjast.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Projekti hinnakirjadele organisatsioonipõhise vaikeväärtuse seadistamine

1. Minge jaotisse **Sätted** > **Üldine** > **Parameetrid**.
2. Leidke kirje loendi **Aktiivsed parameetrid** lehelt ja tehke selle avamiseks topeltklõps. 
3. Valige lehel **Parameetrid** vahekaart **Hinnakiri**. Kuvatakse vaikehinnakirjade loend. See on loend standardkulude ja müügi hinnakirjadest. Iga kasutatava valuuta kohta siin müügi hinnakirja olemasolu kindlustab, et müügi hinnakirjale pannakse vaikeväärtus mistahes müügipakkumise jaoks, mille selles valuutas tehinguid tegevatele klientidele loote.

### <a name="set-up-customer-specific-project-price-lists"></a>Kliendispetsiifiliste projektide hinnakirjade seadistamine

Kliendispetsiifiliste projektide hinnakirju saab seadistada ka siis, kui olete klientidega kokku leppinud peamises hinnastamises.

Kliendispetsiifilise projekti hinnakirja seadistamiseks toimige järgmiselt.

1. Valige alal **Müük** suvand **Kliendid**.
2. Valige ja avage oma aktiivsete kontode loendis selle kliendi kirje, kelle jaoks on teil eraldi hinnakiri.
3. Vahekaardil **Projekti hinnakiri** saate luua uue hinnakirja seose, et projekti hinnakiri oleks erinev selle kliendi jaoks.

## <a name="create-custom-pricing-on-a-project-quote"></a>Projekti hinnapakkumisele kohandatud hinnastamise loomine

Kui teil on olemas organisatsioonide- ja kliendipõhised projekti vaikehinnakirjad, luuakse teie projekti hinnapakkumised auotmaatselt nende projekti hinnakirjade seostega. Teatud juhtudel võib siiski juhtuda, et peate kindla projekti hinnapakkumise jaoks looma kohandatud hinnastamise. 

1. Kontrollige **Projekti hinnapakkumise** vahekaardil **Projekti hinnakiri**, et alamruudustikus ei oleks valitud konkreetset hinnakirja kirjet.
2. Valige **Kohandatud hindade loomine**. See teeb koopiad kõigist praegu hinnapakkumisega seotud standardsetest hinnakirjadest ja seob need koopiad hinnapakkumisega. Olemasolevad seosed standardsete hinnakirjadega eemaldatakse. Seejärel saab müügiesindaja alustada nendes koopiates hindade muutmist. Neid muudetud hindu kohaldatakse ainult selle projekti hinnapakkumise suhtes.
