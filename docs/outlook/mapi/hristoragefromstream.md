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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bd2d0a662585e8aba91250786f88dd310fe37e32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783556"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="2a9e2-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="2a9e2-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="2a9e2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2a9e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2a9e2-105">Couches d’une interface **IStorage** sur un objet **IStream** .</span><span class="sxs-lookup"><span data-stu-id="2a9e2-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a9e2-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2a9e2-106">Header file:</span></span>  <br/> |<span data-ttu-id="2a9e2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2a9e2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2a9e2-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="2a9e2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2a9e2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2a9e2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2a9e2-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="2a9e2-110">Called by:</span></span>  <br/> |<span data-ttu-id="2a9e2-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="2a9e2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="2a9e2-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a9e2-112">Parameters</span></span>

 <span data-ttu-id="2a9e2-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="2a9e2-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="2a9e2-114">[in] Pointeur vers l’objet **IUnknown** implémentation **IStream**.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="2a9e2-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="2a9e2-115">_lpInterface_</span></span>
  
> <span data-ttu-id="2a9e2-116">[in] Pointeur vers l’identificateur d’interface (IID) de l’objet stream.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="2a9e2-117">Une des valeurs suivantes peuvent être transmise dans le paramètre _lpInterface_ : IID_ILockBytes, IID_IStream ou NULL.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="2a9e2-118">En passant NULL _lpInterface_ est identique au transfert IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="2a9e2-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2a9e2-119">_ulFlags_</span></span>
  
> <span data-ttu-id="2a9e2-120">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet de stockage doit être créé par rapport à l’objet stream.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="2a9e2-121">Le paramètre par défaut est STGSTRM_RESET, qui fournit l’accès en lecture seule d’objet stockage et démarre à la position zéro de l’objet stream.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="2a9e2-122">Les indicateurs suivants peuvent avoir n’importe quelle combinaison, sauf comme indiqué précédemment :</span><span class="sxs-lookup"><span data-stu-id="2a9e2-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="2a9e2-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="2a9e2-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="2a9e2-124">Crée un nouvel objet de stockage pour l’objet stream.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="2a9e2-125">Cet indicateur ne peut pas être défini si l’indicateur STGSTRM_RESET est défini.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="2a9e2-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="2a9e2-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="2a9e2-127">Démarre le stockage à la position actuelle du flux.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="2a9e2-128">Cet indicateur ne peut pas être défini si l’indicateur STGSTRM_RESET est défini.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="2a9e2-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="2a9e2-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="2a9e2-130">Permet au fournisseur de service appelant écrire dans le stockage renvoyé.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="2a9e2-131">Cet indicateur ne peut pas être défini si l’indicateur STGSTRM_RESET est défini.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="2a9e2-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="2a9e2-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="2a9e2-133">Stockage commence à la position zéro.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-133">Starts storage at position zero.</span></span> <span data-ttu-id="2a9e2-134">Impossible de définir cet indicateur si n’importe quel autre indicateur est défini.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="2a9e2-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="2a9e2-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="2a9e2-136">[out] Pointeur vers un pointeur vers l’objet **IStorage** renvoyé.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2a9e2-137">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="2a9e2-137">Return value</span></span>

<span data-ttu-id="2a9e2-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="2a9e2-138">S_OK</span></span> 
  
> <span data-ttu-id="2a9e2-139">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2a9e2-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="2a9e2-140">Remarks</span></span>

<span data-ttu-id="2a9e2-141">Banque de messages fournisseurs prennent en charge la fonction **HrIStorageFromStream** à l’aide de l’interface **IStorage** pour les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="2a9e2-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="2a9e2-142">Fournisseurs de magasins doivent implémenter l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="2a9e2-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="2a9e2-143">**HrIStorageFromStream** fournit l’interface **IStorage** pour l’objet **IStream** .</span><span class="sxs-lookup"><span data-stu-id="2a9e2-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="2a9e2-144">Il est possible de passer une interface **IStream** dans _lpUnkIn_soit un **ILockBytes** .</span><span class="sxs-lookup"><span data-stu-id="2a9e2-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

