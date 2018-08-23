---
title: PropCopyMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PropCopyMore
api_type:
- HeaderDef
ms.assetid: 133d47cf-3592-44f3-8cdd-be402d160ee4
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 635525a1c2c3234d724534d225eb07022afc9956
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592121"
---
# <a name="propcopymore"></a><span data-ttu-id="d514b-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="d514b-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="d514b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d514b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d514b-105">Copie une seule valeur de propriété à partir d’un emplacement source vers un emplacement de destination.</span><span class="sxs-lookup"><span data-stu-id="d514b-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d514b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d514b-106">Header file:</span></span>  <br/> |<span data-ttu-id="d514b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d514b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d514b-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="d514b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d514b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d514b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d514b-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="d514b-110">Called by:</span></span>  <br/> |<span data-ttu-id="d514b-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="d514b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="d514b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d514b-112">Parameters</span></span>

 <span data-ttu-id="d514b-113">_lpSPropValueDest_</span><span class="sxs-lookup"><span data-stu-id="d514b-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="d514b-114">[out] Pointeur vers l’emplacement sur lequel cette fonction écrit une structure [SPropValue](spropvalue.md) définissant la valeur de propriété copiées.</span><span class="sxs-lookup"><span data-stu-id="d514b-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="d514b-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="d514b-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="d514b-116">[in] Pointeur vers la structure [SPropValue](spropvalue.md) qui contient la valeur de propriété à copier.</span><span class="sxs-lookup"><span data-stu-id="d514b-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="d514b-117">_lpfAllocMore_</span><span class="sxs-lookup"><span data-stu-id="d514b-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="d514b-118">[in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer plus de mémoire si l’emplacement de destination n’est pas suffisante pour contenir la propriété doit être copié.</span><span class="sxs-lookup"><span data-stu-id="d514b-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="d514b-119">_lpvObject_</span><span class="sxs-lookup"><span data-stu-id="d514b-119">_lpvObject_</span></span>
  
> <span data-ttu-id="d514b-120">[in] Pointeur vers un objet pour lequel **MAPIAllocateMore** alloue de l’espace si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d514b-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d514b-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d514b-121">Return value</span></span>

<span data-ttu-id="d514b-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="d514b-122">S_OK</span></span>
  
> <span data-ttu-id="d514b-123">La valeur de la propriété unique a été correctement copiée.</span><span class="sxs-lookup"><span data-stu-id="d514b-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="d514b-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d514b-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="d514b-125">Un type de propriété inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d514b-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d514b-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="d514b-126">Remarks</span></span>

<span data-ttu-id="d514b-127">Une application cliente ou un fournisseur de services peut utiliser la fonction **PropCopyMore** pour copier une propriété en dehors d’une table qui doit être libéré pour pouvoir le pour utiliser ailleurs.</span><span class="sxs-lookup"><span data-stu-id="d514b-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="d514b-128">**PropCopyMore** n’a pas besoin d’allocation de mémoire, sauf si la valeur de la propriété copiée est d’un type, tel que PT_STRING8, qui ne rentre pas dans une structure [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d514b-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="d514b-129">Pour ces propriétés de grande taille, la fonction alloue de la mémoire à l’aide de la fonction [MAPIAllocateMore](mapiallocatemore.md) à laquelle un pointeur est passé dans le paramètre _lpfAllocMore_ .</span><span class="sxs-lookup"><span data-stu-id="d514b-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="d514b-130">Injudicious utilisation de la mémoire de fragments de **PropCopyMore** ; envisager d’utiliser la fonction [ScCopyProps](sccopyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="d514b-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  

