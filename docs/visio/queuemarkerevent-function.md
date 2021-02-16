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
description: Entraîne l’application à tirer un événement marqueur sur votre module Visual Basic pour Applications code Microsoft (VBA) ou votre compl?ment COM.
ms.openlocfilehash: 841f6acc63497a6f0b8930c89534b5f8b04c0393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418805"
---
# <a name="queuemarkerevent-function"></a><span data-ttu-id="a3009-103">Fonction QUEUEMARKEREVENT</span><span class="sxs-lookup"><span data-stu-id="a3009-103">QUEUEMARKEREVENT Function</span></span>

<span data-ttu-id="a3009-104">Entraîne l’application à tirer un événement marqueur sur votre module Visual Basic pour Applications code Microsoft (VBA) ou votre compl?ment COM.</span><span class="sxs-lookup"><span data-stu-id="a3009-104">Causes the application to fire a marker event to your add-on, Microsoft Visual Basic for Applications (VBA) code, or COM add-in.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a3009-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3009-105">Syntax</span></span>

<span data-ttu-id="a3009-106">QUEUEMARKEREVENT (\*\* *event_string* \*\* )</span><span class="sxs-lookup"><span data-stu-id="a3009-106">QUEUEMARKEREVENT (\*\* *event_string* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a3009-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3009-107">Parameters</span></span>

|<span data-ttu-id="a3009-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a3009-108">**Name**</span></span>|<span data-ttu-id="a3009-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a3009-109">**Required/Optional**</span></span>|<span data-ttu-id="a3009-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a3009-110">**Data Type**</span></span>|<span data-ttu-id="a3009-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a3009-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a3009-112">_event_string_</span><span class="sxs-lookup"><span data-stu-id="a3009-112">_event_string_</span></span> <br/> |<span data-ttu-id="a3009-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a3009-113">Required</span></span>  <br/> |<span data-ttu-id="a3009-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a3009-114">**String**</span></span> <br/> | <span data-ttu-id="a3009-115">Chaîne à transmettre à votre handler d’événements.</span><span class="sxs-lookup"><span data-stu-id="a3009-115">The string to pass to your event handler.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3009-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3009-116">Remarks</span></span>

<span data-ttu-id="a3009-117">La fonction QUEUEMARKEREVENT fournit aux développeurs un moyen de notifier leur code à partir d’une cellule ShapeSheet et de transmettre des informations spécifiques aux solutions.</span><span class="sxs-lookup"><span data-stu-id="a3009-117">The QUEUEMARKEREVENT function provides developers with a way to notify their code from a ShapeSheet cell, and pass solution-specific information.</span></span> <span data-ttu-id="a3009-118">Lorsque la cellule contenant la formule avec la fonction QUEUEMARKEREVENT est évaluée, l’application déclenche un événement marqueur et transmet _event_string_ à tous les handlers d’événements qui écoutent l’événement **MarkerEvent.**</span><span class="sxs-lookup"><span data-stu-id="a3009-118">When the cell containing the formula with the QUEUEMARKEREVENT function is evaluated, the application fires a marker event and passes  _event_string_ to all event handlers that are listening to the **MarkerEvent** event.</span></span> 
  
<span data-ttu-id="a3009-119">Pour plus d’informations sur les événements de marqueur, voir la méthode **QueueMarkerEvent** et les rubriques sur les événements **MarkerEvent** dans la Référence Microsoft Visio Automation.</span><span class="sxs-lookup"><span data-stu-id="a3009-119">For more information about marker events, see the **QueueMarkerEvent** method and **MarkerEvent** event topics in the Microsoft Visio Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a3009-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="a3009-120">Example</span></span>

<span data-ttu-id="a3009-121">QUEUEMARKEREVENT ("MyCustomNotification")</span><span class="sxs-lookup"><span data-stu-id="a3009-121">QUEUEMARKEREVENT ("MyCustomNotification")</span></span> 
  
<span data-ttu-id="a3009-122">Entraîne le déclenchement d’un événement marqueur et transmet la chaîne « MyCustomNotification » aux gestionnaires d’événement qui écoutent l’événement **MarkerEvent**.</span><span class="sxs-lookup"><span data-stu-id="a3009-122">Causes the application to fire a marker event, and passes the string "MyCustomNotification" to event handlers that are listening to the **MarkerEvent** event.</span></span> 
  

