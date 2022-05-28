---
title: Projektipõhiste hinnapakkumiste kopeerimine
description: Selles teemas kirjeldatakse, kuidas kopeerida rakenduses Project Operations projektipõhiseid hinnapakkumisi.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1e8611f34a23d6d87317cc785148c1a3f9c26dca
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588041"
---
# <a name="copy-project-based-quotes"></a>Projektipõhiste hinnapakkumiste kopeerimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Saate hõlpsalt luua uue projekti hinnapakumise, kopeerides olemasoleva. 

- Projekti hinnapakkumise kopeerimiseks valige loendi lehel **Projekti hinnapakkumised** või üksikasjade lehel **Projekti hinnapakkumised** projekti hinnapakkumine, mida soovite kopeerida, ja valige seejärel **Kopeeri**.

See avab dialoogi lehe, kus saate sisestada koopia parameetrid. Järgmises tabelis on loetletud väljad, mis on kaasatud dialoogi lehele. Sõltuvalt teie valitud väärtustest võib koopia protsess muutuda.

| **Väli** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- |
| Teema | Sisestage siht-hinnapakkumise vastav teema või nimi. Kui dialoog avaneb, määrab süsteem selle lähtehinnapakkumise teemaks koos sellele lisatud suvandiga **-koopia**. | |
| Potentsiaalne klient | Viide kliendi ettevõttele või konto kirjele. Kui dialoog avaneb, määrab süsteem selle lähtehinnapakkumise kontole. | See väli on hinnapakkumise peamine klient. |
| Lepingut sõlmiv üksus | Organisatsiooniüksus, mis vastutab selle tehinguga seotud projekti(de) kättetoimetamise eest.
Kui dialoog avaneb, määrab süsteem selle lähtehinnapakkumise lepinguüksusele. | Lepinguüksus on ettevõtte allüksus, kes pärast tehingu sulgemist projektid teostab. Igal lepinguüksusel on valuuta. Valuutat kasutatakse prognoositavate ja tegelike projekti täitmise käigus tekkinud kulude aruandluseks. |
| Valuuta | See on valuuta, milles tehing edastatakse. Kui dialoog avaneb, määrab süsteem selle lähtehinnapakkumise valuutale. Seda saab muuta ja kui see on muutunud, siis välja **Kopeeri hinnakujundus** väärtus on alati **Ei**. Seda seetõttu, et lähtehinnapakkumise hinnakirjad pole enam asjakohased. | Valuutat kasutatakse hinnakirja vaikeväärtuseks, et koostada hinnapakkumise kohta finantskalkulatsioon ning lõpuks arveldada kliendiga, kui tehing on võidetud. |
| Soovitud tarnekuupäev | See on kliendi taotletud tarnekuupäev. | Seda kasutatakse konkreetse sagedusega arvelduse kuupäevadega koos lõpukuupäevana. |
| Hinnakujunduse kopeerimine | Väärtus Jah/ei näitab, kas hinnapakkumise hind tuleks lähtehinnapakkumisest kopeerida. | Kui valisite **Jah**, kopeeritakse projekti hinnakirja ja toodete hinnakirja viiteid lähtehinnapakkumisest siht-hinnapakkumisse. Kui valisite **Ei**, määratakse hinnakirjad uuesti vaikeväärtustele uusimate hinnakirjade põhjal, mis konto või projekti parameetrites häälestati. |

Kui valite dialoogi lehel **OK**, loob süsteem dialoogis valitud parameetrite põhjal projekti hinnapakkumise koopia. Avaneb uus projekti hinnapakkumine. 

> [!NOTE]
> Hinnapakkumise lähtekohast sihtkohta ei kopeerita järgmist teavet.
>
> - Arve ajakavad
> - Hinnapakkumise ja hinnapakkumise rea kliendid
> - Projekti viide projektile – põhinev hinnapakkumise ridadel – kliendi eelarve teave
>
>Kuna see teave on iga hinnapakkumise jaoks väga spetsiifiline, siis neid välju ja kirjeid ei kopeerita. Hinnapakkumise tasemel kopeeritakse projektide ja toodete hinnapakkumiste read, hinnapakkumise rea üksikasjade prognoosid ja mitte ületatavad väärtused. Hindade ja kulumäära vaikeväärtused sõltuvad valikust **Hinnakujunduse kopeerimine**, mis on valikud dialoogi lehel **Parameetrite kopeerimine**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]