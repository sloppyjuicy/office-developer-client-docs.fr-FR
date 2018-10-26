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
ms.openlocfilehash: 8bbe8aa00ce446d228c23e1d474fa5140ae7b40a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581978"
---
# <a name="scduppropset"></a><span data-ttu-id="f3629-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="f3629-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="f3629-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3629-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3629-105">Un tableau de valeurs de propriété dans un bloc de mémoire MAPI combinant les opérations des fonctions [ScCopyProps](sccopyprops.md) et [ScCountProps](sccountprops.md) les doublons.</span><span class="sxs-lookup"><span data-stu-id="f3629-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3629-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f3629-106">Header file:</span></span>  <br/> |<span data-ttu-id="f3629-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f3629-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f3629-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f3629-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f3629-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f3629-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f3629-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f3629-110">Called by:</span></span>  <br/> |<span data-ttu-id="f3629-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="f3629-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="f3629-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3629-112">Parameters</span></span>

 <span data-ttu-id="f3629-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="f3629-113">_cprop_</span></span>
  
> <span data-ttu-id="f3629-114">[in] Nombre de valeurs de propriété dans le tableau indiqué par le paramètre _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="f3629-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="f3629-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="f3629-115">_rgprop_</span></span>
  
> <span data-ttu-id="f3629-116">[in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) définissant les valeurs de propriété à dupliquer.</span><span class="sxs-lookup"><span data-stu-id="f3629-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="f3629-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="f3629-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="f3629-118">[in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire pour le tableau dupliqué.</span><span class="sxs-lookup"><span data-stu-id="f3629-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="f3629-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="f3629-119">_prgprop_</span></span>
  
> <span data-ttu-id="f3629-120">[out] Pointeur vers la position initiale dans la mémoire où est stockée la matrice renvoyée dupliquée des structures **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="f3629-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f3629-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f3629-121">Return value</span></span>

<span data-ttu-id="f3629-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3629-122">S_OK</span></span> 
  
> <span data-ttu-id="f3629-123">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f3629-123">The call succeeded and has returned the expected value or values.</span></span>
    

