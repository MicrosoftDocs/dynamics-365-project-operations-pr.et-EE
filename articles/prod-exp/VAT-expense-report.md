---
title: Käibemaksu sissenõudmine
description: Selles teemas selgitatakse, kuidas saada kõlblike käibemaksutehingute tagastusi.
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76706fd8ced58063b05bc8ebe4b25c1dddbf0890e72e9c7194d17ff2937dc8ca
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986036"
---
# <a name="vat-recovery"></a>Käibemaksu sissenõudmine 

Kõlblikelt käibemaksutehingutelt tagastuste saamiseks peab ettevõtte või organisatsioon tuvastama, koguma, kontrollima ja esitama täpsed andmed. See protsess hõlmab mitut tööülesannet ja sõltuvalt teie ettevõtte suurusest võib see sisaldada mitut töötajat või rolli.

Käibemaksu sissenõudmiseks Kuluhalduse abil tuleb täita järgmised eeltingimused.

- Maksukoodid tuleb luua riikide/piirkondade jaoks, mis on eraldatud kulukategooriate jaoks.
- Iga käibemaksukoodi jaoks tuleb luua käibemaksugrupp.
- Iga käibemaksugrupi jaoks tuleb luua üksuse käibemaksu kood.

Pärast eeltingimuste täitmist peavad töötajad käibemaksutehingutelt tagasimaksete saamiseks teostama järgmised toimingud.

1. Sisestage kuluaruandele krediitkaarditehingute maksuteave, et tuvastada kõlblikud käibemaksutagastused.
2. Kindlustage, et kogu maksuteave on valmis ja seejärel sisestage kuluaruanne.
3. Selliste kulude töötlemine, mis on kõlblikud saama rahvusvahelist käibemaksutagastust.
4. Saatke käibemaksutagastuse andmed kolmanda osapoole tarnijale, et saaksite esitada rahvusvahelise tagasimakse nõude.
5. Siseriikliku käibemaksutagastuse kulude töötlemine.

Järgmistes jaotistes on toodud näited selle kohta, kuidas Contoso töötajad iga etapi läbivad.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Sisestage kuluaruandele krediitkaarditehingute maksuteave, et tuvastada kõlblikud käibemaksutagastused

Ameerika Ühendriikides asuv Contoso müügiesindaja Nancy, kes naasis hiljuti Ühendkuningriigist ärireisilt. Reisi ajal tekkisid talle einestamisel mõned isikliku krediitkaardi kulud. Nancy peab nüüd looma kuluaruande, et oma kulusid ühitada.

Kui Nancy sisestab kuluandesse andmed, valib ta **Ühendkuningriik** väljal **Riik/piirkond** lehel **Kuluaruande redigeerimine**. Seejärel filtreeritakse käibemaksugrupi loend nii, et sellel oleks kuvatud ainult Ühendkuningriigi suhtes kohaldatavad rühmad. Nancy valib käibemaksugrupi **Ühendkuningriik 001** ja seejärel valib käibemaksugrupist üksuse **Eined**. Siis lisab ta majutuse kohta uue tehingu. Kuna Ühendkuningriigi majutuse kohta on ainult üks käibemaksugrupp ja üksuse käibemaksugrupp, täidetakse need andmed Nancy kuluaruandel automaatselt.

Contoso poliitika kohaselt peab kõigil kuludel olema vastav kviitung. Seega, kui Nancy salvestab kuluaruande, saab ta teate, mis ütleb, et ta peab lisama kviitungi iga tema kuluaruandes loetletud tehingu kohta. Nancy kontrollib, et ta on lisanud oma kuluaruandele digitaalse pildi iga tehingu kviitungi kohta ja seejärel esitab aruande kinnitamiseks. Seejärel saadab ta paberkviitungid tugikeskuse töötlevale meeskonnale. See meeskond saadab kolmandast osapoolest tarnijale käibemaksu sissenõudmise andmed, mis esitab Contoso jaoks rahvusvahelise käibemaksu sissenõudmise.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Kindlustage, et kogu maksuteave on valmis ja seejärel sisestage kuluaruanne

Aprillis peab Contoso ostureskontro koordinaator sisestama mis tahes kuluaruandelt puuduva maksuteabe, enne kui aruande saab sisestada. Ta avab lehe **Kuluaruande üksikasjad** ja näeb Nancy kinnitatud kuluaruannet. April avab seejärel kuluaruande, et kuvada tehingute üksikasju. Ta näeb, et Nancy ei sisestanud ühe tehingu jaoks üksuse käibemaksugruppi. Kuna seda teavet ei ole antud, ei saa April kuluaruannet sisestada. Seetõttu vaatab April kuluhalduse lehte **Maksukonfiguratsioonid** ja leiab riigile/piirkonnale ja tehingu tüübile sobiva käibemaksugrupi. April saab nüüd kuluaruande pearaamatusse sisestada.

Kui April kuluaruande sisestab, luuakse käibemaksutagastuse tööüksus. See tööüksus määratakse tugikeskuse töötleva meeskonna liikmele. April saab sõnumi, mis kinnitab, et sisestus oli edukas. Selles teates tuuakse välja ka tagastamiseks tuvastatud käibemaksutehingute number.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Selliste kulude töötlemine, mis on kõlblikud saama rahvusvahelist käibemaksutagastust

Contoso arveldusosakonna töötlemismeeskonna liige Arne vastutab selle eest, et kinnitada kogu kuluaruannetes olev käibemaksu tagastusnõudmise kohta käiv teave. Ta avab lehe **Kulu maksutagastus** ja valib Nancy esitatud kuluaruande. Seejärel Arnie kontrollib, et kõik nõutavad kviitungid on lisatud ja et sisestatud on õige käibemaksugrupi ja üksuse käibemaksukoodid.

Kui Arnie saab Nancylt paberkviitungid, kontrollib ta paberkviitungeid digitaalsete kviitungite suhtes ja seejärel muudab kuluaruande olekuks **Tagasimakseks valmis**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Saatke käibemaksutagastuse andmed kolmanda osapoole tarnijale, et saaksite esitada rahvusvahelise tagasimakse nõude

Kui Arnie on valmis saatma kuluaruande andmed kolmanda osapoole tarnijale, kes esitab käibemaksutagastuse dekralaratsiooni, avab ta lehe **Kulu maksutagastus**. Ta filtreerib lehte nii, et see kuvaks ainult neid kuluaruandeid, mille olekuks on märgitud **Tagasimakseks valmis**. Seejärel valib Arnie **Fail** &gt; **Eksportimine Excelisse**. Kuluaruande käibemaksuandmed eksporditakse Microsoft Exceli töölehele. Arnie esitab selle töölehe kolmanda osapoole tarnijale ja paneb kaasa sõnumi, mis ütleb, et paberkviitungid on saadetud kulleriga.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Siseriikliku käibemaksutagastuse kulude töötlemine

Arnie peab kontrollima, et kuluaruande tehingud vastavad käibemaksutagastuse tingimustele, ja et digitaalsed kviitungid on aruannete juurde manustatud. Selleks et hakata sobilikke kulusid siseriiklikuks maksutagastuseks töötlema, avab Arnie lehe **Kulu maksutagastus** ja valib kontrollimist vajava kuluaruande. Ta kontrollib, et kviitungid on töötaja asemel ettevõtte nimel. Käibemaksutagastuseks peavad kviitungid olema ettevõtte nimel. Seejärel kontrollib Arnie, et rakendati õiget käibemaksurühma ja kauba käibemaksukoodi.

Kui Arnie saab paberkandjal kviitungeid, muudab ta kuluaruande olekuks **Tagasimakseks valmis**. Seejärel saab ta esitada tagasimakse deklaratsiooni vastava maksuhalduri juures. Sellel juhul on vastavaks maksuhalduriks USA Internal Revenue Service (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]