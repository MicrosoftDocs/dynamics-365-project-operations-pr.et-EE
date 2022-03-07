---
title: Tootepõhised hinnapakkumise read
description: Selles teemas antakse teavet tootel põhinevate hinnapakkumiste ridade kohta.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
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
ms.openlocfilehash: 8bde88f5f2d00c09129c6a9363c09f6f6ad1dd90
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284083"
---
# <a name="product-based-quote-lines"></a>Tootepõhised hinnapakkumise read

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Saate luua tootel põhinevaid hinnapakkumise ridu rakenduses Dynamics 365 Project Service Automation. Tootepõhiste hinnapakkumiste ridu saab sisestada ridadel või need võivad olla tootekataloogi objektid.

## <a name="product-catalog"></a>Tootekataloog

Dynamics 365 tootekataloogi toodetel on vaikimisi ühik ja ühikurühm. Kui mitmes tootes on sama atribuutide kogum, saate luua ka tootepere, millel on ka need atribuudid. Kõik ühe tootepere tooted pärivad sama hulga atribuute.

Näiteks ettevõte müüb kordustellimuse litsentse mitmesuguste tarkvarade jaoks. Kõikidel kordustellimuse tarkvaradel on järgmised kaks atribuuti.

- Aktiivsete kasutajate arv 
- Kordustellimuse kestus (kuudes)

Seda tüüpi kataloogi säilitamiseks on hea viis luua tootepere, mille nimi on **Kordustellimuse tarkvara** ja millel on atribuudid **Kasutajate arv** ja **Kordustellimuse kestus**. Seejärel saate lisada üksikuid tooteid, näiteks **Dynamics 365 Sales** või **Dynamics 365 Field Service**, tooteperele **Kordustellimuse tarkvara**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Tootekataloogi üksuste lisamine projekti hinnapakkumisesse

Projekti hinnapakkumise ja projekti lepingu lehtedel on jaotised kahte tüüpi ridade jaoks: projektil põhinevad read ja tootepõhised read. Tootepõhiste ridade puhul kasutatakse rakendust Dynamics 365, et lisada tooteid tootekataloogi hinnapakkumisse. Müügipakkumise rea või projekti lepingurea ripploendis on kõik tooted ja ühikud, mis on seotud hinnapakkumise või projekti lepinguga. Saate lisada ka tooteid, mis ei kuulu hinnapakkumise toodete hinnakirja.

Lisaks saate valida tooted teistest hinnakirjadest või valida tooteid otse tootekataloogi kaudu. Kui valite tooted otse tootekataloogi kaudu, kasutatakse toote müügihinna saamiseks selle toote vaikimisi kasutatavat hinnakirja. Kui vaike-hinnakirja ei määrata, määratakse hinnaks 0 (null).

Kui hinnapakkumise rida põhineb tootekataloogil, saate müügihinna alistada otse hinnapakkumise real. Võtke arvesse, et Dynamics 365 on hinnapakkumise real on väli **Hinnakiri**. Saadaval on kaks väärtust.

- Hinnakirja tühistamine  
- Kasuta vaikeväärtust

Kui määrate selle välja väärtuseks **Hinnakirja tühistamine**, ei sea Dynamics 365 vaikimisi hinda. Toote hinna peate sisestama hinnapakkumise real. Kui määrate selle välja väärtuseks **Kasuta vaikesätet**, kasutab Dynamics 365 vaikimisi müügihinda ja lukustab välja, et seda ei saaks redigeerida.

Pärast seda, kui olete installinud PSA, sisestatakse vaikimisi müügihinnad hinnapakkumise tootepõhistele ridadele. Välja **Hinnakiri** väärtuseks seatakse **Hinnakirja tühistamine**, et saaksite hinnapakkumise ridadel redigeerida vaikimisi kasutatavat hinda.

> ![Hinnakirja tühistamise määramine](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Toodete koguselised tegurid

PSA kasutab kordustellimuse põhiste toodete müügi toetamiseks koguselisi tegureid. Kordustellimusel põhinevate toodete puhul väljendatakse hinnapakkumise või projekti lepingurea kogust kasutaja kuude arvuna.

Tavaliselt talletatakse kordustellimuse tarkvara hinda kataloogis ühe kasutaja kuu hinnana. Kuid selle asemel võite kasutada ka muid aja kirjeldusi. Müügiprotsessi jooksul on hind hinnapakkumise real tavaliselt ühe kasutaja hind kuus, mille IT müügiagent oli kokku leppinud ja diskonteerinud. Igal lepingul on erinev arv kasutajaid ja kordustellimuse kuude arv on erinev. Kogus, mida kasutatakse hinnapakkumise rea summa arvutamiseks, on kasutajate arvu ja kordustellimuse kuude arvu toode.

Seda tüüpi müügi toetamiseks võttis PSA kasutusele koguselised tegurid. Koguselised tegurid sõltuvad toote atribuutidest rakenduses Dynamics 365. Toote teatud atribuutide konfigureerimisel võimaldab PSA teil tähistada nende atribuutide alamhulka või kõiki atribuute, näiteks koguselised tegurid.

PSA kinnitab, et ainult arvandmed või toote atribuudid, millel on arvuline andmetüüp, märgistatakse koguse tegurina. Kui toode, mille jaoks on konfigureeritud koguselised tegurid, lisatakse hinnapakkumise reale, muutub  hinnapakkumise rea väli **Hinnapakkumine** kirjutuskaitstuks. Pärast koguseid sisaldavatele toote atribuutidele väärtuste sisestamist arvutab PSA hinnapakkumise rea koguse.

Näiteks Dynamics 365 võib sisaldada järgmisi atribuute. 

- **Kasutajate arv** – kasutajate arv 
- **Kuude arv** – kordustellimuse kuude arv
- **Toote SKU** 

Atribuute **Kasutajate arv** ja **Kuude arv** saab märgistada koguse tegurina, redigeerides tootesarja atribuute. 

> ![Kasutajate arvu ja kuude arvu märgistamine kvaliteeditegurina](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]