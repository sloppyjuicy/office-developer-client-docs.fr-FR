---
title: IMAPIOfflineSetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.SetCurrentState
api_type:
- COM
ms.assetid: c0aa0df2-79f9-2558-7eb6-accae9bef4b2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 13a4cf401cf51241a52401668eef008d65aa5459
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567138"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="61819-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="61819-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="61819-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61819-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61819-105">Définit l’état actuel d’un objet en mode hors connexion en ligne ou hors connexion.</span><span class="sxs-lookup"><span data-stu-id="61819-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="61819-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="61819-106">Parameters</span></span>

 <span data-ttu-id="61819-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="61819-107">_ulFlags_</span></span>
  
> <span data-ttu-id="61819-108">[in] Modifie le comportement de cet appel.</span><span class="sxs-lookup"><span data-stu-id="61819-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="61819-109">Les valeurs prises en charge sont :</span><span class="sxs-lookup"><span data-stu-id="61819-109">The supported values are:</span></span>
    
<span data-ttu-id="61819-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="61819-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="61819-111">Définition de _ulFlags_ sur cette valeur empêchera l’appel **SetCurrentState** jusqu'à ce que le changement d’état est terminé.</span><span class="sxs-lookup"><span data-stu-id="61819-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="61819-112">Par défaut la transition s’effectue de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="61819-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="61819-113">Lors de la transition se produit de manière asynchrone, tous les appels **SetCurrentState** retournera **E_PENDING** jusqu'à ce que la modification est terminée.</span><span class="sxs-lookup"><span data-stu-id="61819-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="61819-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="61819-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="61819-115">Définit l’état actuel sans blocage.</span><span class="sxs-lookup"><span data-stu-id="61819-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="61819-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="61819-116">_ulMask_</span></span>
  
> <span data-ttu-id="61819-117">[in] La partie de l’état à modifier.</span><span class="sxs-lookup"><span data-stu-id="61819-117">[in] The part of the state to change.</span></span> <span data-ttu-id="61819-118">La seule valeur pris en charge est MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="61819-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="61819-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="61819-119">_ulState_</span></span>
  
> <span data-ttu-id="61819-120">[in] L’état à convertir.</span><span class="sxs-lookup"><span data-stu-id="61819-120">[in] The state to change to.</span></span> <span data-ttu-id="61819-121">Il doit être une de ces deux valeurs :</span><span class="sxs-lookup"><span data-stu-id="61819-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="61819-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="61819-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="61819-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="61819-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="61819-124">_Conservés_</span><span class="sxs-lookup"><span data-stu-id="61819-124">_pReserved_</span></span>
  
> <span data-ttu-id="61819-125">Ce paramètre est réservé à un usage interne Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="61819-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="61819-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="61819-126">Return value</span></span>

<span data-ttu-id="61819-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="61819-127">S_OK</span></span>
  
> <span data-ttu-id="61819-128">L’état de l’objet en mode hors connexion a été modifié correctement.</span><span class="sxs-lookup"><span data-stu-id="61819-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="61819-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="61819-129">E_PENDING</span></span>
  
> <span data-ttu-id="61819-130">Cela indique que la modification de l’état de l’objet en mode hors connexion est en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="61819-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="61819-131">Cela se produit lorsque _ulFlags_ est défini sur MAPIOFFLINE_FLAG_BLOCK dans un appel **SetCurrentState** précédent, tous les appels suivants **SetCurrentState** renverra cette valeur jusqu'à ce que le changement d’état asynchrone est terminé.</span><span class="sxs-lookup"><span data-stu-id="61819-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="61819-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61819-132">See also</span></span>



[<span data-ttu-id="61819-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="61819-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="61819-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="61819-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="61819-135">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="61819-135">MAPI Constants</span></span>](mapi-constants.md)

