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
# <a name="imapiwaitresult--iunknown"></a><span data-ttu-id="10938-103">IMAPIWaitResult : IUnknown</span><span class="sxs-lookup"><span data-stu-id="10938-103">IMAPIWaitResult : IUnknown</span></span>
  
<span data-ttu-id="10938-104">**S’applique** à : Outlook 2013 | Outlook 2016 | Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="10938-104">**Applies to**: Outlook 2013 | Outlook 2016 | Outlook 2019</span></span>

<span data-ttu-id="10938-105">Cette interface est utilisée par les consommateurs d’IMAPIInitMonitor pour contrôler l’endroit où l’attente se produit.</span><span class="sxs-lookup"><span data-stu-id="10938-105">This interface is used by consumers of IMAPIInitMonitor to control where the wait happens.</span></span> <span data-ttu-id="10938-106">Il leur permet de créer l’objet sur un thread et de le déplacer sur un autre thread pour effectuer l’attente réelle.</span><span class="sxs-lookup"><span data-stu-id="10938-106">It allows them create the object on one thread and move it another thread to perform the actual wait.</span></span>

## <a name="vtable-order"></a><span data-ttu-id="10938-107">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="10938-107">Vtable order</span></span>

| <span data-ttu-id="10938-108">fonction</span><span class="sxs-lookup"><span data-stu-id="10938-108">function</span></span> | <span data-ttu-id="10938-109">description</span><span class="sxs-lookup"><span data-stu-id="10938-109">description</span></span> |
|:-----|:-----|
|[<span data-ttu-id="10938-110">HRESULT IMAPIWaitResult::End()</span><span class="sxs-lookup"><span data-stu-id="10938-110">HRESULT IMAPIWaitResult::End()</span></span>](imapiwaitresult-end.md)|<span data-ttu-id="10938-111">Appelé pour lancer l’attente bloquante sur le thread où il est appelé, qui ne doit pas nécessairement être le même thread que celui appelé *IMAPIInitMonitor::BeginWait*.</span><span class="sxs-lookup"><span data-stu-id="10938-111">Called to initiate the blocking wait on the thread where it is called, which does not need to be the same thread that called *IMAPIInitMonitor::BeginWait*.</span></span>|

| <span data-ttu-id="10938-112">informations rapides</span><span class="sxs-lookup"><span data-stu-id="10938-112">quick info</span></span> | <span data-ttu-id="10938-113">result</span><span class="sxs-lookup"><span data-stu-id="10938-113">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="10938-114">Hérite de :</span><span class="sxs-lookup"><span data-stu-id="10938-114">Inherits from:</span></span>  <br/> |<span data-ttu-id="10938-115">IUnknown</span><span class="sxs-lookup"><span data-stu-id="10938-115">IUnknown</span></span>  <br/> |
|<span data-ttu-id="10938-116">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="10938-116">Implemented by:</span></span>  <br/> |  <span data-ttu-id="10938-117">OLMAPI32.DLL</span><span class="sxs-lookup"><span data-stu-id="10938-117">OLMAPI32.DLL</span></span><br/> |
|<span data-ttu-id="10938-118">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="10938-118">Called by:</span></span>  <br/> |<span data-ttu-id="10938-119">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="10938-119">Client applications</span></span>  <br/> |
|<span data-ttu-id="10938-120">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="10938-120">Interface identifier:</span></span>  <br/> |<span data-ttu-id="10938-121">IID_IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="10938-121">IID_IMAPIWaitResult</span></span>  <br/> |

## <a name="see-also"></a><span data-ttu-id="10938-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10938-122">See also</span></span>

[<span data-ttu-id="10938-123">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="10938-123">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="10938-124">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="10938-124">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="10938-125">IMAPIInitMonitor : IUnknown</span><span class="sxs-lookup"><span data-stu-id="10938-125">IMAPIInitMonitor : IUnknown</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="10938-126">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="10938-126">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)
