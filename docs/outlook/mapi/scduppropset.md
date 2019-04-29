---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406016"
---
# <a name="scduppropset"></a><span data-ttu-id="d980f-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="d980f-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="d980f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d980f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d980f-105">Duplique un tableau de valeurs de propriété dans un bloc unique de mémoire MAPI qui combine les opérations des fonctions [ScCopyProps](sccopyprops.md) et [ScCountProps](sccountprops.md) .</span><span class="sxs-lookup"><span data-stu-id="d980f-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d980f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d980f-106">Header file:</span></span>  <br/> |<span data-ttu-id="d980f-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="d980f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d980f-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="d980f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d980f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d980f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d980f-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="d980f-110">Called by:</span></span>  <br/> |<span data-ttu-id="d980f-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="d980f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="d980f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d980f-112">Parameters</span></span>

 <span data-ttu-id="d980f-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="d980f-113">_cprop_</span></span>
  
> <span data-ttu-id="d980f-114">dans Nombre de valeurs de propriété dans le tableau indiqué par le paramètre _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="d980f-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="d980f-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="d980f-115">_rgprop_</span></span>
  
> <span data-ttu-id="d980f-116">dans Pointeur vers un tableau de structures [SPropValue](spropvalue.md) définissant les valeurs de propriété à dupliquer.</span><span class="sxs-lookup"><span data-stu-id="d980f-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="d980f-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="d980f-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="d980f-118">dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire pour le tableau dupliqué.</span><span class="sxs-lookup"><span data-stu-id="d980f-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="d980f-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="d980f-119">_prgprop_</span></span>
  
> <span data-ttu-id="d980f-120">remarquer Pointeur vers la position initiale dans la mémoire où le tableau de structures **SPropValue** en double renvoyé est stocké.</span><span class="sxs-lookup"><span data-stu-id="d980f-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d980f-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d980f-121">Return value</span></span>

<span data-ttu-id="d980f-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="d980f-122">S_OK</span></span> 
  
> <span data-ttu-id="d980f-123">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="d980f-123">The call succeeded and has returned the expected value or values.</span></span>
    

