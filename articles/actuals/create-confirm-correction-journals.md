---
title: Paranduste töölehtede loomine ja kinnitamine
description: See artikkel annab teavet, kuidas luua ja kinnitada paranduse töölehte.
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
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928059"
---
# <a name="create-and-confirm-correction-journals"></a>Paranduste töölehtede loomine ja kinnitamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Mõnikord võib aja- või kulukirje olla valesti sisestatud. Näiteks võib konsultant valida ajakirje loomisel vale kuupäeva või kulu sisestamisel valida vale projekti. Kui konsultant ei saa esitatud kirjeid värskendada, saab taustaadministraator projekti tegelikke näitajaid otse parandada.

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

7. Pärast paranduste töölehe kinnitamist liikuge tagasi värskendatud projekti või projektide juurde, et saaksite oma muudatusi vaadata.

8. Vaadake projekti lehe vahekaardil **Tegelikud näitajad** loendit **Tegelik seostatud vaade**. Loetletud on algsed kirjed ja parandatud kirjed.


## <a name="correct-approved-material-usage-logs"></a>Korrigeeritud kinnitatud materjalikasutuse logid

Ühe või mitme materjalikasutuse logi kirje parandamiseks täitke järgmised toimingud.

1. Valige alas **Müük** vasakpoolsel navigeerimispaanil jaotise **Tehingud** all **Tegelikud näitajad**.

2. Valige loendis **Tegelikud näitajad** veergude filtrite abil tehinguklass **Materjal**, nii et kuvatakse ainult materjalide tegelikud näitajad. Kasutage muid veergude filtreid, et kuvatud tegelikke näitajaid veelgi piirata. Kui olete leidnud soovitud tegelike näitajate kogumi, valige tegelikud näitajad ja seejärel valige **Korrektsed kirjed**. Uus paranduse tööleht luuakse automaatselt ja sellele määratakse tüüp **Materjali parandus**.

3. Leheküljel **Uus tööleht** sisestage lahtrisse **Kirjeldus** paranduse kirjeldus. Seejärel valige vahekaardi **Materjali parandus** jaotises **Materjalide uued väärtused** andmeväljad, mida valitud materjaliridade jaoks parandada. Näiteks saate määrata materjali mõnele teisele projektile või parandada toodet, materjali kuupäeva või alltöövõttu.

4. Valige **Eelvaade**. Seejärel valige dialoogiboksis **OK**.

5. Kontrollige parandusi vahekaardil **Töölehele kandmine**. Saate vaadata algsete tegelike näitajate loendit, mis on seotud valitud materjali kirjetega, mis on tagasipööratud, ja neile vastavate loodud parandatud ridadega.

6. Kui parandatud väärtused on sellised nagu eeldati, valige **Kinnita**. Seejärel valige dialoogiboksis **OK**. Kui väärtused ei vasta ootustele, valige **Tühista** loendisse **Tegelikud näitajad** naasmiseks. Seejärel korrake samme 2 kuni 5.

7. Pärast paranduste töölehe kinnitamist liikuge tagasi värskendatud projekti või projektide juurde, et saaksite oma muudatusi vaadata.

8. Vaadake projekti lehe vahekaardil **Tegelikud näitajad** loendit **Tegelik seostatud vaade**. Loetletud on algsed kirjed ja parandatud kirjed.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
