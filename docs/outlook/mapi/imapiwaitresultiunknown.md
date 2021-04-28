---
title: 'IMAPIWaitResult : IUnknown'
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: d7157f57-709d-4e53-973b-176954e2bb73
description: IMAPIWaitResult
Last modified: April 26, 2021
ms.openlocfilehash: 67a0fffdd0ab6d4989c12568f4d89808ba5adc7a
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062038"
---
# <a name="imapiwaitresult--iunknown"></a><span data-ttu-id="35752-103">IMAPIWaitResult : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35752-103">IMAPIWaitResult : IUnknown</span></span>
  
<span data-ttu-id="35752-104">**S'applique** à : Outlook 2013 | Outlook 2016 | Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="35752-104">**Applies to**: Outlook 2013 | Outlook 2016 | Outlook 2019</span></span>

<span data-ttu-id="35752-105">Cette interface est utilisée par les consommateurs d'IMAPIInitMonitor pour contrôler l'endroit où l'attente se produit.</span><span class="sxs-lookup"><span data-stu-id="35752-105">This interface is used by consumers of IMAPIInitMonitor to control where the wait happens.</span></span> <span data-ttu-id="35752-106">Il leur permet de créer l'objet sur un thread et de le déplacer sur un autre thread pour effectuer l'attente réelle.</span><span class="sxs-lookup"><span data-stu-id="35752-106">It allows them create the object on one thread and move it another thread to perform the actual wait.</span></span>

## <a name="vtable-order"></a><span data-ttu-id="35752-107">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="35752-107">Vtable order</span></span>

| <span data-ttu-id="35752-108">fonction</span><span class="sxs-lookup"><span data-stu-id="35752-108">function</span></span> | <span data-ttu-id="35752-109">description</span><span class="sxs-lookup"><span data-stu-id="35752-109">description</span></span> |
|:-----|:-----|
|[<span data-ttu-id="35752-110">HRESULT IMAPIWaitResult::End()</span><span class="sxs-lookup"><span data-stu-id="35752-110">HRESULT IMAPIWaitResult::End()</span></span>](imapiwaitresult-end.md)|<span data-ttu-id="35752-111">Appelé pour lancer l'attente bloquante sur le thread où il est appelé, qui ne doit pas nécessairement être le même thread que celui appelé *IMAPIInitMonitor::BeginWait*.</span><span class="sxs-lookup"><span data-stu-id="35752-111">Called to initiate the blocking wait on the thread where it is called, which does not need to be the same thread that called *IMAPIInitMonitor::BeginWait*.</span></span>|

| <span data-ttu-id="35752-112">informations rapides</span><span class="sxs-lookup"><span data-stu-id="35752-112">quick info</span></span> | <span data-ttu-id="35752-113">result</span><span class="sxs-lookup"><span data-stu-id="35752-113">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="35752-114">Hérite de :</span><span class="sxs-lookup"><span data-stu-id="35752-114">Inherits from:</span></span>  <br/> |<span data-ttu-id="35752-115">IUnknown</span><span class="sxs-lookup"><span data-stu-id="35752-115">IUnknown</span></span>  <br/> |
|<span data-ttu-id="35752-116">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="35752-116">Implemented by:</span></span>  <br/> |  <span data-ttu-id="35752-117">OLMAPI32.DLL</span><span class="sxs-lookup"><span data-stu-id="35752-117">OLMAPI32.DLL</span></span><br/> |
|<span data-ttu-id="35752-118">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="35752-118">Called by:</span></span>  <br/> |<span data-ttu-id="35752-119">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="35752-119">Client applications</span></span>  <br/> |
|<span data-ttu-id="35752-120">Identificateur d'interface :</span><span class="sxs-lookup"><span data-stu-id="35752-120">Interface identifier:</span></span>  <br/> |<span data-ttu-id="35752-121">IID_IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="35752-121">IID_IMAPIWaitResult</span></span>  <br/> |

## <a name="see-also"></a><span data-ttu-id="35752-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35752-122">See also</span></span>

[<span data-ttu-id="35752-123">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="35752-123">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="35752-124">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="35752-124">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="35752-125">IMAPIInitMonitor : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35752-125">IMAPIInitMonitor : IUnknown</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="35752-126">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="35752-126">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)
