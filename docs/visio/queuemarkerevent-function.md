---
title: QUEUEMARKEREVENT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60107
localization_priority: Normal
ms.assetid: b4671715-4209-7774-c174-c19dc9721a02
description: Entraîne le déclenchement d’un événement marqueur vers votre module complémentaire, Microsoft Visual Basic pour Applications (VBA) code, ou un complément COM.
ms.openlocfilehash: b9175caf0845530c93f6db15e286f3eae21ea415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789380"
---
# <a name="queuemarkerevent-function"></a><span data-ttu-id="789d3-103">QUEUEMARKEREVENT, fonction</span><span class="sxs-lookup"><span data-stu-id="789d3-103">QUEUEMARKEREVENT Function</span></span>

<span data-ttu-id="789d3-104">Entraîne le déclenchement d’un événement marqueur vers votre module complémentaire, Microsoft Visual Basic pour Applications (VBA) code, ou un complément COM.</span><span class="sxs-lookup"><span data-stu-id="789d3-104">Causes the application to fire a marker event to your add-on, Microsoft Visual Basic for Applications (VBA) code, or COM add-in.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="789d3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="789d3-105">Syntax</span></span>

<span data-ttu-id="789d3-106">QUEUEMARKEREVENT (** *chaîne_événement* **)</span><span class="sxs-lookup"><span data-stu-id="789d3-106">QUEUEMARKEREVENT (** *event_string* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="789d3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="789d3-107">Parameters</span></span>

|<span data-ttu-id="789d3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="789d3-108">**Name**</span></span>|<span data-ttu-id="789d3-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="789d3-109">**Required/Optional**</span></span>|<span data-ttu-id="789d3-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="789d3-110">**Data Type**</span></span>|<span data-ttu-id="789d3-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="789d3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="789d3-112">_chaîne_événement_</span><span class="sxs-lookup"><span data-stu-id="789d3-112">_event_string_</span></span> <br/> |<span data-ttu-id="789d3-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="789d3-113">Required</span></span>  <br/> |<span data-ttu-id="789d3-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="789d3-114">**String**</span></span> <br/> | <span data-ttu-id="789d3-115">La chaîne à transmettre à votre gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="789d3-115">The string to pass to your event handler.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="789d3-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="789d3-116">Remarks</span></span>

<span data-ttu-id="789d3-117">La fonction QUEUEMARKEREVENT fournit aux développeurs un moyen de notifier leur code à partir d’une cellule de feuille ShapeSheet et transmettre les informations propres à la solution.</span><span class="sxs-lookup"><span data-stu-id="789d3-117">The QUEUEMARKEREVENT function provides developers with a way to notify their code from a ShapeSheet cell, and pass solution-specific information.</span></span> <span data-ttu-id="789d3-118">Lorsque la cellule contenant la formule avec la fonction QUEUEMARKEREVENT est calculée, l’application déclenche un événement marqueur et transmet _event_string_ à tous les gestionnaires d’événement qui écoutent l’événement **MarkerEvent** .</span><span class="sxs-lookup"><span data-stu-id="789d3-118">When the cell containing the formula with the QUEUEMARKEREVENT function is evaluated, the application fires a marker event and passes  _event_string_ to all event handlers that are listening to the **MarkerEvent** event.</span></span> 
  
<span data-ttu-id="789d3-119">Pour plus d’informations sur les événements marqueurs, reportez-vous à la méthode **QueueMarkerEvent** et les rubriques d’événement **MarkerEvent** dans la référence Automation de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="789d3-119">For more information about marker events, see the **QueueMarkerEvent** method and **MarkerEvent** event topics in the Microsoft Visio Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="789d3-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="789d3-120">Example</span></span>

<span data-ttu-id="789d3-121">QUEUEMARKEREVENT ("MyCustomNotification")</span><span class="sxs-lookup"><span data-stu-id="789d3-121">QUEUEMARKEREVENT ("MyCustomNotification")</span></span> 
  
<span data-ttu-id="789d3-122">Entraîne le déclenchement d’un événement marqueur et transmet la chaîne « MyCustomNotification » aux gestionnaires d’événement qui écoutent l’événement **MarkerEvent** .</span><span class="sxs-lookup"><span data-stu-id="789d3-122">Causes the application to fire a marker event, and passes the string "MyCustomNotification" to event handlers that are listening to the **MarkerEvent** event.</span></span> 
  

