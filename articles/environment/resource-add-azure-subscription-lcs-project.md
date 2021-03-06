---
title: Azure’i kordustellimuse lisamine LCS-projektile
description: See teema pakub teavet selle kohta, kuidas Azure'i tellimust LCS-i projektiga ühendada.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948831"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a>Azure’i kordustellimuse lisamine LCS-projektile

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Pilvepõhiseid keskkondi tuleb juurutada kasutades olemasolevat Azure'i korduvtellimust. See teema selgitab, kuidas olemasolevat Azure'i tellimust LCS-i projektiga ühendada. 

## <a name="grant-admin-consent"></a>Administraatori nõusoleku andmine

1. Valige LCS projekti jaotises **Keskkonnad** suvand **Microsoft Azure'i sätted**.

![Microsoft Azurei Seaded](./media/1MicrosoftAzureSettings.png)

2. Valige lehel **Projekti sätted** vahekaardil **Azure'i konnektorid** suvand **Autoriseeri**. See võimaldab sellele projektile keskkondade juurutamist.

![Azure'i konnektorid](./media/2AzureConnectors.png)

3. Administraatori nõusoleku andmiseks valige uuesti käsk **Autoriseeri**.

![Administraatori nõusoleku andmine](./media/3GrantAdminConsent.png)

4. Aktsepteerige õiguste taotlus.

![Aktsepteerige õiguste taotlus](./media/4AcceptPermissionRequest.png)

Autoriseerimine on nüüd lõpule viidud. 

![Autoriseerimine oli edukas](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Dynamicsi juurutamisteenustele oma Azure'i tellimuse juurdepääsu andmine

1. Avage [Microsoft Azure'i arveldus](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) ja valige oma kordustellimus. Dynamicsi juurutamisteenused vajavad keskkondade juurutamiseks juurdepääsu sellele tellimusele.

![Azure'i tellimuse üksikasjad](./media/6AzureSubscription.png)

2. Valige navigeerimispaanil **Juurdepääsukontroll** ja seejärel valige **Rollimäärangu lisamine**.
3. Valige paremas servas asuvas liuguris **Kaasautori roll** ja leidke ning valige antud loendis jaotis **Dynamicsi juurutamisteenused**. 
4. Valige **Salvesta**.

![Tellimuse juurdepääs](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>LCS-i projektile tellimuse konnektori lisamine

1. Valige oma LCS-i projektis lehel **Microsoft Azure'i sätted** uue konnektori lisamiseks käsk **Lisa**.
2. Sisestage oma Azure'i kordustellimuse ID. Oma Azure'i kordustellimuse ID leiate [Azure'i portaalis](https://ms.portal.azure.com/) ekraani alumisest vasakult nurgast jaotisest  **Sätted**.
3. Valige väljal **Konfigureeri Azure'i ressursihalduri kasutamiseks** suvand **Jah**.
4. Veenduge, et Azure'i kordustellimuse AAD rentniku domeen ühtib kasutatava Azure'i tellimust omava domeeniga ja valige **edasi**.
5. Valige kuval **Microsoft Azure'i seadistus** kinnitamiseks käsk **Edasi**. Kui kuvatakse sellel kuval tõrge, pöörduge tagasi selle teema jaotisse [Dynamicsi juurutamisteenustele Azure'i tellimuse juurdepääsu andmine](#provide) ja veenduge, et olete kõik sammud lõpule viinud.
6. Laadige Azure'i haldussertifikaat oma arvuti kohalikku kausta ja laadige see Azure'i haldusportaali üles, minnes jaotisse **Sätted** > **Haldussertifikaadid**. See sert võimaldab LCS-il teie eest Azure'iga suhelda. Kui teie kasutajal on tellimusele juurdepääs, võite selle etapi vahele jätta.
7. Valige **Edasi**.
8. Valige juurutamiseks Azure'i piirkond ja valige andmekeskus, mis on lähedal sellele, kus kavatsete seda süsteemi kasutada.
9.  Valige käsk **Ühenda**.

Olete Azure'i kordustellimuse edukalt ühendanud. Nüüd saate juurutada Dynamics 365 Finance'i pilvepõhiseid keskkondi.


