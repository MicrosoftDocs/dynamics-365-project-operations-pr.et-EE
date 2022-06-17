---
title: Kuluhalduse konfigureerimine
description: Selles artiklis kirjeldatakse kaalutlusi ja otsuseid, mida peate tegema plaanimisprotsessi ajal enne kuluhalduse konfigureerimist rakenduses Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c9424b8aaf867254bde085cffaa649c846920cc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933993"
---
# <a name="configure-expense-management"></a>Kuluhalduse konfigureerimine

Selles artiklis kirjeldatakse kaalutlusi ja otsuseid, mida peate enne kuluhalduse konfigureerimist plaanimisprotsessi käigus tegema. Kuluhalduses saate talletada teavet makseviiside, reisitellimuste, kuluaruannete, poliitikate jms kohta.

Kuna kuluhalduse konfiguratsiooni plaanimisel tehtud otsused põhinevad teie organisatsiooni hierarhial ja finantsstruktuuril, peate viitama nende alade jaoks plaanitavatele dokumentidele.

## <a name="intercompany-expenses"></a>Kontsernisisesed kulud

Kui lubate kontsernisisesed kulud, lubate juriidilistel olemitel ja töötajatel muude juriidiliste olemite nimel kulusid kanda ning kogute makse oma ettevõtte juriidiliste olemite töötajatelt. Näiteks juriidilise olemi A töötaja lõpetab projekti juriidilise olemi B jaoks ja projekt kannab reisiga seotud kulud. Kui kontsernisisesed kulud on lubatud, saab töötaja seejärel esitada kuluaruande, mis sisestab kulu juriidilisele olemile B ning kulu tuleb seejärel tasuda juriidilise olemi A poolt. Kui teie ettevõttel pole mitut juriidilist olemit, ei pea te kontsernisiseseid kulusid lubama.

**Otsus:** kas soovite lubada kontsernisisesed kulud?

## <a name="financial-management"></a>Finantshaldus

Kuluhaldus on tihedalt seotud teie organisatsiooni finantsjuhtimisega. Palju teie kuluhalduse konfiguratsioonist võetakse aluseks teie organisatsiooni finantsasjade kohta tehtud otsustele. Järgmistes jaotistes kirjeldatakse, millistes valdkondades on vaja plaanimist ja otsuseid, lähtudes teie organisatsiooni finantsotsustest ja juhtiva meeskonna juhistest.

### <a name="per-diems"></a>Päevarahad

Peate määratlema töötaja päevarahad, mida teie organisatsioon pakub. Kuna päevarahad on tavaliselt kasutusel kulude katmiseks, nagu toitlustus, majutus ja muud ettenägematud kulud, saate luua reeglid teie organisatsiooni pakutavate päevarahade kohta. päevarahade määrad võivad põhineda aastaajal, reisisihtkohal või mõlemal. Päevaraha reegli määratlemisel saate määrata, et teatud protsent päevarahade hinnast jäetakse maksmata, kui töötaja saab tasuta einet või teenust. Samuti saate määratleda päevarahade määra tasemed, et määrata minimaalse ja maksimaalse tundide arvu, mille võrra päevaraha töötaja reisile rakendada saab.

**Otsus:**

- Päevarahade vaikereeglid esimese ja viimase päeva kohta.

    - Milline on minimaalne tundide arv, mida töötaja saab päeva eest taotleda, et päevaraha saada?
    - Kas summa, mida pakutakse esimese ja viimase päeva toitlustuse eest, on väiksem? Kui summa on väiksem, siis milline on vähendamise protsent?
    - Kas summa, mida pakutakse esimese ja viimase päeva majutuse eest, on väiksem? Kui summa on väiksem, siis milline on vähendamise protsent?
    - Kas summa, mida pakutakse esimese ja viimase päeva muude kulude eest, on väiksem? Kui summa on väiksem, siis milline on vähendamise protsent?

- Päevaraha vaikereeglid.

    - Kas päevaraha summa väheneb iga toidukorra eest, kui eine on näiteks tasuta? Kui summa on väiksem, siis milline on vähendamise protsent iga eine eest?
    - Kas toidukorra summa vähenemine arvutatakse päeva, reisi või päeva toidukordade kohta?
    - Kas päevarahade summa ümardatakse tavalisel viisil või ülespoole?
    - Kas päevaraha arvutatakse 24-tunnise ajavahemiku või kalendripäeva kohta?

- Päevaraha reeglid, mis põhinevad asukohal.

    - Kas päevarahade määrad erinevad olenevalt asukohast? Millised asukohad on kaasatud?
    - Kui päevaraha määrad erinevad olenevalt asukohast, siis milline protsent on iga asukoha kohta ette nähtud järgmist tüüpi kulutuste jaoks.

        - Toidukorrad
        - Hotell
        - Muud kulud

### <a name="expense-management-journals-and-accounts"></a>Kuluhalduse töölehed ja kontod

Kuluhaldus eeldab mitme töölehe ja konto kasutamist. Peate otsustama näiteks, kas sama kontot kasutatakse sularaha ettemaksete ja krediitkaardiga seotud vaidluste korral.

**Otsus:**

- Millisele pearaamatu töölehele on kinnitatud kuluaruanded sisestatakse?
- Millist kontot kasutatakse sularaha ettemakseteks?
- Kas sularaha ettemaksed tuleb kohe sisestada?

### <a name="payment-methods"></a>Makseviisid

Kui lubate töötajatel kanda kulusid teie ettevõtte nimel, peate määratlema makseviisid, mida töötajad võivad kasutada. Näiteks võite lubada töötajatel kasutada sularaha või ettevõtte krediitkaarti. Samuti võite lubada töötajatel kasutada isiklikke krediitkaarte ja seejärel töötajatele summa tagasi maksma. Peate tegema järgmised otsused iga makseviisi kohta, mida lubate.

**Otsus:**

- Millised makseviisid on lubatud?
- Kes katab makseviisi kulud?
- Kas olemas on tasaarvelduskonto tüüp? Kui teil on tasaarvelduskonto tüüp, siis mis see on?
- Kui teil on tasaarvelduskonto, siis mis konto see on?
- Kui makseviis on krediitkaart, kas makseviisi saab kasutada ainult koos imporditud tehingutega?

### <a name="expense-categories-and-shared-categories"></a>Kulukategooriad ja jagatud kategooriad

Kui töötajad loovad kuluaruande, peavad kõik kirjendatud kulud olema seostatud kulukategooriaga. Kulukategooriate tuletatakse ühiskasutatavatest kategooriatest, mida saab teie organisatsiooni juriidiliste isikutega ühiselt kasutada. Neid kategooriaid saab jagada ka projektihalduses ja raamatupidamises, olenevalt sellest, kuidas teie organisatsioon on määratletud. Vastavalt teie organisatsiooni määratlusele ja juurutuse meeskonna juhistele peate määratlema, kas kuluhalduses kasutatavaid kategooriaid kasutatakse ainult kuluhalduses või kas need tuleks anda ühiskasutusse projektihalduse ja raamatupidamise ja kuluhaldusega. Page tähele, et neid kategooriaid saab kasutada ühiselt projekti ja kulude või projekti ja tootmise vahel, kuid mitte kulude ja tootmise vahel. Peate iga kulukategooria kohta järgmised otsused tegema.

**Otsus:**

- Mis on kulukategooria? Näidete hulka kuuluvad lendude, hotelli või kilometraaži kategooria.
- Kas kulukategooriat võib kasutada ka projektijuhtimises ja raamatupidamises?
- Mis on kulutüüp?
- Milline on kulukategooria jaoks vaikimisi kasutatav makseviis?
- Kas kulukategooria kulud tuleb täpsustada?
- Milline on kulukategooria jaoks peamine vaikekonto?
- Milline on kulukategooria üksuse vaikimisi käibemaksurühm?
- Kas kulukategooria jaoks on lubatud täiendavad makseviisid? Kui lubatud on täiendavad makseviisid, siis millised need on?
- Kas selles kulukategoorias pm alamkategooriaid? Kui on alamkategooriaid, peate langetama ka järgmised otsused.

    - Kas mõni alamkategooria on maksutagastusest välja jäetud?
    - Mis on alamkategooria üksuse käibemaksugrupp?

Kui kulukategooria on kasutusel ka projektihalduses ja raamatupidamises, vastake ülejäänud küsimustele. Muul juhul liikuge edasi järgmise jaotise juurde.

- Milliseid kulukontosid kasutatakse järgmistel kulude korral?

    - Kulu
    - Palgaarvestuse jaotus
    - WIP-kulu väärtus
    - Kulu-üksus
    - WIP-kulu väärtuse-üksus
    - Tekkepõhine kahjum
    - WIP-tekkepõhine kahjum

- Milliseid tulukontosid kasutatakse järgmise korral?

    - Arveldatud tulu
    - Viittulu-müügiväärtus
    - WIP-müügiväärtus
    - Viittulu-tootmine
    - WIP-tootmine
    - Viittulu-kasum
    - WIP-kasum
    - Viittulu-kordustellimus
    - WIP-kordustellimus

### <a name="taxes"></a>Maksud

Kuluga seotud maksude puhul peate määratlema, mis on kuluaruannetes kaasatud või lubatud.

**Otsus:**

- Kas kulu summa sisaldab käibemaksu?
- Kas maksutagastus peaks olema kulude korral lubatud?

    > [!NOTE]
    > Kui plaanisite pearaamatut ning otsustasite rakendada USA käibemaksu ja kasutada käibemaksu reegleid, ei saa te kulude osas maksude tagasinõudmist lubada. (USA käibemaksu ja maksude reeglite kasutamise rakendamiseks seadke suvandi **Rakenda käibemaksu maksustamise reegleid** väärtuseks **Jah**.)

## <a name="policies"></a>Poliitikad

Kui loote kuluaruande poliitikad, saate aidata oma organisatsioonil aega ja raha säästa, kui töötajad selle nimel kulusid kannavad. Poliitikad aitavad tagada, et töötajad jäävad eelarvesse, esitavad kogu nõutava teabe ja kulutavad raha ainult otstarbeliselt. Peate iga teie loodud kuluaruande poliitika ja iga kuluaruande kinnitamise poliitika kohta järgmised otsused tegema.

**Otsus:**

- Mis on poliitika nimi?
- Mille jaoks kulude poliitika on?
- Kui olete varem otsustanud lubada kontsernisisesed kulud, siis millistele teie organisatsiooni ettevõtetele see poliitika rakendub?
- Millal poliitika jõustub?
- Millal poliitika aegub?
- Mis on poliitika reegel?
- Mis on poliitika reegli tulemus?


[!INCLUDE[footer-include](../includes/footer-banner.md)]