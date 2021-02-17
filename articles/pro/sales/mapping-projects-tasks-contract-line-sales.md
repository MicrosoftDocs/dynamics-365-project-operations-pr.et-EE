---
title: Projektide ja ülesannete vastendamine projektipõhise lepingureaga – liht
description: Selles teemas kirjeldatakse projektide ja toimingute lepingureale lisamist ja sealt eemaldamist.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 30a74f683a032d5bd6caed347f4d0a948376d267
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177641"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line---lite"></a>Projektide ja ülesannete vastendamine projektipõhise lepingureaga – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Projektipõhistel lepinguridadel saate vastendada projekti konkreetsed ülesanded lepingureaga.

Kui vastendate konkreetsed ülesanded lepingurea, rakenduvad arveldamise meetod, arveldatavuse valikud, mitteületatavad limiidid ja lepingureal määratletud kliendid ainult neile konkreetsetele ülesannete.

Kui teil on stsenaarium, kus projekti üks faas (näiteks prototüübi faas) on fikseeritud hinnaga ja kõik muud faasid on aja ja materjali põhised, on teil võimalik seostada prototüübi faas ja kõik sellega seotud alam-ülesanded selle etapi lepingureaga fikseeritud hinna arveldusmeetodil.

Kõik teie projekti tööjaotuse struktuuri (WBS) muud etapid saab seostada aja- ja materjalipõhise lepingureaga.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Ülesannete seostamine projektipõhiste lepinguridadega

Ülesanded saab seostada lepinguridadega vahekaardilt **Arveldatavad ülesanded** lehel **Lepingurida** või vahekaardilt **Ülesande arveldamine** lehel **Projekt**.

### <a name="from-the-contract-line-page"></a>Lepingurea lehelt

Projekti ülesannete seostamiseks lepingureaga vahekaardilt **Arveldatavad ülesanded** lehel **Lepingurida** tehke järgmist.

1. Kontrollige projektipõhise lepingurea vahekaardil **Üldine**, et väli **Projekt** oleks täidetud.
2. Väljal **Kaasatud ülesanded** valige suvand **Ainult valitud ülesanded**.
3. Salvestage muudatused. Vorm värskendatakse ja vahekaart **Arveldatavad ülesanded** on nähtav.
4. Valige vahekaart **Arveldatavad ülesanded** ja valige andmeruudustikus suvand **Lisa lepingurea ülesanne**.
5. Valige lehe **Lepingurea ülesanded** rippmenüüst **Ülesanded** tööülesanne. 
6. Sisestage väljale **Arveldustüüp** teave ja valige seejärel nupp **Salvesta ja sule**. Valitud ülesanne seostatakse lepingureaga.

> [!NOTE]
> See pole projekti ülesannete lepinguridadega seostamiseks kõige optimaalsem kogemus. Iga projekt tuleb selles kogemuses käsitsi seostada. Eelistatud viis on vahekaardilt **Ülesande arveldamine** lehel **Projekt**.

### <a name="from-the-project-page"></a>Projekti lehelt

See on ülesannete lepinguridadega seostamiseks optimaalne meetod. Saate valida mitu tööülesannet ning seostada kõik need ja nende alam-ülesanded valitud lepingureaga. Ülesannete seostamiseks lepingureaga lehel **Projekt** tehke järgmist.

1. Kontrollige projektipõhise lepingurea vahekaardil **Üldine**, et väli **Projekt** oleks täidetud.
2. Väljal **Kaasatud ülesanded** valige suvand **Ainult valitud ülesanded**.
3. Salvestage projektipõhine lepingurida. Vorm värskendatakse ja vahekaart **Arveldatavad ülesanded** on nähtav. Selle eesmärk on ainult kontrollimine.
4. Valige projektipõhise lepingurea vahekaardil **Üldine** väljal **Projekt** projekti link.
5. Valige lehel **Projekt** vahekaart **Ülesande arveldamise seadistus**.
6. Seal on kaks ruudustikku. Üks ruudustik on lepinguridadele, mis rakenduvad kogu projektile. Teine ruudustik kohaldub ülesandele spetsiifilisele arveldamise seadistusele. Valige teises ruudustikus üks või mitu tööülesannet ja valige seejärel suvand **Seosta lepinguread**.
7. Valige avaneval dialoogi lehel ripploendist lepingurida.
8. Kasutage ripploendit **Arveldustüüp**, et märkida ülesanded arveldatavaks või mitte-arveldatavaks.
9. Vlige märkeruut, et näidata, kas seostamine peaks hõlmama ka valitud ülesannete alam-ülesandeid. Ruudu märkimine seostab ka valitud ülesannete alam-ülesanded lepingureaga.
10. Valige dialoogi sulgemiseks nupp **Ok**.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Ülesannete seostamise tühistamine projektipõhiste lepinguridadega

### <a name="from-the-contract-line-page"></a>Lepingurea lehelt

Projekti ülesannete seostamise lõpetamiseks lepingureaga vahekaardilt **Arveldatavad ülesanded** lehel **Lepingurida** tehke järgmist.

1. Valige vahekaardil **Arveldatavad ülesanded** käsk **Kustuta lepingurea ülesanne**.
2. Hoiatusteade näitab, et selle seose eemaldamine võib põhjustada mis tahes varem tööülesandele salvestatud tegelike andmete tagasipööramist. Valige dialoogis **OK**, et eemaldada ülesande ja projektipõhise lepingurea seos. 

> [!NOTE]
> See ei kustuta ülesannet projektist. Selle asemel eemaldatakse ülesande seos projektipõhiselt lepingurealt.

### <a name="from-the-project-page"></a>Projekti lehelt

See pole projekti ülesannete lepinguridade seostamise lõpetamiseks palju optimaalsem kogemus. Saate valida mitu tööülesannet ning katkestada kõigi nende ja nende alam-ülesannete seosed valitud lepingureaga. Ülesannete seostamise lõpetamiseks lepingureaga tehke järgmist.

1. Klõpsake projektipõhise lepingurea vahekaardil **Üldine** väljal **Projekt** projekti linki.
2. Valige lehel **Projekt** vahekaart **Ülesande arveldamise seadistus**.
3. Lehel on kaks ruudustikku. Üks ruudustik on lepinguridade jaoks, mis rakenduvad kogu projektile, ja teine kohaldub ülesandele spetsiifilisele arveldamise seadistusele. Valige teises ruudustikus üks või mitu tööülesannet ja valige suvand **Eemalda lepinguridade seos**.
4. Valige avaneval dialoogi lehel ripploendist lepingurida.
5. Vlige märkeruut, et näidata, kas seose eemaldamine peaks hõlmama ka valitud ülesannete mis tahes alam-ülesandeid. Ruudu märkimine eemaldab ka valitud ülesannete alam-ülesannete seose lepinguridadega.
6. Valige **OK**. Hoiatusteade näitab, et selle seose eemaldamine võib põhjustada mis tahes varem tööülesandele salvestatud tegelike andmete tagasipööramist. Valige hoiatusdialoogis **OK**, et eemaldada ülesande ja projektipõhise lepingurea seos.