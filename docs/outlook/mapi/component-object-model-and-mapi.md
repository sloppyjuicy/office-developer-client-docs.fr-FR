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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394117"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="e1339-103">COM (Component Object Model) et MAPI</span><span class="sxs-lookup"><span data-stu-id="e1339-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="e1339-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1339-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1339-105">La documentation du Kit de développement logiciel Windows comprend des informations complètes sur les règles d’implémentation des objets qui sont conformes à l’objet COM (Component Model).</span><span class="sxs-lookup"><span data-stu-id="e1339-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="e1339-106">Ces règles expliquent comment effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1339-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="e1339-107">Concevoir des interfaces et les objets.</span><span class="sxs-lookup"><span data-stu-id="e1339-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="e1339-108">Implémenter l’interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e1339-108">Implement the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="e1339-109">Gérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e1339-109">Manage memory.</span></span>
    
- <span data-ttu-id="e1339-110">Gérer le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="e1339-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="e1339-111">Implémenter des objets apartment de thread.</span><span class="sxs-lookup"><span data-stu-id="e1339-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="e1339-112">Bien que tous les objets MAPI sont considérés comme reposant sur COM, car ils implémentent des interfaces qui héritent de [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI écart et dans certaines situations, les règles COM standards.</span><span class="sxs-lookup"><span data-stu-id="e1339-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="e1339-113">Cette déviation permet aux développeurs une plus grande flexibilité dans leurs implémentations.</span><span class="sxs-lookup"><span data-stu-id="e1339-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="e1339-114">Par exemple, une interface MAPI, comme une interface COM, décrit un contrat entre l’implémentation et de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e1339-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="e1339-115">Une fois que l’interface est créée et publiée, sa définition ne peut pas et ne change pas.</span><span class="sxs-lookup"><span data-stu-id="e1339-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="e1339-116">MAPI ne s’écarte pas cette description, mais il relâche la description quelque peu.</span><span class="sxs-lookup"><span data-stu-id="e1339-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="e1339-117">L’implémentation de la possibilité ne pas implémenter des méthodes, renvoi d’une des valeurs d’erreur à l’appelant :</span><span class="sxs-lookup"><span data-stu-id="e1339-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="e1339-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e1339-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="e1339-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="e1339-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="e1339-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="e1339-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="e1339-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e1339-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="e1339-122">Les autres variations de règles COM standard sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e1339-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="e1339-123">**Règle de programmation COM**</span><span class="sxs-lookup"><span data-stu-id="e1339-123">**COM programming rule**</span></span>|<span data-ttu-id="e1339-124">**Variante MAPI**</span><span class="sxs-lookup"><span data-stu-id="e1339-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e1339-125">Tous les paramètres de chaîne dans les méthodes d’interface doivent être Unicode.</span><span class="sxs-lookup"><span data-stu-id="e1339-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="e1339-126">Les interfaces MAPI sont définies pour autoriser les paramètres de chaîne Unicode ou ANSI.</span><span class="sxs-lookup"><span data-stu-id="e1339-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="e1339-127">De nombreuses méthodes qui ont un paramètre de chaîne ont également un paramètre **ulFlags** ; la largeur d’un paramètre de chaîne est indiquée par la valeur de l’indicateur MAPI_UNICODE dans **ulFlags**.</span><span class="sxs-lookup"><span data-stu-id="e1339-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="e1339-128">Certaines interfaces MAPI ne prend en charge Unicode et renvoyer MAPI_E_BAD_CHARWIDTH lors de l’indicateur MAPI_UNICODE est défini.</span><span class="sxs-lookup"><span data-stu-id="e1339-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="e1339-129">Toutes les méthodes d’interface doivent avoir un type de retour de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="e1339-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="e1339-130">MAPI a au moins une méthode qui retourne une valeur HRESULT non : [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="e1339-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="e1339-131">Les appelants et les responsables de l’implémentation doivent allouer et libérer de la mémoire pour les paramètres de l’interface à l’aide des norme allocateurs de tâche COM.</span><span class="sxs-lookup"><span data-stu-id="e1339-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="e1339-132">Toutes les méthodes MAPI permet de gérer la mémoire pour les paramètres de l’interface les allocateurs liés [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e1339-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="e1339-133">Toutes les implémentations de MAPI des interfaces définies par OLE, tels [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), utilisent les allocateurs de tâche COM standards.</span><span class="sxs-lookup"><span data-stu-id="e1339-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="e1339-134">Toutes les paramètres pointeurs doivent explicitement être définies sur la valeur NULL en cas d’échec d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="e1339-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="e1339-135">Interfaces MAPI nécessitent que les paramètres pointeurs qu'être défini sur NULL ou restent inchangés lorsqu’une méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="e1339-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="e1339-136">Toutes les implémentations de MAPI des interfaces définies par OLE définir explicitement des paramètres sur la valeur NULL en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="e1339-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="e1339-137">Implémenter des objets agrégées autant que possible.</span><span class="sxs-lookup"><span data-stu-id="e1339-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="e1339-138">Interfaces MAPI ne sont pas agrégées.</span><span class="sxs-lookup"><span data-stu-id="e1339-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1339-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1339-139">See also</span></span>



[<span data-ttu-id="e1339-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e1339-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="e1339-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="e1339-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="e1339-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e1339-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="e1339-143">Objet MAPI et vue d’ensemble de l’Interface</span><span class="sxs-lookup"><span data-stu-id="e1339-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

