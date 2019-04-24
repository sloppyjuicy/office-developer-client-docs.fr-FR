---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f308c1f6f3cd2c9904dd94cd6761517bd5b410b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328020"
---
# <a name="ftadcft"></a><span data-ttu-id="03cd5-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="03cd5-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="03cd5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03cd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03cd5-105">Ajoute un entier non signé 64 bits à un autre, éventuellement à l'aide d'un indicateur de transport.</span><span class="sxs-lookup"><span data-stu-id="03cd5-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03cd5-106">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="03cd5-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="03cd5-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="03cd5-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="03cd5-108">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="03cd5-108">Called by:</span></span>  <br/> |<span data-ttu-id="03cd5-109">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="03cd5-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="03cd5-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03cd5-110">Parameters</span></span>

 <span data-ttu-id="03cd5-111">_FT1_</span><span class="sxs-lookup"><span data-stu-id="03cd5-111">_ft1_</span></span>
  
> <span data-ttu-id="03cd5-112">dans Une structure [fileTime](filetime.md) qui contient le premier entier non signé 64 bits à ajouter.</span><span class="sxs-lookup"><span data-stu-id="03cd5-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="03cd5-113">_ft2_</span><span class="sxs-lookup"><span data-stu-id="03cd5-113">_ft2_</span></span>
  
> <span data-ttu-id="03cd5-114">dans Une structure FILETIME qui contient le deuxième entier non signé 64 bits à ajouter.</span><span class="sxs-lookup"><span data-stu-id="03cd5-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="03cd5-115">_pwCarry_</span><span class="sxs-lookup"><span data-stu-id="03cd5-115">_pwCarry_</span></span>
  
> <span data-ttu-id="03cd5-116">[in, out, optional] En entrée, pointeur vers l'indicateur de transport entrant.</span><span class="sxs-lookup"><span data-stu-id="03cd5-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="03cd5-117">En sortie, pointeur vers le résultat du transport pour l'addition.</span><span class="sxs-lookup"><span data-stu-id="03cd5-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="03cd5-118">Ce paramètre peut être NULL si le résultat du transport n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="03cd5-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="03cd5-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="03cd5-119">Return value</span></span>

<span data-ttu-id="03cd5-120">La fonction **FtAdcFt** renvoie une structure **fileTime** qui contient la somme des deux entiers.</span><span class="sxs-lookup"><span data-stu-id="03cd5-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="03cd5-121">Les deux paramètres d'entrée restent inchangés.</span><span class="sxs-lookup"><span data-stu-id="03cd5-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="03cd5-122">Si **pwCarry** est non null, il contient le résultat de transport pour la somme, 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="03cd5-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="03cd5-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="03cd5-123">Remarks</span></span>

<span data-ttu-id="03cd5-124">La fonction **FtAdcFt** est identique à **FtAddFt** lorsque _pwCarry_ est null.</span><span class="sxs-lookup"><span data-stu-id="03cd5-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="03cd5-125">Si _pwCarry_ n'est pas null et pointe sur 0, **FtAdcFt** renvoie la même valeur **fileTime** que **FtAddFt** .</span><span class="sxs-lookup"><span data-stu-id="03cd5-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="03cd5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03cd5-126">See also</span></span>



[<span data-ttu-id="03cd5-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="03cd5-127">FtAddFt</span></span>](ftaddft.md)

