---
title: Projektide ja ülesannete vastendamine projektipõhise hinnapakkumise reaga
description: Selles teemas kirjeldatakse projektide ja tööülesannete vastendamist projektipõhise tööülesande reaga.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 6b396ccf5e76230a42a2f933a3aaa5b8149790bb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/06/2020
ms.locfileid: "3964902"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Projektide ja ülesannete vastendamine projektipõhise hinnapakkumise reaga

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Projektipõhistel hinnapakkumiste ridadel saate vastendada juba hinnapakkumise reaga seostatud projekti konkreetsed ülesanded.

Kui vastendate tööülesanded hinnapakkumise reaga, rakendatakse järgmisi hinnapakkumise real määratletud üksusi ainult nendele ülesannetele.

- Arveldusmeetod
- Arveldatavuse valikud
- Mitteületatavad limiidid
- Kliendid

Näiteks võib teil olla projekt, kus üks etapp on fikseeritud hinnaga ja kõik ülejäänud etapid on aja ja materjalide põhjal. Sel juhul saate seostada esimese etapi ja kõik selle alluvad tööülesanded selle etapi hinnapakkumise rea fikseeritud arveldusmeetodiga. Seejärel saate kõik muud etapid seostada aja- ja materjalidepõhise hinnapakkumise reaga.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Projektipõhiste hinnapakkumise ridadega ülesannete seostamine

Saate tööülesanded seostada hinnapakkumiste ridadega järgmistest asukohtadest.

- Leht **Projekt** > vahekaart **Ülesande arveldus** (optimaalne)
- Leht **Hinnapakkumise rida** vahekaart > **Arveldatavad ülesanded** 

### <a name="from-the-project-page"></a>Projekti lehelt

Leht **Projekt** pakub optimaalset kogemust ülesannete seostamiseks hinnapakkumise ridadega. Sellel lehel saate valida mitu tööülesannet ja seostada kõik need ning nende alluvad tööülesanded valitud hinnapakkumise reaga.

1. Kontrollige, et projektipõhise hinnapakkumise rea vahekaardil **Üldine** olekt täidetud väli **Projekt**.
2. Valige väljal **Kaasatud tööülesanded** valik **Ainult valitud tööülesanded**.
3. Salvestage projektipõhine hinnapakkumise rida. Vormi värskendamisel kuvatakse vahekaarti **Arveldatavad tööülesanded**.
4. Valige vahekaardil **Üldine** projektile link väljalt **Projekt**.
5. Valige lehel **Projektid** vahekaart **Ülesande arveldus**.
6. Valige teisest ruudustikust, mis puudutab ülesandepõhise arvelduse seadistamist, üks või rohkem ülesannet ja seejärel valige suvand **Seosta hinnapakkumise read**.
7. Valige kuvatavas dialoogis hinnapakkumise rida, kus kuvatakse hinnapakkumisel projektipõhiseid hinnapakkumise ridu.
8. Märkige väljal **Arvelduse tüüp**, kas need toimingud on arveldatavad või mitte.
9. Märkige ruut, kui soovite, et ühing peaks kaasama valitud tööülesannete alluvad tööülesanded. Kasti märkimine seostab valitud ülesannete tütarülesanded hinnapakkumise reaga.
10. Valige dialoogi sulgemiseks nupp **Ok**.

### <a name="from-the-quote-line-page"></a>Hinnapakkumise rea lehelt

Projekti tööülesanded saate seostada hinnapakkumise ridadega vahekaardil **Arveldatavad ülesanded** lehel **Hinnapakkumise rida**.

>[!NOTE]
>Optimaalne koht projekti ülesannete seostamiseks hinnapakkumiste ridadega on vahekaart **Ülesande arveldus** lehel **Projekt**. Kui seostate tööülesanded vahekaardilt **Arveldatavad ülesanded** lehelt **Hinnapakkumise rida**, peate iga projekti käsitsi seostama.

1. Kontrollige, et projektipõhise hinnapakkumise rea vahekaardil **Üldine** oleks väljal **Projekt** projekt valitud.
2. Valige väljal **Kaasatud tööülesanded** valik **Ainult valitud tööülesanded**.
3. Salvestage projektipõhine hinnapakkumise rida. Vormi värskendamisel kuvatakse vahekaarti **Arveldatavad tööülesanded**.
4. Valige vahekaardil **Arveldatavad ülesanded** suvand **Lisa hinnapakkumise rea tööülesanne**.
5. Valige lehe **Hinnapakkumise rea ülesanne** väljal **Ülesanded** ülesanne ja valige väljal **Arvelduse tüüp** käsk **Salvesta**. 
6. Sulgege leht. Valitud tööülesanne on nüüd seotud hinnapakkumise reaga.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Ülesannete projektipõhiste hinnapakkumiste ridadest lahti sidumine

### <a name="from-the-project-page"></a>Projekti lehelt

See meetod pakub kõige optimaalsemat kogemust ülesannete hinnapakkumiste ridadest lahti sidumiseks. Saate valida mitu tööülesannet ja siduda valitud hinnapakkumise reast lahti kõik need ning nende alluvad tööülesanded.

1. Valige projekti link projektipõhise hinnapakkumise rea vahekaardilt **Üldine** väljal **Projekt**.
2. Valige lehel **Projektid** vahekaart **Ülesande arveldus**.
3. Valige teisest ruudustikust, mis puudutab ülesandepõhise arvelduse seadistamist, üks või rohkem ülesannet ja seejärel valige suvand **Hinnapakkumise ridade lahti sidumine**.
4. Valige kuvatavas dialoogiboksis hinnapakkumise rida.
5. Märkige ruut, et näidata, kas soovite, et seotus tuleks eemaldada ka valitud ülesannete tütarülesannetelt. Kasti märkimine seob hinnapakkumise reast lahti seob lahti ka tütarülesanded.
6. Valige **OK**. Hoiatusteade hoiatab teid, et kui eemaldate selle seose, võidakse kõik varem toimingule salvestatud tegelikud näitajad tagasi pöörata. 
7. Valige **OK**, et jätkata ja eemaldada seos ülesande ja projektipõhise hinnapakkumise rea vahel.

### <a name="from-the-quote-line-page"></a>Hinnapakkumise rea lehelt

Projekti tööülesanded saate hinnapakkumise ridadest lahti siduda ka vahekaardil **Arveldatavad ülesanded** lehel **Hinnapakkumise rida**.

1. Valige vahekaardil **Arveldatavad ülesanded** suvand **Tühista hinnapakkumise rea tööülesanne**.
2. Valige **OK**. Hoiatusteade hoiatab teid, et kui eemaldate selle seose, võidakse kõik varem toimingule salvestatud tegelikud näitajad tagasi pöörata. 
3. Valige **OK**, et jätkata ja eemaldada seos ülesande ja projektipõhise hinnapakkumise rea vahel.

>[!NOTE]
> See toiming ei kustuta tööülesannet projektist. See eemaldab ainult tööülesande seose projektipõhiselt hinnapakkumise realt.
