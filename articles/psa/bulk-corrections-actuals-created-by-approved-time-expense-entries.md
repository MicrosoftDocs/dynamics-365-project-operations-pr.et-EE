---
title: Kinnitatud aja- ja kulukirjete loodud tegelike näitajate hulgiparandused
description: Selles teemas selgitatakse, kuidas administraator saab teha üksikuid või hulgiparandusi eelnevalt kinnitatud aja- või kulukirjetele, kui arveldus ei ole lõpetatud.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 063c4d017f5904f09c3c239bfa432a128872e4d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144948"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Kinnitatud aja- ja kulukirjete loodud tegelike näitajate hulgiparandused

[!include [banner](../includes/psa-now-project-operations.md)]

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

![Tegelik seostatud vaate loend](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
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

![Kulute tegelikud näitajad](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
