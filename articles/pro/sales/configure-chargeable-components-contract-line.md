---
title: Projektipõhise lepingurea arveldatavate komponentide konfigureerimine
description: See artikkel annab teavet selle kohta, kuidas lisada tasulisi komponente Project Operationsi lepinguridadesse.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e4118e8e56d45ef75f53d828e267a8a9c1c903a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922953"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Projektipõhise lepingurea arveldatavate komponentide konfigureerimine

_**Kehtib järgmistele:** lihtjuurutamine – tehing näidisarveldusele, Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks_

Projektipõhine lepingurida *sisaldas* komponente ja *arveldatavaid* komponente.

Kaasatud komponendid on komponendid, mis kuuluvad:

  - Arveldusmeetod ja kliendi jaotamine
  - Mitteületatavad limiidid 
  - Projektipõhise lepingurea määratletud arve sageduse sätted

Kaasatud komponentide alamhulka saab märkida arveldatavana, kasutades välja **Arveldamise tüüp**. Väli **Arveldamise tüüp** on seatud, mis võimaldab lepingurea kontekstis järgmisi väärtusi.

  - Arveldatav
  - Mittearveldatav

Arveldatavad komponendid saab määratleda tööülesannetes, rollides ja tehingute kategooriates.

Arveldatav tegevus määratletakse projekti lepingurea tööülesannetes ja seda rakendatakse kõigile real kaasatud tehingute klassidele. Kui lepingurea väli **Kaasa tööülesanded** on tühi või seatud väärtusele **Kogu projekt**, ei ole vahekaart **Arveldatavad tööülesanded** saadaval.

Projekti lepingurea rollidele määratud arveldatavuse kehtib ainult tehingu klassile **Aeg**. Kui lepingurea väli **Kaasa aeg** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad rollid** saadaval.

Projekti lepingurea tehingu kategooriate määratud arveldatavuse kehtib ainult tehingu klassile **Kulu**. Kui väli **Kaasa kulu** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad kategooriad** saadaval.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Projekti tööülesande värskendamine arveldatavaks või mittearveldatavaks

Projekti tööülesanne võib olla arveldatav või mittearveldatav kindla lepingurea kohta, mis võimaldab järgmist seadistust.

Kui projektipõhine lepingurida sisaldab väärtust **Aeg** ja teatud ülesannet, siis seostatakse väärtust **T1** sellega kui arveldatav. Kui olemas on teine lepingurida, mis sisaldab väärtust **Kulu**, saate seostada lepingurea väärtuse T1 tööülesannet sellega kui arveldatav. Tulemuseks on, et kogu tööülesande kohta registreeritud aeg on arveldatav ja kõik kulud on mittearveldatavad.

Ülesande arveldamise tüübi saab konfigureerida lepingurea vahekaardil **Arveldatavad ülesanded**, värskendades lepingurea ülesannete andmeruudustikus välja **Arveldamise tüüp**. Teise võimalusena saate värskendada välja **Arvelduse tüüp** ülesande arveldamise seadistuse andmeruudustikus projekti juures, mis näitab ülesandega seotud kontaktiridu.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Rolli värskendamine arveldatavaks või mittearveldatavaks

Roll võib olla arveldatav või mittearveldatav kindla lepingurea kohta.

Rolli arveldamise tüüpi saab konfigureerida lepingurea vahekaardil **Arveldatavad rollid**. Selleks värskendage andmeruudustikus **Arveldatavad rollid** välja **Arveldamise tüüp**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Tehingu kategooria värskendamine arveldatavaks või mittearveldatavaks

Tehingu kategooria võib olla arveldatav või mittearveldatav kindla lepingurea kohta.

Tehingu arveldamise tüüpi saab konfigureerida projektipõhise lepingurea vahekaardil **Arveldatavad kategooriad**. Selleks värskendage andmeruudustikus **Arveldatavad kategooriad** välja **Arveldamise tüüp**.

### <a name="resolve-chargeability"></a>Arveldatavuse lahendamine

Aja jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.

   - **Aeg** lisatakse lepingureale.
   - **Roll** on lepingureal konfigureeritud kui tasustatav.
   - **Kaasatud ülesanded** on lepingureal seatud valikule **Valitud ülesanded**.
 
 Kui need kolm asja on täidetud, konfigureeritakse ülesanne tasustavana. 

Kulu jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.

   - **Kulu** lisatakse lepingureale
   - **Tehingukategooria** on lepingureal konfigureeritud kui tasustatav
   - **Kaasatud ülesanded** on lepingureal seatud valikule **Valitud ülesanne**
  
 Kui need kolm asja on täidetud, konfigureeritakse **Ülesanne** tasustavana. 

Materjali jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.

   - **Materjalid** lisatakse lepingureale
   - **Kaasatud ülesanded** on lepingureal seatud valikule **Valitud ülesanded**

Kui need kaks asja on täidetud, konfigureeritakse **Ülesanne** tasustavana. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Kaasab aja</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Kaasab kulu</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Sisaldab materjale</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Kaasatud ülesanded</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Roll</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategooria</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Toiming</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Tasustatavuse mõju</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Kogu projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Arveldatav </p>
            </td>
            <td width="70" valign="top">
                <p>
Arveldatav </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei saa seadistada </p>
            </td>
            <td width="350" valign="top">
                <p>
Tegeliku aja arveldamine: <strong>arveldatav</strong>
                </p>
                <p>
Tegeliku kulu arveldamise tüüp: <strong>arveldatav</strong>
                </p>
                <p>
Tegeliku materjali arveldamise tüüp: <strong>arveldatav</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Ainult valitud ülesanded </p>
            </td>
            <td width="65" valign="top">
                <p>
Arveldatav </p>
            </td>
            <td width="70" valign="top">
                <p>
Arveldatav </p>
            </td>
            <td width="65" valign="top">
                <p>
Arveldatav </p>
            </td>
            <td width="350" valign="top">
                <p>
Tegeliku aja arveldamine: <strong>arveldatav</strong>
                </p>
                <p>
Tegeliku kulu arveldamise tüüp: <strong>arveldatav</strong>
                </p>
                <p>
Tegeliku materjali arveldamise tüüp: <strong>arveldatav</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Ainult valitud ülesanded </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Mittearveldatav</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Arveldatav </p>
            </td>
            <td width="65" valign="top">
                <p>
Arveldatav </p>
            </td>
            <td width="350" valign="top">
                <p>
Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </p>
                <p>
Tegeliku kulu arveldamise tüüp: Arveldatav </p>
                <p>
Tegeliku materjali arveldamise tüüp: arveldatav </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Ainult valitud ülesanded </p>
            </td>
            <td width="65" valign="top">
                <p>
Arveldatav </p>
            </td>
            <td width="70" valign="top">
                <p>
Arveldatav </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Mittearveldatav</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </p>
                <p>
Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </p>
                <p>
Tegeliku materjali arveldamise tüüp: <strong>mittearveldatav</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Ainult valitud ülesanded </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Mittearveldatav</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Arveldatav </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Mittearveldatav</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </p>
                <p>
Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </p>
                <p>
Tegeliku materjali arveldamise tüüp: <strong>mittearveldatav</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Ainult valitud ülesanded </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Mittearveldatav</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Mittearveldatav</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Arveldatav </p>
            </td>
            <td width="350" valign="top">
                <p>
Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </p>
                <p>
Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </p>
                <p>
Tegeliku materjali arveldamise tüüp: arveldatav </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Kogu projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei saa seadistada </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Arveldatav</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei saa seadistada </p>
            </td>
            <td width="350" valign="top">
                <p>
Tegeliku aja arveldamine: <strong>pole saadaval</strong>
                </p>
                <p>
Tegeliku kulu arveldamise tüüp: Arveldatav </p>
                <p>
Tegeliku materjali arveldamise tüüp: arveldatav </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Kogu projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei saa seadistada </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Mittearveldatav</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei saa seadistada </p>
            </td>
            <td width="350" valign="top">
                <p>
Tegeliku aja arveldamine: <strong>pole saadaval</strong>
                </p>
                <p>
Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </p>
                <p>
Tegeliku materjali arveldamise tüüp: arveldatav </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Kogu projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Arveldatav </p>
            </td>
            <td width="70" valign="top">
                <p>
Ei saa seadistada </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei saa seadistada </p>
            </td>
            <td width="350" valign="top">
                <p>
Tegeliku aja arveldamine: Arveldatav </p>
                <p>
Tegeliku kulu arveldamise tüüp: <strong>pole saadaval</strong>
                </p>
                <p>
Tegeliku materjali arveldamise tüüp: arveldatav </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Kogu projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Mittearveldatav</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Ei saa seadistada </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei saa seadistada </p>
            </td>
            <td width="350" valign="top">
                <p>
Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </p>
                <p>
Tegeliku kulu arveldamise tüüp: <strong>pole saadaval</strong>
                </p>
                <p>
Tegeliku materjali arveldamise tüüp: arveldatav </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Kogu projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Arveldatav </p>
            </td>
            <td width="70" valign="top">
                <p>
Arveldatav </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei saa seadistada </p>
            </td>
            <td width="350" valign="top">
                <p>
Tegeliku aja arveldamine: Arveldatav </p>
                <p>
Tegeliku kulu arveldamise tüüp: Arveldatav </p>
                <p>
Tegeliku materjali arveldamise tüüp: <strong>pole saadaval</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Kogu projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Mittearveldatav</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Mittearveldatav</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei saa seadistada </p>
            </td>
            <td width="350" valign="top">
                <p>
Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </p>
                <p>
Tegeliku kulu arveldamise tüüp:<strong> mittearveldatav</strong>
                </p>
                <p>
Tegeliku materjali arveldamise tüüp:<strong> pole saadaval</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
