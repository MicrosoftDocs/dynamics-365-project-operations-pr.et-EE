---
title: Kontsernisisese arveldamise konfigureerimine
description: See artikkel annab teavet ja näiteid projektide kontsernisisese arvelduse konfigureerimise kohta.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ae0c2662bb6b2789ab520f08c7c21935b651ced5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929351"
---
# <a name="configure-intercompany-invoicing"></a>Kontsernisisese arveldamise konfigureerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Täitke järgmised etapid, et seadistada projektide jaoks kontsernisisene arveldamine lahenduses Dynamics 365 Project Operations. Kontsernisisesed tehingud on projekti lepingust pärinevad aja- ja kulutehingud, mis kuuluvad ühele ettevõtte- või organisatsiooniüksusele, samas kui projektilepingu ressursid on erineva ettevõtte- või organisatsiooniüksuse osad.

## <a name="example-configure-intercompany-invoicing"></a>Näide: kontsernisisese arveldamise konfigureerimine

Järgmises näites on Contoso Robotics USA (USPM) laenav juriidiline isik ja Contoso Robotics UK (GBPM) on laenuandja juriidiline isik. 

1. **Konfigureerige juriidiliste isikute vahel kontsernisisene raamatupidamine**. Kõik laenu andvate ja laenu võtvate juriidiliste isikute paarid peavad olema konfigureeritud pearaamatu [kontsernisisese raamatupidamisarvestuse](/dynamics365/finance/general-ledger/intercompany-accounting-setup) lehel.
    
    1. Teenuses Dynamics 365 Finance, minge jaotisesse **Pearaamat** > **Postitamise seadistamine** > **Kontsernisisene raamatupidamine**. Looge kirje, kasutades järgmist teavet.

        - **Algne ettevõte** = **GBPM**
        - **Sihtettevõte** = **USPM**

2. **Konfigureerige ärisuhted juriidiliste isikute vahel**. Laenu võtva juriidilise isiku kliendi kirje tuleb luua laenuandja juriidilise isiku jaotises. Laenu andva juriidilise isiku kliendi kirje tuleb luua laenusaaja juriidilise isiku jaotises.

     1. Valige väljal Rahandus ettevõte juriidiline isiku **GBPM**.
     2. Avage **Müügireskontro** > **Klient** > **Kõik kliendid**. Looge juriidilise isiku jaoks uus kirje: **USPM**.
     3. Laiendage jaotist **Nimi**, filtreerige kirjed **tüübi järgi** ja valige **Juriidilised isikud**. 
     4. Saate otsida ja valida **Contoso Robotics USA (USPM)** jaoks kliendikirjeid.
     5. Valige **Kasuta vastet**. 
     6. Valige kliendirühm **50 – ettevõttesisesed kliendid** ja seejärel salvestage kirje.
     7. Valige juriidiline isik **USPM**.
     8. Minge jaotisse **Ostureskontro** > **Hankijad** > **Kõik hankijad**. Looge juriidilise isiku jaoks uus kirje: **GBPM**.
     9. Laiendage jaotist **Nimi**, filtreerige kirjed **tüübi järgi** ja valige **Juriidilised isikud**. 
     10. Saate otsida ja valida **Contoso Robotics UK (GBPM)** jaoks kliendikirjeid.
     11. Valige suvand **Kasuta vastet**, valige hankijarühm ja salvestage seejärel kirje.
     12. Valige hankija kirjes **Üldine** > **Seadista** > **Kontsernisisene**.
     13. Vahekaardil **Kauplemise seos** seadke väärtus **Aktiivne** olekusse **Jah**.
     14. Määrake välja **Kliendi ettevõte** väärtuseks **GBPM** ja valige jaotises **Minu konto kirje** kliendikirje, mille olete varem protseduuri käigus loonud.

3. **Konfigureerige kontsernisisesed sätted projekti halduses ja raamatupidamise parameetrites**. 

    1. Valige juriidiline isik **USPM** ja minge jaotisse **Projektihaldus ja raamatupidamine** > **Seadistamine** > **Projektihalduse ja raamatupidamise parameetrid**.
    2. Vahekaardil **Kontsernisisene** valige hankekategooria, et see vastaks automaatselt loodud tarnija arvetele.
    3. Valige jaotises **Vaikimisi kategooria** **Kontsernisisesed ressursid**.
    4. Valige juriidiline isik **GBPM** ja minge jaotisse **Projektihaldus ja raamatupidamine** > **Seadistamine** > **Projektihaldus ja raamatupidamise parameetrid**.
    5. Valige vahekaardil **Kontsernisisene** iga kandetüübi jaoks vaikimisi kasutatav projekti kategooria. Projekti kategooriaid kasutatakse maksude konfigureerimiseks juhul, kui kontsernisiseste tehingute kategooria on olemas ainult laenu võtval juriidilisel isikul. Saate valida, kas koguda tulu kontsernisiseste kannete jaoks. Tekkepõhiselt kirjendatakse, kui tehingud sisestatakse laenamise juriidilisele isikule Project Operationsi integreerimise töölehe kaudu. Tööleht tühistatakse, kui sisestatakse kontsernisisene arve.
    6. Valige rühmas **Kui laenatakse ressursse** **...** > **Uus**. 
    7. Sisestage või valige ruudustikus järgmine teave.

          - **Laenu võttev juriidiline isik** = **USPM**
          - **Tekkepõhine tulu** = **Jah**
          - **Ajatabeli vaikekategooria** = **Vaikesäte – tund**
          - **Kulu vaikekategooria** = **Vaikeväärtus – kulu**

4. **Pearaamatu sisestamise seadistamisel saate määrata kontsernisisesed kulu ja tulu ettevõtted**. Kontsernisisese tulu kontot krediteeritakse, kui kontsernisisese kliendi arve sisestatakse laenamise juriidilisele isikule. Kontsernisisese tulu kontot debiteeritakse, kui vastav ootel olev hankijaarve sisestatakse laenu võtva juriidilise isiku jaoks. Need kontod on seadistatud vastavates juriidilistes isikutes. 
      
     1. Valige jaotises Rahandus laenu võttev juriidiline isik **USPM**. 
     2. Minge jaotisse **Projektihaldus ja raamatupidamine** > **Seadistamine** > **Postitamine** > **Pearaamatu sisestamise seadistamine**. 
     3. Valige vahekaardil **Kulukontod** jaotises **Pearaamatukonto tüüp** **Kontsernisisesed kulud**. Saate luua uue kirje järgmise kandega.
      
        - **Laenu andev juriidiline olem** = **GBPM**
        - **Põhikonto** = valige peamine konto ettevõtesisese kulu jaoks. Selle määramine on kohustuslik. Seadistust kasutatakse jaotises Rahandus ettevõttesiseste voogude jaoks, kuid mitte projektiga seotud ettevõttesisestes voogudes. See valik ei mõjuta järgmisi etappe. 
        
     4. Valige laenu andev juriidiline olem: **GBPM**. 
     5. Minge jaotisse **Projektihaldus ja raamatupidamine** > **Seadistamine** > **Postitamine** > **Pearaamatu sisestamise seadistamine**. 
     6. Valige vahekaardil **Tulukontod** jaotises **Pearaamatukonto tüüp** **Kontsernisisesed tulud**. Saate luua uue kirje järgmise kandega.

        - **Laenu võttev juriidiline olem** = **USPM**
        - **Põhikonto** = valige peamine konto kontsernisisese tulu jaoks. Selle määramine on kohustuslik. Seadistust kasutatakse jaotises Rahandus ettevõttesiseste voogude jaoks, kuid mitte projektiga seotud ettevõttesisestes voogudes. See valik ei mõjuta järgmisi etappe. 

5. **Seadistage tööjõu siirdehind**. Kontsernisisese kande hinnakujundus konfigureeritakse Dataverse’i lahenduses Project Operations. Konfigureerige [tööjõu kulumäärad](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) ja [tööjõu arve määrad](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) kontsernisisese arvelduse jaoks. Kontsernisiseste kuluaruannete puhul ei toetata ülekande hinda. Kontsernisisese ühiku müügihind seatakse alati samale väärtusele kui ümberhangete ühiku omahind.

      Ettevõttes Contoso Robotics UK on arendaja ressursi kulu 88 naela tunnis. Contoso Robotics UK esitab ettevõttele Contoso Robotics USA arve 120 USD iga tunni eest, kui see ressurss töötas USA projektides. Contoso Robotics USA esitab kliendile Adventure Works 200 USD suuruse arve Contoso Robotics UK arendajaressursside tehtud töö eest.

      1. Avage Dataverse’i lahenduses Project Operations jaotis **Müük** > **Hinnakirjad**. Looge uus omahinna loend nimega **Contoso Robotics UK kulumäärad**. 
      2. Looge omahinna loendis järgmise teabega kirje.
         - **Roll** = **Arendaja**
         - **Kulu** = **88 GBP**
      3. Minge jaotisse **sätted** > **Organisatsioonilised üksused** ja lisage see omahinna loend organisatsiooni üksusele **Contoso Robotics UK**.
      4. Minge jaotisse **Müük** > **Hinnakirjad**. Looge uus omahinna loend nimega **Contoso Robotics USA kulumäärad**. 
      5. Looge omahinna loendis järgmise teabega kirje.
          - **Roll** = **Arendaja**
          - **Ressursiettevõte** = **Contoso Robotics UK**
          - **Kulu** = **120 USD**
      6. Minge jaotisse **Sätted** > **Organisatsioonilised üksused** ja lisage see omahinna loend **Contoso Robotics USA kulumäärad** **Contoso Robotics USA** organisatsiooni üksusele.
      7. Minge jaotisse **Müük** > **Hinnakirjad**. Looge müügi hinnakiri nimega **Adventure Worksi arveldusmäärad**. 
      8. Looge müügi hinnakirjas järgmise teabega kirje.
          - **Roll** = **Arendaja**
          - **Ressursiettevõte** = **Contoso Robotics UK**
          - **Arveldusmäär** = **200 USD**
      9. Minge jaotisse **Müük** > **Projekti lepingud** ja lisage hinnakiri **Adventure Worksi arveldusmäärad** Adventure Worksi projekti lepingu hinnakirjale.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
