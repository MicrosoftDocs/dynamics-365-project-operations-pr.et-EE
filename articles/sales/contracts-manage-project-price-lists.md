---
title: Projektilepingute projekti hinnakirja haldamine
description: See teema sisaldab teavet projektilepingutes projekti hinnakirjade haldamise kohta.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 030684576e1f53d27921907b07c9e5e0c5efe612
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133320"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Projektilepingute projekti hinnakirja haldamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Rakenduse Dynamics 365 Project Operations projektilepingud on loodud lepingus mitmel päeval kehtivate müügi hinnakirjade toetamiseks. Project Operationis on uus seostatud olem nimega **Projekti hinnakirjad**. Sellel olemil on üks-mitmele-vastavuse seos projektilepinguga.

Projekti hinnakirju kasutatakse projekti aja ja kulutehingute hinnastamiseks. Kui lepingul on üks või mitu projekti hinnakirja, kasutatakse neid hinnakirju aja ja kulude kalkulatsioonide ning tegelike näitajate hinna jaoks projektide puhu, mis on seostatud lepinguga lepingurea kaudu.

Kui projektilepingus ei ole projekti hinnakirju, näete hoiatussõnumit, et projekti hinnakirju pole ja teie prognoosidele, tegelikule projekti tööle ega kuludele ei lisata hinda. Müügiväärtustele ei lisata hinda.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Projekti hinnakirja projektilepinguga seostamine või seose tühistamine

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a>Projektipõhise töö ja kulude prognoosimiseks konkreetse hinnakirja loomine või seostamine

1. Valige projektilepingus vahekaart **Projekti hinnakirjad**.
2. Valige andmeruudustikus suvand **+ Lisa uus projekti hinnakiri**.
3. Valige **kiirloomise** liuguril hinnakiri. 

  Ripploend kuvab kõik hinnakirjad, mille kontekstiks on määratud **Müük**, kus hinnakirja valuuta ühtib lepingu valuutaga.
  
4. Sisestage projekti hinnakirja seose kirjeldus, valige **Salvesta** ja seejärel sulgege **kiirloomise** liugur.

   Luuakse projekti hinnakirja seos.
   
5. Korrake samme 1–4, et seostada projektilepinguga rohkem kui üks projekti hinnakiri. Looge mitu projekti hinnakirja ainult siis, kui teie iga seostatud projekti hinnakiri jõustub erineval kuupäeval.

> [!NOTE]
> Project Operations ei toeta projekti hinnakirjade kattuvaid jõustumiskuupäevi. Kui tehingul on samaks kuupäevaks mitu projekti hinnakirja, määratakse selle tehingu hind vaikimisi nullile.

### <a name="remove-a-project-price-list-association"></a>Projekti hinnakirja seostamise eemaldamine

- Valige projekti hinnakiri ja valige seejärel andmeruudustikul suvand **Kustuta lepingu projekti hinnakiri**. 

  Hinnakiri eemaldatakse lepingu projekti hinnakirjade seast. Hinnakirja ennast ei kustutata. Kustutatakse ainult lepingu seostamine.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Lepingu projekti hinnakirjade automaatsete vaikeväärtuste määramise häälestamine

Projekti hinnakirja saab häälestada projektilepingu vaikeloendina. See seadistus aitab tagada, et teie organisatsiooni kõik lepingud algavad konkreetsel hinnaperioodil standardse hinnakirjaga.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Projekti hinnakirjade organisatsiooni vaikeväärtuste häälestamine

1. Avage **Sätted** > **Üldine** ja valige seejärel suvand **Parameetrid**.
2. Loendi lehel **Aktiivsed parameetrid** valige ja topeltklõpsake kirjel selle avamiseks. Topeltklõpsamise ajal veenduge, et te ei klõpsaks välja väärtust, mis on hüperlink. 
3. Valige lehel **Aktiivsed parameetrid** vahekaart **Hinnakiri**. Andmevõrgustik kuvab vaikimisi hinnakirjade loendi. See on standardsete kulude ja müügihindade loend. Hinnakirja **Müük** seostamine kõikide valuutadega, milles müüte, tagab et müügi hinnakiri on vaikeväärtus kõikides lepingutes, mille koostate selles valluutas tehinguid tegevatele klientidele.

### <a name="set-up-a-customer-specific-project-price-list"></a>Kliendipõhise projekti hinnakirja häälestamine

Kui te olete leppinud oma klientidega kokku raamhinnakokkuleppe, saate luua ka kliendipõhised projekti hinnakirjad.

1. Minge jaotisse **Müük** > **Kliendid**.
2. Valige aktiivsete kontode loendist klient, kellel on eraldi hinnakiri.
3. Valige avamiseks kliendi kirje ja valige seejärel vahekaart **Projekti hinnakirjad**. Andmeruudustik kuvab sellele kliendile spetsiifiliste projekti hinnakirjade loendi. 
4. Looge siin uus hinnakirja seos, et omada sellele kliendile spetsiifilist projekti hinnakirja.

## <a name="custom-pricing-on-a-project-contract"></a>Projektilepingu kohandatud hinnakiri

Pärast seda, kui teil on organisatsioonile ja kliendile spetsiifilised vaikimisi projekti hinnakirjad, teie projektilepingud luuakse nende projekti hinnakirja seostega automaatselt. Samas projekti hinnakirja lepingu projekti hinnakirjad kopeeritakse alati kuupäeva ja lepingu nimega, mis on nendele lisatud. Kontohaldurid ja projektijuhid saavad seejärel hakata nende koopiate hindasid muutma. Need muudetud hinnad rakenduvad ainult sellele projektilepingule.
