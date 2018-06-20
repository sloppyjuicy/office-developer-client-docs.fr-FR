---
title: CreateIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CreateIProp
api_type:
- COM
ms.assetid: 9bf68814-2564-433d-b762-3d2c83ca3c60
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 906dc4a24b994e079a977808c3f501aaaea9d84f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783105"
---
# <a name="createiprop"></a><span data-ttu-id="4c99e-103">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="4c99e-103">CreateIProp</span></span>

  
  
<span data-ttu-id="4c99e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4c99e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4c99e-105">Crée un objet de données de propriété, autrement dit, un objet [IPropData](ipropdataimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="4c99e-105">Creates a property data object, that is, an [IPropData](ipropdataimapiprop.md) object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c99e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4c99e-106">Header file:</span></span>  <br/> |<span data-ttu-id="4c99e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4c99e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4c99e-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="4c99e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4c99e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4c99e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4c99e-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="4c99e-110">Called by:</span></span>  <br/> |<span data-ttu-id="4c99e-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="4c99e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE CreateIProp(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  LPPROPDATA FAR * lppPropData
);
```

## <a name="parameters"></a><span data-ttu-id="4c99e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c99e-112">Parameters</span></span>

 <span data-ttu-id="4c99e-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4c99e-113">_lpInterface_</span></span>
  
> <span data-ttu-id="4c99e-114">[in] Pointeur vers un identificateur d’interface (IID) pour l’objet de données de propriété.</span><span class="sxs-lookup"><span data-stu-id="4c99e-114">[in] Pointer to an interface identifier (IID) for the property data object.</span></span> <span data-ttu-id="4c99e-115">L’identificateur d’interface valide est IID_IMAPIPropData.</span><span class="sxs-lookup"><span data-stu-id="4c99e-115">The valid interface identifier is IID_IMAPIPropData.</span></span> <span data-ttu-id="4c99e-116">Passage de NULL dans le paramètre _lpInterface_ entraîne également l’objet de données de propriété retournée dans le paramètre _lppPropData_ pour effectuer un cast à l’interface standard pour un objet de données de propriété.</span><span class="sxs-lookup"><span data-stu-id="4c99e-116">Passing NULL in the  _lpInterface_ parameter also causes the property data object returned in the  _lppPropData_ parameter to be cast to the standard interface for a property data object.</span></span> 
    
 <span data-ttu-id="4c99e-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="4c99e-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="4c99e-118">[in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="4c99e-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="4c99e-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="4c99e-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="4c99e-120">[in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer plus de mémoire.</span><span class="sxs-lookup"><span data-stu-id="4c99e-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="4c99e-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="4c99e-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="4c99e-122">[in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="4c99e-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="4c99e-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="4c99e-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="4c99e-124">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="4c99e-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="4c99e-125">_lppPropData_</span><span class="sxs-lookup"><span data-stu-id="4c99e-125">_lppPropData_</span></span>
  
> <span data-ttu-id="4c99e-126">[out] Pointeur vers un pointeur vers l’objet de données de propriété retournées.</span><span class="sxs-lookup"><span data-stu-id="4c99e-126">[out] Pointer to a pointer to the returned property data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4c99e-127">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="4c99e-127">Return value</span></span>

<span data-ttu-id="4c99e-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c99e-128">S_OK</span></span> 
  
> <span data-ttu-id="4c99e-129">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="4c99e-129">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="4c99e-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="4c99e-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="4c99e-131">L’interface demandée n’est pas pris en charge pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="4c99e-131">The requested interface is not supported for this object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c99e-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="4c99e-132">Remarks</span></span>

<span data-ttu-id="4c99e-133">Les paramètres d’entrée _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ point [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), les fonctions [MAPIFreeBuffer](mapifreebuffer.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="4c99e-133">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="4c99e-134">Une application cliente appelant **CreateIProp** passe pointeurs aux fonctions MAPI nommées uniquement ; un fournisseur de services transmet les pointeurs vers ces fonctions qu’elle reçue dans son appel d’initialisation ou récupérés par un appel à la méthode [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="4c99e-134">A client application calling **CreateIProp** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  

