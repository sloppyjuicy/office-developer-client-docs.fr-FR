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
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="307cf-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="307cf-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="307cf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="307cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="307cf-105">Définit l’état actuel d’un objet hors connexion sur en ligne ou hors connexion.</span><span class="sxs-lookup"><span data-stu-id="307cf-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="307cf-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="307cf-106">Parameters</span></span>

 <span data-ttu-id="307cf-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="307cf-107">_ulFlags_</span></span>
  
> <span data-ttu-id="307cf-108">[in] Modifie le comportement de cet appel.</span><span class="sxs-lookup"><span data-stu-id="307cf-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="307cf-109">Les valeurs prises en charge sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="307cf-109">The supported values are:</span></span>
    
<span data-ttu-id="307cf-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="307cf-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="307cf-111">Si  _vous définissez ulFlags_ sur cette valeur, l’appel **SetCurrentState** est bloqué jusqu’à ce que le changement d’état soit terminé.</span><span class="sxs-lookup"><span data-stu-id="307cf-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="307cf-112">Par défaut, la transition a lieu de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="307cf-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="307cf-113">Lorsque la transition se produit de manière asynchrone,  tous les appels **SetCurrentState** sont E_PENDING jusqu’à ce que la modification soit terminée.</span><span class="sxs-lookup"><span data-stu-id="307cf-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="307cf-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="307cf-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="307cf-115">Définit l’état actuel sans blocage.</span><span class="sxs-lookup"><span data-stu-id="307cf-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="307cf-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="307cf-116">_ulMask_</span></span>
  
> <span data-ttu-id="307cf-117">[in] Partie de l’état à modifier.</span><span class="sxs-lookup"><span data-stu-id="307cf-117">[in] The part of the state to change.</span></span> <span data-ttu-id="307cf-118">La seule valeur prise en charge est MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="307cf-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="307cf-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="307cf-119">_ulState_</span></span>
  
> <span data-ttu-id="307cf-120">[in] État à modifier.</span><span class="sxs-lookup"><span data-stu-id="307cf-120">[in] The state to change to.</span></span> <span data-ttu-id="307cf-121">Elle doit être l’une des deux valeurs ci-après :</span><span class="sxs-lookup"><span data-stu-id="307cf-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="307cf-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="307cf-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="307cf-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="307cf-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="307cf-124">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="307cf-124">_pReserved_</span></span>
  
> <span data-ttu-id="307cf-125">Ce paramètre est réservé à un Outlook interne et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="307cf-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="307cf-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="307cf-126">Return value</span></span>

<span data-ttu-id="307cf-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="307cf-127">S_OK</span></span>
  
> <span data-ttu-id="307cf-128">L’état de l’objet hors connexion a été modifié avec succès.</span><span class="sxs-lookup"><span data-stu-id="307cf-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="307cf-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="307cf-129">E_PENDING</span></span>
  
> <span data-ttu-id="307cf-130">Cela indique que l’état de l’objet hors connexion change de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="307cf-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="307cf-131">Cela se produit lorsque  _ulFlags_ est définie sur MAPIOFFLINE_FLAG_BLOCK dans un appel **SetCurrentState** précédent et que tout appel **SetCurrentState** ultérieur retourne cette valeur jusqu’à ce que la modification de l’état asynchrone soit terminée.</span><span class="sxs-lookup"><span data-stu-id="307cf-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="307cf-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="307cf-132">See also</span></span>



[<span data-ttu-id="307cf-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="307cf-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="307cf-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="307cf-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="307cf-135">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="307cf-135">MAPI Constants</span></span>](mapi-constants.md)

