---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1afd922459be2ec4bbbd27a61fdf6fcb425548c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411007"
---
# <a name="sccopyprops"></a><span data-ttu-id="729c6-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="729c6-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="729c6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="729c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="729c6-105">Copie les propriétés définies par un tableau de structures [SPropValue](spropvalue.md) vers une nouvelle destination.</span><span class="sxs-lookup"><span data-stu-id="729c6-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="729c6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="729c6-106">Header file:</span></span>  <br/> |<span data-ttu-id="729c6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="729c6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="729c6-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="729c6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="729c6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="729c6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="729c6-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="729c6-110">Called by:</span></span>  <br/> |<span data-ttu-id="729c6-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="729c6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="729c6-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="729c6-112">Parameters</span></span>

 <span data-ttu-id="729c6-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="729c6-113">_cprop_</span></span>
  
> <span data-ttu-id="729c6-114">[in] Nombre de propriétés à copier.</span><span class="sxs-lookup"><span data-stu-id="729c6-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="729c6-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="729c6-115">_rgprop_</span></span>
  
> <span data-ttu-id="729c6-116">[in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) qui définissent les propriétés à copier.</span><span class="sxs-lookup"><span data-stu-id="729c6-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="729c6-117">Le  _paramètre rgprop_ ne doit pas pointer vers le début du tableau, mais il doit pointer vers le début de l’une des structures **SPropValue** dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="729c6-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="729c6-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="729c6-118">_pvDst_</span></span>
  
> <span data-ttu-id="729c6-119">[in] Pointeur vers la position initiale de la mémoire vers laquelle cette fonction copie les propriétés.</span><span class="sxs-lookup"><span data-stu-id="729c6-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="729c6-120">_pcb_</span><span class="sxs-lookup"><span data-stu-id="729c6-120">_pcb_</span></span>
  
> <span data-ttu-id="729c6-121">[out] Pointeur facultatif vers la taille, en octets, du bloc de mémoire pointé par le _paramètre pvDst._</span><span class="sxs-lookup"><span data-stu-id="729c6-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="729c6-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="729c6-122">Return value</span></span>

<span data-ttu-id="729c6-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="729c6-123">S_OK</span></span>
  
> <span data-ttu-id="729c6-124">Les propriétés ont été copiées avec succès.</span><span class="sxs-lookup"><span data-stu-id="729c6-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="729c6-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="729c6-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="729c6-126">Un type de propriété inconnu a été rencontré.</span><span class="sxs-lookup"><span data-stu-id="729c6-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="729c6-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="729c6-127">Remarks</span></span>

<span data-ttu-id="729c6-128">Le nouveau tableau et ses données résident dans une mémoire tampon créée avec une allocation unique, et la fonction [ScRelocProps](screlocprops.md) peut être utilisée pour ajuster les pointeurs dans les structures [SPropValue](spropvalue.md) individuelles.</span><span class="sxs-lookup"><span data-stu-id="729c6-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="729c6-129">Avant cet ajustement, les pointeurs sont valides.</span><span class="sxs-lookup"><span data-stu-id="729c6-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="729c6-130">**ScCopyProps** conserve l’ordre des propriétés d’origine pour le tableau de propriétés copiées.</span><span class="sxs-lookup"><span data-stu-id="729c6-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="729c6-131">Le _paramètre pcb_ est facultatif ; si elle n’est pas NULL, elle est définie sur le nombre d’octets stockés dans le _paramètre pvDst._</span><span class="sxs-lookup"><span data-stu-id="729c6-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="729c6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="729c6-132">See also</span></span>



[<span data-ttu-id="729c6-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="729c6-133">ScDupPropset</span></span>](scduppropset.md)

