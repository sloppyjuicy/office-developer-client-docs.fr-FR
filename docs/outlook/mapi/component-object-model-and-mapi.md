---
title: COM (Component Object Model) et MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334467"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="7d55c-103">COM (Component Object Model) et MAPI</span><span class="sxs-lookup"><span data-stu-id="7d55c-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="7d55c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d55c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d55c-105">La documentation Windows SDK inclut une discussion complète des règles d’implémentation d’objets conformes au modèle objet composant (COM).</span><span class="sxs-lookup"><span data-stu-id="7d55c-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="7d55c-106">Ces règles d mentent la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="7d55c-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="7d55c-107">Interfaces et objets de conception.</span><span class="sxs-lookup"><span data-stu-id="7d55c-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="7d55c-108">Implémenter [l’interface IUnknown.](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d55c-108">Implement the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="7d55c-109">Gérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="7d55c-109">Manage memory.</span></span>
    
- <span data-ttu-id="7d55c-110">Gérer le décompte des références.</span><span class="sxs-lookup"><span data-stu-id="7d55c-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="7d55c-111">Implémenter des objets threadés en location.</span><span class="sxs-lookup"><span data-stu-id="7d55c-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="7d55c-112">Bien que tous les objets MAPI soient considérés comme basés sur COM, car ils implémentent des interfaces qui héritent [d’IUnknown,](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)MAPI s’écarte dans certaines situations des règles COM standard.</span><span class="sxs-lookup"><span data-stu-id="7d55c-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="7d55c-113">Cet écart permet aux développeurs d’avoir plus de souplesse dans leurs implémentations.</span><span class="sxs-lookup"><span data-stu-id="7d55c-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="7d55c-114">Par exemple, une interface MAPI, comme n’importe quelle interface COM, décrit un contrat entre l’implémenteur et l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7d55c-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="7d55c-115">Une fois l’interface créée et publiée, sa définition ne peut pas et ne change pas.</span><span class="sxs-lookup"><span data-stu-id="7d55c-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="7d55c-116">MAPI ne s’écarte pas de cette description, mais il la relâche un peu.</span><span class="sxs-lookup"><span data-stu-id="7d55c-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="7d55c-117">Les implémenteurs peuvent choisir de ne pas implémenter des méthodes particulières, en renvoyant l’une des valeurs d’erreur suivantes à l’appelant :</span><span class="sxs-lookup"><span data-stu-id="7d55c-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="7d55c-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7d55c-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="7d55c-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="7d55c-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="7d55c-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7d55c-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="7d55c-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7d55c-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="7d55c-122">Les autres écarts par rapport aux règles COM standard sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7d55c-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="7d55c-123">**Règle de programmation COM**</span><span class="sxs-lookup"><span data-stu-id="7d55c-123">**COM programming rule**</span></span>|<span data-ttu-id="7d55c-124">**Variante MAPI**</span><span class="sxs-lookup"><span data-stu-id="7d55c-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7d55c-125">Tous les paramètres de chaîne dans les méthodes d’interface doivent être Unicode.</span><span class="sxs-lookup"><span data-stu-id="7d55c-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="7d55c-126">Les interfaces MAPI sont définies pour autoriser les paramètres de chaîne Unicode ou ANSI.</span><span class="sxs-lookup"><span data-stu-id="7d55c-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="7d55c-127">De nombreuses méthodes qui ont un paramètre de chaîne ont également **un paramètre ulFlags** ; la largeur d’un paramètre de chaîne est indiquée par la valeur de l’indicateur MAPI_UNICODE dans **ulFlags**.</span><span class="sxs-lookup"><span data-stu-id="7d55c-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="7d55c-128">Certaines interfaces MAPI ne prisent pas en charge Unicode et retournent des MAPI_E_BAD_CHARWIDTH lorsque l’MAPI_UNICODE est définie.</span><span class="sxs-lookup"><span data-stu-id="7d55c-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="7d55c-129">Toutes les méthodes d’interface doivent avoir un type de retour HRESULT.</span><span class="sxs-lookup"><span data-stu-id="7d55c-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="7d55c-130">MAPI possède au moins une méthode qui renvoie une valeur non HRESULT : [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="7d55c-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="7d55c-131">Les appelants et les implémenteurs doivent allouer et libérer de la mémoire pour les paramètres d’interface à l’aide des allocations de tâches COM standard.</span><span class="sxs-lookup"><span data-stu-id="7d55c-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="7d55c-132">Toutes les méthodes MAPI utilisent les allocateurs liés [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md) pour gérer la mémoire des paramètres d’interface.</span><span class="sxs-lookup"><span data-stu-id="7d55c-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="7d55c-133">Toutes les implémentations MAPI des interfaces définies par OLE, telles que [IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)utilisent les allocations de tâches COM standard.</span><span class="sxs-lookup"><span data-stu-id="7d55c-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="7d55c-134">Tous les paramètres de pointeur sortant doivent être explicitement définies sur NULL en cas d’échec d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="7d55c-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="7d55c-135">Les interfaces MAPI nécessitent que les paramètres de pointeur de sortie soient définies sur NULL ou restent inchangées en cas d’échec d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="7d55c-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="7d55c-136">Toutes les implémentations MAPI des interfaces définies par OLE définissent explicitement les paramètres sur NULL en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="7d55c-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="7d55c-137">Implémenter des objets aggrégables dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="7d55c-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="7d55c-138">Les interfaces MAPI ne sont pas aggrégables.</span><span class="sxs-lookup"><span data-stu-id="7d55c-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d55c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d55c-139">See also</span></span>



[<span data-ttu-id="7d55c-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="7d55c-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="7d55c-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="7d55c-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="7d55c-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7d55c-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="7d55c-143">Vue d’ensemble de l’interface et de l’objet MAPI</span><span class="sxs-lookup"><span data-stu-id="7d55c-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

