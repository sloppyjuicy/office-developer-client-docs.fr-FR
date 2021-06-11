---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439085"
---
# <a name="ssizerestriction"></a><span data-ttu-id="caa01-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="caa01-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="caa01-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="caa01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="caa01-105">Décrit une restriction de taille utilisée pour tester la taille d’une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="caa01-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="caa01-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="caa01-106">Header file:</span></span>  <br/> |<span data-ttu-id="caa01-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="caa01-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="caa01-108">Members</span><span class="sxs-lookup"><span data-stu-id="caa01-108">Members</span></span>

 <span data-ttu-id="caa01-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="caa01-109">**relop**</span></span>
  
> <span data-ttu-id="caa01-110">Opérateur relationnel utilisé dans la comparaison de tailles.</span><span class="sxs-lookup"><span data-stu-id="caa01-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="caa01-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="caa01-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="caa01-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="caa01-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="caa01-113">La comparaison est réalisée en fonction d’une première valeur supérieure ou égale.</span><span class="sxs-lookup"><span data-stu-id="caa01-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="caa01-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="caa01-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="caa01-115">La comparaison est réalisée en fonction d’une première valeur supérieure.</span><span class="sxs-lookup"><span data-stu-id="caa01-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="caa01-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="caa01-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="caa01-117">La comparaison est réalisée sur la base d’une première valeur inférieure ou égale.</span><span class="sxs-lookup"><span data-stu-id="caa01-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="caa01-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="caa01-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="caa01-119">La comparaison est réalisée en fonction d’une première valeur inférieure.</span><span class="sxs-lookup"><span data-stu-id="caa01-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="caa01-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="caa01-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="caa01-121">La comparaison est basée sur des valeurs différentes.</span><span class="sxs-lookup"><span data-stu-id="caa01-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="caa01-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="caa01-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="caa01-123">La comparaison est réalisée en fonction des valeurs LIKE (expression régulière).</span><span class="sxs-lookup"><span data-stu-id="caa01-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="caa01-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="caa01-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="caa01-125">La comparaison est réalisée sur la base de valeurs égales.</span><span class="sxs-lookup"><span data-stu-id="caa01-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="caa01-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="caa01-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="caa01-127">Balise de propriété identifiant la propriété à tester.</span><span class="sxs-lookup"><span data-stu-id="caa01-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="caa01-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="caa01-128">**cb**</span></span>
  
> <span data-ttu-id="caa01-129">Nombre d’octets dans la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="caa01-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="caa01-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="caa01-130">Remarks</span></span>

<span data-ttu-id="caa01-131">Pour une discussion générale sur le fonctionnement des restrictions, voir [à propos des restrictions.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="caa01-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="caa01-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caa01-132">See also</span></span>



[<span data-ttu-id="caa01-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="caa01-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="caa01-134">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="caa01-134">MAPI Structures</span></span>](mapi-structures.md)

