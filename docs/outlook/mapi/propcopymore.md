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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404469"
---
# <a name="propcopymore"></a><span data-ttu-id="50075-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="50075-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="50075-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50075-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50075-105">Copie une valeur de propriété unique d'un emplacement source vers un emplacement de destination.</span><span class="sxs-lookup"><span data-stu-id="50075-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50075-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="50075-106">Header file:</span></span>  <br/> |<span data-ttu-id="50075-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="50075-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="50075-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="50075-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="50075-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="50075-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="50075-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="50075-110">Called by:</span></span>  <br/> |<span data-ttu-id="50075-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="50075-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="50075-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50075-112">Parameters</span></span>

 <span data-ttu-id="50075-113">_lpSPropValueDest_</span><span class="sxs-lookup"><span data-stu-id="50075-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="50075-114">remarquer Pointeur vers l'emplacement où cette fonction écrit une structure [SPropValue](spropvalue.md) définissant la valeur de la propriété copiée.</span><span class="sxs-lookup"><span data-stu-id="50075-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="50075-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="50075-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="50075-116">dans Pointeur vers la structure [SPropValue](spropvalue.md) qui contient la valeur de propriété à copier.</span><span class="sxs-lookup"><span data-stu-id="50075-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="50075-117">_lpfAllocMore_</span><span class="sxs-lookup"><span data-stu-id="50075-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="50075-118">dans Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire si l'emplacement de destination n'est pas assez grand pour contenir la propriété à copier.</span><span class="sxs-lookup"><span data-stu-id="50075-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="50075-119">_lpvObject_</span><span class="sxs-lookup"><span data-stu-id="50075-119">_lpvObject_</span></span>
  
> <span data-ttu-id="50075-120">dans Pointeur vers un objet pour lequel **MAPIAllocateMore** alloue de l'espace, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="50075-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="50075-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="50075-121">Return value</span></span>

<span data-ttu-id="50075-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="50075-122">S_OK</span></span>
  
> <span data-ttu-id="50075-123">La valeur de la propriété unique a été copiée.</span><span class="sxs-lookup"><span data-stu-id="50075-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="50075-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="50075-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="50075-125">Un type de propriété inconnu a été rencontré.</span><span class="sxs-lookup"><span data-stu-id="50075-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50075-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="50075-126">Remarks</span></span>

<span data-ttu-id="50075-127">Une application cliente ou un fournisseur de services peut utiliser la fonction **PropCopyMore** pour copier une propriété à partir d'une table qui est sur le présent libérée afin de l'utiliser ailleurs.</span><span class="sxs-lookup"><span data-stu-id="50075-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="50075-128">**PropCopyMore** n'a pas besoin d'allouer de la mémoire, sauf si la valeur de la propriété copiée est d'un type tel que PT_STRING8, qui ne rentre pas dans une structure [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="50075-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="50075-129">Pour ces propriétés volumineuses, la fonction alloue de la mémoire à l'aide de la fonction [MAPIAllocateMore](mapiallocatemore.md) à laquelle un pointeur est transmis dans le paramètre _lpfAllocMore_ .</span><span class="sxs-lookup"><span data-stu-id="50075-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="50075-130">Utilisation injudicieuse de la mémoire de fragments **PropCopyMore** ; envisagez d'utiliser la fonction [ScCopyProps](sccopyprops.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="50075-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  

