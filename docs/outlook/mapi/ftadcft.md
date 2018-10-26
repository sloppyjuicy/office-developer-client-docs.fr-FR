---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f073dbb9655585ee56ab38be35bea4ef320042c0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569770"
---
# <a name="ftadcft"></a><span data-ttu-id="3f629-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="3f629-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="3f629-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f629-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f629-105">Ajoute un entier non signé de 64 bits à un autre, si vous le souhaitez à l’aide d’un indicateur de transport.</span><span class="sxs-lookup"><span data-stu-id="3f629-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f629-106">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="3f629-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="3f629-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="3f629-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="3f629-108">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="3f629-108">Called by:</span></span>  <br/> |<span data-ttu-id="3f629-109">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="3f629-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="3f629-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f629-110">Parameters</span></span>

 <span data-ttu-id="3f629-111">_FT1_</span><span class="sxs-lookup"><span data-stu-id="3f629-111">_ft1_</span></span>
  
> <span data-ttu-id="3f629-112">[in] Une structure [FILETIME](filetime.md) qui contient le premier entier non signé 64 bits à ajouter.</span><span class="sxs-lookup"><span data-stu-id="3f629-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="3f629-113">_ft2_</span><span class="sxs-lookup"><span data-stu-id="3f629-113">_ft2_</span></span>
  
> <span data-ttu-id="3f629-114">[in] Une structure FILETIME qui contient le deuxième entier 64 bits non signé à ajouter.</span><span class="sxs-lookup"><span data-stu-id="3f629-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="3f629-115">_pwCarry_</span><span class="sxs-lookup"><span data-stu-id="3f629-115">_pwCarry_</span></span>
  
> <span data-ttu-id="3f629-116">[entrée, sortie, facultatif] À l’entrée, un pointeur vers entrantes exécuter indicateur.</span><span class="sxs-lookup"><span data-stu-id="3f629-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="3f629-117">Dans la sortie, un pointeur vers le résultat de transport pour l’ajout.</span><span class="sxs-lookup"><span data-stu-id="3f629-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="3f629-118">Ce paramètre peut être NULL si le résultat de transport n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3f629-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3f629-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3f629-119">Return value</span></span>

<span data-ttu-id="3f629-120">La fonction **FtAdcFt** renvoie une structure **FILETIME** qui contient la somme de deux entiers.</span><span class="sxs-lookup"><span data-stu-id="3f629-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="3f629-121">Les deux paramètres d’entrée restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="3f629-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="3f629-122">Si **pwCarry** n’est pas NULL, il contient le résultat de transport pour les fonctions sum, 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="3f629-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3f629-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="3f629-123">Remarks</span></span>

<span data-ttu-id="3f629-124">La fonction **FtAdcFt** est identique à **FtAddFt** lorsque _pwCarry_ est NULL.</span><span class="sxs-lookup"><span data-stu-id="3f629-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="3f629-125">Si _pwCarry_ n’est pas NULL et points à 0, **FtAdcFt** renvoie la même valeur **FILETIME** qui renvoie **FtAddFt** .</span><span class="sxs-lookup"><span data-stu-id="3f629-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f629-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f629-126">See also</span></span>



[<span data-ttu-id="3f629-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="3f629-127">FtAddFt</span></span>](ftaddft.md)

