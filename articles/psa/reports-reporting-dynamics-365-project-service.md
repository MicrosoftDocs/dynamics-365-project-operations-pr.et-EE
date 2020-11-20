---
title: Aruandluse avaleht
description: Selles teemas antakse teavet aruandluse kohta rakenduses Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e1a645b157c56066e56b22ea8cf0324fbc1ddd2c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120313"
---
# <a name="reporting-home-page"></a><span data-ttu-id="31015-103">Aruandluse avaleht</span><span class="sxs-lookup"><span data-stu-id="31015-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="31015-104">Microsoft Dynamics 365 Project Service Automation võimaldab projektipõhistel organisatsioonidel oma äritegevust tõhusalt hallata.</span><span class="sxs-lookup"><span data-stu-id="31015-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="31015-105">Iga projekti puhul peavad meeskonnaliikmed haldama müügivõimalusi, kavandama töid ja tegema neile hinnapakkumisi, leidma projektidele ressursse, haldama tööd vastavalt plaanile, esitama tehtud töö eest arveid ning seejärel tegema projekti lõpule viimiseks vajalikku tööd.</span><span class="sxs-lookup"><span data-stu-id="31015-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="31015-106">Võimalus tegevuste kohta aruandeid luua on organisatsiooni seisundi määramisel ja mis tahes parandusmeetmete kasutusele võtmisel otsustava tähtsusega.</span><span class="sxs-lookup"><span data-stu-id="31015-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="31015-107">PSA kasutab kogu oma aruandluse tegemiseks Microsoft Dynamics 365 aruandluse meetodeid ja tehnoloogiaid.</span><span class="sxs-lookup"><span data-stu-id="31015-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="31015-108">Aruandluse suvandite kohta leiate lisateavet teemast [Aruande kirjutamise juhend rakendusele Dynamics 365 Customer Engagement (on-premises), versioon 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="31015-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="31015-109">Aruandeviisard</span><span class="sxs-lookup"><span data-stu-id="31015-109">Report Wizard</span></span>

<span data-ttu-id="31015-110">Aruandeviisard võimaldab mittearendajast kasutajatel lihtsaid aruandeid luua.</span><span class="sxs-lookup"><span data-stu-id="31015-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="31015-111">Kuna rakendus koostatakse olemasoleval platvormil, on kogemus samasugune kui see, mis on dokumenteeritud teemas [Aruande loomine või redigeerimine aruandeviisardi abil](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="31015-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="31015-112">Kuid te kasutate siiski rakendusele Project Service Automation omaseid olemeid.</span><span class="sxs-lookup"><span data-stu-id="31015-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="31015-113">Kohandatud SQL Serveri aruandlusteenuste aruanded</span><span class="sxs-lookup"><span data-stu-id="31015-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="31015-114">Kui teie ettevõte vajab kindlat aruannet, mida ei saa aruandeviisardiga luua, saate luua kohandatud aruande.</span><span class="sxs-lookup"><span data-stu-id="31015-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="31015-115">Teil peab olema installitud Microsoft Visual Studio ja vastavad Microsoft SQL Server Data Tools ning aruannete koostamise laiendused.</span><span class="sxs-lookup"><span data-stu-id="31015-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="31015-116">Lisateavet tööriistade ja versioonide kohta leiate teemast [Aruande koostamise keskkond, kasutades tööriista SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="31015-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="31015-117">Lisateavet kohandatud aruande koostamise kohta leiate teemast [Looge uus aruanne tööriistaga SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="31015-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="31015-118">Power BI ülevaadete rakendused</span><span class="sxs-lookup"><span data-stu-id="31015-118">Power BI insights apps</span></span>

<span data-ttu-id="31015-119">Ühiselt annavad Microsoft Power BI ja Dynamics 365 ülevaadete rakenduste kujul teile oma andmetega töötamiseks võimsa võimaluse.</span><span class="sxs-lookup"><span data-stu-id="31015-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="31015-120">Lisateavet ülevaadete rakenduste kättesaadavuse kohta leiate lehelt [Power BI ülevaadete rakendused](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="31015-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="31015-121">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="31015-121">Additional resources</span></span>
<span data-ttu-id="31015-122">Lisateavet aruandluse kohta rakenduses PSA leiate järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="31015-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="31015-123">Project Service’i andmemudeliga töötamine</span><span class="sxs-lookup"><span data-stu-id="31015-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="31015-124">Armatuurlauad</span><span class="sxs-lookup"><span data-stu-id="31015-124">Dashboards</span></span>](reports-dashboards.md)

