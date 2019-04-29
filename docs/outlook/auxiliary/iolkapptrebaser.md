---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Prend en charge la relocalisation des rendez-vous dans un dossier de calendrier.
ms.openlocfilehash: cf4f7c790a8561f149160c83418a0d5ebd91a455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410069"
---
# <a name="iolkapptrebaser"></a><span data-ttu-id="9b716-103">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="9b716-103">IOlkApptRebaser</span></span>

<span data-ttu-id="9b716-104">Prend en charge la relocalisation des rendez-vous dans un dossier de calendrier.</span><span class="sxs-lookup"><span data-stu-id="9b716-104">Supports rebasing appointments in a calendar folder.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9b716-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="9b716-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b716-106">Hérite de:</span><span class="sxs-lookup"><span data-stu-id="9b716-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="9b716-107">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="9b716-107">**IUnknown**</span></span> <br/> |
|<span data-ttu-id="9b716-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9b716-108">Header file:</span></span>  <br/> |<span data-ttu-id="9b716-109">tzmovelib. h</span><span class="sxs-lookup"><span data-stu-id="9b716-109">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="9b716-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="9b716-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="9b716-111">tzmovelib. dll</span><span class="sxs-lookup"><span data-stu-id="9b716-111">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="9b716-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="9b716-112">Called by:</span></span>  <br/> |<span data-ttu-id="9b716-113">Applications clientes MAPI</span><span class="sxs-lookup"><span data-stu-id="9b716-113">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="9b716-114">Exposé sur:</span><span class="sxs-lookup"><span data-stu-id="9b716-114">Exposed on:</span></span>  <br/> |<span data-ttu-id="9b716-115">Objet de relocalisation Outlook</span><span class="sxs-lookup"><span data-stu-id="9b716-115">Outlook rebasing object</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9b716-116">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="9b716-116">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b716-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="9b716-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="9b716-118">Commence une tâche pour l'énumération de rendez-vous dans un dossier de calendrier pour rechercher les rendez-vous qui ont besoin de relocalisation.</span><span class="sxs-lookup"><span data-stu-id="9b716-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="9b716-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="9b716-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="9b716-120">Attend pour l'énumération de rendez-vous dans un dossier de calendrier pour terminer et renvoie une liste de rendez-vous à cette nécessité la relocalisation.</span><span class="sxs-lookup"><span data-stu-id="9b716-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="9b716-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="9b716-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="9b716-122">Commence une tâche pour la relocalisation des rendez-vous en fonction d'une liste de rendez-vous, généralement obtenue à partir de **EndEnumerateAppointments**.</span><span class="sxs-lookup"><span data-stu-id="9b716-122">Begins a task for appointment rebasing given a list of appointments, usually obtained from **EndEnumerateAppointments**.</span></span>  <br/> |
|<span data-ttu-id="9b716-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="9b716-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="9b716-124">Attend des rendez-vous pour terminer la relocalisation et récupère les résultats.</span><span class="sxs-lookup"><span data-stu-id="9b716-124">Waits for appointment rebasing to complete and retrieves the results.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b716-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b716-125">See also</span></span>

- [<span data-ttu-id="9b716-126">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="9b716-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

