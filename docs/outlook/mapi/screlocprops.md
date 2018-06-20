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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 06590fe55cb02b1abf036156877fd308548436f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787110"
---
# <a name="screlocprops"></a><span data-ttu-id="496a5-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="496a5-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="496a5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="496a5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="496a5-105">Ajuster les pointeurs dans un tableau [SPropValue](spropvalue.md) après que le tableau et ses données ont été copiés ou déplacés vers un nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="496a5-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="496a5-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="496a5-106">Header file:</span></span>  <br/> |<span data-ttu-id="496a5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="496a5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="496a5-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="496a5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="496a5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="496a5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="496a5-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="496a5-110">Called by:</span></span>  <br/> |<span data-ttu-id="496a5-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="496a5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="496a5-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="496a5-112">Parameters</span></span>

 <span data-ttu-id="496a5-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="496a5-113">_cprop_</span></span>
  
> <span data-ttu-id="496a5-114">[in] Nombre de propriétés dans le tableau indiqué par le paramètre _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="496a5-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="496a5-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="496a5-115">_rgprop_</span></span>
  
> <span data-ttu-id="496a5-116">[in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) pour lequel des pointeurs doivent être ajustés.</span><span class="sxs-lookup"><span data-stu-id="496a5-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="496a5-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="496a5-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="496a5-118">[in] Pointeur vers l’adresse de base d’origine du tableau indiqué par le paramètre _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="496a5-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="496a5-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="496a5-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="496a5-120">[in] Pointeur vers la nouvelle adresse de base du tableau indiqué par le paramètre _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="496a5-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="496a5-121">_carte de circuit imprimé_</span><span class="sxs-lookup"><span data-stu-id="496a5-121">_pcb_</span></span>
  
> <span data-ttu-id="496a5-122">[entrée, sortie] Pointeur facultatif à la taille, en octets, du tableau indiquée par le paramètre _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="496a5-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="496a5-123">Si ce n’est pas NULL, le paramètre de la _carte de circuits imprimés_ est défini sur le nombre d’octets stocké dans le paramètre _pvD_ .</span><span class="sxs-lookup"><span data-stu-id="496a5-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="496a5-124">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="496a5-124">Return value</span></span>

<span data-ttu-id="496a5-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="496a5-125">S_OK</span></span>
  
> <span data-ttu-id="496a5-126">Pointeurs ont été ajustés avec succès.</span><span class="sxs-lookup"><span data-stu-id="496a5-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="496a5-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="496a5-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="496a5-128">Un ou les deux paramètres ne sont pas valides, ou un type de propriété inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="496a5-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="496a5-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="496a5-129">Remarks</span></span>

<span data-ttu-id="496a5-130">La fonction **ScRelocProps** fonctionne sur l’hypothèse que le tableau de valeurs de propriété pour laquelle des pointeurs sont ajustées alloué initialement en un seul appel semblable à un appel à la fonction **ScCopyProps** .</span><span class="sxs-lookup"><span data-stu-id="496a5-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="496a5-131">Si une application cliente ou un fournisseur de services fonctionne avec une valeur de propriété qui est générée à partir des blocs de mémoire, il doit utiliser [ScCopyProps](sccopyprops.md) pour copier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="496a5-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="496a5-132">**ScRelocProps** est utilisée pour mettre à jour de la validité des pointeurs dans un tableau [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="496a5-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="496a5-133">Pour maintenir la validité des pointeurs lorsque vous écrivez de ce type de tableau à et lire à partir d’un disque, effectuez les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="496a5-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="496a5-134">Avant d’écrire le tableau et les données sur un disque, appelez **ScRelocProps** dans le tableau avec le paramètre _pvBaseNew_ pointe vers une valeur standard zéro, par exemple.</span><span class="sxs-lookup"><span data-stu-id="496a5-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="496a5-135">Après avoir lu le tableau et les données d’un disque, appelez **ScRelocProps** dans le tableau avec le paramètre _pvBaseOld_ égale à la même valeur standard utilisée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="496a5-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="496a5-136">Le tableau et les données doivent être lus dans un tampon créé en une seule fois.</span><span class="sxs-lookup"><span data-stu-id="496a5-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="496a5-137">Le paramètre de la _carte de circuit imprimé_ à **ScRelocProps** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="496a5-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="496a5-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="496a5-138">See also</span></span>



[<span data-ttu-id="496a5-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="496a5-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="496a5-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="496a5-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="496a5-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="496a5-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="496a5-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="496a5-142">ScRelocNotifications</span></span>](screlocnotifications.md)

