---
title: Projekti reserveeringu loomine ajakavapaneelilt
description: Selles teemas kirjeldatakse, kuidas ajakavapaneelilt projekti reserveeringut luua.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d33786a5d0a2485a06d174eb7afcbaaa2f337cf6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992961"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Projekti reserveeringu loomine ajakavapaneelilt

[!include [banner](../includes/psa-now-project-operations.md)]

Te saate ressursi projektile reserveerida kas otse vahekaardil **Meeskond** või luues ressursinõude üldise meeskonnaliikme määrangust ja seejärel loodud nõuet projekti meeskonnaliikmega täites.

Samuti saate ressurssi projektile reserveerida otse ajakavapaneelilt. Selle tegemiseks on kolm viisi:

- **Broneerige loodud ressursinõudest:** saate luua ressursinõude pärast seda, kui loote üldise ressursi ja määrate projekti raames tööülesanded.

- **Broneerige esmasest nõudest:** esmased nõuded kuvatakse ajakavapaneelil vahekaardil **Projekt**. 

- **Broneerige uuest ressursinõudest:** saate luua ressursinõude nullist ja seostada selle projektiga. Ajakavapaneelil kuvatakse ressursinõuet vahekaardil **Avatud nõuded**.

## <a name="book-from-a-generated-resource-requirement"></a>Loodud ressursinõude kaudu reserveerimine

Saate luua üldise ressursi ja määrata sellele projektis ülesande või mitu ülesannet. Seejärel loote üldise meeskonnaliikme kaudu ressursinõude. 

1.  Ajakavapaneelil kuvatakse seda ressursinõuet vahekaardil **Avatud nõuded**. Kui teil on mitu avatud nõuet, võib teil ruudustikus vaja minna veerufiltrite abi. 

    ![Nõude vahekaardi avamine ajakavapaneelil](media/FAQ-Project-Booking-Schedule-Board-1.png "Kuvatõmmis reserveeringute ja määrangute tabelist")

2. Valige nõue. Valitud rea kohal avaneb vahekaart **Otsi kättesaadavust**.
 
3. Selle vahekaardi valimine käivitab ajakavapaneeli ajakava abi, mis filtreerib ressursinõudele vastavad saadavalolevad ressursid. Pärast seda saate ressurssi reserveerida.

4. Samuti saate ajakavapaneeli all valitud rea pukseerida ülalolevas ruudustikus olevale ressursile. Kui selle paigale asetate, avaneb paremal paneel **Ressursi reserveeringu loomine**.

    Käsu **Reserveeri** valimine reserveerib ressursi projekti meeskonda.

![Ressursi broneeringu loomine](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Peamisest nõudest reserveerimine

Projekti loomisel rakenduses Project Service luuakse automaatselt ressursinõue nimetusega peamine nõue. Tegemist on tühja nõudega, mida kasutatakse ajakavapaneeli kaudu ressursi kiireks reserveerimiseks ilma nõude genereerimiseta või täiesti uue nõude loomiseta. Kuna nõue on tühi, peate täpsustama nii kuupäevad kui ka eraldamismeetodi ja vajaduse korral tunnid. 

1. Peamise nõudega ressursi reserveerimiseks ajakavapaneelil valige vahekaart **Projekt**. Kui teil on palju projekte, peate võib olla kasutama veerus **Projekt** veerufiltreid.

   ![Veerufiltrid ajakavapaneelil](media/FAQ-Project-Booking-Schedule-Board-2.png "Kuvatõmmis reserveeringute ja määrangute tabelist")

2. Valige nõue, mille nimeks on vaid projekti nimi ja kestus on null (0).

3. Valige rea kohal avanev vahekaart **Otsi kättesaadavust**. See käivitab ajakavapaneeli ajakava abirežiimi ja näitab saadavalolevaid ressursse, mida saab projektile reserveerida.

4. Kuna **peamine nõue** on tühi nõue, mille kestus on null (0), peate kestuse määrama paneeli **Ressursi reserveeringu loomine** kaudu, kui valite ja reserveerite ressursi.

5. Samuti saate valida **projekti peamise nõude** ajakavapaneeli alt ja pukseerida selle ressursile, et reserveerida.
 
    Kuna **peamine nõue** on tühi nõue, mille kestus on null (0), peate kestuse määrama paneeli **Ressursi reserveeringu loomine** kaudu, kui valite ja reserveerite ressursi.
 
    Kui reserveerite ressurssi ajakavapaneeli **peamise nõude** kaudu, siis lisate selle projekti meeskonnale ilma ühegi määranguta.
 
## <a name="book-from-a-new-resource-requirement"></a>Uue ressursinõude kaudu reserveerimine
Uue ressursinõude kaudu broneerimiseks täitke järgmised juhised. 

1. Avage jaotis **Ressursinõuded** ja valige käsk **Uus**, et luua uus ressursinõue.

2. Valige vahekaardil **Projekt** projekti nõude seostamiseks projekt.
 
    Seda uut nõuet kuvatakse ajakavapaneelil **avatud nõudena**, mida saate täita.

3. Reserveerige ressurss, et lisada see projekti meeskonda.

4. Nüüd, kui ressurss on reserveeritud, peate ülesandeid käsitsi määrama.



[!INCLUDE[footer-include](../includes/footer-banner.md)]