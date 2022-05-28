---
title: Kuidas ma saan projekti etappide äriprotsessi vooge kohandada?
description: Ülevaade, kuidas projekti etappide äriprotsessi vooge kohandada.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7efbb19161878e13a1b0d33bc1bc4e06521445c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596965"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Kuidas ma saan projekti etappide äriprotsessi vooge kohandada?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Rakenduse Project Service varasemates versioonides on teadaolev piirang, et projekti etappide äriprotsessi voos peavad etappide nimed täpselt ühtima oodatud ingliskeelsete nimedega (**Quote**, **Plan**, **Close**). Vastasel korral ei tööta ingliskeelsetel etapinimedel tuginev äriloogika korrapäraselt. Seetõttu ei näe te projekti vormil tuttavaid toiminguid nagu **Vaheta protsessi** või **Redigeeri protsessi**. 

Selle piiranguga tegeleti versioonis 2.4.5.48 ja hilisemates. Selles artiklis pakutakse võimalikke lahendusi, kui teil on vaja kohandada varasemate versioonide äriprotsessi voo vaikevariante.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Äriloogika vajab ingliskeelsete etapinimedega täpselt ühtimist

Projekti etappide äriprotsessi voog sisaldab äriloogikat, mis juhib rakenduses järgmisi käitumisi.
- Kui projekt on seotud pakkumisega, siis määrab kood äriprotsessi voo etapile **Quote** (Pakkumine).
- Kui projekt on seotud lepinguga, siis määrab kood äriprotsessi voo etapile **Plan** (Plaan).
- Kui äriprotsessi voog liigutatakse etappi **Close** (Sulgemine), siis desaktiveeritakse projekti kirje. Kui projekt desaktiveeritakse, siis seatakse projekti vorm ja tööjaotuse struktuur (WBS) kirjutuskaitstud olekusse, väljastatakse nimega ressursi reserveeringud ning desaktiveeritakse kõik seostatud hinnakirjad.

See äriloogika tugineb ingliskeelsetel projekti etappide nimedel. Ingliskeelsetest etappide nimedest sõltumine on peamine põhjus, miks ei julgustata projekti etappide äriprotsessi voo kohandamist, ja miks te ei näe projekti üksuses tavapäraseid ärivoo toiminguid nagu **Vaheta protsessi** ega **Redigeeri protsessi**.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Mis juhtub, kui etapi nimed ei ühti ingliskeelsete nimedega?

Rakenduse Project Service versioon 1.x platvormil 8.2 – kui äriprotsessi voo etappide nimed ei ühti täpselt ingliskeelsete nimedega, siis äriloogika, mis määrab pakkumistele või lepingutele õige etapi või sulgeb need, jäetakse vahele. Tõrketeadet ei kuvata. Seetõttu näib, nagu saaksite kohandada projekti etappide äriprotsessi vooge. Kuid ükski automaatne protsess ei tööta pakkumiste, lepingute ega projektide sulgemiste jaoks.

Rakenduse Project Service versioonis 2.4.4.30 platvormil 9.0 muudeti äriprotsessi voogude arhitektuuri põhjalikult, mistõttu tuli ümber kirjutada äriprotsessi voo äriloogika. Selle tulemusena kuvatakse teile tõrketeade, kui protsessi etappide nimed ei ühti oodatud ingliskeelsete nimedega. 

Seega, kui soovite projekti üksuse jaoks kohandada projekti etappide äriprotsessi vooge, saate projekti üksuse äriprotsessi voo vaikevariandile lisada vaid täiesti uusi etappe, säilitades etappe **Quote** (Pakkumine), **Plan** (Plaan) ja **Close** (Sulgemine) oma esialgsetel kujudel. See piirang tagab, et teil ei esine tõrkeid äriloogikas, mis ootab äriprotsessi voost ingliskeelseid etappide nimesid.

Versioonis 2.4.5.48 või hilisemas on selles artiklis kirjeldatud äriloogika projekti üksuse äriprotsessi voo vaikevariandist eemaldatud. Sellele või uuemale versioonile täiendamine võimaldab teil äriprotsessi voo vaikevarianti kohandada või enda omaga asendada. 

## <a name="workarounds-for-earlier-versions"></a>Lahendused varasematele versioonidele

Kui täiendamine pole võimalik, saate projekti üksuse äriprotsessi voo projekti etappe kohandada kahel järgmisel viisil.

1. Lisage vaikekonfiguratsioonile lisaetappe, säilitades ingliskeelsed nimetused etappidele **Quote** (Pakkumine), **Plan** (Plaan) ja **Close** (Sulgemine).


![Kuvatõmmis vaikekonfiguratsioonile etappide lisamisest.](media/FAQ-Customize-BPF-1.png)
 
2. Looge oma äriprotsessi voog ja muutke see projekti üksuse jaoks peamiseks äriprotsessi vooks – see võimaldab teil etappide jaoks soovitud nimesid kasutada. Siiski, kui soovite kasutada samu standardseid projekti etappe **Quote** (Pakkumine), **Plan** (Plaan) ja **Close** (Sulgemine), siis peate tegema kohandusi, mis põhinevad teie kohandatud etappide nimedel. Keerukam loogika on projekti sulgemises, mille saate ikkagi käivitada, kui desaktiveerite projekti kirje.

![BPF-i kohandamine.](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Muud tähelepanekud rakenduse Project Service versiooni 2.4.4.30 või varasema kohta platvormil 9.0

Rakenduse Project Service versioonis 2.4.4.30 või varasemas platvormil 9.0 ei värskendata kohandatud äriprotsessi voo puhul projekti üksuse välja **Projekti nimi**, mida kasutatakse tabelis **Projektid etappide järgi** ja projekti loendi vaadetes, sest see väli on seotud projekti etappide äriprotsessi voo vaikevariandiga. Seda probleemi saate lahendada järgmiselt.

- Lisage kohandatud väli, et hõivata praegune äriprotsessi voo etapp, mida värskendatakse siis, kui kasutaja edeneb läbi kohandatud äriprotsessi voo.

- Muutke tabelit **Projektid etappide järgi**, et töötada vaikekonfiguratsiooni asemel oma kohandatud väljaga.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Juhised enda protsessi voo loomiseks projekti üksuse jaoks

Enda protsessi voo loomiseks projekti üksuse jaoks tehke järgmist.

1. Valige **Sätted** > **Protsessikeskus**. Ärge kopeerige projekti etappide äriprotsessi voogu, sest sellega koos kopeeritakse ka rakenduse Project Service äriloogika.

  ![Loo protsess.](media/FAQ-Customize-BPF-3.png)

2. Kasutage funktsiooni Process Designer (Protsessi kujundaja), et luua soovitud etappide nimesid. Kui soovite samu funktsioone nagu vaikeetappidel **Quote** (Pakkumine), **Plan** (Plaan) ja **Close** (Sulgemine), siis peate need looma teie kohandatud äriprotsessi voo etappide nimede põhjal.

   ![Kuvatõmmis funktsiooni Protsessikujundaja kasutamisest BPF-i kohandamiseks.](media/FAQ-Customize-BPF-4.png) 

3. Klõpsake funktsioonis Protsessi kujundaja nuppu **Protsessi voo järjestus**, et muuta kohandatud äriprotsessi voog projekti üksuse peamiseks äriprotsessi vooks, liigutades selleks seda projekti etappide äriprotsessi voo kohale loendi tippu.


   [Kuvatõmmis protsessi voo järjestuse kasutamisest](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Järgmised juhised kehtivad rakenduse Project Service versiooni 2.4.4.30 või varasema kohta platvormil 9.0

4. Lisage projekti üksusele uus kohandatud väli, et hõivata oma kohandatud äriprotsessi voo kohandatud etapid. Peate lisama äriloogika (lisandmooduli/töövoo), et värskendada seda välja siis, kui kohandatud äriprotsessi voo etappi värskendatakse.

   ![Kuvatõmmis projekti olemi kohandamisest.](media/FAQ-Customize-BPF-6-720.png)

5. Muutke tabelit **Projektid etappide järgi**, et kasutada oma uut kohandatud välja etappide jaoks.

   ![Kuvatõmmis tabeli Projektid etappide järgi kasutamisest.](media/FAQ-Customize-BPF-7-720.png)

6. Muutke projekti üksuse vaateid, et need hõlmaksid teie uut kohandatud välja kõikide etappide jaoks.

   ![Kuvatõmmis projekti olemi vaadete muutmisest.](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
