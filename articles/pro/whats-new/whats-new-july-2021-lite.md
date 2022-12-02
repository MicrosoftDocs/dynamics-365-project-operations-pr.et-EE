---
title: Mis on uut juulis 2021 – Project Operationsi lihtjuurutus
description: See artikkel annab teavet Project Operationsi lihtjuurutuse 2021. aasta juuli väljaandes olevate kvaliteedivärskenduste kohta.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7964f38c1bc7a8e0440e2e922ff153fd9bede131
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913983"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Mis on uut juulis 2021 – Project Operationsi lihtjuurutus

_Kohaldub: lihtjuurutus - tehing proforma arveldusega_

See artikkel kehtib rakenduse Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

  - Project Operations Dataverse’i keskkonna versioonis 4.12.0.148 või 4.12.0.152.

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
| Üldist                       | 2376405              | Parandati väljaandjapõhine värskendusprobleem (kvaliteedivärskendus on saadaval versioonis 4.12.0.152)                                                                                                                     |
