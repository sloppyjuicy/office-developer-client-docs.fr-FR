---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421087"
---
# <a name="screlocprops"></a><span data-ttu-id="7b0bd-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="7b0bd-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="7b0bd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b0bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b0bd-105">Ajuste les pointeurs dans un tableau [SPropValue](spropvalue.md) après que le tableau et ses données ont été copiés ou déplacés vers un nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="7b0bd-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b0bd-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7b0bd-106">Header file:</span></span>  <br/> |<span data-ttu-id="7b0bd-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7b0bd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7b0bd-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="7b0bd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7b0bd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7b0bd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7b0bd-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="7b0bd-110">Called by:</span></span>  <br/> |<span data-ttu-id="7b0bd-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="7b0bd-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="7b0bd-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b0bd-112">Parameters</span></span>

 <span data-ttu-id="7b0bd-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="7b0bd-113">_cprop_</span></span>
  
> <span data-ttu-id="7b0bd-114">dans Nombre de propriétés dans le tableau vers lequel pointe le paramètre _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="7b0bd-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="7b0bd-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="7b0bd-115">_rgprop_</span></span>
  
> <span data-ttu-id="7b0bd-116">dans Pointeur vers un tableau de structures [SPropValue](spropvalue.md) pour lesquelles les pointeurs doivent être ajustés.</span><span class="sxs-lookup"><span data-stu-id="7b0bd-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="7b0bd-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="7b0bd-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="7b0bd-118">dans Pointeur vers l'adresse de base d'origine du tableau vers lequel pointe le paramètre _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="7b0bd-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="7b0bd-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="7b0bd-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="7b0bd-120">dans Pointeur vers la nouvelle adresse de base du tableau désigné par le paramètre _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="7b0bd-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="7b0bd-121">_circuits_</span><span class="sxs-lookup"><span data-stu-id="7b0bd-121">_pcb_</span></span>
  
> <span data-ttu-id="7b0bd-122">[in, out] Pointeur facultatif vers la taille, en octets, du tableau indiqué par le paramètre _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="7b0bd-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="7b0bd-123">Si la valeur n'est pas NULL, le paramètre _PCB_ est défini sur le nombre d'octets stockés dans le paramètre _pvD_ .</span><span class="sxs-lookup"><span data-stu-id="7b0bd-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7b0bd-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7b0bd-124">Return value</span></span>

<span data-ttu-id="7b0bd-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b0bd-125">S_OK</span></span>
  
> <span data-ttu-id="7b0bd-126">Les pointeurs ont été ajustés avec succès.</span><span class="sxs-lookup"><span data-stu-id="7b0bd-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="7b0bd-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7b0bd-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="7b0bd-128">Un ou les deux paramètres n'étaient pas valides ou un type de propriété inconnu a été rencontré.</span><span class="sxs-lookup"><span data-stu-id="7b0bd-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b0bd-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="7b0bd-129">Remarks</span></span>

<span data-ttu-id="7b0bd-130">La fonction **ScRelocProps** agit sur l'hypothèse que le tableau de valeurs de propriété pour lequel les pointeurs sont ajustés a été alloué à l'origine dans un appel unique semblable à un appel à la fonction **ScCopyProps** .</span><span class="sxs-lookup"><span data-stu-id="7b0bd-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="7b0bd-131">Si une application cliente ou un fournisseur de services travaille avec une valeur de propriété qui est générée à partir de blocs de mémoire disjoints, elle doit utiliser [ScCopyProps](sccopyprops.md) pour copier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="7b0bd-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="7b0bd-132">**ScRelocProps** est utilisé pour maintenir la validité des pointeurs dans un tableau [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="7b0bd-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="7b0bd-133">Pour maintenir la validité des pointeurs lors de l'écriture et de la lecture d'un tel tableau sur un disque, effectuez les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="7b0bd-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="7b0bd-134">Avant d'écrire le tableau et les données sur un disque, appelez **ScRelocProps** sur le tableau avec le paramètre _pvBaseNew_ pointant vers un zéro de valeur standard, par exemple.</span><span class="sxs-lookup"><span data-stu-id="7b0bd-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="7b0bd-135">Après avoir lu le tableau et les données à partir d'un disque, appelez **ScRelocProps** sur le tableau avec le paramètre _pvBaseOld_ égal à la même valeur standard utilisée à l'étape 1.</span><span class="sxs-lookup"><span data-stu-id="7b0bd-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="7b0bd-136">Le tableau et les données doivent être lus dans une mémoire tampon créée avec une seule allocation.</span><span class="sxs-lookup"><span data-stu-id="7b0bd-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="7b0bd-137">Le paramètre _PCB_ vers **ScRelocProps** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="7b0bd-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7b0bd-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b0bd-138">See also</span></span>



[<span data-ttu-id="7b0bd-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="7b0bd-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="7b0bd-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="7b0bd-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="7b0bd-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="7b0bd-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="7b0bd-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="7b0bd-142">ScRelocNotifications</span></span>](screlocnotifications.md)

