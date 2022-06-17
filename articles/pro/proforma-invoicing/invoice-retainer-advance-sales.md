---
title: Honorari või ettemaksu arve
description: Selles artiklis antakse teavet selle kohta, kuidas esitada arve hoidjale või ettemaksule Project Operationsis.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 044186d5c7759866dec3883103acec19cb571c11
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914489"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Honorari või ettemaksu arve

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations toetab honoraril põhinevaid lepinguid ja ühekordseid ettemakseid. Projekti lepingu korral saate salvestada honoraride või ühekordse ettemakse ajakava. Kuid projekti lepingu tasemel salvestamine ei tee muuda honorari ega ettemaksu kohe kasutamiseks saadaolevaks. Honorari või ettemakse kasutamiseks arvel, mille kliendile tegelikult esitate, tuleb kõigepealt arveldada honorar või ettemakse.

Honorari või ettemakse arveldamiseks täitke järgmised juhised.

1. Valige **Müük** > **Arveldamine** > **Honorarid ja ettemaksed**. 
2. Kasutage lehel **Ettemaksed ja honorarid** filtrit, et valida arve jaoks konkreetne honorar või ettemakse ja märkige selle olekuks **Arveldamiseks valmis**.
3. Looge arve kas käsitsi loendist **Projekti leping** või üksikasjade lehelt. Honorar või ettemakse kuvatakse arve mustandi lehel **Arve** jaotises **Ettemaksed ja honorarid**.
4. Kinnitage arve. See muudab honorari või ettemaksu kasutamiseks saadaolevaks. Arve saate kinnitada loendilehel **Honorarid ja ettemaksed**. Arveldatud ettemakse või honorari puhul kuvatakse saadaolev summa ruudustikus.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Looge arve ruudustikus honorar või ettemakse.

Saate luua honorari või ettemakse otse arvel.

1. Uue honorari või ettemaksu loomiseks valige arve mustandi andmeruudustikus **Ettemaksed ja honorarid** suvand **Uus**. 
2. Lisage lehel **Kiirloomine** vajalik teave ja seejärel valige suvand **Salvesta**. Arvega seotud projekti lepingus luuakse honorar või ettemaks. Honorari ja ettemakse väärtuseks määratakse automaatselt **Arveldamiseks valmis** ja seejärel lisatakse see lehel **Arve** andmeruudustikku **Ettemaksed ja honorarid**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Arveldatud honorari või ettemaksu vastavusse viimine

Pärast seda, kui honorar või ettemakse on arveldatud, saab neid kasutada või vastavusse viia arvega, mil on aeg, kulud, vahe-eesmärgid või muud projektil põhinevad tasud. Kliendile kuvatakse arve summa, mis on vähendatud selles arves kasutatud honorari või ettemaksu summa võrra.

Iga arve jaoks, mis luuakse projekti lepingu kohta, mille jaoks on honorare või ettemakseid arveldatud, rakendab Project Operation arvele automaatselt honorari või ettemakse.

Seda saab näha lehe **Arve** ruudustikus **Rakendatud honorarid ja ettemaksed**. Järgmine tabel annab teavet väljade kohta, mis on lehe **Projekti arve** ruudustikus **Rakendatud honorarid ja ettemaksed**.

| Väli | Asukoht | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- | --- |
| Kirjeldus | Lehe **Projekti arve** ruudustik **Rakendatud honorarid ja ettemaksed** |See kirjutuskaitstud väli kirjeldab selles arves kasutatud honorari või ettemakset. Seda väärtust ei saa arvel muuta. Seda väärtust saab muuta lehe **Projekti leping** andmeruudustikus. | Seda välja saab kliendile kuvada prinditud arvel, et näidata, milline honorar või ettemakse on arvele rakendatud. |
| Tarnekuupäev | Lehe **Projekti arve** ruudustik **Rakendatud honorarid ja ettemaksed**  | See kirjutuskaitstud väli esitab selles arves kasutatud honorari või ettemakse arve kuupäeva. Seda väärtust ei saa arvel muuta. Seda väärtust saab muuta lehe **Projekti leping** andmeruudustikus. | Seda välja saab kliendile kuvada prinditud arvel, et näidata kuupäeva, millal honorari või ettemakse arve kliendile esimest korda esitati. |
| Summa | Lehe **Projekti arve** ruudustik **Rakendatud honorarid ja ettemaksed**  | See kirjutuskaitstud väli esitab selles arves kasutatud honorari või ettemakse summa. Seda väärtust ei saa arvel muuta. Seda väärtust saab muuta lehe **Projekti leping** andmeruudustikus. | Seda välja saab kliendile kuvada prinditud arvel, et näidata honorari või ettemakse algset summat, mille klient tasus. |
| Kasutatud summa | Lehe **Projekti arve** ruudustik **Rakendatud honorarid ja ettemaksed**  | See kirjutuskaitstud väli esitab arvutatud väärtuse, mis võtab kokku, kui palju on honorari või ettemakset kasutatud. | Seda välja saab kliendile kuvada prinditud arvel, et näidata honorari või ettemakse summat, mis on juba kasutatud. |
| Rea summa | Lehe **Projekti arve** ruudustik **Rakendatud honorarid ja ettemaksed**  | See redigeeritav väli esitab selles projekti arves kasutatud honorari või ettemakse summa. See summa ei saa olla suurem kui summa, mis on saadaval ettemaksena. Süsteem arvutab automaatselt ruudustiku väljade **Summa** ja **Kasutatud summa** vahe. Saate seda summat vähendada, et kasutada väiksemat summat kui on saadaval, kuid te ei saa suurendada summat, et kasutada rohkem kui on saadaval. | Seda välja saab kliendile kuvada prinditud arvel, et näidata honorari või ettemakse summat, mida arvel kasutatakse. |
| Honorari saldo summa. | Lehe **Projekti arve** ruudustik **Rakendatud honorarid ja ettemaksed**  | See kirjutuskaitstud väli esitab väärtuse, kui palju honorarist või ettemaksest pärast arve kinnitamist alles on. | Seda välja saab kliendile kuvada prinditud arvel, et näidata honorari või ettemakse summat, mis pärast arve kinnitamist ja maksmist alles jääb. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]