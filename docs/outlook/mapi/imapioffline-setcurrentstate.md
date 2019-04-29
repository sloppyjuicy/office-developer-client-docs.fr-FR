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
ms.openlocfilehash: 0b6837b51b09ecd9a60630c613e1806cb10c1d87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421738"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="15255-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="15255-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="15255-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15255-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15255-105">Définit l'état actuel d'un objet hors connexion sur en ligne ou hors connexion.</span><span class="sxs-lookup"><span data-stu-id="15255-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="15255-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15255-106">Parameters</span></span>

 <span data-ttu-id="15255-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="15255-107">_ulFlags_</span></span>
  
> <span data-ttu-id="15255-108">dans Modifie le comportement de cet appel.</span><span class="sxs-lookup"><span data-stu-id="15255-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="15255-109">Les valeurs prises en charge sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="15255-109">The supported values are:</span></span>
    
<span data-ttu-id="15255-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="15255-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="15255-111">Le fait de définir _ulFlags_ sur cette valeur bloque l'appel **SetCurrentState** jusqu'à ce que le changement d'État soit terminé.</span><span class="sxs-lookup"><span data-stu-id="15255-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="15255-112">Par défaut, la transition a lieu de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="15255-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="15255-113">Lorsque la transition se produit de manière asynchrone, tous les appels **SetCurrentState** renvoient **E_PENDING** jusqu'à la fin de la modification.</span><span class="sxs-lookup"><span data-stu-id="15255-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="15255-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="15255-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="15255-115">Définit l'état actuel sans blocage.</span><span class="sxs-lookup"><span data-stu-id="15255-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="15255-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="15255-116">_ulMask_</span></span>
  
> <span data-ttu-id="15255-117">dans Partie de l'État à modifier.</span><span class="sxs-lookup"><span data-stu-id="15255-117">[in] The part of the state to change.</span></span> <span data-ttu-id="15255-118">La seule valeur prise en charge est MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="15255-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="15255-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="15255-119">_ulState_</span></span>
  
> <span data-ttu-id="15255-120">dans État à modifier.</span><span class="sxs-lookup"><span data-stu-id="15255-120">[in] The state to change to.</span></span> <span data-ttu-id="15255-121">Il doit s'agir de l'une des deux valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="15255-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="15255-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="15255-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="15255-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="15255-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="15255-124">_Disparition_</span><span class="sxs-lookup"><span data-stu-id="15255-124">_pReserved_</span></span>
  
> <span data-ttu-id="15255-125">Ce paramètre est réservé à un usage interne d'Outlook et n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="15255-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="15255-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="15255-126">Return value</span></span>

<span data-ttu-id="15255-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="15255-127">S_OK</span></span>
  
> <span data-ttu-id="15255-128">L'état de l'objet hors connexion a été modifié.</span><span class="sxs-lookup"><span data-stu-id="15255-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="15255-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="15255-129">E_PENDING</span></span>
  
> <span data-ttu-id="15255-130">Cela indique que l'état de l'objet hors connexion est modifié de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="15255-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="15255-131">Cela se produit lorsque _ulFlags_ est défini sur MAPIOFFLINE_FLAG_BLOCK dans un appel de **SetCurrentState** précédent et que tout appel ultérieur de **SetCurrentState** renverra cette valeur jusqu'à ce que le changement d'état asynchrone soit terminé.</span><span class="sxs-lookup"><span data-stu-id="15255-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="15255-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15255-132">See also</span></span>



[<span data-ttu-id="15255-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="15255-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="15255-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="15255-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="15255-135">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="15255-135">MAPI Constants</span></span>](mapi-constants.md)

