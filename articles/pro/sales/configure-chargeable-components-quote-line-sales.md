---
title: Hinnapakkumise rea arveldatavate komponentide konfigureerimine
description: Selles artiklis antakse teavet tasuliste ja mittetasustatavate komponentide seadistamise kohta projektipõhisel hinnapakkumisreal.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d4829055f429546c7911a05a765bc28ae085afa1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930037"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Hinnapakkumise rea arveldatavate komponentide konfigureerimine 

_**Kehtib järgmistele:** lihtjuurutamine – tehing näidisarveldusele, Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks_

Projektipõhine hinnapakkumise rida sisaldab *kaasatud* komponente ja *arveldatavaid* komponente.

Kaasatud komponente võidakse:

  - Arveldusmeetod ja kliendi jaotamine
  - Mitteületatavad limiidid 
  - Projektipõhise hinnapakkumise rea määratletud arve sageduse sätted

Kaasatud komponentide alamhulka saab märkida arveldatavana, kasutades välja **Arveldamise tüüp**. Väli **Arveldamise tüüp** on seatud, mis võimaldab hinnapakkumise rea kontekstis järgmisi väärtusi.

  - Arveldatav
  - Mittearveldatav

Arveldatavad komponendid saab määratleda tööülesannetes, rollides ja tehingute kategooriates.

Arveldatav tegevus määratletakse hinnapakkumise rea tööülesannetes ja seda rakendatakse kõigile real kaasatud tehingute klassidele. Kui väli **Kaasa tööülesanded** on seatud väärtusele **Kogu projekt** või see on tühjaks jäetud, ei ole vahekaart **Arveldatavad tööülesanded** saadaval.

Hinnapakkumise rea rollidele on määratud arveldatavus ja see kehtib ainult tehingu klassile **Aeg**. Kui projekti hinnapakkumise rea väli **Kaasa aeg** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad rollid** saadaval.

Hinnapakkumise rea tehingu kategooriatele on määratud arveldatavus ja see kehtib ainult tehingu klassile **Kulu**. Kui projekti hinnapakkumise rea väli **Kaasa kulud** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad kategooriad** saadaval.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Projekti tööülesande värskendamine arveldatavaks või mittearveldatavaks

Projekti tööülesanne võib olla arveldatav või mittearveldatav kindla projektipõhise hinnapakkumise rea kohta, mis võimaldab järgmist seadistust.

Kui projektipõhise hinnapakkumise rida sisaldab väärtust **Aeg** ja tööülesannet **T1**, seostatakse tööülesanne hinnapakkumise reaga kui arveldatav. Kui olemas on teine hinnapakkumise rida, mis sisaldab väärtust **Kulud**, saate seostada hinnapakkumise rea tööülesannet **T1** sellega kui arveldatav. Tulemuseks on, et kogu tööülesande kohta registreeritud aeg on arveldatav ja kõik kulud on mittearveldatavad.

Ülesande arveldamise tüübi saab konfigureerida projektipõhise hinnapakkumise rea vahekaardil **Arveldatavad ülesanded**, värskendades välja **Arveldamise tüüp** andmeruudustikus **Hinnapakkumise rea ülesanded**. Teise võimalusena saate värskendada projekti ülesande arveldamise tüüpi väljal **Arvelduse tüüp** ülesande arveldamise seadistuse andmeruudustikus projekti juures, mis näitab ülesandega seotud hinnapakkumise ridu.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Rolli värskendamine arveldatavaks või mittearveldatavaks

Roll võib konkreetse projektipõhise hinnapakkumise rea puhul olla arveldatav või mittearveldatav.

Rolli arveldamise tüübi saab konfigureerida hinnapakkumise rea vahekaardil **Arveldatavad rollid**, värskendades välja **Arveldamise tüüp** andmeruudustikus **Arveldatavad rollid**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Tehingu kategooria värskendamine arveldatavaks või mittearveldatavaks

Tehingu kategooria võib olla arveldatav või mittearveldatav kindla hinnapakkumise rea kohta.

Tehingu arveldamise tüübi saab konfigureerida hinnapakkumise rea vahekaardil **Arveldatavad kategooriad**, värskendades välja **Arveldamise tüüp** andmeruudustikus **Arveldatavad kategooriad**.

### <a name="resolve-chargeability"></a>Arveldatavuse lahendamine
Aja jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.

   - **Aeg** lisatakse hinnapakkumise reale.
   - **Roll** on hinnapakkumise real konfigureeritud kui tasustatav.
   - **Kaasatud ülesanded** on hinnapakkumise real seatud valikule **Valitud ülesanded**. 

Kui need kolm asja on täidetud, konfigureeritakse **Ülesanne** samuti tasustavana. 

Kulu jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul. 

   - **Kulu** lisatakse hinnapakkumise reale.
   - **Tehingukategooria** on hinnapakkumise real konfigureeritud kui tasustatav.
   - **Kaasatud ülesanded** on hinnapakkumise real seatud valikule **Valitud ülesanded**.

Kui need kolm asja on täidetud, konfigureeritakse **Ülesanne** samuti tasustavana. 

Materjali jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.

   - **Materjalid** lisatakse hinnapakkumise reale.
   - **Kaasatud ülesanded** on hinnapakkumise real seatud valikule **Valitud ülesanded**.

Kui need kas asja on täidetud, peaks **Ülesanne** olema samuti konfigureeritud tasustavana. 


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
Ei saa määrata </p>
            </td>
            <td width="350" valign="top">
                <p>
Tegeliku aja arveldamine: Arveldatav </p>
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
Arveldatav </p>
            </td>
            <td width="350" valign="top">
                <p>
Tegeliku aja arveldamine: Arveldatav </p>
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
Ei saa määrata </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Arveldatav</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei saa määrata </p>
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
Ei saa määrata </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Mittearveldatav</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei saa määrata </p>
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
Ei saa määrata </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei saa määrata </p>
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
Ei saa määrata </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei saa määrata </p>
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
Ei saa määrata </p>
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
Ei saa määrata </p>
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
