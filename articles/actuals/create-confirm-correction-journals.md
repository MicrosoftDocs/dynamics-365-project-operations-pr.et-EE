---
title: Paranduste töölehtede loomine ja kinnitamine
description: Selles teemas antakse teavet, kuidas luua ja kinnitada paranduse töölehte.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6cc22168cdfefc4ae7b833bea75f68ba37c1ee67
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127741"
---
# <a name="create-and-confirm-correction-journals"></a>Paranduste töölehtede loomine ja kinnitamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Mõnikord võib aja- või kulukirje olla valesti sisestatud. Näiteks võib konsultant ajakirje loomisel valida vale kuupäev või kulu sisestades numbrite järjekorda muuta. Kui konsultant ei saa esitatud kirjetele värskendusi teha, saab administraator projekti kirje otse ära parandada.

Selle teema toimingute lõpuleviimiseks on teil vaja administraatori õigusi.

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

Näiteks on järgmisel joonisel kaks reaüksust kogustega 8.00, millel on summa veerus loetletud deebetid. Lisaks on kaks reaüksust kogusega -8.00, mis näitavad summa veerus krediteeritud summasid. Need parandused viivad koguse nulli.

 
## <a name="correct-approved-expense-entries"></a>Kinnitatud kulukirjete parandamine

Ühe või rohkema kulukirje parandamiseks läbige järgmised etapid. 

1. Valige alas **Müük** vasakpoolsel navigeerimispaanil jaotise **Tehingud** all **Kinnitatud kulud**.

2. Valige loendis **Kinnitatud kulud** projekt, mida soovite parandada, ja seejärel valige **Kirjete parandamine**. Luuakse automaatselt uus paranduse tööleht, millele on määratud tüüp **Kulude parandus**. 

3. Sisestage lehel **Uus tööleht** parandusele **Kirjeldus** ja valige vahekaardi **Kulude parandus** jaotises **Kulude uued väärtused** need andmeväljad, mida soovite valitud kuluridade puhul parandada. Näiteks saate määrata kulu teisele **Projektile** või parandada väärtusi **Kulu kategooria**, **Kulu kuupäeva** või **Reserveeritav ressurss**.

4. Valige **Eelvaade**. Valkige dialoogiboksis **OK**. 

5. Kinnitage parandused vahekaardil **Töölehe read**. Saate vaadata algsete tegelike näitajate loendit, mis on seotud valitud kulukirjetega, mis on tagasipööratud, ja neile vastavate loodud parandatud ridadega.

6. Kui parandatud väärtused on sellised nagu eeldati, valige **Kinnita**. Valkige dialoogiboksis **OK.** Kui väärtused ei ole näidatud nii nagu eeldatud, valige **Tühista**, et naasta loendisse **Kinnitatud kulud**. Korrake toiminguid 2 kuni 5. 

> [!NOTE]
> Parandatud tegelikud väärtused on samad, mille valisite jaotises **Kulude uued väärtused**.

7. Pärast paranduste töölehe kinnitamist minge tagasi värskendatud projekti või projektide juurde, et saaksite oma muudatusi vaadata.  

8. Vaadake projekti lehe vahekaardil **Tegelikud näitajad** välja **Tegelik seostatud vaade**. Loetletud on algsed kirjed ja parandatud kirjed. Järgmisel joonisel on kuvatud algsed kulukirje summad ja vastavad parandatud kulukirje summad. 


