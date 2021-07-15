---
title: Mis on uut juulis 2021 – Project Operationsi lihtjuurutus
description: Selles teemas antakse teavet Project Operationsi lihtjuurutuse 2021. aasta juuli väljaandes olevate kvaliteedivärskenduste kohta.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6992498df5beb97d4e7197e301f093320dc28a23
ms.sourcegitcommit: 3abf1e67938d91bd826b025ae3187cd313f556b9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433648"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Mis on uut juulis 2021 – Project Operationsi lihtjuurutus

_Kohaldub: lihtjuurutus - tehing proforma arveldusega_

See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.

  - Project Operations Dataverse’i keskkonna versioonis 4.12.0.148.

## <a name="quality-updates"></a>Kvaliteedi värskendused
| **Funktsiooni ala**              | **Viitenumber** | **Kvaliteedi värskendus**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Arveldamine ja hinnakujundus           | 2224046              | Väli **Kannete klass** on redigeeritav vahekaardil **Hinnapakkumise rea üksikasjad**, kuid see on lukus, kui töötate lehelt **Hinnapakkumise rea üksikasjad**.                                                                     |
| Arveldamine ja hinnakujundus           | 2224400              | Toiming **Sule hinnapakkumine võidetuna** nurjub, kui hinnapakkumisel pole kuupäeva vahe-eesmärke.                                                                                                                                    |
| Arveldamine ja hinnakujundus           | 2234089              | Kui sisestate toote kirjelduse käsitsi, tühjendatakse see pärast materjalide prognoosi koguse sisestamist.                                                                                                                         |
| Arveldamine ja hinnakujundus           | 2234100              | Ruudustik **Ülesande arveldamise häälestus** ei sisalda veergu **Materjal** ja selle väärtust projekti vahekaardil **Ülesande arveldamine**.                                                                                                       |
| Arveldamine ja hinnakujundus           | 2277409              | Toote ID pole materjalitüübi rea jaoks lepingurea üksikasjades saadaval.                                                                                                                                        |
| Arveldamine ja hinnakujundus           | 2281728              | Lepingurea mittevajalike uuesti hindamise tegelike näitajate loomine põhjustab andmemahu olulist kasvu, mis mõjutab jõudlust.                                                                                |
| Arveldamine ja hinnakujundus           | 2298668              | Tagasi võetud ja kustutatud kuluga seotud töölehe ridasid ei eemaldata.                                                                                                                                     |
| Arveldamine ja hinnakujundus           | 2300192              | Kui arvet redigeerib mitu kasutajat, saab kinnitatud arvel luua uue arve rea üksikasju.                                                                                   |
| Arveldamine ja hinnakujundus           | 2301569              | Arveid ei saa parandada, kui rakendatud on honorari summa \$0.                                                                                                                                        |
| Arveldamine ja hinnakujundus           | 2307965              | Kui kategooria hind luuakse puuduvate väärtustega, kuvatakse tõrge.                                                                                                                           |
| Arveldamine ja hinnakujundus           | 2326870              | Tõrge atribuudis **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** kui **producttypecode** on nullväärtusega.                                                                            |
| Arveldamine ja hinnakujundus           | 2332732              | Kui lepingurea vahe-eesmärk luuakse ilma tellimuse reata, kuvatakse tõrge.                                                                                                                |
| Projekti plaanimine ja jälgimine | 2181094              | Projekti ajastamise API toetab nüüd PSS-i logisid ja toimingukomplekti logisid, mida säilitatakse 90 päeva.                                                                                                                  |
| Projekti plaanimine ja jälgimine | 2254201              | Silt **Ajakavarežiim** värskendatakse üksikasjadega, mis kirjeldavad vaikeloogikat.                                                                                                                                      |
| Projekti plaanimine ja jälgimine | 2300252              | Vastuse **openProject** vahemälu värskendatakse ja see sisaldab vahemälu võtme, **põhi-URL-i** ja **Segmendi URL-i** loa omanikku, et **Taotluse URL** saaks alati uuesti luua, kui **põhi-URL** muutub. |
| Projekti plaanimine ja jälgimine | 2301312              | **msdyn_membershipstatus** on **projektimeeskonna liikme** vaatest eemaldatud.                                                                                                                                        |
| Projekti plaanimine ja jälgimine | 2302759              | Tooteid tuuakse tarbetult vahekaartidel **Ressursimääramised**, **Prognoosid** ja **Kuluprognoosid**.                                                                                                        |
| Projekti plaanimine ja jälgimine | 2308050              | **CopyProject** nurjub tõrkega „Kaugteenusega rääkimise sõne toomine nurjus”.                                                                                                                           |
| Projekti plaanimine ja jälgimine | 2322650              | Vaade **Projektiülesande loend** on värskendatud, et kuvada vaikimisi ülesande kuupäev.                                                                                                            |
| Projekti plaanimine ja jälgimine | 2327266              | **CopyProject** tekita prognooside kopeerimisel tõrke „Võtit ei leitud sõnastikust”.                                                                                                      |
| Projekti plaanimine ja jälgimine | 2328123              | **CopyProject** loob tõrke „Kaugteenusega rääkimise sõne toomine nurjus”.                                                                                                                          |
| Projekti plaanimine ja jälgimine | 2336258              | **CopyProject** ikopeerib ressursside asukohanimed valesti.                                                                                                                                                 |
| Arveldamine ja hinnakujundus           | 2224476              | Väli **Broneeritatav ressurss** ei lähe vaikimisi õigesti tagasi logitud kasutajale lehel **Materjali kasutus**.                                                                                                            |
| Ressursihaldus           | 2277249              | Ilmub tõrge, kui mitte-projektipõhist nõuet värskendatakse.                                                                                                            |
| Ressursihaldus           | 2323869              | Ressursi kasutamine ei tunne filtreeritud ressursse õigesti ära.                                                                                                                                             |
| Aeg ja kulu              | 2176538              | Juhtelemendile **Ajakirje** rakendatakse valed filtritoimingud.                                                                                                                                                   |
| Aeg ja kulu              | 2177462              | Ajakirje ruudustikust kustutamisel ei värskendata nuppude **Esita**, **Võta tagasi**, **Kustuta** ja **Redigeeri kirjet** olekuid eeldatud viisil.                                                                                        |
| Aeg ja kulu              | 2299985              | **TimeEntriesImportFromResourceAssignment** ei säilita algus-/lõpuaega määramise kontuuridest.                                                                                                  |
| Aeg ja kulu              | 2318426              | Pärast ajakirje esitamist saab lukus välju endiselt redigeerida.                                                                                                                                   |
| Aeg ja kulu              | 2323749              | Kulu loomisel broneeritatava ressursi vahekaardilt **Seotud** ilmneb tõrge.                                                                                                      |
| Aeg ja kulu              | 2327678              | Kui loote broneeritatava ressursi vahekaardilt **Seotud**, ei edastata põhiressurssi ajakirje juhtelemendile.                                                                            |
| Üldist                       | 2296857              | Pikaajaliste tööde edenemise jälgimine.                                                                                                                                                                        |
| Üldist                       | 2253682              | Project Operationsi topeltkirjutamise lahendust ei peaks installima, kui topeltkirjutamise tuum on installitud keskkonnas, kus puudub topeltkirjutamise korraldamise lahendus.                                                |
| Üldist                       | 2316420              | Project Service’i tuuma ettevalmistamine nurjub, kui rakenduse kasutaja ettevõtte üksust muudetakse.                                                                                                                     |