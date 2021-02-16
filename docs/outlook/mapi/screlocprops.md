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
# <a name="screlocprops"></a><span data-ttu-id="d093b-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="d093b-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="d093b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d093b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d093b-105">Ajuste les pointeurs dans un tableau [SPropValue](spropvalue.md) une fois que le tableau et ses données ont été copiés ou déplacés vers un nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="d093b-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d093b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d093b-106">Header file:</span></span>  <br/> |<span data-ttu-id="d093b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d093b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d093b-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="d093b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d093b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d093b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d093b-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="d093b-110">Called by:</span></span>  <br/> |<span data-ttu-id="d093b-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="d093b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="d093b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d093b-112">Parameters</span></span>

 <span data-ttu-id="d093b-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="d093b-113">_cprop_</span></span>
  
> <span data-ttu-id="d093b-114">[in] Nombre de propriétés dans le tableau pointées par le _paramètre rgprop._</span><span class="sxs-lookup"><span data-stu-id="d093b-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="d093b-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="d093b-115">_rgprop_</span></span>
  
> <span data-ttu-id="d093b-116">[in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) pour lesquelles les pointeurs doivent être ajustés.</span><span class="sxs-lookup"><span data-stu-id="d093b-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="d093b-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="d093b-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="d093b-118">[in] Pointeur vers l’adresse de base d’origine du tableau pointée par le _paramètre rgprop._</span><span class="sxs-lookup"><span data-stu-id="d093b-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="d093b-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="d093b-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="d093b-120">[in] Pointeur vers la nouvelle adresse de base du tableau pointée par le _paramètre rgprop._</span><span class="sxs-lookup"><span data-stu-id="d093b-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="d093b-121">_pcb_</span><span class="sxs-lookup"><span data-stu-id="d093b-121">_pcb_</span></span>
  
> <span data-ttu-id="d093b-122">[in, out] Pointeur facultatif vers la taille, en octets, du tableau indiqué par le _paramètre pvBaseNew._</span><span class="sxs-lookup"><span data-stu-id="d093b-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="d093b-123">Si la valeur n’est pas NULL, le _paramètre pcb_ est définie sur le nombre d’octets stockés dans le _paramètre pvD._</span><span class="sxs-lookup"><span data-stu-id="d093b-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d093b-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d093b-124">Return value</span></span>

<span data-ttu-id="d093b-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="d093b-125">S_OK</span></span>
  
> <span data-ttu-id="d093b-126">Les pointeurs ont été correctement ajustés.</span><span class="sxs-lookup"><span data-stu-id="d093b-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="d093b-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d093b-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="d093b-128">Un ou les deux paramètres n’étaient pas valides ou un type de propriété inconnu a été rencontré.</span><span class="sxs-lookup"><span data-stu-id="d093b-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d093b-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="d093b-129">Remarks</span></span>

<span data-ttu-id="d093b-130">La **fonction ScRelocProps** fonctionne sur l’hypothèse que le tableau de valeurs de propriétés pour lequel les pointeurs sont ajustés a été initialement alloué dans un seul appel semblable à un appel à la fonction **ScCopyProps.**</span><span class="sxs-lookup"><span data-stu-id="d093b-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="d093b-131">Si une application cliente ou un fournisseur de services utilise une valeur de propriété qui est construite à partir de blocs de mémoire disjoints, il doit utiliser [ScCopyProps](sccopyprops.md) pour copier les propriétés à la place.</span><span class="sxs-lookup"><span data-stu-id="d093b-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="d093b-132">**ScRelocProps est** utilisé pour maintenir la validité des pointeurs dans un tableau [SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="d093b-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="d093b-133">Pour conserver la validité des pointeurs lors de l’écriture et de la lecture d’un tel tableau sur un disque, effectuez les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d093b-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="d093b-134">Avant d’écrire le tableau et les données sur un disque, appelez **ScRelocProps** sur le tableau avec le paramètre  _pvBaseNew_ pointant vers une valeur standard zéro, par exemple.</span><span class="sxs-lookup"><span data-stu-id="d093b-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="d093b-135">Après avoir lu le tableau et les données à partir d’un disque, appelez **ScRelocProps** sur le tableau avec le paramètre  _pvBaseOld_ égal à la valeur standard utilisée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="d093b-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="d093b-136">Le tableau et les données doivent être lus dans une mémoire tampon créée avec une allocation unique.</span><span class="sxs-lookup"><span data-stu-id="d093b-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="d093b-137">Le  _paramètre pcb_ de **ScRelocProps est** facultatif.</span><span class="sxs-lookup"><span data-stu-id="d093b-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d093b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d093b-138">See also</span></span>



[<span data-ttu-id="d093b-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d093b-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="d093b-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="d093b-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="d093b-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="d093b-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="d093b-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="d093b-142">ScRelocNotifications</span></span>](screlocnotifications.md)

