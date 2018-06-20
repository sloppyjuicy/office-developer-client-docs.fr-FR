---
title: MAPI et component Object Model
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cf687a7bfadb0981ca3440c2f81bc5de8f910924
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783066"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="8e942-103">MAPI et component Object Model</span><span class="sxs-lookup"><span data-stu-id="8e942-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="8e942-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e942-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e942-105">La documentation du Kit de développement logiciel Windows comprend des informations complètes sur les règles d’implémentation des objets qui sont conformes à l’objet COM (Component Model).</span><span class="sxs-lookup"><span data-stu-id="8e942-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="8e942-106">Ces règles expliquent comment effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e942-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="8e942-107">Concevoir des interfaces et les objets.</span><span class="sxs-lookup"><span data-stu-id="8e942-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="8e942-108">Implémenter l’interface [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8e942-108">Implement the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="8e942-109">Gérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="8e942-109">Manage memory.</span></span>
    
- <span data-ttu-id="8e942-110">Gérer le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="8e942-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="8e942-111">Implémenter des objets apartment de thread.</span><span class="sxs-lookup"><span data-stu-id="8e942-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="8e942-112">Bien que tous les objets MAPI sont considérés comme reposant sur COM, car ils implémentent des interfaces qui héritent de [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx), MAPI écart et dans certaines situations, les règles COM standards.</span><span class="sxs-lookup"><span data-stu-id="8e942-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="8e942-113">Cette déviation permet aux développeurs une plus grande flexibilité dans leurs implémentations.</span><span class="sxs-lookup"><span data-stu-id="8e942-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="8e942-114">Par exemple, une interface MAPI, comme une interface COM, décrit un contrat entre l’implémentation et de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="8e942-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="8e942-115">Une fois que l’interface est créée et publiée, sa définition ne peut pas et ne change pas.</span><span class="sxs-lookup"><span data-stu-id="8e942-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="8e942-116">MAPI ne s’écarte pas cette description, mais il relâche la description quelque peu.</span><span class="sxs-lookup"><span data-stu-id="8e942-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="8e942-117">L’implémentation de la possibilité ne pas implémenter des méthodes, renvoi d’une des valeurs d’erreur à l’appelant :</span><span class="sxs-lookup"><span data-stu-id="8e942-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="8e942-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8e942-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="8e942-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="8e942-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="8e942-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="8e942-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="8e942-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8e942-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="8e942-122">Les autres variations de règles COM standard sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8e942-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="8e942-123">**Règle de programmation COM**</span><span class="sxs-lookup"><span data-stu-id="8e942-123">**COM programming rule**</span></span>|<span data-ttu-id="8e942-124">**Variante MAPI**</span><span class="sxs-lookup"><span data-stu-id="8e942-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8e942-125">Tous les paramètres de chaîne dans les méthodes d’interface doivent être Unicode.</span><span class="sxs-lookup"><span data-stu-id="8e942-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="8e942-126">Les interfaces MAPI sont définies pour autoriser les paramètres de chaîne Unicode ou ANSI.</span><span class="sxs-lookup"><span data-stu-id="8e942-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="8e942-127">De nombreuses méthodes qui ont un paramètre de chaîne ont également un paramètre **ulFlags** ; la largeur d’un paramètre de chaîne est indiquée par la valeur de l’indicateur MAPI_UNICODE dans **ulFlags**.</span><span class="sxs-lookup"><span data-stu-id="8e942-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="8e942-128">Certaines interfaces MAPI ne prend en charge Unicode et renvoyer MAPI_E_BAD_CHARWIDTH lors de l’indicateur MAPI_UNICODE est défini.</span><span class="sxs-lookup"><span data-stu-id="8e942-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="8e942-129">Toutes les méthodes d’interface doivent avoir un type de retour de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="8e942-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="8e942-130">MAPI a au moins une méthode qui retourne une valeur HRESULT non : [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="8e942-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="8e942-131">Les appelants et les responsables de l’implémentation doivent allouer et libérer de la mémoire pour les paramètres de l’interface à l’aide des norme allocateurs de tâche COM.</span><span class="sxs-lookup"><span data-stu-id="8e942-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="8e942-132">Toutes les méthodes MAPI permet de gérer la mémoire pour les paramètres de l’interface les allocateurs liés [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8e942-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="8e942-133">Toutes les implémentations de MAPI des interfaces définies par OLE, tels [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx), utilisent les allocateurs de tâche COM standards.</span><span class="sxs-lookup"><span data-stu-id="8e942-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="8e942-134">Toutes les paramètres pointeurs doivent explicitement être définies sur la valeur NULL en cas d’échec d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="8e942-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="8e942-135">Interfaces MAPI nécessitent que les paramètres pointeurs qu'être défini sur NULL ou restent inchangés lorsqu’une méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="8e942-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="8e942-136">Toutes les implémentations de MAPI des interfaces définies par OLE définir explicitement des paramètres sur la valeur NULL en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="8e942-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="8e942-137">Implémenter des objets agrégées autant que possible.</span><span class="sxs-lookup"><span data-stu-id="8e942-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="8e942-138">Interfaces MAPI ne sont pas agrégées.</span><span class="sxs-lookup"><span data-stu-id="8e942-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e942-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e942-139">See also</span></span>



[<span data-ttu-id="8e942-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="8e942-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="8e942-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="8e942-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="8e942-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8e942-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="8e942-143">Objet MAPI et vue d’ensemble de l’Interface</span><span class="sxs-lookup"><span data-stu-id="8e942-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

