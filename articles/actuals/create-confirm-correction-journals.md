---
title: Paranduste töölehtede loomine ja kinnitamine
description: Selles teemas antakse teavet, kuidas luua ja kinnitada paranduse töölehte.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c15db854e3d130150ad7afc707a126b37c57f62d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582798"
---
# <a name="create-and-confirm-correction-journals"></a>Paranduste töölehtede loomine ja kinnitamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Mõnikord võib aja- või kulukanne sisestada valesti. Näiteks võib konsultant valida ajakirje loomisel vale kuupäeva või valida kulu sisestamisel vale projekti. Kui konsultant ei saa esitatud kandeid värskendada, saab tagavaraadministraator projekti tegelikud andmed otse parandada.

## <a name="correct-approved-time-entries"></a>Kinnitatud ajakirjete parandamine     

Projekti ühe või mitme ajakirje parandamiseks läbige järgmised sammud.

1. Valige alal **Müük** väärtus **Kanded** ja seejärel valige **Kinnitatud aeg**. 

2. Otsige ja valige loendist **Kinnitatud aeg** parandamiseks üks või rohkem kinnitatud ajakirjet. Filtri abil saate otsida seostuvaid kirjeid. Näiteks võite filtreerida projekti ID järgi ja valida kõik selle projekti ID-ga kinnitatud ajakirjed.

3. Valige **Kirjete parandamine**. Luuakse automaatselt uus paranduse tööleht, millele on määratud tüüp **Aja parandus**. Teie valitud kirjed lisatakse töölehele. 

4. Sisestage lehel **Uus tööleht** oma paranduste töölehele **Kirjeldus** ja seejärel valige vahekaart **Ajakirje parandused**.  

5. Värskendage jaotises **Ajakannete uued väärtused** väljad vajadusel õige teabega. Näiteks saate muuta määratud projekti või reserveeritavat ressurssi.

6. Valige **Eelvaade**. Valkige dialoogiboksis **OK**. Vahekaardil **Töölehe read** saate vaadata algsete tegelike näitajate loendit, mis on seotud valitud ajakannetega, mis on tagasipööratud, ja neile vastavate loodud parandatud ridadega. Kui tuleb teha täiendavaid parandusi, korrake etappe 5 ja 6. 

    > [!NOTE]
    > Kõik parandatud tegelikud väärtused on samad, mille valisite jaotises **Ajakannete uued väärtused**.

7. Kui parandust kuvatakse nii nagu eeldati, valige **Kinnita**. Valkige dialoogiboksis **OK**.

8. Minge tagasi alasse **Müük**, valige **Projektid** ja seejärel avage projekt, mille ajakandeid te äsja uuendasite. 

9. Vaadake tehtud muudatusi lehe **Projektid** vahekaardil **Tegelikud näitajad**. 

    > [!NOTE]
    > Kui vahekaart **Tegelikud näitajad** ei ole kuvatud, valige **Seostuvad** > **Tegelikud näitajad**.  

10. Loendis **Tegelik seostatud vaade** näete, et tagasipööratud algsed ajakanded on endiselt loetletud, nagu on ka vastavad parandatud ajakanded. 

 
## <a name="correct-approved-expense-entries"></a>Kinnitatud kulukirjete parandamine

Ühe või rohkema kulukirje parandamiseks läbige järgmised etapid. 

1. Valige alas **Müük** vasakpoolsel navigeerimispaanil jaotise **Tehingud** all **Kinnitatud kulud**.

2. Valige loendis **Kinnitatud kulud** projekt, mida soovite parandada, ja seejärel valige **Kirjete parandamine**. Luuakse automaatselt uus paranduse tööleht, millele on määratud tüüp **Kulude parandus**. 

3. Sisestage lehel **Uus tööleht** parandusele **Kirjeldus** ja valige vahekaardi **Kulude parandus** jaotises **Kulude uued väärtused** need andmeväljad, mida soovite valitud kuluridade puhul parandada. Näiteks saate määrata kulu teisele **Projektile** või parandada väärtusi **Kulu kategooria**, **Kulu kuupäeva** või **Reserveeritav ressurss**.

4. Valige **Eelvaade**. Valkige dialoogiboksis **OK**. 

5. Kinnitage parandused vahekaardil **Töölehe read**. Saate vaadata algsete tegelike näitajate loendit, mis on seotud valitud kulukirjetega, mis on tagasipööratud, ja neile vastavate loodud parandatud ridadega.

6. Kui parandatud väärtused on sellised nagu eeldati, valige **Kinnita**. Valkige dialoogiboksis **OK.** Kui väärtused ei ole näidatud nii nagu eeldatud, valige **Tühista**, et naasta loendisse **Kinnitatud kulud**. Korrake toiminguid 2 kuni 5. 

7. Pärast parandustöölehe kinnitamist naaske muudatuste vaatamiseks värskendatud projekti või projektide juurde.

8. Vaadake projekti lehel vahekaardil **Tegelikud andmed üle** loend Tegelik seostatud **vaade**. Loetletud on algsed kirjed ja parandatud kirjed.


## <a name="correct-approved-material-usage-logs"></a>Parandatud kinnitatud materjali kasutuslogid

Ühe või mitme materjali kasutuslogi kande parandamiseks tehke järgmist.

1. Valige **alal Müük** vasakpoolsel navigeerimispaanil jaotises **Kanded** väärtus **Tegelikud**.

2. **Kasutage loendis Tegelikud veerufiltrid** materjalikande **klassi valimiseks**, nii et kuvatakse ainult materjalide tegelikud tegelikud andmed. Kuvatavate tegelike lahtrite edasiseks piiramiseks kasutage muid veerufiltreid. Pärast soovitud tegelike kogumi leidmist valige tegelikud andmed ja seejärel valige **Õiged kanded**. Luuakse automaatselt uus parandustööleht ja **määratakse materjaliparanduse** tüüp.

3. Sisestage **lehe Uus tööleht** väljale **Kirjeldus** paranduse kirjeldus. **Seejärel valige menüü** Materjaliparandus **jaotises Uued materjaliväärtused** valitud materjaliridade jaoks korrigeeritavad andmeväljad. Näiteks saate materjali määrata mõnele muule projektile või parandada toodet, materjali kuupäeva või allhankelepingut.

4. Valige **Eelvaade**. Seejärel valige dialoogiboksis **OK**.

5. Kontrollige vahekaardil **Töölehe read** parandusi. Saate vaadata loendit algsetest tegelikest, mis on seotud tühistatud valitud materjalikannetega ja loodud parandatud vastavate ridadega.

6. Kui parandatud väärtused on sellised nagu eeldati, valige **Kinnita**. Seejärel valige dialoogiboksis **OK**. Kui väärtused pole ootuspärased, valige **loendisse Tegelikud** naasmiseks **Loobu**. Seejärel korrake samme 2 kuni 5.

7. Pärast parandustöölehe kinnitamist naaske muudatuste vaatamiseks värskendatud projekti või projektide juurde.

8. Vaadake projekti lehel vahekaardil **Tegelikud andmed üle** loend Tegelik seostatud **vaade**. Loetletud on algsed kirjed ja parandatud kirjed.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
