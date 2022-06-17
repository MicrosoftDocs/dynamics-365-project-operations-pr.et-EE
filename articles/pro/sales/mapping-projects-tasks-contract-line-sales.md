---
title: Projektide ja ülesannete vastendamine projektipõhise lepingureaga – liht
description: Selles artiklis antakse teavet projektide ja ülesannete lisamise ja eemaldamise kohta lepingureale.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c8075e3161acd904969f964e5ab32dfe04edc4b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932521"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Projektide ja ülesannete vastendamine projektipõhise lepingureaga 

_**Kehtib järgmistele:** lihtjuurutamine – tehing näidisarveldusele, Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks_

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
