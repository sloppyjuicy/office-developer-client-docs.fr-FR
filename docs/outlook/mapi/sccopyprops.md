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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: eb3b3b3c9c2e9cffb77febf9c96baed40ce3f9e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566221"
---
# <a name="sccopyprops"></a><span data-ttu-id="42e41-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="42e41-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="42e41-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42e41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42e41-105">Copie les propriétés définies par un tableau de structures [SPropValue](spropvalue.md) vers un nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="42e41-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42e41-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="42e41-106">Header file:</span></span>  <br/> |<span data-ttu-id="42e41-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="42e41-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="42e41-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="42e41-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="42e41-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="42e41-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="42e41-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="42e41-110">Called by:</span></span>  <br/> |<span data-ttu-id="42e41-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="42e41-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="42e41-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42e41-112">Parameters</span></span>

 <span data-ttu-id="42e41-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="42e41-113">_cprop_</span></span>
  
> <span data-ttu-id="42e41-114">[in] Nombre de propriétés à copier.</span><span class="sxs-lookup"><span data-stu-id="42e41-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="42e41-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="42e41-115">_rgprop_</span></span>
  
> <span data-ttu-id="42e41-116">[in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) qui définissent les propriétés à copier.</span><span class="sxs-lookup"><span data-stu-id="42e41-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="42e41-117">Le paramètre _rgprop_ ne doit pas pointer vers le début du tableau, mais il doit pointer vers le début d’une des structures **SPropValue** dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="42e41-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="42e41-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="42e41-118">_pvDst_</span></span>
  
> <span data-ttu-id="42e41-119">[in] Pointeur vers la position initiale dans la mémoire à laquelle cette fonction copie les propriétés.</span><span class="sxs-lookup"><span data-stu-id="42e41-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="42e41-120">_carte de circuit imprimé_</span><span class="sxs-lookup"><span data-stu-id="42e41-120">_pcb_</span></span>
  
> <span data-ttu-id="42e41-121">[out] Pointeur facultatif à la taille, en octets, du bloc de mémoire vers laquelle pointé le paramètre _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="42e41-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="42e41-122">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="42e41-122">Return value</span></span>

<span data-ttu-id="42e41-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="42e41-123">S_OK</span></span>
  
> <span data-ttu-id="42e41-124">Les propriétés ont été copiées avec succès.</span><span class="sxs-lookup"><span data-stu-id="42e41-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="42e41-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="42e41-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="42e41-126">Un type de propriété inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="42e41-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42e41-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="42e41-127">Remarks</span></span>

<span data-ttu-id="42e41-128">Le nouveau tableau et ses données résident dans une mémoire tampon créée en une seule fois, et la fonction [ScRelocProps](screlocprops.md) peut être utilisée pour ajuster les pointeurs dans les structures [SPropValue](spropvalue.md) individuels.</span><span class="sxs-lookup"><span data-stu-id="42e41-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="42e41-129">Avant cet ajustement, les pointeurs sont valides.</span><span class="sxs-lookup"><span data-stu-id="42e41-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="42e41-130">**ScCopyProps** conserve l’ordre des propriétés d’origine du tableau de propriétés copiées.</span><span class="sxs-lookup"><span data-stu-id="42e41-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="42e41-131">Le paramètre de la _carte de circuits imprimés_ est facultatif ; s’il n’est pas NULL, elle est définie pour le nombre d’octets stocké dans le paramètre _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="42e41-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42e41-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42e41-132">See also</span></span>



[<span data-ttu-id="42e41-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="42e41-133">ScDupPropset</span></span>](scduppropset.md)

