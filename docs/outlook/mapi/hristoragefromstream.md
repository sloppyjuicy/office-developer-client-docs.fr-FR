---
title: HrIStorageFromStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrIStorageFromStream
api_type:
- HeaderDef
ms.assetid: 1cdc95b8-a156-4600-9e20-caaa02680e87
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1362b1131d937ef240aa1962db8c1b5116786c67
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416831"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="278dc-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="278dc-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="278dc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="278dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="278dc-105">Couches **d’une interface IStorage** sur un **objet IStream.**</span><span class="sxs-lookup"><span data-stu-id="278dc-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="278dc-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="278dc-106">Header file:</span></span>  <br/> |<span data-ttu-id="278dc-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="278dc-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="278dc-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="278dc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="278dc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="278dc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="278dc-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="278dc-110">Called by:</span></span>  <br/> |<span data-ttu-id="278dc-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="278dc-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="278dc-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="278dc-112">Parameters</span></span>

 <span data-ttu-id="278dc-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="278dc-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="278dc-114">[in] Pointeur vers **l’objet IUnknown** implémentant **IStream**.</span><span class="sxs-lookup"><span data-stu-id="278dc-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="278dc-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="278dc-115">_lpInterface_</span></span>
  
> <span data-ttu-id="278dc-116">[in] Pointeur vers l’identificateur d’interface (IID) de l’objet de flux.</span><span class="sxs-lookup"><span data-stu-id="278dc-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="278dc-117">L’une des valeurs suivantes peut être transmise dans le paramètre  _lpInterface_ : NULL, IID_IStream ou IID_ILockBytes.</span><span class="sxs-lookup"><span data-stu-id="278dc-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="278dc-118">La transmission de la valeur NULL  _dans lpInterface_ est la même que la transmission IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="278dc-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="278dc-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="278dc-119">_ulFlags_</span></span>
  
> <span data-ttu-id="278dc-120">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet de stockage doit être créé par rapport au flux.</span><span class="sxs-lookup"><span data-stu-id="278dc-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="278dc-121">Le paramètre par défaut est STGSTRM_RESET, ce qui donne à l’objet de stockage un accès en lecture seule et le démarre à la position zéro du flux.</span><span class="sxs-lookup"><span data-stu-id="278dc-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="278dc-122">Les indicateurs suivants peuvent être définies dans n’importe quelle combinaison, sauf comme indiqué :</span><span class="sxs-lookup"><span data-stu-id="278dc-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="278dc-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="278dc-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="278dc-124">Crée un objet de stockage pour l’objet stream.</span><span class="sxs-lookup"><span data-stu-id="278dc-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="278dc-125">Cet indicateur ne peut pas être définie si l’STGSTRM_RESET est définie.</span><span class="sxs-lookup"><span data-stu-id="278dc-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="278dc-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="278dc-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="278dc-127">Démarre le stockage à la position actuelle du flux.</span><span class="sxs-lookup"><span data-stu-id="278dc-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="278dc-128">Cet indicateur ne peut pas être définie si l’STGSTRM_RESET est définie.</span><span class="sxs-lookup"><span data-stu-id="278dc-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="278dc-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="278dc-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="278dc-130">Permet au fournisseur de services d’appel d’écrire dans le stockage renvoyé.</span><span class="sxs-lookup"><span data-stu-id="278dc-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="278dc-131">Cet indicateur ne peut pas être définie si l’STGSTRM_RESET est définie.</span><span class="sxs-lookup"><span data-stu-id="278dc-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="278dc-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="278dc-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="278dc-133">Démarre le stockage à la position zéro.</span><span class="sxs-lookup"><span data-stu-id="278dc-133">Starts storage at position zero.</span></span> <span data-ttu-id="278dc-134">Cet indicateur ne peut pas être définie si un autre indicateur est définie.</span><span class="sxs-lookup"><span data-stu-id="278dc-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="278dc-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="278dc-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="278dc-136">[out] Pointeur vers un pointeur vers l’objet **IStorage** renvoyé.</span><span class="sxs-lookup"><span data-stu-id="278dc-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="278dc-137">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="278dc-137">Return value</span></span>

<span data-ttu-id="278dc-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="278dc-138">S_OK</span></span> 
  
> <span data-ttu-id="278dc-139">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="278dc-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="278dc-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="278dc-140">Remarks</span></span>

<span data-ttu-id="278dc-141">Les fournisseurs de magasins de messages supportent la fonction **HrIStorageFromStream** à l’aide de l’interface **IStorage** pour les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="278dc-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="278dc-142">Les fournisseurs du Store doivent implémenter **l’interface IStream.**</span><span class="sxs-lookup"><span data-stu-id="278dc-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="278dc-143">**HrIStorageFromStream fournit** l’interface **IStorage** pour l’objet **IStream.**</span><span class="sxs-lookup"><span data-stu-id="278dc-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="278dc-144">Il est possible de transmettre un **ILockBytes** ou une interface **IStream** dans  _lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="278dc-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

