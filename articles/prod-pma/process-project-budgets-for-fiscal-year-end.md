---
title: Projekti eelarvete ülekandmine finantsaasta lõpus
description: Selles artiklis kirjeldatakse kuidas viia allesolevaid eelarve summasid tulevastesse aastatesse ja luua eelarve registri üksikasju.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: be3dc039b92e88cac6f6b3b7f72bc32ecf587539
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008036"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Projekti eelarvete ülekandmine finantsaasta lõpus

[!include [banner](../includes/banner.md)]

Mitmeaastase projektiga töötamisel võib finantsaasta lõpus olla allesolev eelarve. Saate allesolevad eelarve summad tulevasse aastasse üle viia ja luua eelarve registri üksikasjad pearaamatu seotud kontode summade jaoks. Enne allesolevate summade ülekandmist vaadake üle ja analüüsige allesolevaid eelarve summasid.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Allesolevate eelarve summade ülevaatamine ja analüüs

Projektide aasta lõpu eelarve summade üle vaatamiseks toimige järgmiselt, kuid ärge kandke summasid üle.

1. Minge jaotisse **Projektijuhtimine ja raamatupidamine** > **Perioodiline** > **Eelarved** > **Ülekantavad eelarved**. 
2. Kontrollige lehe **Projekti eelarve ülekandmise protsess** vahekaardil **Aasta lõpu võimalused**, et suvand **Kanna allesjäänud projekti eelarve summad edasi** pole lubatud.
3. Valige vahekaardi **Parameetrid** väljal **Projekti eelarve aasta** finantsaasta, mille allesolevat eelarve summat soovite vaadata. 
4. Valige väljal **Finantsaasta avamine** finantsaasta, mille allesolevat eelarve summat soovite vaadata. 
5. Valige väljal **Prognoosimudelist** väärtus **Allesolev eelarve**. 
6. Kui soovite kaasata projekte, mis vastavad teie valitud kriteeriumidele ja millel pole allesolevat eelarvet, valige suvand **Kuva ilma allesolevata**.  
7. Valige vahekaardil **Vali eelarved** käsku **Too kõik eelarved**, et laadida kõik eelarved, mis vastavad teie valitud kriteeriumidele, ja seejärel valige **Töötle**. 
8. Sellise andmebaasi päringu loomiseks, mis laadib teatud eelarvete kogumi paanile, valige käsk **Too valitud eelarved**.

Paani kindla rea kohta lisateabe saamiseks valige rida ja seejärel valige suvand **Kuva eelarve üksikasjad** või **Kuva kontod**.

## <a name="carry-forward-remaining-budget-amounts"></a>Allesolevate eelarve summade ülekandmine 

Allesolevate eelarve summade töötlemisel saate luua pearaamatusse ülekantavatele summadele kanded. Pearaamatu kannete loomiseks täitke juhised jaotises [Eelarve summade ülekandmine ja pearaamatu kannete loomine](#carry-forward). 

> [!NOTE]
> Ülekantud eelarvelised summad kantakse edasi prognoosimudelisse, mis on lehel **Prognoosimudelid** ülekandmise prognoosi mudeliks valitud.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Eelarve summade ülekandmine ja pearaamatu kannete loomine

1.  Valige **Projektijuhtimine ja raamatupidamine** > **Perioodiline** > **Eelarved** > **Ülekantavad eelarved**. 
2. Valige lehel **Projekti eelarve ülekandmise protsess** väärtus **Aastalõpp** ja lubage seejärel suvandid **Kanna üle allesolevad projekti eelarve summad** ja **Loo pearaamatusse eelarve registri kanded**. 
3. Valige vahekaardil **Parameetrid** väljade rühmas **Projekti parameetrid** järgnev.

   - **Projekti eelarve aasta**: valige selle finantsaasta algus, mille allesolevaid eelarve summasid soovite vaadata. 
   - **Kasum ja kahjum**: pearaamatusse kasumi- ja kahjumi kannete loomine. 
   -  **WIP**: pearaamatusse käimasoleva töö (WIP) kannete loomine.
   -  **Palgaarvestuse**: pearaamatusse palgaarvestuse jaotuse kannete loomine. 

5. Esitage väljade rühma **Pearaamat** järgmine teave. 

   - Valige väljal **Finantsaasta avamine** finantsaasta, millele soovite projektide allesolevad eelarve summad kanda. Vaikeväärtus on üks aasta pärast välja **Projekti eelarve aasta**.
   -  Valige väljal **Ülekandmise periood** periood, millele soovite pearaamatus eelarve registri üksikasjad luua. See on tavaliselt finantsaasta esimene periood.

6. Esitage väljade rühma **Kopeeri kust/kuhu** järgmine teave.

   - Valige väljal **Prognoosimudelist** projekti prognoosimudel, mis on seotud allesolevate eelarve summadega, mida soovite projektidele üle kanda. 
   - Valige väljal **Pearaamatu eelarve mudelisse** pearaamatu eelarvemudel, mis on seotud eelarve summadega, mida soovite pearaamatusse üle kanda. 
   -  Valige **Kanna üle müügi valuuta**, et kasutada projekti müügi valuutat pearaamatu kannete jaoks, mis on loodud eelarve summade edastamisel projektidele. Kui suvand pole valitud, kasutavad kanded arvestusvaluutat. 
   -  Valige **Kuva ilma allesolevata**, et kaasata projektid, milles ei ole allesolevaid eelarve summasid, aga mis vastavad teistele kriteeriumidele, mille olete valinud alumisel paanil kuvatud projektides.

7. Valige vahekaardil **Vali eelarved** käsk **Too kõik eelarved**, et laadid kõik eelarved, mis vastavad teie valitud kriteeriumidele. Kui eelistate luua sellise andmebaasi päringu, mis laadib teatud projekti eelarvete kogumi paanile, valige käsk **Too valitud eelarved**.
8. Valige iga projekti jaoks, mida soovite töödelda, projekti rea alguses soovitud suvand.

    > [!TIP]
    > Kõigi või enamiku projektide valimiseks märkige ülemises vasakus nurgas olev märkeruut. Mistahes projekti töötlemise välistamiseks tühjendage selle projekti ruut.

9. Valitud projektide allesolevate eelarve summade ülekandmiseks valitud finantsaastasse ja pearaamatusse eelarve registri üksikasjade loomiseks valige **Töötle**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Eelarve summade ülekandmine pearaamatu kandeid loomata

1. Minge jaotisse **Projektijuhtimine ja raamatupidamine** > **Perioodiline** > **Eelarved** > **Ülekantavad eelarved**.
2. Valige lehe **Projekti eelarve ülekandmise protsess** väljal **Aasta lõpu võimalused**, et suvand **Kanna allesjäänud projekti eelarve summad edasi**.
3. Valige rühma **Parameetrid** väljal **Projekti eelarve aasta** finantsaasta, mille allesolevaid eelarve summasid soovite vaadata.
4. Esitage rühma **Kopeeri kust/kuhu** järgmine teave.

   - Valige väljal **Prognoosimudelist** projekti prognoosimudel, mis on seotud allesolevate eelarve summadega, mida soovite projektidele üle kanda. 
   - Valige **Kuva ilma allesolevata**, et kaasata projektid, millel ei ole allesolevaid eelarve summasid, aga mis vastavad teistele valitud kriteeriumidele.
   - Valige rühmas **Vali eelarved** käsk **Too kõik eelarved**, et laadid kõik eelarved, mis vastavad teie valitud kriteeriumidele. Sellise andmebaasi päringu loomiseks, mis laadib teatud projekti eelarvete kogumi paanile, valige käsk **Too valitud eelarved**.

5. Valige iga projekti jaoks, mida soovite töödelda, projekti rea alguses soovitud suvand. 
6. Valige **Töötle**, et kanda valitud projektide allesolevad eelarve summad üle valitud finantsaastasse.



[!INCLUDE[footer-include](../includes/footer-banner.md)]