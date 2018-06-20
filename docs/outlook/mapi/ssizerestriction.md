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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 134eb844ef7b72d396c300b27a87a3a7ae320cf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787258"
---
# <a name="ssizerestriction"></a><span data-ttu-id="77eb7-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="77eb7-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="77eb7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="77eb7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="77eb7-105">Décrit une restriction de taille qui est utilisée pour tester la taille d’une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="77eb7-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77eb7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="77eb7-106">Header file:</span></span>  <br/> |<span data-ttu-id="77eb7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="77eb7-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="77eb7-108">Membres</span><span class="sxs-lookup"><span data-stu-id="77eb7-108">Members</span></span>

 <span data-ttu-id="77eb7-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="77eb7-109">**relop**</span></span>
  
> <span data-ttu-id="77eb7-110">Opérateur de relation qui est utilisé dans la comparaison de taille.</span><span class="sxs-lookup"><span data-stu-id="77eb7-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="77eb7-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="77eb7-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="77eb7-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="77eb7-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="77eb7-113">La comparaison est effectuée en fonction d’une première valeur supérieure ou égale.</span><span class="sxs-lookup"><span data-stu-id="77eb7-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="77eb7-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="77eb7-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="77eb7-115">La comparaison est effectuée en fonction d’une première valeur supérieure.</span><span class="sxs-lookup"><span data-stu-id="77eb7-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="77eb7-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="77eb7-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="77eb7-117">La comparaison est effectuée en fonction d’une première valeur inférieur ou égale.</span><span class="sxs-lookup"><span data-stu-id="77eb7-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="77eb7-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="77eb7-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="77eb7-119">La comparaison est effectuée en fonction d’une première valeur plus faible.</span><span class="sxs-lookup"><span data-stu-id="77eb7-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="77eb7-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="77eb7-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="77eb7-121">La comparaison est effectuée en fonction de comparaison.</span><span class="sxs-lookup"><span data-stu-id="77eb7-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="77eb7-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="77eb7-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="77eb7-123">La comparaison est effectuée en fonction de comme valeurs (expression régulière).</span><span class="sxs-lookup"><span data-stu-id="77eb7-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="77eb7-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="77eb7-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="77eb7-125">La comparaison est effectuée en fonction des valeurs égales.</span><span class="sxs-lookup"><span data-stu-id="77eb7-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="77eb7-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="77eb7-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="77eb7-127">Balise de propriété qui identifie la propriété à tester.</span><span class="sxs-lookup"><span data-stu-id="77eb7-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="77eb7-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="77eb7-128">**cb**</span></span>
  
> <span data-ttu-id="77eb7-129">Nombre d’octets de la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="77eb7-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77eb7-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="77eb7-130">Remarks</span></span>

<span data-ttu-id="77eb7-131">Pour une présentation générale du fonctionnement des restrictions, voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="77eb7-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="77eb7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77eb7-132">See also</span></span>



[<span data-ttu-id="77eb7-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="77eb7-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="77eb7-134">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="77eb7-134">MAPI Structures</span></span>](mapi-structures.md)

