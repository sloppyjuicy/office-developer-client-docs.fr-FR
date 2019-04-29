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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e318d7a709a09e67ebf423db0263985523d2fc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406807"
---
# <a name="createiprop"></a><span data-ttu-id="ab31e-103">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="ab31e-103">CreateIProp</span></span>

  
  
<span data-ttu-id="ab31e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab31e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab31e-105">Crée un objet de données de propriété, autrement dit, un objet [IPropData](ipropdataimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="ab31e-105">Creates a property data object, that is, an [IPropData](ipropdataimapiprop.md) object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab31e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ab31e-106">Header file:</span></span>  <br/> |<span data-ttu-id="ab31e-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="ab31e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ab31e-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="ab31e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ab31e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ab31e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ab31e-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="ab31e-110">Called by:</span></span>  <br/> |<span data-ttu-id="ab31e-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="ab31e-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="ab31e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab31e-112">Parameters</span></span>

 <span data-ttu-id="ab31e-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ab31e-113">_lpInterface_</span></span>
  
> <span data-ttu-id="ab31e-114">dans Pointeur vers un identificateur d'interface (IID) pour l'objet de données de propriété.</span><span class="sxs-lookup"><span data-stu-id="ab31e-114">[in] Pointer to an interface identifier (IID) for the property data object.</span></span> <span data-ttu-id="ab31e-115">L'identificateur d'interface valide est IID_IMAPIPropData.</span><span class="sxs-lookup"><span data-stu-id="ab31e-115">The valid interface identifier is IID_IMAPIPropData.</span></span> <span data-ttu-id="ab31e-116">Le fait de transmettre NULL dans le paramètre _lpInterface_ entraîne également le cast de l'objet de données de propriété renvoyé dans le paramètre _lppPropData_ en interface standard pour un objet de données de propriété.</span><span class="sxs-lookup"><span data-stu-id="ab31e-116">Passing NULL in the  _lpInterface_ parameter also causes the property data object returned in the  _lppPropData_ parameter to be cast to the standard interface for a property data object.</span></span> 
    
 <span data-ttu-id="ab31e-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="ab31e-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="ab31e-118">dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="ab31e-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="ab31e-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="ab31e-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="ab31e-120">dans Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="ab31e-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="ab31e-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="ab31e-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="ab31e-122">dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="ab31e-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="ab31e-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="ab31e-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="ab31e-124">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="ab31e-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="ab31e-125">_lppPropData_</span><span class="sxs-lookup"><span data-stu-id="ab31e-125">_lppPropData_</span></span>
  
> <span data-ttu-id="ab31e-126">remarquer Pointeur vers un pointeur vers l'objet de données de propriété renvoyé.</span><span class="sxs-lookup"><span data-stu-id="ab31e-126">[out] Pointer to a pointer to the returned property data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ab31e-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ab31e-127">Return value</span></span>

<span data-ttu-id="ab31e-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab31e-128">S_OK</span></span> 
  
> <span data-ttu-id="ab31e-129">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="ab31e-129">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="ab31e-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ab31e-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="ab31e-131">L'interface demandée n'est pas prise en charge pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="ab31e-131">The requested interface is not supported for this object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab31e-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="ab31e-132">Remarks</span></span>

<span data-ttu-id="ab31e-133">Les paramètres d'entrée _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pointent vers les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="ab31e-133">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="ab31e-134">Une application cliente qui appelle **CreateIProp** passe des pointeurs vers les fonctions MAPI que vous venez de nommer; un fournisseur de services transmet les pointeurs à ces fonctions qu'il a reçues dans son appel d'initialisation ou qu'il a récupéré avec un appel à la méthode [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="ab31e-134">A client application calling **CreateIProp** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  

